---
title: サブジェクト権利要求のデータ一致
f1.keywords:
- CSH
ms.author: chvukosw
author: chvukosw
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
ms.localizationpriority: medium
ms.collection:
- M365-security-compliance
- M365-priva-subject-rights-requests
search.appverid:
- MOE150
- MET150
description: データ主体に関する追加情報を Microsoft Priva にアップロードする方法について説明します。
ms.openlocfilehash: 90ee0e8e21d25954c11113992cbb7ece847c85ab
ms.sourcegitcommit: 6b88d22d0250cbb9a4ba1f71665f29cb67939851
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/05/2022
ms.locfileid: "65059741"
---
# <a name="data-matching-for-subject-rights-requests"></a>サブジェクト権利要求のデータ一致

データ照合を使用すると、組織は Microsoft Priva が正確に指定されたデータ値に基づいてデータ主体を識別できるようにします。 これにより、内部担当者と対話する外部ユーザーの両方に対して、それらのデータ値に対応するデータ主体のコンテンツを特定する精度を高めることができます。 また、サブジェクト権利要求の作成時にフィールドを手動で指定する必要性が簡素化され、サブジェクトの権利要求内と、最も多くのデータ 主体コンテンツを含むアイテムを示す [概要] タイルのコンテキストが提供されます。 このビューの詳細については、「 [Priva で個人データを検索して視覚化する](priva-data-profile.md#items-with-the-most-data-subject-content)」を参照してください。

データ照合機能を使用するには、Privacy Management ロール グループのメンバーである必要があります。 [Microsoft Purview コンプライアンス ポータル](https://compliance.microsoft.com/)の Priva 内から、上部のナビゲーションで **設定** を選択し、**データ照合** を選択します。 ここから、個人データ スキーマを定義し、次に示すように個人データのアップロードを提供する必要があります。 アイテムは追加でき、追加したアイテムは削除できますが、アイテムを変更することはできません。

## <a name="prepare-for-data-import"></a>データインポートの準備

スキーマを定義したり、データをアップロードしたりする前に、データ主体の情報のソースを特定する必要があります。 必要なファイル形式は.csvであり、Microsoft Excelなどのアプリケーションで読み取ることができます。 列ヘッダーが最初の行に表示されるように、このエクスポートを構造化します。 これらのヘッダーには、個人データ スキーマの属性の名前を含める必要があります。 各フィールドのデータの形式を確認します。 いずれかのデータにコンマが含まれている場合は、これらの値を二重引用符で囲んで、個別のフィールドに解析されないようにします。

## <a name="define-the-personal-data-schema"></a>個人データ スキーマを定義する

データ照合を設定する最初の手順は、個人データ スキーマを定義することです。このスキーマでは、データ主体の属性について説明します。 このスキーマは、データ照合設定領域の最初のタブにアップロードします。 必要なファイルには、 **個人用データ スキーマ** XML ファイルと **ルール パッケージ** XML ファイルが含まれます。

### <a name="personal-data-schema-xml"></a>個人データ スキーマ XML

個人データ スキーマ ファイルは、必要な列名を定義する XML ファイルです。

- このスキーマ ファイル *pdm.xml* に名前を付けます。
- 次の例に示すように、フィールド名タグを使用して各列名を定義します。
- 検索可能なフィールドには、最大 5 つのフィールドまで検索可能 = "true" を使用します。 フィールド名の少なくとも 1 つは検索可能である必要があります。 サンプル構文: `\<Field name="" searchable=""/>`.
- 個人用データ スキーマには、DataStore タグ セクションがあります。 フィールド名には、primaryKeyField、upnField、firstNameField、lastNameField の 4 つの必須フィールドをマップする必要があります。

例として、次の XML ファイルでは、検索可能な 5 つのフィールド (PatientID、MRN、SSN、電話、DOB) が指定されたサンプル スキーマが定義されています。 primaryKeyField は PatientID にマップされ、upnField は MRN にマップされ、firstNameField は FirstName にマップされ、lastNameField は LastName にマップされます。

この例は、コピー、変更、使用が可能です。

 ```xml
<PdmSchema xmlns="http://schemas.microsoft.com/office/2020/pdm">
      <DataStore name="Patientrecords" description="Schema for patient records" version="1" primaryKeyField="PatientID" upnField="MRN" firstNameField="FirstName" lastNameField="LastName">
            <Field name="PatientID" searchable="true"/>
            <Field name="MRN" searchable="true" />
            <Field name="FirstName" />
            <Field name="LastName" />
            <Field name="SSN" searchable="true" />
            <Field name="Phone" searchable="true" />
            <Field name="DOB" searchable="true" />
            <Field name="Gender" />
            <Field name="Address" />
      </DataStore>
</PdmSchema>
 ```

### <a name="rule-package-xml"></a>ルール パッケージ XML

ルール パッケージを設定するときは、上記で作成した個人データ スキーマ ファイルを正しく参照してください:pdm.xml。 次のルール パッケージ XML のサンプルでは、データ一致の機密型を作成するために、次のフィールドをカスタマイズする必要があります。

- **RulePack ID** & **PrivacyMatch ID**: New-GUID を使用して GUID を生成します。
- **データストア**: このフィールドは、使用する個人データ一致参照データ ストアを指定します。 構成された個人データ スキーマの定義済みの DataStore 名を指定します。
- **idMatch**: このフィールドは、個人データ一致の主な要素を指します。
  - **一致**: 完全参照で使用するフィールドを指定します。 個人データ スキーマから検索可能なフィールド名を指定します。
  - **分類**: このフィールドは、個人データ一致検索をトリガーする機密型一致を指定します。 既存の組み込みまたはカスタムの機密情報の種類の名前または GUID を指定できます。 パフォーマンスの問題を回避するために、個人データ一致の分類要素としてカスタム機密情報の種類を使用する場合は、コンテンツの大きな割合 ("任意の数値" や "任意の 5 文字の単語" など) に一致するカスタムの機密情報の種類を使用しないでください。 サポート キーワードを追加するか、カスタム分類の機密情報の種類の定義に書式設定を含めることをお勧めします。
- **一致**: このフィールドは、idMatch の近くで見つかった追加の証拠を指します。
  - **一致**: DataStore の個人用データ スキーマにフィールド名を指定します。
- **リソース**: このセクションでは、複数のロケールで機密性の高い型の名前と説明を指定します。
  - **idRef**: ExactMatch ID の GUID を指定します。
  - **名前&説明**: 必要に応じてカスタマイズします。

以下のルール パッケージ XML の例では、個人用データ スキーマ XML を作成する前の手順のpdm.xmlサンプル ファイルを参照しています。

- **データストア**: dataStore 名は、前に作成したスキーマ ファイルを参照します。dataStore = "PatientRecords" です。
- **idMatch**: idMatch 値は、前に作成したpdm.xml ファイルに一覧表示されている検索可能なフィールドを参照します。idMatch は ="SSN" と一致します。
  - **分類**: 分類値は、既存またはカスタムの機密情報の種類を参照します。分類 = "米国社会保障番号 (SSN)" です。 (この場合は、既存の機密情報の種類の米国社会保障番号を使用します。)

次のコード例のように、(Unicode エンコードを使用して) XML 形式でルール パッケージを作成します。 この例は、コピー、変更、および使用できます。

 ```xml
<RulePackage xmlns="http://schemas.microsoft.com/office/2020/pdm">
  <RulePack id="fd098e03-1796-41a5-8ab6-198c93c62b21">
    <Version build="0" major="2" minor="0" revision="0" />
    <Publisher id="eb553734-8306-44b4-9ad5-c388ad970528" />
    <Details defaultLangCode="en-us">
      <LocalizedDetails langcode="en-us">
        <PublisherName>IP DLP</PublisherName>
        <Name>Health Care PDM Rulepack</Name>
        <Description>This rule package contains the Personal Data Match sensitive type for health care sensitive types.</Description>
      </LocalizedDetails>
    </Details>
  </RulePack>
  <Rules>
    <PrivacyMatch id = "E1CC861E-3FE9-4A58-82DF-4BD259EAB381" patternsProximity = "300" dataStore ="PatientRecords" recommendedConfidence = "65" >
      <Pattern confidenceLevel="65">
        <idMatch matches = "SSN" classification = "U.S. Social Security Number (SSN)" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <idMatch matches = "SSN" classification = "U.S. Social Security Number (SSN)" />
        <Any minMatches ="3" maxMatches ="6">
          <match matches="PatientID" />
          <match matches="MRN"/>
          <match matches="FirstName"/>
          <match matches="LastName"/>
          <match matches="Phone"/>
          <match matches="DOB"/>
        </Any>
      </Pattern>
    </PrivacyMatch>
    <LocalizedStrings>
      <Resource idRef="E1CC861E-3FE9-4A58-82DF-4BD259EAB381">
        <Name default="true" langcode="en-us">Patient SSN Exact Match.</Name>
        <Description default="true" langcode="en-us">PDM Sensitive type for detecting Patient SSN.</Description>
      </Resource>
    </LocalizedStrings>
  </Rules>
</RulePackage>
 ```

## <a name="sensitive-info-types"></a>機密情報の種類

データ照合を設定する 2 番目の手順は、個人データ一致 (PDM) に対して一意の機密情報の種類を作成することです。 [機密情報の種類 (SIT)は](/microsoft-365/compliance/sensitive-information-type-learn-about)、社会保障やクレジット カード番号などの機密情報を検出するパターン ベースの分類子です。 PFX の機密情報の種類を設定すると、一致を検出するために一般的な値ではなく正確なデータ値を使用できます。 この手順を開始するには、[ **PFX 機密情報の種類の作成** ] を選択して作成ウィザードを開始します。

## <a name="upload-personal-data"></a>個人データのアップロード

個人データ スキーマと機密情報の種類を定義した後、3 番目の手順は個人データをアップロードすることです。 **[個人用データのアップロード**] タブに移動し、[**追加]** を選択し、最初の手順で定義した個人用スキーマを選択してから、個人データを含むファイルをアップロードします。

この個人データをアップロードするには、ローカル ファイルを選択するか、個人データ ファイルを含む既存のMicrosoft Azure Storageの場所に SAS URL を指定します。
作成されたスキーマに準拠するこのプロセスの最初の手順としてファイルを準備した場合は、そのファイルをアップロードに使用できます。

## <a name="legal-disclaimer"></a>法的免責事項

[Microsoft Priva の法的免責事項](priva-disclaimer.md)

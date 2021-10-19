---
title: プライバシー管理でサブジェクト権限要求のデータ一致を管理する
f1.keywords:
- CSH
ms.author: v-jgriffee
author: jmgriffee
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
ms.localizationpriority: medium
ms.collection:
- M365-security-compliance
- M365-privacy-management
search.appverid:
- MOE150
- MET150
description: データ主体に関する追加情報をプライバシー管理にアップロードする方法について説明します。
ms.openlocfilehash: 00a902705336d766993e805d78609a48334b2bf6
ms.sourcegitcommit: 85e085eb17af8b4efd1f45207445e1b3c3679600
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/19/2021
ms.locfileid: "60478394"
---
# <a name="manage-data-matching-for-subject-rights-requests"></a>サブジェクト権限要求のデータ一致を管理する

データ照合を使用すると、組織は、提供された正確なデータ値に基づいてデータ主体を識別するプライバシー管理を有効にできます。 これにより、内部担当者と操作する外部ユーザーの両方のデータ値に対応するデータ主体コンテンツを検索する精度を高めることができます。 また、サブジェクト権限要求の作成中にフィールドを手動で指定する必要性が簡素化され、件名の権利要求内のコンテキストと、最も多くのデータ主体コンテンツを持つアイテムを紹介する [概要] タイルが提供されます。 そのビューの詳細については、「データを検索して [視覚化する」を参照してください](privacy-management-data-profile.md#items-with-the-most-data-subject-content)。

データ照合機能を使用するには、プライバシー管理役割グループのメンバーである必要があります。 [プライバシー管理] の [Microsoft 365 コンプライアンス センター] から設定ナビゲーションで [データの一致]**を選択します**。 [](https://compliance.microsoft.com/) ここから、以下に示すように、個人データ スキーマを定義し、個人データのアップロードを提供する必要があります。 アイテムを追加したり、UI を使用して追加したアイテムを削除したりできる点に注意してください。 ただし、現時点では UI からアイテムを変更することはできません。

## <a name="prepare-for-data-import"></a>データインポートの準備

スキーマを定義するか、データをアップロードする前に、データ主体情報のソースを特定する必要があります。 必要なファイル形式は、.csvなどのアプリケーションで読み取Microsoft Excel。 列ヘッダーを最初の行に表示するには、このエクスポートを構成します。 これらのヘッダーには、個人データ スキーマの属性の名前を含める必要があります。 各フィールドのデータの形式を確認します。 データにコンマが含まれている場合は、これらの値を二重引用符で囲み、個別のフィールドに解析されません。

## <a name="define-the-personal-data-schema"></a>個人データ スキーマの定義

個人データ スキーマは、データ主体の属性を記述します。 アップロード一致する設定領域の最初のタブで、このスキーマを選択します。 必要なファイルには、個人 **データ スキーマ** XML ファイルとルール パッケージ XML **ファイルが** 含まれます。

### <a name="personal-data-schema-xml"></a>個人データ スキーマ XML

個人データ スキーマ ファイルは、必要な列名を定義する XML ファイルです。

- このスキーマ ファイルに名前を *付pdm.xml。*
- 次の例に示す Field Name タグを使用して、各列名を定義します。
- 検索可能なフィールドには、最大 5 つのフィールドまで検索可能 = "true" を使用します。 少なくとも 1 つのフィールド名が検索可能である必要があります。 サンプル構文: `\<Field name="" searchable=""/>` .
- 個人データ スキーマには、DataStore タグ セクションがあります。 4 つの必須フィールドをフィールド名にマップする必要があります。primaryKeyField、upnField、firstNameField、lastNameField。

例として、次の XML ファイルはサンプル スキーマを定義し、5 つのフィールドを検索可能として指定します。PatientID、MRN、SSN、電話、DOB です。 primaryKeyField は PatientID にマップされ、upnField は MRN にマップされ、firstNameField は FirstName にマップされ、lastNameField は LastName にマップされます。

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

ルール パッケージを設定する場合は、上記で作成した個人データ スキーマ ファイルを正しく参照してください。pdm.xml。 次のルール パッケージ XML のサンプルでは、データ一致の機密情報の種類を作成するために、次のフィールドをカスタマイズする必要があります。

- **RulePack id**  & **PrivacyMatch ID**: New-GUID を使用して GUID を生成します。
- **データストア**: このフィールドは、使用する個人データ一致参照データ ストアを指定します。 構成済みの個人データ スキーマの定義済みの DataStore 名を指定します。
- **idMatch**: このフィールドは、個人データの一致のプライマリ要素をポイントします。
  - **一致**: 正確な参照で使用するフィールドを指定します。 個人データ スキーマから検索可能なフィールド名を指定します。
  - **分類**: このフィールドは、個人データの一致参照をトリガーする機密の種類の一致を指定します。 既存の組み込みまたはカスタムの機密情報の種類の名前または GUID を指定できます。 パフォーマンスの問題を回避するために、個人データの分類要素としてカスタム機密情報の種類を使用する場合は、コンテンツの大きな割合 ("any number" や "任意の 5 文字の単語" など) に一致するカスタム機密情報の種類を使用しません。 サポート キーワードを追加するか、カスタム分類機密情報の種類の定義に書式を含めてお勧めします。
- **一** 致 : このフィールドは、idMatch の近接で見つかった追加の証拠を示します。
  - **一致**: DataStore の個人データ スキーマに任意のフィールド名を指定します。
- **リソース**: このセクションでは、複数の地域で機密型の名前と説明を指定します。
  - **idRef**: ExactMatch ID の GUID を指定します。
  - **名前&説明:** 必要に応じてカスタマイズします。

以下のルール パッケージ XML の例では、個人データ スキーマ XML をpdm.xml前の手順のサンプル ファイルを参照しています。

- **データストア**: dataStore 名は、以前に作成したスキーマ ファイルを参照します。dataStore = "PatientRecords" です。
- **idMatch**: idMatch 値は、前に作成した pdm.xml ファイルにリストされている検索可能なフィールドを参照します。idMatch 一致 = "SSN" です。
  - **分類**: 分類値は、既存またはカスタムの機密情報の種類を参照します。分類 = "米国社会保障番号 (SSN)")。 (この場合は、既存の機密情報の種類の米国社会保障番号を使用します。)

次のコード例のように、XML 形式 (Unicode エンコード付き) でルール パッケージを作成します。 この例では、コピー、変更、および使用できます。

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

## <a name="upload-personal-data"></a>アップロードデータの取得
個人データ スキーマを定義した後、データ一致設定ページの 2 番目のタブで個人データのアップロードを実行できます。 [追加] **を選択** すると、最初の手順で定義した個人用スキーマを選択し、個人データを含むファイルをアップロードします。

この個人データをアップロードするには、ローカル ファイルを選択するか、個人データ ファイルを含む既存Microsoft Azure Storage場所に SAS URL を指定します。
作成したスキーマに準拠するファイルをこのプロセスの最初の手順として準備した場合は、そのファイルをアップロードに使用できます。

## <a name="legal-disclaimer"></a>法的免責事項

[プライバシー管理の法的免責事項](privacy-management-disclaimer.md)

---
title: レポートを生成し、件名の権利要求を満たす
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
description: サブジェクト権限要求用に Microsoft Priva によって作成されたデータ パッケージを管理し、データ主体への要求を満たす方法について説明します。
ms.openlocfilehash: 8a6a41188de78508401b0dfffb3d7cdefb2320a5
ms.sourcegitcommit: 4965df24fdc907f7a6e397f2c78019aaf72c7580
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/17/2022
ms.locfileid: "63564447"
---
# <a name="generate-reports-and-fulfill-a-subject-rights-request"></a>レポートを生成し、件名の権利要求を満たす

Microsoft Priva でサブジェクト権限要求のデータ レビューを完了した後、フルフィルメントを要求できます。 Priva はレポートを作成し、データ レビュー プロセス中に **Include のマークが** 付いたファイルを収集します。 これらのデータ パッケージから選択したファイルは、要求を完了するためにデータ主体に送信できます。 また、Priva は、Microsoft 365権限要求 API を活用して自動化機能を導入することもできます。

## <a name="understanding-reports"></a>レポートについて

サブジェクト権限要求 **の [** データの確認] ステージで [レビューの完了] を選択すると、要求の最終レポートが自動的に生成されます。 件名の **権利要求** の詳細ページの [レポート] タブで、[状態] 列は、レポートの生成が進行中で、レポートがダウンロード可能な状態を **示します**。 レポートの作成が完了するには、最大で 30 分かかる場合があります。

レポートは、次の 2 つのセクションに分かれています。
1. **データ主体のレポート**: これらのレポートには、要求のフルフィルメントの一環としてデータ主体に返される情報が含まれる。 ここでは、データ主体に送信するファイルを含むデータ パッケージを見つける場所です。
   > [!IMPORTANT]
   > データ パッケージは、データ レビュー中にアイテムを Include としてマーク **した** 場合にのみ生成されます。

   > [!IMPORTANT]
   > データ パッケージは、エクスポートおよびアクセス **の** 種類 **の要求にのみ** 生成されます。 データ パッケージは、フォローアップ要求の **タグ付きリストに対して生成** されません。 件名の要求 [の種類に関する詳細を確認します](subject-rights-requests-create.md#use-the-subject-rights-request-creation-wizard)。

2. **内部使用のレポート**: これらのレポートは、サブジェクト権限要求に関連する組織の内部レコード用です。 監査ログと、データレビュー中にタグを適用したファイルの一覧が含まれます。

## <a name="prepare-final-reports-for-the-data-subject"></a>データ主体の最終レポートを準備する

サブジェクト権限要求データ パッケージは、zip ファイルとして生成されます。 このパッケージを生成するには、最大 30 分かかる場合があります。 準備ができたら、[件名の権利の要求] ページから件名の権利要求を開き、[レポート]  タブを開き、ダウンロードを見つけて、zip ファイルを開きます。

データ パッケージには、さまざまなファイルが含まれています。 Azure フォルダー外のファイルは参照用に提供され、主に管理者が使用する必要があります。 データ主体の主要な資料は、Azure フォルダーに **含** まれている。

このフォルダーの内容を注意深く確認し、必要なファイルのみをデータ主体に提出することをお勧めします。 対応を評価して、適用される法律の要件を満たした要件に合わせて調整する必要があります。

### <a name="azure-folder-contents"></a>Azure フォルダーの内容

このフォルダーを開き、ファイルを **開AEDExport.zip** します。 コンテンツには、次のものが含まれます。

- [ **Extracted_text_files** ] フォルダーには、ネイティブ ファイル (サポートされている場合) から抽出されたテキストが含まれる。
- **NativeFiles フォルダーには**、ネイティブ ファイル形式 **のすべての含** まれるアイテムが含まれます。
- やり直されたファイルは **NativeFiles** フォルダーにあり、接尾辞 "_burn.pdf" を付_burn.pdf。
- エクスポートされたファイルの名前は、個人データの保護に役立つ一意の識別子を使用して変更されます。 一意の名前を元のファイル名と相互参照するには、次の **Export_load_file.csv。** 元のファイル名には機密情報が含まれる場合があります。この情報に適用されるポリシーに従う必要があります。

zip ファイルの内容を確認した後、必要に応じて変更して、最終パッケージに含めたくないコンテンツを削除します。 完了したら、データ主体に安全に送信します。

## <a name="integrate-with-partner-solutions"></a>パートナー ソリューションとの統合

Priva Subject Rights Requests ソリューションを既存のビジネス プロセスおよびツールと統合するには、Microsoft 365 Subject Rights 要求 API を使用します。 API を使用すると、簡単かつ強力な方法で、件名の権利戦略に自動化を導入できます。

データ主体が組織から情報を要求する場合、API は、要求の一意の条件に基づいて、Microsoft 365内でこれらの要求を作成するのに役立ちます。 Microsoft 365 でサブジェクト権限要求を作成し、そのステージを通じて要求の進捗状況を追跡し、要求が処理を完了し、コンテンツが取得する準備ができていることを確認できます。 この API は、ISV、パートナーがソリューションで Microsoft 365 に対応する場合、または組織がビジネス アプリケーションで使用する場合など、ソリューションの拡張性を高め、誰でも使用できます。

詳細については、「Use [the Microsoft Graphアクセス権要求 API」を参照してください](/graph/api/resources/subjectrightsrequest-subjectrightsrequestapioverview)。

## <a name="manage-data-retention"></a>データ保持の管理

このツールを使用して生成されたレポートと、Azure に保存された注釈付きファイルなどの関連データは、指定された時間保存されます。 データ保持期間は **Priva 設定** 定義され、すべてのサブジェクト権限要求に適用されます。 データ保持期間を表示または変更するには、次の手順に従います。

1. Priva Subject Rights Requests のどこからでも、画面 **設定** 右上隅にある [歯車] (歯車アイコン) を選択します。
2. 左側 **のナビゲーションで [データ保持期間** ] を選択します。
3. ドロップダウン メニューを使用して、保持期間として 30 日または 90 日のいずれかを選択します。

選択したデータ保持期間が組織のポリシーと法的義務に準拠している必要があります。

## <a name="legal-disclaimer"></a>法的免責事項

[Microsoft Priva の法的免責事項](priva-disclaimer.md)

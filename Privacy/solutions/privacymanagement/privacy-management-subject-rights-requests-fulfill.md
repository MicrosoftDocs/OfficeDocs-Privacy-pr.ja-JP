---
title: プライバシー管理で件名の権利要求レポートを管理し、要求を満たす
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
description: プライバシー管理によって作成されたデータ パッケージをサブジェクト権限要求に対して管理し、データ主体に対する要求を満たす方法について説明します。
ms.openlocfilehash: 424bb4edc6ddcab86200d76cee767bc9699b281a
ms.sourcegitcommit: 85e085eb17af8b4efd1f45207445e1b3c3679600
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/19/2021
ms.locfileid: "60478195"
---
# <a name="manage-subject-rights-requests-reports-and-fulfill-requests"></a>件名の要求レポートを管理し、要求を満たす

サブジェクト権限要求のデータ レビューを完了すると、フルフィルメントを要求できます。 プライバシー管理は、レポートを作成し、データ レビュー プロセス中に Include の **マークが** 付いたファイルを収集します。 これらのデータ パッケージから選択したファイルは、要求を完了するためにデータ主体に送信できます。 また、プライバシー管理は、Microsoft 365権限要求 API を活用して自動化機能を導入することもできます。

## <a name="prepare-final-reports-for-the-data-subject"></a>データ主体の最終レポートを準備する

サブジェクト権限要求データ パッケージは、zip ファイルとして生成されます。 このパッケージを生成するには、最大 30 分かかる場合があります。 準備ができたら、[件名の権利の要求] ページから件名の権利要求を開き、[レポート] タブを開き、ダウンロードを見つけて、zip ファイルを開きます。

データ パッケージには、さまざまなファイルが含まれています。 Azure フォルダー外のファイルは参照用に提供され、主に管理者が使用する必要があります。 データ主体の主要な資料は **、Azure** フォルダーに含まれている。

このフォルダーの内容を注意深く確認し、必要なファイルのみをデータ主体に提出することをお勧めします。 対応を評価して、適用される法律の要件を満たした対応に合わせて調整する必要があります。

### <a name="azure-folder-contents"></a>Azure フォルダーの内容

このフォルダーを開き、ファイルを **開AEDExport.zip** します。 コンテンツには、次のものが含まれます。

- **[Extracted_text_files]** フォルダーには、ネイティブ ファイル (サポートされている場合) から抽出されたテキストが含まれる。
- **NativeFiles フォルダーには**、ネイティブ ファイル形式 **のすべての含** まれるアイテムが含まれます。
- 編集されたファイルは **NativeFiles** フォルダーにあり、接尾辞は "_burn.pdf" です。
- エクスポートされたファイルの名前は、個人データの保護に役立つ一意の識別子を使用して変更されます。 一意の名前を元のファイル名と相互参照するには、次の **Export_load_file.csv。** 元のファイル名には機密情報が含まれる場合があります。この情報に適用されるポリシーに従う必要があります。

zip ファイルの内容を確認した後、必要に応じて変更して、最終パッケージに含めたくないコンテンツを削除します。 完了したら、データ主体に安全に送信します。

## <a name="integrate-with-partner-solutions"></a>パートナー ソリューションとの統合

サブジェクト権限要求 API をMicrosoft 365して、既存のビジネス プロセスおよびツールと Microsoft 365統合できます。 これにより、件名の権利戦略にオートメーションを導入するための簡単かつ強力な方法が提供されます。

データ主体が組織から情報を要求する場合、API を活用して、その要求にカスタムの条件に基づいて、Microsoft 365 内にそれらの要求を作成できます。 Microsoft 365 でサブジェクト権限要求を作成し、そのステージを通じて要求の進捗状況を追跡し、要求が処理を完了し、コンテンツが取得する準備ができていることを確認できます。 この API は、ISV、パートナーがソリューションで Microsoft 365 に対応する場合、または組織がビジネス アプリケーションで使用する場合など、ソリューションの拡張性を高め、誰でも使用できます。

詳細については、「Use [the Microsoft Graphサブジェクト権限要求 API」を参照してください](/graph/api/resources/subjectrightsrequest-subjectrightsrequestapioverview)。

## <a name="manage-data-retention"></a>データ保持の管理

このツールを使用して生成されたレポートと、Azure に保存された注釈付きファイルなどの関連データは、指定された時間保存されます。 この期間は、[データ保持期間] セクション **設定を通** じてグローバルレベルで定義され、30 日から 90 日間の間で選択できます。 これらのデータ保持期間がポリシーおよび法的義務に準拠している必要があります。

## <a name="legal-disclaimer"></a>法的免責事項

[プライバシー管理の法的免責事項](privacy-management-disclaimer.md)

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
ms.openlocfilehash: 861a08b1f2ca5b3f82546c54db16c4518a8e9a70
ms.sourcegitcommit: f145dff5e387a8e26db2f3a2c7de125978fbacc9
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/28/2022
ms.locfileid: "62249205"
---
# <a name="generate-reports-and-fulfill-a-subject-rights-request"></a>レポートを生成し、件名の権利要求を満たす

Microsoft Priva でサブジェクト権限要求のデータ レビューを完了した後、フルフィルメントを要求できます。 Priva はレポートを作成し、データ レビュー プロセス中に **Include のマークが** 付いたファイルを収集します。 これらのデータ パッケージから選択したファイルは、要求を完了するためにデータ主体に送信できます。 また、Priva は、Microsoft 365権限要求 API を活用して自動化機能を導入することもできます。

## <a name="prepare-final-reports-for-the-data-subject"></a>データ主体の最終レポートを準備する

サブジェクト権限要求データ パッケージは、zip ファイルとして生成されます。 このパッケージを生成するには、最大 30 分かかる場合があります。 準備ができたら、[件名の権利の要求] ページから件名の権利要求を開き、[レポート]  タブを開き、ダウンロードを見つけて、zip ファイルを開きます。

データ パッケージには、さまざまなファイルが含まれています。 Azure フォルダー外のファイルは参照用に提供され、主に管理者が使用する必要があります。 データ主体の主要な資料は、Azure フォルダーに **含** まれている。

このフォルダーの内容を注意深く確認し、必要なファイルのみをデータ主体に提出することをお勧めします。 対応を評価して、適用される法律の要件を満たした要件に合わせて調整する必要があります。

### <a name="azure-folder-contents"></a>Azure フォルダーの内容

このフォルダーを開き、ファイルを **開AEDExport.zip** します。 コンテンツには、次のものが含まれます。

- [ **Extracted_text_files** ] フォルダーには、ネイティブ ファイル (サポートされている場合) から抽出されたテキストが含まれる。
- **NativeFiles フォルダーには**、ネイティブ ファイル形式 **のすべての含** まれるアイテムが含まれます。
- やり直されたファイルは **NativeFiles フォルダーにあり** 、接尾辞 "_burn.pdf" を付_burn.pdf。
- エクスポートされたファイルの名前は、個人データの保護に役立つ一意の識別子を使用して変更されます。 一意の名前を元のファイル名と相互参照するには、次のコマンドを **使用Export_load_file.csv**。 元のファイル名には機密情報が含まれる場合があります。この情報に適用されるポリシーに従う必要があります。

zip ファイルの内容を確認した後、必要に応じて変更して、最終パッケージに含めたくないコンテンツを削除します。 完了したら、データ主体に安全に送信します。

## <a name="integrate-with-partner-solutions"></a>パートナー ソリューションとの統合

Priva Subject Rights Requests ソリューションを既存のビジネス プロセスおよびツールと統合するには、Microsoft 365 Subject Rights 要求 API を活用します。 これにより、件名の権利戦略にオートメーションを導入するための簡単かつ強力な方法が提供されます。

データ主体が組織から情報を要求する場合、API を活用して、その要求にカスタムの条件に基づいて、Microsoft 365 内にそれらの要求を作成できます。 Microsoft 365 でサブジェクト権限要求を作成し、そのステージを通じて要求の進捗状況を追跡し、要求が処理を完了し、コンテンツが取得する準備ができていることを確認できます。 この API は、ISV、パートナーがソリューションで Microsoft 365 に対応する場合、または組織がビジネス アプリケーションで使用する場合など、ソリューションの拡張性を高め、誰でも使用できます。

詳細については、「Use [the Microsoft Graphサブジェクト権限要求 API」を参照してください](/graph/api/resources/subjectrightsrequest-subjectrightsrequestapioverview)。

## <a name="manage-data-retention"></a>データ保持の管理

このツールを使用して生成されたレポートと、Azure に保存された注釈付きファイルなどの関連データは、指定された時間保存されます。 この期間は、[データ保持期間] セクション設定を通じてグローバル レベルで定義され、30 日から 90 日の間で選択できます。 これらのデータ保持期間がポリシーおよび法的義務に準拠している必要があります。

## <a name="legal-disclaimer"></a>法的免責事項

[Microsoft Priva の法的免責事項](priva-disclaimer.md)

---
title: サブジェクト権利要求でのデータの見積もりと取得
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
description: データの取得方法と、Microsoft Priva 主体の権利要求の検索設定を変更する方法について説明します。
ms.openlocfilehash: a2586e987f7a03905feedfd587aab43dba3d9e6b
ms.sourcegitcommit: 8cbafebb1a1b26a0bd92e500a1e6d6c60243c64b
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/20/2022
ms.locfileid: "66166666"
---
# <a name="data-estimate-and-retrieval"></a>データの推定と取得

**この記事では**、サブジェクト権利要求のデータの見積もりとデータ取得ステージについて説明します。 要求の検索クエリを表示し、検索を絞り込むための編集を行う方法について説明します。

## <a name="data-estimate"></a>データの見積もり
要求を作成すると、PrivaはMicrosoft 365環境内のコンテンツ内のデータ主体に対する一致の検索をすぐに開始します。 条件に一致すると考えるすべての項目が特定されると、要求の **[概要**] ページの **[データの見積もり概要**] カードに見積もりが表示されます。 検索範囲内のデータの量は、見積もりの完了に要する時間の長さに影響します。

要求は、 **データの取得** の次の段階に自動的に移動し、関係者がデータのレビューに関して共同作業するためにすべてのコンテンツ項目がまとめられます。 場合によっては、取得に移る前にデータの見積もりを一時停止し、続行する前に次の手順について通知します。

### <a name="pause-in-data-estimate"></a>データ見積もりの一時停止

**データ見積もり** 段階で要求が一時停止する理由は 2 つあります。

1. 要求を作成するときに、最初に見積もりを取得することを選択できます。 詳細については、 [カスタム要求を作成する](subject-rights-requests-create.md#custom-setup-guided-process-to-choose-all-settings) 手順 6 を参照してください。

2. 見積もりで確認する項目の数が多い (10,000 件を超える) 場合、ワークフローは一時停止します。 この時点で、結果をプレビューし、 [検索クエリを編集](subject-rights-requests-create.md#refining-your-search) するか、引き続き識別されたアイテムを取得するかを決定できます。

**データの見積もり** で要求が一時停止されると、要求の詳細ページにカードが表示され、アイテムの数、ボリューム、場所、および **検索クエリの詳細を表示** するためのリンクに関する概要情報が表示されます。

![データ見積もりカード。](../media/priva-srr-data-estimate.png)

## <a name="view-and-edit-search-queries"></a>検索クエリを表示および編集する

要求の検索に関する詳細情報を表示するには、**データ見積もりの概要** カードで **検索クエリの詳細を表示** するを選択します。 ポップアップ ウィンドウが開き、クエリが要約され、検出された内容の詳細が表示されます。 ここから、次のオプションを使用できます。

- [ **結果のプレビュー** ] を選択して、現在の検索設定で返されるコンテンツの種類のプレビューを取得します。
- [ **検索クエリの編集] を** 選択して、検索設定を変更します。

**[検索クエリの編集]** を選択すると、ガイド付きプロセスに従ってプロパティを変更または追加し、データ主体を識別し、条件を変更し、検索対象の場所を調整します。 詳細については、検索の [絞り込みの](subject-rights-requests-create.md#refining-your-search) 手順に従ってください。 新しい検索クエリの最終バージョンを確認し、[ **保存]** を選択して、もう一度検索を開始できます。

新しい見積もりが生成され、要求の状態が **データの見積もり** に戻ります。 新しい検索が完了するまでに最大 60 分かかる場合があります。 完了すると、要求の詳細ページに更新された結果が表示されます。

続行する準備ができたら、画面の右上にある [ **データの取得** ] を選択して、データ取得ステージに進みます。

## <a name="retrieve-data"></a>データを取得する

データ取得ステージは、データ主体の個人データを含むすべてのファイル、電子メール、チャット、画像、およびその他のコンテンツ 項目が取得されるときに行われます。 項目は、レビューのためにAzure Blob Storage コンテナーにまとめされます。 データの量によっては、データの取得に数分または大幅に時間がかかる場合があります。

このステージが完了すると、要求は **自動的にレビュー データ** の次のステージに移動します。

## <a name="next-steps"></a>次の手順

主なタスクと関係者との共同作業について詳しくは [、サブジェクト権利要求のデータの確認](subject-rights-requests-data-review.md) に関するページ **をご覧** ください。

## <a name="legal-disclaimer"></a>法的免責事項

[Microsoft Priva法的免責事項](priva-disclaimer.md)
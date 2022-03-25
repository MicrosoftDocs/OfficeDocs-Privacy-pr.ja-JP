---
title: Priva の設定を構成する
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
- M365-priva-privacy-risk-management
search.appverid:
- MOE150
- MET150
description: Microsoft Priva のグローバル設定オプションについて説明します。
ms.openlocfilehash: d1e19ffc587f346c5ca1b414a772649342cdccaa
ms.sourcegitcommit: beeb693075ef692e95d679f366301df8517b2ac3
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/23/2022
ms.locfileid: "63765490"
---
# <a name="configure-priva-settings"></a>Priva の設定を構成する

画面の右上隅にある歯車アイコンを選択すると、Microsoft Priva の設定を管理できます。 ここでのオプションを使用すると、高レベルの基本設定を設定し、キー プロパティをカスタマイズできます。 このページでは、主要なカテゴリの概要を設定します。

## <a name="anonymization"></a>匿名化

プライバシー リスク管理機能内の匿名化されたバージョンのユーザー名を、特定の役割のユーザーに表示できます。 匿名化機能は、機密データの確認中にユーザーの ID をマスクするために、識別可能な表示名を汎用ラベルに置き換える機能です。 このオプションは、Subject Rights Requests ソリューションには適用されません。

## <a name="user-notification-emails"></a>ユーザー通知メール  

プライバシー リスク管理のポリシーを使用すると、環境内の潜在的なプライバシー リスクを評価するためのパラメーターを設定できます。 ポリシーの一致が検出されると、プライバシー リスク管理は、実行する是正措置に関する推奨事項とプライバシー トレーニングへのリンクを含む電子メールをユーザーに送信できます。 この **設定**、プライバシー リスク管理全体の電子メール通知機能を有効または無効にできます。 通知機能が無効になっている場合、設定メールはすべて無効になります。 ポリシーの詳細については、「プライバシー リスク管理で [ポリシーを作成する」を参照してください](risk-management-policies.md)。

## <a name="teams-collaboration"></a>Teams のコラボレーション  

すべてのMicrosoft Teamsと Priva Subject Rights Requests を統合して、関係者とのコラボレーションを強化します。 サブジェクト権限要求が作成されるたび、関連付けられたチームがユーザーにTeams。 ユーザーは、要求の [共同作業者] タブからチームに追加できます。件名の権利要求の詳細については、「 [Priva Subject Rights Requestsについて」を参照してください](subject-rights-requests.md)。

## <a name="data-matching"></a>データの照合  

このセクションを使用して、データ主体の属性を記述するデータ スキーマをアップロードします。これは、Microsoft 365 環境内で個人データを検索するときに適切なデータ主体を識別するのに役立ちます。 スキーマとルール パッケージは、XML 形式で作成およびアップロードされます。 [ **個人データのアップロード]** で、指定されたスキーマに一致する個人データを送信することもできます。 独自のファイルを作成してアップロードするか、Azure から個人データをアップロードできます。 件名の権利要求の詳細については、「 [Priva Subject Rights Requestsについて」を参照してください](subject-rights-requests.md)。

## <a name="data-retention-periods"></a>データ保持期間

この設定は、Priva Subject Rights Requests に関連しています。 これにより、要求が閉じた後に生成された収集データとレポートを保持する期間の設定を制御できます。 これは 30 日または 90 日に設定できます。作成したすべてのサブジェクト権限要求に適用されます。 データ保持期間が組織のポリシーと法的義務に準拠することを確認することをお勧めします。 サブジェクト権限要求 [のデータ保持について詳しくは、次の情報をご覧ください](subject-rights-requests-reports.md#retention-periods-for-reports-and-data)。

## <a name="data-review-tags"></a>データ レビュー タグ

データ レビュー タグを使用して、サブジェクト権限要求で取得されるコンテンツ アイテムにマークを付けできます。 この設定領域では、タグを管理できます。 Priva には、フォローアップ、削除、および更新 **の** **3 つの既定** のタグ **があります**。 これらのタグ名は編集できますが、組織にとって意味のあるこれらのタグの説明を提供できます。

Priva には、組織の使用に合わせて名前を付け、定義できる 2 つのカスタム タグも用意されています。 名前を編集するまで、カスタム タグ **1** とカスタム タグ **2** として表示されます。

タグ名と説明を編集するには、以下の手順に従います。

- [Priva 設定] **ページで、[** データ レビュー **タグ] を選択します**。
- 編集するタグを一覧から探し、その名前の横にある **[鉛筆** の編集] アイコンを選択します。
- フライアウト ウィンドウで、使用可能なフィールドで編集を行います。 システム タグの場合は、説明のみを編集できます。 カスタム タグの場合は、名前と説明を編集できます。
- 完了したら、[送信] を **選択して** 変更を保存します。

タグ設定は、すべてのサブジェクト権限要求に適用されます。

サブジェクト権限要求 [のデータを確認する際にタグを適用する方法について詳しくは、次のページをご覧ください](subject-rights-requests-data-review.md#apply-tags)。
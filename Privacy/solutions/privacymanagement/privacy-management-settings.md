---
title: プライバシー管理の設定を構成する
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
description: プライバシー管理のグローバル設定オプションについて説明します。
ms.openlocfilehash: 662a3979a0b4fed87beb364fd658569bd6aab074
ms.sourcegitcommit: 85e085eb17af8b4efd1f45207445e1b3c3679600
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/19/2021
ms.locfileid: "60478206"
---
# <a name="configure-privacy-management-settings"></a>プライバシー管理の設定を構成する

プライバシー管理の設定を管理するには、画面の右上隅にある歯車アイコンを選択します。 ここでのオプションを使用すると、高レベルの基本設定を設定し、キー プロパティをカスタマイズできます。 このページでは、主要なカテゴリとカテゴリの設定します。

## <a name="anonymization"></a>匿名化

この機能を使用すると、プライバシー管理機能内の匿名化されたバージョンのユーザー名を、特定の役割のユーザーに表示できます。 識別可能な表示名を汎用ラベルに置き換え、機密データを確認しながらユーザーの ID をマスクします。 このオプションは、サブジェクト権限要求モジュールには適用されません。

## <a name="user-notification-emails"></a>ユーザー通知メール  

プライバシー管理のポリシーを使用すると、環境内の潜在的なプライバシー リスクを評価するためのパラメーターを設定できます。 ポリシーの一致が検出されると、プライバシー管理は、修正措置に関する推奨事項とプライバシー トレーニングへのリンクを含む電子メールをユーザーに送信できます。 この設定、プライバシー管理全体の電子メール通知機能を有効または無効にできます。 通知機能が無効になっている場合、設定メールはすべて無効になります。 ポリシーの詳細については、「ポリシーの作成と [管理」を参照してください](privacy-management-policies.md)。

## <a name="teams-collaboration"></a>Teams のコラボレーション  

すべてのMicrosoft Teamsをプライバシー管理と統合して、関係者とのコラボレーションを強化します。 サブジェクト権限要求が作成される度に、関連付けられたチームがユーザーにTeams。 ユーザーは、要求の [共同作業者] タブからチームに追加できます。サブジェクト権限要求の詳細については、「対象権限要求の [管理」を参照してください](privacy-management-subject-rights-requests.md)。

## <a name="data-matching"></a>データの照合  

このセクションを使用して、データ主体の属性を記述するデータ スキーマをアップロードします。これは、Microsoft 365 環境内で個人データを検索するときに適切なデータ主体を識別するのに役立ちます。 スキーマとルール パッケージは、XML 形式で作成およびアップロードされます。 [個人データのアップロード] で、指定されたスキーマに一致する個人データを送信することもできます。 独自のファイルを作成してアップロードするか、Azure から個人データをアップロードできます。 サブジェクト権限要求の詳細については、「対象権限要求の [管理」を参照してください](privacy-management-subject-rights-requests.md)。

## <a name="data-retention-periods"></a>データ保持期間

この設定は、件名の要求に関連しています。 これにより、要求を閉じた後に生成した収集データとレポートを保持する期間の設定を制御できます。 これは、30 日または 90 日に設定できます。 これらのデータ保持期間がポリシーおよび法的義務に準拠している必要があります。 サブジェクト権限要求の詳細については、「対象権限要求の [管理」を参照してください](privacy-management-subject-rights-requests.md)。

## <a name="data-review-tags"></a>データ レビュー タグ

サブジェクト権限要求で取得したファイルにマークを付ける場合に使用するタグを管理します。 これらのタグは、手動で削除する必要があるコンテンツなど、さらに注意が必要なコンテンツを示すために使用できます。 設定のこのセクションでは、カスタム タグの名前と説明を編集できます。 システムによって提供される組み込みタグのタグの説明を編集することもできます。 システム タグの名前は変更できません。 サブジェクト権限要求の詳細については、「データを確認し、件名の権利要求で共同作業 [する」を参照してください](privacy-management-subject-rights-requests-review.md#step-3-review-data)。

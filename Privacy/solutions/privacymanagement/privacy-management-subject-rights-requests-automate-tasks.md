---
title: プライバシー管理でサブジェクト権限要求タスクを自動化する
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
description: プライバシー管理におけるサブジェクト権限要求Power Automateタスクを自動化するのに役立つ Microsoft Power Automateを使用する方法について説明します。
ms.openlocfilehash: df76e87e3298b2ccc6c897d485e695d0f1ae35c9
ms.sourcegitcommit: 85e085eb17af8b4efd1f45207445e1b3c3679600
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/19/2021
ms.locfileid: "60478189"
---
# <a name="automate-subject-rights-requests-tasks"></a>件名の要求タスクを自動化する

Microsoft Power Automateは、アプリケーションとサービス全体でアクションを自動化するワークフロー サービスです。 Microsoft 365 のプライバシー管理の Power Automate フローを有効にした場合、ServiceNow でチケットを作成したり、期日に関する予定表のリマインダーを追加したりなど、ケースとユーザーの重要なタスクを自動化できます。 このドキュメントの詳細についてはPower Automateドキュメント サイトを[参照してください](/power-automate/getting-started)。

プライバシー管理をMicrosoft 365サブスクリプションをお持ちのお客様は、推奨されるプライバシー管理Power Automateテンプレートを使用するために別のライセンスPower Automate必要はありません。 これらのテンプレートは、組織をサポートし、コア プライバシー管理シナリオをカバーするためにカスタマイズできます。 これらのテンプレートでプレミアム Power Automate 機能を使用する場合、Microsoft 365 コンプライアンス コネクタを使用してカスタム テンプレートを作成するか、Microsoft 365 の他のコンプライアンス領域に Power Automate テンプレートを使用する場合は、Power Automate ライセンスが必要な場合があります。

## <a name="create-a-new-power-automate-flow-from-a-template"></a>テンプレートから新Power Automateフローを作成する

1. [権限の [Microsoft 365 コンプライアンス センター]](https://compliance.microsoft.com/)で、ナビゲーションの [プライバシー管理] セクションに移動し、[件名の権利の要求 **] を選択します**。
1. 一覧から操作する件名の権限要求を開き、[自動化]を選択し、[管理] を選択してPower Automate **します**。 [フロー] フライアウト ウィンドウが開きます。
1. [新規] **オプションを** 使用し、使用可能なオプションから使用するテンプレートを選択します。 ここから、ウィザードの指示に従ってセットアップを完了します。 オプションは、テンプレートの種類によって異なります。

テンプレートのインスタンスを保存した後、フロー インスタンスが適切なコンテキストと ID を持つ必要がある場合は、サブジェクト権限要求の詳細ページから実行する必要があります。 要求を開き、[自動化] メニューに **戻** り、テンプレートを選択し、[フローの実行] **を選択します**。 [フロー実行アクティビティの表示] を選択すると、過去 **のアクティビティを確認できます**。

### <a name="power-automate-templates-in-privacy-management"></a>Power Automate管理のテンプレート

- **ServiceNow でプライバシー管理** ケースのレコードを作成する : このテンプレートは、ServiceNow ソリューションを使用して件名の権利要求ケースを追跡する組織向けです。 ServiceNow に接続するアカウントを含む、ServiceNow インスタンスの詳細を入力する必要があります。 このアカウントには、ServiceNow でインシデントを作成し、インシデントの詳細を入力する機能が必要です。 インスタンスに接続すると、サブジェクト権限要求管理者は ServiceNow でケースのレコードを作成できます。必要に応じて、テンプレートが選択したフィールドに設定する内容をカスタマイズできます。 コネクタの詳細については [、「ServiceNow Connector リファレンス ページ」を参照してください](/connectors/service-now/)。
- **予定表のアラームを作成** する: このテンプレートは、件名の権利の要求に対して、Outlookカレンダーで期日通知を設定します。 このツールは、要求のプロパティ (要求の名前や期限など) から特定の詳細を入力します。 説明の詳細を追加し、受信者を指定し、その他の詳細設定を調整できます。
- **件名権限要求のタグ** でファイルを取得する : このテンプレートを使用すると、特定のタグが与えられた件名の権利要求のファイルを検索できます。 フローを編集してカスタム アクションを実行したり、返されるファイルの一覧を表示して内部プロセスやツールを活用できます。

## <a name="share-a-power-automate-flow"></a>データ フロー Power Automateする

フローを共有Power Automate、別の所有者を追加して、フローの編集、更新、および削除を許可できます。 すべての所有者は、実行履歴にアクセスし、他の所有者を追加または削除できます。 フローを共有するには、操作するサブジェクト権限要求を開き、[自動化]を選択し、[フローの管理] **Power Automateします**。 このウィンドウから既存のフローを選択し、[共有] オプションを使用してユーザーまたはグループを追加できます。

このウィンドウでは、サービス フローで使用されているサービスへの埋め込み接続を管理Power Automateもあります。 これらの設定を変更すると、フローを実行する機能に影響を与える可能性があります。

## <a name="edit-or-delete-power-automate-flow"></a>フローを編集またはPower Automateする

アプリケーション フローの詳細を調整Power Automate、件名の権限要求を開き、[自動化] を選択し、[フローの管理] をPower Automate **します**。 このウィンドウから、既存のフローを選択して詳細を表示できます。 任意のセクションで [編集] を使用してプロパティを変更し、保存します。

フローを完全に削除するには、[削除] オプション **を使用** します。 すべての所有者のフローが削除され、すべてのユーザーに対してアンインストールされます。 以前のフロー インスタンスは、データ損失を回避するために引き続き実行されます。 削除が最終的に行う前に、選択内容を確認できます。

## <a name="legal-disclaimer"></a>法的免責事項

[プライバシー管理の法的免責事項](privacy-management-disclaimer.md)

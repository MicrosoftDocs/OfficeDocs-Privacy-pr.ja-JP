---
title: 'サブジェクト権利要求のタスクを自動化する '
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
description: Microsoft Power Automateを使用して、Priva のサブジェクト権利要求に関する重要なタスクを自動化する方法について説明します。
ms.openlocfilehash: ec9edde16b60c2326ca899e587dfe5dc7a1e32f5
ms.sourcegitcommit: 09ecdaded9a9f8f79587f2acb978dc53b83e5c01
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/19/2022
ms.locfileid: "64930498"
---
# <a name="automate-tasks-in-subject-rights-requests"></a>サブジェクト権利要求のタスクを自動化する 

Microsoft Power Automateは、アプリケーションとサービス間のアクションを自動化するワークフロー サービスです。 Microsoft Priva Subject Rights Requests のPower Automate フローを有効にすると、ServiceNow でのチケットの作成や期限に関する予定表のリマインダーの追加など、ケースとユーザーの重要なタスクを自動化できます。 Power Automateの詳細については、[ドキュメント サイトを参照してください](/power-automate/getting-started)。

Subject Rights Requests サブスクリプションをお持ちのお客様は、Priva に推奨されるPower Automate テンプレートを使用するために、別のPower Automate ライセンスは必要ありません。 これらのテンプレートは、組織をサポートし、主要なサブジェクト権利要求シナリオをカバーするようにカスタマイズできます。 これらのテンプレートで Premium Power Automate 機能を使用する場合、Microsoft 365 コンプライアンス コネクタを使用してカスタム テンプレートを作成する場合、またはMicrosoft 365の他のコンプライアンス領域でPower Automate テンプレートを使用する場合は、さらにPower Automate ライセンスが必要になる場合があります。

## <a name="create-a-new-power-automate-flow-from-a-template"></a>テンプレートから新しいPower Automate フローを作成する

1. [Microsoft Purview コンプライアンス ポータル](https://compliance.microsoft.com/)で、ナビゲーションの [Priva] セクションに移動し、[**Priva Subject Rights Requests**] を選択します。
1. 操作するサブジェクト権限要求を一覧から開き、[**自動化**]、[**Power Automate フローの管理**] の順に選択します。 [フロー] ポップアップ ウィンドウが開きます。
1. **[新規**] オプションを使用し、使用可能なオプションから使用するテンプレートを選択します。 ここから、ウィザードの指示に従ってセットアップを完了します。 オプションは、テンプレートの種類によって異なります。

テンプレートのインスタンスを保存した後、フロー インスタンスが適切なコンテキストと ID を持つように、サブジェクト権限要求の詳細ページからテンプレートを実行する必要があります。 要求を開き、[ **自動化** ] メニューに戻り、テンプレートを選択して、[ **フローの実行**] を選択します。 [フロー実行アクティビティの表示] を選択すると、過去の **アクティビティを確認** できます。

### <a name="power-automate-templates-in-priva"></a>Priva でテンプレートをPower Automateする

- **ServiceNow でプライバシー管理ケースのレコードを作成** する: このテンプレートは、ServiceNow ソリューションを使用してサブジェクト権利要求ケースを追跡する組織向けです。 ServiceNow に接続するアカウントを含め、ServiceNow インスタンスの詳細を入力するように求められます。 このアカウントには、ServiceNow でインシデントを作成し、インシデントの詳細を入力する機能が必要です。 インスタンスに接続すると、サブジェクト権限要求管理者は ServiceNow でケースのレコードを作成でき、必要に応じて、テンプレートが選択したフィールドに設定する内容をカスタマイズできます。 コネクタの詳細については、 [ServiceNow コネクタのリファレンス ページを参照](/connectors/service-now/)してください。
- **予定表のリマインダーを作成する**: このテンプレートは、件名の権利要求のOutlook予定表で期限のリマインダーを設定するためのテンプレートです。 このツールは、要求の名前や期限など、要求のプロパティから特定の詳細を入力します。 わかりやすい詳細を追加したり、受信者を指定したり、その他の詳細設定を調整したりできます。
- **サブジェクト権限要求のタグでファイルを取得** する: このテンプレートを使用すると、特定のタグが与えられたサブジェクト権限要求のファイルを検索できます。 フローを編集してカスタム アクションを実行したり、返されたファイルの一覧を表示して内部プロセスやツールを活用したりできます。

## <a name="share-a-power-automate-flow"></a>Power Automate フローを共有する

Power Automate フローを共有することで、別の所有者を追加し、フローの編集、更新、削除を許可できます。 すべての所有者は、実行履歴にアクセスし、他の所有者を追加または削除することもできます。 フローを共有するには、操作するサブジェクト権限要求を開き、[**自動化**]、[**Power Automate フローの管理**] の順に選択します。 このウィンドウから既存のフローを選択し、[共有] オプションを使用してユーザーまたはグループを追加できます。

このウィンドウでは、Power Automate フローで使用されているサービスへの埋め込み接続を管理することもできます。 これらの設定を変更すると、フローを実行する機能に影響を与える可能性があります。

## <a name="edit-or-delete-power-automate-flow"></a>フロー Power Automate編集または削除する

Power Automate フローの詳細を調整するには、サブジェクト権限要求を開き、[**自動化**] を選択し、[**Power Automate フローの管理**] を選択します。 このウィンドウから、既存のフローを選択して詳細を表示できます。 任意のセクションで Edit を使用してプロパティを変更し、保存します。

フローを完全に削除するには、[削除] オプションを使用 **します** 。 すべての所有者のフローが削除され、すべてのユーザーに対してアンインストールされます。 以前のフロー インスタンスは、データ損失を回避するために引き続き実行されます。 削除が終了する前に、選択内容を確認できます。

## <a name="legal-disclaimer"></a>法的免責事項

[Microsoft Priva の法的免責事項](priva-disclaimer.md)

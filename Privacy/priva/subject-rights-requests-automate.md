---
title: Microsoft Graph APIおよびPower Automateと統合する
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
description: Microsoft Graph APIおよびPower Automateと統合して、Priva 主体の権利要求機能を拡張する方法について説明します。
ms.openlocfilehash: e4fcad2067ece3d1a6338e6d4891c59d91205a33
ms.sourcegitcommit: 9315064bf5bb9e889318e61ec5f082f36c815e1e
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/02/2022
ms.locfileid: "65851642"
---
# <a name="integrate-and-extend-through-microsoft-graph-api-and-power-automate"></a>Microsoft Graph APIとPower Automateを統合して拡張する

Microsoft Graph Subject Rights Request API を使用して、Priva 主体の権利要求を既存のビジネス プロセスやツールと統合できます。 また、予定表のリマインダーの設定や ServiceNow でのケースの作成などのタスクに組み込みのPower Automate フローを使用して、サブジェクト権利要求の自動化機能を拡張することもできます。

## <a name="microsoft-graph-subject-rights-requests-api"></a>Microsoft Graph Subject Rights Requests API

Microsoft 365 Subject Rights Request API は、既存のサブジェクト権利戦略に自動化を導入するためのシンプルで強力な方法を提供します。 個々のユーザーが組織に情報を要求する場合、API を使用すると、その要求の条件に基づいてMicrosoft 365内にこれらの要求を作成できます。 Microsoft 365でサブジェクト権限要求を作成し、その進行状況を追跡し、要求の処理が完了し、コンテンツを取得する準備が整ったときに確認することができます。

MICROSOFT の API は、ISV、ソリューション内のMicrosoft 365に対応するパートナー、ビジネス アプリケーションのラインで API を使用しようとしている組織など、ソリューションの拡張性を高めるために誰でも利用できます。

[Microsoft Graphサブジェクト権利要求 API を使用する](/graph/api/resources/subjectrightsrequest-subjectrightsrequestapioverview)に関するページの完全なドキュメントを参照してください。

## <a name="power-automate-templates-for-subject-rights-requests"></a>サブジェクト権利要求のPower Automate テンプレート

Microsoft Power Automateは、アプリケーションとサービス間のアクションを自動化するワークフロー サービスです。 サブジェクト権利要求には、ユーザーがサブジェクト権限要求を管理するのに役立つ組み込みのPower Automate テンプレートが含まれています。 ユーザーは、ServiceNow でチケットを作成したり、期限に関する予定表のリマインダーを追加したりするようなプロセスの自動化フローを設定できます。 Power Automateの詳細については、[Power Automateのドキュメントを参照してください](/power-automate/getting-started)。

Subject Rights Requests サブスクリプションを購入した場合、推奨されるPower Automate テンプレートを使用するために別のPower Automate ライセンスは必要ありません。 これらのテンプレートは、組織をサポートし、主要なサブジェクト権利要求シナリオをカバーするようにカスタマイズできます。 ただし、これらのテンプレートで Premium Power Automate機能を使用したり、独自のテンプレートを作成したりするには、追加のライセンスが必要になる場合があります。

### <a name="available-templates"></a>使用可能なテンプレート

- **ServiceNow でPrivaプライバシー管理ケースのレコードを作成** する: このテンプレートは、ServiceNow ソリューションを使用してサブジェクト権利要求ケースを追跡する組織向けです。 ServiceNow に接続するアカウントを含め、ServiceNow インスタンスの詳細を入力するように求められます。 このアカウントには、ServiceNow でインシデントを作成し、インシデントの詳細を入力する機能が必要です。 インスタンスに接続すると、サブジェクト権限要求管理者は ServiceNow でケースのレコードを作成でき、必要に応じて、テンプレートが選択したフィールドに設定する内容をカスタマイズできます。 コネクタの詳細については、 [ServiceNow コネクタのドキュメントを参照してください](/connectors/service-now/)。

- **Privaプライバシー管理ケースをフォローアップする予定表のリマインダーを追加** する: このテンプレートは、件名の権利要求のOutlook予定表で期限のリマインダーを設定するためのテンプレートです。 このツールは、要求の名前や期限など、要求のプロパティから特定の詳細を入力します。 わかりやすい詳細を追加したり、受信者を指定したり、その他の詳細設定を調整したりできます。

- **Privaサブジェクト権限要求のタグでファイルを取得** する: このテンプレートを使用すると、特定のタグが与えられたサブジェクト権限要求のファイルを検索できます。 フローを編集してカスタム アクションを実行したり、内部プロセスやツールに使用する返されたファイルの一覧を表示したりできます。

### <a name="create-a-new-power-automate-flow-from-a-template"></a>テンプレートから新しいPower Automate フローを作成する

1. [Microsoft Purview コンプライアンス ポータル](https://compliance.microsoft.com/)で、左側のナビゲーションで **Priva 主体の権利要求** を選択します。

2. 作業するサブジェクト権限要求を見つけて、一覧から選択して詳細ページを開きます。

3. 右上隅にある **[自動化**] を選択し、[**Power Automate フローの管理**] を選択してフローポップアップ ウィンドウを開きます。

4. [ **新規** ] を選択し、使用可能なオプションから使用するテンプレートを選択します。 ここから、プロンプトに従ってカスタマイズし、フローの構築を完了する手順を追加します。 オプションは、使用するテンプレートによって異なります (以下のテンプレートの種類を参照)。

5. 完了したら、**[保存]** を選択します。

テンプレートのインスタンスを保存した後、フロー インスタンスが適切なコンテキストと ID を持つよう、要求の詳細ページから実行する必要があります。 要求を開き、[ **自動化** ] メニューに戻り、テンプレートを選択して、[ **フローの実行**] を選択します。 [フロー実行アクティビティの表示] を選択すると、過去の **アクティビティを確認** できます。

### <a name="share-a-power-automate-flow"></a>Power Automate フローを共有する

Power Automate フローを共有すると、別の所有者を追加し、フローの編集、更新、削除を行うことができます。 すべての所有者は、実行履歴にアクセスし、他の所有者を追加または削除できます。 

フローを共有するには、操作するサブジェクト権限要求を開き、[**自動化**]、[**Power Automate フローの管理**] の順に選択します。 このウィンドウから既存のフローを選択し、[ **共有** ] オプションを使用してユーザーまたはグループを追加できます。

このウィンドウでは、Power Automate フローで使用されているサービスへの埋め込み接続を管理することもできます。 これらの設定を変更すると、フローを実行する機能に影響を与える可能性があります。

### <a name="edit-or-delete-power-automate-flow"></a>フロー Power Automate編集または削除する

Power Automate フローの詳細を調整するには、要求の詳細ページの右上隅にある **[自動化**] を選択し、[**Power Automate フローの管理**] を選択します。

**[Power Automate フロー**] ウィンドウで、編集するフローを選択し、コマンド バーから **[編集]** を選択してステップを編集または追加します。 完了したら、[保存] を選択 **します**。

フローを削除するには、**Power Automate フロー** ウィンドウの一覧からフローを選択し、コマンド バーから **[削除**] を選択します。 フローはすべての所有者に対して削除され、すべてのユーザーに対してアンインストールされます。 以前のフロー インスタンスは、データ損失を回避するために引き続き実行されます。 削除が最終的になる前に、確認を求められます。

## <a name="legal-disclaimer"></a>法的免責事項

[Microsoft Priva法的免責事項](priva-disclaimer.md)

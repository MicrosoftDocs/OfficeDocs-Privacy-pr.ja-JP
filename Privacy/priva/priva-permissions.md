---
title: Microsoft Priva でユーザーのアクセス許可を設定し、役割を割り当てる
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
- M365-priva-privacy-risk-management
- M365-priva-subject-rights-requests
search.appverid:
- MOE150
- MET150
description: Microsoft Priva のアクセス許可を設定し、ユーザーを役割グループに割り当てる方法について説明します。
ms.openlocfilehash: bcc2e108f10e427e55034621f2f8b5c40e6d9184
ms.sourcegitcommit: f145dff5e387a8e26db2f3a2c7de125978fbacc9
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/28/2022
ms.locfileid: "62249108"
---
# <a name="set-user-permissions-and-assign-roles-in-microsoft-priva"></a>Microsoft Priva でユーザーのアクセス許可を設定し、役割を割り当てる

組織のメンバーに Microsoft Priva を使用するアクセス許可を付与するには、組織のグループ内の適切な役割グループに割り当Microsoft 365 コンプライアンス センター。

> [!NOTE]
> ほとんどの Priva の役割は現在、"プライバシー管理" として指定されています。 完全なリストについては、以下を参照してください。 Priva に固有の役割は、ユーザーのAzure Active Directory。

## <a name="sign-in-and-set-permissions"></a>サインインしてアクセス許可を設定する

1. [アクセス許可] [のMicrosoft 365 コンプライアンス センター](https://compliance.microsoft.com/)左側 **のナビゲーションで [アクセス許可]** を選択します。  
2. [コンプライアンス センター] **ドロップダウンで、[** 役割] を **選択します**。 役割グループの完全な一覧が表示されます。
3. 1 人以上のユーザーを追加する役割グループを探し、グループ名の左にあるチェック ボックスをオンにします。
4. そのグループのポップアップ ウィンドウで、**[メンバー]** ヘッダーの下の **[編集]** を選択します。  
5. **[メンバーの選択]** を選びます。 別のポップアップ ウィンドウが表示されます。
6. **[追加]** を選択して、グループに追加する 1 人以上のユーザーを選択します。  
7. 追加する名前の横にあるチェックボックスを選択し、下部にある **[追加]** ボタンを選択します。  
8. ユーザーの割り当てが完了したら、[完了]、 **次** に[保存]、 **次に [** 閉じる] の順に **選択します**。

## <a name="learn-more-about-role-groups-and-roles"></a>役割グループと役割の詳細

チームの構造に応じて、ユーザーを特定の役割グループに割り当て、さまざまな Priva 機能セットを管理するオプションがあります。 メンバーは、実行する必要があるタスクと適切なファイル アクセスのレベルに応じて、役割グループに割り当てる必要があります。 各役割グループには、1 つ以上の役割が含まれます。 これらの役割は、そのグループのメンバーに対して有効または制限されている特定の Priva タスクまたはキー関数に関連する場合があります。 したがって、ユーザーによって、特定の Priva 機能への表示とアクセスのレベルが異なる場合があります。

役割グループは、必要に応じてカスタマイズできます。 アクセスが偶発的に失われなされないように、カスタマイズする既存の役割グループのコピーを作成し、コピーに識別可能な名前を付け、新しいグループに対する変更を行って確認し、必要に応じてユーザーを割り当てすることをお勧めします。

## <a name="privacy-management-role-group"></a>プライバシー管理役割グループ

このグループには、1 つのグループ内のすべての Priva アクセス許可ロールが含まれる。 この役割グループは、同じ個人がすべての職務を遂行できる組織に適している場合があります。 この役割グループにメンバーシップを提供すると、ライセンスを保持している Priva のすべての機能へのフル アクセスがアカウントに付与されます。

このグループのアクティブなメンバーが常に 1 つ以上あるか確認することをお勧めします。

役割には、次のものが含まれます。

- ケース管理  
- データ分類コンテンツ ビューアー  
- データ分類リスト ビューアー  
- プライバシー管理管理者  
- プライバシー管理の分析  
- プライバシー管理の調査  
- プライバシー管理の永続的な貢献  
- プライバシー管理一時的な投稿  
- プライバシー管理ビューアー  
- Subject Rights Request Admin  
- View-Onlyケース

## <a name="privacy-management-administrators-role-group"></a>プライバシー管理管理者役割グループ

この役割グループのメンバーは、プライバシー リスク管理ポリシー、サブジェクト権限要求、アクセス許可、および設定の作成、読み取り、更新、削除など、Priva 機能に幅広くアクセスできます。

役割には、次のものが含まれます。

- ケース管理  
- プライバシー管理管理者  
- View-Onlyケース

## <a name="privacy-management-analysts-role-group"></a>プライバシー管理アナリストの役割グループ

この役割グループのメンバーは、ケース アナリストとして機能します。 ポリシーの一致を調査し、ファイル メタデータを表示し、修復アクションを実行できます。 このグループは、コンテンツ エクスプローラーを介して完全なファイルにアクセスできません。

役割には、次のものが含まれます。

- ケース管理  
- データ分類リスト ビューアー  
- プライバシー管理の分析  
- View-Onlyケース

### <a name="privacy-management-investigators-role-group"></a>プライバシー管理の調査者役割グループ

このグループのメンバーは、データ調査者として機能します。 ポリシーの一致を調査し、関連付けられたファイル コンテンツを表示し、修復アクションを実行できます。 このグループは、コンテンツ エクスプローラーを介してファイルにアクセスできます。

役割には、次のものが含まれます。

- ケース管理  
- データ分類コンテンツ ビューアー  
- データ分類リスト ビューアー  
- プライバシー管理の調査  
- View-Onlyケース

## <a name="privacy-management-viewer-role-group"></a>プライバシー管理ビューアーの役割グループ

このグループのメンバーは、概要、データ プロファイル、件名要求レポートなど、Priva で分析情報を表示できます。

役割には、次のものが含まれます。

- プライバシー管理ビューアー

## <a name="subject-rights-request-administrators-role-group"></a>Subject Rights Request Administrators 役割グループ

このグループのメンバーは、サブジェクト権限要求を管理および作成するフル アクセス権を持っています。

役割には、次のものが含まれます。

- Subject Rights Request Admin

## <a name="privacy-management-contributors-role-group"></a>プライバシー管理投稿者役割グループ

このグループのメンバーは、共同編集者として追加されたサブジェクト権限要求にアクセスできます。  

役割には、次のものが含まれます。

- プライバシー管理一時的な投稿  
- プライバシー管理の永続的な貢献

## <a name="legal-disclaimer"></a>法的免責事項

[Microsoft Priva の法的免責事項](priva-disclaimer.md)
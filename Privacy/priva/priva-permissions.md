---
title: Microsoft Privaでユーザーのアクセス許可を設定し、ロールを割り当てる
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
description: Microsoft Privaアクセス許可を設定し、ユーザーをロール グループに割り当てる方法について説明します。
ms.openlocfilehash: eca08327e2db909475dbf4c072b8f6843de3d57b
ms.sourcegitcommit: 3c27ecf7c86c8a3db38cae8819fc090eed192b4f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/25/2022
ms.locfileid: "65678224"
---
# <a name="set-user-permissions-and-assign-roles-in-microsoft-priva"></a>Microsoft Privaでユーザーのアクセス許可を設定し、ロールを割り当てる

組織のメンバーにMicrosoft Privaを使用するアクセス許可を付与するには、Microsoft Purview コンプライアンス ポータルの適切な役割グループに割り当てます。

> [!NOTE]
> ほとんどのPrivaロールは現在、"プライバシー管理" として指定されています。 完全な一覧については、以下を参照してください。 Privaに固有のロールは、Azure Active Directoryには表示されません。

## <a name="sign-in-and-set-permissions"></a>サインインしてアクセス許可を設定する

1. [Microsoft Purview コンプライアンス ポータル](https://compliance.microsoft.com/)に移動し、左側のナビゲーションで **[アクセス許可**] を選択します。  
2. **[Microsoft Purview ソリューション**] ドロップダウンで、[**ロール**] を選択します。 役割グループの完全な一覧が表示されます。
3. 1 人以上のユーザーを追加する役割グループを見つけて (以下の役割グループの説明を参照)、グループ名の左側にあるチェック ボックスをオンにします。
4. そのグループのポップアップ ウィンドウの [ **メンバー** ] ヘッダーの下にある [編集] を選択 **します**。  
5. ポップアップ ウィンドウで、左側のナビゲーションで [ **メンバーの選択** ] を選択します。 別のポップアップ ウィンドウが表示されます。
6. **[追加]** を選択して、グループに追加する 1 人以上のユーザーを選択します。  
7. 追加する名前の横にあるチェックボックスを選択し、下部にある **[追加]** ボタンを選択します。  
8. ユーザーの割り当てが完了したら、[ **完了]**、[ **保存]**、[ **閉じる**] の順に選択します。

## <a name="learn-more-about-role-groups-and-roles"></a>ロール グループとロールの詳細を確認する

チームの構造に応じて、ユーザーを特定のロール グループに割り当てて、さまざまなPriva機能のセットを管理するオプションがあります。 メンバーは、実行する必要があるタスクと適切なファイル アクセスのレベルに応じて、ロール グループに割り当てる必要があります。 各役割グループには、1 つ以上のロールが含まれています。 これらのロールは、そのグループのメンバーに対して有効または制限されている特定のPriva タスクまたは主要な機能に関連する場合があります。 そのため、ユーザーごとに、特定のPriva機能に対する可視性とアクセスレベルが異なる場合があります。

必要に応じて、ロール グループをカスタマイズできます。 誤ってアクセスを失わないように、カスタマイズする既存の役割グループのコピーを作成し、コピーに識別可能な名前を付け、新しいグループに変更を加えて確認し、必要に応じてユーザーを割り当てることをお勧めします。

## <a name="privacy-management-role-group"></a>プライバシー管理の役割グループ

このグループには、1 つのグループ内のすべてのPrivaアクセス許可ロールが含まれます。 この役割グループは、同じ個人がすべての職務を遂行できる組織に適している可能性があります。 このロール グループにメンバーシップを提供すると、そのアカウントに、ライセンスを保持しているPrivaのすべての機能へのフル アクセス権が付与されます。

このグループのアクティブなメンバーが常に 1 つ以上存在することを確認することをお勧めします。

ロールは次のとおりです。

- ケース管理  
- データ分類コンテンツ ビューアー  
- データ分類リスト ビューアー  
- プライバシー管理管理  
- プライバシー管理分析  
- プライバシー管理の調査  
- プライバシー管理の永続的な貢献  
- プライバシー管理の一時的な貢献  
- プライバシー管理ビューアー  
- サブジェクト権利要求管理  
- View-Only ケース

## <a name="privacy-management-administrators-role-group"></a>プライバシー管理管理者の役割グループ

このロール グループのメンバーは、プライバシー リスク管理ポリシーの作成、読み取り、更新、削除、サブジェクト権利要求、アクセス許可、設定など、Priva機能に幅広くアクセスできます。

ロールは次のとおりです。

- ケース管理  
- プライバシー管理管理  
- View-Only ケース

## <a name="privacy-management-analysts-role-group"></a>Privacy Management Analysts ロール グループ

この役割グループのメンバーは、ケース アナリストとして機能します。 ポリシーの一致を調査し、ファイル メタデータを表示し、修復アクションを実行できます。 このグループは、コンテンツ エクスプローラーを介して完全なファイルにアクセスできません。

ロールは次のとおりです。

- ケース管理  
- データ分類リスト ビューアー  
- プライバシー管理分析  
- View-Only ケース

### <a name="privacy-management-investigators-role-group"></a>Privacy Management Investigators ロール グループ

このグループのメンバーは、データ調査担当者として機能します。 ポリシーの一致を調査し、関連するファイル の内容を表示し、修復アクションを実行できます。 このグループは、コンテンツ エクスプローラーからファイルにアクセスできます。

ロールは次のとおりです。

- ケース管理  
- データ分類コンテンツ ビューアー  
- データ分類リスト ビューアー  
- プライバシー管理の調査  
- View-Only ケース

## <a name="privacy-management-viewer-role-group"></a>プライバシー管理ビューアーの役割グループ

このグループのメンバーは、概要、データ プロファイル、件名要求レポートなどの分析情報をPrivaで表示できます。

ロールは次のとおりです。

- プライバシー管理ビューアー

## <a name="subject-rights-request-administrators-role-group"></a>Subject Rights Request Administrators ロール グループ

このグループのメンバーは、サブジェクト権限要求を管理および作成するためのフル アクセス権を持ちます。

ロールは次のとおりです。

- サブジェクト権利要求管理

## <a name="privacy-management-contributors-role-group"></a>プライバシー管理共同作成者の役割グループ

このグループのメンバーは、コラボレーターとして追加されたサブジェクト権限要求にアクセスできます。  

ロールは次のとおりです。

- プライバシー管理の一時的な貢献  
- プライバシー管理の永続的な貢献

## <a name="legal-disclaimer"></a>法的免責事項

[Microsoft Priva法的免責事項](priva-disclaimer.md)
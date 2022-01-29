---
title: プライバシー リスク管理でユーザー通知を送信する
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
search.appverid:
- MOE150
- MET150
description: プライバシー リスク管理で見つかったポリシーの一致についてコンテンツ所有者に通知する方法と、これらの電子メール通知を使用して問題を修復する方法について説明します。
ms.openlocfilehash: 2215224adf932f806f16429560d4a694cd47a859
ms.sourcegitcommit: f145dff5e387a8e26db2f3a2c7de125978fbacc9
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/28/2022
ms.locfileid: "62249085"
---
# <a name="send-user-notifications-in-privacy-risk-management"></a>プライバシー リスク管理でユーザー通知を送信する

Microsoft Priva のプライバシー リスク管理では、データの過剰露出、データ最小化、およびデータ転送ポリシーの一致について、コンテンツ所有者に直接通知できます。 電子メール通知を使用すると、ユーザーは確認する必要があるコンテンツについて簡単に確認できます。また、メール内のプロンプトを使用して適切な修正アクションを適用できます。 これらのメールには、独自のプライバシー トレーニングへのリンクも含まれます。 データ転送ポリシーの場合は、通知とポリシー のヒントをチャネルで共有Teamsできます。

## <a name="prepare-training-content-for-policy-notifications"></a>ポリシー通知のトレーニング コンテンツを準備する

通知を生成するポリシーには、プライバシー トレーニングへのリンクを含む必要があります。 組織のプライバシー ガイドラインへのアクセスを提供すると、ユーザーに独自のベスト プラクティスとポリシーについて情報を提供できます。 また、電子メールで推奨される修復アクションのコンテキストを提供し、ユーザーが将来の良好なデータ管理の決定に備えるのに役立ちます。

ポリシーを設定する前に、含めるトレーニング URL を決定します。 ポリシーごとに 1 つのリンクを提供できます。そのため、各シナリオに固有の参照を選択することをお勧めします。

## <a name="set-up-email-notifications-for-policies"></a>ポリシーの電子メール通知を設定する

カスタム ポリシーを作成したり、ポリシーを編集したりするときに、電子メール通知を構成できます。 詳細 [な手順については、「プライバシー リスク管理でポリシーを作成](risk-management-policies.md) する」を参照してください。 電子メール通知の設定は、ポリシー ウィザードの **[結果** ] タブにあります。 ここでは、通知を送信する頻度を決定し、プライバシー トレーニング URL を設定し、電子メールの件名または本文のカスタム テキストを入力できます。

## <a name="remediate-issues-from-email-notifications"></a>電子メール通知から問題を修復する

ユーザーがポリシーの一致に関する電子メール通知を受け取った場合、ユーザーは電子メールのプロンプトに従って直ちに修正アクションを実行できます。 たとえば、データオーバー露出ポリシーで、アクセスが広すぎる可能性がある個人データの一致が見つかった場合、結果の電子メールは、アイテムを非公開にするボタンプロンプトを提供する場合があります。 指定されたアイテムを保持する必要がある場合、ユーザーはアイテムを保持する選択もできます。 提供される推奨されるアクションは、各種類のポリシーに関連します。

## <a name="send-notifications-in-teams"></a>メールで通知を送信Teams

データ転送ポリシーの場合、ユーザーは、ポリシーの一致が検出されると、セキュリティで保護されたチャネルTeams推奨事項を受け取る可能性があります。 これらのヒントは、個人データの責任ある使用についてユーザーに教育します。 ヒント関連するトレーニングへのリンクも含まれます。

これらの通知の設定の詳細については、「プライバシー リスク管理 [でポリシーを作成する」を参照してください](risk-management-policies.md#set-user-email-notifications)。

## <a name="legal-disclaimer"></a>法的免責事項

[Microsoft Priva の法的免責事項](priva-disclaimer.md)

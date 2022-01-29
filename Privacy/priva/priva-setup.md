---
title: Priva の使用を開始する
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
- MET150fcf
description: 組織の Microsoft Priva をセットアップし、役割とアクセス許可を設定し、重要な設定を構成する方法について説明します。
ms.openlocfilehash: 62e28361b57dd866b95ce566616473ed1a71e4ad
ms.sourcegitcommit: f145dff5e387a8e26db2f3a2c7de125978fbacc9
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/28/2022
ms.locfileid: "62249101"
---
# <a name="get-started-with-priva"></a>Priva の使用を開始する

Microsoft Priva を使用してプライバシー リスクの特定と軽減を支援する準備が整った場合は、次の手順に従って前提条件を設定し、プライバシーに関する分析情報の確認を開始してください。

## <a name="step-1-confirm-subscriptions-and-licensing"></a>手順 1: サブスクリプションとライセンスを確認する

Priva は、Microsoft 365 コンプライアンス センター内で利用できます。次のライセンス[を](https://compliance.microsoft.com/)持つ組織が購入できます。

- Microsoft 365 E3、E5、A3、A5
- Office 365 E1 E3、E5、A1、A3、A5

Priva は、Priva Privacy Risk Management と Priva Subject Rights Requests という 2 つの異なるソリューションのライセンス オプションを提供します。 これらは個別または一緒に購入できます。 サブジェクト権限要求のライセンスを取得する場合は、処理する必要がある要求の数に応じて適切なライセンス層を選択できます。 追加の要求は、いつでも購入できます。

ライセンスのガイダンスに関する詳細については、「[セキュリティとコンプライアンスのための Microsoft 365 ライセンス ガイダンス](/office365/servicedescriptions/microsoft-365-service-descriptions/microsoft-365-tenantlevel-services-licensing-guidance/microsoft-365-security-compliance-licensing-guidance#privacy-management)」を参照してください。

> [!Note]
> Priva は、米国政府機関 (Community) (GCC) GCC高、または国防総省 (DoD) のお客様には使用できません。

### <a name="get-free-trial-license"></a>無料試用版ライセンスを取得する

Priva の使用を開始するには、無料試用版ライセンスを利用できます。 参加資格と参加方法については、「無料の [Priva 試用版について」を参照してください](priva-trial.md)。

## <a name="step-2-enable-the-microsoft-365-audit-log"></a>手順 2: 監査ログMicrosoft 365有効にする

Microsoft 365監査ログは、組織内のすべてのアクティビティの概要です。 プライバシー リスク管理ポリシーは、ポリシーの分析情報を生成するためにこれらのアクティビティを使用する場合があります。

組織で既に監査ログが有効になっている可能性があります。 初めて使用を開始する必要がある場合は、「監査ログ[](/microsoft-365/compliance/turn-audit-log-search-on-or-off)の検索をオンまたはオフにする」を参照して、監査を有効にする手順について説明します。 監査を有効にすると、監査ログの準備中で、準備が完了してから数時間で検索を実行できるというメッセージが表示されます。 このアクションを行う必要があるのは 1 回だけです。 監査ログの使用のMicrosoft 365詳細については、「監査ログの[検索」を参照してください](/microsoft-365/compliance/search-the-audit-log-in-security-and-compliance)。

## <a name="step-3-set-user-permissions-and-assign-roles"></a>手順 3: ユーザーのアクセス許可を設定し、役割を割り当てる

Priva は、役割ベースのアクセス制御 (RBAC) アクセス許可モデルを使用します。 役割が割り当てられているユーザーだけが Priva にアクセスできます。各ユーザーが許可するアクションは、役割の種類によって制限されます。

グローバル管理者は、Priva にアクセスし、他のユーザーを役割に割り当てるアクセス許可を持っています。 ユーザーは、Priva のサインインとアクセス許可[の設定Microsoft 365 コンプライアンス センター](https://compliance.microsoft.com/)アクセス許可を設定できます。 クイック スタートの場合、プライバシー管理役割グループには、Priva のすべての機能にアクセスするためのアクセス許可があります。 このグループは、同じ個人がすべての職務を遂行できる組織に適している場合があります。 その他のプライバシーロールを使用すると、より詳細な制御を行い、選択した機能にユーザーを割り当てることができます。

役割グループとアクセスを許可する方法の詳細については、「ユーザーのアクセス許可を設定し、Priva で役割を割り当てる」 [を参照してください](priva-permissions.md)。

## <a name="step-4-start-finding-and-visualizing-your-data"></a>手順 4: データの検索と視覚化を開始する

Priva にサインインすると、[概要] ページが **表示** されます。 このページでは、Microsoft 365 環境での個人データの進化に関する動的な分析情報を提供し、問題をすばやく特定し、リスク 指標を特定し、問題を解決するためのアクションを実行するのに役立ちます。 [概要] には、サインアップの最初の 24 時間以内に最初の分析情報を入力する必要があります。 Priva を引き続き使用すると、概要ページが更新され、現在の情報が提供されます。

データに関する時間の詳細な分析のために、データ プロファイル ページは、より多くの視覚化と分析を提供し、地理的な場所と場所別に組織のデータを全体的にMicrosoft 365します。

これらのページの詳細については、「Priva で個人データを検索 [して視覚化する」を参照してください](priva-data-profile.md)。

## <a name="step-5-start-managing-risks-with-default-policies"></a>手順 5: 既定のポリシーを使用してリスクの管理を開始する

プライバシー リスク管理は、データの評価を開始し、データの最小化、データの過剰露出、およびデータ転送に関する重要なリスク シナリオを確認します。 これらのポリシーは既定で有効になっています。 これらのポリシーを使用して、リスクの場所を評価し、ユーザーに対するユーザーの電子メール通知を有効にし、ユーザーの注意に問題を引き出し、これらのリスクの修復を導きます。 さらに、提供されるポリシー テンプレートから独自のポリシーを作成およびカスタマイズできます。 法律顧問と協議して特定される可能性がある組織の法的および規制上のコンプライアンスニーズを満たしたポリシーを調整できます。 詳細については、「プライバシー リスク管理 [でポリシーを作成する」を参照してください](risk-management-policies.md)。

## <a name="step-6-get-started-with-subject-rights-requests"></a>手順 6: サブジェクト権限要求の使用を開始する

Priva Subject Rights Requests は、サブジェクト権限要求のフルフィルメント プロセスを自動化し、既存のビジネス プロセスに適合するデータとカスタマイズ可能なワークフローに簡単にアクセスできます。 関連するデータを簡単に検索し、結果を確認し、レポートを作成できます。 その途中で、組織内の他の専門家と安全に共同作業を行い、件名の権利要求を完了できます。 組み込みのテンプレートを使用して、ビジネス ワークフローを管理およびカスタマイズすることもできます。 これらの機能の使用の詳細については、「 [Priva Subject Rights Requestsについて」を参照してください](subject-rights-requests.md)。

## <a name="legal-disclaimer"></a>法的免責事項

[Microsoft Priva の法的免責事項](priva-disclaimer.md)

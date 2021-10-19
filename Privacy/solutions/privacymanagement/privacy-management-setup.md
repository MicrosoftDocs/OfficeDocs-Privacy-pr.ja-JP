---
title: プライバシー管理の使用を開始する
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
- MET150fcf
description: 組織のプライバシー管理を設定し、役割とアクセス許可を設定し、重要な設定を構成する方法について説明します。
ms.openlocfilehash: 0f64c581fbeb13726ee9ca2a0f695a5d4f55eb97
ms.sourcegitcommit: 85e085eb17af8b4efd1f45207445e1b3c3679600
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/19/2021
ms.locfileid: "60478194"
---
# <a name="get-started-with-privacy-management"></a>プライバシー管理の使用を開始する

プライバシー リスクの特定と軽減に関する支援のために Microsoft プライバシー管理の使用を開始する準備が整った場合は、次の手順に従って前提条件を設定し、プライバシーに関する分析情報の探索を開始してください。

## <a name="step-1-confirm-subscriptions-and-licensing"></a>手順 1: サブスクリプションとライセンスを確認する

プライバシー管理は、Microsoft 365 コンプライアンス センター内[で](https://compliance.microsoft.com/)利用できます。次のライセンスを持つ組織が購入できます。

- Microsoft 365 E3、E5、A3、A5
- Office 365 E1 E3、E5、A1、A3、A5

プライバシー管理は、ソリューションの 2 つの異なるモジュール (リスクとサブジェクト権限の要求) のライセンス オプションを提供します。 これらは個別または一緒に購入できます。 サブジェクト権限要求のライセンスを取得する場合は、処理する必要がある要求の数に応じて適切なライセンス層を選択できます。 追加の要求は、いつでも購入できます。

ライセンスのガイダンスに関する詳細については、「[セキュリティとコンプライアンスのための Microsoft 365 ライセンス ガイダンス](/office365/servicedescriptions/microsoft-365-service-descriptions/microsoft-365-tenantlevel-services-licensing-guidance/microsoft-365-security-compliance-licensing-guidance#privacy-management)」を参照してください。

> [!Note]
> プライバシー管理は、米国政府機関 (Community) (GCC) GCC高、または国防総省 (DoD) のお客様には利用できません。

### <a name="get-free-trial-license"></a>無料試用版ライセンスを取得する

無料試用版ライセンスは、プライバシー管理の開始に使用できます。 参加資格と参加方法については、「無料のプライバシー管理試用版について」 [を参照してください](privacy-management-trial.md)。

## <a name="step-2-enable-the-microsoft-365-audit-log"></a>手順 2: 監査ログMicrosoft 365有効にする

Microsoft 365監査ログは、組織内のすべてのアクティビティの概要です。 プライバシー管理ポリシーは、これらのアクティビティを使用してポリシーの分析情報を生成する場合があります。

組織で既に監査ログが有効になっている可能性があります。 初めて使用を開始する必要がある場合は、「監査ログ[](/microsoft-365/compliance/turn-audit-log-search-on-or-off)の検索をオンまたはオフにする」を参照して、監査を有効にする手順について説明します。 監査を有効にすると、監査ログの準備中で、準備が完了してから数時間で検索を実行できるというメッセージが表示されます。 このアクションを行う必要があるのは 1 回だけです。 監査ログの使用のMicrosoft 365詳細については、「監査ログの検索[」を参照してください](/microsoft-365/compliance/search-the-audit-log-in-security-and-compliance)。

## <a name="step-3-set-user-permissions-and-assign-roles"></a>手順 3: ユーザーのアクセス許可を設定し、役割を割り当てる

プライバシー管理では、役割ベースのアクセス制御 (RBAC) アクセス許可モデルを使用します。 役割が割り当てられているユーザーだけがプライバシー管理にアクセスできます。各ユーザーが許可するアクションは、役割の種類によって制限されます。

グローバル管理者には、プライバシー管理にアクセスし、他のユーザーを役割に割り当てる権限があります。 ユーザーは、サインインして、プライバシー管理用のMicrosoft 365 コンプライアンス センター[アクセス許可](https://compliance.microsoft.com/)を設定できます。 クイック スタートとして、プライバシー管理役割グループには、プライバシー管理のすべての機能にアクセスするためのアクセス許可があります。 このグループは、同じ個人がプライバシー管理ソリューション内のすべての職務を遂行できる組織に適している可能性があります。 その他のプライバシーロールを使用すると、より詳細な制御を行い、選択した機能にユーザーを割り当てることができます。

役割グループとアクセスを許可する方法の詳細については、「ユーザーアクセス許可の設定と役割の割り当て [」を参照してください](privacy-management-permissions.md)。

## <a name="step-4-start-finding-and-visualizing-your-data"></a>手順 4: データの検索と視覚化を開始する

プライバシー管理にサインインすると、[概要] ページが **表示** されます。 このページでは、Microsoft 365 環境での個人データの進化に関する動的な分析情報を提供し、問題をすばやく特定し、リスク 指標を特定し、問題を解決するためのアクションを実行するのに役立ちます。 [概要] には、サインアップの最初の 24 時間以内に最初の分析情報を入力する必要があります。 プライバシー管理を引き続き使用すると、概要ページが更新され、現在の情報が提供されます。

データに関する時間の詳細な分析のために、データ プロファイル ページは、より多くの視覚化と分析を提供し、地理的な場所および Microsoft 365 場所別に組織のデータを全体的に表示します。

これらのページの詳細については、「データを検索して [視覚化する」を参照してください](privacy-management-data-profile.md)。

## <a name="step-5-start-managing-risks-with-default-policies"></a>手順 5: 既定のポリシーを使用してリスクの管理を開始する

プライバシー管理は、データの評価を開始し、データの最小化、データの過剰露出、およびデータ転送に関する重要なリスク シナリオを確認します。 これらのポリシーは既定で有効になっています。 これらのポリシーを使用して、リスクの場所を評価し、ユーザーに対するユーザーの電子メール通知を有効にし、ユーザーの注意に問題を引き出し、これらのリスクの修復を導きます。 さらに、提供されるポリシー テンプレートから独自のポリシーを作成およびカスタマイズできます。 法律顧問と協議して特定される可能性がある組織の法的および規制上のコンプライアンスニーズを満たしたポリシーを調整できます。 詳細については、「プライバシー管理の [ポリシーを使用してプライバシー リスクを管理する」を参照してください](privacy-management-policies.md)。

## <a name="step-6-get-started-with-subject-rights-requests"></a>手順 6: サブジェクト権限要求の使用を開始する

プライバシー管理は、既存のビジネス プロセスに適合するデータとカスタマイズ可能なワークフローに簡単にアクセスして、件名の権利要求フルフィルメント プロセスを自動化します。 関連するデータを簡単に検索し、結果を確認し、レポートを作成できます。 その途中で、組織内の他の専門家と安全に共同作業を行い、件名の権利要求を完了できます。 組み込みのテンプレートを使用して、ビジネス ワークフローを管理およびカスタマイズすることもできます。 これらの機能の使用の詳細については、「対象権限要求の [管理」を参照してください](privacy-management-subject-rights-requests.md)。

## <a name="legal-disclaimer"></a>法的免責事項

[プライバシー管理の法的免責事項](privacy-management-disclaimer.md)

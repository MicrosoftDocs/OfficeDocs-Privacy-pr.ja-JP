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
description: 組織のMicrosoft Privaを設定し、ロールとアクセス許可を設定し、重要な設定を構成する方法について説明します。
ms.openlocfilehash: 945cbfd2625be50cb89eeaa8fe09e0effaea79d5
ms.sourcegitcommit: 3c27ecf7c86c8a3db38cae8819fc090eed192b4f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/25/2022
ms.locfileid: "65678214"
---
# <a name="get-started-with-priva"></a>Priva の使用を開始する

組織でプライバシー リスクを特定して軽減するためにMicrosoft Privaの使用を開始する準備ができたら、次の手順に従ってセットアップを行います。

## <a name="confirm-subscriptions-and-licensing"></a>サブスクリプションとライセンスを確認する

Privaは[Microsoft Purview コンプライアンス ポータル](https://compliance.microsoft.com/)内で使用でき、次のライセンスを持つ組織が購入できます。

- Microsoft 365 E3、E5、A3、A5
- Office 365 E1、E3、E5、A1、A3、A5

Privaには、Priva プライバシー リスク管理とPriva 主体の権利要求という 2 つの異なるソリューションのライセンス オプションが用意されています。 これらは個別に購入することも、まとめて購入することもできます。 サブジェクト権利要求のライセンスを取得する場合は、処理する必要がある要求の数に対して適切なライセンスレベルを選択できます。 追加の要求はいつでも購入できます。

ライセンスのガイダンスに関する詳細については、「[セキュリティとコンプライアンスのための Microsoft 365 ライセンス ガイダンス](/office365/servicedescriptions/microsoft-365-service-descriptions/microsoft-365-tenantlevel-services-licensing-guidance/microsoft-365-security-compliance-licensing-guidance#microsoft-priva)」を参照してください。

> [!Note]
> Privaは、米国政府Community (GCC) Moderate、GCC High、または国防総省 (DoD) のお客様にはご利用いただけません。

### <a name="start-a-free-trial"></a>無料試用版を開始する

無料試用版サブスクリプションを使用して、両方のPriva ソリューションのすべての機能を調べます。 [Priva試用版](priva-trial.md)にサインアップする方法について説明します。

## <a name="enable-the-microsoft-365-audit-log"></a>Microsoft 365監査ログを有効にする

Microsoft 365監査ログは、組織内のすべてのアクティビティの概要です。 プライバシー リスク管理ポリシーは、ポリシー分析情報を生成するためにこれらのアクティビティを使用する場合があります。

組織で監査ログが既に有効になっている可能性があります。 初めて使用を開始する必要がある場合は、「 [監査ログの検索を有効または無効にする」](/microsoft-365/compliance/turn-audit-log-search-on-or-off) を参照して、監査を有効にする詳細な手順を確認してください。 監査を有効にすると、監査ログの準備中で、準備が完了してから数時間で検索を実行できるというメッセージが表示されます。 このアクションを行う必要があるのは 1 回だけです。 Microsoft 365監査ログの使用の詳細については、「[監査ログを検索する」を](/microsoft-365/compliance/search-the-audit-log-in-security-and-compliance)参照してください。

## <a name="set-user-permissions-and-assign-roles"></a>ユーザー権限の設定とロールの割り当て

Privaは、ロールベースのアクセス制御 (RBAC) アクセス許可モデルを使用します。 ロールが割り当てられているユーザーのみがPrivaにアクセスでき、各ユーザーが許可するアクションはロールの種類によって制限されます。

グローバル管理者には、Privaにアクセスし、他のユーザーをロールに割り当てるアクセス許可があります。 Privaの[Microsoft Purview コンプライアンス ポータル](https://compliance.microsoft.com/)でサインインし、ユーザーのアクセス許可を設定できます。 クイック スタートのために、Privacy Management ロール グループには、Privaのすべての機能にアクセスするためのアクセス許可があります。 このグループは、同じ個人がすべての職務を遂行できる組織に適している可能性があります。 他のプライバシー ロールを使用すると、より詳細な制御を行い、選択した機能にユーザーを割り当てることができます。

ロール グループとアクセスを許可する方法の詳細については、「[Privaでユーザーのアクセス許可を設定し、ロールを割り当てる](priva-permissions.md)」を参照してください。

## <a name="start-finding-and-visualizing-your-data"></a>データの検索と視覚化を開始する

Privaにサインインすると、[**概要**] ページが表示されます。 このページでは、Microsoft 365環境での個人データの進化に関する動的な分析情報を提供し、問題をすばやく特定し、リスク インジケーターを特定し、問題を解決するためのアクションを実行するのに役立ちます。 概要には、サインアップ後最初の 24 時間以内に初期分析情報を入力する必要があります。 Privaを引き続き使用すると、概要ページが更新され、現在の情報が引き続き提供されます。

時間の経過に伴うデータの詳細な分析情報を得るための **データ プロファイル** ページでは、より多くの視覚化と分析が提供され、地理的な場所とMicrosoft 365場所別に組織のデータを包括的に把握できます。

これらのページの詳細については、「[Privaで個人データを検索して視覚化する](priva-data-profile.md)」を参照してください。

## <a name="start-managing-risks-with-default-policies"></a>既定のポリシーを使用してリスクの管理を開始する

プライバシー リスク管理は、データの評価を開始し、データの最小化、データの露出過剰、およびデータ転送に関する重要なリスク シナリオについて説明します。 これらのポリシーは既定で有効になっています。 これらのポリシーを使用して、リスクの場所を評価し、ユーザーに対してユーザーの電子メール通知を有効にして、問題を注意に向けて提起し、これらのリスクの修復をガイドすることができます。 また、指定されたポリシー テンプレートから独自のポリシーを作成してカスタマイズすることもできます。 法的助言者と相談して特定できる場合に、組織の法的および規制上のコンプライアンスのニーズに合わせてポリシーを調整できます。 詳細については、「 [プライバシー リスク管理でポリシーを作成する」を](risk-management-policies.md)参照してください。

## <a name="get-started-with-subject-rights-requests"></a>サブジェクト権限要求を使用した概要

Priva 主体の権利要求は、サブジェクト権限要求フルフィルメント プロセスを自動化し、既存のビジネス プロセスに適合するデータとカスタマイズ可能なワークフローに簡単にアクセスできるようにします。 関連するデータを簡単に見つけ、結果を確認し、レポートを作成できます。 その過程で、組織内の他の専門家と安全に共同作業して、サブジェクトの権利要求を完了できます。 また、組み込みのテンプレートを使用してビジネス ワークフローを管理およびカスタマイズすることもできます。 これらの機能の使用の詳細については、「[Priva 主体の権利要求の詳細](subject-rights-requests.md)」を参照してください。

## <a name="priva-availability"></a>可用性のPriva

Microsoft Privaは世界中のお客様が利用できます。 組織がデータ所在地の要件を満たすために次に示すローカル データ センターのいずれかでテナントをプロビジョニングした場合、Priva ソリューションはMicrosoft Purview コンプライアンス ポータルの左側のナビゲーションでは利用できません。

- ノルウェー
- ポーランド
- カタール
- シンガポール
- 南アフリカ
- 韓国
- スペイン
- スウェーデン
- スイス
- アラブ首長国連邦

## <a name="legal-disclaimer"></a>法的免責事項

[Microsoft Priva法的免責事項](priva-disclaimer.md)

---
title: Priva Subject Rights Requests の詳細
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
description: Microsoft Priva の Subject Rights Requests ソリューションは、個人データを検索し、コンテンツのレビューとレポートの作成に関して共同作業を行う際に役立ちます。
ms.openlocfilehash: 25eb785651ec0edd1035aba54b20d19404619b80
ms.sourcegitcommit: 02921b2dd438a517191522567908046b136a89e2
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/23/2022
ms.locfileid: "63758446"
---
# <a name="learn-about-priva-subject-rights-requests"></a>Priva Subject Rights Requests の詳細

世界中の特定のプライバシー規制に従って、個人 (またはデータ *主体) は*、企業が収集した個人データを確認または管理する要求を行う場合があります。 これらの要求は、データ主体要求 (DSR)、データ主体アクセス要求 (DSAR)、またはコンシューマー権限要求とも呼ばれます。 大量の情報を保存する企業では、関連するデータを見つけることは、大きな作業になります。

Microsoft Priva は、Subject Rights Requests ソリューションを通じてこれらの問い合わせを処理するのに役立ちます。 対象データの検索、結果の確認、適切なファイルの収集、レポートの作成を支援するワークフロー、自動化、およびコラボレーション機能を提供します。

## <a name="how-priva-supports-subject-rights-request-fulfillment"></a>Priva がサブジェクト権限要求のフルフィルメントをサポートする方法

件名の要求サイクルは、組織に対する個人の要求から始まります。 受信すると、Priva の機能を使用して、そのデータの収集、共同作業、レビュー、レポートの作成を行います。 その後、データ主体に調査結果を通知し、データの削除など、要求を満たすために Priva の外部で必要なその他のアクションを実行できます。 途中でワークフローを管理および自動化するために、統合されたテンプレートをPower Automateすることもできます。

### <a name="create-requests-and-collect-data"></a>要求を作成してデータを収集する

Priva には、組織がデータ に保存しているコンテンツ内のデータ主体に関連するデータを検索するための強力な検索Microsoft 365。 また、これらの要求に対して収集したデータ内で確認するアイテムの優先順位付けにも役立ちます。 Priva は、機密Microsoft Information Protection可能性のあるコンテンツを示し、特別なレビューを必要とする可能性がある機密ラベルを認識し、アイテムにこれらのラベルをフラグします。 さらに、Priva は、複数のユーザーのデータを含む可能性のあるアイテムを検出してフラグを設定できます。そこで、データ主体にコンテンツを提供する前にコンテンツをやり直す必要がある場合があります。

詳細については、「サブジェクト権限要求 [を作成する」を参照してください](subject-rights-requests-create.md)。

### <a name="data-matching"></a>データの照合

データ照合を使用すると、Priva が指定された正確なデータ値に基づいてデータ主体を識別できます。 この種類の情報をアップロードすると、コンテンツの検索精度が向上し、サブジェクト権限要求の作成時にフィールドを手動で指定する必要が簡素化されます。 また、件名権限要求内のコンテキストと、データ主体のコンテンツが最も多いアイテムを紹介する [概要] タイルも提供します。 詳細については、「Subject [Rights Requests のデータ一致」を参照してください](subject-rights-requests-data-match.md)。

### <a name="review-data-and-collaborate-on-requests"></a>データを確認し、要求に対して共同作業する

データが収集された後、結果を評価し、レポートとエクスポートに含める最も関連性の高いアイテムを選択し、必要なやり直しを行います。 これは、Subject Rights Requests パイプライン内のチーム メンバー間で共同で実行できます。

詳細については、「対象権限要求 [のデータを確認する」を参照してください](subject-rights-requests-data-review.md)。

### <a name="fulfill-requests"></a>要求を満たす

Priva では、レポートを作成し、データ主体に送り返すファイルを収集するためのツールを提供します。 詳細については、「レポートを生成 [し、件名の権利要求を満たす」を参照してください](subject-rights-requests-reports.md)。

### <a name="automate-tasks"></a>自動タスク

組み込みのテンプレートを使用して、Priva 内でワークフロー プロセスをPower Automateできます。 これらのテンプレートは、ServiceNow でのチケットの提出や予定表の招待の設定など、タスクをサポートします。 詳細については、「Subject [Rights Requests」の「タスクの自動化」を参照してください](subject-rights-requests-automate.md)。

## <a name="legal-disclaimer"></a>法的免責事項

[Microsoft Priva の法的免責事項](priva-disclaimer.md)

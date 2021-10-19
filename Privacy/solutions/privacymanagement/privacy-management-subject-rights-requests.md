---
title: プライバシー管理における件名の権利要求の詳細
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
description: プライバシー管理のサブジェクト権限要求領域は、個人データを検索し、コンテンツのレビューとレポートの作成に関して共同作業を行う際に役立ちます。
ms.openlocfilehash: 7809f3a9dbf40b1cc0c745f710a3831ce6cf77ca
ms.sourcegitcommit: 85e085eb17af8b4efd1f45207445e1b3c3679600
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/19/2021
ms.locfileid: "60478433"
---
# <a name="learn-about-subject-rights-requests"></a>件名の要求の詳細

世界中の特定のプライバシー規制に従って、個人 (またはデータ *主体)* は、企業が収集した個人データを確認または管理する要求を行う場合があります。 これらの要求は、データ主体要求 (DSRs)、データ主体アクセス要求 (DSA)、またはコンシューマー権限要求とも呼ばれます。 大量の情報を保存する企業では、関連するデータを見つけることは、大きな作業になります。

プライバシー管理は、サブジェクト権限の要求を通じてこれらの問い合わせを処理するのに役立ちます。 対象データの検索、結果の確認、適切なファイルの収集、レポートの作成を支援するワークフロー、自動化、およびコラボレーション機能を提供します。

## <a name="how-privacy-management-supports-subject-rights-request-fulfillment"></a>プライバシー管理がサブジェクト権限要求のフルフィルメントをサポートする方法

件名の要求サイクルは、組織に対する個人の要求から始まります。 受信すると、プライバシー管理の機能を使用して、そのデータの収集、共同作業、レビュー、レポートの作成を行います。 その後、データ主体に調査結果を通知し、データの削除など、要求を満たすためにプライバシー管理の外部で必要なその他のアクションを実行できます。 途中でワークフローを管理および自動化するために、プライバシー管理の統合されたテンプレートPower Automateすることもできます。

![件名の要求のワークフロー。](../../media/privacy-management-srr-cycle.png)

### <a name="create-requests-and-collect-data"></a>要求を作成してデータを収集する

プライバシー管理は、組織がコンテンツに保存しているコンテンツ内のデータ主体に関連するデータを検索するための強力な検索Microsoft 365。 また、これらの要求に対して収集したデータ内で確認するアイテムの優先順位付けにも役立ちます。 プライバシー管理では、機密ラベルMicrosoft Information Protection、特別なレビューが必要な可能性のあるコンテンツを示す機密ラベルを認識し、これらのラベルでアイテムにフラグを設定します。 さらに、プライバシー管理では、複数のユーザーのデータを含む可能性のあるアイテムを検出してフラグを設定できます。データ主体にコンテンツを提供する前にコンテンツをやり直す必要がある場合があります。

詳細については、「サブジェクト権限要求 [を作成する」を参照してください](privacy-management-subject-rights-requests-create.md)。

### <a name="data-matching"></a>データの照合

データ照合を使用すると、プライバシー管理を有効にして、提供された正確なデータ値に基づいてデータ主体を識別できます。 この種類の情報をアップロードすると、コンテンツの検索精度が向上し、サブジェクト権限要求の作成時にフィールドを手動で指定する必要が簡素化されます。 また、件名権限要求内のコンテキストと、データ主体のコンテンツが最も多いアイテムを紹介する [概要] タイルも提供します。 詳細については、「データ一致の [管理」を参照してください](privacy-management-subject-rights-requests-data-matching.md)。

### <a name="review-data-and-collaborate-on-requests"></a>データを確認し、要求に対して共同作業する

データが収集された後、結果を評価し、レポートとエクスポートに含める最も関連性の高いアイテムを選択し、必要なやり直しを行います。 これは、プライバシー管理パイプライン内のチーム メンバー間で共同で実行できます。
詳細については、「件名の権限要求 [に関するレビューと共同作業」を参照してください](privacy-management-subject-rights-requests-review.md)。

### <a name="fulfill-requests"></a>要求を満たす

プライバシー管理では、レポートを作成し、データ主体に送り返すファイルを収集するためのツールを提供します。 詳細については、「対象権限要求のエクスポートを管理し、要求を [満たす」を参照してください](privacy-management-subject-rights-requests-fulfill.md)。

### <a name="automate-tasks"></a>自動タスク

組み込みのテンプレートを使用して、プライバシー管理内でワークフロー プロセスをPower Automateできます。 これらのテンプレートは、ServiceNow でのチケットの提出や予定表の招待の設定など、タスクをサポートします。 詳細については、「サブジェクト権限要求 [タスクの自動化」を参照してください](privacy-management-subject-rights-requests-automate-tasks.md)。

## <a name="legal-disclaimer"></a>法的免責事項

[プライバシー管理の法的免責事項](privacy-management-disclaimer.md)

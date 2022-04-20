---
title: Priva Subject Rights Requests について学習する
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
description: Microsoft Priva の Subject Rights Requests ソリューションは、個人データを見つけ、コンテンツのレビューとレポートの作成に関する共同作業に役立ちます。
ms.openlocfilehash: 37ee3fc795559d216a7a8cd620cff2c3ca689c2b
ms.sourcegitcommit: 09ecdaded9a9f8f79587f2acb978dc53b83e5c01
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/19/2022
ms.locfileid: "64930628"
---
# <a name="learn-about-priva-subject-rights-requests"></a>Priva Subject Rights Requests について学習する

世界中の特定のプライバシー規制に従って、個人 (または *データ主体*) は、企業が収集した個人に関する個人データの確認または管理を要求する場合があります。 これらの要求は、データ主体要求 (DSR)、データ主体アクセス要求 (DSAR)、またはコンシューマー権限要求とも呼ばれます。 大量の情報を格納する企業の場合、関連するデータを見つけることは手ごわい作業になる可能性があります。

Microsoft Priva は、サブジェクト権利要求ソリューションを通じて、これらの問い合わせを処理するのに役立ちます。 これにより、件名データの検索、結果の確認、適切なファイルの収集、レポートの作成を支援するワークフロー、自動化、コラボレーション機能が提供されます。

## <a name="how-priva-supports-subject-rights-request-fulfillment"></a>Priva がサブジェクト権利要求のフルフィルメントをサポートする方法

サブジェクト権利要求サイクルは、組織に対する個人の要求から始まります。 受信したら、Priva の機能を使用して、そのデータの収集、共同作業、レビュー、レポートの作成を行うことができます。 その後、結果のデータ主体に通知し、データの削除など、要求を満たすために Priva の外部で必要なその他のアクションを実行できます。 ワークフローの管理と自動化を支援するために、統合されたPower Automate テンプレートを使用することもできます。

### <a name="create-requests-and-collect-data"></a>要求を作成してデータを収集する

Priva には、組織がMicrosoft 365に保存するコンテンツ内のデータ主体に関連するデータを検索するための強力な検索オプションが用意されています。 また、これらの要求に対して収集したデータ内でレビューする項目に優先順位を付ける場合にも役立ちます。 Priva は Microsoft Purview Information Protectionの秘密度ラベルを認識しています。これは、機密性が高く、特別なレビューが必要になる可能性のあるコンテンツを示し、これらのラベルでアイテムにフラグを設定します。 さらに、Priva は、複数のユーザーのデータを含む可能性のあるアイテムを検出してフラグを設定できます。データ主体にコンテンツを提供する前にコンテンツをやり直す必要がある場合があります。

詳細については、「 [サブジェクト権限要求を作成する](subject-rights-requests-create.md)」を参照してください。

### <a name="data-matching"></a>データ一致

データマッチングを使用すると、Priva が正確に指定されたデータ値に基づいてデータ主体を識別できるようにします。 この種類の情報をアップロードすると、コンテンツの検索の精度が向上し、サブジェクト権利要求の作成時にフィールドを手動で指定する必要性が簡素化されます。 また、サブジェクトの権利要求内と、データ主体のコンテンツが最も多いアイテムを示す [概要] タイルのコンテキストも提供されます。 詳細については、「 [サブジェクト権利要求のデータ照合](subject-rights-requests-data-match.md)」を参照してください。

### <a name="review-data-and-collaborate-on-requests"></a>データを確認し、要求に対して共同作業する

データが収集されたら、結果を評価し、レポートとエクスポートに含める最も関連性の高い項目を選択し、必要なやり直しを行うことができます。 これは、Subject Rights Requests パイプライン内のチーム メンバー間で共同で行うことができます。

詳細については、「 [サブジェクト権限要求のデータを確認する](subject-rights-requests-data-review.md)」を参照してください。

### <a name="fulfill-requests"></a>要求をフルフィルメントする

Priva には、レポートを作成し、データ主体に返送するファイルを収集するためのツールが用意されています。 詳細については、「レポートを [生成し、サブジェクト権限要求を満たす](subject-rights-requests-reports.md)」を参照してください。

### <a name="automate-tasks"></a>自動タスク

組み込みのPower Automate テンプレートを使用して、Priva 内でワークフロー プロセスを作成および自動化できます。 これらのテンプレートは、ServiceNow でのチケットの提出や予定表の招待の設定などのタスクをサポートします。 詳細については、「 [Subject Rights Requests のタスクを自動化する](subject-rights-requests-automate.md)」を参照してください。

## <a name="legal-disclaimer"></a>法的免責事項

[Microsoft Priva の法的免責事項](priva-disclaimer.md)

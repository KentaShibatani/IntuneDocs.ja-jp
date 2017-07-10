---
title: "ロールアウト コミュニケーション計画の作成"
description: "この記事では、Microsoft Intune クラウドのみの設計および実装で、ロールアウトの情報伝達計画を立てる方法について説明します。"
keywords: 
author: andredm7
ms.author: andredm
manager: angrobe
ms.date: 06/13/2016
ms.topic: article
ms.prod: 
ms.service: microsoft-intune
ms.technology: 
ms.assetid: 393ebe75-d001-485a-b81c-6361c8b5e6ee
ms.reviewer: jeffbu, cgerth
ms.suite: ems
ms.custom: intune-classic
ms.translationtype: Human Translation
ms.sourcegitcommit: 1911c8a2460a98218027c40a26d81f1ca4c482f5
ms.openlocfilehash: 1443f8b8ca45fbf4880d0ebf57e5cd2657f8c261
ms.contentlocale: ja-jp
ms.lasthandoff: 06/13/2017


---

# <a name="develop-a-rollout-communication-plan"></a>ロールアウト コミュニケーション計画の作成

[!INCLUDE[note for both-portals](./includes/note-for-both-portals.md)]

前のセクションでは、Intune 管理の対象となる組織グループ、Intune ロールアウトの期間、登録オプションなどの特定について説明しました。 次に、Intune ロールアウトの情報伝達計画を立てる必要があります。 Intune ロールアウトの情報伝達計画には、次の 4 つの領域を含める必要があります。

-   伝達する情報

-   伝達に使用する配信方法

-   情報を受け取るユーザー

-   情報伝達のタイムライン

それぞれの領域について詳しく説明します。

## <a name="what-needs-to-be-communicated"></a>伝達する必要がある情報

伝達する情報は、Intune ロールアウト プロセスのどの段階で伝達するかによって異なります。 組織によっては、Intune ロールアウトのキックオフ、登録前、登録後の順に、組織グループとユーザーに段階的に伝達する場合があります。 各段階で伝達される可能性がある情報の種類について説明します。

**キックオフ段階:** Intune プロジェクト自体について概要を説明する広範な情報伝達。Intune の概要、Intune を採用する理由 (組織とユーザーにとっての利点など)、展開とロールアウトに関する作業の計画概要などの領域の情報があります。

**登録前段階:** Intune と補助的なサービス (Office、Outlook、OneDrive など) に関する情報、組織グループとユーザーが Intune を受け取る予定に関するユーザー リソースと具体的なタイムラインを含む広範な情報伝達。

**登録段階:** Intune を受け取る予定の組織グループ/ユーザーを対象にした情報伝達。Intune を受け取る準備が整ったことをユーザーに知らせ、登録手順と、サポートや質問の窓口に関する情報を伝えます。

**登録後段階:** Intune に登録された組織グループ/ユーザーを対象にした情報伝達。ユーザーに役立つ追加のリソースを提供し、登録時と登録後の使用感に関するフィードバックを収集します。

## <a name="communication-delivery-methods"></a>情報の配信方法

Intune ロールアウトに関する情報を対象となる組織グループとユーザーに伝達するには、いくつかの配信方法があります。 次の一覧では、情報の配信方法の例とその方法を使用する段階を示しています。

-   組織全体を対象にした対面の会議または Skype 会議 (キックオフ段階)

-   電子メール (登録前段階、登録段階、登録後段階)

-   組織の Web サイト (すべての段階)

-   Yammer、ポスター、チラシ (キックオフ段階、登録前段階)

## <a name="communications-timeline"></a>情報伝達のタイムライン

伝達する内容と情報伝達方法を決めたら、次の手順は、情報を伝達するタイミングと相手など、情報伝達のタイムラインを決めることです。 たとえば、最初の Intune プロジェクト キックオフの情報伝達は、組織全体または一部のみを対象にして、Intune ロールアウトを開始する数週間前に行います。 次に、Intune ロールアウト スケジュールに合わせて組織グループとユーザーに段階的に伝えます。 次の例は、Intune ロールアウトの情報伝達の大まかな計画のサンプルです。

  | **情報伝達計画** | **7 月** | **8 月** | **9 月** | **10 月** |
|:---:|:---:|:---:|:---:|:---:|
| 段階 1  | すべて |  |  |  |                                                         
| キックオフ会議 | 第 1 週 |  |  |  |                                                         
| 段階 2 | IT 部門 | 営業/マーケティング | 小売 | 人事、財務、幹部 |
| ロールアウト前電子メール 1 | 第 1 週 | 第 1 週 | 第 1 週 | 第 1 週 |
| 段階 3 | IT 部門 | 営業/マーケティング | 小売 | 人事、財務、幹部 |
| ロールアウト前電子メール 2 | 第 2 週 | 第 2 週 | 第 2 週 | 第 2 週 |
| 段階 4 | IT 部門 | 営業/マーケティング | 小売 | 人事、財務、幹部 |
| 登録電子メール | 第 3 週 | 第 3 週 | 第 3 週 | 第 3 週 |
| 段階 5 | IT 部門 | 営業/マーケティング | 小売 | 人事、財務、幹部 |
| 登録後電子メール | 第 4 週 | 第 4 週 | 第 4 週 | 第 4 週 |

## <a name="next-section"></a>次のセクション

次のセクションは、[サポート計画](planning-guide-support-plan.md)を立てる場合のガイダンスです。

---
title: "Windows 情報保護を構成する - Intune"
titleSuffix: Intune Azure preview
description: "Intune Azure プレビュー: Windows 情報保護を管理するために使用できる Intune 設定について説明します。"
keywords: 
author: robstackmsft
ms.author: robstack
manager: angrobe
ms.date: 04/14/2017
ms.topic: article
ms.prod: 
ms.service: microsoft-intune
ms.technology: 
ms.assetid: f233672c-7d9b-4554-af1f-92c001a1a3c5
ms.reviewer: heenamac
ms.suite: ems
ms.custom: intune-azure
ms.translationtype: Human Translation
ms.sourcegitcommit: 9ff1adae93fe6873f5551cf58b1a2e89638dee85
ms.openlocfilehash: fc58b07fe33ff6223dfa182fb4f81f15379295fa
ms.contentlocale: ja-jp
ms.lasthandoff: 05/23/2017


---

# <a name="how-to-configure-windows-information-protection-in-microsoft-intune"></a>Microsoft Intune で Windows Information Protection を構成する方法

[!INCLUDE[azure_preview](./includes/azure_preview.md)]

企業内に従業員所有デバイスが増加するのに従い、企業のコントロールが届かない電子メール、ソーシャル メディア、パブリック クラウドなどのアプリやサービスを介して偶発的にデータが漏えいするリスクも増大しています。 たとえば、従業員が個人用の電子メール アカウントから最新のエンジニアリング画像を送信したり、製品情報をコピーしてツイートに貼り付けたり、作成中の営業レポートをパブリック クラウドの記憶域に保存したりするときなどです。

**Windows 情報保護**は、この潜在的なデータ漏えいの防止に役立ちます。それ以外の場合は従業員のエクスペリエンスを妨げることはありません。 また、企業が所有するデバイスと従業員が作業のために持ち込む個人用デバイスでもエンタープライズ アプリとデータを偶発的なデータ漏えいから保護します。既存の環境や他のアプリを変更する必要はありません。

この Intune ポリシーは、Windows 情報保護によって保護されているアプリ、エンタープライズ ネットワークの場所、保護レベル、および暗号化設定の一覧を管理します。

>[!NOTE]
> Windows 10 ポータル サイト アプリを Windows Information Protection とともに使用するには、ポータル サイト アプリを Windows Information Protection モードの**除外対象**に追加する必要があります。 

### <a name="next-steps"></a>次のステップ
詳細については、「[Protect your enterprise data using Windows Information Protection (Windows 情報保護を使用してエンタープライズ データを保護する)](https://technet.microsoft.com/itpro/windows/keep-secure/protect-enterprise-data-using-wip)」を参照してください。

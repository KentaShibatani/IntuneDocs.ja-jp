---
title: ユーザー デバイスの関連付け - Intune データ ウェアハウス
titlesuffix: Microsoft Intune
description: Intune のデータ ウェアハウス API の変更一覧。
keywords: Intune データ ウェアハウス
author: Erikre
ms.author: erikre
manager: dougeby
ms.date: 01/02/2018
ms.topic: article
ms.prod: ''
ms.service: microsoft-intune
ms.technology: ''
ms.assetid: 777484A7-09CE-4409-987F-76B3F87DFE93
ms.reviewer: aanavath
ms.suite: ems
ms.custom: intune-classic
ms.openlocfilehash: e78d2c75710b97ec67b64bd745629e7863778bd0
ms.sourcegitcommit: 5eba4bad151be32346aedc7cbb0333d71934f8cf
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/16/2018
---
# <a name="user-device-association"></a>ユーザー デバイスの関連付け

**UserDeviceAssociation** エンティティには、組織内のユーザー デバイスの関連付けが含まれています。


|        名前        |                                           説明                                            |        例         |
|--------------------|--------------------------------------------------------------------------------------------------|------------------------|
|      UserKey       |              データ ウェアハウス内のユーザーを示す一意識別子 (代理キー)。               |          123           |
|     DeviceKey      |                      データ ウェアハウス内のデバイスを示す一意識別子。                      |          123           |
| CreatedDateTimeUTC |           ユーザー デバイスの関連付けが作成されたときの日時。 UTC 形式を使用します。           | 11/23/2016 12:00:00 AM |
|     IsDeleted      | ユーザーがそのデバイスを登録解除し、その関連付けが最新でなくなったことを示します。 |       真/偽       |
|  EndedDateTimeUTC  |              IsDeleted が <strong>True</strong> に変更されたときの日時 (UTC)。               | 06/23/2017 12:00:00 AM |


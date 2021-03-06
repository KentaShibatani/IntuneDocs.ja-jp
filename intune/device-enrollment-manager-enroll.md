---
title: デバイス登録マネージャー アカウントを使用してデバイスを登録する
titlesuffix: Microsoft Intune
description: デバイス登録マネージャー アカウントを使用してデバイスを Intune に登録します。 "
keywords: ''
author: ErikjeMS
ms.author: erikje
manager: dougeby
ms.date: 02/22/2018
ms.topic: article
ms.prod: ''
ms.service: microsoft-intune
ms.technology: ''
ms.assetid: 7196b33e-d303-4415-ad0b-2ecdb14230fd
ms.reviewer: damionw
ms.suite: ems
ms.custom: intune-azure
ms.openlocfilehash: 870d61cce47132b19b4c3d8b7357f84a21a443e4
ms.sourcegitcommit: 5eba4bad151be32346aedc7cbb0333d71934f8cf
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/16/2018
---
# <a name="enroll-devices-by-using-a-device-enrollment-manager-account"></a>デバイス登録マネージャー アカウントを使用してデバイスを登録する

[!INCLUDE [azure_portal](./includes/azure_portal.md)]

組織は Intune を使用して、単一のユーザー アカウントで多数のモバイル デバイスを管理することができます。 *デバイス登録マネージャー (DEM)* アカウントは、最大で 1,000 台のデバイスを登録できる特別なユーザー アカウントです。 既存のユーザーを DEM アカウントに追加し、特別な DEM 機能を与えます。 登録される各デバイスは 1 つのライセンスを使用します。 このアカウントで登録したデバイスは、個人用 ("BYOD") デバイスではなく共有デバイスとして使用することをお勧めします。  

ユーザーをデバイス登録マネージャーとして追加するには、そのユーザーが [Azure Portal ](https://portal.azure.com)に存在する必要があります。 最適なセキュリティのために、DEM ユーザーを Intune 管理にも指定することは避けてください。

>[!NOTE]
>DEM による登録方法は、[Apple Configurator とセットアップ アシスタント](apple-configurator-setup-assistant-enroll-ios.md)、[Apple Configurator と直接登録](apple-configurator-direct-enroll-ios.md)、[Apple School Manager (ASM)](apple-school-manager-set-up-ios.md)、または [Device Enrollment Program (DEP)](device-enrollment-program-enroll-ios.md) という他の登録方法と一緒に使用することはできません。

## <a name="example-of-a-device-enrollment-manager-scenario"></a>デバイス登録マネージャーのシナリオの例

あるレストランで、接客担当スタッフが販売時点管理に使い、調理担当スタッフがオーダーのモニターに使う POS タブレットが 50 台必要になりました。 従業員は、会社のデータにアクセスしたり、ユーザーとしてサインインしたりする必要はありません。 Intune 管理者はデバイス登録マネージャー アカウントを作成し、レストランの監督者を DEM アカウントに追加します。 監督者は DEM の機能を使用できます。 これで監督者は DEM の資格情報を利用し、50 台のタブレット デバイスを登録できます。

[Azure Portal](https://portal.azure.com) 内のユーザーのみがデバイス登録マネージャーになることができます。 デバイス登録マネージャーのユーザーを Intune 管理者にすることはできません。

DEM ユーザーができること:

-   Intune に最大 1,000 台のデバイスを登録する
-   ポータル サイトにサインインして会社のアプリを取得する
-   タブレットにロール固有のアプリを展開することで、会社データへのアクセスを構成する

## <a name="limitations-of-devices-that-are-enrolled-with-a-dem-account"></a>DEM アカウントで登録されるデバイスの制限事項

デバイス登録マネージャー アカウントを使用して登録されているデバイスには、次の制限があります。

  - ユーザーごとのアクセスはできません。 デバイスには割り当てられたユーザーがないため、電子メールや会社のデータ アクセスがありません。 VPN 構成などを使用すれば、デバイス アプリがデータにアクセスすることはできます。
  - DEM ユーザーは、会社ポータルを使用して、デバイス自体で DEM 登録のデバイスを登録解除することはできません。 Intune 管理者は登録を解除できます。
  - ポータル サイト アプリまたは Web サイトには、ローカルのデバイスのみが表示されます。
  - アプリ管理のための Apple ID 要件がユーザー単位になるため、ユーザーはユーザー ライセンスで Apple Volume Purchase Program (VPP) アプリを利用することはできません。
  - (iOS のみ) DEM を利用して iOS デバイスを登録する場合は、Apple Configurator、Apple Device Enrollment Program (DEP)、または Apple School Manager (ASM) を利用してデバイスを登録することはできません。
  - (Android のみ) 1 つの DEM アカウントに登録できる Android for Work デバイスの数は限られています。 DEM アカウントごとに最大 10 台の Android の仕事用プロファイル デバイスを登録できます。 この制限は、従来の Android の登録には適用されません。
  - デバイスでは、デバイス ライセンスがある場合に VPP アプリをインストールすることができます。
  - 各デバイスには、デバイスのライセンスが必要です。 [ユーザーとデバイスのライセンス](licenses-assign.md#how-user-and-device-licenses-affect-access-to-services)の詳細についてはこちらです。


> [!NOTE]
> デバイス登録マネージャーによって管理されているデバイスに会社のアプリを展開できます。 **必須のインストール**としてポータル サイト アプリをデバイス登録マネージャーのユーザー アカウントに展開します。
> パフォーマンスを改善するために、DEM デバイスでポータル サイト アプリを表示すると、ローカル デバイスのみが表示されます。 その他の DEM デバイスのリモート管理は、Intune 管理コンソールからのみ実行できます。


## <a name="add-a-device-enrollment-manager"></a>デバイス登録マネージャーの追加

1.  [Azure Portal の Intune](https://aka.ms/intuneportal) で、**[デバイスの登録]** > **[デバイス登録マネージャー]** の順に選択します。

2.  **[追加]** を選択します。

3.  **[ユーザーの追加]** ブレードで、DEM ユーザーのユーザー プリンシパル名を入力し、**[追加]** を選択します。 DEM ユーザーが DEM ユーザーの一覧に追加されます。

## <a name="permissions-for-dem"></a>DEM のアクセス許可

DEM 登録タスクを実行するには、グローバル管理者または Intune サービス管理者の Azure AD ロールが必要です。 また、これらのロールは、カスタムのユーザー ロールに一覧表示され使用可能である RBAC のアクセス許可に関係なく、すべての DEM ユーザーを表示するのに必要です。 グローバル管理者または Intune サービス管理者のロールが割り当てられていないユーザーで、デバイス登録マネージャー ロールの読み取りアクセス許可を持つユーザーは、自分が作成した DEM ユーザーのみ表示できます。 これらの機能の RBAC ロールのサポートについては、今後発表される予定です。

ユーザーにグローバル管理者または Intune サービス管理者のロールが割り当てられていないが、デバイス登録マネージャー ロールが割り当てられていてその読み取りアクセス許可を持っているという場合は、そのユーザー自身が作成した DEM ユーザーのみ表示できます。

## <a name="remove-a-device-enrollment-manager"></a>デバイス登録マネージャーの削除

デバイス登録マネージャーを削除しても、登録済みのデバイスに影響はありません。 デバイス登録マネージャーを削除した場合は次のようになります。

-   登録済みデバイスは影響を受けず、引き続き完全に管理されます。
-   削除されたデバイス登録マネージャー アカウントの資格情報は有効なままです。
-   削除されたデバイス登録マネージャーでは、デバイスのワイプとインベントリからの削除を実行できません。
-   削除されたデバイス登録マネージャーは、Intune 管理者によって構成されたデバイスを、ユーザーあたりの上限数まで登録することのみできます。

**デバイス登録マネージャーを削除するには**

1. [Azure Portal の Intune](https://aka.ms/intuneportal) で、**[デバイスの登録]**、**[デバイス登録マネージャー]** の順に選びます。
2. **[デバイス登録マネージャー]** ブレードで、DEM ユーザーを選択し、**[削除]** を選択します。

## <a name="view-the-properties-of-a-device-enrollment-manager"></a>デバイス登録マネージャーのプロパティの表示

1. [Azure Portal](https://portal.azure.com) で、**[デバイスの登録]**、**[デバイス登録マネージャー]** の順に選びます。
2. **[デバイス登録マネージャー]** ブレードで、DEM ユーザーを右クリックし、**[プロパティ]** を選択します。

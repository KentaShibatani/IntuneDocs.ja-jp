---
title: "Intune 移行中にデバイス コンプライアンス ポリシーとアプリ管理ポリシーを構成する"
description: "この記事では、Intune 移行中にデバイスのコンプライアンス ポリシーとアプリ管理ポリシーを構成するために必要な手順について説明します。"
keywords: 
author: andredm7
ms.author: andredm
manager: angrobe
ms.date: 06/12/2017
ms.topic: article
ms.prod: 
ms.service: microsoft-intune
ms.technology: 
ms.assetid: 0062d08e-e5b3-4f73-8b64-5ad95adbe945
ms.reviewer: dagerrit
ms.suite: ems
ms.custom: intune-classic
ms.openlocfilehash: 5e848dda6643a28141a8f5f1d0bdc01f2bd9d390
ms.sourcegitcommit: 34cfebfc1d8b81032f4d41869d74dda559e677e2
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/01/2017
---
# <a name="configure-device-compliance-and-app-management-policies"></a>デバイス コンプライアンス ポリシーとアプリ管理ポリシーを構成する

[!INCLUDE[note for both-portals](./includes/note-for-both-portals.md)]

Intune 移行時の主な目標は、すべてのデバイスが登録されてポリシーに準拠することです。 デバイス ポリシーは企業が所有する単一ユーザーのデバイスの管理だけでなく、個人用 (BYOD) デバイスや共有デバイス (キオスク、店頭端末機器、教室で複数の学生が共有するタブレットなど)、またユーザーレス デバイス (iOS のみ) の管理に役立ちます。

デバイス プラットフォームごとに設定は異なりますが、Intune デバイス ポリシーは次のモバイル デバイス管理機能を提供することで、それぞれのデバイス プラットフォームで動作します。

-   各ユーザーが登録するデバイス数の制限。

-   デバイスの設定 (デバイス レベルの暗号化、パスワードの文字数、カメラの使用など) の管理。

-   アプリ、電子メール プロファイル、VPN プロファイルなどの提供。

-   セキュリティ コンプライアンス ポリシーのデバイス レベルの基準の評価。

> [!IMPORTANT]
> デバイス管理ポリシーは、個々のデバイスやユーザーに直接割り当てられるわけではなく、ユーザー グループに割り当てられます。 ユーザー グループにポリシーが直接適用されることにより、ユーザーのデバイスにポリシーが適用されます。あるいはデバイス グループにポリシーが適用されることにより、グループのメンバーにポリシーが適用されます。

## <a name="task-list-for-device-compliance-policies"></a>デバイス コンプライアンス ポリシーのタスク一覧

### <a name="task-1-add-device-groups-optional"></a>タスク 1: デバイス グループを追加する (省略可能)

ユーザー ID ではなくデバイス ID に基づいてさまざまな管理タスクを実行する必要がある場合に、デバイス グループを作成することができます。

デバイス グループは、専用ユーザーがいないデバイス (キオスク デバイス、交代勤務従業員が共有するデバイス、または特定の場所に割り当てられたデバイスなど) の管理に役立ちます。

デバイスを登録する前にデバイス グループを構成しておくと、デバイスが自動的にグループ化されるデバイス カテゴリを登録時に利用して、グループのデバイス ポリシーを自動的に受信することができます。 「[グループの概要](/intune/groups-get-started)」をご覧ください。

### <a name="task-2-use-resource-access-profiles-wi-fi-vpn-and-email-certificates"></a>タスク 2: リソース アクセス プロファイル (Wi-Fi、VPN、および電子メールの証明書) を使用する

リソース アクセス プロファイルは、登録されたデバイスに証明書とアクセス構成をプロビジョニングします。

MDM の評価要件のセクションで既に説明したように、証明書ベースの認証を使用している場合は、[証明書を構成](/intune/certificates-configure)してください。

### <a name="task-3-create-and-deploy-device-configuration-profiles"></a>タスク 3: デバイス構成プロファイルを作成して展開する

デバイス構成プロファイルを作成して、デバイス レベルの設定 (カメラの無効化、アプリ ストア、単一アプリ モードの構成、ホーム画面など) を適用する必要があります。

- デバイス プロファイルについては、[こちら](/intune/device-profiles)をご覧ください。

####  <a name="direct-import-of-ios-configuration-profiles-optional"></a>iOS 構成プロファイルの直接インポート (省略可能)

-   **Apple Configurator iOS プロファイル (iOS 7.1 以降):** 既存の MDM ソリューションで Apple Configurator プロファイル (.mobileconfig ファイル) を使用している場合、Intune ではカスタムの構成ポリシーとして、このプロファイルを直接インポートすることができます。

-   **iOS モバイル アプリケーション構成ポリシー:** 既存の MDM ソリューションで iOS モバイル アプリケーション構成ポリシーを使用している場合、Apple によりプロパティ一覧で指定された XML 形式を満たす限り、Intune はこのポリシーを直接インポートすることができます。

- iOS のカスタム ポリシーを追加する方法は[こちら](/intune/custom-settings-ios)を参照してください。

### <a name="task-4-create-and-deploy-device-compliance-policies-optional"></a>タスク 4: デバイス コンプライアンス ポリシーを作成して展開する (省略可能)

デバイス コンプライアンス ポリシーはセキュリティ指向の設定を評価し、デバイスが会社の基準に準拠しているかどうかを示すレポートを提供します。 デバイス コンプライアンス ポリシーは、次のようなセキュリティ指向の要素を評価します。

-   PIN の長さ

-   脱獄状態

-   OS のバージョン

デバイス コンプライアンス設定に関する他のリソースは次を参照してください。

-   デバイス コンプライアンス ポリシーは、[こちら](/intune-classic/deploy-use/introduction-to-device-compliance-policies-in-microsoft-intune)を参照してください。

-   デバイス コンプライアンス ポリシーの作成方法は、[こちら](/intune-classic/deploy-use/create-a-device-compliance-policy-in-microsoft-intune)を参照してください。

### <a name="task-5-publish-and-deploy-apps"></a>タスク 5: アプリを公開して展開する

Intune MDM を使用する場合は、アプリの自動インストールを要求するか、ポータル サイトでアプリを使用できるようにすることで、アプリをプロビジョニングできます。

-   アプリの追加方法は[こちら](/intune-classic/deploy-use/add-apps)を参照してください。

-   アプリの展開方法は[こちら](/intune-classic/deploy-use/deploy-apps)を参照してください。

### <a name="task-6-enable-device-enrollment"></a>タスク 6: デバイスの登録を可能にする

登録により、デバイスでの制御のプロビジョニングによる管理が確立します。 企業所有およびユーザー個人のデバイスの登録を準備する方法については、[こちら](/intune/device-enrollment)を参照してください。

## <a name="next-steps"></a>次のステップ 

[アプリ保護ポリシーを構成する (オプション)](migration-guide-app-protection-policies.md)
---
title: Skycure iOS アプリ構成ポリシーをダウンロードする
description: エンドユーザーに展開した Skycure iOS アプリで使用する Skycure iOS アプリ構成ポリシーをダウンロードします。
keywords: ''
author: andredm7
ms.author: andredm
manager: dougeby
ms.date: 03/16/2017
ms.topic: article
ms.prod: ''
ms.service: microsoft-intune
ms.technology: ''
ms.assetid: d211b876-4d3a-473c-999f-843c0a16cd22
ROBOTS: NOINDEX,NOFOLLOW
ms.reviewer: heenamac
ms.suite: ems
ms.custom: intune-classic
ms.openlocfilehash: 2f3cf3b2b18eeadf6779b7a8e96d75e569e6e3be
ms.sourcegitcommit: 5eba4bad151be32346aedc7cbb0333d71934f8cf
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/16/2018
---
# <a name="download-skycure-ios-app-configuration-policy"></a>Skycure iOS アプリ構成ポリシーをダウンロードする

[!INCLUDE [classic-portal](../includes/classic-portal.md)]

## <a name="before-you-begin"></a>始める前に

次の手順を実行するには、Skycure 管理コンソールにログインする必要があります。

> [!TIP] 
> Microsoft Internet Explorer 11 または Edge を利用しているときは、場合によっては、プライベート モードを利用して Skycure 管理コンソールを開く必要があります。

## <a name="to-download-the-ios-app-configuration-policy"></a>iOS アプリ構成ポリシーをダウンロードするには

1.  [Skycure 管理コンソール](https://aad.skycure.com)に進みます。

2.  自分の **Skycure 管理者資格情報**を入力し、**[続行]** をクリックします。

    ![Skycure 管理コンソールのログイン](../media/mtp/skycure-ios-app-1.png)

    > [!IMPORTANT] 
    > Skycure 管理者のユーザー名は電子メール アカウントですが、そのアカウントは Azure Active Directory の有効なアカウントでなければなりません。有効なユーザーではない場合、ログインは失敗します。 Skycure は、シングル サインオン (SSO) を使用して、管理者ユーザー名の認証に Azure Active Directory を使用します。

3.  **[設定]** &gt; **[Device Management Integrations (デバイス管理統合)]** &gt; **[EMM Integration Selection (EMM 統合選択)]** の順に進み、**[Microsoft Intune]** を選択し、選択を保存します。

2.  **[Integration setup files (統合セットアップ ファイル)]** リンクをクリックし、生成された \*.zip ファイルを保存します。 この .zip ファイルには **skycure\_configuration.plist** ファイルが含まれます。このファイルを利用して、Intune クラシック ポータルで iOS アプリ構成ポリシーが作成されます。

![Skycure 統合セットアップ ファイル](../media/mtp/skycure-ios-app-2.png)

## <a name="next-steps"></a>次の手順

[Skycure アプリ、Microsoft Authenticator アプリ、iOS 構成ポリシーの追加](/intune-classic/deploy-use/add-skycure-apps-microsoft-authenticator-and-ios-app-configuration-policy)

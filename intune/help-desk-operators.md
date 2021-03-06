---
title: ヘルプ デスクのトラブルシューティング ポータル
titlesuffix: Microsoft Intune
description: ヘルプ デスクのスタッフが、トラブルシューティング ポータルを使用して、ユーザーの技術的な問題を解決します。
keywords: ''
author: dougeby
ms.author: dougeby
manager: dougeby
ms.date: 03/02/2018
ms.topic: article
ms.prod: ''
ms.service: microsoft-intune
ms.technology: ''
ms.assetid: 1f39c02a-8d8a-4911-b4e1-e8d014dbce95
ms.reviewer: sumitp
ms.custom: intune-azure
ms.openlocfilehash: 5d924e216dd6d0fe13bc4c7718b5368db1d35f8c
ms.sourcegitcommit: dbea918d2c0c335b2251fea18d7341340eafd673
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/26/2018
---
# <a name="use-the-troubleshooting-portal-to-help-users-at-your-company"></a>トラブルシューティング ポータルを使用して社内のユーザーをサポートする

[!INCLUDE [azure_portal](./includes/azure_portal.md)]

トラブルシューティング ポータルでは、ヘルプ デスクのオペレーターや Intune の管理者が、ユーザーのヘルプ要求に対処するためにユーザー情報を表示することができます。 ヘルプ デスクが含まれる組織は、ユーザーのグループに**ヘルプ デスク オペレーター**を割り当てることができます。 ヘルプ デスク オペレーター ロールの場合、**[トラブルシューティング]** ウィンドウを使用できます。

**[トラブルシューティング]** ウィンドウにもユーザー登録に関する問題が表示されます。 問題に関する詳細と推奨される修復手順は、管理者およびヘルプ デスクのオペレーターが問題をトラブルシューティングするのに役立ちます。 登録に関する特定の問題はキャプチャされず、一部のエラーには推奨される修復方法がない場合があります。

ヘルプ デスク オペレーター ロールを追加する手順については、「[Intune でのロール ベースの管理制御 (RBAC)](/intune/role-based-access-control)」を参照してください。

ユーザーが Intune で技術的な問題をサポートに連絡すると、ヘルプ デスク オペレーターがそのユーザーの名前を入力します。 Intune には、次のような階層 1 の多くの問題を解決するのに役立つデータが示されます。

- ユーザーの状態
- ［割り当て］
- ポリシー準拠の問題
- デバイスが見つからない
- デバイスが VPN または Wi-Fi の設定を取得できない
- アプリのインストールの失敗

## <a name="to-review-troubleshooting-details"></a>トラブルシューティングの詳細を確認するには

トラブルシューティング ウィンドウで、**[ユーザーの選択]** を選択してユーザー情報を表示します。 ユーザー情報は、ユーザーと彼らのデバイスの現在の状態を理解するのに役立ちます。  

1. サインイン、 [Azure ポータル](https://portal.azure.com)します。
2. **[すべてのサービス]**、**[Intune]** の順に選択します。 Intune は **[監視 + 管理]** セクションにあります。
3. **[Intune]** ウィンドウで、**[トラブルシューティング]** を選択します。
4. **[選択]** をクリックして、トラブルシューティングを行うユーザーを選択します。
5. 名前または電子メール アドレスを入力して、ユーザーを選択します。 **[選択]** をクリックします。 ユーザーのトラブルシューティング情報が、トラブルシューティング ウィンドウに表示されます。 情報については、次の表で説明します。

> [!Note]  
> **[トラブルシューティング]** ウィンドウには、ブラウザーで [https://aka.ms/intunetroubleshooting](https://aka.ms/intunetroubleshooting) に移動してアクセスすることもできます。

## <a name="areas-of-troubleshooting-dashboard"></a>トラブルシューティング ダッシュボードの領域

**[トラブルシューティング]** ウィンドウを使用して、ユーザー情報を確認することができます。

![](/intune/media/troubleshooting-dash.png)

| 領域 | 名前 | 説明 |
| ---  | ---  | ---         |
| 1.   | アカウントの状態  | 現在の Intune テナントの状態が**アクティブ**または**非アクティブ**として表示されます。       |
| 2.   | ユーザー選択  | 現在選択されているユーザーの名前。 **[ユーザーの変更]** をクリックして、新しいユーザーを選択します。       |
| 3.   | ユーザーの状態  | ユーザーの Intune ライセンスの状態、デバイスの数、各デバイスのコンプライアンス状態、アプリの数、およびアプリのコンプライアンス状態が表示されます。       |
| 4.   | ユーザー情報  | 一覧を使用して、ウィンドウで確認する詳細を選択します。 <br>以下を選択できます。 <ul><li>モバイル アプリ<li>アプリ保護ポリシー<li>Compliance ポリシー<li> 構成ポリシー</ul>      |
| 5.   | グループのメンバーシップ  | 内容は省略       |

## <a name="mobile-apps-reference"></a>モバイル アプリ リファレンス

Intune および Azure Active Directory (AD) で管理されているユーザーが所有するデバイスで実行されているアプリ。

### <a name="properties"></a>[プロパティ]

モバイル アプリのプロパティ。

| プロパティ      | 説明                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 名前          | アプリケーションの名前。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| OS            | デバイスにインストールされているオペレーティング システム。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| 型          | アプリごとに割り当ての種類を選択できます。  <br> **[使用可能]** - ユーザーがポータル サイト アプリまたは Web サイトからアプリをインストールします。  <br> **[該当なし]** - アプリはポータル サイトにインストールまたは表示されません。 <br> **[アンインストール]** - アプリは選択したグループのデバイスからアンインストールされます。  <br> **[登録せずに使用可能]** - このアプリを、デバイスが Intune に登録されていないユーザーのグループに割り当てます。 |
| ［更新日時］ | デバイスの種類の名前。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |

### <a name="devices"></a>[デバイス]

Intune によって管理されているか、Intune または Azure AD で管理されているユーザーによって管理されているデバイス。

| プロパティ           | 説明                                                                                                                         |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| デバイス名        | デバイスの種類の名前。                                                                                                     |
| 管理者         | ポリシーが変更されたときのタイムスタンプ。                                                                                              |
| Azure AD の結合の種類 | 各ユーザーのアプリ保護アプリの状態。 アプリの状態は、**[確認済み]** か **[未確認]** のはずです。 |
| 所有権          | デバイス所有権の種類。 **会社**、**個人**、および**不明**のいずれかが示されます。                                               |
| Intune 準拠   | デバイスの種類の名前。                                                                                                     |
| Azure AD 準拠 | 各ユーザーのアプリ保護アプリの状態。 アプリの状態は、**[確認済み]** か **[未確認]** のはずです。 |
| OS                 | デバイスにインストールされているオペレーティング システム。                                                                                       |
| OS のバージョン         | デバイスのオペレーティング システムのバージョン番号。                                                                                  |
| 最後のチェックイン      | デバイスの種類の名前。                                                                                                     |

### <a name="app-protection-status"></a>アプリの保護の状態

アプリ保護ポリシーは、Enterprise Mobility Solution (EMS) テクノロジと統合されたモバイル アプリで使用できます。 これにより、会社のデータがモバイル アプリ (Office モバイル アプリを含む) にダウンロードされる場合の保護基準が示されます。 

| プロパティ    | 説明                                                                           |
|-------------|---------------------------------------------------------------------------------------|
| 状態      | デバイス所有権の種類。 **会社**、**個人**、および**不明**のいずれかが示されます。 |
| アプリ名    | アプリケーションの名前                                                           |
| デバイス名 | デバイスの種類の名前。                                                       |
| デバイスの種類 | デバイスの種類の名前。                                                       |
| ポリシー    | デバイス所有権の種類。 **会社**、**個人**、および**不明**のいずれかが示されます。 |
| 最後の同期   | デバイスと Intune が最後に同期された時刻のタイムスタンプ。                   |

## <a name="app-protection-policies-reference"></a>アプリ保護ポリシー リファレンス

アプリ保護ポリシーは、EMS テクノロジと統合されたモバイル アプリで使用できます。 これにより、会社のデータがモバイル アプリ (Office モバイル アプリを含む) にダウンロードされる場合の保護基準が示されます。 

### <a name="properties"></a>[プロパティ]

Intune で管理されるデバイスのアプリ保護ポリシーの状態を以下の表にまとめます。

| プロパティ    | 説明                                                                                                                                |
|-------------|-------------------------------------------------------------------------------------------------------------------------------------|
| 名前        | アプリケーションの名前。                                                                                                        |
| 展開済み    | 各ユーザーのアプリ保護アプリの状態。 アプリの状態は、**[確認済み]** か **[未確認]** のはずです。 |
| プラットフォーム    | デバイス所有権の種類。 **会社**、**個人**、および**不明**のいずれかが示されます。                                               |
| 登録  | デバイスの種類の名前。                                                                                                     |
| ［最終更新日時］ | ポリシーが変更されたときのタイムスタンプ。                                                                                              |

### <a name="devices"></a>[デバイス]

Intune によって管理されているか、Intune または Azure AD で管理されているユーザーによって管理されているデバイス。

| プロパティ           | テキスト                                                                                                                                |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| ［デバイス名］        | デバイスの種類の名前。                                                                                                     |
| 管理者         | ポリシーが変更されたときのタイムスタンプ。                                                                                              |
| Azure AD の結合の種類 | 各ユーザーのアプリ保護アプリの状態。 アプリの状態は、**[確認済み]** か **[未確認]** のはずです。 |
| 所有権          | デバイス所有権の種類。 **会社**、**個人**、および**不明**のいずれかが示されます。                                               |
| Intune 準拠   | デバイスの種類の名前。                                                                                                     |
| Azure AD 準拠 | 各ユーザーのアプリ保護アプリの状態。 アプリの状態は、**[確認済み]** か **[未確認]** のはずです。 |
| Azure AD 準拠 | 各ユーザーのアプリ保護アプリの状態。 アプリの状態は、**[確認済み]** か **[未確認]** のはずです。 |
| OS                 | デバイスにインストールされているオペレーティング システム。                                                                                       |
| OS のバージョン         | デバイスのオペレーティング システムのバージョン番号。                                                                                  |
| 最後のチェックイン      | デバイスの種類の名前。                                                                                                     |

## <a name="compliance-policies-reference"></a>コンプライアンス ポリシー リファレンス

会社のアプリやデータにアクセスするために使用するデバイスが、デバイスにアクセスする場合の PIN の使用や、デバイスに格納されるデータの暗号化などの特定のルールに準拠していることを確認します。

### <a name="properties"></a>[プロパティ]

コンプライアンス ポリシーのプロパティ。

| プロパティ      | 説明                                                                                                                         |
|---------------|-------------------------------------------------------------------------------------------------------------------------------------|
| 割り当て    | 各ユーザーのアプリ保護アプリの状態。 アプリの状態は、**[確認済み]** か **[未確認]** のはずです。 |
| 名前          | アプリケーションの名前。                                                                                                        |
| OS            | デバイスにインストールされているオペレーティング システム。                                                                                       |
| ポリシーの種類   | デバイス所有権の種類。 **会社**、**個人**、および**不明**のいずれかが示されます。                                               |
| ［更新日時］ | デバイスの種類の名前。                                                                                                     |

### <a name="devices"></a>[デバイス]

Intune によって管理されているか、Intune または Azure AD で管理されているユーザーによって管理されているデバイス。

| プロパティ           | 説明                                                                                                                         |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| デバイス名        | デバイスの種類の名前。                                                                                                     |
| 管理者         | ポリシーが変更されたときのタイムスタンプ。                                                                                              |
| Azure AD の結合の種類 | 各ユーザーのアプリ保護アプリの状態。 アプリの状態は、**[確認済み]** か **[未確認]** のはずです。 |
| 所有権          | デバイス所有権の種類。 **会社**、**個人**、および**不明**のいずれかが示されます。                                               |
| Intune 準拠   | デバイスの種類の名前。                                                                                                     |
| Azure AD 準拠 | 各ユーザーのアプリ保護アプリの状態。 アプリの状態は、**[確認済み]** か **[未確認]** のはずです。 |
| OS                 | デバイスにインストールされているオペレーティング システム。                                                                                       |
| OS のバージョン         | デバイスのオペレーティング システムのバージョン番号。                                                                                  |
| 最後のチェックイン      | デバイスの種類の名前。                                                                                                     |

### <a name="app-protection-policies"></a>アプリ保護ポリシー

アプリ保護ポリシーは、EMS テクノロジと統合されたモバイル アプリで使用できます。 これにより、会社のデータがモバイル アプリ (Office モバイル アプリを含む) にダウンロードされる場合の保護基準が示されます。 

| プロパティ    | 説明                                                                           |
|-------------|---------------------------------------------------------------------------------------|
| 状態      | デバイス所有権の種類。 **会社**、**個人**、および**不明**のいずれかが示されます。 |
| アプリ名    | アプリケーションの名前                                                           |
| デバイス名 | デバイスの種類の名前。                                                       |
| デバイスの種類 | デバイスの種類の名前。                                                       |
| ポリシー    | デバイス所有権の種類。 **会社**、**個人**、および**不明**のいずれかが示されます。 |
| 最後の同期   | デバイスと Intune が最後に同期された時刻のタイムスタンプ。                   |

## <a name="configuration-policies-reference"></a>構成ポリシー リファレンス

アプリ構成ポリシーは、ベンダー固有の構成のモバイル アプリで使用できます。 

### <a name="properties"></a>[プロパティ]

構成ポリシーのプロパティ。

| プロパティ      | 説明                                                                                                                         |
|---------------|-------------------------------------------------------------------------------------------------------------------------------------|
| 割り当て    | 各ユーザーのアプリ保護アプリの状態。 アプリの状態は、**[確認済み]** か **[未確認]** のはずです。 |
| 名前          | アプリケーションの名前。                                                                                                        |
| OS            | デバイスにインストールされているオペレーティング システム。                                                                                       |
| ポリシーの種類   | デバイス所有権の種類。 **会社**、**個人**、および**不明**のいずれかが示されます。                                               |
| ［更新日時］ | デバイスの種類の名前。                                                                                                     |

### <a name="devices"></a>[デバイス]

Intune によって管理されているか、Intune または Azure AD で管理されているユーザーによって管理されているデバイス。

| プロパティ           | 説明                                                                                                                         |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| デバイス名        | デバイスの種類の名前。                                                                                                     |
| 管理者         | ポリシーが変更されたときのタイムスタンプ。                                                                                              |
| Azure AD の結合の種類 | 各ユーザーのアプリ保護アプリの状態。 アプリの状態は、**[確認済み]** か **[未確認]** のはずです。 |
| 所有権          | デバイス所有権の種類。 **会社**、**個人**、および**不明**のいずれかが示されます。                                               |
| Intune 準拠   | デバイスの種類の名前。                                                                                                     |
| Azure AD 準拠 | 各ユーザーのアプリ保護アプリの状態。 アプリの状態は、**[確認済み]** か **[未確認]** のはずです。 |
| OS                 | デバイスにインストールされているオペレーティング システム。                                                                                       |
| OS のバージョン         | デバイスのオペレーティング システムのバージョン番号。                                                                                  |
| 最後のチェックイン      | デバイスの種類の名前。                                                                                                     |


### <a name="app-protection-policies"></a>アプリ保護ポリシー

アプリ保護ポリシーは、EMS テクノロジと統合されたモバイル アプリで使用できます。 これにより、会社のデータがモバイル アプリ (Office モバイル アプリを含む) にダウンロードされる場合の保護基準が示されます。 

| プロパティ    | 説明                                                                           |
|-------------|---------------------------------------------------------------------------------------|
| 状態      | デバイス所有権の種類。 **会社**、**個人**、および**不明**のいずれかが示されます。 |
| アプリ名    | アプリケーションの名前                                                           |
| デバイス名 | デバイスの種類の名前。                                                       |
| デバイスの種類 | デバイスの種類の名前。                                                       |
| ポリシー    | デバイス所有権の種類。 **会社**、**個人**、および**不明**のいずれかが示されます。 |
| 最後の同期   | デバイスと Intune が最後に同期された時刻のタイムスタンプ。                   |

## <a name="next-steps"></a>次の手順

ロール ベースの管理制御 (RBAC) の詳細を学習し、組織デバイス、モバイル アプリケーション管理、データ保護タスクにおけるロールを定義することができます。 詳細については、「[Intune でのロール ベースの管理制御 (RBAC)](/intune/role-based-access-control)」を参照してください。

Microsoft Intune の既知の問題について学習します。 詳細については、「[Microsoft Intune の既知の問題](/intune/known-issues)」を参照してください。

サポート チケットを作成し、必要なときにヘルプを表示する方法を学習します。 「[Microsoft Intune のサポートを受ける方法](/intune/get-support)」を参照してください。

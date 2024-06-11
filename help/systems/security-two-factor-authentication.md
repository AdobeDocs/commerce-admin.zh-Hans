---
title: 双重身份验证(2FA)
description: 了解双重身份验证支持以确保系统和数据的安全。
exl-id: d9eb3dd6-4a7b-411a-ac08-0441803cd59a
role: Admin
feature: Configuration, Security, User Account
source-git-commit: b31ed0e76df67a486012d8ec4997d9f19e17d371
workflow-type: tm+mt
source-wordcount: '789'
ht-degree: 0%

---

# 双重身份验证(2FA)

Commerce _管理员_ 用于您的Adobe Commerce或Magento Open Source安装，提供对商店、订单和客户数据的访问。 为防止对您的数据进行未经授权的访问，所有尝试登录 _管理员_ 必须完成身份验证过程以验证其身份。

>[!NOTE]
>
>此双重身份验证(2FA)实施适用于 _管理员_ 仅适用，不适用于客户帐户。 保护您的Commerce帐户的双因素身份验证具有单独的设置。 要了解更多信息，请访问 [保护您的Commerce帐户](../getting-started/commerce-account-secure.md).

二元身份验证被广泛使用，通常在同一应用程序上为不同的网站生成访问代码。 此附加身份验证可确保只有您才能登录到您的用户帐户。 如果您丢失了密码或机器人猜到了密码，则双重身份验证会增加一层保护。 例如，您可以使用Google Authenticator生成商店管理员、Commerce帐户和Google帐户的代码。

![安全配置iphone - 2FA](./assets/google-authenticator-iphone.png){width="300"}

Adobe Commerce支持来自多个提供商的2FA方法。 有些客户要求安装生成一次性密码(OTP)的应用程序，用户可在登录时输入该密码以验证其身份。 通用第二因子(U2F)设备类似于密钥链，并生成用于验证身份的唯一密钥。 其它设备在插入USB端口时验证身份。 作为商店管理员，您可以要求一个或多个可用的2FA方法来验证用户身份。 您的2FA配置适用于与Adobe Commerce安装关联的所有网站和商店。

用户首次登录到 _管理员_，则必须设置每个 [2FA](../configuration-reference/security/2fa.md) 方法，并使用关联的应用程序或设备验证其身份。 进行此初始设置后，用户每次登录时都必须使用配置的方法之一进行身份验证。 每个用户的2FA信息均记录在 _管理员_ 帐户，可以是 [重置](security-two-factor-authentication-manage.md) 如有必要。 要了解有关登录过程的更多信息，请访问 [_管理员_ 登录](../getting-started/admin-signin.md).

>[!NOTE]
>
>已启用AdobeIdentity Management服务(IMS)身份验证的存储已禁用本地Adobe Commerce和Magento Open Source2FA。 使用Adobe凭据登录到其Commerce实例的管理员用户不需要对许多管理员任务重新进行身份验证。 当管理员用户登录到其当前会话时，身份验证由Adobe IMS处理。 请参阅 [AdobeIdentity Management服务(IMS)集成概述](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/ims/adobe-ims-integration-overview.html).

你可以看这个 [视频演示](https://video.tv.adobe.com/v/339104?quality=12&learn=on) 有关“管理员”中双重身份验证的概述。

## 配置所需的2FA提供商

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中，展开 **[!UICONTROL Security]** 并选择 **[!UICONTROL 2FA]**.

1. 在 _[!UICONTROL General]_部分，选择要使用的提供程序。

   | 提供商 | 函数 |
   |--- |--- |
   | [!UICONTROL Google Authenticator] | 在应用程序中生成用于用户验证的一次性密码。 |
   | [!UICONTROL Duo Security] | 提供短信和推送通知。 |
   | [!UICONTROL Authy] | 生成依赖于时间的六位数代码，并提供短信或语音呼叫2FA保护或令牌。 |
   | [!UICONTROL U2F Devices (Yubikey and others)] | 使用物理设备进行身份验证，例如 [[!DNL YubiKey]](https://www.yubico.com/). |

   要选择多种方法，请按住Ctrl键(PC)或Command键(Mac)并单击每个项目。

1. 完成每个所需2FA方法的设置。

   ![安全配置 — 2FA](../configuration-reference/security/assets/2fa-general.png){width="600" zoomable="yes"}

1. 完成后，单击 **[!UICONTROL Save Config]**.

   用户首次登录到 _管理员_&#x200B;中，他们必须设置每个所需的2FA方法。 进行此初始设置后，每次登录时都必须使用配置的方法之一进行身份验证。

## 2FA提供程序设置

完成所需的每个2FA方法的设置。

### Google

要更改一次性密码(OTP)在登录期间可用的时间，请清除 **[!UICONTROL Use system value]** 复选框。 然后，输入所需的秒数 **[!UICONTROL OTP Window]** 才有效。

![安全配置 — Google](../configuration-reference/security/assets/2fa-google.png){width="600" zoomable="yes"}

>[!NOTE]
>
>在Adobe Commerce 2.4.7及更高版本中，OTP窗口配置设置控制系统接受管理员的一次性密码(OTP)过期后的时间（以秒为单位）。 此值必须小于30秒。 系统默认设置为 `29`.<br><br> 在版本2.4.6中， OTP窗口设置确定保持有效的过去和将来的OTP代码数。 值 `1` 指示当前OTP代码加上一个过去代码和一个将来代码在任何给定时间点都保持有效。

### [!DNL Duo Security]

从您的Duo Security帐户输入以下凭据：

- 集成密钥
- 密钥
- API主机名

![安全配置 — 双核](../configuration-reference/security/assets/2fa-duo-security.png){width="600" zoomable="yes"}

### [!DNL Authy]

1. 输入来自您的 [!DNL Authy] 帐户。

1. 要更改验证期间显示的默认消息，请清除 **[!UICONTROL Use system value]** 复选框。 然后，输入 **[!UICONTROL OneTouch Message]** 您希望显示的对象。

   ![安全配置 — 授权](../configuration-reference/security/assets/2fa-authy.png){width="600" zoomable="yes"}

### U2F设备([!DNL Yubikey] 及其他)

默认情况下，在身份验证过程中使用存储域。 要使用自定义域解决身份验证难题，请清除 **[!UICONTROL Use system value]** 复选框。 然后，输入 **[!UICONTROL WebAPi Challenge Domain]**.

![安全配置 — U2F设备](../configuration-reference/security/assets/2fa-u2f-key.png){width="600" zoomable="yes"}

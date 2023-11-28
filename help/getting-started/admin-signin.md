---
title: 您的管理员用户帐户
description: 了解您的管理员帐户以及如何使用双重身份验证登录到管理员。
exl-id: ad576533-5914-49d1-8e73-3f59c55543a5
feature: Admin Workspace, User Account
source-git-commit: fff3464c9da50927bbe9773a17b0f6858360d788
workflow-type: tm+mt
source-wordcount: '964'
ht-degree: 0%

---

# 您的管理员帐户

主管理员帐户最初是在安装期间设置的，可能包含初始占位符信息或示例数据信息。 此帐户的指定所有者可以个性化用户名和密码，并随时更新名字、姓氏和电子邮件地址。 此帐户， _超级用户_ 默认情况下，会创建业务所需的管理员用户帐户。

- 请参阅 [创建用户](../systems/permissions-users-all.md#create-a-user) 有关添加或编辑用户的信息。

- 请参阅 [权限](../systems/permissions.md) 和 [用户角色](../systems/permissions-user-roles.md) 有关管理员和用户角色的信息。

{{ims-admin-note}}

## 管理员登录

此 [!DNL Commerce] _管理员_ 受多层安全措施的保护，以防止未经授权访问您的存储、订单和客户数据。 第一次登录到 _管理员_，您需要输入用户名和密码，并设置 [双重身份验证](../systems/security-two-factor-authentication.md) (2FA)。

根据存储配置，可能存在 [验证码](../systems/security-google-recaptcha.md) 解决难题，例如输入一系列键盘字符、解决难题或单击一系列具有共同主题的图像。 这些测试旨在将您识别为人类，而不是自动机器人。

为了提高安全性，您可以确定 _管理员_ 每个用户具有 [权限](../systems/permissions.md) 以访问，还可以限制 [登录尝试](../configuration-reference/advanced/admin.md). 默认情况下，在六次尝试后，帐户将被锁定，用户必须等待几分钟再重试。 [锁定的帐户](../systems/permissions-users-all.md#locked-users) 也可以从重置 _管理员_.

>[!NOTE]
>
>第一次登录到 _管理员_，则系统会提示您 _允许收集管理员使用情况数据_. 请参阅 [使用情况数据收集](admin.md#usage-data-collection) 以了解更多信息。

![管理员登录](./assets/admin-login.png){width="400"}

### 步骤1：设置双重身份验证

登录 _管理员_ 您必须设置两个因素身份验证解决方案，并且随时可以使用。 要详细了解每个解决方案使用的身份验证过程，请参阅 [使用双重身份验证](../systems/security-two-factor-authentication-use.md). 默认情况下， [!DNL Commerce] 支持 [Google身份验证器][1].

询问您的 [!DNL Commerce] 商店支持哪些2FA解决方案的系统管理员。 然后，根据提供商的说明完成首选2FA解决方案的设置。

### 第2步：登录到管理员

1. 输入 _管理员_ URL指定于 [!DNL Commerce] 安装。

   默认 _管理员_ URL类似于 `https://www.yourdomain.com/your-custom-admin-domain`.

   >[!NOTE]
   >
   >尽管本文档使用 `admin` 作为大多数示例中的基本URL，建议您选择唯一且难以猜测的 [自定义URL](../stores-purchase/store-urls.md) 对于 _管理员_ 你店里的。

   您可以为页面添加书签或在桌面上保存快捷方式以便轻松访问。

1. 输入您的 _管理员_ **[!UICONTROL Username]** 和 **[!UICONTROL Password]**.

1. （可选）如果您的商店启用了验证码，请按照屏幕上的说明解决挑战。

   要了解更多信息，请参阅 [验证码](../systems/security-captcha.md) 和 [reCAPTCHA](../systems/security-google-recaptcha.md).

1. 单击 **[!UICONTROL Sign in]**.

   如果这是您首次登录 _管理员_ 您应会从帐户收到一封电子邮件，其中包含指向配置说明的链接。

### 步骤3：完成2FA配置

以下示例说明如何配对 _管理员_ 使用Google Authenticator的帐户。

1. 出现二维码时，请使用以下方法之一捕获该代码，并将Google Authenticator与 _管理员_ 帐户。

   ![设置Google身份验证器](./assets/admin-login-google-auth-setup.png){width="400"}

   - 使用智能手机捕获二维码

     在智能手机上，启动Google Authenticator。 点按 _加号_ (+)图标。 然后在屏幕底部，点按 **[!UICONTROL Scan Barcode]** 并拍照QR码。

   - 从浏览器中捕获二维码

     如果将Google Authenticator作为扩展安装在浏览器中，请单击 **验证者** 图标，然后捕获页面。

   - 手动输入二维码

     复制二维码下方的文本字符串。 使用智能手机或浏览器启动Google Authenticator，然后单击加号(+)。 然后，选择 **[!UICONTROL Manual Entry]**. 下 **[!UICONTROL Account]**，输入与您的关联的电子邮件地址 _管理员_ 将二维码字符串粘贴到 **[!UICONTROL Key]** 字段。

1. 登录 _管理员_ 使用双重身份验证，将Google Authenticator生成的六位数代码输入到 **[!UICONTROL Authenticator code]** 字段，然后单击 **[!UICONTROL Confirm]**.

   ![输入验证程序代码](./assets/admin-login-2fa-google.png){width="400"}

## 重置密码

不允许重复使用分配给帐户的最后4个密码。

1. 输入 **[!UICONTROL Email Address]** 与 _管理员_ 帐户。

   ![忘记密码](./assets/admin-sign-in-forgot-password.png){width="400"}

1. 单击 **[!UICONTROL Retrieve Password]**.

   如果某个帐户与电子邮件地址关联，则会发送一封电子邮件以重置密码。

   >[!NOTE]
   >
   >An _管理员_ 密码长度必须为7个或更多字符，且包含字母和数字。 请参阅 [配置 _管理员_ 安全性](../systems/security-admin.md) 有关密码选项的信息。

## 注销管理员

1. 在右上角，单击 _帐户_ (![帐户](../assets/icon-admin-user.png))图标。

1. 单击 **[!UICONTROL Sign Out]**.

   ![注销](./assets/admin-sign-out.png){width="700" zoomable="yes"}

此 _[!UICONTROL Sign In]_页面显示您已注销的消息。 注销_&#x200B;管理员&#x200B;_无论何时离开计算机，无人照看。

## 编辑帐户信息

1. 单击 _帐户_ (![“帐户”图标](../assets/icon-admin-user.png))图标。

1. 单击 **[!UICONTROL Account Setting]**.

   ![帐户信息](./assets/admin-account-information.png){width="700" zoomable="yes"}

1. 对您的帐户信息进行必要的更改。

   如果更改登录凭据，请确保将它们存储在安全位置。

1. 输入您的当前帐户密码。

1. 单击 **[!UICONTROL Save Account]**.

## 允许多个管理员登录

管理员提供管理订单、客户、产品、运输和支付功能的权限。 作为安全最佳实践，默认配置设置为不允许管理员用户帐户多次登录。 但是，您可以更改此设置，以允许管理员用户从多个设备登录以适应您的业务工作流。

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧导航面板中，展开 **[!UICONTROL Advanced]** 并选择 **[!UICONTROL Admin]**.

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Security]** 部分。

1. 对象 **管理员帐户共享**，选择 `Yes`.

   ![允许管理员帐户共享](./assets/multiple-admin-login.png){width="700" zoomable="yes"}

1. 单击 **[!UICONTROL Save Config]**.

## 将管理员用户登录名设置为区分大小写

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧导航面板中，展开 **[!UICONTROL Advanced]** 并选择 **[!UICONTROL Admin]**.

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Security]** 部分。

1. 设置 **[!UICONTROL Login is Case Sensitive]** 字段至 `Yes`.

1. 单击 **[!UICONTROL Save Config]**.

[1]: https://play.google.com/store/apps/details?id=com.google.android.apps.authenticator2&amp;hl=en_US

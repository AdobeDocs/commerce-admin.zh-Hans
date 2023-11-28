---
title: Google reCAPTCHA
description: 了解如何配置Google reCAPTCHA以进行管理员访问和注册客户启动的各种店面操作。
exl-id: c3b53702-0882-4ac4-9cf5-39fefc90005e
role: Admin
feature: Configuration, Security
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '1063'
ht-degree: 0%

---

# Google reCAPTCHA

[Google reCAPTCHA](https://developers.google.com/recaptcha) 确保人(而不是计算机（或“机器人”）与您的网站进行交互。 与标准Adobe Commerce和Magento Open Source不同 [验证码](security-captcha.md)，Google reCAPTCHA通过一系列不同的显示选项和方法提供了增强的安全性。 Google reCAPTCHA帐户的信息板中提供了其他网站流量信息。

Google reCAPTCHA是单独为管理员和店面配置的。

- 对于管理员，可在以下位置使用Google reCAPTCHA： [登录](../getting-started/admin-signin.md) 页面和用户请求密码重置时。 如果标准商务 [验证码](security-captcha.md) 如果启用，则可以同时使用Google reCAPTCHA而不会出现任何问题。

- 对于店面，Google reCAPTCHA可用于登录到 [客户帐户](../customers/customer-sign-in.md)，发送来自 [联系我们](../getting-started/store-details.md#contact-us-form) 页面和许多其他店面位置。

  ![Google reCAPTCHA — 客户登录](./assets/customer-account-login-recaptcha.png){width="700" zoomable="yes"}

Google reCAPTCHA可通过多种方式实施：

- _reCAPTCHA v3不可见_  — 使用算法对用户交互进行评级，并根据得分确定用户是人类的可能性。

- _reCAPTCHA v2不可见_  — 无需用户交互即可执行后台验证。 用户和客户会自动进行验证，但可能需要选择特定图像来完成挑战。

- _reCAPTCHA v2（“我不是机器人”）_  — 使用验证请求 _“我不是机器人”_ 复选框。

>[!IMPORTANT]
>
>在配置Google reCAPTCHA之前，请确保 `PHP.ini` 文件包含以下设置： `allow_url_fopen = 1`. 这可能需要开发人员的帮助。 请参阅 [必需的PHP设置](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/php-settings.html)安装指南中的{：target=&quot;_blank&quot;}。

## 步骤1：生成Google reCAPTCHA密钥

Google reCAPTCHA需要启用一对API密钥。 您可以通过reCAPTCHA网站免费获取这些密钥。 在生成密钥之前，您必须知道要使用的reCAPTCHA类型。

1. 打开Google reCAPTCHA页面并登录到您的帐户。

1. 对象 **[!UICONTROL Label]**，输入名称以标识要内部引用的键。

   对于在Adobe Commerce或Magento Open Source安装中使用的每个reCAPTCHA类型，您需要一组密钥。 例如： `Commerce Invisible`

1. 对象 **[!UICONTROL reCAPTCHA type]**&#x200B;中，选择要使用的方法。

   - _reCAPTCHA v3不可见_
   - _reCAPTCHA v2不可见_
   - _reCAPTCHA v2（“我不是机器人”）_

1. 对象 **[!UICONTROL Domain]**，输入您商店的域。 例如： mystore.com

   如果您有多个具有不同域的商店，请在单独的一行中输入每个域。

   - 添加您的商店域和任何子域。
   - 您可以添加 `localhost`、其他本地VM域以及测试所需的暂存域。

1. 选中此复选框可 **[!UICONTROL Accept the reCAPTCHA Terms of Service]**.

1. （可选）选择 **[!UICONTROL Send alerts to owners]** 用于在Google检测到问题或可疑流量时发送通知的复选框。

1. 单击 **[!UICONTROL Submit]** 完成注册并接收密钥。

   >[!IMPORTANT]
   >
   >并非所有键值都适用于所有类型的reCAPTCHA，错误应用它们可能会导致意外行为。 例如，为reCAPTCHA v2“我不是机器人”生成的Google reCAPTCHA密钥不能用于 _reCAPTCHA v2不可见_ 并且可以阻止已启用reCAPTCHA的功能。

## 步骤2：为管理员配置Google reCAPTCHA

1. 登录到您的管理员帐户。

1. 在管理员侧边栏上，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在右上角，设置 **[!UICONTROL Store View]** 到 `Default Config`.

1. 在左侧面板中，展开 **[!UICONTROL Security]** 并单击 **[!UICONTROL Google reCAPTCHA Admin Panel]**.

   >[!NOTE]
   >
   >清除 **[!UICONTROL Use system value]** 用于要配置的每个字段的复选框。

1. 使用 _[!DNL reCAPTCHA v2 ("I am not a robot")]_，展开&#x200B;**[!UICONTROL reCAPTCHA v2 ("I am not a robot")]**部分并执行以下操作：

   - 对象 **[!UICONTROL Google API Website Key]**，输入在注册Google reCAPTCHA帐户时为此reCAPTCHA类型创建的网站密钥。

   - 对象 **[!UICONTROL Google API Secret Key]**，输入与您的Google reCAPTCHA帐户关联的密钥。

   - 对象 **[!UICONTROL Size]**&#x200B;中，选择要显示的Google reCAPTCHA框的大小。 选项： `Normal (default)` / `Compact`

   - 对象 **[!UICONTROL Theme]**，选择要用于设置Google reCAPTCHA框样式的主题。 选项： `Light Theme (default)` / `Dark Theme`

   - 对象 **[!UICONTROL Language Code]**，输入两个字符的代码以指定 [用于Google reCAPTCHA文本和消息的语言](https://developers.google.com/recaptcha/docs/language).

   ![reCAPTCHA v2 - “我不是机器人”](../configuration-reference/security/assets/recaptcha-admin-v2-not-robot.png){width="600" zoomable="yes"}

1. 使用 _[!DNL reCAPTCHA v2 Invisible]_，展开&#x200B;**[!UICONTROL reCAPTCHA v2 Invisible]**部分并执行以下操作：

   - 对象 **[!UICONTROL Google API Website Key]**，输入在注册Google reCAPTCHA帐户时为此reCAPTCHA类型创建的网站密钥。

   - 对象 **[!UICONTROL Google API Secret Key]**，输入与您的Google reCAPTCHA帐户关联的密钥。

   - 对象 **[!UICONTROL Invisible Badge Position]**，选择要在每个页面上使用的徽章位置。 选项： `Inline` / `Bottom Right` / `Bottom Left`

   - 对象 **[!UICONTROL Theme]**，选择要用于设置Google reCAPTCHA框样式的主题。 选项： `Light Theme (default)` / `Dark Theme`

   - 对象 **[!UICONTROL Language Code]**，请输入一个双字符代码，以指定 [用于Google reCAPTCHA文本和消息的语言](https://developers.google.com/recaptcha/docs/language).

   ![reCAPTCHA v2不可见](../configuration-reference/security/assets/recaptcha-admin-v2-invisible.png){width="600" zoomable="yes"}

1. 使用 _[!DNL reCAPTCHA v3 Invisible]_，展开&#x200B;**[!UICONTROL reCAPTCHA v3 Invisible]**部分并执行以下操作：

   - 对象 **[!UICONTROL Google API Website Key]**，输入在注册Google reCAPTCHA帐户时为此reCAPTCHA类型创建的网站密钥。

   - 对象 **[!UICONTROL Google API Secret Key]**，输入与您的Google reCAPTCHA帐户关联的密钥。

   - 输入 **[!UICONTROL Minimum Score Threshold]** 识别何时将用户交互标记为潜在风险；其中1.0是典型的用户交互，0.0可能是机器人。 默认： `0.5`

   - 对象 **[!UICONTROL Invisible Badge Position]**，选择要在每个页面上使用的位置。 选项： `Inline` / `Bottom Right` / `Bottom Left`

   - 对象 **[!UICONTROL Theme]**，选择要用于设置Google reCAPTCHA框样式的主题。 选项： `Light Theme (default)` / `Dark Theme`

   - 对象 **[!UICONTROL Language Code]**，请输入一个双字符代码，以指定 [用于Google reCAPTCHA文本和消息的语言](https://developers.google.com/recaptcha/docs/language).

   ![reCAPTCHA v3不可见](../configuration-reference/security/assets/recaptcha-admin-v3-invisible.png){width="600" zoomable="yes"}

1. 展开 **[!UICONTROL reCAPTCHA Validation Failure Messages]** 并输入在验证失败或无法完成时显示在管理员中的消息。

   ![reCAPTCHA失败消息](../configuration-reference/security/assets/recaptcha-admin-failure-messages.png){width="600" zoomable="yes"}

1. 展开 **[!UICONTROL Admin Panel]** 部分，并根据需要配置以下各项：

   - 设置 **[!UICONTROL Enable for Login]** 用于管理员登录页面的reCAPTCHA类型。

   - 设置 **[!UICONTROL Enable for Forgot Password]** 重新设置密码请求的reCAPTCHA类型。

   ![reCAPTCHA管理选项](../configuration-reference/security/assets/recaptcha-admin-panel.png){width="600" zoomable="yes"}

## 步骤3：为店面配置Google reCAPTCHA

1. 在左侧面板中的 _[!UICONTROL Security]_，选择&#x200B;**[!UICONTROL Google reCAPTCHA Storefront]**.

1. 填写要在店面中使用的每个reCAPTCHA类型的部分。

   请参阅以下内容中的信息 _步骤2：为管理员配置Google reCAPTCHA_ 以了解有关每个reCAPTCHA类型的选项的详细信息。

1. 展开 **[!UICONTROL reCAPTCHA Validation Failure Messages]** 并输入在验证失败或无法完成时显示在店面中的消息。

1. 展开 **[!UICONTROL Storefront]** 部分。

   >[!NOTE]
   >
   >清除 **[!UICONTROL Use system value]** 用于要配置的每个字段的复选框。

1. 将每个店面位置字段设置为您已配置为使用的reCAPTCHA类型。

   - [!UICONTROL Enable for Customer Login]
   - [!UICONTROL Enable for Forgot Password]
   - [!UICONTROL Enable for Create New Customer Account]
   - [!UICONTROL Enable for Edit Customer Account]
   - [!UICONTROL Enable for Create New Company Account] ![适用于Adobe Commerce的B2B](../assets/b2b.svg) (仅适用于Adobe Commerce的B2B版本)
   - [!UICONTROL Enable for Contact Us]
   - [!UICONTROL Enable for Product Review]
   - [!UICONTROL Enable for Newsletter Subscription]
   - [!UICONTROL Enable for Gift Card] ![Adobe Commerce](../assets/adobe-logo.svg) (仅限Adobe Commerce)
   - [!UICONTROL Enable for Invitation Create Account]
   - [!UICONTROL Enable for Send To Friend]
   - [!UICONTROL Enable for Checkout/Placing Order]
   - [!UICONTROL Enable for Wishlist Sharing]
   - [!UICONTROL Enable for Coupon Codes]
   - [!UICONTROL Enable for PayPal PayflowPro payment form]

   ![店面选项配置](../configuration-reference/security/assets/recaptcha-storefront.png){width="600" zoomable="yes"}

## 步骤4：保存配置

1. 配置设置完成后，单击 **[!UICONTROL Save Config]**.

1. 在工作区顶部的消息中，单击 **[!UICONTROL Cache Management]** 并刷新每个无效缓存。

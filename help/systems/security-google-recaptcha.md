---
title: Google reCAPTCHA
description: 了解如何配置Google reCAPTCHA以进行管理员访问和注册客户启动的各种店面操作。
exl-id: c3b53702-0882-4ac4-9cf5-39fefc90005e
role: Admin
feature: Configuration, Security
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '1046'
ht-degree: 0%

---

# Google reCAPTCHA

[Google reCAPTCHA](https://developers.google.com/recaptcha)确保人（而不是“机器人”）与您的网站进行交互。 与标准Adobe Commerce和Magento Open Source[CAPTCHA](security-captcha.md)不同，Google reCAPTCHA通过选择不同的显示选项和方法提供了增强的安全性。 Google reCAPTCHA帐户的信息板中提供了其他网站流量信息。

Google reCAPTCHA是单独为管理员和店面配置的。

- 对于管理员，可在[登录](../getting-started/admin-signin.md)页面上以及用户请求重置密码时使用Google reCAPTCHA。 如果标准Commerce [CAPTCHA](security-captcha.md)也处于启用状态，则可以同时使用Google reCAPTCHA而不会出现任何问题。

- 对于店面，Google reCAPTCHA可用于登录到[客户帐户](../customers/customer-sign-in.md)，从[联系我们](../getting-started/store-details.md#contact-us-form)页面发送消息，以及在许多其他店面位置。

  ![Google reCAPTCHA — 客户登录](./assets/customer-account-login-recaptcha.png){width="700" zoomable="yes"}

Google reCAPTCHA可通过多种方式实施：

- _reCAPTCHA v3不可见_ — 使用算法对用户交互进行评级，并根据得分确定用户是否为人类的可能性。

- _reCAPTCHA v2不可见_ — 无需用户交互即可执行后台验证。 用户和客户会自动进行验证，但可能需要选择特定图像来完成挑战。

- _reCAPTCHA v2 （“我不是机器人”）_ — 使用&#x200B;_“我不是机器人”_&#x200B;复选框验证请求。

>[!IMPORTANT]
>
>在配置Google reCAPTCHA之前，请确保您的`PHP.ini`文件包含以下设置： `allow_url_fopen = 1`。 这可能需要开发人员的帮助。 请参阅安装指南中的[必需的PHP设置](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/php-settings.html){：target=&quot;_blank&quot;}。

## 步骤1：生成Google reCAPTCHA密钥

Google reCAPTCHA需要启用一对API密钥。 您可以通过reCAPTCHA网站免费获取这些密钥。 在生成密钥之前，您必须知道要使用的reCAPTCHA类型。

1. 打开Google reCAPTCHA页面并登录到您的帐户。

1. 为&#x200B;**[!UICONTROL Label]**&#x200B;输入一个名称以标识内部引用的键。

   对于在Adobe Commerce或Magento Open Source安装中使用的每个reCAPTCHA类型，您需要一组密钥。 例如： `Commerce Invisible`

1. 对于&#x200B;**[!UICONTROL reCAPTCHA type]**，选择要使用的方法。

   - _reCAPTCHA v3不可见_
   - _reCAPTCHA v2不可见_
   - _reCAPTCHA v2 （“我不是机器人”）_

1. 对于&#x200B;**[!UICONTROL Domain]**，请输入商店的域。 例如： mystore.com

   如果您有多个具有不同域的商店，请在单独的一行中输入每个域。

   - 添加您的商店域和任何子域。
   - 您可以根据需要添加`localhost`、其他本地VM域和暂存域以进行测试。

1. 选中&#x200B;**[!UICONTROL Accept the reCAPTCHA Terms of Service]**&#x200B;的复选框。

1. （可选）选中&#x200B;**[!UICONTROL Send alerts to owners]**&#x200B;复选框以在Google检测到问题或可疑通信时发送通知。

1. 单击&#x200B;**[!UICONTROL Submit]**&#x200B;完成注册并接收密钥。

   >[!IMPORTANT]
   >
   >并非所有键值都适用于所有类型的reCAPTCHA，错误应用它们可能会导致意外行为。 例如，为reCAPTCHA v2“我不是机器人”生成的Google reCAPTCHA密钥不适用于&#x200B;_reCAPTCHA v2 Invisible_，并且可能会阻止启用了reCAPTCHA的功能。

## 步骤2：为管理员配置Google reCAPTCHA

1. 登录到您的管理员帐户。

1. 在管理员侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在右上角，将&#x200B;**[!UICONTROL Store View]**&#x200B;设置为`Default Config`。

1. 在左侧面板中，展开&#x200B;**[!UICONTROL Security]**&#x200B;并单击&#x200B;**[!UICONTROL Google reCAPTCHA Admin Panel]**。

   >[!NOTE]
   >
   >清除要配置的每个字段的&#x200B;**[!UICONTROL Use system value]**&#x200B;复选框。

1. 要使用&#x200B;_[!DNL reCAPTCHA v2 ("I am not a robot")]_，请展开&#x200B;**[!UICONTROL reCAPTCHA v2 ("I am not a robot")]**部分并执行以下操作：

   - 对于&#x200B;**[!UICONTROL Google API Website Key]**，请输入在注册Google reCAPTCHA帐户时为此reCAPTCHA类型创建的网站密钥。

   - 对于&#x200B;**[!UICONTROL Google API Secret Key]**，输入与您的Google reCAPTCHA帐户关联的密钥。

   - 对于&#x200B;**[!UICONTROL Size]**，选择要显示的Google reCAPTCHA框的大小。 选项： `Normal (default)` / `Compact`

   - 对于&#x200B;**[!UICONTROL Theme]**，选择要用于设置Google reCAPTCHA框样式的主题。 选项： `Light Theme (default)` / `Dark Theme`

   - 对于&#x200B;**[!UICONTROL Language Code]**，输入双字符代码以指定用于Google reCAPTCHA文本和消息传送的[语言](https://developers.google.com/recaptcha/docs/language)。

   ![reCAPTCHA v2 — “我不是机器人”](../configuration-reference/security/assets/recaptcha-admin-v2-not-robot.png){width="600" zoomable="yes"}

1. 要使用&#x200B;_[!DNL reCAPTCHA v2 Invisible]_，请展开&#x200B;**[!UICONTROL reCAPTCHA v2 Invisible]**部分并执行以下操作：

   - 对于&#x200B;**[!UICONTROL Google API Website Key]**，请输入在注册Google reCAPTCHA帐户时为此reCAPTCHA类型创建的网站密钥。

   - 对于&#x200B;**[!UICONTROL Google API Secret Key]**，输入与您的Google reCAPTCHA帐户关联的密钥。

   - 对于&#x200B;**[!UICONTROL Invisible Badge Position]**，选择要在每个页面上使用的徽章位置。 选项： `Inline` / `Bottom Right` / `Bottom Left`

   - 对于&#x200B;**[!UICONTROL Theme]**，选择要用于设置Google reCAPTCHA框样式的主题。 选项： `Light Theme (default)` / `Dark Theme`

   - 对于&#x200B;**[!UICONTROL Language Code]**，请输入一个双字符代码，该代码指定用于Google reCAPTCHA文本和消息传送的[语言](https://developers.google.com/recaptcha/docs/language)。

   ![reCAPTCHA v2不可见](../configuration-reference/security/assets/recaptcha-admin-v2-invisible.png){width="600" zoomable="yes"}

1. 要使用&#x200B;_[!DNL reCAPTCHA v3 Invisible]_，请展开&#x200B;**[!UICONTROL reCAPTCHA v3 Invisible]**部分并执行以下操作：

   - 对于&#x200B;**[!UICONTROL Google API Website Key]**，请输入在注册Google reCAPTCHA帐户时为此reCAPTCHA类型创建的网站密钥。

   - 对于&#x200B;**[!UICONTROL Google API Secret Key]**，输入与您的Google reCAPTCHA帐户关联的密钥。

   - 输入&#x200B;**[!UICONTROL Minimum Score Threshold]**&#x200B;以标识何时将用户交互标记为潜在风险；其中1.0是典型的用户交互，0.0可能是机器人。 默认： `0.5`

   - 对于&#x200B;**[!UICONTROL Invisible Badge Position]**，选择要在每个页面上使用的位置。 选项： `Inline` / `Bottom Right` / `Bottom Left`

   - 对于&#x200B;**[!UICONTROL Theme]**，选择要用于设置Google reCAPTCHA框样式的主题。 选项： `Light Theme (default)` / `Dark Theme`

   - 对于&#x200B;**[!UICONTROL Language Code]**，请输入一个双字符代码，该代码指定用于Google reCAPTCHA文本和消息传送的[语言](https://developers.google.com/recaptcha/docs/language)。

   ![reCAPTCHA v3不可见](../configuration-reference/security/assets/recaptcha-admin-v3-invisible.png){width="600" zoomable="yes"}

1. 展开&#x200B;**[!UICONTROL reCAPTCHA Validation Failure Messages]**&#x200B;并输入在验证失败或无法完成时显示在管理员中的消息。

   ![reCAPTCHA失败消息](../configuration-reference/security/assets/recaptcha-admin-failure-messages.png){width="600" zoomable="yes"}

1. 展开&#x200B;**[!UICONTROL Admin Panel]**&#x200B;部分并根据需要配置以下内容：

   - 将&#x200B;**[!UICONTROL Enable for Login]**&#x200B;设置为要用于管理员登录页面的reCAPTCHA类型。

   - 将&#x200B;**[!UICONTROL Enable for Forgot Password]**&#x200B;设置为要用于密码重置请求的reCAPTCHA类型。

   ![reCAPTCHA管理选项](../configuration-reference/security/assets/recaptcha-admin-panel.png){width="600" zoomable="yes"}

## 步骤3：为店面配置Google reCAPTCHA

1. 在左侧面板中的&#x200B;_[!UICONTROL Security]_下，选择&#x200B;**[!UICONTROL Google reCAPTCHA Storefront]**。

1. 填写要在店面中使用的每个reCAPTCHA类型的部分。

   有关每个reCAPTCHA类型的选项的详细信息，请参阅&#x200B;_步骤2：为管理员配置Google reCAPTCHA_&#x200B;中的信息。

1. 展开&#x200B;**[!UICONTROL reCAPTCHA Validation Failure Messages]**&#x200B;并输入在验证失败或无法完成时显示在店面中的消息。

1. 展开&#x200B;**[!UICONTROL Storefront]**&#x200B;部分。

   >[!NOTE]
   >
   >清除要配置的每个字段的&#x200B;**[!UICONTROL Use system value]**&#x200B;复选框。

1. 将每个店面位置字段设置为您已配置为使用的reCAPTCHA类型。

   - [!UICONTROL Enable for Customer Login]
   - [!UICONTROL Enable for Forgot Password]
   - [!UICONTROL Enable for Create New Customer Account]
   - [!UICONTROL Enable for Edit Customer Account]
   - [!UICONTROL Enable for Create New Company Account] ![Adobe Commerce B2B](../assets/b2b.svg)(仅适用于Adobe Commerce B2B)
   - [!UICONTROL Enable for Contact Us]
   - [!UICONTROL Enable for Product Review]
   - [!UICONTROL Enable for Newsletter Subscription]
   - [!UICONTROL Enable for Gift Card] ![Adobe Commerce](../assets/adobe-logo.svg)(仅限Adobe Commerce)
   - [!UICONTROL Enable for Invitation Create Account]
   - [!UICONTROL Enable for Send To Friend]
   - [!UICONTROL Enable for Checkout/Placing Order]
   - [!UICONTROL Enable for Wishlist Sharing]
   - [!UICONTROL Enable for Coupon Codes]
   - [!UICONTROL Enable for PayPal PayflowPro payment form]

   ![店面选项配置](../configuration-reference/security/assets/recaptcha-storefront.png){width="600" zoomable="yes"}

## 步骤4：保存配置

1. 配置设置完成后，单击&#x200B;**[!UICONTROL Save Config]**。

1. 在工作区顶部的消息中，单击&#x200B;**[!UICONTROL Cache Management]**&#x200B;并刷新每个无效缓存。

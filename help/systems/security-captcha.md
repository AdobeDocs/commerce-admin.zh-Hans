---
title: 验证码
description: 了解如何配置验证码以进行管理员访问和注册客户启动的各种店面操作。
exl-id: b2867ad5-7d48-4e9f-b84e-3cf0a14ec16f
role: Admin
feature: Configuration, Security
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '946'
ht-degree: 0%

---

# 验证码

验证码是一种可视设备，可确保人(而不是计算机（或“机器人”）)与站点进行交互。 CAPTCHA是 _全自动公共图灵测试将计算机和人类区分开来_. 它可用于管理员访问和注册客户启动的各种店面操作。 Adobe Commerce和Magento Open Source支持本主题中所述的标准验证码和 [Google reCAPTCHA](security-google-recaptcha.md).

您可以根据需要多次重新加载验证码，方法是单击图像右上角的重新加载图标。 CAPTCHA是完全可配置的，并且每次都可以设置，或者仅在定义的失败登录尝试次数之后设置。

![使用验证码登录](./assets/customer-account-login-captcha.png){width="700" zoomable="yes"}

## 为管理员配置验证码

为了提高安全性，您可以在“管理员登录和忘记密码”页面中添加验证码。 管理员用户可以通过单击 _重新加载_ ![“重新加载”图标](./assets/CAPTCHA-icon-reload.png) 图标（位于图像的右上角）。 重新加载的次数不受限制。

![管理员 — 使用验证码登录](./assets/security-captcha-admin.png){width="300"}

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中，展开 **[!UICONTROL Advanced]** 并选择 **[!UICONTROL Admin]**.

1. 在右上角，设置 **[!UICONTROL Store View]** 到 `Default`.

   如果 [范围](../getting-started/websites-stores-views.md#scope-settings) ，请选择您希望应用验证码配置的网站。

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL CAPTCHA]** 部分。

1. 设置 **[!UICONTROL Enable CAPTCHA in Admin]** 到 `Yes`. 然后完成其余选项，如下所示：

   ![管理员 — 验证码配置](../configuration-reference/advanced/assets/admin-captcha.png){width="600" zoomable="yes"}

   - 输入 **[!UICONTROL Font]** 用于CAPTCHA符号(默认： `LinLibertine`)。

     要添加您自己的字体，字体文件必须与Commerce安装位于同一目录中，并且必须在 `config.xml` 验证码模块的文件，位于 `app/code/Magento/Captcha/etc`.

   - 选择以下任一项 **[!UICONTROL Forms]** 其中将使用CAPTCHA。 要选择多个表单，请按住Ctrl键(PC)或Command键(Mac)。

      - `Admin Login`
      - `Admin Forgot Password`

   - 设置 **[!UICONTROL Displaying Modes]** 更改为以下任一项：

      - `Always`  — 始终需要验证码才能登录到管理员。
      - `After number of attempts to login`  — 此选项仅适用于“管理员登录”表单。 选中后， _[!UICONTROL Number of Unsuccessful Attempts to Login]_字段。 输入要允许的登录尝试次数。 值为0（零）类似于将“显示模式”设置为 `Always`.

     为了跟踪失败的登录尝试次数，每次尝试使用一个电子邮件地址和一个IP地址登录都会被计数。 允许从同一IP地址登录的最大次数是1,000。 此限制仅在启用CAPTCHA时适用。

   - 对象 **[!UICONTROL Number of Unsuccessful Attempts to Login]**，输入在验证码出现之前管理员可以尝试登录的次数。 如果设置为零(`0`)，始终需要验证码。

   - 对象 **[!UICONTROL CAPTCHA Timeout (minutes)]**，输入验证码过期前的分钟数。 验证码过期后，管理员必须重新加载页面。

   - 输入 **[!UICONTROL Number of Symbols]** 以在CAPTCHA中显示。 最多八个(`8`)符号。 对于随每个CAPTCHA更改的可变符号数，请输入一个范围(例如 `5-8`)。

   - 对象 **[!UICONTROL Symbols Used in CAPTCHA]**，输入要在验证码中随机显示的字母（a-z和A-Z）和数字(0-9)。 难以与其他符号区分的符号，例如 `i`， `l`，或 `1`默认验证码符号集中不包含。

   - 设置 **[!UICONTROL Case Sensitive]** 到 `Yes` 如果您希望要求管理员完全按照验证码中所示输入大写或小写的字符。

1. 完成后，单击 **[!UICONTROL Save Config]**.

## 为店面配置验证码

客户每次登录其帐户时，或多次尝试登录失败后，都可能需要输入验证码。 此外，在整个店面中使用的许多表单都可以配置为需要由验证码进行验证。

![结账时进行验证码](./assets/storefront-checkout-payment-captcha.png){width="700" zoomable="yes"}

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中，展开 **[!UICONTROL Customers]** 并选择 **[!UICONTROL Customer Configuration]**.

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL CAPTCHA]** 部分。

![客户验证码配置](../configuration-reference/customers/assets/customer-configuration-captcha.png){width="600" zoomable="yes"}

1. 设置 **[!UICONTROL Enable CAPTCHA on Storefront]** 到 `Yes`. 然后完成其余选项，如下所示：

   - 输入 **[!UICONTROL Font]** 用于CAPTCHA符号(默认： `LinLibertine`)。

     要添加您自己的字体，字体文件必须与Commerce安装位于同一目录中，并且必须在 `config.xml` 验证码模块的文件。

   - 选择以下任一项 **[!UICONTROL Forms]** 其中将使用CAPTCHA。 要选择多个表单，请按住Ctrl键(PC)或Command键(Mac)。

      - `Applying coupon code`
      - `Checkout/Placing Order`
      - `Create user`
      - `Login`
      - `Forgot password`
      - `Contact Us`
      - `Change password`
      - `Share Wishlist Form`
      - `Payflow Pro` (请参阅 [安全补丁](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/payments/paypal-payflow-pro-active-carding-activity.html) _知识库_ article)
      - `Send to Friend Form` ![Magento Open Source](../assets/open-source.svg) (仅限Magento Open Source)
      - `Add Gift Card Code` ![Adobe Commerce](../assets/adobe-logo.svg) (仅限Adobe Commerce)
      - `Create company` ![适用于Adobe Commerce的B2B](../assets/b2b.svg) (仅适用于Adobe Commerce的B2B版本)

   - 设置 **[!UICONTROL Displaying Mode]** 更改为以下任一项：

      - `Always`  — 始终需要验证码才能访问选定的表单。
      - `After number of attempts to login`  — 输入出现CAPTCHA之前的登录尝试次数。 值0（零）类似于“始终”。 选中后，将显示失败的登录尝试次数。 此选项不适用于“忘记密码”表单，该表单如果启用，将始终显示CAPTCHA。

   - 对象 **[!UICONTROL Number of Unsuccessful Attempts to Login]**，输入客户在验证码出现之前可以失败登录的次数。 如果设置为零(`0`)，始终使用CAPTCHA。

   - 对象 **[!UICONTROL CAPTCHA Timeout (minutes)]**，输入验证码过期前的分钟数。 验证码过期后，客户必须重新加载页面才能生成新的验证码。

   - 输入 **[!UICONTROL Number of Symbols]** 以在CAPTCHA中显示。 最多八个(`8`)符号。 对于随每个CAPTCHA更改的可变符号数，请输入一个范围(例如 `5-8`)。

   - 对象 **[!UICONTROL Symbols Used in CAPTCHA]**，输入要在验证码中随机显示的字母（a-z和A-Z）和数字(0-9)。 默认字符集不包括类似符号，例如 `I` 或 `1`. 为了获得最佳效果，请使用用户可轻松识别的符号。

   - 设置 **[!UICONTROL Case Sensitive]** 到 `Yes` 如果您希望客户完全按照验证码中的说明输入大写或小写的字符。

1. 完成后，单击 **[!UICONTROL Save Config]**.

---
title: 配置电子邮件通信
description: 了解如何配置电子邮件通信，包括返回的电子邮件或特定电子邮件地址的回复的路由。
exl-id: 7e62e9c5-f214-4fd5-becc-99dcb093cd5c
feature: Communications, Configuration
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 0%

---

# 配置电子邮件通信

此 _邮件发送设置_ 允许您将返回的电子邮件或电子邮件回复路由到特定地址。 如果您的应用商店运行在SMTP或Windows服务器上，则可以验证主机和端口设置。

>[!IMPORTANT]
>
>**安全声明** 所有商家都应立即设置其邮件发送配置，以防最近发现的潜在远程代码执行漏洞。 在解决此问题之前，强烈建议您避免使用 [!DNL Sendmail] 用于电子邮件通信。 在 _[!UICONTROL Mail Sending Settings]_，请确保_[!UICONTROL Set Return Path]_ 设置为 `No`.

有关配置设置的详细列表，请参阅 [_[!UICONTROL Mail Sending Settings]_](../configuration-reference/advanced/system.md) 在 _配置引用_.

## 配置电子邮件通信

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中，展开 **[!UICONTROL Advanced]** 并选择 **[!UICONTROL System]**.

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Mail Sending Settings]** 部分并执行以下操作：

   ![高级配置 — 邮件发送设置](../configuration-reference/advanced/assets/system-mail-sending-settings.png){width="600" zoomable="yes"}

   - 如有必要，请设置 **[!UICONTROL Disable Email Communications]** 到 `No`.

   - 对象 **[!UICONTROL Transport]**，从存储区中选择电子邮件通信的传输类型： `Sendmail` 或 `SMTP`

   - 如果在SMTP或Windows服务器上运行，请验证以下设置：

      - **[!UICONTROL Host]** - `localhost` 或其他

      - **[!UICONTROL Port (25)]** - `25` 或其他

   - 对象 **[!UICONTROL Set Return Path]**&#x200B;中，选择以下选项之一：

      - `No`  — （建议的安全措施）将返回的电子邮件路由到默认商店电子邮件地址。
      - `Yes`  — 将返回的电子邮件路由到默认商店电子邮件地址。
      - `Specified`  — 将返回的电子邮件路由到中指定的电子邮件地址 **[!UICONTROL Return Path Email]**.

   - 如果在SMTP服务器上运行，请配置连接：

      - **[!UICONTROL Username]**  — 输入SMTP服务器的登录用户名。
      - **[!UICONTROL Password]**  — 输入SMTP服务器登录密码。
      - **[!UICONTROL Auth]**  — 选择SMTP服务器连接的身份验证类型： `NONE` ， `PLAIN`，或 `LOGIN`
      - **[!UICONTROL SSL]**  — 选择服务器安全证书的验证类型： `SSL` 或 `TLS`

     ![高级配置 — 邮件发送设置](../configuration-reference/advanced/assets/system-mail-sending-settings-smtp.png){width="600" zoomable="yes"}

1. 在左侧面板中，展开 **[!UICONTROL Sales]** 并选择 **[!UICONTROL Sales Emails]**.

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL General Settings]** 部分。

1. 设置 **[!UICONTROL Asynchronous sending]** 到 `Enable`.

   ![销售配置 — 电子邮件常规设置](../configuration-reference/sales/assets/sales-emails-general-settings.png){width="600" zoomable="yes"}

   有关配置设置的详细列表，请参阅 [_常规设置_](../configuration-reference/sales/sales-emails.md) 在 _配置引用_.

1. 完成后，单击 **[!UICONTROL Save Config]**.

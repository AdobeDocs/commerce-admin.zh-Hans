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

通过&#x200B;_邮件发送设置_，您可以将返回的电子邮件或回复路由到特定地址。 如果您的应用商店运行在SMTP或Windows服务器上，则可以验证主机和端口设置。

>[!IMPORTANT]
>
>**安全声明**&#x200B;所有商家应立即设置其邮件发送配置，以防止最近发现的潜在远程代码执行攻击。 在解决此问题之前，强烈建议您避免使用[!DNL Sendmail]进行电子邮件通信。 在&#x200B;_[!UICONTROL Mail Sending Settings]_中，确保_[!UICONTROL Set Return Path]_&#x200B;设置为`No`。

有关配置设置的详细列表，请参阅&#x200B;_配置引用_&#x200B;中的[_[!UICONTROL Mail Sending Settings]_](../configuration-reference/advanced/system.md)。

## 配置电子邮件通信

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧面板中，展开&#x200B;**[!UICONTROL Advanced]**&#x200B;并选择&#x200B;**[!UICONTROL System]**。

1. 展开&#x200B;**[!UICONTROL Mail Sending Settings]**&#x200B;部分中的![扩展选择器](../assets/icon-display-expand.png)并执行以下操作：

   ![高级配置 — 邮件发送设置](../configuration-reference/advanced/assets/system-mail-sending-settings.png){width="600" zoomable="yes"}

   - 如有必要，请将&#x200B;**[!UICONTROL Disable Email Communications]**&#x200B;设置为`No`。

   - 对于&#x200B;**[!UICONTROL Transport]**，从存储区中选择电子邮件通信的传输类型： `Sendmail`或`SMTP`

   - 如果在SMTP或Windows服务器上运行，请验证以下设置：

      - **[!UICONTROL Host]** - `localhost`或其他

      - **[!UICONTROL Port (25)]** - `25`或其他

   - 对于&#x200B;**[!UICONTROL Set Return Path]**，请选择以下选项之一：

      - `No` - （推荐的安全措施）路由将电子邮件返回至默认商店电子邮件地址。
      - `Yes` — 路由将电子邮件返回到默认商店电子邮件地址。
      - `Specified` — 路由将电子邮件返回到&#x200B;**[!UICONTROL Return Path Email]**&#x200B;中指定的电子邮件地址。

   - 如果在SMTP服务器上运行，请配置连接：

      - **[!UICONTROL Username]** — 输入SMTP服务器的登录用户名。
      - **[!UICONTROL Password]** — 输入SMTP服务器登录密码。
      - **[!UICONTROL Auth]** — 为SMTP服务器连接选择身份验证类型： `NONE`、`PLAIN`或`LOGIN`
      - **[!UICONTROL SSL]** — 选择服务器安全证书的验证类型： `SSL`或`TLS`

     ![高级配置 — 邮件发送设置](../configuration-reference/advanced/assets/system-mail-sending-settings-smtp.png){width="600" zoomable="yes"}

1. 在左侧面板中，展开&#x200B;**[!UICONTROL Sales]**&#x200B;并选择&#x200B;**[!UICONTROL Sales Emails]**。

1. 展开&#x200B;**[!UICONTROL General Settings]**&#x200B;部分的![扩展选择器](../assets/icon-display-expand.png)。

1. 将&#x200B;**[!UICONTROL Asynchronous sending]**&#x200B;设置为`Enable`。

   ![销售配置 — 电子邮件常规设置](../configuration-reference/sales/assets/sales-emails-general-settings.png){width="600" zoomable="yes"}

   有关配置设置的详细列表，请参阅&#x200B;_配置引用_&#x200B;中的&#x200B;[_常规设置_](../configuration-reference/sales/sales-emails.md)。

1. 完成后，单击&#x200B;**[!UICONTROL Save Config]**。

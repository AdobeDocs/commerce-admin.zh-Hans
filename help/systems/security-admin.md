---
title: 配置管理员安全
description: 了解如何为商店管理员配置安全性。
exl-id: 931fd8ad-96b7-42e5-9c3e-4bb9ca85b1ba
role: Admin
feature: Admin Workspace, Configuration, Security
source-git-commit: e301cfaeec3a8427fff6138ba041bdbd7433c137
workflow-type: tm+mt
source-wordcount: '704'
ht-degree: 0%

---

# 配置管理员安全

我们建议您采取多层面的方法来保护您的商店的安全。 您可以首先使用不容易猜到的[自定义管理员URL](../stores-purchase/store-urls.md#use-a-custom-admin-url)，而不是显而易见的“管理员”或“后端”。 默认情况下，用于[登录](../getting-started/admin-signin.md)到Admin的密码长度必须为7个或更多字符，且包含字母和数字。 作为[最佳实践](https://experienceleague.adobe.com/docs/commerce-operations/implementation-playbook/best-practices/launch/security-best-practices.html?lang=zh-Hans)，请仅使用包含字母、数字和符号组合的强管理员密码。 Adobe Commerce和Magento Open Source不允许重用分配给该帐户的最近四个密码。

管理员安全配置使您能够：

- 向URL添加密钥
- 要求密码区分大小写
- 限制管理员会话的长度
- 限制密码的生命周期
- 限制在Admin用户帐户为[锁定](permissions-users-all.md#locked-users)之前可以尝试登录的次数。

为了提高安全性，您可以配置在当前会话过期之前键盘处于非活动状态的长度，并要求用户名和密码区分大小写。

除了此部分中的安全设置外，还需要[双重身份验证](security-two-factor-authentication.md) (2FA)以应用程序或设备生成的一次性密码验证用户的身份。 首次登录到Admin时，系统会提示您设置2FA。 为了提高安全性，也可以将管理员登录配置为需要[CAPTCHA](security-captcha.md)。

>[!NOTE]
>
>已启用[!DNL Adobe Identity Management Services] (IMS)身份验证的存储已禁用本机Adobe Commerce和Magento Open Source2FA。 使用Adobe凭据登录到其Commerce实例的管理员用户不需要对许多管理员任务重新进行身份验证。 当管理员用户登录到其当前会话时，身份验证由Adobe IMS处理。 请参阅[[!DNL Adobe Identity Management Service] (IMS)集成概述](../getting-started/adobe-ims-integration-overview.md)。

有关技术信息，请参阅开发人员文档中的[安全概述](https://developer.adobe.com/commerce/php/architecture/basics/security/){：target=&quot;_blank&quot;}。

![管理员安全](../configuration-reference/advanced/assets/admin-security.png){width="600" zoomable="yes"}

## 配置管理员安全

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧面板中的&#x200B;_[!UICONTROL Advanced]_&#x200B;下，选择&#x200B;**[!UICONTROL Admin]**。

1. 展开&#x200B;**[!UICONTROL Security]**&#x200B;部分的![扩展选择器](../assets/icon-display-expand.png)。

1. 要阻止管理员用户从不同设备上的同一帐户登录，请将&#x200B;**[!UICONTROL Admin Account Sharing]**&#x200B;设置为`No`。

1. 要确定用于管理密码重置请求的方法，请将&#x200B;**[!UICONTROL Password Reset Protection Type]**&#x200B;设置为以下任一项：

   - `By IP and Email` — 在收到来自通知的响应发送到与管理员帐户关联的电子邮件地址后，可以联机重置密码。
   - `By IP` — 密码可以在线重置，而无需其他确认。
   - `By Email` — 只有通过电子邮件响应发送到与管理员帐户关联的电子邮件地址的通知才能重置密码。
   - `None` — 密码只能由存储管理员重置。

1. 设置登录安全选项：

   - 对于&#x200B;**[!UICONTROL Recovery Link Expiration Period (hours)]**，输入密码恢复链接保持有效的小时数。

   - 要确定每小时可提交的最大密码请求数，请输入&#x200B;**[!UICONTROL Max Number of Password Reset Requests]**&#x200B;的数量。

   - 对于&#x200B;**[!UICONTROL Min Time Between Password Reset Requests]**，请输入密码重置请求之间必须经过的最小分钟数。

   - 要将密钥附加到管理员URL作为防御漏洞的手段，请将&#x200B;**[!UICONTROL Add Secret Key to URLs]**&#x200B;设置为`Yes`。 默认情况下，此设置处于启用状态。

   - 若要要求在任何输入的登录凭据中使用大写和小写字符与系统中存储的内容相匹配，请将&#x200B;**[!UICONTROL Login is Case Sensitive]**&#x200B;设置为`Yes`。

   - 若要确定管理员会话在超时之前的长度，请在&#x200B;**[!UICONTROL Admin Session Lifetime (seconds)]**&#x200B;字段中输入会话的持续时间（以秒为单位）。 该值必须为60秒或更大。

   - 对于&#x200B;**[!UICONTROL Maximum Login Failures to Lockout Account]**，输入帐户锁定前用户尝试登录Admin的次数。 默认情况下，允许尝试6次。 对于无限次的登录尝试，请将该字段留空。

   - 对于&#x200B;**[!UICONTROL Lockout Time (minutes)]**，输入当达到最大尝试次数时，管理员帐户被锁定的分钟数。

1. 设置密码选项：

   - 要限制管理员密码的生命周期，请输入密码对&#x200B;**[!UICONTROL Password Lifetime (days)]**&#x200B;有效的天数。 对于无限长的生命周期，请将此字段留空。

   - 将&#x200B;**[!UICONTROL Password Change]**&#x200B;设置为以下项之一：

      - `Forced` — 要求管理员用户在设置帐户后更改密码。
      - `Recommended` — 建议管理员用户在设置帐户后更改密码。

1. 完成后，单击&#x200B;**[!UICONTROL Save Config]**。

## 管理员密码要求

默认情况下，管理员密码长度必须为7个或更多字符，并且包含字母和数字。

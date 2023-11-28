---
title: 配置管理员安全
description: 了解如何为商店管理员配置安全性。
exl-id: 931fd8ad-96b7-42e5-9c3e-4bb9ca85b1ba
role: Admin
feature: Admin Workspace, Configuration, Security
source-git-commit: e301cfaeec3a8427fff6138ba041bdbd7433c137
workflow-type: tm+mt
source-wordcount: '716'
ht-degree: 0%

---

# 配置管理员安全

我们建议您采取多层面的方法来保护您的商店的安全。 您可以从使用 [自定义管理员URL](../stores-purchase/store-urls.md#use-a-custom-admin-url) 这并非易事，而不是显而易见的“管理员”或“后端”。 默认情况下，用于 [登录](../getting-started/admin-signin.md) 对于管理员，长度必须为7个或更多字符，并且包含字母和数字。 作为 [最佳实践](https://experienceleague.adobe.com/docs/commerce-operations/implementation-playbook/best-practices/launch/security-best-practices.html)，仅使用包含字母、数字和符号组合的强管理员密码。 Adobe Commerce和Magento Open Source不允许重用分配给该帐户的最近四个密码。

管理员安全配置使您能够：

- 向URL添加密钥
- 要求密码区分大小写
- 限制管理员会话的长度
- 限制密码的生命周期
- 限制在管理员用户帐户到期之前可以尝试登录的次数 [已锁定](permissions-users-all.md#locked-users).

为了提高安全性，您可以配置在当前会话过期之前键盘处于非活动状态的长度，并要求用户名和密码区分大小写。

除了此部分中的安全设置外， [双重身份验证](security-two-factor-authentication.md) 要使用应用程序或设备生成的一次性密码验证用户身份，需要使用(2FA)。 首次登录到Admin时，系统会提示您设置2FA。 为了提高安全性，也可以将管理员登录配置为需要 [验证码](security-captcha.md).

>[!NOTE]
>
>已启用存储 [!DNL Adobe Identity Management Services] (IMS)身份验证已禁用本机Adobe Commerce和Magento Open Source2FA。 使用Adobe凭据登录其Commerce实例的管理员用户不需要对许多管理员任务重新进行身份验证。 当管理员用户登录到其当前会话时，身份验证由Adobe IMS处理。 请参阅 [[!DNL Adobe Identity Management Service] (IMS)集成概述](../getting-started/adobe-ims-integration-overview.md).

有关技术信息，请参阅 [安全性概述](https://developer.adobe.com/commerce/php/architecture/basics/security/){：target=&quot;_blank&quot;}开发人员文档。

![管理员安全](../configuration-reference/advanced/assets/admin-security.png){width="600" zoomable="yes"}

## 配置管理员安全

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中的 _[!UICONTROL Advanced]_，选择&#x200B;**[!UICONTROL Admin]**.

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Security]** 部分。

1. 要阻止管理员用户在不同的设备上从同一帐户登录，请设置 **[!UICONTROL Admin Account Sharing]** 到 `No`.

1. 要确定用于管理密码重置请求的方法，请设置 **[!UICONTROL Password Reset Protection Type]** 更改为以下任一项：

   - `By IP and Email`  — 在收到来自通知的响应发送到与管理员帐户关联的电子邮件地址后，可以在线重置密码。
   - `By IP`  — 无需其他确认即可在线重置密码。
   - `By Email`  — 只有通过电子邮件响应发送到与管理员帐户关联的电子邮件地址的通知才能重置密码。
   - `None`  — 密码只能由存储管理员重置。

1. 设置登录安全选项：

   - 对象 **[!UICONTROL Recovery Link Expiration Period (hours)]**，输入密码恢复链接保持有效的小时数。

   - 要确定每小时可以提交的最大密码请求数，请输入 **[!UICONTROL Max Number of Password Reset Requests]**.

   - 对象 **[!UICONTROL Min Time Between Password Reset Requests]**，输入在密码重置请求之间必须经过的最小分钟数。

   - 要将密钥附加到管理员URL以防范攻击，请设置 **[!UICONTROL Add Secret Key to URLs]** 到 `Yes`. 默认情况下，此设置处于启用状态。

   - 要要求在任何输入的登录凭据中使用大写字符和小写字符与系统中存储的内容相匹配，请设置 **[!UICONTROL Login is Case Sensitive]** 到 `Yes`.

   - 要确定管理员会话在超时之前的长度，请以秒为单位输入会话的持续时间 **[!UICONTROL Admin Session Lifetime (seconds)]** 字段。 该值必须为60秒或更大。

   - 对象 **[!UICONTROL Maximum Login Failures to Lockout Account]**，输入在帐户锁定之前，用户尝试登录到管理员的次数。 默认情况下，允许尝试6次。 对于无限次的登录尝试，请将该字段留空。

   - 对象 **[!UICONTROL Lockout Time (minutes)]**，输入当达到最大尝试次数时，管理员帐户被锁定的分钟数。

1. 设置密码选项：

   - 要限制管理员密码的生命周期，请输入密码的有效天数 **[!UICONTROL Password Lifetime (days)]**. 对于无限长的生命周期，请将此字段留空。

   - 设置 **[!UICONTROL Password Change]** 更改为以下任一项：

      - `Forced`  — 要求管理员用户在设置帐户后更改密码。
      - `Recommended`  — 建议管理员用户在设置帐户后更改密码。

1. 完成后，单击 **[!UICONTROL Save Config]**.

## 管理员密码要求

默认情况下，管理员密码长度必须为7个或更多字符，并且包含字母和数字。

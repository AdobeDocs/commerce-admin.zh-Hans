---
title: 会话管理
description: 了解如何配置会话管理以保护管理员和店面。
exl-id: ad954218-aa3e-44e6-b23f-008de7fc7543
role: Admin
feature: Configuration, Security
badgePaas: label="仅限PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="仅适用于云项目(Adobe管理的PaaS基础架构)和内部部署项目上的Adobe Commerce 。"
source-git-commit: 9a68d9702cec9b812414d39e8d04c71751121a37
workflow-type: tm+mt
source-wordcount: '769'
ht-degree: 0%

---

# 会话管理

[会话管理](https://cheatsheetseries.owasp.org/cheatsheets/Session_Management_Cheat_Sheet.html)是针对API安全的反拒绝服务(DoS)最佳实践。 会话表示访客在您的网站上花费的时间，与管理员用户或客户登录其帐户的时间长短无关。

会话是与同一用户关联的一系列网络HTTP请求和响应事务。 这是一种在客户端（管理员）访问服务器时将客户端与其数据关联起来的方法。 会话用于建立变量，例如访问权和本地化设置，这些变量适用于用户在会话期间与Web应用程序的每次交互。

## 会话大小

使用以下配置设置可限制管理员用户和店面访客的最大会话大小：

- **[!UICONTROL Max Session Size in Admin]** — 限制以字节为单位的最大会话大小。 使用`0`禁用。
- **[!UICONTROL Max Session Size in Storefront]** — 限制以字节为单位的最大会话大小。 使用`0`禁用。

>[!TIP]
>
>这两个设置都以字节计量，默认为`256000`字节（或256 KB）。

**_要配置最大会话大小：_**

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧面板中，展开&#x200B;**[!UICONTROL Advanced]**&#x200B;并选择&#x200B;**[!UICONTROL System]**。

1. 展开![扩展选择器](../assets/icon-display-expand.png) **[!UICONTROL Security]**&#x200B;部分以访问会话设置。

   ![会话设置](../configuration-reference/advanced/assets/system-security.png){width="600" zoomable="yes"}

1. 输入以字节为单位的新会话大小。

   >[!WARNING]
   >
   >将该值设置过低可能会导致问题。 如果设置缺省值256000字节下面的任一选项，您将看到一条警告消息。 如果单击&#x200B;**[!UICONTROL No]**，系统会将值更改为`256000`。

1. 单击&#x200B;**[!UICONTROL Save Config]**。

### 管理员会话

如果超过最大会话大小，将显示一条错误消息，并且系统会将会话大小约束记录到`var/log`目录。

如果在设置会话大小过低后无法访问管理员，请使用CLI重置配置：

```bash
bin/magento config:set system/security/max_session_size_admin 256000
```

### 店面会议

如果超过最大会话大小，则不会显示任何错误，但系统会将会话大小约束记录到`var/log`目录。

## 会话验证

Adobe Commerce和Magento Open Source允许您验证会话变量，作为防止可能的会话固定攻击或试图毒害或劫持用户会话的保护措施。 会话验证设置可确定在每次访问商店时如何验证会话变量，以及会话ID是否包含在商店的URL中。

有关技术信息，请参阅&#x200B;_配置指南_&#x200B;中的[对会话存储使用Redis](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cache/redis/redis-session.html)。

![常规配置 — Web会话验证](../configuration-reference/general/assets/web-session-validation-settings.png){width="600" zoomable="yes"}

通过将验证变量中的值与为用户存储在`$_SESSION`数据中的会话数据进行比较，验证会检查访客的真实身份。 如果信息未按预期发送，并且对应的变量为空，则验证失败。 根据会话验证设置，如果会话变量未能通过验证过程，则客户端会话将立即终止。

启用所有验证变量有助于防止攻击，但也可能影响服务器的性能。 默认情况下，禁用所有会话变量验证。 我们建议您尝试这些设置，以找到适合您的Adobe Commerce或Magento Open Source安装的最佳组合。 激活所有验证变量可能会过度限制，并且可能会阻止访问具有通过代理服务器或从防火墙后面发起的Internet连接的客户。 要了解有关会话变量及其使用的更多信息，请参阅Linux®系统的系统管理文档。

**_要配置会话验证：_**

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧面板中，展开&#x200B;_[!UICONTROL General]_&#x200B;并选择&#x200B;**[!UICONTROL Web]**。

1. 展开&#x200B;**[!UICONTROL Session Validation Settings]**&#x200B;部分的![扩展选择器](../assets/icon-display-expand.png)。

1. 设置每个配置选项：

   - **[!UICONTROL Validate REMOTE_ADDR]** — 设置为`Yes`以验证请求的IP地址是否与`$_SESSION`变量中存储的内容匹配。

   - **[!UICONTROL Validate HTTP_VIA]** — 设置为`Yes`以验证传入请求的代理地址是否与`$_SESSION`变量中存储的地址匹配。

   - **[!UICONTROL Validate HTTP_X_FORWARDED_FOR]** — 设置为`Yes`以验证请求的转发地址是否与`$_SESSION`变量中存储的地址匹配。

   - **[!UICONTROL Validate HTTP_USER_AGENT]** — 设置为`Yes`以验证会话期间用于访问存储的浏览器或设备是否与`$_SESSION`变量中存储的内容匹配。

1. 完成后，单击&#x200B;**[!UICONTROL Save Config]**。

## 管理会话生命周期

作为安全措施，_管理员_&#x200B;最初设置为在键盘不活动达900秒（15分钟）后超时。 您可以调整会话的生命周期以适合您的工作方式。

**_要调整管理员会话生命周期：_**

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧面板中向下滚动并展开&#x200B;**[!UICONTROL Advanced]**。

1. 单击&#x200B;**[!UICONTROL Admin]**。

1. 展开&#x200B;**[!UICONTROL Security]**&#x200B;部分的![扩展选择器](../assets/icon-display-expand.png)。

1. 对于&#x200B;**[!UICONTROL Admin Session Lifetime (seconds)]**，输入会话在超时之前保持活动状态的秒数。

   ![高级配置 — 管理员安全设置](../configuration-reference/advanced/assets/admin-security.png){width="600" zoomable="yes"}

1. 完成后，单击&#x200B;**[!UICONTROL Save Config]**。

---
title: Google站点工具
description: 了解可用于优化内容、分析流量并将目录连接到购物聚合和市场的Google工具集成。
exl-id: 09c48f1e-792b-4553-82fc-cd1a119b15d0
feature: Marketing Tools, Integration
TQID: https://experienceleague.adobe.com/P-IniOyLDfDk8oe1v9ysmRV6yC7IWpxUBaFF--2YMCg
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: ba9e5be9-7de1-4f71-a5d2-baead0e425eeid: c32adafa-ed01-4b31-997e-2413013911b0id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: b5520579-b31f-4df7-9281-f0d9f91e2edcid: d095671a-1355-40aa-8b5f-06c33c68080bid: eddd9b14-83bd-4ff4-9072-54a4a484abb7id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 662
ht-degree: 0%

---

# Google站点工具

您的商店配置与以下Google工具集成，以帮助优化内容、分析流量并将目录连接到购物聚合和市场。

- [Google Analytics](google-analytics.md) — 使用&#x200B;_Google Universal Analytics_&#x200B;定义额外的自定义维度和量度以进行跟踪，支持离线和移动设备应用程序交互，并可访问正在进行的更新。

- [Google标签管理器](google-tag-manager.md) - ![Adobe Commerce](../assets/adobe-logo.svg)（仅限Adobe Commerce）使用Google标签管理器管理许多与营销活动事件相关的标签。

- [Google AdWords](google-adwords.md) — 创建Google AdWords促销活动并跟踪您应用商店的转化情况。

{{gtag-api-note}}

## Google隐私设置

如果您的企业需要遵守隐私法规，例如[GDPR](../getting-started/compliance-gdpr.md)或[CCPA](../getting-started/compliance-ccpa.md)，请更改Google工具的默认设置以满足隐私要求。 请按照以下步骤操作，以确保您对客户数据的使用始终遵循相关规定。

### 步骤1：更新Google设置

1. [登录到您公司的Google Analytics帐户](https://www.google.com/analytics/){: target="_blank"}。

1. 在左侧边栏的底部，选择&#x200B;**[!UICONTROL Admin]**，然后导航到要编辑的帐户（如果适用）。

1. 在&#x200B;**[!UICONTROL Account]**&#x200B;列中，单击&#x200B;**[!UICONTROL Account Settings]**。

1. 为满足隐私法规要求，请关闭数据共享。

   默认的Google Analytics设置与Google和其他方共享您的公司数据。要关闭数据共享，请清除以下设置的选择复选框：

   - Google产品和服务
   - 基准测试
   - 技术支持
   - 客户专家

1. 接受&#x200B;_数据处理修正_。

   Google广告数据处理术语介绍Google如何处理数据，以及它为遵守GDPR的业务确保数据安全而采取的措施。 此外，还会保留法人主体和联系人信息的记录以及修订。 要[了解详情](https://support.google.com/analytics/answer/3379636){: target="_blank"}，请单击页面顶部消息中的链接。

   - 向下滚动页面至&#x200B;**[!UICONTROL Data Processing Amendment]**。
   - 单击&#x200B;**[!UICONTROL Review Amendment]**&#x200B;以阅读&#x200B;_Google广告数据处理条款_。
   - 单击&#x200B;**[!UICONTROL Accept]**。
   - 单击&#x200B;**[!UICONTROL Save]**。

1. 完成&#x200B;_DPA管理_&#x200B;详细信息。

   - 单击&#x200B;**[!UICONTROL Manage DPA Details]**&#x200B;打开DPA管理页面，您可以在其中编辑联系人和贵组织的法人。

   - 在&#x200B;**[!UICONTROL Legal Entities]**&#x200B;部分中，单击&#x200B;_编辑_ （![Google编辑图标](./assets/google-icon-edit.png) ）图标，并为您的组织添加一个或多个注册名称。 完成后，单击&#x200B;**[!UICONTROL Save]**。

   - 在&#x200B;**联系人**&#x200B;部分中，单击&#x200B;_添加_ （![Google添加图标](./assets/google-icon-add.png) ）图标，然后输入第一个联系人的信息。 接下来，选中每个适用角色的复选框，然后单击&#x200B;**[!UICONTROL Add]**。

      - 主要联系人 — （通知电子邮件地址）接收通知的联系人。
      - 数据保护官员 — （如果适用）为推动隐私法规合规而指定的人员。
      - 欧洲经济区(EEA)代表 — （如果适用）代表欧盟以外客户履行其GDPR义务的人员。

     重复以上步骤以添加其他联系人（如果适用）。

### 步骤2：修改您的Google JS库

Google支持三个JavaScript库来测量网站使用情况，具体取决于Google产品： `gtag.js`、`analytics.js`和`ga.js`。 为了满足隐私要求，可以修改标准代码，如下所示：

#### 将IP地址匿名化

要对&#x200B;**_Google Universal Analytics_**&#x200B;使用的IP地址进行匿名处理，请将以下代码片段添加到Web服务器上的`analytics.js`库中：

analytics.js

```
: `ga('set', 'anonymizeIp', true);`
```

要了解更多信息，请参阅Google帮助中的[Analytics.js字段引用](https://developers.google.com/analytics/devguides/collection/analyticsjs/field-reference){: target="_blank"}。

如果使用旧版`ga.js`库，请添加以下代码片段：

ga.js

```
: `ga('set', 'anonymizeIp', true);`
```

要对&#x200B;**_Google Tag Manager_**&#x200B;使用的IP地址进行匿名处理，请将Web服务器上`gtag.js`库中的`anonymize_ip`参数设置为`true`。

gtag.js

```
: `gtag('event', 'your_event', { 'anonymize_ip': true })`
```

要了解更多信息，请参阅Google帮助中的Analytics中的[IP匿名化](https://support.google.com/analytics/answer/2763052)。

#### 强制SSL

要强制通过安全套接字层(SSL)传输所有Google数据，请将以下代码片段添加到Web服务器上的`analytics.js`库中。

analytics.js

```
: `ga('set', 'forceSSL', true);`
```

### 步骤3：更新您的隐私政策

更新您的[隐私政策](../getting-started/privacy-policy.md)以声明您的公司：

- 使用Google Analytics
- 隐藏IP地址以隐藏个人信息
- 已关闭Google数据共享
- 不将其他Google服务与Google Analytics Cookie结合使用

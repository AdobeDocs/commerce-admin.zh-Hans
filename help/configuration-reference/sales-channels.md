---
title: '[!UICONTROL Sales Channels] > [!UICONTROL Global Settings]'
description: 查看Commerce管理员的[!UICONTROL Sales Channels] &gt； [!UICONTROL Global Settings]页面上的配置设置。
exl-id: 28a5ef4b-265e-457a-9480-96763785b5fd
feature: Configuration, Sales Channels
TQID: https://experienceleague.adobe.com/jnjAspEdJbx3unjmoqgH12JEiLz4ThbgFGeFOArOonU
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 225
ht-degree: 0%

---

# [!UICONTROL Sales Channels] > [!UICONTROL Global Settings]

{{config}}

安装[[!DNL Amazon Sales Channel]](https://experienceleague.adobe.com/docs/commerce-channels/amazon/getting-started/install.html?lang=zh-Hans)时，这些设置可用。

![Sales Channel设置](./assets/config-sales-channel-global-settings.png)<!-- zoom -->

| 字段 | [作用域](../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|-----|---------|------|
| [!UICONTROL Clear Log History] | 全局 | 选项：<br/><br/>**`Once Daily`**：选择此选项可每天清除一次商店的活动历史记录。<br/><br/>**`Once Weekly`**：选择此选项可每周清除一次商店的活动历史记录。<br/><br/>**`Once Monthly`**： （默认）选择此选项可每月清除一次商店的活动历史记录。 |
| [!UICONTROL Background Tasks (CRON) Source] | 全局 | 选择`Magento CRON`以指定[!DNL Amazon Sales Channel]使用您的Commerce cron设置来确定与Amazon Seller Central的通信和数据同步时间间隔。 |
| [!UICONTROL Enable Debug Logging] | 全局 | 选择`Enabled`以在需要故障排除时收集其他同步数据。<br/><br/>此选项默认处于禁用状态，应仅在疑难解答需要时启用，因为继续记录会对性能产生负面影响。 如果为疑难解答启用，则应在完成时将其禁用。 |
| [!UICONTROL Read-Only Mode] | 全局 | 选择`Enabled`以阻止所有传出状态更改的API请求。 在禁用只读模式之前，可能会保存更改，但不会发送更改。 要再次启动数据传输，请选择`Disabled`。<br/><br/>当数据库迁移到实例的新副本时（当存储的URL在配置中更改时检测到），只读模式会自动启用。<br/><br/>这是设计用于生产实例的副本，如&#x200B;_Staging_&#x200B;或&#x200B;_QA_，不应在生产实例上使用。<br/><br/>**_注意&#x200B;_**：必须清除配置缓存才能启用[!UICONTROL Read-Only Mode]。 |

{style="table-layout:auto"}

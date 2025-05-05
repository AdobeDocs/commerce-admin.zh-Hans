---
title: 计划订单工序
description: 了解支持此功能的计划订单操作和订单cron设置。
exl-id: 330fe75a-d901-4696-946e-fa7af9ea3d40
feature: Orders, Configuration
source-git-commit: fdc14758788fa5cd0391371ebfafb478dadec8a4
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 0%

---

# 计划订单工序

使用[Cron](../systems/cron.md)作业来计划以下顺序处理任务：

![订单网格](./assets/orders-grid.png){width="700" zoomable="yes"}

## 设置待定付款订单生命周期

具有待处理付款的订单的生命周期由&#x200B;_订单Cron设置_&#x200B;配置决定。 默认值为480分钟，即8小时。

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧面板中，展开&#x200B;**[!UICONTROL Sales]**&#x200B;部分并在下面选择&#x200B;**[!UICONTROL Sales]**。

1. 展开&#x200B;**[!UICONTROL Orders Cron Settings]**&#x200B;部分的![扩展选择器](../assets/icon-display-expand.png)。

   ![订单Cron设置](../configuration-reference/sales/assets/sales-orders-cron-settings.png){width="600" zoomable="yes"}

1. 对于&#x200B;**[!UICONTROL Pending Payment Order Lifetime (minutes)]**，请输入挂起的付款过期之前的分钟数。

1. 单击&#x200B;**[!UICONTROL Save Config]**。

## 启用计划的网格更新并重新编制索引

网格设置配置将计划更新到以下订单管理网格，并按[Cron](../systems/cron.md)的计划重新索引数据：

- [订购](orders.md#orders-workspace)
- [发票](invoices.md)
- [装运](shipments.md)
- [贷项通知单](credit-memos.md)

通过调度这些任务，可以避免在保存数据时发生的锁定，并减少处理时间。 启用后，任何更新仅在计划的cron作业期间发生。 为获得最佳结果，应将Cron配置为每分钟运行一次。

**_要启用更新并重新编制索引：_**

仅[!BADGE PaaS]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="仅适用于云项目(Adobe管理的PaaS基础架构)和内部部署项目上的Adobe Commerce 。"}启用[生产模式](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/setup/application-modes.html#production-mode)&#x200B;(云基础架构上的Adobe Commerce中使用的默认模式)时，请运行以下命令：

`bin/magento config:set dev/grid/async_indexing 1`

启用[默认模式](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/setup/application-modes.html#default-mode)时，请完成以下步骤：

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧面板中，展开&#x200B;**[!UICONTROL Advanced]**&#x200B;部分并选择&#x200B;**[!UICONTROL Developer]**。

1. 展开&#x200B;**[!UICONTROL Grid Settings]**&#x200B;部分的![扩展选择器](../assets/icon-display-expand.png)。

1. 将&#x200B;**[!UICONTROL Asynchronous Indexing]**&#x200B;设置为`Enable`。

   ![网格设置](../configuration-reference/advanced/assets/developer-grid-settings.png){width="600" zoomable="yes"}

1. 单击&#x200B;**[!UICONTROL Save Config]**。

---
title: 计划订单工序
description: 了解支持此功能的计划订单操作和订单cron设置。
exl-id: 330fe75a-d901-4696-946e-fa7af9ea3d40
feature: Orders, Configuration
source-git-commit: db859c40cd6f052a8f1153e245c23d9f1ea97d33
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 0%

---

# 计划订单工序

使用 [Cron](../systems/cron.md) 作业来计划以下订单处理任务：

![订单网格](./assets/orders-grid.png){width="700" zoomable="yes"}

## 设置待定付款订单生命周期

含未决付款的订单的期限由 _订单Cron设置_ 配置。 默认值为480分钟，即8小时。

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中，展开 **[!UICONTROL Sales]** 部分并选择 **[!UICONTROL Sales]** 下方。

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Orders Cron Settings]** 部分。

   ![订单Cron设置](../configuration-reference/sales/assets/sales-orders-cron-settings.png){width="600" zoomable="yes"}

1. 对象 **[!UICONTROL Pending Payment Order Lifetime (minutes)]**，输入待处理付款过期之前经过的分钟数。

1. 单击 **[!UICONTROL Save Config]**.

## 启用计划的网格更新并重新编制索引

“网格设置”配置计划更新以下订单管理网格，并按计划重新索引数据 [Cron](../systems/cron.md)：

- [订购](orders.md#orders-workspace)
- [发票](invoices.md)
- [装运](shipments.md)
- [贷项通知单](credit-memos.md)

通过调度这些任务，可以避免在保存数据时发生的锁定，并减少处理时间。 启用后，任何更新仅在计划的cron作业期间发生。 为获得最佳结果，应将Cron配置为每分钟运行一次。

**_要启用更新并重新编制索引，请执行以下操作：_**

时间 [生产模式](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/setup/application-modes.html#production-mode) (云基础架构上的Adobe Commerce中使用的默认模式)已启用，请运行以下命令：

``bin/magento config:set dev/grid/async_indexing 1``

时间 [默认模式](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/setup/application-modes.html#default-mode) 已启用，请完成以下步骤：

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中，展开 **[!UICONTROL Advanced]** 部分并选择 **[!UICONTROL Developer]**.

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Grid Settings]** 部分。

1. 设置 **[!UICONTROL Asynchronous Indexing]** 到 `Enable`.

   ![网格设置](../configuration-reference/advanced/assets/developer-grid-settings.png){width="600" zoomable="yes"}

1. 单击 **[!UICONTROL Save Config]**.

---
title: 允许取消订单
description: 了解如何为您的客户提供取消功能。
feature: Orders, Storefront
exl-id: 5a8ef668-f929-4188-8574-0bccdd076f3e
source-git-commit: a9d1dc4fe50e98f0f1dfc8ec204930e2cc885d6e
workflow-type: tm+mt
source-wordcount: '300'
ht-degree: 0%

---

# 允许取消订单

启用后，您可以直接从客户帐户取消订单。 默认情况下禁用取消。

## 为订单启用的取消条件

- 必须启用&#x200B;_允许取消订单_&#x200B;配置选项。

- 如果订单处于`Hold`、`Canceled`、`Complete`或`Closed`状态，则店面将禁用取消选项。

- 如果订单中的任何项目已发运，则店面将禁用取消选项。

- 如果存在已付款的项目，则会启用取消选项，并为该项目创建退款。

- 如果订单处于`Pending`或`Processing`状态，则店面中已启用取消选项。

## 配置以允许客户取消并自定义取消原因

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧面板中，展开&#x200B;**[!UICONTROL Sales]**&#x200B;并选择&#x200B;**[!UICONTROL Sales]**。

1. 展开&#x200B;**[!UICONTROL Order cancellation]**&#x200B;部分的![扩展选择器](../assets/icon-display-expand.png)。

   ![订单取消选项](../configuration-reference/sales/assets/sales-order-cancellation.png){width="600" zoomable="yes"}

1. 将&#x200B;**[!UICONTROL Order cancellation through GraphQL]**&#x200B;设置为`Yes`。

   此设置从店面的客户帐户启用取消功能。

1. 在&#x200B;**[!UICONTROL Order Order cancellation reasons]**&#x200B;中，您可以添加、删除或修改任何取消原因。

   使用此设置，当客户取消订单时，取消原因会显示在店面中。
请确保您至少指定了一个原因。

1. 单击&#x200B;**[!UICONTROL Save Config]**。

## 从店面取消

客户可以从以下三个页面为特定订单启动取消功能：

- _我的订单_&#x200B;页

- _订单视图_&#x200B;页面

- _我的帐户_&#x200B;页面

### 我的订单

如果可以取消订单，则“我的订单”页中会显示&#x200B;_取消订单_&#x200B;按钮。

![店面示例 — “我的订单”页面](./assets/my-order-page-view-cancel.png){width="700" zoomable="yes"}

### 订单查看页面

如果可以取消订单，“查看订单”页面中会显示&#x200B;_取消订单_&#x200B;按钮。

![订单详细信息页面](./assets/order-view-page-cancel.png){width="700" zoomable="yes"}

### 我的帐户

如果可以取消订单，“我的帐户”页的“最近订单”部分将显示&#x200B;_取消订单_&#x200B;按钮。

![我的帐户页](./assets/my-account-page-view-cancel.png){width="700" zoomable="yes"}

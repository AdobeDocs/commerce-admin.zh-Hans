---
title: 允许重新排序
description: 了解如何为您的客户提供重新订购功能。
exl-id: 9fe4c4fb-8596-4fd0-a93b-927ebdfc0c94
feature: Orders, Storefront
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '432'
ht-degree: 0%

---

# 允许重新排序

启用后，可以直接从客户帐户或&#x200B;_管理员_&#x200B;中的原始订单进行重新排序。 默认情况下，将启用重新排序。

![管理员中的客户重新排序链接](./assets/customer-reorder.png){width="700" zoomable="yes"}

## 为订单启用重新排序的条件

- 必须启用&#x200B;_允许重新排序_&#x200B;配置选项。

- 如果订单处于`Hold`或`Payment Review`状态，则重新排序选项被禁用。

- 如果订单中的任何项目不可用、缺货或已禁用，店面将禁用重新排序选项。

- 即使任何项目缺货或停用，_管理员_&#x200B;也可以重新排序。

## 配置以允许客户重新订购

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧面板中，展开&#x200B;**[!UICONTROL Sales]**&#x200B;并在下面选择&#x200B;**[!UICONTROL Sales]**。

1. 展开&#x200B;**[!UICONTROL Reorder]**&#x200B;部分的![扩展选择器](../assets/icon-display-expand.png)。

   ![重新排序选项](../configuration-reference/sales/assets/sales-reorder.png){width="600" zoomable="yes"}

1. 将&#x200B;**[!UICONTROL Allow Reorder]**&#x200B;设置为`Yes`。

   此设置从管理员的店面或订单列表中的客户帐户启用重新排序功能。

1. 单击&#x200B;**[!UICONTROL Save Config]**。

## 从店面重新排序

客户可以从以下两个页面启动特定订单的重新订购功能：

- _我的订单_&#x200B;页

- _订单视图_&#x200B;页面

### 我的订单

带有订单的列表中始终显示&#x200B;_重新排序_&#x200B;按钮（即使订单中的所有产品都不可重新排序）。

![店面示例 — “我的订单”页面](./assets/my-order-page-view.png){width="700" zoomable="yes"}

**案例1。**&#x200B;订单中的所有产品均&#x200B;**可用**&#x200B;进行重新排序

用户被重定向到购物车，并且所有产品都已添加到购物车

![购物车](./assets/shopping-cart-page.png){width="700" zoomable="yes"}

**案例2.**&#x200B;订单中的部分/所有产品&#x200B;**不可用**&#x200B;重新排序

>[!NOTE]
>
>可以对`Not Visible Individually`产品重新排序。

_重新排序_&#x200B;按钮未出现在&#x200B;_我的订单_&#x200B;和&#x200B;_查看订单_&#x200B;页面上。

![我的订单页1](./assets/my-orders-view-page1.png){width="700" zoomable="yes"}

### 订单查看页面

**案例1。**&#x200B;订单中的所有产品都可供重新订购

用户被重定向到购物车，并且所有产品都已添加到购物车

**案例2.**&#x200B;订单中的部分/所有产品&#x200B;**不可用**&#x200B;重新排序

>[!NOTE]
>
>可以对`Not Visible Individually`产品重新排序。

_重新排序_&#x200B;按钮未出现在&#x200B;_我的订单_&#x200B;和&#x200B;_查看订单_&#x200B;页面上。

![订单详细信息页面](./assets/order-view-page.png){width="700" zoomable="yes"}

### 购物车不为空

如果购物车不为空且用户单击&#x200B;**[!UICONTROL Reorder]**（从&#x200B;_我的订单_&#x200B;或&#x200B;_订单视图_&#x200B;页面），则现有产品将保留在购物车中，并添加重新订购产品。

![对项目重新排序](./assets/shopping-cart-view1.png){width="700" zoomable="yes"}

## 管理员重新排序

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Sales]** > **[!UICONTROL Orders]**。

1. 找到订单并在&#x200B;**[!UICONTROL View]**&#x200B;模式下打开。

1. 单击顶部按钮栏中显示的&#x200B;**[!UICONTROL Reorder]**。

   ![管理员中的订单详细信息](./assets/order-view-admin.png){width="600" zoomable="yes"}

   单击&#x200B;**[!UICONTROL Reorder]**&#x200B;后，将打开&#x200B;_新建订单_&#x200B;页面，其中对产品进行了重新排序。

   ![创建重新排序](./assets/create-reorder-page.png){width="600" zoomable="yes"}

1. 根据需要填写所有必填字段。

1. 要提交订单，请单击&#x200B;**[!UICONTROL Submit Order]**。

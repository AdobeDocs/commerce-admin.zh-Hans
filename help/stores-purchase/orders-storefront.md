---
title: 店面订单管理
description: 了解客户如何在Commerce店面查看和管理其订单历史记录。
exl-id: 85d953e6-f5a1-4a5e-a6ef-36b9cf6988bb
feature: Orders, Storefront
source-git-commit: c13a4b730ed70ed4829cc20b13c2723137dcbb3a
workflow-type: tm+mt
source-wordcount: '753'
ht-degree: 0%

---

# 店面订单管理

客户可以从其帐户访问其所有订单。 订单可以查看、过滤、跟踪和重新提交为新订单。 根据订单的状态，客户可以打印其订单、发票、发运和退款记录。

## 筛选订单

{{b2b-feature}}

您的初始&#x200B;_[!UICONTROL My Orders]_&#x200B;结果还包含来自商业实例中所有网站的从属用户的匹配订单。 与公司帐户关联的客户可以筛选订单列表，以快速查找结果中的记录。 要显示筛选器选项，客户单击&#x200B;**[!UICONTROL Filter]**，然后单击&#x200B;**[!UICONTROL Close]**&#x200B;以隐藏筛选器。

![我的订单](./assets/account-dashboard-my-orders-b2b.png){width="700" zoomable="yes"}

| 筛选 | 描述 |
| ------ | ----------- |
| [!UICONTROL SKU or Product Name] | 输入SKU或产品名称。 |
| [!UICONTROL Order Number] | 可以是完整或部分订单编号。 |
| [!UICONTROL Order Status] | 从下拉列表中选择值以按状态筛选。 |
| [!UICONTROL Invoice Number] | 输入完整的或部分发票编号。 |
| [!UICONTROL Order Date] | 设置一个或两个日期字段以按订单日期过滤。 |
| [!UICONTROL Created by] | 按订单创建者筛选公司订单。 |
| [!UICONTROL Order Total] | 设置最小值、最大值或同时设置这两个值，以按订单合计进行筛选。 |

## 查看订单

客户在列表中找到订单并单击&#x200B;**[!UICONTROL View Order]**。 从未结订单中，他们可以执行以下任一操作：

![查看订单](./assets/customer-account-order-items-ordered.png){width="700" zoomable="yes"}

### 查看最近订购的产品

对于在下订单后登录的客户，**[!UICONTROL Recent Orders]**&#x200B;块会显示在侧边栏和&#x200B;**[!UICONTROL My Account]**&#x200B;页面上。 它显示上次购买的五个产品。

客户可以通过选择产品并单击&#x200B;**[!UICONTROL Add to Cart]**&#x200B;将产品读入购物车。 他们还可以通过单击&#x200B;**[!UICONTROL View all]**&#x200B;查看最后的订单，该订单将重定向到&#x200B;_[!UICONTROL My Account]_&#x200B;页面和&#x200B;**[!UICONTROL Recent Orders]**&#x200B;块。

### 打印订单

1. 客户单击&#x200B;**[!UICONTROL Print Order]**。

1. 按照“打印”对话框中的说明完成打印。

### 打印发票

1. 在&#x200B;**[!UICONTROL Invoices]**&#x200B;选项卡上，客户单击以下任一项：

   - **[!UICONTROL Print All Invoices]**

   - **[!UICONTROL Print Invoice]**

   ![发票](./assets/customer-account-order-invoices.png){width="700" zoomable="yes"}

1. 使用“打印”对话框完成打印。

### 打印装运

1. 在&#x200B;**[!UICONTROL Order Shipments]**&#x200B;选项卡上，客户单击以下任一项：

   - **[!UICONTROL Print All Shipments]**

   - **[!UICONTROL Print Shipment]**

   ![打印所有装运](./assets/customer-account-order-shipments.png){width="700" zoomable="yes"}

1. 使用“打印”对话框完成打印。

### 跟踪装运

1. 在&#x200B;**[!UICONTROL Order Shipments]**&#x200B;选项卡上，单击&#x200B;**[!UICONTROL Track this Shipment]**。

   任何可用的跟踪信息都会显示在弹出窗口中。

1. 准备就绪后，客户单击&#x200B;**[!UICONTROL Close Window]**。

### 打印退款

1. 在&#x200B;**退款**&#x200B;选项卡上，客户单击以下任一项：

   - **打印所有退款**

   - **打印退款**

   ![退款](./assets/customer-account-order-refunds.png){width="700" zoomable="yes"}

1. 使用“打印”对话框完成打印。

启用&#x200B;[_允许重新排序_](reorders-allow.md)&#x200B;配置选项后，客户可以使用重新排序。

客户可以从以下两个页面启动特定订单的重新订购功能：

- “我的订单”页
- 订单查看页面

## 重新排序

_[!UICONTROL Reorder]_&#x200B;链接显示在列表中，订单位于&#x200B;_[!UICONTROL View]_&#x200B;链接附近。

![重新排序我的订单页面上的链接](./assets/account-dashboard-reorder.png){width="700" zoomable="yes"}

**案例1。**&#x200B;订单中的所有产品都可供重新订购

客户将被重定向到购物车，并且所有产品都会添加到购物车。

**案例2.**&#x200B;订单中的部分/所有产品不可重新订购

>[!NOTE]
>
>可以对`Not Visible Individually`产品重新排序。

_[!UICONTROL Reorder]_&#x200B;链接未出现在&#x200B;_[!UICONTROL My Orders]_&#x200B;和&#x200B;_[!UICONTROL View Order]_&#x200B;页面上。

![我的订单页](./assets/account-dashboard-reorder-grid.png){width="700" zoomable="yes"}

>[!TIP]
>
>如果购物车不为空且客户单击&#x200B;**[!UICONTROL Reorder]** （从[!UICONTROL My Orders]或[!UICONTROL Order View]页面），则现有产品将保留在购物车中，并添加重新订购产品。

## 取消订单

启用&#x200B;[_允许取消_](cancel-allow.md)&#x200B;配置选项后，客户即可使用“取消”。

客户可以从以下三个页面为特定订单启动取消功能：

- “我的订单”页
- 订单查看页面
- 我的帐户页面

_[!UICONTROL Cancel Order]_&#x200B;链接显示在&#x200B;_[!UICONTROL Reorder]_&#x200B;链接附近。 如果无法取消订单，则不会显示链接。

在“我的订单”页面上![取消链接](./assets/account-dashboard-cancel.png){width="700" zoomable="yes"}

要执行取消，客户：

1. 单击&#x200B;**[!UICONTROL Cancel Order]**

1. 提供取消原因

   ![取消订单原因](./assets/cancel-order-reasons.png){width="700" zoomable="yes"}

   您可以在&#x200B;[_允许取消_](cancel-allow.md)&#x200B;页面上自定义取消原因。

1. 单击&#x200B;**[!UICONTROL Confirm]**

   在“我的订单”页面上![取消](./assets/cancel-order.png){width="700" zoomable="yes"}

   取消后，将处理处于&#x200B;_[!UICONTROL Pending]_&#x200B;状态、更改为&#x200B;_[!UICONTROL Canceled]_&#x200B;状态、处于&#x200B;_[!UICONTROL Processing]_&#x200B;状态、更改为&#x200B;_[!UICONTROL Closed]_&#x200B;状态以及退款的订单。

   取消完成后，会向客户发送电子邮件。

   ![取消订单电子邮件](./assets/cancel-order-email.png){width="700" zoomable="yes"}

   取消信息将添加到客户的订单历史记录中。 它显示在订单的注释内和“注释历史记录”选项卡中。

   ![取消订单备注](./assets/cancel-order-notes.png){width="700" zoomable="yes"}

   ![取消评论历史记录](./assets/cancel-order-comments.png){width="700" zoomable="yes"}

   如果由于某种原因订单更改为无法取消的状态，且客户未刷新页面，则仍会显示取消订单的链接。 但是，当他们尝试取消时，会显示错误消息。

   ![取消订单错误消息](./assets/cancel-order-error-message.png){width="700" zoomable="yes"}

   刷新页面后，您可以看到订单已完成，这就是取消不起作用的原因。

   ![刷新后取消订单](./assets/cancel-order-after-refresh.png){width="700" zoomable="yes"}

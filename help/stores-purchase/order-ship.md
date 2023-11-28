---
title: 发送订单
description: 了解如何填写处理订单的配送信息，以及查看配送和跟踪信息。
exl-id: 60b0e66a-8ee6-4091-94ce-179cc2fdf57a
feature: Orders, Shipping/Delivery
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '448'
ht-degree: 0%

---

# 发送订单

已付款但正在等待装运的订单具有 `Processing` 状态。 装运记录包含与订单关联的履行流程的详细历史记录。 在订单履行之前，可以发运部分货物。

1. 在 _管理员_ 侧栏，选择 **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. 在 _[!UICONTROL Orders]_列表，查找要发运的订单，然后单击以将其打开。

1. 在右上角，单击 **[!UICONTROL Ship]** 按钮。

1. 如果要更新帐单或送货地址，请单击 **[!UICONTROL Edit]** 在部分的右上角显示的链接。

   进行必要的更改，然后单击 **[!UICONTROL Save Order Address]**.

1. 要让承运人生成装运标签，请选择 **[!UICONTROL Create Shipping Label]** 复选框，并设置以下选项：

   - 要添加跟踪编号，请向下滚动到 _[!UICONTROL Shipping Information]_部分，然后单击&#x200B;**[!UICONTROL Add Tracking Number]**.

   - 执行以下操作之一：

      - 选择 **[!UICONTROL Carrier]** 并输入跟踪 **[!UICONTROL Number]**.

      - 设置 **[!UICONTROL Carrier]** 到 `Custom Value`，输入 **[!UICONTROL Title]** ，然后输入跟踪 **[!UICONTROL Number]**.

      - [查看跟踪信息](#track-the-shipment).

1. 要进行部分发运，请向下滚动到“要发运的物料”部分，然后输入 **[!UICONTROL Qty to Ship]** 每个项目。

1. 要通过电子邮件将发运通知客户，请执行以下操作：

   - 输入您要包含在 **[!UICONTROL Shipment Comments]** 盒子。

   - 要在发送给客户的通知电子邮件中包含注释，请选择 **[!UICONTROL Append Comments]** 复选框。

   - 要向自己发送装运电子邮件的副本，请选择 **[!UICONTROL Email Copy of Shipment]** 复选框。

     发票电子邮件的状态显示在已完成发票的发票编号旁边，表示已发送或未发送。

1. 完成后，单击 **[!UICONTROL Submit Shipment]**.

   订单的状态更改自 `Processing` 到 `Complete`.

>[!NOTE]
>
>如果以“店内交货”方式下订单，则无法使用配送选项。 单击 **[!UICONTROL Notify Order is Ready for Pickup]** 以触发发送给客户的电子邮件。 订单的状态随后更改为 `Complete`.

## 查看装运详细信息

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Sales]** > **[!UICONTROL Shipments]**.

1. 在列表中查找装运，然后单击以打开记录。

1. 如果要在订单中添加评论，请向下滚动到 _[!UICONTROL Comments History]_部分，然后在框中输入注释。

   - 要通过电子邮件向客户发送评论，请选择 **[!UICONTROL Notify Customer by Email]** 复选框。

   - 要在客户帐户中发布评论，请选择 **[!UICONTROL Visible on Frontend]** 复选框。

1. 单击 **[!UICONTROL Submit Comment]**.

## 跟踪装运

**方法1：** 从订单信息选项卡

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. 在网格中查找装运订单，然后单击 **[!UICONTROL View]**.

1. 向下滚动到 _[!UICONTROL Shipping & Handling Information]_部分并单击&#x200B;**[!UICONTROL Track Order]**.

   任何可用的跟踪信息都会显示在弹出窗口中。

1. 准备就绪后，单击 **[!UICONTROL Close Window]**.

**方法2：** 从订单发运标签

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Sales]** > **[!UICONTROL Shipments]**.

1. 在列表中查找装运，然后单击以打开记录。

1. 单击 **[!UICONTROL Track this Shipment]**.

   任何可用的跟踪信息都会显示在弹出窗口中。

1. 准备就绪后，单击 **[!UICONTROL Close Window]**.

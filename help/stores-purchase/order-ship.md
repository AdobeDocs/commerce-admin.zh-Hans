---
title: 发送订单
description: 了解如何填写处理订单的配送信息，以及查看配送和跟踪信息。
exl-id: 60b0e66a-8ee6-4091-94ce-179cc2fdf57a
feature: Orders, Shipping/Delivery
TQID: https://experienceleague.adobe.com/w1MPvqsRVfsRwEcRB5uClGM3vnwAda3sOtkZzuLBKAA
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 453
ht-degree: 0%

---

# 发送订单

已付款但正在等待装运的订单具有`Processing`状态。 装运记录包含与订单关联的履行流程的详细历史记录。 在订单履行之前，可以发运部分货物。

1. 在&#x200B;_管理员_&#x200B;侧边栏上，选择&#x200B;**[!UICONTROL Sales]** > **[!UICONTROL Orders]**。

1. 在&#x200B;_[!UICONTROL Orders]_列表中，找到要发运的订单，然后单击以将其打开。

1. 单击右上角的&#x200B;**[!UICONTROL Ship]**&#x200B;按钮。

1. 如果要更新帐单或送货地址，请单击部分右上角的&#x200B;**[!UICONTROL Edit]**&#x200B;链接。

   进行必要的更改，然后单击&#x200B;**[!UICONTROL Save Order Address]**。

1. 要让承运人生成装运标签，请选中&#x200B;**[!UICONTROL Create Shipping Label]**&#x200B;复选框并设置选项：

   - 要添加跟踪编号，请向下滚动到&#x200B;_[!UICONTROL Shipping Information]_部分，然后单击&#x200B;**[!UICONTROL Add Tracking Number]**。

   - 执行以下操作之一：

      - 选择&#x200B;**[!UICONTROL Carrier]**&#x200B;并输入跟踪&#x200B;**[!UICONTROL Number]**。

      - 将&#x200B;**[!UICONTROL Carrier]**&#x200B;设置为`Custom Value`，输入自定义运营商的&#x200B;**[!UICONTROL Title]**，然后输入跟踪&#x200B;**[!UICONTROL Number]**。

      - [查看跟踪信息](#track-the-shipment)。

1. 要进行部分发运，请向下滚动到“要发运的项目”部分，然后为每个项目输入&#x200B;**[!UICONTROL Qty to Ship]**。

1. 要通过电子邮件将发运通知客户，请执行以下操作：

   - 在&#x200B;**[!UICONTROL Shipment Comments]**&#x200B;框中输入您要包含的任何注释。

   - 要在发送给客户的通知电子邮件中包含注释，请选中&#x200B;**[!UICONTROL Append Comments]**&#x200B;复选框。

   - 要向自己发送装运电子邮件的副本，请选中&#x200B;**[!UICONTROL Email Copy of Shipment]**&#x200B;复选框。

     发票电子邮件的状态显示在已完成发票的发票编号旁边，表示已发送或未发送。

1. 完成后，单击&#x200B;**[!UICONTROL Submit Shipment]**。

   订单的状态从`Processing`更改为`Complete`。

>[!NOTE]
>
>如果以“店内交货”方式下订单，则无法使用配送选项。 单击&#x200B;**[!UICONTROL Notify Order is Ready for Pickup]**&#x200B;以触发发送给客户的电子邮件。 订单的状态随后更改为`Complete`。

## 查看装运详细信息

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Sales]** > **[!UICONTROL Shipments]**。

1. 在列表中查找装运，然后单击以打开记录。

1. 如果要向订单添加评论，请向下滚动到&#x200B;_[!UICONTROL Comments History]_部分，然后在框中输入评论。

   - 要通过电子邮件将评论发送给客户，请选中&#x200B;**[!UICONTROL Notify Customer by Email]**&#x200B;复选框。

   - 要在客户的帐户中发布评论，请选中&#x200B;**[!UICONTROL Visible on Frontend]**&#x200B;复选框。

1. 单击&#x200B;**[!UICONTROL Update]**。

## 跟踪装运

**方法1：**&#x200B;来自订单信息选项卡

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Sales]** > **[!UICONTROL Orders]**。

1. 在网格中查找装运订单，然后单击&#x200B;**[!UICONTROL View]**。

1. 向下滚动到&#x200B;_[!UICONTROL Shipping & Handling Information]_部分，然后单击&#x200B;**[!UICONTROL Track Order]**。

   任何可用的跟踪信息都会显示在弹出窗口中。

1. 准备就绪后，单击&#x200B;**[!UICONTROL Close Window]**。

**方法2：**&#x200B;来自订单发运标签

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Sales]** > **[!UICONTROL Shipments]**。

1. 在列表中查找装运，然后单击以打开记录。

1. 单击&#x200B;**[!UICONTROL Track this Shipment]**。

   任何可用的跟踪信息都会显示在弹出窗口中。

1. 准备就绪后，单击&#x200B;**[!UICONTROL Close Window]**。

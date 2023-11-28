---
title: 货到付款(COD)
description: 了解如何将货到付款设置为商店的离线付款方式。
exl-id: dcf94734-a66e-4d32-b389-b47c979ceaa9
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 0%

---

# 货到付款(COD)

Adobe Commerce和Magento Open Source允许您接受 _货到付款_ (COD)购买支付。 您只能接受来自特定国家/地区的货到付款申请，而且您可以对配置进行微调，使其具有最小和最大订单总限额。

装运承运人会在交货时收到客户的付款，然后会将付款转给您。 您可以调整承运人服务收取的任何运费和手续费。

**_要设置货到付款付款，请执行以下操作：_**

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中，展开 **[!UICONTROL Sales]** 并选择 **[!UICONTROL Payment Methods]**.

1. 下 _其他支付方式_，展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Cash On Delivery Payment]** 部分。

   ![货到付款](../configuration-reference/sales/assets/payment-methods-cash-on-delivery-payment.png){width="600" zoomable="yes"}

   有关每个配置设置的详细说明，请参阅 [货到付款](../configuration-reference/sales/payment-methods.md#cash-on-delivery-payment) 在 _配置参考指南_.

   >[!NOTE]
   >
   >如有必要，请先清除 **[!UICONTROL Use system value]** 复选框以更改这些设置。

1. 要激活交货时付款，请设置 **[!UICONTROL Enabled]** 到 `Yes`.

1. 对象 **[!UICONTROL Title]**，输入在结账期间标识COD支付方式的标题。

1. 设置 **[!UICONTROL New Order Status]** 到 `Pending` 直到确认收到付款。

   如果您愿意，可以使用 `Processing` 或 `Suspected Fraud` 使用此付款方法的新订单的状态。

1. 设置 **[!UICONTROL Payment from Applicable Countries]** 更改为以下任一项：

   - `All Allowed Countries`  — 来自所有客户的客户 [国家/地区](../getting-started/store-details.md#country-options) 在商店配置中指定的可使用此付款方式。
   - `Specific Countries`  — 选择此选项后， _[!UICONTROL Payment from Specific Countries]_列表出现。 要选择多个国家/地区，请按住Ctrl键(PC)或Command键(Mac)并单击每个选项。

1. 输入 **[!UICONTROL Instructions]** 接受货到付款订单的交货。

1. 设置 **[!UICONTROL Minimum Order Total]** 和 **[!UICONTROL Maximum Order Total]** 符合货到付款条件的订单金额。

   >[!NOTE]
   >
   >订单符合合计在最小或最大订单合计之间或与最小或最大订单合计匹配的条件。

1. 对象 **[!UICONTROL Sort Order]**，请输入一个数字，以确定此项目在结账时显示的付款方式列表中的位置。

   此数字相对于其他支付方式。 (`0` =第一个， `1` =秒， `2` =第三，依此类推。)

1. 完成后，单击 **[!UICONTROL Save Config]**.

---
title: 支票和汇票
description: 了解如何将支票和汇票设置为商店的离线付款方式。
exl-id: e004f0c3-f659-4b08-a41a-88bfc05acaab
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 0%

---

# 支票和汇票

Adobe Commerce和Magento Open Source允许您接受支票或汇票付款。 此 _支票/汇票_ 默认情况下，您的商店已启用付款方式。 您只能接受来自特定国家/地区的支票和汇票，并且您可以对配置进行微调，使其具有最小和最大订单总限制。

**_要通过支票或汇票配置付款，请执行以下操作：_**

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中，展开 **[!UICONTROL Sales]** 并选择 **[!UICONTROL Payment Methods]**.

1. 下 _[!UICONTROL Other Payment Methods]_，展开 ![扩展选择器](../assets/icon-display-expand.png) 该&#x200B;**[!UICONTROL Check / Money Order]**部分。

   ![支票/汇票](../configuration-reference/sales/assets/payment-methods-check-money-order.png){width="600" zoomable="yes"}

   有关每个配置设置的详细说明，请参阅 [支票/汇票](../configuration-reference/sales/payment-methods.md#check--money-order) 在 _配置参考指南_.

   >[!NOTE]
   >
   >如有必要，请先清除 **[!UICONTROL Use system value]** 复选框以更改这些设置。

1. 要接受支票或汇票付款，请设置 **[!UICONTROL Enabled]** 到 `Yes`.

1. 对象 **[!UICONTROL Title]**，输入在结账时标识支票/汇票支付方式的标题。

1. 如果订单通常等待批准，则接受默认值 **[!UICONTROL New Order Status]** 作为 `Pending"` 直到它获得批准。

   如果您愿意，可以使用 `Processing` 或 `Suspected Fraud` 使用此付款方法的新订单的状态。

1. 设置 **[!UICONTROL Payment from Applicable Countries]** 更改为以下任一项：

   - `All Allowed Countries`  — 来自所有客户的客户 [国家/地区](../getting-started/store-details.md#country-options) 在商店配置中指定的可使用此付款方式。
   - `Specific Countries`  — 选择此选项后， _[!UICONTROL Payment from Specific Countries]_列表出现。 要选择多个国家/地区，请按住Ctrl键(PC)或Command键(Mac)并单击每个选项。

1. 对象 **[!UICONTROL Make Check Payable To]**，输入支票必须支付到的交易方名称。

1. 对象 **[!UICONTROL Send Check To]**，输入邮寄支票的街道地址或邮政信箱。

1. 设置 **[!UICONTROL Minimum Order Total]** 和 **[!UICONTROL Maximum Order Total]** 此付款方式所需的订单金额。

   >[!NOTE]
   >
   >如果合计在最小或最大合计值之间，或者与最小或最大合计值完全匹配，则订单合格。

1. 对象 **[!UICONTROL Sort Order]**，请输入一个数字，以确定此项目在结账时显示的付款方式列表中的位置。

   此数字相对于其他支付方式。 (`0` =第一个， `1` =秒， `2` =第三，依此类推。)

1. 完成后，单击 **[!UICONTROL Save Config]**.

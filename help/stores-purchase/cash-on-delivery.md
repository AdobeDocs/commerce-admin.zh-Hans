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

Adobe Commerce和Magento Open Source允许您接受针对购买的&#x200B;_货到付款_ (COD)。 您只能接受来自特定国家/地区的货到付款申请，而且您可以对配置进行微调，使其具有最小和最大订单总限额。

装运承运人会在交货时收到客户的付款，然后会将付款转给您。 您可以调整承运人服务收取的任何运费和手续费。

**_要设置货到付款现金：_**

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧面板中，展开&#x200B;**[!UICONTROL Sales]**&#x200B;并选择&#x200B;**[!UICONTROL Payment Methods]**。

1. 在&#x200B;_其他付款方式_&#x200B;下，展开![扩展选择器](../assets/icon-display-expand.png) **[!UICONTROL Cash On Delivery Payment]**&#x200B;部分。

   ![货到付款](../configuration-reference/sales/assets/payment-methods-cash-on-delivery-payment.png){width="600" zoomable="yes"}

   有关这些配置设置的详细说明，请参阅&#x200B;_配置参考指南_&#x200B;中的[货到付款付款](../configuration-reference/sales/payment-methods.md#cash-on-delivery-payment)。

   >[!NOTE]
   >
   >如有必要，请先清除&#x200B;**[!UICONTROL Use system value]**&#x200B;复选框以更改这些设置。

1. 要激活货到付款付款，请将&#x200B;**[!UICONTROL Enabled]**&#x200B;设置为`Yes`。

1. 对于&#x200B;**[!UICONTROL Title]**，输入在结账期间标识COD付款方式的标题。

1. 将&#x200B;**[!UICONTROL New Order Status]**&#x200B;设置为`Pending`，直到确认收到付款。

   如果您愿意，可以使用此付款方式为新订单使用`Processing`或`Suspected Fraud`状态。

1. 将&#x200B;**[!UICONTROL Payment from Applicable Countries]**&#x200B;设置为以下项之一：

   - `All Allowed Countries` — 来自您商店配置中指定的所有[国家/地区](../getting-started/store-details.md#country-options)的客户都可以使用此付款方式。
   - `Specific Countries` — 选择此选项后，将显示&#x200B;_[!UICONTROL Payment from Specific Countries]_列表。 要选择多个国家/地区，请按住Ctrl键(PC)或Command键(Mac)并单击每个选项。

1. 输入用于接受货到付款订单交货的&#x200B;**[!UICONTROL Instructions]**。

1. 将&#x200B;**[!UICONTROL Minimum Order Total]**&#x200B;和&#x200B;**[!UICONTROL Maximum Order Total]**&#x200B;设置为符合货到付款条件的订单金额。

   >[!NOTE]
   >
   >订单符合合计在最小或最大订单合计之间或与最小或最大订单合计匹配的条件。

1. 对于&#x200B;**[!UICONTROL Sort Order]**，输入一个数字，该数字确定此项目在结帐期间显示的付款方法列表中的位置。

   此数字相对于其他支付方式。 （`0` =第一，`1` =第二，`2` =第三，依此类推。）

1. 完成后，单击&#x200B;**[!UICONTROL Save Config]**。

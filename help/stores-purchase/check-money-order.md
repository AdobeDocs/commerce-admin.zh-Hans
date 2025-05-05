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

Adobe Commerce和Magento Open Source允许您接受支票或汇票付款。 默认情况下，已为你的商店启用&#x200B;_支票/汇票_&#x200B;付款方式。 您只能接受来自特定国家/地区的支票和汇票，并且您可以对配置进行微调，使其具有最小和最大订单总限制。

**_若要通过支票或汇票配置付款：_**

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧面板中，展开&#x200B;**[!UICONTROL Sales]**&#x200B;并选择&#x200B;**[!UICONTROL Payment Methods]**。

1. 在&#x200B;_[!UICONTROL Other Payment Methods]_&#x200B;下，展开&#x200B;**[!UICONTROL Check / Money Order]**&#x200B;部分的![扩展选择器](../assets/icon-display-expand.png)。

   ![支票/汇票](../configuration-reference/sales/assets/payment-methods-check-money-order.png){width="600" zoomable="yes"}

   有关这些配置设置的详细说明，请参阅&#x200B;_配置参考指南_&#x200B;中的[支票/汇票](../configuration-reference/sales/payment-methods.md#check--money-order)。

   >[!NOTE]
   >
   >如有必要，请先清除&#x200B;**[!UICONTROL Use system value]**&#x200B;复选框以更改这些设置。

1. 若要接受支票或汇票付款，请将&#x200B;**[!UICONTROL Enabled]**&#x200B;设置为`Yes`。

1. 对于&#x200B;**[!UICONTROL Title]**，输入在结帐期间标识支票/汇票付款方式的标题。

1. 如果订单通常等待批准，请接受默认&#x200B;**[!UICONTROL New Order Status]**&#x200B;作为`Pending"`，直到它获得批准。

   如果您愿意，可以使用此付款方式为新订单使用`Processing`或`Suspected Fraud`状态。

1. 将&#x200B;**[!UICONTROL Payment from Applicable Countries]**&#x200B;设置为以下项之一：

   - `All Allowed Countries` — 来自您商店配置中指定的所有[国家/地区](../getting-started/store-details.md#country-options)的客户都可以使用此付款方式。
   - `Specific Countries` — 选择此选项后，将显示&#x200B;_[!UICONTROL Payment from Specific Countries]_&#x200B;列表。 要选择多个国家/地区，请按住Ctrl键(PC)或Command键(Mac)并单击每个选项。

1. 对于&#x200B;**[!UICONTROL Make Check Payable To]**，输入支票必须支付到的参与方的名称。

1. 对于&#x200B;**[!UICONTROL Send Check To]**，输入邮寄支票的街道地址或邮政信箱。

1. 将&#x200B;**[!UICONTROL Minimum Order Total]**&#x200B;和&#x200B;**[!UICONTROL Maximum Order Total]**&#x200B;设置为符合此付款方法条件的订单金额。

   >[!NOTE]
   >
   >如果合计在最小或最大合计值之间，或者与最小或最大合计值完全匹配，则订单合格。

1. 对于&#x200B;**[!UICONTROL Sort Order]**，输入一个数字，该数字确定此项目在结帐期间显示的付款方法列表中的位置。

   此数字相对于其他支付方式。 （`0` =第一，`1` =第二，`2` =第三，依此类推。）

1. 完成后，单击&#x200B;**[!UICONTROL Save Config]**。

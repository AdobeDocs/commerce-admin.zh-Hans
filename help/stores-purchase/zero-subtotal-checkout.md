---
title: 零小计签出
description: 了解如何设置零小计作为商店的离线付款方式。
exl-id: c14ce289-8292-41d9-a448-f493c784f35c
feature: Checkout, Configuration
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 0%

---

# 零小计签出

_零小计结帐_&#x200B;可用于应用折扣后征税的零小计订单。 例如，在以下情况下可以使用零小计签出：

- 折扣涵盖购买的全部价格，无需额外付运费。

- 客户向购物车添加[可下载](../catalog/product-create-downloadable.md)或[虚拟](../catalog/product-create-virtual.md)产品，价格等于零。

- [简单](../catalog/product-create-simple.md)产品的价格为零，并且可以使用[免费送货](shipping-free.md)方法。

- [优惠券代码](../merchandising-promotions/price-rules-cart-coupon.md)涵盖产品和配送的全部价格。

为了节省时间，可以将零小计订单设置为自动开票。

**_要配置零小计签出：_**

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧面板中，展开&#x200B;**[!UICONTROL Sales]**&#x200B;并选择&#x200B;**[!UICONTROL Payment Methods]**。

1. 在&#x200B;_[!UICONTROL Other Payment Methods]_下，展开&#x200B;**[!UICONTROL Zero Subtotal Checkout]**部分的![扩展选择器](../assets/icon-display-expand.png)。

   ![零小计签出](../configuration-reference/sales/assets/payment-methods-zero-subtotal-checkout.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >如有必要，请先清除&#x200B;**[!UICONTROL Use system value]**&#x200B;复选框以更改这些设置。

1. 要激活零小计签出，请将&#x200B;**[!UICONTROL Enabled]**&#x200B;设置为`Yes`。

1. 对于&#x200B;**[!UICONTROL Title]**，输入在结账期间标识Zero Subtotal方法的标题。

1. 如果订单通常等待批准，请接受默认&#x200B;**[!UICONTROL New Order Status]**&#x200B;作为`Pending"`，直到订单获得批准为止。

   如果您愿意，可以使用此付款方式为新订单使用`Processing`或`Suspected Fraud`状态。

1. 如果要自动为余额为零的所有项目开票，请将&#x200B;**[!UICONTROL Automatically Invoice All Items]**&#x200B;设置为`Yes`。

   仅当&#x200B;**[!UICONTROL New Order Status]**&#x200B;选项设置为`Processing`时，此选项才可用。

   >[!NOTE]
   >
   >如果&#x200B;_[!UICONTROL New Order Status]_设置为`Processing`且_[!UICONTROL Automatically Invoice All Items]_&#x200B;设置为`No`，则还必须为[订单状态](order-status.md#custom-order-status)页面上的&#x200B;**[!UICONTROL Order State]** = `Pending`和&#x200B;**[!UICONTROL Default Status]** = `No`映射分配&#x200B;**[!UICONTROL Order Status]** = `Processing`。

1. 将&#x200B;**[!UICONTROL Payment from Applicable Countries]**&#x200B;设置为以下项之一：

   - `All Allowed Countries` — 来自您商店配置中指定的所有[国家/地区](../getting-started/store-details.md#country-options)的客户都可以使用此付款方式。
   - `Specific Countries` — 选择此选项后，将显示&#x200B;_[!UICONTROL Payment from Specific Countries]_列表。 要选择多个国家/地区，请按住Ctrl键(PC)或Command键(Mac)并单击每个选项。

1. 对于&#x200B;**[!UICONTROL Sort Order]**，输入一个数字，该数字确定此项目在结帐期间显示的付款方法列表中的位置。

   此数字相对于其他支付方式。 （`0` =第一，`1` =第二，`2` =第三，依此类推。）

1. 完成后，单击&#x200B;**[!UICONTROL Save Config]**。

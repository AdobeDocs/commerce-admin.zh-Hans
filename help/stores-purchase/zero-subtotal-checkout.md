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

_零小计签出_ 可用于应用折扣后征税的零小计订单。 例如，在以下情况下可以使用零小计签出：

- 折扣涵盖购买的全部价格，无需额外付运费。

- 客户添加 [可下载](../catalog/product-create-downloadable.md) 或 [虚拟](../catalog/product-create-virtual.md) 产品到购物车，价格等于零。

- 的价格 [简单](../catalog/product-create-simple.md) 乘积为零，并且 [免费送货](shipping-free.md) 方法可用。

- A [优惠券代码](../merchandising-promotions/price-rules-cart-coupon.md) 涵盖产品和运输的全部价格。

为了节省时间，可以将零小计订单设置为自动开票。

**_要配置零小计签出，请执行以下操作：_**

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中，展开 **[!UICONTROL Sales]** 并选择 **[!UICONTROL Payment Methods]**.

1. 下 _[!UICONTROL Other Payment Methods]_，展开 ![扩展选择器](../assets/icon-display-expand.png) 该&#x200B;**[!UICONTROL Zero Subtotal Checkout]**部分。

   ![零小计签出](../configuration-reference/sales/assets/payment-methods-zero-subtotal-checkout.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >如有必要，请先清除 **[!UICONTROL Use system value]** 复选框以更改这些设置。

1. 要激活零小计签出，请设置 **[!UICONTROL Enabled]** 到 `Yes`.

1. 对象 **[!UICONTROL Title]**，输入在结账期间标识零小计方法的标题。

1. 如果订单通常等待批准，则接受默认值 **[!UICONTROL New Order Status]** 作为 `Pending"` 直到订单获得批准。

   如果您愿意，可以使用 `Processing` 或 `Suspected Fraud` 使用此付款方法的新订单的状态。

1. 设置 **[!UICONTROL Automatically Invoice All Items]** 到 `Yes` 如果您要自动为余额为零的所有物料开票。

   此选项仅在 **[!UICONTROL New Order Status]** 选项设置为 `Processing`.

   >[!NOTE]
   >
   >如果 _[!UICONTROL New Order Status]_设置为 `Processing` 和_[!UICONTROL Automatically Invoice All Items]_ 设置为 `No`，您还必须分配 **[!UICONTROL Order Status]** = `Processing` 对于 **[!UICONTROL Order State]** = `Pending` 和 **[!UICONTROL Default Status]** = `No` 映射 [订单状态](order-status.md#custom-order-status) 页面。

1. 设置 **[!UICONTROL Payment from Applicable Countries]** 更改为以下任一项：

   - `All Allowed Countries`  — 来自所有客户的客户 [国家/地区](../getting-started/store-details.md#country-options) 在商店配置中指定的可使用此付款方式。
   - `Specific Countries`  — 选择此选项后， _[!UICONTROL Payment from Specific Countries]_列表出现。 要选择多个国家/地区，请按住Ctrl键(PC)或Command键(Mac)并单击每个选项。

1. 对象 **[!UICONTROL Sort Order]**，请输入一个数字，以确定此项目在结账时显示的付款方式列表中的位置。

   此数字相对于其他支付方式。 (`0` =第一个， `1` =秒， `2` =第三，依此类推。)

1. 完成后，单击 **[!UICONTROL Save Config]**.

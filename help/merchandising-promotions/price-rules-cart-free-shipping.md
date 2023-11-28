---
title: 购物车价格规则示例 — 免运费促销
description: 查看使用购物车价格规则提供免运费的示例。
exl-id: f7652254-ff01-44ff-a207-2d7cf2017517
feature: Merchandising, Price Rules, Shopping Cart, Shipping/Delivery
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '399'
ht-degree: 0%

---

# 购物车价格规则示例 — 免运费促销

免费送货可以作为促销活动提供，无论是否有 [优惠券](price-rules-cart-coupon.md). 免费送货优惠券或优惠券也可以应用于客户提货订单，这样就可以对订单开票并送货以完成 [工作流](../stores-purchase/order-processing.md#order-workflow-and-processing).

某些装运承运人配置使您能够根据最低订单提供免运费。 要扩展此基本功能，您可以使用购物车价格规则根据多个产品属性、购物车内容和客户组创建复杂的条件。

## 步骤1. 启用免费送货

1. 启用 [免费送货](../stores-purchase/shipping-free.md) 在您的商店配置中。

1. 完成任何的免费送货设置 [运营商服务](../stores-purchase/carriers.md) 用于免费送货。

## 步骤2. 创建购物车价格规则

在 _管理员_ 侧栏，转到 **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Cart Price Rules]**.

请按照以下步骤设置您要提供的免运费促销类型。

### 示例1：任何订单的免运费

1. 完成 **[!UICONTROL Rule Information]** 如下所示：

   - 输入 **[!UICONTROL Rule Name]** 以供内部参考。
   - 输入摘要 **[!UICONTROL Description]** 以描述规则。
   - 设置 **[!UICONTROL Active]** 到 `Yes`.
   - 在 **[!UICONTROL Websites]** 框中，选择要提供免运费优惠券的每个站点。
   - 选择 **[!UICONTROL Customer Groups]** 规则适用的对象。
   - 设置 **[!UICONTROL Coupon]** 更改为以下任一项：
      - 要提供免运费促销活动而不提供优惠券，请接受默认值(`No Coupon`)设置。
      - 要将优惠券与价格规则结合使用，请选择 `Specific Coupon`. 如有必要，请完成说明以设置 [优惠券](price-rules-cart-coupon.md).

1. 向下滚动并展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Actions]** 部分并执行以下操作：

   - 设置 **[!UICONTROL Apply]** 到 `Percent of product price discount`.
   - 设置 **[!UICONTROL Apply to Shipping Amount]** 到 `Yes`.
   - 设置 **[!UICONTROL Free Shipping]** 到 `For matching items only`.

   ![购物车价格规则 — 免运费操作](./assets/free-shipping-actions.png){width="600" zoomable="yes"}

### 示例2：金额超过$的订单的免费发运

1. 完成 **[!UICONTROL General Information]** 如上一个示例中所述的设置。

1. 向下滚动并展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Conditions]** 部分。

1. 单击 _添加_ (![“添加”图标](../assets/icon-add-green-circle.png))以插入条件并执行以下操作：

   - 在下面的列表中 **[!UICONTROL Cart Attribute]**，选择 `Subtotal`.
   - 单击 **[!UICONTROL is]** 并选择 `equals or greater than`.
   - 单击 **...** 并输入小计的阈值，例如 `100`，以完成条件。

   ![购物车价格规则 — 条件](./assets/free-shipping-condition1.png){width="600" zoomable="yes"}

1. 如有必要，请展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Actions]** 部分并执行以下操作：

   - 设置 **[!UICONTROL Apply]** 到 `Percent of product price discount`.
   - 设置 **[!UICONTROL Apply to Shipping Amount]** 到 `Yes`.
   - 设置 **[!UICONTROL Free Shipping]** 到 `For matching items only`.

## 步骤3. 完成标签

完成 [步骤4](price-rules-cart.md) ，以输入在结帐期间显示的任何标签。

## 步骤4. 保存并测试规则

{{new-price-rule}}

1. 规则完成后，单击 **[!UICONTROL Save Rule]**.

1. 测试规则以确保其正常工作。

---
title: 购物车价格规则示例 — 具有最小购买量的折扣
description: 查看使用购物车价格规则提供最低购买折扣的示例。
exl-id: dc06cd12-d23b-4836-9ad2-93ca60dac927
feature: Merchandising, Price Rules, Shopping Cart
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '346'
ht-degree: 0%

---

# 购物车价格规则示例 — 具有最小购买量的折扣

可使用购物车价格规则根据最低购买提供百分比折扣。 在以下示例中，25%的折扣适用于特定类别中超过$200.00的所有购买。 折扣格式如下：

所有Y（类别）在Z美元以上有X%优惠

## 步骤1. 创建购物车规则

按照基本[说明](price-rules-cart.md)创建购物车规则。

## 步骤2. 定义条件

1. 向下滚动并展开&#x200B;**[!UICONTROL Conditions]**&#x200B;部分的![扩展选择器](../assets/icon-display-expand.png)。

1. 单击&#x200B;_添加_ （![添加图标](../assets/icon-add-green-circle.png)）并选择&#x200B;**[!UICONTROL Product Attribute Combination]**。

   ![购物车价格规则条件 — 产品属性组合](./assets/condition1.png){width="500" zoomable="yes"}

1. 单击下一行开头的&#x200B;_添加_ （![添加图标](../assets/icon-add-green-circle.png)），然后在&#x200B;**[!UICONTROL Product Attribute]**&#x200B;下的列表中选择&#x200B;**[!UICONTROL Category]**。

   - 单击(**...**) _更多_&#x200B;链接以显示其他选项。

     ![购物车价格规则条件 — 类别选项](./assets/condition3.png){width="600" zoomable="yes"}

   - 单击&#x200B;_选择器_ （![列表图标](../assets/icon-list-chooser.png)）图标查看可用的类别。 在类别树中，选中要包含的每个类别的复选框。 单击复选图标接受类别选择。

     ![购物车价格规则条件 — 类别](./assets/condition4.png){width="600" zoomable="yes"}

1. 单击下一行开头的&#x200B;_添加_ （![添加图标](../assets/icon-add-green-circle.png)）并执行以下操作：

   - 在&#x200B;**[!UICONTROL Cart Item Attribute]**&#x200B;下的列表中，选择&#x200B;**[!UICONTROL Price in cart]**。

     ![购物车价格规则条件 — 购物车项目属性](./assets/condition5.png){width="500"}

   - 单击&#x200B;**是**&#x200B;并选择`equals or greater than`。

   - 单击&#x200B;**...**&#x200B;并输入购物车中的价格必须符合此条件的金额。 例如，输入`30`。

     ![购物车价格规则条件 — 购物车中的价格](./assets/condition6.png){width="500"}

1. 单击&#x200B;**[!UICONTROL Save and Continue Edit]**。

## 步骤3. 定义操作

1. 展开&#x200B;**[!UICONTROL Actions]**&#x200B;部分中的![扩展选择器](../assets/icon-display-expand.png)并执行以下操作：

   ![购物车价格规则操作](./assets/minimum-discount-actions.png){width="600" zoomable="yes"}

   - 将&#x200B;**[!UICONTROL Apply]**&#x200B;设置为`Percent of product price discount`。

   - 输入&#x200B;**[!UICONTROL Discount Amount]**。 例如，输入`10`获得10%的折扣。

   - 要阻止将其他促销活动应用于购买，请将&#x200B;**[!UICONTROL Discard subsequent rules]**&#x200B;设置为`Yes`。

1. 单击&#x200B;**[!UICONTROL Save and Continue Edit]**&#x200B;并根据需要完成规则。

## 步骤4. 完成标签

完成购物车价格规则说明的[第4](price-rules-cart.md)步，以输入结帐期间出现的任何标签。

## 步骤5：保存并测试规则

{{new-price-rule}}

1. 规则完成后，单击&#x200B;**[!UICONTROL Save Rule]**。

1. 测试规则以确保其正常工作。

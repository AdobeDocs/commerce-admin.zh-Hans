---
title: 价格规则中的动态块
description: 将动态块与促销价格规则关联。
exl-id: e1564df2-1c06-4d11-a32d-6f5c0be974e3
feature: Page Content, Price Rules
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 0%

---

# 价格规则中的动态块

{{ee-feature}}

任何 [动态块](dynamic-blocks.md) 创建的任何其他活动均可与促销相关联。 要建立关联，必须先创建动态块和 [目录价格规则](../merchandising-promotions/price-rules-catalog.md) 或 [购物车价格规则](../merchandising-promotions/price-rules-cart.md). 关联可以在处理价格规则时或在处理动态块时建立。

>[!IMPORTANT]
>
>创建此关联后，将显示动态块 **仅限** 规则触发时。 如果促销活动定位到区段A，则该块将显示到区段A。如果促销活动未处于活动状态，则不会显示块。

## 将动态块与价格规则关联

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_并选择下列选项之一：

   - **[!UICONTROL Catalog Price Rules]**
   - **[!UICONTROL Cart Price Rules]**

1. 在网格中，查找要与动态块关联的规则，并在编辑模式下打开。

1. 向下滚动并展开 ![扩展选择器](../assets/icon-display-expand.png) **[!UICONTROL Related Dynamic Blocks]**.

1. 在第一列中，将过滤器设置为 `Any` 并单击 **[!UICONTROL Reset Filter]**.

   网格现在会列出所有可用的动态块。

1. 选中要与规则关联的每个动态块的复选框。

   ![添加所选的动态块](./assets/price-rule-cart-related-dynamic-blocks-any.png){width="600" zoomable="yes"}

1. 完成后，单击 **[!UICONTROL Save]**.

## 将价格规则与动态块关联

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Dynamic Blocks]**.

1. 在网格中查找动态块，并在编辑模式下打开。

1. 向下滚动并展开 **[!UICONTROL Related Promotions]**.

   当前关联的所有价格规则都会显示在网格中。

1. 添加新的关联规则或删除当前关联。

   - 要关联购物车促销，请单击 **[!UICONTROL Add Cart Price Rules]**.

   - 要关联与产品相关的促销，请单击 **[!UICONTROL Add Catalog Price Rules]**.

1. 在网格中，选中要与动态块关联的每个规则的复选框。

1. 单击 **[!UICONTROL Add Selected]**.

   ![将所选价格规则添加到动态块](./assets/pb-dynamic-block-add-related-cart-price-rules.png){width="600" zoomable="yes"}

1. 完成后，单击 **[!UICONTROL Save]**.

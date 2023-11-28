---
title: 按产品分配库存数量
description: 了解如何更新产品的库存数量并跟踪现有可用库存量。
exl-id: 935385bb-6657-4d49-980e-96a3d0d3a187
feature: Inventory, Products
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 0%

---

# 按产品分配数量

添加后 [源](sources-assign-per-product.md)，更新产品的库存数量。 这些值跟踪现有可用库存量。

要在发运中隐藏来源的库存而不删除来源，请设置 _[!UICONTROL Source Item Status]_到 `Out of Stock`. SSA和发运选项只能访问下列来源 `In Stock` 具有可用库存数量。

所有更新的数量和来源都会显示在产品网格中。

## 更新数量

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. 在编辑模式下查找并打开产品。

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Sources]** 部分。

1. 设置 **[!UICONTROL Source Item Status]** 到 `In Stock`.

1. 要更新现有库存量，请输入 **[!UICONTROL Qty]**.

1. 要设置库存数量通知，请执行以下操作之一：

   - 自定义通知数量 — 取消选择 **[!UICONTROL Use Default]** 复选框，并输入金额 **[!UICONTROL Notify Qty]**.
   - 默认通知数量 — 选择 **[!UICONTROL Use Default]** 复选框。 [!DNL Commerce] 检查并使用中的设置 _[!UICONTROL Advanced Inventory]_或全局存储配置。

   ![更新每个来源的产品数量](assets/inventory-product-quantity-edit.png){width="350" zoomable="yes"}

1. 执行以下操作之一进行保存：

   - 单击 **[!UICONTROL Save]**.

   - 在 **[!UICONTROL Save]** (![菜单箭头](../assets/icon-menu-down-arrow-red.png))菜单，选择 **[!UICONTROL Save & Close]**.


“产品网格”将更新为所有来源和相关数量的列表。 对于已分配源超过五个的产品，将鼠标悬停在 _[!UICONTROL Quantity per Source]_列以查看完整列表。

![每个来源的产品数量](assets/inventory-product-quantity.png){width="600" zoomable="yes"}

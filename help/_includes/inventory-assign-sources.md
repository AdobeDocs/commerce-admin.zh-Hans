---
title: 库存 — 分配来源和数量
description: 有关创建目录产品时分配来源和数量的“已重用”部分。
source-git-commit: f36925217230e558043078fdc274f5e69c096c1e
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 0%

---

# 库存 — 分配来源和数量

对于多源商家，使用 [[!DNL Inventory Management]](../inventory-management/introduction.md)，向下滚动到 **源** 并分配来源和数量：

1. 要添加源，请单击 **[!UICONTROL Assign Sources]**.

1. 浏览或搜索源，然后选中要为产品添加的源旁边的复选框。

   ![将源分配给产品](../catalog/assets/inventory-product-assign-sources.png){width="600" zoomable="yes"}

1. 单击 **[!UICONTROL Done]** 以添加源。

1. 要管理源的数量和状态，请单击 **[!UICONTROL Advanced Inventory]** 并设置 **[!UICONTROL Manage Stock]** 到 `Yes`.

1. 设置 **[!UICONTROL Source Item Status]** 到 `In Stock`.

1. 输入金额更新 **[!UICONTROL Qty]** 用于库存量。

1. 要设置库存数量通知，请执行以下操作之一：

   - _自定义通知数量_  — 清除 **[!UICONTROL Notify Quantity Use Default]** 复选框，并输入金额 **[!UICONTROL Notify Quantity]**.

   - _默认通知数量_  — 选择 **[!UICONTROL Notify Quantity Use Default]** 复选框。 Commerce检查并使用中的设置 [!UICONTROL Advanced Inventory] 或全局存储配置。

   ![更新每个来源的产品数量](../catalog/assets/inventory-product-quantity.png){width="600" zoomable="yes"}

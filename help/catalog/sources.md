---
title: 产品设置 —  [!UICONTROL Sources]
description: 对于产品， [!UICONTROL Sources] 设置提供对 [!DNL Inventory Management] 分发产品的来源。
exl-id: 986f6031-0edc-4105-aa02-1c22364b3e7c
feature: Catalog Management, Products, Inventory
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 1%

---

# 产品设置 —  [!UICONTROL Sources]

此 _[!UICONTROL Sources]_产品设置的部分列出了分发产品的来源。 它用于分配和取消分配来源，以及管理产品的数量和可用性。 仅当为您的存储定义了多个源时，才会显示此部分。 有关源的详细信息，请参阅 [管理源](../inventory-management/sources-manage.md).

## 为产品分配源

1. 单击 **[!UICONTROL Assign Source]**.

1. 选中所需源的复选框。

1. 单击 **[!UICONTROL Done]**.

1. 选择 **[!UICONTROL Source Item Status]** 并输入 **[!UICONTROL Qty]** 和 **[!UICONTROL Notify Qty]** 值。

1. 单击 **[!UICONTROL Save]** 以保存更改。

![源视图](./assets/catalog-sources-list.png){width="600" zoomable="yes"}

## 字段引用

| 字段 | 描述 |
|--- |--- |
| [!UICONTROL Name] | 源的唯一名称。 |
| [!UICONTROL Source Status] | 确定在目录中是启用还是禁用该产品。 |
| [!UICONTROL Source Item Status] | 确定产品的当前可用性。 选项：<br />**[!UICONTROL In Stock]**— 使产品可供购买。<br />**[!UICONTROL Out of Stock]**  — 除非激活延交订单，否则将阻止产品可供购买，并从目录中删除列表。 |
| [!UICONTROL Qty] | 每个来源的现有库存量。 |
| [!UICONTROL Notify Qty] | 的金额 _通知数量_ 对于此特定源，如果 `Notify Quantity Use Default` 未选中。 |
| [!UICONTROL Notify Qty Use Default] | 指示使用默认设置 _通知数量_ 在产品的“高级清单”或商店配置的全局设置中。 有关产品的高级清单设置的详细信息，请参阅 [配置高级产品选项](../inventory-management/product-options.md). |
| [!UICONTROL Actions] | 对于已分配的源，单击 **[!UICONTROL Unassign]** 使源不可用于产品。 对于未分配的源，单击 **[!UICONTROL Assign Sources]** 使源对产品可用。 有关详情 [!UICONTROL Assign Sources] 选项，请参见 [按产品分配源](../inventory-management/sources-assign-per-product.md). |

{style="table-layout:auto"}

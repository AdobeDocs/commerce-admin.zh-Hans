---
title: “配置 [!DNL Inventory Management] 产品选项”
description: 了解如何配置 [!DNL Inventory Management] 产品配置选项。
exl-id: b5cff7d2-5197-4362-9503-b07c80793ac7
feature: Inventory, Products
source-git-commit: ccd93a54b6fa23a7a54fb423f8232c72cd8fe027
workflow-type: tm+mt
source-wordcount: '859'
ht-degree: 0%

---

# 配置 [!DNL Inventory Management] 产品选项

这些配置仅适用于已编辑的产品，并覆盖全局网站级别的所有配置。 在编辑产品时，通过 _[!UICONTROL Sources]_部分和_[!UICONTROL Advanced Inventory]_ 页面。

- 按源配置产品选项
- 配置高级清单的产品选项

## 按源显示的产品选项

根据以下条件配置数量和其他设置 [已添加源](sources-add.md) 以购买产品。

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. 在编辑模式下打开产品。

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Sources]** 部分，并为每个源配置产品设置：

   - 输入 **[!UICONTROL Qty]** （数量）金额。

   - 设置 **[!UICONTROL Source Item Status]** 作为 `In Stock` 或 `Out of Stock`.

   - 要修改“通知每个来源的数量低于”，请清除或选择 **[!UICONTROL Notify Quantity Use Default]** 复选框。

     如果清除，请输入触发物料缺货通知的库存水平金额。 输入的金额将从库存层的项目可销售数量中扣除。

     `Select to use Default` - [!DNL Commerce] 检查产品的高级清单选项以了解配置设置。
     `Clear to Modify`  — 为“通知数量”输入值，覆盖“高级库存”和“商店”配置设置。

   ![产品的“源”部分](assets/inventory-product-quantity-edit.png){width="350" zoomable="yes"}

1. 完成后，单击 **[!UICONTROL Done]**，则 **[!UICONTROL Save]**.

### 字段描述

| 字段 | 范围 | 描述 |
|--|--|--|
| [!UICONTROL Source Code] | 全局 | 的唯一代码 [源](sources-manage.md). |
| [!UICONTROL Name] | 全局 | 源的唯一名称。 |
| [!UICONTROL Status] | 全局 | 在目录中启用或禁用产品。 |
| [!UICONTROL Source Item Status] | 全局 | 确定产品的当前可用性。 选项：<br />`In Stock`  — 使产品可供购买。<br />`Out of Stock`  — 除非激活延交订单，否则将阻止产品可供购买，并从目录中删除列表。 |
| [!UICONTROL Qty] | 全局 | 每个来源或地点的现有库存量。 |
| [!UICONTROL Notify Quantity] | 全局 | 的金额 _[!UICONTROL Notify for Quantity Below]_对于此特定源，如果_[!UICONTROL Notify Quantity Use Default]_ 未选中。 |
| [!UICONTROL Notify Quantity Use Default] | 全局 | 指示使用默认设置 _[!UICONTROL Notify for Quantity Below]_在产品中_[!UICONTROL Advanced Inventory]_ 或存储配置中的全局设置。 |

## 高级产品选项

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. 在编辑模式下打开产品。

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Sources]** 部分并单击 **[!UICONTROL Advanced Inventory]**.

1. 要启用 [库存控制](enable.md) 对于目录，设置 **[!UICONTROL Manage Stock]** 到 `Yes`.

   >[!NOTE]
   >
   >[!UICONTROL Manage Stock] 子产品中的设置会覆盖可配置的产品。

   ![产品的高级库存](assets/inventory-backorders-product-settings.png){width="600" zoomable="yes"}

1. 输入金额 **[!UICONTROL Out-of-Stock Threshold]**：

   | 值 | 描述 |
   | ----- | ----- |
   | 正数 | 替换为 _[!UICONTROL Backorders]_禁用，请输入正值。 |
   | 零 | 替换为 _[!UICONTROL Backorders]_已启用，正在输入 `0` 允许无限延交。 |
   | 负金额 | 替换为 _[!UICONTROL Backorders]_已启用，建议输入负值。 该金额将添加到可销售数量。 例如，输入 `-50` 允许订单数量不超过此金额。 |

1. 输入 **[!UICONTROL Minimum Qty Allowed in Shopping Cart]**.

1. 输入 **[!UICONTROL Maximum Qty Allowed in Shopping Cart]**.

1. 设置 **[!UICONTROL Qty uses Decimals]** 到 `Yes` 客户在输入订购数量时可以使用小数值而不是整数。

1. 设置 **[!UICONTROL Allow Multiple Boxes for Shipping]** 到 `Yes` 如果产品可以单独销售（多个盒子）。 在以下情况下，此选项可见： **[!UICONTROL Qty Uses Decimals]** 设置为 `Yes` 仅限。

1. 设置 **[!UICONTROL Backorders]** 更改为以下任一项：

   | 选项 | 描述 |
   | ----- | ----- |
   | `No Backorders` | 产品缺货时不接受延交订单。 |
   | `Allow Qty Below 0` | 要在数量低于零时接受延交订单，请执行以下操作： |
   | `Allow Qty Below 0 and Notify Customer` | 在数量低于零时接受延交订单，并通知客户仍然可以下订单。 |

   有关更多信息，请参阅 [配置延交订单](backorders.md).

1. 要激活产品的数量增量，请设置 **[!UICONTROL Enable Qty Increments]** 到 `Yes` 并输入为满足此要求而必须购买的项目数 **[!UICONTROL Qty Increments]** 字段。

   例如，以6为增量销售的项目可以以6、12、18等数量购买。

1. 完成后，单击 **[!UICONTROL Done]** 然后 **[!UICONTROL Save]**.

### 字段描述

| 字段 | 范围 | 描述 |
|--|--|--|
| [!UICONTROL Manage Stock] | 全局 | 确定是否使用库存控制管理目录中的此产品。 设置为启用或禁用全部 [!DNL Inventory Management] 功能。 当您完成退货或贷项通知单时，产品数量会自动返回至受影响的来源数量。 如果使用第三方ERP系统，则可能需要禁用。 |
| [!UICONTROL Out-of-Stock Threshold] | 全局 | 确定将产品视为缺货的库存水平。 选项：<br />正值 — 禁用延交订单后，请输入正金额。<br />零(0) — 启用“延交订单”后，输入零将允许无限延交订单。<br />负值 — 在启用延交订单的情况下，建议输入负金额。 该金额将添加到可销售数量。 例如，输入 `-50` 允许订单数量不超过此金额。 |
| [!UICONTROL Minimum Qty Allowed in Shopping Cart] | 全局 | 确定单个订单可购买产品的最小数量。 |
| [!UICONTROL Maximum Qty Allowed in Shopping Cart] | 全局 | 确定单笔订单可购买产品的最大数量。 |
| [!UICONTROL Qty Uses Decimals] | 全局 | 确定在输入订购数量时，客户是否可以使用小数值而不是整数。 选项：<br />`Yes`  — 允许以小数形式输入值，而不是整数。 小数点适合按重量、体积或长度销售的产品。<br />`No`  — 要求以整数输入数量值。 |
| [!UICONTROL Allow Multiple Boxes for Shipping] | 全局 | 确定产品部件是否可以单独发运。 在以下情况下，此选项可见： **[!UICONTROL Qty Uses Decimals]** = `Yes`. |
| [!UICONTROL Backorders] | 全局 | 确定如何管理延交订单。 延交订单不会更改订单的处理状态。 无论产品是否有库存，在下单后仍会立即授权或获取资金。 产品在可用时即发运。 启用后，建议您为缺货阈值输入负值。 选项：<br/>`No Backorders`  — 当产品缺货时，不接受延交订单。<br />`Allow Qty Below 0`  — 在数量低于零时接受延交订单。<br />`Allow Qty Below 0 and Notify Customer`  — 在数量低于零时接受延交订单，但通知客户仍然可以下订单。 |
| [!UICONTROL Enable Qty Increments] | 全局 | 确定产品是否可以按数量递增销售。 |

>[!NOTE]
>
>简单产品配置会覆盖特定产品的可配置产品配置。

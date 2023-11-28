---
title: 固定产品税(FPT)
description: 了解如何设置必须添加到特定产品类型的固定产品税(FPT)。
exl-id: f1b475cb-a6fe-4b51-a0c3-7d0a202bd332
feature: Checkout, Invoices, Taxes, Products
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '867'
ht-degree: 0%

---

# 固定产品税(FPT)

某些税务管辖区具有必须对某些类型产品添加的固定税。 您可以设置 _固定产品税_ (FPT)适用于您商店的纳税计算。 在某些国家，可利用废旧电气和电子设备税来征税。 此税也称为 _生态税_ 或 _eco税_，并收集某些类型的电子产品以抵消回收成本。 它是固定金额，而不是产品价格的百分比。

固定产品税基于产品在物料层应用。 在某些司法管辖区，这种税收需要额外计算%。 无论是否纳税，您的税务管辖区可能还有关于向客户显示产品价格的规则。 确保您了解规则并相应地设置FPT显示选项。

在电子邮件中引用FPT价格时请务必谨慎，因为价格的差异可能会影响客户对其订单的信心。 例如，如果您显示“订单复查”价格而不显示FPT，则购买具有相关FPT的项目的客户将看到包含FPT税额但不包含明细细分的总额。 两地价差可能使一些顾客放弃他们的购物车，因为总额与预期不同。

## FPT显示价格

| FPT | 显示设置和计算 | |
|--- |--- |---|
| 未纳税 | **[!UICONTROL Excluding FPT]** | FPT在购物车中显示为一个单独的行，该值用于相应的计税中。 |
| | **[!UICONTROL Including FPT]** | FPT将添加到项目的基本价格；但不包含在基于税则的计算中。 |
| | **[!UICONTROL Excluding FPT, FPT Description, Final Price]** | 价格显示时没有FPT金额或说明。 基于税则的计算中不包括FPT。 |
| 已纳税 | **[!UICONTROL Excluding FPT]** | FPT在购物车中显示为一个单独的行，该值用于相应的计税中。 |
| | **[!UICONTROL Including FPT]** | FPT包含在项目的价格中，并且不需要更改税费计算。 |
| | **[!UICONTROL Excluding FPT, FPT Description, Final Price]** | 显示的价格不包含FPT金额或说明。 但是，FPT包含在基于税则的计算中。 |

{style="table-layout:auto"}

## 配置FPT

固定产品税(FPT) [输入类型](../catalog/attributes-input-types.md) 创建用于管理每个区域的税的字段部分。

以下说明说明说明如何使用“eco tax”为例，为您的商店设置固定产品税。 在设置税范围以及税适用的国家（地区）和省（州）之后，根据您选择的选项，输入字段可以根据本地要求进行更改。 要了解更多信息，请参阅 [创建产品属性](../catalog/attribute-product-create.md).

### 步骤1：启用固定产品税

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中，展开 **[!UICONTROL Sales]** 并选择 **[!UICONTROL Tax]**.

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Fixed Product Taxes]** 部分。

1. 设置 **[!UICONTROL Enable FPT]** 到 `Yes`.

1. 要确定如何在商店价格中使用固定产品税，请选择以下每个价格显示位置的FPT设置：

   - **[!UICONTROL Display Prices in Product Lists]**
   - **[!UICONTROL Display Prices on Product View Page]**
   - **[!UICONTROL Display Prices in Sales Modules]**
   - **[!UICONTROL Display Prices in Emails]**

   选项（每个选项相同）：

   - `Including FPT Only`
   - `Including FPT and FPT description`
   - `Excluding FPT. Including FPT description and final price`
   - `Excluding FPT`

1. 设置 **[!UICONTROL Apply Tax to FPT]** 根据需要。

1. 设置 **[!UICONTROL Include FPT in Subtotal]** 根据需要。

   ![固定产品税](../configuration-reference/sales/assets/tax-fixed-product-taxes.png){width="600" zoomable="yes"}

   有关每个配置设置的详细说明，请参阅 [固定产品税](../configuration-reference/sales/tax.md#fixed-product-taxes) 在 _配置参考指南_.

1. 完成后，单击 **[!UICONTROL Save Config]**.

### 步骤2：创建FPT属性

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. 在右上角，单击 **[!UICONTROL Add New Attribute]** 并执行以下操作：

   - 对象 **[!UICONTROL Default Label]**，输入用于标识属性的标签。

   - 设置 **[!UICONTROL Catalog Input for Store Owner]** 到 `Fixed Product Tax`.

   ![属性属性](./assets/tax-fpt-attribute-properties.png){width="600" zoomable="yes"}

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Advanced Attribute Properties]** 并设置属性选项：

   - **[!UICONTROL Attribute Code]**  — 以小写形式输入唯一标识符，且不含空格或特殊字符。 最大长度为30个字符。 您可以将“默认标签”字段中的文本保留为空。

   - **[!UICONTROL Add to Column Options]**  — 如果您希望FPT字段显示在 [产品列表](../catalog/products-list.md)，设置为 `Yes`.

   - **[!UICONTROL Use in Filter Options]**  — 如果您希望能够 [筛选](../getting-started/admin-workspace.md) 网格中的产品基于FPT字段的值，设置为 `Yes`.

   ![高级属性属性](./assets/tax-fpt-advanced-attribute-properties.png){width="600" zoomable="yes"}

1. （可选）在左侧面板中，选择 **[!UICONTROL Manage Labels]** 并输入要使用的标签，而不是每个商店视图的默认标签。

   ![管理标签](./assets/attribute-new-manage-labels.png){width="600" zoomable="yes"}

1. 完成后，单击 **[!UICONTROL Save Attribute]**.

1. 出现提示时，刷新 [缓存](../systems/cache-management.md).

### 步骤3：将FPT属性添加到属性集

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Attribute Set]**.

1. 在列表中，单击属性集以在编辑模式下打开记录。

   ![属性集列表](./assets/attribute-sets-list.png){width="600" zoomable="yes"}

1. 将FPT属性从列表中 **[!UICONTROL Unassigned Attributes]** 在右侧 **[!UICONTROL Groups]** 列表放在中心列中。

   每个组文件夹对应于产品信息的一个部分。 当产品在编辑模式下打开时，您可以将属性放置到所需的任何位置。

   ![编辑属性集](./assets/tax-fpt-attribute-set-drag.png){width="600" zoomable="yes"}

1. 完成后，单击 **[!UICONTROL Save]**.

1. 对每个应包括固定产品税的属性集重复此步骤。

### 步骤4：将FPT应用于特定产品

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. 在编辑模式下打开需要固定产品税的产品。

1. 查找 **[!UICONTROL FPT]** 添加到属性集并单击的字段的部分 **[!UICONTROL Add Tax]**.

1. 指定产品的适用税：

   ![加拿大的固定产品税](./assets/tax-product-fpt-canada.png){width="600" zoomable="yes"}

   - 如果您的Commerce实例具有多个网站，请选择适当的 **[!UICONTROL Website]** 和基础货币。 在此示例中，字段默认设置为 `All Websites [USD]`.

   - 设置 **[!UICONTROL Country/State]** 到固定产品税适用的区域。

   - 对象 **[!UICONTROL Tax]**，输入小数形式的固定产品税。

1. 要添加更多固定产品税，请单击 **[!UICONTROL Add Tax]** 然后重复这个过程。

1. 完成后，单击 **[!UICONTROL Save]**.

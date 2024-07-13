---
title: 固定产品税(FPT)
description: 了解如何设置必须添加到特定产品类型的固定产品税(FPT)。
exl-id: f1b475cb-a6fe-4b51-a0c3-7d0a202bd332
feature: Checkout, Invoices, Taxes, Products
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '872'
ht-degree: 0%

---

# 固定产品税(FPT)

某些税务管辖区具有必须对某些类型产品添加的固定税。 您可以根据需要为商店的税务计算设置&#x200B;_固定产品税_ (FPT)。 在某些国家，可利用废旧电气和电子设备税来征税。 此税也称为&#x200B;_生态税_&#x200B;或&#x200B;_生态税_，征收于特定类型的电子产品，以抵消回收成本。 它是固定金额，而不是产品价格的百分比。

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

固定产品税(FPT) [输入类型](../catalog/attributes-input-types.md)创建用于管理每个区域税款的字段部分。

以下说明说明说明如何使用“eco tax”为例，为您的商店设置固定产品税。 在设置税范围以及税适用的国家（地区）和省（州）之后，根据您选择的选项，输入字段可以根据本地要求进行更改。 若要了解详细信息，请参阅[创建产品属性](../catalog/attribute-product-create.md)。

### 步骤1：启用固定产品税

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧面板中，展开&#x200B;**[!UICONTROL Sales]**&#x200B;并选择&#x200B;**[!UICONTROL Tax]**。

1. 展开&#x200B;**[!UICONTROL Fixed Product Taxes]**&#x200B;部分的![扩展选择器](../assets/icon-display-expand.png)。

1. 将&#x200B;**[!UICONTROL Enable FPT]**&#x200B;设置为`Yes`。

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

1. 根据需要设置&#x200B;**[!UICONTROL Apply Tax to FPT]**。

1. 根据需要设置&#x200B;**[!UICONTROL Include FPT in Subtotal]**。

   ![固定产品税](../configuration-reference/sales/assets/tax-fixed-product-taxes.png){width="600" zoomable="yes"}

   有关每个配置设置的详细说明，请参阅&#x200B;_配置参考指南_&#x200B;中的[固定产品税](../configuration-reference/sales/tax.md#fixed-product-taxes)。

1. 完成后，单击&#x200B;**[!UICONTROL Save Config]**。

### 步骤2：创建FPT属性

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**。

1. 单击右上角的&#x200B;**[!UICONTROL Add New Attribute]**&#x200B;并执行以下操作：

   - 对于&#x200B;**[!UICONTROL Default Label]**，请输入标识该属性的标签。

   - 将&#x200B;**[!UICONTROL Catalog Input for Store Owner]**&#x200B;设置为`Fixed Product Tax`。

   ![属性属性](./assets/tax-fpt-attribute-properties.png){width="600" zoomable="yes"}

1. 展开![扩展选择器](../assets/icon-display-expand.png) **[!UICONTROL Advanced Attribute Properties]**&#x200B;部分并设置属性选项：

   - **[!UICONTROL Attribute Code]** — 以小写形式输入唯一标识符，不带空格或特殊字符。 最大长度为30个字符。 您可以将“默认标签”字段中的文本保留为空。

   - **[!UICONTROL Add to Column Options]** — 如果您希望FPT字段出现在[产品列表](../catalog/products-list.md)中，请设置为`Yes`。

   - **[!UICONTROL Use in Filter Options]** — 如果要能够根据FPT字段的值[筛选](../getting-started/admin-workspace.md)网格中的产品，请设置为`Yes`。

   ![高级属性属性](./assets/tax-fpt-advanced-attribute-properties.png){width="600" zoomable="yes"}

1. （可选）在左侧面板中，选择&#x200B;**[!UICONTROL Manage Labels]**&#x200B;并输入要使用的标签，而不是每个商店视图的默认标签。

   ![管理标签](./assets/attribute-new-manage-labels.png){width="600" zoomable="yes"}

1. 完成后，单击&#x200B;**[!UICONTROL Save Attribute]**。

1. 出现提示时，刷新[缓存](../systems/cache-management.md)。

### 步骤3：将FPT属性添加到属性集

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Attribute Set]**。

1. 在列表中，单击属性集以在编辑模式下打开记录。

   ![属性集列表](./assets/attribute-sets-list.png){width="600" zoomable="yes"}

1. 将FPT属性从右侧的&#x200B;**[!UICONTROL Unassigned Attributes]**&#x200B;列表拖到中心列中的&#x200B;**[!UICONTROL Groups]**&#x200B;列表中。

   每个组文件夹对应于产品信息的一个部分。 当产品在编辑模式下打开时，您可以将属性放置到所需的任何位置。

   ![编辑属性集](./assets/tax-fpt-attribute-set-drag.png){width="600" zoomable="yes"}

1. 完成后，单击&#x200B;**[!UICONTROL Save]**。

1. 对每个应包括固定产品税的属性集重复此步骤。

### 步骤4：将FPT应用于特定产品

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Catalog]** > **[!UICONTROL Products]**。

1. 在编辑模式下打开需要固定产品税的产品。

1. 查找您添加到属性集的字段的&#x200B;**[!UICONTROL FPT]**&#x200B;部分，然后单击&#x200B;**[!UICONTROL Add Tax]**。

1. 指定产品的适用税：

   加拿大的![固定产品税](./assets/tax-product-fpt-canada.png){width="600" zoomable="yes"}

   - 如果您的Commerce实例具有多个网站，请选择适当的&#x200B;**[!UICONTROL Website]**&#x200B;和基本货币。 在此示例中，字段默认设置为`All Websites [USD]`。

   - 将&#x200B;**[!UICONTROL Country/State]**&#x200B;设置为固定产品税适用的区域。

   - 对于&#x200B;**[!UICONTROL Tax]**，输入小数形式的固定产品税。

1. 要添加更多固定产品税，请单击&#x200B;**[!UICONTROL Add Tax]**&#x200B;并重复此过程。

1. 完成后，单击&#x200B;**[!UICONTROL Save]**。

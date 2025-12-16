---
title: 可配置产品
description: 了解如何创建可配置的产品，以便为购物者提供用于选择的变体。
exl-id: 2066fd20-5227-41e9-b213-31825a58ebd9
feature: Catalog Management, Products
source-git-commit: 6fcbcd3b7cace10f0841a46b3cd27343862b3f3b
workflow-type: tm+mt
source-wordcount: '1981'
ht-degree: 0%

---

# 可配置产品

可配置产品显示为单个产品，其中包含变体（如颜色或大小）的下拉选项。 每个变体都是一个单独的简单产品，具有自己的SKU，支持单独的库存跟踪 — 与具有自定义选项的简单产品不同。

**最适合：**&#x200B;具有多个选项（颜色、大小、材质等）的产品，您需要跟踪每个变体的库存。 初始设置需要较长时间，但提供了更好的可扩展性。

![可配置的产品](./assets/product-configurable.png){width="700" zoomable="yes"}

## 开始之前

### 先决条件核对清单

在创建可配置产品之前，请确保您具有：

1. **属性集** — 包含变量属性（如颜色和大小）的属性集
1. **已创建变体属性** — 属性已使用以下设置进行配置
1. **产品图像** — （可选但推荐）父产品和每个变体的图像

### 属性要求

用于产品变体的每个属性都必须具有以下设置：

| 属性 | 必需的设置 |
|--- |--- |
| [!UICONTROL Scope] | `Global` |
| [!UICONTROL Catalog Input Type for Store Owner] | `Dropdown`、`Visual Swatch`或`Text Swatch` |
| [!UICONTROL Values Required] | `Yes` |

{style="table-layout:auto"}

有关创建属性的说明，请参阅[产品属性](product-attributes.md)。

## 阶段1：创建产品基础

### 步骤1：选择产品类型

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Catalog]** > **[!UICONTROL Products]**。

1. 在右上角的&#x200B;_[!UICONTROL Add Product]_（![菜单箭头](../assets/icon-menu-down-arrow-red.png){width="25"} ）菜单中，选择&#x200B;**[!UICONTROL Configurable Product]**。

   ![添加可配置产品](./assets/product-add-configurable.png){width="700" zoomable="yes"}

### 步骤2：选择属性集

[属性集](attribute-sets.md)确定哪些字段出现在产品表单中，哪些属性可用于变体。

1. 单击页面顶部的属性集字段，然后执行下列操作之一：

   - 对于&#x200B;**[!UICONTROL Search]**，输入属性集的名称。
   - 在列表中，选择要使用的属性集。

   表单会更新以反映所选的属性集。

1. 如果需要向属性集添加其他属性，请单击&#x200B;**[!UICONTROL Add Attribute]**&#x200B;并按照[添加属性](product-attributes-add.md)中的说明操作。

   ![选择模板](./assets/product-create-choose-attribute-set.png){width="600" zoomable="yes"}

### 步骤3：输入基本信息

1. 输入产品&#x200B;**[!UICONTROL Product Name]**。

1. 接受基于产品名称的默认&#x200B;**[!UICONTROL SKU]**&#x200B;或输入其他值。

1. 输入产品&#x200B;**[!UICONTROL Price]**。

   >[!NOTE]
   >
   >此价格由子产品价格覆盖。 向客户显示的实际价格来自[!UICONTROL In Stock]子产品。

1. 由于产品尚未准备好发布，请将&#x200B;**[!UICONTROL Enable Product]**&#x200B;设置为`No`。

1. 单击&#x200B;**[!UICONTROL Save]**&#x200B;并继续。

   保存产品后，[商店视图](introduction.md#product-scope)选择器将显示在左上角。

1. 选择要提供产品的&#x200B;**[!UICONTROL Store View]**。

   ![选择商店视图](./assets/product-create-store-view-choose.png){width="600" zoomable="yes"}

### 步骤4：完成基本设置

1. 将&#x200B;**[!UICONTROL Tax Class]**&#x200B;设置为以下项之一：

   - `None`
   - `Taxable Goods`

1. 将&#x200B;**[!UICONTROL Quantity]**&#x200B;留空。 数量由产品变体决定。

1. 保留&#x200B;**[!UICONTROL Stock Status]**&#x200B;设置。

   可配置产品的库存状态由其关联变体决定。 由于保存产品时没有数量，因此&#x200B;**[!UICONTROL Stock Status]**&#x200B;设置为`Out of Stock`。

   >[!NOTE]
   >
   >可配置产品的&#x200B;**库存状态**&#x200B;是&#x200B;**_半手动_**&#x200B;控制的设置，部分基于其子产品的库存状态。 它是&#x200B;**_多条件_**&#x200B;库存状态计算的一部分。 有关详细信息，请参阅[配置库存状态](#configure-stock-status)。

1. 输入产品&#x200B;**[!UICONTROL Weight]**。

   >[!NOTE]
   >
   >可配置产品必须始终具有权重。 如果您从下拉列表中选择&#x200B;**[!UICONTROL This item has no weight]**，则在您保存产品时，它会自动更改为&#x200B;**[!UICONTROL This item has weight]**。

1. 接受&#x200B;**[!UICONTROL Visibility]**&#x200B;的默认`Catalog, Search`设置。

1. 若要在[新产品](../content-design/widget-new-products-list.md)的列表中包含该产品，请选中&#x200B;**[!UICONTROL Set Product as New]**&#x200B;复选框。

1. 要将类别分配给产品，请单击&#x200B;**[!UICONTROL Select…]**&#x200B;框并执行以下操作之一：

   **选择现有类别：**

   - 开始在框中键入以查找匹配项。

   - 选中要分配的每个类别的复选框。

   ![为捆绑包产品选择一个或多个类别](./assets/product-create-categories.png){width="600" zoomable="yes"}

   **创建新类别：**

   - 单击&#x200B;**[!UICONTROL New Category]**。

   - 输入&#x200B;**[!UICONTROL Category Name]**&#x200B;并选择&#x200B;**[!UICONTROL Parent Category]**&#x200B;以确定其在菜单结构中的位置。

   - 单击&#x200B;**[!UICONTROL Create Category]**。

1. 选择&#x200B;**[!UICONTROL Country of Manufacture]**。

   根据属性集，可能会显示其他属性。 您可以稍后完成它们。

### 步骤5：保存并继续

这是保存您工作的好时机。 单击右上角的&#x200B;**[!UICONTROL Save]**。 在下一个阶段，您将为每个变体设置配置。

## 阶段2：添加产品变体

以下步骤显示如何为多个变体添加配置。 页面顶部的进度条显示您在进程中的当前位置。

**示例：**&#x200B;对于具有3种颜色和3种尺寸的衬衫，您将创建9个具有唯一SKU的简单产品（每个组合一个）。 默认情况下，每个变体的产品名称和SKU都基于属性值和父产品名称或SKU。

### 步骤6：选择变体属性

1. 向下滚动到&#x200B;_[!UICONTROL Configurations]_部分，然后单击&#x200B;**[!UICONTROL Create Configurations]**。

   ![配置](./assets/product-configurable-create-configurations.png){width="600" zoomable="yes"}

1. 选中要作为变体包含的每个属性的复选框。

   对于此示例，已选择`color`和`size`。

   ![选择属性](./assets/product-create-configurable-step1.png){width="600" zoomable="yes"}

   该列表包括可在可配置产品中使用的属性集中的所有属性。

1. 如果需要添加属性，请单击&#x200B;**[!UICONTROL Create New Attribute]**&#x200B;并执行以下操作：

   - 填写属性属性。

   - 单击&#x200B;**[!UICONTROL Save Attribute]**。

   - 选中属性的复选框。

1. 单击右上角的&#x200B;**[!UICONTROL Next]**。

### 步骤7：选择属性值

1. 对于每个属性，选中应用于产品的值的复选框。

   ![属性值](./assets/product-create-configurable-step2.png){width="600" zoomable="yes"}

1. 要重新排列属性，请抓住&#x200B;_重新排序_ （ ![排序顺序图标](../assets/icon-sort-order.png) ）图标，并将节移动到新位置。

   顺序确定下拉列表在产品页面上的位置。

1. 在进度条中，单击&#x200B;**[!UICONTROL Next]**。

### 步骤8：配置映像、定价和库存

此步骤确定每个配置的映像、定价和数量。 每个页面可用的选项都相同。 您可以将相同的设置应用于所有SKU，将唯一的设置应用于每个SKU，或者暂时跳过这些设置。

#### 配置图像

选择适用的配置选项：

**选项1：将一组图像应用于所有SKU**

1. 选择&#x200B;**[!UICONTROL Apply single set of images to all SKUs]**。

1. 浏览到每个要包含在产品库中的图像，或将图像拖到框中。

![对所有SKU使用相同的图像](./assets/product-configurations-images-apply-single-set.png){width="600" zoomable="yes"}

**选项2：为每个SKU应用唯一的图像**

由于父产品图像已上传，因此使用此选项可上传每个变体的图像。 当有人购买特定变量时，您可以添加显示在购物车中的不同图像。

1. 选择&#x200B;**[!UICONTROL Apply unique images by attribute to each SKU]**。

1. 选择图像说明的&#x200B;**[!UICONTROL Attribute]**，如`color`。

1. 对于每个属性值，浏览到该配置要使用的图像，或将它们拖到框中。

   如果将图像拖到值框中，它也会出现在其他值的部分中。 要删除图像，请单击&#x200B;_垃圾桶_ （![垃圾桶图标](../assets/icon-delete-trashcan-solid.png)）图标。

   每个SKU ![独特图像](./assets/product-configurable-create-configurations-add-images-unique.png){width="600" zoomable="yes"}

#### 配置定价

>[!NOTE]
>
>可配置产品在目录中没有自己的价格。 可配置产品价格派生自其[!UICONTROL In Stock]子产品。

选择适用的配置选项：

**选项1：对所有SKU应用相同的价格**

1. 如果所有变体的价格相同，请选择&#x200B;**[!UICONTROL Apply single price to all SKUs]**。

1. 输入&#x200B;**[!UICONTROL Price]**。

   ![每个SKU的价格相同](./assets/product-configurable-create-configurations-price-all-skus.png){width="600" zoomable="yes"}

**选项2：为每个SKU应用不同的价格**

1. 如果每个变体或某些变体的价格不同，请选择&#x200B;**[!UICONTROL Apply unique prices by attribute to each SKU]**。

1. 选择作为价差基础的&#x200B;**[!UICONTROL Attribute]**。

1. 为每个属性值输入&#x200B;**[!UICONTROL Price]**。

   在本例中，XL大小的成本较高。

   每个SKU的![唯一价格](./assets/product-configurable-create-configurations-price-unique.png){width="600" zoomable="yes"}

#### 配置清单

选择适用的配置选项：

**选项1：对所有SKU应用相同的数量**

如果所有SKU的数量相同，请选择&#x200B;**[!UICONTROL Apply single quantity to each SKU]**&#x200B;并指定数量。

单个Source商家(_S):_

输入&#x200B;**[!UICONTROL Quantity]**。

使用[Inventory management ](../inventory-management/introduction.md):_的多Source商家(_M)

为所有生成的产品变型分配来源和添加数量：

1. 选择&#x200B;**[!UICONTROL Apply single quantity to each SKU]**&#x200B;选项。

1. 要添加源，请单击&#x200B;**[!UICONTROL Assign Sources]**。

1. 浏览或搜索要添加的源。 选中产品源旁边的复选框。

1. 输入每个来源的现有库存量。

   所有SKU的![单个数量，分配源](./assets/inventory-configure-product-quantity.png){width="600" zoomable="yes"}

**选项2：按属性应用不同的数量**

单个Source商家(_S):_

为每个属性值输入&#x200B;**[!UICONTROL Quantity]**。

使用[Inventory management ](../inventory-management/introduction.md):_的多Source商家(_M)

为所有生成的产品变型分配来源和添加数量：

1. 选择&#x200B;**[!UICONTROL Apply unique quantity by attribute to each SKU]**。

1. 为每个变体输入&#x200B;**[!UICONTROL Quantity]**。

   ![每个属性的不同数量](./assets/product-configurations-quantity-different.png){width="600" zoomable="yes"}

完成图像、价格和数量的配置后，单击右上角的&#x200B;**[!UICONTROL Next]**。

### 步骤9：生成产品配置

请等待片刻，以便显示产品列表，然后执行以下操作之一：

- 如果您对配置满意，请单击&#x200B;**[!UICONTROL Generate Products]**。

- 要进行更正，请单击&#x200B;**[!UICONTROL Back]**。

![在生成产品变体之前查看摘要](./assets/product-create-configurable-summary.png){width="600" zoomable="yes"}

当前产品变体显示在&#x200B;_配置_&#x200B;部分的底部。

![当前配置](./assets/product-create-configurable-generated.png){width="600" zoomable="yes"}

### 步骤10：添加产品图像

1. 向下滚动并展开![部分的](../assets/icon-display-expand.png)扩展选择器&#x200B;_[!UICONTROL Images and Videos]_。

1. 单击&#x200B;_摄像头_&#x200B;图块，并浏览到用于可配置产品的主图像。

有关详细信息，请参阅[图像和视频](product-images-and-video.md)。

### 步骤11：完成产品信息

根据需要向下滚动并完成以下部分中的信息：

- [内容](product-content.md)

- [相关产品、向上销售和交叉销售](related-products-up-sells-cross-sells.md)

- [搜索引擎优化](product-search-engine-optimization.md)

- [可自定义的选项](settings-advanced-custom-options.md)

- [网站中的产品](settings-basic-websites.md)

- [设计](settings-advanced-design.md)

- [礼品选项](product-gift-options.md)

## 阶段3：发布产品

### 步骤12：发布产品

1. 如果您已准备好发布目录中的产品，请将&#x200B;**[!UICONTROL Enable Product]**&#x200B;设置为`Yes`。

1. 执行以下操作之一：

   **方法1：保存并预览**

   - 单击右上角的&#x200B;**[!UICONTROL Save]**。

   - 要查看您商店中的产品，请在&#x200B;**[!UICONTROL Customer View]**&#x200B;管理员&#x200B;_（_&#x200B;菜单箭头![ ）菜单上选择](../assets/icon-menu-down-arrow-black.png)。

   该存储将在新的浏览器选项卡中打开。

   ![客户视图](./assets/product-admin-customer-view.png){width="600" zoomable="yes"}

   **方法2：保存并关闭**

   在&#x200B;_[!UICONTROL Save]_（![菜单箭头](../assets/icon-menu-down-arrow-red.png){width="25"} ）菜单中，选择&#x200B;**[!UICONTROL Save & Close]**。

## 配置库存状态

可配置产品库存状态与简单产品库存状态不同。 对于可配置产品，库存状态是&#x200B;**_多条件_**&#x200B;计算的一部分。

### 库存状态的工作方式

股票状态行为的主要原则为：

| 您已将状态设置为 | 结果 | 由子产品控制？ |
|---|---|---|
| `Out of Stock` （手动） | 在管理员和店面中始终显示`Out of Stock` | 否 — 在手动更改为`In Stock`之前保持不变 |
| `In Stock` （手动） | 状态是基于子产品的动态的 | 部分 — 请参阅下面的详细信息 |

{style="table-layout:auto"}

### 当设置为“有货”时

手动将可配置产品库存状态设置为`In Stock`时，其行为因库存设置而异：

**仅使用默认源/库存：**

- **管理员和店面：**&#x200B;库存状态自动反映子产品的可用性

**至少具有一个自定义源/库存：**

- **店面：**&#x200B;库存状态自动反映子产品可用性
- **管理员：**&#x200B;保留为`In Stock`，直到手动更改（不受子产品控制）为止

>[!NOTE]
>
>自定义库存和来源是[Inventory management](../inventory-management/sources-stocks.md)扩展的一部分。 强烈建议您专门使用此工具来管理库存和来源。 默认的source和stock函数是`CatalogInventory`模块的一部分，该模块现已弃用。

### 手动库存状态更改

如果您手动将Stock状态设置为`Out of Stock`（通过管理员用户操作、文件导入或API调用），则在手动将其更改回`Out of Stock`之前，它会在管理员和店面中保留`In Stock`。 它不受子产品库存状态的影响。

## 系统配置（可选）

### 在购物车缩略图中显示变量图像

如果您对每个变体具有不同的图像，则可以配置系统以显示购物车缩略图的正确图像。

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧面板中，展开&#x200B;**[!UICONTROL Sales]**&#x200B;并选择&#x200B;**[!UICONTROL Checkout]**。

1. 展开![部分的](../assets/icon-display-expand.png)扩展选择器&#x200B;_[!UICONTROL Shopping Cart]_。

1. 将&#x200B;**[!UICONTROL Configurable Product Image]**&#x200B;设置为`Product Thumbnail Itself`。

1. 单击&#x200B;**[!UICONTROL Save Config]**。

   ![购物车 — 可配置产品图像](./assets/config-checkout-configurable-product.png){width="600" zoomable="yes"}

## 关键注意事项

- **变量类型：**&#x200B;购物者可以从下拉列表、多选、可视样本和文本样本输入类型中选择选项。 每个选项都是一个单独的简单产品。

- **库存跟踪：**&#x200B;与具有自定义选项的简单产品不同，可配置产品会单独跟踪每个变体的库存。

- **子产品类型：**&#x200B;子产品可以是简单或虚拟产品&#x200B;**没有自定义选项**。 若要使子产品成为虚拟产品，请为每个子产品的`Тhis item has no weight`设置选择&#x200B;**[!UICONTROL Weight]**。

- **全局分配：**&#x200B;子产品同时在所有网站、商店和商店视图中进行全局分配和取消分配&#x200B;**全局分配**。

- **定价：**&#x200B;可配置产品在目录中没有自己的价格。 显示的价格来自其[!UICONTROL In Stock]子产品。

- **属性：**&#x200B;变体属性必须具有全局范围，必须要求客户选择一个值。 属性必须包含在用于可配置产品的属性集中。

- **购物车缩略图：**&#x200B;购物车缩略图可以显示来自可配置产品记录或产品变体的图像。 请参阅上面的[系统配置](#system-configuration-optional)。

- **样本行为：** [样本属性](swatches.md#create-swatches-for-products)可以通过在属性编辑页面上将&#x200B;**[!UICONTROL Update Product Preview Image]**&#x200B;设置为`No`来选择样本时，将样本属性配置为不显示相应的简单产品图像。

- **图像库行为：**&#x200B;主题控制用户切换产品配置时图像库的行为。 _Blank_&#x200B;主题的默认行为使用选定的变量覆盖父可配置产品图像。 对于Luma主题，默认行为是将选定的变体图像附加到父可配置产品图像之前。

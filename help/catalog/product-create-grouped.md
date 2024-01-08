---
title: 已分组的产品
description: 了解如何创建由简单独立产品组成的分组产品，这些产品以组形式呈现。
exl-id: af42b7fc-27f2-4c5a-b504-a70a324fae76
feature: Catalog Management, Products
source-git-commit: 140930df515d1e0604b18a4ebf689254b9487b53
workflow-type: tm+mt
source-wordcount: '1055'
ht-degree: 0%

---

# 已分组的产品

分组产品由简单独立产品组成，这些产品以组形式显示。 您可以提供单个产品的变体或按季节或主题对它们进行分组。 展示分组产品可以鼓励客户购买附加产品。 通过分组产品，可以轻松提供产品的变体并在同一页面上列出所有变体。

例如，您可以销售未售出的餐具，并列出在正式位置设置中使用的每种类型的餐具。 有些人可能会点多份沙拉叉、鱼叉、晚餐叉、晚餐刀、鱼刀、黄油刀、汤匙和甜点勺子。 其他客户可能会订购一个简单的叉子、刀和勺子。 客户可以根据需要订购任意数量的每个项目。

尽管它们以组形式呈现，但组中的每个产品都是作为单独的项目购买的。 在购物车中，每个项目和购买的数量都显示为单独的行项目。

下面的说明演示了使用创建分组产品的过程 [产品模板](attribute-sets.md)、必填字段和基本设置。 每个必填字段都标有红色星号(`*`)。 完成基础知识后，您可以根据需要完成其他产品设置。

![已分组的产品](./assets/product-grouped.png){width="700" zoomable="yes"}

## 步骤1：选择产品类型

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. 在 _[!UICONTROL Add Product]_( ![菜单箭头](../assets/icon-menu-down-arrow-red.png){width="25"} )菜单，然后选择&#x200B;**[!UICONTROL Grouped Product]**.

   ![添加分组的产品](./assets/product-add-grouped.png){width="700" zoomable="yes"}

## 步骤2：选择属性集

选择 [属性集](attribute-sets.md) 作为产品的模板，执行以下操作之一：

- 要搜索，请输入 **[!UICONTROL Attribute Set]**.
- 在列表中，选择要使用的属性集。

将更新表单以反映更改。

![选择模板](./assets/product-create-choose-attribute-set.png){width="600" zoomable="yes"}

如果所需属性不存在，则可以在创建产品时添加新属性：

- 在右上角，单击 **[!UICONTROL Add Attribute]**.
- 定义新属性(请参阅 [将属性添加到产品](product-attributes-add.md))。

  ![新建属性](./assets/product-attribute-add-select.png){width="600" zoomable="yes"}

要向产品添加现有属性，请使用 [筛选器控件](../getting-started/admin-grid-controls.md) 在网格中查找属性并执行以下操作：

- 选中要添加的每个属性的第一列中的复选框。
- 单击 **[!UICONTROL Add Selected]**.

## 第3步：完成所需的设置

1. 输入 **[!UICONTROL Product Name]**.

1. 接受默认值 **[!UICONTROL SKU]** 基于产品名称或输入其他名称。

   请注意 **[!UICONTROL Quantity]** 字段不可用，因为该值派生自组成该组的各个产品。

   分组的产品在目录中没有自己的价格。 分类产品价格乃按本集团所包含个别产品之价格计算。

1. 由于产品尚未准备好发布，请设置 **[!UICONTROL Enable Product]** 到 `No` ( ![切换否](../assets/toggle-no.png) )。

1. 单击 **[!UICONTROL Save]** 并继续。

   保存产品后，产品名称将显示在页面顶部，并且 [商店视图](introduction.md#product-scope) 选择器显示在左上角。

1. 选择 **[!UICONTROL Store View]** 在产品可用的位置。

   ![选择商店视图](./assets/product-create-store-view-choose.png){width="600" zoomable="yes"}

## 步骤4：完成基本设置

1. 接受 **[!UICONTROL Stock Status]** 设置 `In Stock`.

1. 要分配 **[!UICONTROL Categories]** 对于产品，单击 **[!UICONTROL Select…]** 框并执行以下任一操作：

   **选择现有类别：**

   - 在框中开始键入，直到找到匹配项为止。

   - 选中要分配的类别的复选框。

   **创建类别：**

   - 单击 **[!UICONTROL New Category]**.

   - 输入 **[!UICONTROL Category Name]** 并选择 **[!UICONTROL Parent Category]**，确定其在菜单结构中的位置。

   - 单击 **[!UICONTROL Create Category]**.

1. 接受 **[!UICONTROL Visibility]** 设置 `Catalog, Search`.

1. 要在中突出显示该产品，请执行以下操作 [新产品列表](../content-design/widget-new-products-list.md)，选择 **[!UICONTROL Set Product as New]** **[!UICONTROL from]** 和 **[!UICONTROL to]** 日历中的日期。

1. 选择 **[!UICONTROL Country of Manufacture]**.

   可能有其他单个属性用于描述产品。 所选内容会改变属性集，您可以稍后完成它们。

## 步骤5：将产品添加到组

1. 向下滚动到 **[!UICONTROL Grouped Products]** 部分并单击 **[!UICONTROL Add Products to Group]**.

   ![分组的产品](./assets/product-grouped-products.png){width="600" zoomable="yes"}

1. 如有必要，请使用 [过滤器](../getting-started/admin-grid-controls.md) 查找要包含在组中的产品。

1. 在列表中，选中要包含在组中的每个项目的复选框。

   >[!NOTE]
   >
   >只有简单、可下载且没有可配置选项的虚拟产品才能分组为子产品。 其他产品类型不会显示在选择列表中。

   ![添加所选产品](./assets/product-grouped-add-products.png){width="600" zoomable="yes"}

1. 要将它们添加到产品组，请单击 **[!UICONTROL Add Selected Products]**.

   选定的产品将显示在 _[!UICONTROL Grouped Products]_部分。

   对于具有下列项的多源商家 [Inventory management](../inventory-management/sources-stocks.md)，该网格包括 **[!UICONTROL Quantity per Source]** 具有每个分配的来源和库存库存库存量的列。

   ![组中的产品](./assets/product-grouped-grouped-products-section.png){width="600" zoomable="yes"}

1. 输入 **[!UICONTROL Default Quantity]** 用于任何项目。

1. 要更改产品的顺序，请抓取 _更改顺序_ 图标( ![位置控制器](../assets/icon-sort-order.png) )并将产品拖到列表中的新位置。

1. 要从组中删除产品，请单击 **[!UICONTROL Remove]**.

## 第5步：完成产品信息

根据需要完成以下部分中的信息：

- [内容](product-content.md)
- [图像和视频](product-images-and-video.md)
- [搜索引擎优化](product-search-engine-optimization.md)
- [相关产品、向上销售和交叉销售](related-products-up-sells-cross-sells.md)
- [可自定义的选项](settings-advanced-custom-options.md)
- [网站中的产品](settings-basic-websites.md)
- [设计](settings-advanced-design.md)
- [礼品选项](product-gift-options.md)

## 步骤6：发布产品

1. 如果您已准备好在目录中发布产品，请设置 **[!UICONTROL Enable Product]** 到 `Yes`.

1. 执行以下操作之一：

   **方法1：** 保存并预览

   - 在右上角，单击 **[!UICONTROL Save]**.

   - 要查看您商店中的产品，请选择 **[!UICONTROL Customer View]** 在 _管理员_ ( ![菜单箭头](../assets/icon-menu-down-arrow-black.png) )菜单。

     该存储将在新的浏览器选项卡中打开。

     ![客户视图](./assets/product-admin-customer-view.png){width="700" zoomable="yes"}

   **方法2：** 保存并关闭

   - 在 _[!UICONTROL Save]_( ![菜单箭头](../assets/icon-menu-down-arrow-red.png){width="25"} )菜单，选择&#x200B;**[!UICONTROL Save & Close]**.

## 步骤7：配置购物车缩略图（可选）

如果您组中的每个产品具有不同的图像，则可以设置配置以将正确的图像用于购物车缩略图。

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中，展开 **[!UICONTROL Sales]** 并选择 **[!UICONTROL Checkout]**.

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Shopping Cart]**.

   有关这些配置选项的详细列表，请参见 [购物车](../configuration-reference/sales/checkout.md#shopping-cart) 在 _配置引用_.

1. 设置 **[!UICONTROL Grouped Product Image]** 到 `Product Thumbnail Itself`.

   ![购物车](./assets/config-sales-cart-grouped-product.png){width="600" zoomable="yes"}

   如有必要，请取消选择 **[!UICONTROL Use system value]** 复选框。

1. 单击 **[!UICONTROL Save Config]**.

## 注意事项

- 分组产品本质上是一组简单的关联产品。

- 分组的子产品可以是简单、可下载或虚拟产品 **[!UICONTROL without custom options]**.

- 每个购买的项目单独出现在购物车中，而不是作为组的一部分出现。

- 分组的产品在目录中没有自己的价格。 分类产品价格乃按本集团所包含个别产品之价格计算。

- 可将购物车中的缩略图图像设置为显示来自分组的父产品或相关产品的图像。

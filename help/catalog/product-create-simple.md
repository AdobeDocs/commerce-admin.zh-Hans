---
title: 简单产品
description: 了解如何创建可单独销售或作为分组、可配置或捆绑产品一部分的简单产品。
exl-id: 3ac9b28d-3929-4fd6-97ca-145ea6d6897c
feature: Catalog Management, Products
source-git-commit: 4a3aa2aa32b692341edabd41fdb608e3cff5d8e0
workflow-type: tm+mt
source-wordcount: '602'
ht-degree: 0%

---

# 简单产品

利用产品类型强大功能的关键之一是，了解何时使用简单的独立产品。 简单产品可以单独销售，也可以作为分组、可配置或捆绑产品的一部分销售。 具有自定义选项的简单产品有时称为&#x200B;_复合产品_。

以下说明演示了使用[产品模板](attribute-sets.md)、必填字段和基本设置创建简单产品的过程。 每个必填字段都标有红色星号(`*`)。 完成基础知识后，您可以根据需要完成其他产品设置。

![简单产品](./assets/product-simple.png){width="700" zoomable="yes"}

## 步骤1：选择产品类型

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Catalog]** > **[!UICONTROL Products]**。

1. 在右上角的&#x200B;_[!UICONTROL Add Product]_（![菜单箭头](../assets/icon-menu-down-arrow-red.png){width="25"} ）菜单中，选择&#x200B;**[!UICONTROL Simple Product]**。

   ![添加简单产品](./assets/product-add-simple.png){width="700" zoomable="yes"}

## 步骤2：选择属性集

选择用作产品模板的[属性集](attribute-sets.md)：

- 单击&#x200B;**[!UICONTROL Attribute Set]**&#x200B;字段并输入属性集的全部或部分名称。

- 在显示的列表中，选择要使用的属性集。

将更新表单以反映更改。

![选择属性集](./assets/product-create-choose-attribute-set.png){width="600" zoomable="yes"}

## 第3步：完成所需的设置

1. 输入&#x200B;**[!UICONTROL Product Name]**。

1. 接受基于产品名称的默认&#x200B;**[!UICONTROL SKU]**&#x200B;或输入其他名称。

1. 输入产品&#x200B;**[!UICONTROL Price]**。

1. 由于产品尚未准备好发布，请将&#x200B;**[!UICONTROL Enable Product]**&#x200B;选项设置为`No`。

1. 单击&#x200B;**[!UICONTROL Save]**&#x200B;并继续。

   保存产品后，[商店视图](introduction.md#product-scope)选择器将显示在左上角。

1. 选择要提供产品的&#x200B;**[!UICONTROL Store View]**。

   ![选择商店视图](./assets/product-create-store-view-choose.png){width="600" zoomable="yes"}

## 步骤4：完成基本设置

1. 将&#x200B;**[!UICONTROL Tax Class]**&#x200B;设置为以下项之一：

   - `None`
   - `Taxable Goods`
   - `Refund Adjustments`
   - `Gift Options`
   - `Order Gift Wrapping`
   - `Item Gift Wrapping`
   - `Printed Gift Card`
   - `Reward Points`
   - `VAT Reduced`
   - `VAT Standard`

1. 输入有库存的产品的&#x200B;**[!UICONTROL Quantity]**。

   默认情况下，**[!UICONTROL Stock Status]**&#x200B;设置为`In Stock`。

   >[!NOTE]
   >
   >如果启用[Inventory management](../inventory-management/introduction.md)，则Single Source商家将设置此部分中的数量。 多Source商家在“来源”部分添加来源和数量。 请参阅以下&#x200B;_分配来源和数量(Inventory management)_&#x200B;部分。

1. 输入产品的&#x200B;**[!UICONTROL Weight]**。

1. 接受&#x200B;**[!UICONTROL Visibility]**&#x200B;的默认`Catalog, Search`设置。

1. 要将&#x200B;_[!UICONTROL Categories]_分配给产品，请单击&#x200B;**[!UICONTROL Select…]**框并执行以下任一操作：

   **选择现有类别**：

   - 在框中开始键入，直到找到匹配项为止。

   - 选中要分配的每个类别的复选框。

   **创建类别**：

   - 单击&#x200B;**[!UICONTROL New Category]**。

   - 输入&#x200B;**[!UICONTROL Category Name]**&#x200B;并选择&#x200B;**[!UICONTROL Parent Category]**&#x200B;以确定其在菜单结构中的位置。

   - 单击&#x200B;**[!UICONTROL Create Category]**。

1. 若要在[新产品](../content-design/widget-new-products-list.md)的列表中包含该产品，请选中&#x200B;**[!UICONTROL Set Product as New]**&#x200B;复选框。

1. 选择&#x200B;**[!UICONTROL Country of Manufacture]**。

可能有其他单个属性用于描述产品。 选择因属性集而异，您可以稍后完成它们。

### 分配来源和数量([!DNL Inventory Management])

{{$include /help/_includes/inventory-assign-sources.md}}

## 第5步：完成产品信息

根据需要向下滚动并完成以下部分中的信息：

- [内容](product-content.md)
- [图像和视频](product-images-and-video.md)
- [相关产品、向上销售和交叉销售](related-products-up-sells-cross-sells.md)
- [搜索引擎优化](product-search-engine-optimization.md)
- [可自定义的选项](settings-advanced-custom-options.md)
- [网站中的产品](settings-basic-websites.md)
- [设计](settings-advanced-design.md)
- [礼品选项](product-gift-options.md)

## 步骤6：发布产品

1. 如果您已准备好发布目录中的产品，请将&#x200B;**[!UICONTROL Enable Product]**&#x200B;开关设置为`Yes`。

1. 执行以下操作之一：

   - **方法1：**&#x200B;保存并预览

      - 单击右上角的&#x200B;**[!UICONTROL Save]**。

      - 要查看您商店中的产品，请在&#x200B;**[!UICONTROL Customer View]**&#x200B;管理员&#x200B;_（_&#x200B;菜单箭头![）菜单上选择](../assets/icon-menu-down-arrow-black.png)。

     该存储将在新的浏览器选项卡中打开。

     ![客户视图](./assets/product-admin-customer-view.png){width="600" zoomable="yes"}

   - **方法2：**&#x200B;保存并关闭

     在&#x200B;_[!UICONTROL Save]_（![菜单箭头](../assets/icon-menu-down-arrow-red.png){width="25"} ）菜单中，选择&#x200B;**[!UICONTROL Save & Close]**。

## 注意事项

- 简单产品可包含在可配置、捆绑和分组产品类型中。

- 简单产品配置会覆盖特定产品的可配置产品配置。

- 简单的产品可以具有包含各种输入类型的自定义选项，这使得从单个SKU销售多种产品变体成为可能。

<!-- Last updated from includes: 2023-05-19 17:14:58 -->

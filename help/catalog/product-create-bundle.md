---
title: 捆绑产品
description: 了解如何创建捆绑产品，让购物者能够在您的商店中构建定制产品。
exl-id: dfa31eb8-2330-44eb-889b-5d10ce56ef13
feature: Catalog Management, Products
source-git-commit: 891b94d84ed411232aa163f99bb110780d399dfb
workflow-type: tm+mt
source-wordcount: '1547'
ht-degree: 0%

---

# 捆绑产品

捆绑包是一个 _构建您自己的_，可自定义的产品。 捆绑包中的每个项目可以基于以下产品类型之一：

- [简单产品](product-create-simple.md)
- [虚拟产品](product-create-virtual.md)

![捆绑产品](./assets/product-bundle.png){width="700" zoomable="yes"}

当客户单击以下任一选项时，即会显示这些选项 **[!UICONTROL Customize]** 或 **[!UICONTROL Add to Cart]**. 由于捆绑包中包含的产品各不相同，因此SKU、价格和重量可以设置为动态值或固定值。

>[!NOTE]
>
>最小广告价(MAP)不适用于使用动态定价的捆绑销售产品。

>[!NOTE]
>
>父捆绑产品始终自动显示为其所有子产品的追加销售产品。

如果 [即时购买](../stores-purchase/checkout-instant-purchase.md) 可用， _即时购买_ 按钮显示在页面上 _添加到购物车_ 包中每个项目的按钮。

![自定义捆绑包](./assets/product-bundle-customize.png){width="600" zoomable="yes"}

以下说明将引导您完成使用创建捆绑产品的过程 [产品模板](attribute-sets.md)、必填字段和基本设置。 每个必填字段都标有红色星号(`*`)。 完成基础知识后，您可以根据需要完成其他产品设置。

## 步骤1：选择产品类型

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. 在右上角 _[!UICONTROL Add Product]_( ![菜单箭头](../assets/icon-menu-down-arrow-red.png){width="25"} )菜单，选择&#x200B;**[!UICONTROL Bundle Product]**.

   ![添加捆绑产品](./assets/product-add-bundle.png){width="700" zoomable="yes"}

## 步骤2：选择属性集

选择 [属性集](attribute-sets.md) 作为产品的模板，执行以下操作之一：

- 对象 **[!UICONTROL Search]**，输入属性集的名称，
- 在列表中，选择要使用的属性集。

将更新表单以反映更改。

![选择模板](./assets/product-create-choose-attribute-set.png){width="600" zoomable="yes"}

## 第3步：完成所需的设置

1. 输入产品 **[!UICONTROL Product Name]**.

1. 接受默认值 **[!UICONTROL SKU]** 基于产品名称或输入其他值。

   要确定分配给每个捆绑项目的SKU类型，请执行以下操作：

   - A **[!UICONTROL Dynamic SKU]** 可以通过向默认SKU添加后缀来自动分配给每个捆绑项目。 默认情况下，设置为 `Yes`.

   - 如果您希望为每个捆绑项目分配唯一的SKU，请设置 **[!UICONTROL Dynamic SKU]** 到 `No`.

   ![动态SKU和价格](./assets/product-bundle-manual-sku.png){width="600" zoomable="yes"}

1. 要确定捆绑包的价格，请执行下列操作之一：

   - 要使价格反映客户选择的选项，请设置 **[!UICONTROL Dynamic Price]** 到 `Yes` 然后离开 **[!UICONTROL Price]** 空白。

   - 要对捆绑包收取固定价格，请设置 **[!UICONTROL Dynamic Price]** 到 `No` 并输入 **[!UICONTROL Price]** 你要为这包东西收费。

   >[!NOTE]
   >
   >[!UICONTROL Special Price] 和 [!UICONTROL Customer Group Price] （层价格）始终设置为所有捆绑产品类型的折扣百分比。

1. 由于产品尚未准备好发布，请设置 **[!UICONTROL Enable Product]** 到 `No`.

1. 单击 **[!UICONTROL Save]** 并继续。

   保存产品后， [商店视图](introduction.md#product-scope) 选择器显示在左上角。

1. 选择 **[!UICONTROL Store View]** 在产品可用的位置。

   ![选择商店视图](./assets/product-create-store-view-choose.png){width="600" zoomable="yes"}

## 步骤4：完成基本设置

1. 如果捆绑包具有固定定价，请设置 **[!UICONTROL Tax Class]** 更改为以下任一项：

   - `None`
   - `Taxable Goods`

   如果捆绑包具有动态定价，则税是针对 **_每个_** 捆绑包项。 如果捆绑包具有固定定价，则税是针对以下项目确定的： **_全部_** 捆绑产品。

1. 请注意以下事项：

   - 此 **[!UICONTROL Quantity]** 不可用，因为值是每个捆绑项目确定的。

   - 默认情况下， **[!UICONTROL Stock Status]** 设置为 `In Stock`.

1. 要确定束的重量，请执行下列操作之一：

   - 要使权重反映客户选择的选项，请设置 **[!UICONTROL Dynamic Weight]** 设置 `Yes` 然后离开 **[!UICONTROL Weight]** 空白。

   - 要为捆绑分配固定权重，请设置 **[!UICONTROL Dynamic Weight]** 到 `No` 并输入 **[!UICONTROL Weight]** 捆绑包的。

   ![动态权重](./assets/product-bundle-dynamic-weight.png){width="600" zoomable="yes"}

1. 在列表中突出显示该产品： [新产品](../content-design/widget-new-products-list.md)，选择 **[!UICONTROL Set Product as New]** 复选框。

1. 接受默认值 **[!UICONTROL Visibility]** 设置 `Catalog, Search`.

1. 要分配 _[!UICONTROL Categories]_对于产品，单击&#x200B;**[!UICONTROL Select…]**框并执行以下任一操作：

   **选择现有类别：**

   - 在框中开始键入，直到找到匹配项为止。

   - 选中要分配的每个类别的复选框。

   ![为捆绑产品选择一个或多个类别](./assets/product-create-categories.png){width="600" zoomable="yes"}

   **创建类别：**

   - 单击 **[!UICONTROL New Category]**.

   - 输入 **[!UICONTROL Category Name]** 并选择 **[!UICONTROL Parent Category]**，确定其在菜单结构中的位置。

   - 单击 **[!UICONTROL Create Category]**.

1. 选择 **[!UICONTROL Country of Manufacture]**.

   可能有其他属性用于描述产品。 所选内容会改变属性集，您可以稍后完成它们。

## 步骤5：添加捆绑项目

此 _[!UICONTROL Bundle Items]_section用于将项目添加到捆绑产品类型并编辑当前选定的项目。

![为产品定义的捆绑项目](./assets/product-bundle-items-ball.png){width="600" zoomable="yes"}

1. 向下滚动到 _捆绑包项目_ 分区和设置 **[!UICONTROL Ship Bundle Items]** 更改为以下任一项：

   - `Separately`
   - `Together`

   如果您选择 `Together`，所有捆绑项目必须分配相同的 [源](../inventory-management/sources-manage.md).

1. 单击 **[!UICONTROL Add Option]** 并执行以下操作：

   - 输入 **[!UICONTROL Option Title]** 用作字段标签。

   - 设置 **[!UICONTROL Input Type]** 更改为以下任一项：

      - `Drop-down`
      - `Radio buttons`
      - `Checkbox`
      - `Multiple Select`

   - 要使字段成为必填项，请选择 **[!UICONTROL Required]** 复选框。

   - 单击 **[!UICONTROL Add Products to Option]** ，然后选中要包含在此选项中的每个产品的复选框。

     如果有多种产品，请使用列表过滤器和分页控件来查找所需的产品。

   - 单击 **[!UICONTROL Add Selected Products]**.

     ![添加所选产品](./assets/product-bundle-add-products-to-option.png){width="600" zoomable="yes"}

   - 项目出现在 _选项_ 部分，选择一个项目作为 **[!UICONTROL Default]** 选择。

   - 在 _默认数量_ 列，输入客户选择物料时要添加到捆绑中的每项物料的数量。

   - 要允许客户更改捆绑项目的数量，请选择 **[!UICONTROL User Defined]**.


     >[!NOTE]
     >
     >量可以是预设值或用户定义的值。 但是，请勿将 _[!UICONTROL User Defined]_属性到复选框或多选输入类型。

     默认情况下，客户不能更改捆绑项目中包含的“默认数量”。 但是，客户可以输入要包括在捆绑中的物料数量。

     例如，如果将Sprite Status Ball的“缺省量”设置为 `2` 和客户订单 `4` 在该捆绑”选项中，购买的总球数为 `8`.

     ![项目详细信息](./assets/product-bundle-item-detail.png){width="600" zoomable="yes"}

1. 对要添加到捆绑包中的每个项目重复这些步骤。

1. 要更改束截面中的项目顺序，请单击 _移动_ ( ![“移动”图标](../assets/icon-move.png) )图标，并将项目拖到适当的位置。

   ![更改捆绑项目的顺序](./assets/product-bundle-items-move.png){width="600" zoomable="yes"}

   也可以在导出的捆绑产品的数据中更改项目的顺序，然后重新导入到目录中。 有关更多信息，请参阅 [导入捆绑包产品](../systems/data-transfer-bundle-products.md).

   为了更好地查看工作区，请先折叠每个部分，然后将它们拖动到适当位置。

1. 要从捆绑包中删除任何项目，请单击 **[!UICONTROL Delete]** ( ![“垃圾桶”图标](../assets/icon-delete-trashcan.png) )图标。

1. 完成后，单击 **[!UICONTROL Save]**.

## 步骤6：完成产品信息

根据需要向下滚动并完成以下部分中的信息：

- [内容](product-content.md)
- [图像和视频](product-images-and-video.md)
- [搜索引擎优化](product-search-engine-optimization.md)
- [相关产品、向上销售和交叉销售](related-products-up-sells-cross-sells.md)
- [可自定义的选项](settings-advanced-custom-options.md)
- [网站中的产品](settings-basic-websites.md)
- [设计](settings-advanced-design.md)
- [礼品选项](product-gift-options.md)

## 步骤7：发布产品

1. 如果您已准备好在目录中发布产品，请设置 **[!UICONTROL Enable Product]** 到 `Yes` ( ![切换是](../assets/toggle-yes.png) )。

1. 执行以下操作之一：

   **方法1：** 保存并预览

   - 在右上角，单击 **[!UICONTROL Save]**.

   - 要查看您商店中的产品，请选择 **[!UICONTROL Customer View]** 在 _管理员_ ( ![菜单箭头](../assets/icon-menu-down-arrow-black.png) )菜单。

     该存储将在新的浏览器选项卡中打开。

   ![客户视图](./assets/product-admin-customer-view.png){width="600" zoomable="yes"}

   **方法2：** 保存并关闭

   在 _[!UICONTROL Save]_( ![菜单箭头](../assets/icon-menu-down-arrow-red.png){width="25"} )菜单，选择&#x200B;**[!UICONTROL Save & Close]**.

## 输入控件

| 控件 | 描述 | 示例 |
|--- |--- |--- |
| [!UICONTROL Drop-down] | 显示包含产品名称和价格的选项下拉列表。 只能选择一个项目。 | ![下拉面板](./assets/product-bundle-input-type-drop-down.png){width="200"} |
| [!UICONTROL Radio Buttons] | 显示每个选项的单选按钮，其后是产品名称和价格。 只能选择一个项目。 | ![单选按钮](./assets/product-bundle-input-type-radio-buttons.png){width="200"} |
| [!UICONTROL Checkbox] | 显示每个选项的复选框，后跟产品名称和价格。 可以选择多个项目。 | ![复选框](./assets/product-bundle-input-type-checkbox.png){width="200"} |
| [!UICONTROL Multiple Select] | 显示选项列表以及产品名称和价格。 要选择多个项目，请按住Ctrl键(PC)或Command键(Mac)并单击每个项目。 | ![多选](./assets/product-bundle-input-type-multiple-select.png){width="200"} |

{style="table-layout:auto"}

## 字段描述

| 字段 | 描述 |
|--- |--- |
| [!UICONTROL SKU] | 确定每个项目是否分配了变量或动态SKU，或者是否为捆绑包使用固定SKU。 选项： `Fixed` / `Dynamic` |
| [!UICONTROL Weight] | 指定权重是根据所选项目计算的，还是为整个包的固定权重。 选项： `Fixed` / `Dynamic` |
| [!UICONTROL Price View] | 确定产品价格是显示为从最低价到最贵（价格范围）的某个范围，还是显示为最低价（最低价）。 选项： `Price Range` / `As Low As` |
| 发运捆绑包项目 | 指定是否可单独装运单个物料。 |

{style="table-layout:auto"}

## 捆绑产品库存状态

捆绑产品库存状态为 **_自动更改为缺货_** 出现以下任一情况时：

- 所有选项都是可选的，所有关联产品都是 _缺货_.

- 某些选项是必需的，并且与任何必需选项关联的产品为 _缺货_.

捆绑产品库存状态为 **_未自动更改为缺货_** 出现以下任一情况时：

- 所有选项都是可选的，并且至少有一个关联产品是 _有货_.

- 某些选项是必需的，并且每个必需选项中至少有一个关联产品是 _有货_.

## 注意事项

![复选框](../assets/checkbox.png) 客户可以 _构建他们自己的_ 捆绑产品。

![复选框](../assets/checkbox.png) 捆绑包项目可以是简单或虚拟产品，而无需自定义选项。

![复选框](../assets/checkbox.png) “价格视图”可以设置为 `Price Range` 或 `As Low As`.

![复选框](../assets/checkbox.png) SKU和权重可以为 `Fixed` 或 `Dynamic`.

![复选框](../assets/checkbox.png) 量可以是预设值或用户定义的值。 但是，请勿将 _[!UICONTROL User Defined]_属性到复选框或多选输入类型。

![复选框](../assets/checkbox.png) 捆绑项目可以一起发运或单独发运。

![复选框](../assets/checkbox.png) 父捆绑产品始终自动显示为其所有子产品的追加销售产品。

![复选框](../assets/checkbox.png) [!UICONTROL Special Price] 和 [!UICONTROL Customer Group Price] （层价格）始终设置为所有捆绑产品类型的折扣百分比。

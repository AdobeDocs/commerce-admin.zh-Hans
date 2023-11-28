---
title: 创建和删除产品属性
description: 了解如何创建和删除产品属性，这些属性用于描述目录中产品的特定特征。
exl-id: fd0e5d5b-a917-4e55-8ec2-7ebb040d3d06
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '1159'
ht-degree: 0%

---

# 创建和删除产品属性

您可以在处理产品时创建属性，也可以从 _[!UICONTROL Product Attributes]_页面。 以下步骤显示如何从创建属性_[!UICONTROL Stores]_ 菜单。

## 步骤1：描述基本属性属性

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. 单击 **[!UICONTROL Add New Attribute]**.

   ![新建属性属性](./assets/attribute-properties.png){width="600" zoomable="yes"}

1. 对象 **[!UICONTROL Default Label]**，输入用于标识属性的标签。

1. 要确定用于数据输入的输入控件的类型，请设置 **[!UICONTROL Catalog Input Type for Store Owner]** 更改为以下任一项：

   | 属性 | 描述 |
   |--- |--- |
   | `Text Field` | 单行输入文本字段。 |
   | `Text Area` | 用于输入文本段落（如产品说明）的多行输入字段。 您可以使用WYSIWYG编辑器设置带有HTML标记的文本格式，或者直接在文本中输入标记。 |
   | `Text Editor` | 属性位置处具有完整功能的文本编辑器。 |
   | 日期 | 在中显示日期值 [首选格式](attributes-input-types.md#date-and-time-options) 和 [时区](../getting-started/store-details.md#locale-options). 可以从列表或日历中选择日期值( ![日历图标](../assets/icon-calendar.png) )。 <br/><br/>**_注意：_**根据您的系统配置，_管理员&#x200B;_用户可以直接在字段中输入日期，或从日历或列表中选择日期。 有关指定日期和时间值的信息，请参见 [日期和时间选项](attributes-input-types.md#date-and-time-options). |
   | `Yes/No` | 显示一个预定义选项的下拉列表 `Yes` 和 `No`. |
   | `Dropdown` | 显示仅接受单个选择的值的下拉列表。 下拉列表输入类型是的关键组件 [可配置产品](product-create-configurable.md). |
   | `Multiple Select` | 显示接受多个选择的值的下拉列表。 |
   | `Price` | 此输入类型用于创建除预定义属性之外的价格字段：价格、特殊价格、层价格和成本。 使用的货币由系统配置决定。 |
   | `Media Image` | 将额外的图像与产品相关联，例如产品徽标、护理说明或食品标签中的成分。 将媒体图像属性添加到产品的属性集时，它将与基本图像、小型图像和缩略图一起成为额外的图像类型。 媒体图像属性可从中排除 [店面媒体浏览器](catalog-images-video.md#storefront-media-browser). |
   | `Fixed Product Tax` | 允许您定义 [FPT率](../stores-purchase/fixed-product-tax.md) 根据您区域设置的要求而定。 |
   | `Visual Swatch` | 显示描述可配置产品的颜色、纹理或图案的色板。 A [可视色板](swatches.md) 可以使用十六进制颜色值填充，或者显示一个上传的图像，该图像表示选项的颜色、材质、纹理或图案。 |
   | `Text Swatch` | 经常用于表示大小的可配置产品选项的基于文本的表示形式。 [文本样本](swatches.md#text-based-swatches) 还可以包括十六进制颜色值。 |
   | `Page Builder` | 功能齐全的 [页面生成器](../page-builder/introduction.md) 位于属性位置的工作区，可轻松地将吸引人的内容添加到产品页面。 |

   {style="table-layout:auto"}

1. 如果要在客户购买产品之前需要选择选项，请设置 **[!UICONTROL Values Required]** 到 `Yes`.

1. 对象 [!UICONTROL Dropdown] 和 [!UICONTROL Multiple Select] 输入类型，请执行以下操作：

   - 下 _[!UICONTROL Manage Options]_，单击&#x200B;**[!UICONTROL Add Option]**.

   - 输入要显示在列表中的第一个值。

     您可以为管理员输入一个值，并为每个商店视图输入值的转换。 如果您只有一个商店视图，则只能输入管理员值，并且该值也用于店面。

   - 单击 **[!UICONTROL Add Option]** 并为要包含在列表中的每个选项重复上一步骤。

   - 选择 **[!UICONTROL Is Default]** 以使用选项作为默认值。

   ![产品属性 — 管理选项](./assets/product-attribute-add-values-colors.png){width="600" zoomable="yes"}

## 步骤2：描述高级属性（如果需要）

1. 输入唯一值 **[!UICONTROL Attribute Code]** 小写字符，不带空格。

   ![产品属性 — 高级属性](./assets/product-attribute-advanced-attribute-properties.png){width="600" zoomable="yes"}

   可用的选项取决于 _[!UICONTROL Catalog Input Type for Store Owner]_设置。

1. 设置 **[!UICONTROL Scope]** 以指示 [存储层级](../getting-started/websites-stores-views.md) 属性才能使用。

1. 如果要防止任何重复值输入，请设置 **[!UICONTROL Unique Value]** 到 `Yes`.

1. 对于输入值的输入类型，通过设置对输入到文本字段中的任何数据运行有效性测试 **[!UICONTROL Input Validation for Store Owner]** 字段应包含的数据类型。

   此字段不可用于具有选定值的输入类型。 该测试可以验证以下任一项：

   - `Decimal Number`
   - `Integer Number`
   - `Email`
   - `URL`
   - `Letters`
   - `Letters (a-z, A-Z) or Numbers (0-9)`

   ![输入验证](./assets/product-attribute-input-validation.png){width="400"}

1. 将此属性添加到 [产品列表](products-list.md)，将以下选项设置为 `Yes`.

   - **添加到列选项**  — 将属性作为列包含在 _[!UICONTROL Products]_列表。
   - **在筛选器选项中使用**  — 将过滤器控件添加到中的列标题 _[!UICONTROL Products]_列表。

## 步骤3：输入字段标签

1. 在左侧导航中，选择 **[!UICONTROL Manage Labels]**.

1. 输入 **[!UICONTROL Title]** 用作字段的标签。

   如果您的商店以不同的语言提供，则可以为每个视图输入已翻译的标题。

   ![产品属性 — 管理标题](./assets/product-attribute-add-manage-titles.png){width="600" zoomable="yes"}

## 步骤4：描述店面属性

1. 在左侧导航中，选择 **[!UICONTROL Storefront Properties]**.

   ![产品属性 — 店面属性](./assets/product-attribute-add-storefront-properties.png){width="600" zoomable="yes"}

   可用的选项取决于 _[!UICONTROL Catalog Input Type for Store Owner]_设置。

1. 如果属性可供搜索，请设置 **[!UICONTROL Use in Search]** 到 `Yes`.

   - 设置 **[!UICONTROL Search Weight]** 值以控制项目在搜索结果中的显示位置：1（最低重量）到10（最高重量）。

   - 设置 **[!UICONTROL Visible in Advanced Search]** 根据需要。 了解详情，请参阅 [高级搜索](search.md#advanced-search).

1. 要在产品比较中包含属性，请设置 **[!UICONTROL Comparable on Storefront]** 到 `Yes`.

1. 对于下拉列表、多选和价格字段，请执行以下操作：

   - 要在分层导航中将属性用作过滤器，请设置 **[!UICONTROL Use in Layered Navigation]** 到 `Yes`.

   - 要在搜索结果页面的分层导航中使用属性，请设置 **[!UICONTROL Use in Search Results Layered Navigation]** 到 `Yes`.

   - 对象 **[!UICONTROL Position]**&#x200B;中，输入一个数字以指示属性在分层导航块中的相对位置。

1. 要在价格规则中使用属性，请设置 **[!UICONTROL Use for Promo Rule Conditions]** 到 `Yes`.

1. 要允许使用HTML设置文本格式，请设置 **[!UICONTROL Allow HTML Tags on Frontend]** 到 `Yes`.

   此设置使WYSIWYG编辑器可用于字段。

1. 要在产品页面上包含属性，请设置 **[!UICONTROL Visible on Catalog Pages on Storefront]** 到 `Yes`.

1. 如果您的主题支持，请完成以下设置：

   - 要在产品列表中包括属性，请设置 **[!UICONTROL Used in Product Listing]** 到 `Yes`.

   - 要将属性用作产品清单的排序参数，请设置 **[!UICONTROL Used for Sorting in Product Listing]** 到 `Yes`.

1. 完成后，单击 **[!UICONTROL Save Attribute]**.

## 步骤5：将创建的属性分配给属性集

要在产品创建页面上显示的属性，请将其添加到特定属性集。

1. 完成之前的步骤后，转到 **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Attribute Set]**.

1. 在列表中选择所需的属性集，然后在编辑模式下将其打开。

1. 将创建的属性从 **[!UICONTROL Unassigned Attributes]** 列表到中的相应文件夹 **组** 列。

1. 完成后，单击 **[!UICONTROL Save]**.

## 可配置产品的属性

用作选项下拉列表的任何属性。 [可配置产品](product-create-configurable.md) 必须具有以下属性：

| 属性 | 值 |
|----------|------ |
| 商店所有者的目录输入类型 | 下拉列表 |
| 范围 | 全局 |

{style="table-layout:auto"}

## 删除属性

删除属性后，该属性会从任何相关的产品和属性集中删除。 系统属性是存储的核心功能的一部分，无法删除。

在删除属性之前，请确保该属性当前未被目录中的任何产品使用。 确定某个属性是否正在使用的一个简单方法是使用 [导出](../systems/data-export.md) 用于检查产品实体属性列表的工具。 如果属性未包含在列表中，则目录中的任何产品都不会使用该属性。

**_要删除属性，请执行以下操作：_**

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. 在列表中查找属性，并在编辑模式下打开。

1. 单击 **[!UICONTROL Delete Attribute]**.

   ![删除属性](./assets/attribute-delete.png){width="600" zoomable="yes"}

1. 提示确认时，单击 **[!UICONTROL OK]**.

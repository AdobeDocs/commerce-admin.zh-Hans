---
title: 创建和删除产品属性
description: 了解如何创建和删除产品属性，这些属性用于描述目录中产品的特定特征。
exl-id: fd0e5d5b-a917-4e55-8ec2-7ebb040d3d06
feature: Catalog Management, Products
source-git-commit: 3768fc8896dd353e5cc29b4fe82862d6653d6348
workflow-type: tm+mt
source-wordcount: '1189'
ht-degree: 0%

---

# 创建和删除产品属性

您可以在处理产品时或从&#x200B;_[!UICONTROL Product Attributes]_页面创建属性。 以下步骤显示如何从_[!UICONTROL Stores]_&#x200B;菜单创建属性。

## 步骤1：描述基本属性属性

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**。

1. 单击&#x200B;**[!UICONTROL Add New Attribute]**。

   ![新属性属性](./assets/attribute-properties.png){width="600" zoomable="yes"}

1. 对于&#x200B;**[!UICONTROL Default Label]**，请输入标识该属性的标签。

1. 要确定用于数据输入的输入控件的类型，请将&#x200B;**[!UICONTROL Catalog Input Type for Store Owner]**&#x200B;设置为以下项之一：

   | 属性 | 描述 |
   |--- |--- |
   | `Text Field` | 单行输入文本字段。 |
   | `Text Area` | 用于输入文本段落（如产品说明）的多行输入字段。 您可以使用WYSIWYG编辑器使用HTML标记设置文本格式，或直接在文本中输入标记。 |
   | `Text Editor` | 属性位置处具有完整功能的文本编辑器。 |
   | 日期 | 以[首选格式](attributes-input-types.md#date-and-time-options)和[时区](../getting-started/store-details.md#locale-options)显示日期值。 可以从列表或日历（ ![日历图标](../assets/icon-calendar.png) ）中选择日期值。 <br/><br/>**_注意：_**根据您的系统配置，_管理员&#x200B;_用户可以在字段中直接输入日期或从日历或列表中选择日期。 有关指定日期和时间值的信息，请参阅[日期和时间选项](attributes-input-types.md#date-and-time-options)。 |
   | `Yes/No` | 显示一个预定义选项为`Yes`和`No`的下拉列表。 |
   | `Dropdown` | 显示仅接受单个选择的值的下拉列表。 下拉列表输入类型是[可配置产品](product-create-configurable.md)的关键组件。 |
   | `Multiple Select` | 显示接受多个选择的值的下拉列表。 |
   | `Price` | 此输入类型用于创建除预定义属性之外的价格字段：价格、特殊价格、层价格和成本。 使用的货币由系统配置决定。 |
   | `Media Image` | 将额外的图像与产品相关联，例如产品徽标、护理说明或食品标签中的成分。 将媒体图像属性添加到产品的属性集时，它将与基本图像、小型图像和缩略图一起成为额外的图像类型。 媒体图像属性可以从[店面媒体浏览器](catalog-images-video.md#storefront-media-browser)中排除。 |
   | `Fixed Product Tax` | 允许您根据区域设置要求定义[FPT费率](../stores-purchase/fixed-product-tax.md)。 |
   | `Visual Swatch` | 显示描述可配置产品的颜色、纹理或图案的色板。 [可视色板](swatches.md)可以用十六进制颜色值填充，或显示代表选项的颜色、材质、纹理或图案的上传图像。 |
   | `Text Swatch` | 经常用于表示大小的可配置产品选项的基于文本的表示形式。 [文本样本](swatches.md#text-based-swatches)还可以包含十六进制颜色值。 |
   | `Page Builder` | 属性位置处的[页面生成器](../page-builder/introduction.md)工作区功能完善，可轻松将吸引人的内容添加到产品页面。 |

   {style="table-layout:auto"}

1. 如果要在客户购买产品之前需要选择选项，请将&#x200B;**[!UICONTROL Values Required]**&#x200B;设置为`Yes`。

1. 对于[!UICONTROL Dropdown]和[!UICONTROL Multiple Select]输入类型，请执行以下操作：

   - 在&#x200B;_[!UICONTROL Manage Options]_下，单击&#x200B;**[!UICONTROL Add Option]**。

   - 输入要显示在列表中的第一个值。

     您可以为管理员输入一个值，并为每个商店视图输入值的转换。 如果您只有一个商店视图，则只能输入管理员值，并且该值也用于店面。

   - 单击&#x200B;**[!UICONTROL Add Option]**&#x200B;并对要包含在列表中的每个选项重复上一步。

   - 选择&#x200B;**[!UICONTROL Is Default]**&#x200B;以使用该选项作为默认值。

   ![产品属性 — 管理选项](./assets/product-attribute-add-values-colors.png){width="600" zoomable="yes"}

## 步骤2：描述高级属性（如果需要）

1. 以小写字符输入唯一&#x200B;**[!UICONTROL Attribute Code]**，且不含空格。

   >[!NOTE]
   >
   >不建议在[!UICONTROL Attribute Code]字段中使用`type`值。 这可能会导致错误，因为`type`值已保留供系统使用。

   ![产品属性 — 高级属性](./assets/product-attribute-advanced-attribute-properties.png){width="600" zoomable="yes"}

   可用的选项取决于&#x200B;_[!UICONTROL Catalog Input Type for Store Owner]_设置。

1. 设置&#x200B;**[!UICONTROL Scope]**&#x200B;以指示[存储层次结构](../getting-started/websites-stores-views.md)中可以使用属性的位置。

1. 如果要防止任何重复值条目，请将&#x200B;**[!UICONTROL Unique Value]**&#x200B;设置为`Yes`。

1. 对于输入值的输入类型，通过将&#x200B;**[!UICONTROL Input Validation for Store Owner]**&#x200B;设置为字段应包含的数据类型，对输入到文本字段中的任何数据运行有效性测试。

   此字段不可用于具有选定值的输入类型。 该测试可以验证以下任一项：

   - `Decimal Number`
   - `Integer Number`
   - `Email`
   - `URL`
   - `Letters`
   - `Letters (a-z, A-Z) or Numbers (0-9)`

   ![输入验证](./assets/product-attribute-input-validation.png){width="400"}

1. 若要将此属性添加到[产品列表](products-list.md)，请将以下选项设置为`Yes`。

   - **添加到列选项** — 在&#x200B;_[!UICONTROL Products]_列表中包括属性作为列。
   - **在筛选器选项中使用** — 向&#x200B;_[!UICONTROL Products]_列表中的列标题添加筛选器控件。

## 步骤3：输入字段标签

1. 在左侧导航中，选择&#x200B;**[!UICONTROL Manage Labels]**。

1. 输入要用作字段标签的&#x200B;**[!UICONTROL Title]**。

   如果您的商店以不同的语言提供，则可以为每个视图输入已翻译的标题。

   ![产品属性 — 管理标题](./assets/product-attribute-add-manage-titles.png){width="600" zoomable="yes"}

## 步骤4：描述店面属性

1. 在左侧导航中，选择&#x200B;**[!UICONTROL Storefront Properties]**。

   ![产品属性 — 店面属性](./assets/product-attribute-add-storefront-properties.png){width="600" zoomable="yes"}

   可用的选项取决于&#x200B;_[!UICONTROL Catalog Input Type for Store Owner]_设置。

1. 如果属性可供搜索，请将&#x200B;**[!UICONTROL Use in Search]**&#x200B;设置为`Yes`。

   - 将&#x200B;**[!UICONTROL Search Weight]**&#x200B;值设置为控制该项在搜索结果中出现的位置： 1（最低权重）到10（最高权重）。

   - 根据需要设置&#x200B;**[!UICONTROL Visible in Advanced Search]**。 在[高级搜索](search.md#advanced-search)中了解详情。

1. 若要在产品比较中包含该属性，请将&#x200B;**[!UICONTROL Comparable on Storefront]**&#x200B;设置为`Yes`。

1. 对于下拉列表、多选和价格字段，请执行以下操作：

   - 若要在分层导航中将属性用作过滤器，请将&#x200B;**[!UICONTROL Use in Layered Navigation]**&#x200B;设置为`Yes`。

   - 要在搜索结果页面的分层导航中使用属性，请将&#x200B;**[!UICONTROL Use in Search Results Layered Navigation]**&#x200B;设置为`Yes`。

   - 对于&#x200B;**[!UICONTROL Position]**，输入一个数字以指示属性在分层导航块中的相对位置。

1. 要在价格规则中使用属性，请将&#x200B;**[!UICONTROL Use for Promo Rule Conditions]**&#x200B;设置为`Yes`。

1. 若要允许使用HTML格式化文本，请将&#x200B;**[!UICONTROL Allow HTML Tags on Frontend]**&#x200B;设置为`Yes`。

   此设置使WYSIWYG编辑器可用于字段。

1. 若要在产品页面上包含该属性，请将&#x200B;**[!UICONTROL Visible on Catalog Pages on Storefront]**&#x200B;设置为`Yes`。

1. 如果您的主题支持，请完成以下设置：

   - 若要在产品列表中包含该属性，请将&#x200B;**[!UICONTROL Used in Product Listing]**&#x200B;设置为`Yes`。

   - 要将属性用作产品清单的排序参数，请将&#x200B;**[!UICONTROL Used for Sorting in Product Listing]**&#x200B;设置为`Yes`。

1. 完成后，单击&#x200B;**[!UICONTROL Save Attribute]**。

## 步骤5：将创建的属性分配给属性集

要在产品创建页面上显示的属性，请将其添加到特定属性集。

1. 完成之前的步骤后，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Attribute Set]**。

1. 在列表中选择所需的属性集，然后在编辑模式下将其打开。

1. 将创建的属性从&#x200B;**[!UICONTROL Unassigned Attributes]**&#x200B;列表拖到&#x200B;**组**&#x200B;列中的相应文件夹。

1. 完成后，单击&#x200B;**[!UICONTROL Save]**。

## 可配置产品的属性

任何用作[可配置产品](product-create-configurable.md)的选项下拉列表的属性都必须具有以下属性：

| 属性 | 值 |
|----------|------ |
| 商店所有者的目录输入类型 | 下拉列表 |
| 范围 | 全局 |

{style="table-layout:auto"}

## 删除属性

删除属性后，该属性会从任何相关的产品和属性集中删除。 系统属性是存储的核心功能的一部分，无法删除。

在删除属性之前，请确保该属性当前未被目录中的任何产品使用。 确定属性是否正在使用的一个简单方法是使用[导出](../systems/data-export.md)工具检查产品实体属性的列表。 如果属性未包含在列表中，则目录中的任何产品都不会使用该属性。

**_要删除属性：_**

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**。

1. 在列表中查找属性，并在编辑模式下打开。

1. 单击&#x200B;**[!UICONTROL Delete Attribute]**。

   ![删除属性](./assets/attribute-delete.png){width="600" zoomable="yes"}

1. 提示确认时，单击&#x200B;**[!UICONTROL OK]**。

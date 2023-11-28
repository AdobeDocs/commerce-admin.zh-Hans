---
title: 将属性添加到产品
description: 了解如何将属性添加到目录中的产品。
exl-id: 1f92807a-2362-48a2-8d3a-4aef90a5671f
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '737'
ht-degree: 0%

---

# 将属性添加到产品

虽然属性主要通过 [商店](../stores-purchase/stores-menu.md) 菜单，您还可以添加新属性 _正在运行_ 处理产品时。 您可以从现有属性列表中进行选择或创建属性。 新属性将添加到 [属性集](../catalog/attribute-sets.md) 产品所基于的对象。

## 步骤1：添加属性

1. 在编辑模式下打开产品。

1. 在右上角，单击 **[!UICONTROL Add Attribute]**.

   ![具有默认属性集的新产品](./assets/product-attribute-add.png){width="600" zoomable="yes"}

1. 要向产品添加现有属性，请使用 [筛选器控件](../getting-started/admin-grid-controls.md) 在网格中查找属性并执行以下操作：

   - 选中要添加的每个属性的第一列中的复选框。

   - 单击 **[!UICONTROL Add Selected]**.

   ![选择属性](./assets/product-attribute-add-select.png){width="600" zoomable="yes"}

1. 要定义新属性，请单击 **[!UICONTROL Create New Attribute]** 并完成步骤2中的项目。

## 步骤2：描述基本属性属性

![属性属性](./assets/product-attribute-add-new.png){width="600" zoomable="yes"}

1. 下 _[!UICONTROL Attribute Properties]_，输入&#x200B;**[!UICONTROL Attribute Label]**以标识属性。

1. 设置 **[!UICONTROL Catalog Input Type for Store Owner]** 到类型 [输入控制](attributes-input-types.md) 用于数据输入。

   如果属性用于 [可配置产品](product-create-configurable.md)，选择 `Dropdown`. 然后，设置 **[!UICONTROL Required]** 到 `Yes`.

1. 对象 `Dropdown` 和 `Multiple Select` 输入类型，请执行以下操作：

   - 下 **[!UICONTROL Values]**，单击 **[!UICONTROL Add Value]**.

   - 输入要显示在列表中的第一个值。

     您可以为管理员输入一个值，并为每个商店视图输入值的转换。 如果您只有一个商店视图，则只能输入管理员值，并且该值也用于店面。

   - 单击 **[!UICONTROL Add Value]** 并为要包含在列表中的每个选项重复上一步骤。

   - 选择 **[!UICONTROL Is Default]** 以使用选项作为默认值。

   ![值](./assets/product-attribute-add-values-colors.png){width="600" zoomable="yes"}

1. 如果您需要客户在购买产品之前选择一个选项，请设置 **[!UICONTROL Required]** 到 `Yes`.

## 步骤3：描述高级属性（可选）

![高级属性属性](./assets/product-attribute-advanced-attribute-properties.png){width="600" zoomable="yes"}

1. 输入唯一值 **[!UICONTROL Attribute Code]** 小写字符，不带空格。

1. 设置 **[!UICONTROL Scope]** 以指示在商店层次结构中可以使用属性的位置。

   如果属性用于 [可配置产品](product-create-configurable.md)，选择 `Global`.

1. 如果此属性仅适用于此产品，请设置 **[!UICONTROL Unique Value]** 到 `Yes`.

1. 要对输入到文本字段中的任何数据运行有效性测试，请设置 **[!UICONTROL Input Validation for Store Owner]** 字段应包含的数据类型。

   此字段不可用于具有选定值的输入类型。 输入验证可用于以下任意内容：

   - `Decimal Number`
   - `Integer Number`
   - `Email`
   - `URL`
   - `Letters`
   - `Letters (a-z, A-Z) or Numbers (0-9)`

   ![输入验证](./assets/product-attribute-input-validation.png){width="500"}

1. 如果您希望能够将属性作为列包含在Products网格中，请设置 **[!UICONTROL Add to Column Options]** 到 `Yes`.

1. 如果您希望能够过滤 _[!UICONTROL Products]_按此列网格，设置&#x200B;**[!UICONTROL Use in Filter Options]**到 `Yes`.

## 步骤4：输入字段标签

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Manage titles]** 部分。

1. 输入 **[!UICONTROL Title]** 用作字段的标签。

   如果您的商店以不同的语言提供，则可以为每个视图输入已翻译的标题。

   ![管理标题](./assets/product-attribute-add-manage-titles.png){width="600" zoomable="yes"}

## 步骤5：描述店面属性

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Storefront Properties]** 部分。

   ![店面属性](./assets/product-attribute-add-storefront-properties.png){width="600" zoomable="yes"}

1. 要使属性可用于搜索，请设置 **[!UICONTROL Use in Search]** 到 `Yes`.

1. 要在产品比较中包含属性，请设置 **[!UICONTROL Comparable on Storefront]** 到 `Yes`.

1. 要在分层导航中包含下拉列表、多选或价格属性，请设置 **[!UICONTROL Use in Search Results Layered Navigation]** 更改为以下任一项：

   - `Filterable (with results)`  — 分层导航仅包括那些可找到匹配产品的过滤器。 任何已应用于列表中显示的所有产品的属性值都不会显示为可用过滤器。 可用过滤器列表中还会忽略计数为零(0)的产品匹配的属性值。<br/><br/>产品过滤列表仅包含与过滤器匹配的产品。 仅当选定的过滤器更改了显示的内容时，才会更新产品列表。

   - `Filterable (no results)`  — 分层导航包括所有可用属性值及其产品数的过滤器，其中包括产品匹配为零(0)的产品。 如果属性值是样本，则该值将显示为过滤器，但会被划掉。

1. 要在搜索结果页面上的分层导航中使用，请设置 **[!UICONTROL Use in Search Results Navigation]** 到 `Yes` 并在 **[!UICONTROL Position]** 字段。

   位置编号表示属性在分层导航块中的相对位置。

1. 要在价格规则中使用属性，请设置 **[!UICONTROL Use for Promo Rule Conditions]** 到 `Yes`.

1. 要允许使用HTML设置文本格式，请设置 **[!UICONTROL Allow HTML Tags on Storefront]** 到 `Yes`.

   此设置使WYSIWYG编辑器在编辑字段时可用。

1. 要在产品页面上包含属性，请设置 **[!UICONTROL Visible on Catalog Pages on Storefront]** 到 `Yes`.

1. 按照主题的支持，完成以下设置：

   - 要在产品列表中包括属性，请设置 **[!UICONTROL Used in Product Listing]** 到 `Yes`.

   - 要将属性用作产品清单的排序参数，请设置 **[!UICONTROL Used for Sorting in Product Listing]** 到 `Yes`.

1. 完成后，单击 **[!UICONTROL Save Attribute]**.

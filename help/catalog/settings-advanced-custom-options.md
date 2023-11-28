---
title: 产品设置 —  [!UICONTROL Customizable Options]
description: 对于产品， [!UICONTROL Customizable Options] 通过设置，您可以提供一系列包含文本、选择和日期输入类型的选项。
exl-id: 7d23c5c5-2b2a-4f2a-b843-9c27b851be5f
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '811'
ht-degree: 0%

---

# 产品设置 —  [!UICONTROL Customizable Options]

向产品添加可自定义选项是一种提供选项选项的简单方法，这些选项包含文本、选择和日期输入类型。 如果您的库存需求非常简单，可定制选项就是一个很好的解决方案。 但是，因为它们基于单个SKU的变体，所以不能用于管理库存或作为价格规则条件的基础。 如果您有多个具有相同选项的产品，则可以设置一个产品并将选项导入其他产品。

当客户购买带有可自定义选项的产品时，每个选定选项的描述都会显示在产品描述下方，并且任何关联的加价（或标记）都会自动应用于项目的价格。

![带有可自定义选项的产品详细信息](./assets/storefront-customizable-option-product-detail.png){width="700" zoomable="yes"}

如果购买触发了购物车价格规则，则初始计算将首先应用于产品价格，然后应用于行项目价格，并对适用的可自定义选项进行任何调整。 在下面的示例中，客户以74.00美元的价格购买了一个饺子包，另外还购买了一个可定制的单字母选项。 产品基本价格加价为14.80美元，调整后的价格为88.80美元。在这种情况下，购买饺子包会触发基于产品SKU的购物车价格规则，并对购买应用折扣，外加免运费。 尽管可自定义选项未触发购物车价格规则，但它会将折扣应用于购物车内容，其中包括可自定义选项的标记。

![带有可自定义选项和价格规则的购物车](./assets/storefront-customizable-option-cart-price-rule.png){width="700" zoomable="yes"}

>[!NOTE]
>
>目录价格规则折扣不适用于固定价格可自定义选项。

## 创建可自定义的选项

1. 在编辑模式下打开产品。

1. 向下滚动并展开 ![扩展选择器](../assets/icon-display-expand.png) 该 _[!UICONTROL Customizable Options]_部分。

1. 单击 **[!UICONTROL Add Option]**.

   ![可自定义的选项](./assets/product-customizable-options.png){width="600" zoomable="yes"}

1. 完成新的选项设置：

   - 对象 **[!UICONTROL Option Title]**，输入选项的名称。

   - 设置 **[!UICONTROL Option Type]** 作为数据输入的类型。

   - 如果购买产品不需要此选项，请取消选择 **[!UICONTROL Required]** 复选框。

1. 根据数据输入类型填写字段：

   - 对象 **[!UICONTROL Title]**，输入此选项的名称。

   - （可选）对于 **[!UICONTROL Price]**，输入适用于此选项的基本产品价格的任何加价或减价。

   - 设置 **[!UICONTROL Price Type]** 更改为以下任一项：

      - `Fixed`  — 变体的价格与基础产品的价格不同，不同的是固定货币金额，如$1。
      - `Percentage`  — 变化价格与基本产品价格之间有百分比差异，例如10%。

   - （可选）输入 **[!UICONTROL SKU]** 用于选项。 选项SKU是添加到产品SKU的后缀。

   - 如果 _[!UICONTROL Option Type]_是 `File`，设置文件的参数。 对象&#x200B;**[!UICONTROL Compatible File Extensions]**，请输入有效的扩展名作为逗号分隔值(例如 `png, jpg, gif`)。 对象&#x200B;**[!UICONTROL Maximum Image Size]**，输入最大图像大小（以像素为单位）。 如果是文本条目，请输入最大值&#x200B;**[!UICONTROL Maximum Characters]**.

   ![为自定义选项添加值](./assets/product-customizable-options-add-values.png){width="600" zoomable="yes"}

1. （可选）如果要添加其他可自定义选项，请单击 **[!UICONTROL Add Option]**.

   - 像之前一样完成设置。

   - 要更改选项的顺序，请单击 _[!UICONTROL Order]_![“排序顺序”图标](../assets/icon-sort-order.png) 图标并将选项拖动到列表中的新位置。

   对每个要添加的选项重复此步骤。

1. 完成后，单击 **[!UICONTROL Save]**.

## 导入可自定义的选项

1. 在 _可自定义的选项_ 部分，单击 **[!UICONTROL Import Options]**.


1. 所有带有可自定义选项的产品都会显示在网格中。

1. 在列表中，选中包含要导入的选项的产品复选框。

1. 单击 **[!UICONTROL Import]**.

1. 完成后，您可以继续添加更多自定义选项或单击 **[!UICONTROL Save and Close]**.

## 输入类型

| 类型 | 描述 |
|---------------------|---------------|
| [!UICONTROL Text] | 客户可在其中输入所需信息的输入行或文本框。 选项：<br />**[!UICONTROL Field]**— 单行输入文本字段。<br />**[!UICONTROL Area]**  — 多行输入字段。 此类型不支持HTML等高级格式。 使用最大字符数限制可输入的文本长度，并确保在管理员中输入的文本有正确的表示形式。 |
| [!UICONTROL File] | 允许客户上传文件。 |
| [!UICONTROL Select] | 允许客户根据使用的输入类型选择单个选项或多个选项。 选项：<br />**[!UICONTROL Drop-down]**— 仅允许一个选择的选项下拉列表。<br />**[!UICONTROL Radio Buttons]**  — 一组仅允许进行一项选择的选项。<br />**[!UICONTROL Checkbox]**— 复选框是是/否选项的变体。 如果产品有多个复选框，则可以进行多个选择。<br />**[!UICONTROL Multiple Select]**  — 一个下拉列表框，其中包含接受多个选择的选项。 要选择多个选项，请按住Ctrl (PC)或Command (Mac)键并单击每个选项。 |
| [!UICONTROL Date] | 允许客户输入日期或时间，或从日历中选择值。 选项： <br />**[!UICONTROL Date]**— 日期值的输入字段。 可以直接在字段中键入日期或从列表或日历中选择日期。 输入方法和格式由 [日期和时间选项](attributes-input-types.md#date-and-time-options) 配置。<br />**[!UICONTROL Date & Time]**  — 日期和时间值的输入字段。<br />**[!UICONTROL Time]**— 时间值的输入字段。 |

{style="table-layout:auto"}

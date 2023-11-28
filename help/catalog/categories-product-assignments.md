---
title: 类别产品分配
description: 了解如何使用 [!UICONTROL Products in Category] 用于控制当前将哪些产品分配给类别的设置。
exl-id: e7ab11c0-2d55-4824-a397-a1c858344d4f
feature: Catalog Management, Categories, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '809'
ht-degree: 0%

---

# 类别产品分配

对于类别，请使用 _[!UICONTROL Products in Category]_部分，以查看当前分配给该类别的产品。 每列顶部的搜索过滤器用于在类别中添加和删除产品。 您还可以使用 [类别规则](../merchandising-promotions/category-product-rules.md) ( ![Adobe Commerce](../assets/adobe-logo.svg) 仅限Adobe Commerce)，以便在满足一组条件时动态更改产品选择。 要了解更多信息，请参阅 [Visual Merchandiser](../merchandising-promotions/visual-merchandiser.md))。

>[!TIP]
>
>在类别规则设置过程中，产品包括 _已排序_， _匹配_， _已指定_、和 _已取消分配_ 根据那个规则 **_仅限_** 保存此类别时。 要确保在将新产品添加到目录时根据规则分配该产品，您可以 **必须重新保存每个类别** 设置为按规则匹配产品。 此外，如果任何产品库存状态更改为 `In Stock` 或 `Out of Stock` 类别中的产品包括 _已排序_ 根据 **自动排序** 规则，您必须单击 **[!UICONTROL Save Category]**.

![类别产品](./assets/category-products-in-category.png){width="600" zoomable="yes"}

>[!NOTE]
>
>在类别页面上， `Out of stock` 始终显示产品 **_之后_** `In Stock` 产品列表上所有排序类型的产品。

>[!NOTE]
>
>此 _Stock_ 列显示的可销售产品数量 _**选定的类别范围**_ 仅限。 当为产品管理多个库存时，您应在相应的范围之间切换以显示其他 _Stock_ 中的列值 _类别产品_ 网格。

## 应用类别规则

{{ee-feature}}

1. 设置 **[!UICONTROL Match products by rule]** 到 `Yes`.

   此时会显示自动排序和条件选项。

   ![按规则匹配产品](./assets/category-match-products-by-rule.png){width="600" zoomable="yes"}

1. 设置 **[!UICONTROL Automatic Sorting]** 顺序。

   此自动排序基于当前条件。

   - `Stock level`  — 移至顶部或底部。
   - `Special price`  — 移至顶部或底部。
   - `New Products`  — 首先列出最新产品。
   - `Color`  — 按颜色的字母顺序排序。
   - `Name`  — 按名称以升序或降序排序。
   - `SKU`  — 按SKU按升序或降序排序
   - `Price`  — 按价格升序或降序排序。

1. 单击 **[!UICONTROL Add Condition]** 并执行以下操作：

   - 选择 **[!UICONTROL Attribute]** 这就是条件的基本所在。
   - 选择 **[!UICONTROL Operator]** 是构成表达式所必需的。
   - 输入 **[!UICONTROL Value]** 这就对了。

   ![将条件添加到类别规则](./assets/category-rule-create.png){width="600" zoomable="yes"}

   对每个要用于描述要满足的条件的属性重复此过程。 例如，要匹配在7到30天前创建的产品，请执行以下操作：

   - 设置 **[!UICONTROL Date Created]** 到 `Less than 30`.
   - 设置 **[!UICONTROL Logic]** 到 `AND`.
   - 设置 **[!UICONTROL Date Modified]** 到 `Greater than 7`.

1. 完成后，单击 **[!UICONTROL Save Category]**.

### 页面选项

| 选项 | 描述 |
|--- |--- |
| [!UICONTROL Match products by rule] | 确定类别中的产品列表是否由类别规则动态生成。 选项： `Yes` / `No` |
| [!UICONTROL Automatic Sorting] | 自动将排序顺序应用于类别产品列表。 选项： <br/>`None`<br/>`Move low stock to top`<br/>`Move low stock to bottom`<br/>`Special price to top`<br/>`Special price to bottom`<br/>`Newest products first`<br/>`Sort by color`<br/>`Name: A - Z`<br/>`Name: Z - A`<br/>`SKU: Ascending`<br/>`SKU: Descending`<br/>`Price: High to Low`<br/>`Price: Low to High` |
| [!UICONTROL Add Condition] | 向规则添加另一个条件。 |

{style="table-layout:auto"}

### 页面完成情况

| 选项 | 描述 |
|--- |--- |
| [!UICONTROL Attribute] | 确定用作条件基础的属性。 选项： <br/>**[!UICONTROL Clone Category ID(s)]**— 根据类别ID从多个类别中动态克隆产品，而无需对产品进行排序和排序。<br/>**[!UICONTROL Color]**  — 包括基于颜色的产品。 <br/>**[!UICONTROL Date Created (days ago)]**— 包含基于产品添加到目录后天数的产品。<br/>**[!UICONTROL Date Modified (days ago)]**  — 包括基于上次修改产品后天数的产品。 <br/>**[!UICONTROL Name]**— 包括基于产品名称的产品。<br/>**[!UICONTROL Price]**  — 包括基于价格的产品。 <br/>**[!UICONTROL Quantity]**— 包括基于库存数量的产品。<br/>** SKU **— 包括基于SKU的产品。 |
| [!UICONTROL Operator] | 指定应用于属性值以满足条件的运算符。 除非指定了运算符， `Equal` 用作默认值。 选项： `Equal` / `Not equal` / `Greater than` / `Greater than or equal to` / `Less than` / `Less than or equal to` / `Contains` |
| [!UICONTROL Value] | 指定属性必须符合条件的值。 |
| [!UICONTROL Logic] | 用于定义多个条件，仅在添加另一个条件时显示。 选项： `OR` / `AND` |

{style="table-layout:auto"}

>[!NOTE]
>
>通过组合所有可销售的子产品数量来计算带有子选项的可配置产品的数量。 考虑可配置产品的示例 _耐力健身背心_ 紫色、红色和黄色选项，以及每种颜色的不同数量。 在此方案中，父产品数量是紫色、红色和黄色子产品的组合可销售数量。

## 控件


## 页面控件

{{ee-feature}}

| 控件 | 描述 |
|----------|--------------|
| ![列表查看](../assets/icon-view-list.png) | 列表查看 |
| ![以图块查看](../assets/icon-view-tiles.png) | 以图块查看 |
| ![切换否](../assets/toggle-no.png) | 按规则匹配 — 否 |
| ![切换是](../assets/toggle-yes.png) | 按规则匹配 — 是 |
| ![移动控制器](../assets/icon-move.png) | 使用拖放控件，可获取产品并将其移动到网格当前页面中的另一个位置。 要了解更多信息，请参阅 [Visual Merchandiser](../merchandising-promotions/visual-merchandiser.md). |
| ![位置控制器](../assets/control-position.png) | 确定产品在列表中的位置。 |

{style="table-layout:auto"}

## 页面控件

{{ce-feature}}

| 控件 | 描述 |
|----------|--------------|
| ![已选中复选框](../assets/checkbox-selected.png) | 使用第一列标题中的复选框可选择所有产品或清除所有选择。 第一行中的控件确定搜索类型，可以设置为包括任何记录，或者仅包括已分配或未分配给类别的记录。 每行第一列中的复选框用于标识要添加到类别的产品。 选项： `Yes` / `No` / `Any` |
| [!UICONTROL Search Filters] | 每列顶部的过滤器控件可用于输入要在列表中包括或忽略的特定值，具体取决于“全选”设置。 |
| [!UICONTROL Reset Filter] | 清除所有搜索过滤器。 |
| [!UICONTROL Search] | 根据筛选条件搜索目录并显示结果。 |

{style="table-layout:auto"}

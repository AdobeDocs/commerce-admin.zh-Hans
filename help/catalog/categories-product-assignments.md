---
title: 类别产品分配
description: 了解如何使用[!UICONTROL Products in Category]设置来控制当前分配给该类别的产品。
exl-id: e7ab11c0-2d55-4824-a397-a1c858344d4f
feature: Catalog Management, Categories, Products
source-git-commit: 5aea3aa13ab0eb74866fc0cbcbfe08b5099abe95
workflow-type: tm+mt
source-wordcount: '791'
ht-degree: 0%

---

# 类别产品分配

对于类别，请使用&#x200B;_[!UICONTROL Products in Category]_&#x200B;部分查看当前分配给该类别的产品。 每列顶部的搜索过滤器用于在类别中添加和删除产品。 您还可以使用[类别规则](../merchandising-promotions/category-product-rules.md)(仅限![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce)在满足一组条件时动态更改产品选择。 若要了解详细信息，请参阅[可视化促销器](../merchandising-promotions/visual-merchandiser.md)。

>[!TIP]
>
>在类别规则设置期间，当保存此类别时，产品为&#x200B;_已排序_、_匹配_、_已分配_&#x200B;和&#x200B;_已取消分配_（仅根据此规则&#x200B;**__**）。 要确保在将新产品添加到目录时根据规则分配该产品，您&#x200B;**必须重新保存设置为按规则匹配产品的每个类别**。 此外，如果任何产品库存状态更改为`In Stock`或`Out of Stock`，并且类别中的产品按照&#x200B;_自动排序_&#x200B;规则&#x200B;**排序**，则必须单击&#x200B;**[!UICONTROL Save Category]**。

![类别产品](./assets/category-products-in-category.png){width="600" zoomable="yes"}

>[!NOTE]
>
>_Stock_&#x200B;列仅显示&#x200B;_&#x200B;**选定类别范围**&#x200B;_&#x200B;的可用产品数量。 为产品管理多个库存时，您应在相应的范围之间切换以在&#x200B;_类别产品_&#x200B;网格中显示其他&#x200B;_库存_&#x200B;列值。

## 应用类别规则

{{ee-feature}}

1. 将&#x200B;**[!UICONTROL Match products by rule]**&#x200B;设置为`Yes`。

   此时会显示自动排序和条件选项。

   ![按规则匹配产品](./assets/category-match-products-by-rule.png){width="600" zoomable="yes"}

1. 设置&#x200B;**[!UICONTROL Automatic Sorting]**&#x200B;顺序。

   此自动排序基于当前条件。

   - `Stock level` — 移至顶部或底部。
   - `Special price` — 移至顶部或底部。
   - `New Products` — 首先列出最新产品。
   - `Color` — 按颜色的字母顺序排序。
   - `Name` — 按名称以升序或降序排序。
   - `SKU` — 按SKU以升序或降序排序
   - `Price` — 按价格升序或降序排序。

1. 单击&#x200B;**[!UICONTROL Add Condition]**&#x200B;并执行以下操作：

   - 选择作为条件基础的&#x200B;**[!UICONTROL Attribute]**。
   - 选择构成表达式所需的&#x200B;**[!UICONTROL Operator]**。
   - 输入要匹配的&#x200B;**[!UICONTROL Value]**。

   ![将条件添加到类别规则](./assets/category-rule-create.png){width="600" zoomable="yes"}

   对每个要用于描述要满足的条件的属性重复此过程。 例如，要匹配在7到30天前创建的产品，请执行以下操作：

   - 将&#x200B;**[!UICONTROL Date Created]**&#x200B;设置为`Less than 30`。
   - 将&#x200B;**[!UICONTROL Logic]**&#x200B;设置为`AND`。
   - 将&#x200B;**[!UICONTROL Date Modified]**&#x200B;设置为`Greater than 7`。

1. 完成后，单击&#x200B;**[!UICONTROL Save Category]**。

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
| [!UICONTROL Attribute] | 确定用作条件基础的属性。 选项： <br/>**[!UICONTROL Clone Category ID(s)]**— 根据类别ID从多个类别中动态克隆产品，而不对其排序和排序。<br/>**[!UICONTROL Color]** — 包含基于颜色的产品。 <br/>**[!UICONTROL Date Created (days ago)]**— 包含基于产品添加到目录后天数的产品。<br/>**[!UICONTROL Date Modified (days ago)]** — 包括基于上次修改产品后天数的产品。 <br/>**[!UICONTROL Name]**— 包含基于产品名称的产品。<br/>**[!UICONTROL Price]** — 包括基于价格的产品。 <br/>**[!UICONTROL Quantity]**— 包括基于库存数量的产品。<br/>**&#x200B; SKU &#x200B;**— 包含基于SKU的产品。 |
| [!UICONTROL Operator] | 指定应用于属性值以满足条件的运算符。 除非指定运算符，否则默认使用`Equal`。 选项： `Equal` / `Not equal` / `Greater than` / `Greater than or equal to` / `Less than` / `Less than or equal to` / `Contains` |
| [!UICONTROL Value] | 指定属性必须符合条件的值。 |
| [!UICONTROL Logic] | 用于定义多个条件，仅在添加另一个条件时显示。 选项： `OR` / `AND` |

{style="table-layout:auto"}

>[!NOTE]
>
>可通过组合所有子产品数量来计算带有子选项的可配置产品的数量。 以可配置产品&#x200B;_耐用健身背心_&#x200B;为例，其颜色选项为紫色、红色和黄色，且每种颜色的颜色数量不同。 在此方案中，父产品数量是紫色、红色和黄色子产品的组合数量。

## 控件


## 页面控件

{{ee-feature}}

| 控件 | 描述 |
|----------|--------------|
| ![列表查看](../assets/icon-view-list.png) | 列表查看 |
| ![以图块查看](../assets/icon-view-tiles.png) | 以图块查看 |
| ![切换否](../assets/toggle-no.png) | 按规则匹配 — 否 |
| ![切换是](../assets/toggle-yes.png) | 按规则匹配 — 是 |
| ![移动控制器](../assets/icon-move.png) | 使用拖放控件，可获取产品并将其移动到网格当前页面中的另一个位置。 若要了解详细信息，请参阅[可视化促销器](../merchandising-promotions/visual-merchandiser.md)。 |
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

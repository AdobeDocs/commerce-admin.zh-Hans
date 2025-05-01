---
title: 促销的类别规则
description: 了解如何创建规则以根据一组条件动态更改产品选择。
exl-id: 765b863a-bb83-418b-9fca-ef0a148b09eb
feature: Categories, Merchandising
badgePaas: label="仅限PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="仅适用于云项目(Adobe管理的PaaS基础架构)和内部部署项目上的Adobe Commerce 。"
source-git-commit: 6d782e3aafa7460a0e0d5ca07a2bde2ae371a9ea
workflow-type: tm+mt
source-wordcount: '1098'
ht-degree: 0%

---

# 促销的类别规则

{{ee-feature}}

类别规则根据一组条件动态地更改产品选择。 每个类别只能有一个类别规则，但单个规则可以有多个条件。 例如，您可以为特定品牌创建类别规则。 即使未将同一品牌的产品分配到同一类别，这些产品也会自动添加到列表中。 您可以根据需要向表达式添加任意数量的条件，以描述要包含的产品。

>[!TIP]
>
>在类别规则设置期间，当保存此类别时，产品为&#x200B;_已排序_、_匹配_、_已分配_&#x200B;和&#x200B;_已取消分配_（仅根据此规则&#x200B;**__**）。 例如，如果您将产品添加到目录并且要根据规则分配产品，则&#x200B;**必须重新保存每个设置为按规则匹配产品的类别**。 此外，如果任何产品库存状态更改为`In Stock`或`Out of Stock`，并且类别中的产品应根据&#x200B;**[!UICONTROL Automatic Sorting]**&#x200B;规则进行&#x200B;_排序_，则必须单击&#x200B;**[!UICONTROL Save Category]**。

每个条件都由一个属性、值和逻辑运算符组成。 只有属性设置为`Yes`的&#x200B;_[[!UICONTROL Use in Product Listing]](../catalog/attribute-product-create.md)_属性才能在类别规则中使用。 如果要使用产品列表中未包括的属性，则必须为属性设置此属性。 尽管不支持日期属性，但您可以使用“创建日期”或“修改日期”属性来定义日期或日期范围。 例如，要仅包括上周创建的产品，请将“创建日期”设置为值`<7`。

>[!NOTE]
>
>确保将规则中使用的每个属性配置为&#x200B;[_smart_&#x200B;属性](smart-attributes-configure.md)。

![类别产品规则](../catalog/assets/category-product-rule-with-stock.png){width="600" zoomable="yes"}

类别产品规则可以根据确定哪些产品出现在类别中的条件，加快将特定产品分配给类别的过程。 在[Visual Merchandiser](visual-merchandiser.md)配置中指定了可与类别产品规则一起使用的“智能”属性。

>[!NOTE]
>
>应用类别产品规则时请务必谨慎，因为任何不符合条件的产品都会从类别中删除。 例如，如果创建的规则仅包含紫色油箱顶部，则所有其他油箱顶部都将从类别中删除。

## 步骤1：配置&#x200B;_smart_&#x200B;属性

1. 对于规则中要使用的每个属性，确保[[!UICONTROL Use in Product Listing]](../catalog/product-attributes.md)店面属性设置为`Yes`。

   >[!NOTE]
   >
   >确保您选择的属性不是多选&#x200B;_[!UICONTROL Input Type]_。

1. 完成[配置](smart-attributes-configure.md)以标识要与Visual Merchandiser一起使用的每个&#x200B;_smart_&#x200B;属性。

## 第2步：创建类别规则

1. 在类别树中，打开要编辑的类别。

1. 在&#x200B;**[!UICONTROL Products in Category]**&#x200B;部分中，将&#x200B;**[!UICONTROL Match products by rule]**&#x200B;设置为`Yes`。

   此时会显示自动排序和条件选项。

1. 单击&#x200B;**[!UICONTROL Add Condition]**。

1. 选择作为条件基础的&#x200B;**[!UICONTROL Attribute]**。

1. 将&#x200B;**[!UICONTROL Operator]**&#x200B;设置为以下项之一：

   - `Equal`
   - `Not equal`
   - `Greater than`
   - `Greater than or equal to`
   - `Less than`
   - `Less than or equal to`
   - `Contains`

1. 输入要匹配的&#x200B;**[!UICONTROL Value]**。

   ![将条件添加到类别规则](../catalog/assets/category-rule-create.png){width="500"}

1. 对描述要满足的条件所需的每个属性重复此过程。

   例如，要匹配七天到30天前创建的产品，请执行以下操作：

   - 将&#x200B;**[!UICONTROL Date Created]**&#x200B;设置为`Less than 30`。

   - 将&#x200B;**[!UICONTROL Logic]**&#x200B;设置为`AND`。

     >[!NOTE]
     >
     >选择`AND`时，该规则将应用于满足所有条件的产品。 选择`OR`后，它将适用于至少满足一个条件的产品。

   - 将&#x200B;**[!UICONTROL Date Modified]**&#x200B;设置为`Greater than 7`。

1. 若要自动将排序顺序应用到动态生成的产品列表，请设置&#x200B;**[!UICONTROL Automatic Sorting]**。

   ![自动排序](./assets/automatic-sorting-field.png){width="600" zoomable="yes"}

   排序顺序选项是全局定义的，并根据当前条件应用。 无法为网站、商店或商店视图级别设置不同的排序顺序。

   | 排序选项 | 描述 |
   |-----------| -----------|
   | [!UICONTROL Stock quantity] | 根据股票排序，从顶部或底部： `Move low stock to top`或`Move out of stock to bottom` |
   | [!UICONTROL Special price] | 根据价格排序，从顶部或底部： `Special price to top`或`Special price to bottom` |
   | [!UICONTROL New Products] | 列出最新产品： `Newest products first` |
   | [!UICONTROL Color] | 按颜色的字母顺序排序： `Sort by color` |
   | [!UICONTROL Product Names] | 按名称升序或降序排序： `Name A - Z`或`Name Z -A` |
   | [!UICONTROL SKU] | 按SKU升序或降序排序：`SKU: Ascending`或`SKU: Descending` |
   | [!UICONTROL Price] | 按价格升序或降序排序：`Price: High to low`或`Price: Low to high` |

   {style="table-layout:auto"}

1. 完成后，单击&#x200B;**[!UICONTROL Save Category]**。

>[!NOTE]
>
>设置类别规则时，在保存类别时会匹配产品并将其分配给规则。 如果将产品添加到目录并希望将其包含在规则中，则必须重新保存设置为按规则匹配产品的每个类别。 这样可以确保包含新产品。

### 菜单选项

- **[!UICONTROL Match products by rule]** — 确定类别中的产品列表是否由类别规则动态生成。 选项： `Yes` / `No`

- **[!UICONTROL Automatic Sorting]** — 自动将排序顺序应用于类别产品列表。 选项： `None`、`Move low stock to top`、`Move low stock to bottom`、`Special price to top`、`Special price to bottom`、`Newest products first`、`Sort by color`、`Name: A - Z`、`Name: Z - A`、`SKU: Ascending`、`SKU: Descending`、`Price: High to Low`和`Price: Low to High`

  >[!NOTE]
  >
  >如果您有一个带子产品的可配置产品，则父产品库存会根据子产品库存的总和来计算。 考虑一个示例，您在此示例中可配置产品&#x200B;_Proteus Fitness Shirt_，该产品具有橙色、红色和黄色子产品，每种子产品的库存量不同。 父产品库存基于橙色、红色和黄色子产品的库存合计计算。 使用`Move low stock to top`选项，它通过组合其所有可销售子产品库存来计算父产品的库存，并相应地对其进行排序。

- **[!UICONTROL Add Condition]** — 向规则添加另一个条件。

- **[!UICONTROL Attribute]** — 确定用作条件基础的属性。 选项：

  | 选项 | 描述 |
  | ------ | ----------- |
  | `Clone Category ID(s)` | 根据类别ID从多个类别中动态克隆产品，而无需对产品进行排序和排序。 |
  | `Color` | 包括基于颜色的产品。 |
  | `Date Created (days ago)` | 包括基于将产品添加到目录后天数的产品。 |
  | `Date Modified (days ago)` | 包括基于上次修改产品后天数的产品。 |
  | `Name` | 包括基于产品名称的产品。 |
  | `Price` | 包括基于价格的产品。 此属性不适用于可配置产品，因为它们没有自己的价格。 |
  | `Quantity` | 包括基于库存数量的产品。 |
  | `SKU` | 包括基于SKU的产品。 |

  {style="table-layout:auto"}

  >[!NOTE]
  >
  >通过组合所有可销售的子产品数量来计算带有子选项的可配置产品的数量。 假设您有一个可配置的产品&#x200B;_基本健身背心_，它有紫色、红色和黄色选项，且每种选项的数量不同。 在这种情况下，母产品（基本健身箱）数量是紫色、红色和黄色子产品的组合可销售数量。

- **[!UICONTROL Operator]** — 指定应用于属性值以满足条件的运算符。 除非指定运算符，否则默认使用`Equal`。 选项： `Equal`、`Not equal`、`Greater than`、`Greater than or equal to`、`Less than`、`Less than or equal to`和`Contains`

- **[!UICONTROL Value]** — 指定属性必须符合条件的值。

- **[!UICONTROL Logic]** - Logic列用于定义多个条件，并且仅在添加另一个条件时显示。 运算符遵循MySQL [布尔运算符](https://dev.mysql.com/doc/refman/8.0/en/operator-precedence.html)的优先级规则。 选项： `AND` / `OR`

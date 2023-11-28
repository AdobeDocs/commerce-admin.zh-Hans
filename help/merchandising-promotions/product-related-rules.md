---
title: 相关产品规则
description: 了解相关的产品规则以及如何使用它们向客户动态展示相关产品、进行追加销售和交叉销售。
exl-id: ff566e13-cbe8-42f1-be3a-684e364b86dd
feature: Merchandising, Products, Storefront
source-git-commit: 91e6c63f1f6f16b957366f9d5cc651f9eded31c8
workflow-type: tm+mt
source-wordcount: '823'
ht-degree: 0%

---

# 相关产品规则（目标规则）

{{ee-feature}}

通过相关产品规则，您可以定位显示为相关产品、向上销售和交叉销售呈现给客户的产品选择。 每个产品规则都可以与 [客户区段](../customers/customer-segments.md) 以生成针对性促销的动态显示。

由于可以同时触发多个活动规则，因此您可以为每个规则设置优先级。 它定义应用规则的顺序以及产品在页面上的显示顺序。

要访问相关的产品规则，请转到 **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Related Product Rules]**.

![相关产品规则列表](./assets/related-products-rules.png){width="700" zoomable="yes"}

## 列描述

| 列 | 描述 |
|--- |--- |
| [!UICONTROL ID] | 分配给每个相关产品规则的唯一数字标识符 |
| [!UICONTROL Rule] | 相关产品规则的名称 |
| [!UICONTROL Start] | 使用动态日历字段(_[!UICONTROL To:]_和_[!UICONTROL From:]_)，以根据创建规则时定义的规则的开始日期筛选列表。 |
| [!UICONTROL End] | 使用动态日历字段(_[!UICONTROL To:]_和_[!UICONTROL From:]_)，以根据创建规则时定义的规则结束日期筛选列表。 |
| [!UICONTROL Priority] | 在此字段中输入文本以根据为规则定义的优先级筛选列表。 |
| [!UICONTROL Applies To] | 此选项筛选适用于的规则列表 `Related Products`， `Up-sells`、和 `Cross-sells`. |
| [!UICONTROL Status] | 使用此选项可根据规则状态筛选列表(`Active` 或 `Inactive`)。 |

{style="table-layout:auto"}

## 规则优先级

在任意给定时间，可能会触发多个活动规则以显示相关产品、追加销售和交叉销售。 每个规则的优先级决定了产品在页面上的显示顺序。 该值可以设置为任意整数，使用 `1` 有最高优先权。

可包含在产品关系规则中的产品ID的数量由 `Result Limit` 值，其最大值为20。 此 `Result Limit` 值，与 `Configurable Maximum` ，则基于规则的特定产品促销将变为 `Real Limit`，并确定列表中可以显示的匹配产品的实际数量。

[结果限制] + [可配置的最大值] = [实际限制]

例如，假设您有三个规则，其优先级为 `1`， `2`、和 `3`.

- 有两个匹配的产品返回 _规则1_，六个匹配产品 _规则2_，以及20种匹配的产品 _规则3_.
- 在配置中， _[!UICONTROL Maximum Number of Products for Related Products List]_设置为 `6`.

  | 规则 | 优先级 | 匹配产品 |
  |---|---|-----|
  | 规则1 | `1` | `2` |
  | 规则2 | `2` | `6` |
  | 规则3 | `3` | `20` |

如果第一个规则返回的匹配产品多于所允许的 _可配置的最大限制_，但小于 _实数限制_，将使用其他规则中的匹配产品（按优先级顺序），直到 _实数限制_ 已到达。

按优先级，匹配产品返回自 _规则1_ 首先用于填充所有26个可用插槽。 由于规则1仅返回了两个匹配的产品，因此还有空间容纳24个产品。 _规则2_ 具有次高优先级，并返回六个匹配的产品。 现在有18个可用的插槽可供填充。 _规则3_ 具有下一级别的优先级，并有足够的匹配产品来填充剩余的18个版块。 当所有可用插槽均已满时，根据设置的旋转模式，可能会将产品随机排列或按ID排序到每个优先级中，然后减少到可配置的最大限制。 在这种情况下，其余六个产品将显示在商店中。

>[!NOTE]
>
>选定产品始终显示在基于规则的产品之前，无论旋转模式如何。

## 配置基于规则的产品关系

产品关系规则的行为和匹配产品的显示由配置设置决定。 这些设置确定可以显示多少个与规则匹配的产品，以及这些产品的显示顺序。

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧的面板中，展开 **[!UICONTROL Catalog]** 并选择 **[!UICONTROL Catalog]** 下方。

1. 展开 ![扩展](../assets/icon-display-expand.png) 该 **[!UICONTROL Rules-Based Product Relations]** 部分。

   ![目录配置 — 基于规则的产品关系](../configuration-reference/catalog/assets/catalog-rule-based-product-relations.png){width="600" zoomable="yes"}

1. 输入 **[!UICONTROL Maximum Number of Products in the Related Products List]**.

1. 设置 **[!UICONTROL Show Related Products]** 更改为以下任一项：

   - `Both Selected and Rule Based`
   - `Selected Only`
   - `Rule-Based Only`

1. 设置 **[!UICONTROL Rotation Mode for Products in Related Product List]** 更改为以下任一项：

   - `By Priority, Then by ID`
   - `By Priority, Then Random`
   - `Weighted Random`

1. 要完成交叉销售产品设置，请执行以下操作：

   - 输入 **[!UICONTROL Maximum Number of Products in the Cross-Sell Product List]**.

   - 设置 **[!UICONTROL Show Cross-Sell Products]** 更改为以下任一项：

      - `Both Selected and Rule Based`
      - `Selected Only`
      - `Rule-Based Only`

   - 设置 **[!UICONTROL Rotation Mode for Products in Cross-Sell Product List]** 更改为以下任一项：

      - `By Priority, Then by ID`
      - `By Priority, Then Random`
      - `Weighted Random`

1. 要完成追加销售产品设置，请执行以下操作：

   - 输入 **[!UICONTROL Maximum Number of Products in the Upsell Product List]**.

   - 设置 **[!UICONTROL Show Upsell Products]** 更改为以下任一项：

      - `Both Selected and Rule Based`
      - `Selected Only`
      - `Rule-Based Only`

   - 设置 **[!UICONTROL Rotation Mode for Products in Upsell Product List]** 更改为以下任一项：

      - `By Priority, Then by ID`
      - `By Priority, Then Random`
      - `Weighted Random`

1. 完成后，单击 **[!UICONTROL Save Config]**.

### 旋转模式

| 模式 | 描述 |
|---|---|
| [!UICONTROL By Priority, Then by ID] | 产品先按优先级排序，然后在每个优先级内按ID重新排序。 只有在高优先级规则中没有产品剩余以填充可用插槽时，才会显示较低优先级规则中的产品。 |
| [!UICONTROL By Priority, Then Random] | 产品先按优先级排序，然后在每个优先级内随机分配。 只有在高优先级规则中没有产品剩余以填充可用插槽时，才会显示较低优先级规则中的产品。 |
| [!UICONTROL Weighted Random] | 产品是随机分配的，这样，属于具有较高优先级的规则的产品比属于具有较低优先级的规则的产品出现概率更高。 然后，将产品缩减到可配置的最大限制，并按优先级重新分组。 此模式允许低优先级的产品有时显示，即使剩余的插槽中可以填满较高优先级的规则中的产品 |

{style="table-layout:auto"}

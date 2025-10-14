---
title: 相关产品规则
description: 了解相关的产品规则以及如何使用它们向客户动态展示相关产品、进行追加销售和交叉销售。
exl-id: ff566e13-cbe8-42f1-be3a-684e364b86dd
feature: Merchandising, Products, Storefront
source-git-commit: 4971fe457b7fd58d8b71951981bc889386610a99
workflow-type: tm+mt
source-wordcount: '884'
ht-degree: 0%

---

# 相关产品规则（目标规则）

{{ee-feature}}

通过相关产品规则，您可以定位显示为相关产品、向上销售和交叉销售呈现给客户的产品选择。 每个产品规则都可以与[客户区段](../customers/customer-segments.md)关联，以产生目标促销的动态显示。

由于可以同时触发多个活动规则，因此您可以为每个规则设置优先级。 它定义应用规则的顺序以及产品在页面上的显示顺序。

要访问相关产品规则，请转到&#x200B;**[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Related Product Rules]**。

![相关产品规则列表](./assets/related-products-rules.png){width="700" zoomable="yes"}

## 列描述

| 列 | 描述 |
|--- |--- |
| [!UICONTROL ID] | 分配给每个相关产品规则的唯一数字标识符 |
| [!UICONTROL Rule] | 相关产品规则的名称 |
| [!UICONTROL Start] | 使用动态日历字段（_[!UICONTROL To:]_&#x200B;和&#x200B;_[!UICONTROL From:]_）根据创建规则时定义的规则的开始日期筛选列表。 |
| [!UICONTROL End] | 使用动态日历字段（_[!UICONTROL To:]_&#x200B;和&#x200B;_[!UICONTROL From:]_）根据创建规则时定义的规则的结束日期筛选列表。 |
| [!UICONTROL Priority] | 在此字段中输入文本以根据为规则定义的优先级筛选列表。 |
| [!UICONTROL Applies To] | 此选项筛选应用于`Related Products`、`Up-sells`和`Cross-sells`的规则列表。 |
| [!UICONTROL Status] | 使用此选项可根据规则状态（`Active`或`Inactive`）筛选列表。 |

{style="table-layout:auto"}

## 规则优先级

在任意给定时间，可能会触发多个活动规则以显示相关产品、追加销售和交叉销售。 每个规则的优先级决定了产品在页面上的显示顺序。 该值可以设置为任意整数，其中`1`具有最高优先级。

产品关系规则中可包含的产品ID的数量由`Result Limit`值决定，该值的最大值为20。 与基于规则的特定产品促销活动的`Configurable Maximum`相结合的`Result Limit`值将变为`Real Limit`，并确定列表中可以显示的匹配产品的实际数量。

[结果限制] + [可配置的最大值] = [实际限制]

例如，假设您有三个规则，其优先级为`1`、`2`和`3`。

- 为&#x200B;_规则1_&#x200B;返回了两个匹配产品，为&#x200B;_规则2_&#x200B;返回了六个匹配产品，为&#x200B;_规则3_&#x200B;返回了20个匹配产品。
- 在配置中，_[!UICONTROL Maximum Number of Products for Related Products List]_&#x200B;设置为`6`。

  | 规则 | 优先级 | 匹配产品 |
  |---|---|-----|
  | 规则1 | `1` | `2` |
  | 规则2 | `2` | `6` |
  | 规则3 | `3` | `20` |

如果第一个规则返回的匹配产品超过&#x200B;_可配置的最大限制_&#x200B;所允许的数量，但少于&#x200B;_实际限制_，则将使用其他规则中的匹配产品（按优先级顺序），直到达到&#x200B;_实际限制_。

按优先级，从&#x200B;_规则1_&#x200B;返回的匹配产品可以首先用于填充所有26个可用版块。 由于规则1仅返回了两个匹配的产品，因此还有空间容纳24个产品。 _规则2_&#x200B;具有下一个最高优先级，并返回另外六个匹配的产品。 现在有18个可用的插槽可供填充。 _规则3_&#x200B;具有下一级别的优先级，匹配的产品足以填充剩余的18个版块。 当所有可用插槽均已满时，根据设置的旋转模式，可能会将产品随机排列或按ID排序到每个优先级中，然后减少到可配置的最大限制。 在这种情况下，其余六个产品将显示在商店中。

>[!NOTE]
>
>选定产品始终显示在基于规则的产品之前，无论旋转模式如何。

## 配置基于规则的产品关系

产品关系规则的行为和匹配产品的显示由配置设置决定。 这些设置确定可以显示多少个与规则匹配的产品，以及这些产品的显示顺序。

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧的面板中，展开&#x200B;**[!UICONTROL Catalog]**&#x200B;并在下面选择&#x200B;**[!UICONTROL Catalog]**。

1. 展开&#x200B;**[!UICONTROL Rules-Based Product Relations]**&#x200B;部分的![扩展](../assets/icon-display-expand.png)。

   ![目录配置 — 基于规则的产品关系](../configuration-reference/catalog/assets/catalog-rule-based-product-relations.png){width="600" zoomable="yes"}

1. 输入&#x200B;**[!UICONTROL Maximum Number of Products in the Related Products List]**。

1. 将&#x200B;**[!UICONTROL Show Related Products]**&#x200B;设置为以下项之一：

   - `Both Selected and Rule Based`
   - `Selected Only`
   - `Rule-Based Only`

1. 将&#x200B;**[!UICONTROL Rotation Mode for Products in Related Product List]**&#x200B;设置为以下项之一：

   - `By Priority, Then by ID`
   - `By Priority, Then Random`
   - `Weighted Random`

1. 要完成交叉销售产品设置，请执行以下操作：

   - 输入&#x200B;**[!UICONTROL Maximum Number of Products in the Cross-Sell Product List]**。

   - 将&#x200B;**[!UICONTROL Show Cross-Sell Products]**&#x200B;设置为以下项之一：

      - `Both Selected and Rule Based`
      - `Selected Only`
      - `Rule-Based Only`

   - 将&#x200B;**[!UICONTROL Rotation Mode for Products in Cross-Sell Product List]**&#x200B;设置为以下项之一：

      - `By Priority, Then by ID`
      - `By Priority, Then Random`
      - `Weighted Random`

1. 要完成追加销售产品设置，请执行以下操作：

   - 输入&#x200B;**[!UICONTROL Maximum Number of Products in the Upsell Product List]**。

   - 将&#x200B;**[!UICONTROL Show Upsell Products]**&#x200B;设置为以下项之一：

      - `Both Selected and Rule Based`
      - `Selected Only`
      - `Rule-Based Only`

   - 将&#x200B;**[!UICONTROL Rotation Mode for Products in Upsell Product List]**&#x200B;设置为以下项之一：

      - `By Priority, Then by ID`
      - `By Priority, Then Random`
      - `Weighted Random`

1. 完成后，单击&#x200B;**[!UICONTROL Save Config]**。

### 旋转模式

| 模式 | 描述 |
|---|---|
| [!UICONTROL By Priority, Then by ID] | 产品先按优先级排序，然后在每个优先级内按ID重新排序。 只有在高优先级规则中没有产品剩余以填充可用插槽时，才会显示较低优先级规则中的产品。 |
| [!UICONTROL By Priority, Then Random] | 产品先按优先级排序，然后在每个优先级内随机分配。 只有在高优先级规则中没有产品剩余以填充可用插槽时，才会显示较低优先级规则中的产品。 |
| [!UICONTROL Weighted Random] | 产品是随机分配的，这样，属于具有较高优先级的规则的产品比属于具有较低优先级的规则的产品出现概率更高。 然后，将产品缩减到可配置的最大限制，并按优先级重新分组。 此模式允许低优先级的产品有时显示，即使剩余的插槽中可以填满较高优先级的规则中的产品 |

{style="table-layout:auto"}

## 使用Real-Time CDP受众来通知相关的产品规则

>[!NOTE]
>
>此功能处于测试阶段。 如果要加入Beta版计划，请向[dataconnection@adobe.com](mailto:dataconnection@adobe.com)发送请求。


了解如何在您的Adobe Commerce实例中[激活](../customers/audience-activation.md)Real-Time CDP受众，以告知相关的产品规则。

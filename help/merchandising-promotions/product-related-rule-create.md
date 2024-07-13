---
title: 创建相关的产品规则
description: 了解如何创建可触发的相关产品规则以显示相关产品、追加销售和交叉销售。
exl-id: fbc059ec-d3e6-46ca-810a-a979a0631dd8
feature: Merchandising, Products, Storefront
source-git-commit: cea943cd7f4d148c885fbd113c3bc08bfdf63ea0
workflow-type: tm+mt
source-wordcount: '655'
ht-degree: 0%

---

# 创建相关的产品规则

{{ee-feature}}

创建相关产品规则的过程与设置价格规则类似。 首先，定义要匹配的条件，然后选择要显示的产品。 在任意给定时间，可能会触发多个活动规则以显示相关产品、追加销售和交叉销售。 每个规则的优先级决定了产品块在页面上的显示顺序。

>[!NOTE]
>
>对于要在目标规则中使用的属性，[_[!UICONTROL Use for Promo Rule Conditions]_](../catalog/product-attributes.md)属性必须设置为`Yes`。

>[!NOTE]
>
>对于所有产品属性，`All Store Views`范围值始终同时用于[!UICONTROL Products to Match]和[!UICONTROL Products to Display]条件。 当产品属性对于不同的商店视图和网站具有不同的值时，这也适用。

## 创建相关的产品规则

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Related Product Rules]**。

1. 单击右上角的&#x200B;**[!UICONTROL Add Rule]**。

   ![相关产品规则 — 信息](./assets/catalog-related-products-rule-information.png){width="600" zoomable="yes"}

1. 按如下方式完成&#x200B;**[!UICONTROL Rule Information]**：

   - 输入&#x200B;**[!UICONTROL Rule Name]**&#x200B;以标识在管理员中工作时的规则。

   - 对于&#x200B;**[!UICONTROL Priority]**，输入一个数字，以决定当其他规则的结果指向同一位置时，结果在页面上出现的顺序。 数字`1`是最高优先级。

   - 要启用规则，请将&#x200B;**[!UICONTROL Status]**&#x200B;设置为`Active`。

   - 将&#x200B;**[!UICONTROL Apply To]**&#x200B;设置为以下项之一：

      - `Related Products`
      - `Up-sells`
      - `Cross-sells`

   - 如果规则在特定时间范围内处于活动状态，请输入&#x200B;**[!UICONTROL From]**&#x200B;和&#x200B;**[!UICONTROL To]**&#x200B;日期。

   - 对于&#x200B;**[!UICONTROL Result Limit]**，输入要显示在结果列表中的记录数。 最大数量为20。

   - 如果规则应用于特定的[客户区段](../customers/customer-segments.md)，请将&#x200B;**[!UICONTROL Customer Segments]**&#x200B;设置为`Specified`并从列表中选择客户区段。

   - 如果规则应用于特定的[Real-Time CDP受众](../customers/audience-activation.md)，请将&#x200B;**[!UICONTROL Real-Time CDP Audience]**&#x200B;设置为`Specified`并从列表中选择Real-Time CDP受众。 此功能处于测试阶段。 如果要加入Beta版计划，请向[dataconnection@adobe.com](mailto:dataconnection@adobe.com)发送请求。

     ![相关产品规则 — Real-Time CDP受众](./assets/rtcdp-related-products.png){width="500"}

1. 在左侧面板中，选择&#x200B;**[!UICONTROL Products to Match]**&#x200B;并生成条件，就像您生成[目录价格规则](price-rules-catalog.md)一样。

   ![相关产品规则 — 要匹配的产品](./assets/catalog-related-products-match.png){width="500"}

1. 在左侧面板中，选择&#x200B;**[!UICONTROL Products to Display]**&#x200B;并生成与[目录价格规则](price-rules-catalog.md)相同的结果条件。

   ![相关产品规则 — 要显示的产品](./assets/catalog-related-products-to-display.png){width="500"}

   完成条件以描述要包含在显示结果中的产品。

1. 完成后，单击&#x200B;**[!UICONTROL Save]**。

## 删除相关产品规则

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Related Product Rules]**。

1. 查找要删除的相关产品规则。

1. 单击规则以打开详细信息页面。

1. 单击右上角的&#x200B;**[!UICONTROL Delete]**。

1. 要确认操作，请单击&#x200B;**[!UICONTROL OK]**。

## 相关产品规则演示

观看本视频，了解如何创建相关的产品规则：

>[!VIDEO](https://video.tv.adobe.com/v/343837?quality=12&learn=on)

## 字段描述

| 字段 | 描述 |
|--- |--- |
| [!UICONTROL Rule Name] | 标识规则供内部使用的名称。 |
| [!UICONTROL Priority] | 确定规则的结果与针对页面上相同位置的其他结果集一起显示时的显示顺序。 该值可以设置为任意整数，最高优先级为1。 例如，如果有多个适用向上销售规则，则优先级最高的规则出现在其他规则之前。 每组结果中产品的排序顺序是随机的。 任何手动配置的追加销售、交叉销售和相关产品始终在任何基于规则的产品促销之前出现在页面上。 |
| [!UICONTROL Status] | 控制规则的活动状态。 选项： `Active` / `Inactive` |
| [!UICONTROL Apply To] | 标识与规则关联的产品关系类型。 选项： `Related Products` / `Up-sells` / `Cross-sells` |
| [!UICONTROL From Date] | 如果规则在一定时间内处于活动状态，则此设置将确定规则处于活动状态的第一个日期。 |
| [!UICONTROL To Date] | 如果规则在一定时间内处于活动状态，则此设置将确定规则处于活动状态的最后日期。 |
| [!UICONTROL Result Limit] | 确定一次显示在结果中的产品数量。 最大数量为20。 如果找到更多匹配结果，则每次刷新页面时，产品都会在块中旋转。 |
| [!UICONTROL Customer Segments] | 标识应用规则的客户区段。 选项： `All` / `Specified` |

{style="table-layout:auto"}

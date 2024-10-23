---
title: 购物车价格规则的计划更改
description: 了解如何在营销活动中按计划应用购物车价格规则，并将其与其他内容更改分组。
exl-id: 4c9caa04-1e11-440d-b3db-7cc5fc83a08f
feature: Merchandising, Price Rules, Shopping Cart
source-git-commit: 0ceb61e6f1629a3bef16c550362c1db25b4aefa5
workflow-type: tm+mt
source-wordcount: '489'
ht-degree: 0%

---

# 购物车价格规则的计划更改

{{ee-feature}}

购物车价格规则可以作为营销活动的一部分按计划应用，并与其他内容更改一起分组。 您可以根据对价格规则的计划更改创建促销活动，或将更改应用于现有促销活动。

>[!NOTE]
>
>[!UICONTROL From]和[!UICONTROL To]字段已在![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce中移除，无法直接在购物车价格规则中修改。 您必须为这些激活创建计划的更新。

![购物车价格规则 — 计划的更改](./assets/content-staging-price-rules-cart-scheduled-changes.png){width="700" zoomable="yes"}

>[!NOTE]
>
>所有计划的更新将连续应用。 这意味着任何实体都只能在一个时间点进行一次计划更新。 任何计划的更新将应用于其时间范围内的所有存储视图。 因此，实体无法同时对不同存储视图进行不同的计划更新。 所有存储视图中的所有实体属性值（不受当前计划更新影响）均从默认值获取，而不是从上次计划更新获取。

如果同一促销活动中运行了多个价格规则，则价格规则的&#x200B;_[!UICONTROL Priority]_设置将确定哪条规则优先。 若要了解详细信息，请参阅[内容暂存](../content-design/content-staging.md)。

>[!NOTE]
>
>如果活动营销活动最初创建时没有结束日期，则以后无法编辑活动以包含结束日期。 在这种情况下，需要创建一个重复的市场活动并输入所需的结束日期。

>[!NOTE]
>
>如果某个营销活动链接到多个购物车价格规则，则只能从[内容暂存仪表板](../content-design/content-staging-dashboard.md)编辑该营销活动。

请牢记以下注意事项：

- 如果包含价格规则的促销活动最初创建时没有结束日期，则以后无法编辑该促销活动以包含结束日期。 建议您在创建营销活动时添加结束日期，或创建现有营销活动的重复版本，并根据需要向重复版本添加结束日期。
- 使用计划更新启用带有结束日期的购物车价格规则时，请确保将规则设置为最初禁用。 已生效的规则不遵循结束日期。
- 优惠券未关联到购物车价格规则。 计划更新不提供对&#x200B;_[!UICONTROL Rule Information]_选项卡上的_[!UICONTROL Coupon]_、_[!UICONTROL Coupon Code]_、_[!UICONTROL Uses per Coupon]_&#x200B;和&#x200B;_[!UICONTROL Uses per Customer]_字段的访问权限。 另外，_[!UICONTROL Manage Coupon Codes]_&#x200B;选项卡中的所有设置均不可用。

>[!IMPORTANT]
>
>营销活动&#x200B;**[!UICONTROL Start Date]**&#x200B;和&#x200B;**[!UICONTROL End Date]**&#x200B;必须使用从每个网站的本地时区转换而来的&#x200B;**_默认_**&#x200B;管理时区来定义。 请考虑以下示例：您有多个网站位于不同时区，但您想要基于美国时区启动Campaign。 在这种情况下，您需要为每个本地时区计划单独的更新，并将&#x200B;**[!UICONTROL Start Date]**&#x200B;和&#x200B;**[!UICONTROL End Date]**&#x200B;从每个本地网站时区转换为默认的管理时区。

---
title: 购物车价格规则的计划更改
description: 了解如何在营销活动中按计划应用购物车价格规则，并将其与其他内容更改分组。
exl-id: 4c9caa04-1e11-440d-b3db-7cc5fc83a08f
feature: Merchandising, Price Rules, Shopping Cart
source-git-commit: 3d04e7213d90bb4c323acce69ac31c1dbcb7ca49
workflow-type: tm+mt
source-wordcount: '424'
ht-degree: 0%

---

# 购物车价格规则的计划更改

{{ee-feature}}

购物车价格规则可以作为营销活动的一部分按计划应用，并与其他内容更改一起分组。 您可以根据对价格规则的计划更改创建促销活动，或将更改应用于现有促销活动。

>[!NOTE]
>
>此 [!UICONTROL From] 和 [!UICONTROL To] 中的字段已删除 ![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce ，且无法直接在购物车价格规则中修改。 您必须为这些激活创建计划的更新。

![购物车价格规则 — 计划的更改](./assets/content-staging-price-rules-cart-scheduled-changes.png){width="700" zoomable="yes"}

>[!NOTE]
>
>所有计划的更新将连续应用。 这意味着任何实体都只能在一个时间点进行一次计划更新。 任何计划的更新将应用于其时间范围内的所有存储视图。 因此，实体无法同时对不同存储视图进行不同的计划更新。 所有存储视图中的所有实体属性值（不受当前计划更新影响）均从默认值获取，而不是从上次计划更新获取。

如果同一促销活动中运行了多个价格规则，则 _[!UICONTROL Priority]_价格规则的设置将确定哪条规则优先。 要了解更多信息，请参阅 [内容暂存](../content-design/content-staging.md).

请牢记以下注意事项：

- 如果包含价格规则的促销活动最初创建时没有结束日期，则以后无法编辑该促销活动以包含结束日期。 建议您在创建营销活动时添加结束日期，或创建现有营销活动的重复版本，并根据需要向重复版本添加结束日期。
- 使用计划更新启用带有结束日期的购物车价格规则时，请确保将规则设置为最初禁用。 已生效的规则不遵循结束日期。
- 优惠券未关联到购物车价格规则。 计划更新不提供对的访问权限 _[!UICONTROL Coupon]_，_[!UICONTROL Coupon Code]_， _[!UICONTROL Uses per Coupon]_、和_[!UICONTROL Uses per Customer]_ 字段位于 _[!UICONTROL Rule Information]_选项卡。 此外，来自以下各项的所有设置：_[!UICONTROL Manage Coupon Codes]_ 选项卡不可用。

>[!IMPORTANT]
>
>营销活动 **[!UICONTROL Start Date]** 和 **[!UICONTROL End Date]** 必须使用 **_默认_** 管理时区，从每个网站的本地时区转换而来。 请考虑以下示例：您有多个网站位于不同时区，但您想要基于美国时区启动Campaign。 在这种情况下，您需要为每个本地时区计划单独的更新，并设置 **[!UICONTROL Start Date]** 和 **[!UICONTROL End Date]** 从每个本地网站时区转换为默认的管理时区。

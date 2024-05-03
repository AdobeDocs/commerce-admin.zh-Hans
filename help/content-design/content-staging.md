---
title: 内容暂存
description: 内容暂存使您的业务团队能够直接从管理员轻松创建、预览和计划存储的各种内容更新。
exl-id: 929cd020-cbc7-40bf-a22c-02df35212ecf
feature: Page Content, Staging
source-git-commit: 3d04e7213d90bb4c323acce69ac31c1dbcb7ca49
workflow-type: tm+mt
source-wordcount: '833'
ht-degree: 0%

---

# 内容暂存

{{ee-feature}}

内容暂存使您的业务团队能够直接从创建、预览和计划为商店进行广泛的内容更新。 _管理员_. 例如，不要以静态页面来思考，而应将页面视为可翻转的不同元素的集合 _日期_ 或 _关_ 按计划执行。 您可以使用内容暂存创建一个页面，该页面会在一年中按计划自动更改。

术语 _营销活动_ 指计划更改的记录，或从“暂存功能板”管理的更改集合。 可以在日历或时间轴上查看更改。 术语 _计划的更改_ 和 _计划的更新_ 可互换，指单个更改。

当您计划在特定时间段内进行内容更改时，当计划的更改过期时，内容将恢复到以前的版本。 您可以创建同一基线内容的多个版本以用于未来的更新。 您还可以回溯时间线以查看内容的早期版本。 要保存草稿版本，只需在时间轴上指定一个日期，该日期距离未来很远，并且绝不会投入生产。

>[!NOTE]
>
>与开始日期和结束日期相关的字段已删除 ![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce和不能直接在购物车价格规则、目录价格规则、产品、类别和CMS页面上修改。 您必须为这些激活创建计划的更新。

## 内容暂存对象和营销活动

为以下任何对象创建新的计划更新时，系统会将相应的营销活动创建为占位符，并且 _[!UICONTROL Scheduled Changes]_框显示在页面顶部。 占位符营销活动具有开始日期，但没有结束日期。 您可以将内容更新安排为营销活动的一部分，然后按日期、时间或商店视图预览和共享更改。 为一个对象创建新营销活动后，可将其指定为其他对象的计划更新。

- [产品](../catalog/product-scheduled-changes.md)
- [类别](../catalog/category-scheduled-changes.md)
- [目录价格规则](../merchandising-promotions/price-rule-catalog-scheduled-changes.md)
- [购物车价格规则](../merchandising-promotions/price-rule-cart-scheduled-changes.md)
- [CMS页面](pages-workspace.md#scheduled-changes)
- [CMS块](blocks.md)

## 内容暂存工作流

1. **创建基线内容**

   基线是指没有营销活动的资产内容，包括 _[!UICONTROL Scheduled Changes]_部分。 将始终使用基线内容，除非存在在时间轴上针对该位置计划了更改的活动营销活动。

1. **创建第一个营销活动**

   根据需要使用开始和结束日期创建您的第一个营销活动。 要使营销活动处于开放状态，请将结束日期留空。 第一个营销活动结束时，将恢复原始基线内容。

   >[!NOTE]
   >
   >市场活动开始日期和结束日期必须通过使用 **_默认_** 管理时区，从每个网站的本地时区转换而来。 请考虑以下示例：您有多个位于不同时区的网站，但您希望基于美国时区启动营销活动。 在这种情况下，您必须为每个本地时区计划单独的更新，并设置 **[!UICONTROL Start Date]** 和 **[!UICONTROL End Date]** ，从每个本地网站时区转换为默认的管理时区。

1. **添加第二个营销活动**

   创建第二个营销活动，并根据需要提供开始和结束日期。 第二个营销活动可以分配给完全不同的时间段。 为同一资产创建多个营销活动时，营销活动不能重叠。 您可以根据需要创建任意数量的营销活动。

   >[!NOTE]
   >
   >所有计划的更新都连续应用，这意味着任何实体一次只能有一个计划的更新。 任何计划的更新将应用于其时间范围内的所有存储视图。 因此，一个实体不能同时对不同存储视图进行不同的计划更新。 所有存储视图中的所有实体属性值（不受当前计划更新影响）均从默认值获取，而不是从上次计划更新获取。

1. **恢复基线内容**

   如果所有营销活动都有结束日期，则当所有活动的营销活动结束时，将恢复基线内容。

>[!NOTE]
>
>当实体的暂存更新处于活动状态时，编辑实体即编辑当前活动的暂存更新。 它不会影响基线内容，该内容在暂存更新结束时恢复。

## [!UICONTROL Content Staging] 仪表板

此 [!UICONTROL Content Staging] [仪表板](content-staging-dashboard.md) 允许查看所有计划的站点更改和更新。 可以预览营销活动的任何一天、日期范围或时间段，并与他人共享。

![暂存仪表板](./assets/content-staging-dashboard-grid.png){width="600" zoomable="yes"}

## 内容暂存演示

要了解内容暂存，请观看此视频：

>[!VIDEO](https://video.tv.adobe.com/v/343784?quality=12)

## 资源疑难解答

有关排查内容暂存问题的帮助，请参阅以下内容 [!DNL Commerce] 支持知识库文章：

- [由于内容暂存问题，所有页面均显示错误404](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/site-down-or-unresponsive/error-404-on-all-pages-due-to-content-staging-issue.html)
- [计划内容暂存更新未与过时的Fastly缓存一起显示](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/scheduled-content-staging-updates-not-displayed-with-stale-fastly-cache.html)
- [我是否可以为共享目录中的价格计划内容暂存更新？](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/faq/can-i-schedule-content-staging-updates-for-prices-in-a-shared-catalog.html)

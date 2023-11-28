---
title: 计划内容更新
description: 请查看此促销活动示例，以安排产品的临时价格变更。
exl-id: 36b7d7f6-4590-4192-a82b-e5f645b05f62
feature: Page Content, Staging
source-git-commit: b3897ba034770229ef8f3117231bed286abdddb9
workflow-type: tm+mt
source-wordcount: '636'
ht-degree: 0%

---

# 计划内容更新

{{ee-feature}}

以下示例说明如何计划产品的临时价格更改。 其中包括计划和预览更改，以及查看日历中的计划更新。 尽管此示例仅包括一项更改，但营销活动可能包括对产品、价格规则、CMS页面和其他计划同时发生的实体的多项更改。 按照类似的方法指定开始/结束日期 [!UICONTROL Set Product As New] 属性。

>[!NOTE]
>您必须创建计划的更新，以指定开始（和结束）日期 [!UICONTROL Set Product As New]. 对象 [!UICONTROL Special Price] 和 [!UICONTROL Design Change]，则从Adobe Commerce中删除了起始/截止日期字段，这些字段仅在Magento Open Source中可用。
>
>所有计划的更新都连续应用，这意味着任何实体一次只能有一个计划的更新。 任何计划的更新将应用于其时间范围内的所有存储视图。 因此，一个实体不能同时对不同存储视图进行不同的计划更新。 所有存储视图中的所有实体属性值（不受当前计划更新影响）均从默认值获取，而不是从上次计划更新获取。

## 计划产品更新

1. 从 _[!UICONTROL Products]_网格，在编辑模式下打开产品。

1. 在 _[!UICONTROL Scheduled Changes]_框中，单击&#x200B;**[!UICONTROL Schedule New Update]**.

   ![计划新更新](./assets/content-staging-product-schedule-new-update.png){width="600" zoomable="yes"}

1. 使用 **[!UICONTROL Save as a New Update]** 选项，设置更新的基本参数：

   - 对象 **[!UICONTROL Update Name]**，输入新内容暂存营销活动的名称。

   - 输入摘要 **[!UICONTROL Description]** 以及如何使用它。

   - 使用日历(![日历图标](../assets/icon-calendar.png))工具来选择 **开始日期** 和 **结束日期** 来参加竞选的。

     要创建开放营销活动，请勿指定结束日期（留空）。 在本例中，营销活动计划于新年的午夜(太平洋标准时间2021年1月1日凌晨12:00开始。


     对于创建时没有结束日期的价格规则市场活动，以后将无法添加结束日期。 在这种情况下，需要创建一个营销策划，并将开始日期设置为希望旧营销策划结束的日期和希望新营销策划开始的日期。 在该开始日期，旧营销活动结束，新营销活动开始（按定义）。

     ![计划产品更新](./assets/content-staging-campaign-schedule-update.png){width="600" zoomable="yes"}

     >[!NOTE]
     >
     >必须通过使用以下各项定义促销活动的开始日期和结束日期 **_默认_** 管理时区，从每个网站的本地时区转换而来。 例如，如果您有多个网站位于不同时区，但希望根据美国（默认）时区启动促销活动，则必须为每个本地时区计划单独的更新。 在这种情况下，设置 **[!UICONTROL Start Date]** 和 **[!UICONTROL End Date]** 从每个本地网站时区转换为默认管理员时区的内容。

1. 向下滚动到 _[!UICONTROL Price]_并单击&#x200B;**[!UICONTROL Advanced Pricing]**.

1. 输入 **[!UICONTROL Special Price]** 在计划的营销活动期间搜索产品，然后单击 **[!UICONTROL Done]**.

1. 完成后，单击 **[!UICONTROL Save]**.

   计划的更改将出现在产品页面的顶部，其中包含营销活动的开始和结束日期。

   ![计划的更改](./assets/content-staging-product-scheduled-update-preview-rope.png){width="600" zoomable="yes"}

## 编辑计划的更改

1. 在 _计划的更改_ 框中，单击 **[!UICONTROL View/Edit]**.

1. 对计划更新进行任何必要的更改。

1. 单击 **[!UICONTROL Save]**.

## 预览计划的更改

在 _计划的更改_ 框中，单击 **[!UICONTROL Preview]**.

预览会打开一个新的浏览器选项卡，并显示产品在计划的营销活动期间的显示方式。

>[!NOTE]
>
>计划更新的暂存预览始终从 **默认** 商店视图，模拟客户在暂存更新促销活动中导航的体验。

有关使用预览内容工具更改预览日期和范围的更多信息，请参阅 [预览营销活动](content-staging-preview.md). 您还可以与同事共享指向商店预览的链接。

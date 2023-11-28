---
title: 计划的产品更新
description: 了解如何安排对产品清单的更改，以支持活动和促销计划。
exl-id: ce1aebe6-9032-438d-b950-4b13116b8ed3
feature: Catalog Management, Products
source-git-commit: 1e809696ee6d623d162226628329ed53e8f71511
workflow-type: tm+mt
source-wordcount: '603'
ht-degree: 0%

---

# 计划产品更新

{{ee-feature}}

产品更新可以按计划应用，并与其他内容更改分组。 您可以使用 [内容暂存](../content-design/content-staging.md) 以根据对产品的计划更改创建营销活动，或将更改应用于现有营销活动。

>[!NOTE]
>
>所有计划的更新都连续应用，这意味着任何实体一次只能有一个计划的更新。 任何计划的更新将应用于其时间范围内的所有存储视图。 因此，实体无法同时对不同存储视图进行不同的计划更新。 所有存储视图中的所有实体属性值（不受当前计划更新影响）均从默认值获取，而不是从上次计划更新获取。

>[!NOTE]
>
>计划更新的暂存预览始终从 **默认** 商店视图，模拟客户在暂存更新促销活动中导航的体验。

## 创建计划的更新

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. 选择现有产品并单击 **[!UICONTROL Edit]**.

1. 单击 **[!UICONTROL Schedule New Update]**.

1. 选择 **[!UICONTROL Save as a New Update]**.

1. 对象 **[!UICONTROL Update Name]**，输入新内容暂存营销活动的名称。

1. 输入摘要 **[!UICONTROL Description]** 以及如何使用它。

1. 使用日历(![日历图标](../assets/icon-calendar.png))工具来选择 **[!UICONTROL Start Date]** 和 **[!UICONTROL End Date]** 来参加竞选的。

   >[!NOTE]
   >
   >营销活动 **[!UICONTROL Start Date]** 和 **[!UICONTROL End Date]** 必须使用 **_默认_** 管理时区，从每个网站的本地时区转换而来。 例如，对于位于不同时区的多个网站，如果您希望根据美国时区启动促销活动，则必须为每个本地时区计划单独的更新。 设置 **[!UICONTROL Start Date]** 和 **[!UICONTROL End Date]** ，并将其从本地网站时区转换为默认的管理时区。

   ![计划为新更新](./assets/product-schedule-as-new.png){width="600" zoomable="yes"}

1. 向下滚动到 _[!UICONTROL Price]_并单击&#x200B;**[!UICONTROL Advanced Pricing]**.

1. 输入 **[!UICONTROL Special Price]** 在计划的营销活动期间搜索产品，然后单击 **[!UICONTROL Done]**.

1. 完成后，单击 **[!UICONTROL Save]**.

## 分配给现有更新

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. 选择现有产品并单击 **[!UICONTROL Edit]**.

1. 单击 **[!UICONTROL Schedule New Update]**.

1. 选择 **[!UICONTROL Assign to Existing Campaign]**.

1. 在列表中，选择要修改的营销策划。

   ![分配给现有营销活动](./assets/scheduled-changes-assign-to-existing-campaign.png){width="600" zoomable="yes"}

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) **[!UICONTROL Content]**.

1. 完成后，单击 **[!UICONTROL Save]**.

## 查看计划的更改

计划的更改将出现在产品页面的顶部，其中包含营销活动的开始和结束日期。

![计划的更改](./assets/view-product-scheduled-changes.png){width="600" zoomable="yes"}

## 编辑计划的更改

1. 在 _[!UICONTROL Scheduled Changes]_框中，单击&#x200B;**[!UICONTROL View/Edit]**.

1. 对计划更新进行任何必要的更改。

1. 单击 **[!UICONTROL Save]**.

## 删除计划的更改

1. 在 _[!UICONTROL Scheduled Changes]_框中，单击&#x200B;**[!UICONTROL View/Edit]**.

1. 在顶部栏中，单击 **[!UICONTROL Remove from Update]**.

   ![删除计划的更改](./assets/remove-product-scheduled-changes.png){width="600" zoomable="yes"}

1. 在对话框中，选择 **[!UICONTROL Delete the Update]** 并单击 **[!UICONTROL Done]**.

   >[!NOTE]
   >
   >产品将从更新中删除，并且所有计划的更改都将丢失。

## 计划设计更新

{{ce-feature}}

此 _[!UICONTROL Schedule Design Update]_部分允许您对产品页面的外观进行临时更改。 您可以安排在某一季节、促销活动中进行设计更改，也可以只进行更改以更新内容。 可以提前计划设计变更，使其生效，或者_&#x200B;滴管&#x200B;_，根据您定义的计划。

![计划的设计更新](./assets/product-design-update-scheduled-ce.png){width="600" zoomable="yes"}


| 字段 | 描述 |
|--- |--- |
| [!UICONTROL Schedule Update From/To] | 确定将自定义布局应用于产品时的日期范围。 |
| [!UICONTROL New Theme] | 将自定义主题应用于产品。 |
| [!UICONTROL New Layout] | 将不同的布局应用于产品页面。 选项： <br/>**[!UICONTROL No layout updates]**— 默认情况下，产品页面不提供布局更新。<br/>**[!UICONTROL Empty]**  — 允许您定义自己的布局，如4列页面。 （需要了解XML。） <br/>**[!UICONTROL 1 column]**— 将一列式布局应用于产品页。<br/>**[!UICONTROL 2 columns with left bar]**  — 将带有左侧栏的双列布局应用于产品页面。 <br/>**[!UICONTROL 2 columns with right bar]**— 将带有右侧栏的两列布局应用于产品页面。<br/>**[!UICONTROL 3 columns]**  — 将三列布局应用于产品页。 |

{style="table-layout:auto"}

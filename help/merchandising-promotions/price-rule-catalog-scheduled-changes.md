---
title: 目录价格规则的计划更改
description: 了解如何按计划应用目录价格规则作为营销活动的一部分并按照其他内容更改进行分组。
exl-id: ec4b915f-0a27-438d-b1b0-f1bcd297af6d
feature: Merchandising, Price Rules, Catalog Management
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '797'
ht-degree: 0%

---

# 目录价格规则的计划更改

{{ee-feature}}

保存或更新新价格规则后，“计划的更改”框将显示在页面顶部。 目录价格规则可以按计划作为促销活动的一部分应用，并与其他内容更改一起分组。 您可以根据对价格规则的计划更改创建促销活动，或将更改应用于现有促销活动。

>[!NOTE]
>
>所有计划的更新将连续应用。 这意味着任何实体都只能在一个时间点进行一次计划更新。 任何计划的更新将应用于其时间范围内的所有存储视图。 因此，实体无法同时对不同存储视图进行不同的计划更新。 所有存储视图中的所有实体属性值（不受当前计划更新影响）均从默认值获取，而不是从上次计划更新获取。

如果在同一促销活动中运行了多个价格规则，则价格规则的“优先级”设置将确定哪条规则优先。 要了解更多信息，请参阅 [内容暂存](../content-design/content-staging.md).

>[!IMPORTANT]
>
>如果包含价格规则的促销活动最初创建时没有结束日期，则以后无法编辑该促销活动以包含结束日期。 建议您在创建营销策划时添加结束日期，或创建现有营销策划的重复版本，并根据需要在重复版本中添加结束日期。

![目录价格规则 — 计划的更改](./assets/price-rule-catalog-scheduled.png){width="600" zoomable="yes"}

## 计划目录价格规则的更新

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**目录价格规则**.

1. 在编辑模式下打开规则。

1. 在 **[!UICONTROL Scheduled Changes]** 框中，单击 **[!UICONTROL Schedule New Update]**.

1. 使用 **[!UICONTROL Save as a New Update]** 选项，请执行以下操作：

   - 对象 **[!UICONTROL Update Name]**，输入规则更新的名称。

   - 输入摘要 **[!UICONTROL Description]** 更新，包括应用它的方法或原因。

   - 使用 _日历_ (![日历图标](../assets/icon-calendar.png))以选择 **[!DNL Start Date]** 和 **[!UICONTROL End Date]** 以使计划的更改生效。 要创建开放更改，请将结束日期留空。

   ![目录价格规则 — 新的计划更改](./assets/price-rule-catalog-schedule-update.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >开始和结束日期/时间由默认的管理员面板日期/时间和时区决定，而不是由特定网站的时区决定。 考虑网站的时区，以正确确定开始和结束时间。 为位于不同时区、需要在特定本地时间启动和/或停止的网站创建单独的规则。

1. 向下滚动到 **[!UICONTROL Rule Information]** 部分，并根据需要更改规则。

   您可以计划更改任何规则参数，包括规则的网站（范围）/客户组、规则的条件和规则应用的操作。 有关更多信息，请参阅 [创建目录价格规则](price-rules-catalog-create.md).

   >[!NOTE]
   >
   >如果您更改了任何规则信息参数，请确保 _[!UICONTROL Status]_已正确设置。 如果您希望更改会生成一个主动应用的规则，则状态应为`Active`.

1. 完成后，单击 **[!UICONTROL Save]**.

   计划的更改将显示在页面顶部，其中包含营销活动的开始和结束日期。

## 编辑计划的规则更改

1. 在 **[!UICONTROL Scheduled Changes]** 框中，单击 **[!UICONTROL View/Edit]**.

1. 对计划更新进行任何必要的更改。

1. 单击 **[!UICONTROL Save]**.

## 预览计划的规则更改

1. 在 **[!UICONTROL Scheduled Changes]** 框中，单击 **[!UICONTROL Preview]**.

   预览会打开一个新的浏览器选项卡，加载应用了计划更改的店面。 导航到受更改影响的产品。

   ![预览计划的更改](./assets/price-rule-catalog-scheduled-update-preview.png){width="600" zoomable="yes"}

1. 在“预览”窗口的左上角，单击 **[!UICONTROL Calendar]**.

   日历详细信息显示安排在同一天举行的其他营销活动。 列表中的每条记录都是一个单独的规则更新。

   ![特定日期的计划更新列表](./assets/price-rule-catalog-scheduled-preview-calendar.png){width="600" zoomable="yes"}

1. 要预览不同的日期或时间，请单击 **[!UICONTROL Date & Time]** 日历 ![日历图标](../assets/icon-calendar.png) 并执行以下操作：

   - 选择其他日期和/或时间。

   - 单击 **[!UICONTROL Preview]**.

1. 要返回到日历，请单击 **[!UICONTROL Calendar]** 在预览页面的标题中。

   在此，您可以执行以下操作：

   **共享指向预览的链接**

   要与同事共享商店预览的链接，请单击 **[!UICONTROL Share]**. 将链接复制到剪贴板并将其粘贴到电子邮件正文中。

   >[!NOTE]
   >
   >需要管理员用户帐户才能查看共享预览。 如果您的 [角色具有访问权限](../systems/permissions-user-roles.md) 要创建管理员用户帐户，必须在共享之前为新用户创建该帐户。

   **更改预览范围**

   要查看不同商店视图的计划更改，请单击 **[!UICONTROL Scope]** 在预览页面的标题中。 选择要预览的网站、商店或商店视图。

1. 如有必要，请返回到日历并单击 **[!UICONTROL View/Edit]** 在 _[!UICONTROL Action]_列打开另一个计划的更新。

---
title: 类别的计划更改
description: 了解如何计划类别更改以支持营销活动和商店促销。
exl-id: 9e25082f-4e76-4148-b76e-dca0b14971eb
feature: Catalog Management, Categories
source-git-commit: 74cc26e74c3efabc914c27b6d8327a85a77fd6e6
workflow-type: tm+mt
source-wordcount: '432'
ht-degree: 0%

---

# 类别的计划更改

{{ee-feature}}

类别更新可以按计划应用，并与其他内容更改分组。 您可以根据对类别的计划更改创建营销活动，或将更改应用于现有营销活动。 若要了解详细信息，请参阅[内容暂存](../content-design/content-staging.md)。

>[!NOTE]
>
>[!UICONTROL Schedule Design Update]选项卡已在![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce中移除，无法直接在类别上修改。 您必须为这些激活创建计划的更新。

>[!NOTE]
>
>所有计划的更新都连续应用，这意味着任何实体一次只能有一个计划的更新。 任何计划的更新将应用于其时间范围内的所有存储视图。 因此，一个实体无法同时对不同存储视图进行多次计划更新。 所有存储视图中的所有实体属性值（不受当前计划更新影响）均从默认值获取，而不是从上次计划更新获取。

## 计划类别的更新

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Catalog]** > **[!UICONTROL Categories]**。

1. 在左侧的类别树中，选择要修改的类别。

1. 在页面顶部的&#x200B;_计划更改_&#x200B;框中，单击&#x200B;**[!UICONTROL Schedule New Update]**。

   ![计划的更改](./assets/category-scheduled-changes.png){width="600" zoomable="yes"}

1. 选择&#x200B;**[!UICONTROL Save as a New Update]**&#x200B;选项后，设置更新的基本参数：

   - 为&#x200B;**[!UICONTROL Update Name]**&#x200B;输入新内容暂存营销活动的名称。

   - 输入更新的简短&#x200B;**[!UICONTROL Description]**&#x200B;及其使用方式。

   - 使用日历（ ![日历图标](../assets/icon-calendar.png) ）工具为营销活动选择&#x200B;**[!UICONTROL Start Date]**&#x200B;和&#x200B;**[!UICONTROL End Date]**。

   >[!IMPORTANT]
   >
   >营销活动&#x200B;**[!UICONTROL Start Date]**&#x200B;和&#x200B;**[!UICONTROL End Date]**&#x200B;必须使用从每个网站的本地时区转换而来的&#x200B;**_默认_**&#x200B;管理时区进行定义。 例如，对于位于不同时区的多个网站，如果您希望根据美国时区启动促销活动，则必须为每个本地时区计划单独的更新。 您为每个设置了&#x200B;**[!UICONTROL Start Date]**&#x200B;和&#x200B;**[!UICONTROL End Date]**，它们已从本地网站时区转换为默认的管理时区。

   ![计划的更改](./assets/category-scheduled-changes-new-update.png){width="600" zoomable="yes"}

1. 对计划更新进行任何必要的更改。

1. 要预览更改，请单击右上角按钮栏中的&#x200B;**[!UICONTROL Preview]**。

1. 完成后，单击&#x200B;**[!UICONTROL Save]**。

## 分配给现有更新

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Catalog]** > **[!UICONTROL Categories]**。

1. 在左侧的类别树中，选择要修改的类别。

1. 在页面顶部的&#x200B;_计划更改_&#x200B;框中，单击&#x200B;**[!UICONTROL Schedule New Update]**。

1. 选择&#x200B;**[!UICONTROL Assign to Existing Campaign]**。

1. 在列表中，找到所需的营销活动，然后单击&#x200B;**[!UICONTROL Select]**。

1. 对计划更新进行必要的更改。

1. 完成后，单击&#x200B;**[!UICONTROL Save]**。

   >[!NOTE]
   >
   >如果营销活动链接到多个类别，则只能从[内容暂存仪表板](../content-design/content-staging-dashboard.md)编辑营销活动。
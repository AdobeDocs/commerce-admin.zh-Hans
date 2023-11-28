---
title: 类别 — 设计设置
description: 了解如何使用 [!UICONTROL Design] 用于定义类别、所有关联产品页面和页面布局的外观和感觉的设置。
exl-id: 6dc216ac-1c52-4196-9c93-e5cad19901b5
feature: Catalog Management, Categories, Page Content
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 0%

---

# 类别 — 设计设置

此 _[!UICONTROL Design]_部分允许您控制类别、所有关联产品页面和页面布局的外观。 您可以为促销自定义类别页面及其关联产品，或区分类别。 例如，您可以为某个品牌或某个特定系列的产品开发一种独特的设计，或者针对特定的时间段应用更新。

![类别的设计设置](./assets/category-design.png){width="600" zoomable="yes"}

>[!NOTE]
>
>当同一产品被分配给多个类别，每个类别的设计设置不同时，建议设置 **将类别路径用于产品URL** = `Yes` 在 [搜索引擎优化配置选项](../configuration-reference/catalog/catalog.md#search-engine-optimization). 要访问此设置，请转到  **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**，展开&#x200B;**[!UICONTROL Catalog]**并选择&#x200B;**目录**，然后展开&#x200B;**搜索引擎优化**部分。

| 字段 | 描述 |
|--- |--- |
| [!UICONTROL Use Parent Category Settings] | 允许当前类别从父类别继承设计设置。 如果使用，则“设计”部分中的所有其他字段将变为不可用。 选项： `Yes` / ` No` |
| [!UICONTROL Theme] | 将自定义主题应用于类别。 |
| [!UICONTROL Layout] | 将不同的布局应用于类别页面。 选项： <br/>**[!UICONTROL No layout updates]**— 默认情况下，布局更新不适用于类别页面。<br/>**[!UICONTROL Empty]**  — 使用定义您自己的页面布局。 （需要了解XML。） <br/>**[!UICONTROL 1 column]**— 将一列式布局应用于类别页。<br/>**[!UICONTROL 2 columns with left bar]**  — 将带有左侧栏的双列布局应用于类别页面。 <br/>**[!UICONTROL 2 columns with right bar]**— 将带有右侧栏的双列布局应用于类别页面。<br/>**[!UICONTROL 3 columns]**  — 将三列布局应用于类别页面。<br/>**[!UICONTROL Page -- Full Width]**-(需要 [页面生成器](../page-builder/introduction.md))将CMS页面的全宽布局应用于类别页面。<br/>**[!UICONTROL Category -- Full Width]**  — （需要页面生成器）将类别页面的全宽布局应用于类别页面。 <br/>**[!UICONTROL Product -- Full Width]**— （需要页面生成器）将产品页面的全宽布局应用于类别页面。 |
| [!UICONTROL Custom Layout Update] | 列出服务器上可用的自定义布局更新文件。 选择要应用于类别的自定义布局更新。 |
| [!UICONTROL Apply Design to Products] | 选中后，将自定义设置应用于类别中的所有产品。 |

{style="table-layout:auto"}

## [!UICONTROL Scheduled Design Update]

{{ce-feature}}

此 _[!UICONTROL Scheduled Design Update]_部分确定将自定义设计应用于类别页面时的日期范围。

| 字段 | 描述 |
|--- |--- |
| [!UICONTROL Schedule Update From/To] | 确定将自定义布局应用于类别时的日期范围。 |

![计划的设计更新](./assets/category-scheduled-design-update.png){width="600" zoomable="yes"}

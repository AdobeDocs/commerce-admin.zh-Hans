---
title: 类别 — 显示设置
description: 了解如何使用 [!UICONTROL Display] 用于定义哪些内容元素显示在类别页面上的设置以及产品的显示顺序。
exl-id: bb3a1b00-ba56-4113-8208-860963612333
feature: Catalog Management, Categories, Page Content
source-git-commit: b99212b2c6977fc788e75df4bdce608fc4998dc4
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 0%

---

# 类别 — 显示设置

显示设置确定哪些内容元素显示在类别页面上，以及产品显示的顺序。 您可以启用CMS块、设置类别的锚点状态以及管理分类选项 _[!UICONTROL Display Settings]_选项卡。 有关如何在店面中反映类别的示例，请参阅 [目录导航](navigation.md).

![显示类别设置](./assets/category-display-settings.png){width="600" zoomable="yes"}

| 字段 | 描述 |
|--- |--- |
| [!UICONTROL Display Mode] | 确定类别页面上显示的内容元素。 选项： `Products Only` / `Static Block Only` / `Static Block and Products` |
| [!UICONTROL Anchor] | 当设置为 `Yes`，包括 _[!UICONTROL filter by attribute]_部分。 选项： `Yes` / `No` |
| [!UICONTROL Available Product Listing Sort By] | （必需）默认值为 `Position`， `Name`、和 `Price`. 要自定义排序选项，请取消选择 **[!UICONTROL Use All Available Attributes]** 复选框，然后选择要使用的属性。 您可以根据需要定义和添加属性。 此设置不适用于 [!DNL Live Search] [产品列表页面小组件](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/live-search-storefront/plp-styling). |
| [!UICONTROL Default Product Listing Sort By] | （必需）定义默认值 _[!UICONTROL Sort By]_选项，取消选择&#x200B;**[!UICONTROL Use Config Settings]**复选框，然后选择一个属性。 此设置不适用于 [!DNL Live Search] [产品列表页面小组件](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/live-search-storefront/plp-styling). |
| [!UICONTROL Layered Navigation Price Step] | 默认情况下，Commerce将以10、100和1000为增量显示价格范围，具体取决于列表中的产品。 要更改价格步骤范围，请取消选择 **[!UICONTROL Use Config Settings]** 复选框。 |

{style="table-layout:auto"}

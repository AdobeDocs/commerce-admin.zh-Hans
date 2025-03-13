---
title: 搜索结果
description: 了解如何配置产品如何与在快速搜索框或高级搜索表单中输入的搜索条件相匹配。
exl-id: c721fb3b-ee31-4d2b-b4ea-9ae2c80aa800
feature: Catalog Management, Search
source-git-commit: 5da244a548b15863fe31b5df8b509f8e63df27c2
workflow-type: tm+mt
source-wordcount: '887'
ht-degree: 0%

---

# 搜索结果

>[!NOTE]
>
>此页面介绍与[实时搜索](https://experienceleague.adobe.com/docs/commerce/live-search/overview.html)可能不同的标准搜索功能。

_搜索结果_&#x200B;列表包括与“快速搜索”框或“高级搜索”表单中输入的搜索条件匹配的所有产品。 目录中的每个产品列表基本上具有相同的控件。 唯一的区别是，一个是搜索查询的结果，另一个区别是[导航](navigation.md)的结果。

结果可以格式化为网格或列表，并按属性选择进行排序。 如果页面上的产品超出其容纳范围，则会显示分页控件。 使用这些控件可从一个页面移动到下一个页面。 每页的记录数由目录前端配置决定。 有关详细信息，请参阅[产品列表](navigation-product-listings.md)。

使用&#x200B;**Elasticsearch**：

- 对于后缀的搜索，没有现成的支持。 例如，如果关键字只包含SKU的端部，则按SKU搜索可能不会返回预期结果。
- 仅对`name`和`sku`产品属性现成支持按前缀搜索（部分关键词搜索）。 其他所有产品属性均按整个关键字进行搜索，且完全匹配。
- `name`和`sku`产品属性的搜索结果基于相关性，而不是完全匹配。 最相关的匹配项，例如完全匹配的&#x200B;_产品名称_&#x200B;或&#x200B;_SKU_&#x200B;将列在最前。 要搜索完全匹配项，客户可以在搜索查询中使用双引号。 例如，`WSH12-32-Red`搜索查询可能返回多个产品，按相关性排序。 但是`"WSH12-32-Red"`搜索查询只返回一个产品，**_与_**&#x200B;完全匹配`sku`。

![包含分页控件的搜索结果](./assets/storefront-search-results-shorts.png){width="700" zoomable="yes"}

>[!IMPORTANT]
>
>由于Elasticsearch 7将于2023年8月宣布终止支持，建议所有Adobe Commerce客户迁移到OpenSearch 2.x搜索引擎。 有关在产品升级期间迁移搜索引擎的信息，请参阅&#x200B;_升级指南_&#x200B;中的[迁移到OpenSearch](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/prepare/opensearch-migration.html)。

## 用于扩展搜索结果的关键字映射

此技术使用属性在两个产品之间创建基于关键字的关联，以便搜索任一产品都会返回两个产品的结果。 您可以使用关键词映射来促销搜索结果中的产品，否则不会显示产品。

![关键字映射的搜索结果](./assets/storefront-search-results-extended.png){width="700" zoomable="yes"}

以下示例使用基于SKU的关键字映射。 在搜索框中输入任一SKU后，两个产品都会显示在结果中。 映射以下可配置产品的SKU，而不是产品变体的SKU：

- 蒙大拿风衣(MJ03)
- 查兹袋鼠连帽衫(MH01)

### 步骤1：创建属性

1. 在&#x200B;_[!UICONTROL Products]_列表中，以编辑模式打开`Montana Wind Jacket` (MJ03)。
1. 单击右上角的&#x200B;**[!UICONTROL Add Attribute]**。
1. 在&#x200B;_选择属性_&#x200B;页面上，单击&#x200B;**[!UICONTROL Create New Attribute]**。
1. 按如下方式填写属性属性：

   **[!UICONTROL Attribute Properties]**

   - [!UICONTROL Attribute Label] - `Search Keywords`
   - [!UICONTROL Catalog Input Type for Store Owner] - `Text Field`

   **[!UICONTROL Advanced Attribute Properties]**

   - [!UICONTROL Add to Column Options] - `Yes` （默认）
   - [!UICONTROL Use in Filter Options] - `Yes` （默认）

   **[!UICONTROL Storefront Properties]**

   - [!UICONTROL Use in Search] - `Yes`
   - [!UICONTROL Visible on Catalog Pages in the Storefront] - `No`
   - [!UICONTROL Used in Product Listings] - `No`

1. 完成后，单击&#x200B;**[!UICONTROL Save Attribute]**。

   该属性将添加到产品的属性集中。

### 步骤2：映射第一个产品

1. 在产品设置页面上，向下滚动并展开&#x200B;_[!UICONTROL Attributes]_部分。
1. 在&#x200B;**[!UICONTROL Search Keywords]**&#x200B;字段中，输入要映射到此产品的SKU `MH01`。

   您可以在Search Keywords字段中输入多个以空格分隔的SKU。 在此示例中，只输入一个。

   具有搜索关键字的![Attributes部分](./assets/search-keywords-attribute.png){width="600" zoomable="yes"}

1. 完成后，单击&#x200B;**[!UICONTROL Save]**。
1. 转到&#x200B;**[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**并刷新&#x200B;**[!UICONTROL Page Cache]**。

### 步骤3：映射第二个产品

1. 在&#x200B;_[!UICONTROL Products]_列表中，以编辑模式打开`Chaz Kangaroo Hoodie` (MH01)。
1. 向下滚动并展开&#x200B;**[!UICONTROL Attributes]**&#x200B;部分。
1. 在&#x200B;**[!UICONTROL Search Keywords]**&#x200B;字段中，输入另一个产品`MJ03`的SKU。
1. 单击&#x200B;**[!UICONTROL Save]**。
1. 转到&#x200B;**[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**并刷新&#x200B;**[!UICONTROL Page Cache]**。

### 步骤4：在店面中测试

1. 转到店面并在&#x200B;_快速搜索_&#x200B;框中输入`MJ03`。
1. 验证搜索结果列表中是否返回了这两个产品。

## 加权搜索

可以为为目录搜索启用的产品属性分配权重，以便在搜索结果中赋予它们较高的值。 较重属性的返回先于较轻属性的返回。 例如，如果系统中有两个属性，搜索权重为3的&#x200B;_color_&#x200B;和搜索权重为1的&#x200B;_description_。 对单词&#x200B;_red_&#x200B;的搜索将返回搜索结果顶部颜色属性值为`red`的产品列表，并返回搜索结果底部描述包含单词&#x200B;_red_&#x200B;的产品。 在此示例中，`color`属性的定义权重大于`description`属性。

>[!IMPORTANT]
>
>按相关性排序受&#x200B;**_多个_**&#x200B;标准以及它们之间&#x200B;**_同时_**&#x200B;的关系影响。 [!UICONTROL Search Weight]只是这些条件之一。 这意味着，有时搜索权重较低的属性可能仍比搜索权重较高的属性具有更大的相关性。 其他标准可以包括任何给定属性中的匹配数、找到的搜索词的位置以及搜索词之前和之后的整体文本结构。

**_设置属性的搜索权重属性：_**

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**。

1. 在列表中查找属性并在编辑模式下打开。

1. 在左侧面板中，选择&#x200B;**[!UICONTROL Storefront Properties]**&#x200B;并执行以下操作：

   - 要在搜索查询中包含该属性，请将&#x200B;**[!UICONTROL Use in Search]**&#x200B;设置为`Yes`。

   - 要建立属性的搜索值，请将&#x200B;**[!UICONTROL Search Weight]**&#x200B;设置为从1到10的数字，其中`10`具有最高优先级。 如果未输入值，则所有属性的搜索权重均默认为`1`。

   ![搜索权重](./assets/search-weight.png){width="600" zoomable="yes"}

1. 完成后，单击&#x200B;**[!UICONTROL Save Attribute]**。

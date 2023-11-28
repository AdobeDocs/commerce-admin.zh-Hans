---
title: 分层导航
description: 了解分层导航如何让购物者轻松根据类别、价格范围或任何其他可用属性查找产品。
exl-id: 5f17528a-3593-449c-a044-98736a4ae913
feature: Catalog Management, Categories, Site Navigation
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '1263'
ht-degree: 1%

---

# 分层导航

>[!NOTE]
>
>本节中介绍的标准分层导航与Live Search的过滤导航不同，后者使用 [Facet](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/live-search-admin/facets/facets.html).

通过分层导航，可以轻松地根据类别、价格范围或任何其他可用属性查找产品。 分层导航通常显示在搜索结果和类别页面的左列，有时显示在主页上。 标准导航包括 _购买者_ 类别和价格范围的列表。 您可以配置分层导航的显示，包括产品数量和价格范围。

![按类别和价格划分的分层导航](./assets/navigation-layered-basic.png){width="700" zoomable="yes"}

## 可过滤属性

>[!NOTE]
>
>本主题中描述的可过滤属性要求有所不同 [实时搜索](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/overview.html). 要了解更多信息，请参阅 [Facet](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/live-search-admin/facets/facets.html).

分层导航可用于按类别或属性搜索产品。 例如，当购物者从顶部导航中选择“Mens/Shorts”类别时，初始结果将包括该类别中的所有产品。 可以通过选择特定的样式、气候、颜色、材质、图案或价格或值的组合进一步过滤列表。 可过滤的属性显示在展开部分中，其中列出了每个属性值。 作为一个选项，可以将具有匹配结果的产品列表配置为包含具有或不具有匹配项的产品。

属性属性与产品输入类型相结合，可确定哪些属性可用于分层导航。 分层导航仅适用于 [_锚点_](categories-display-settings.md) 类别，但也可以添加到搜索结果页面。 此 **商店所有者的目录输入类型** 每个属性的属性必须设置为 `Yes/No`， `Dropdown`， `Multiple Select`，或 `Price`. 要使属性可过滤， **在分层导航中使用** 每个的属性必须设置为 `Filterable (with results)` 或 `Filterable (no results)`.

_示例：带有结果的可筛选属性_

![分层导航中的可过滤属性](./assets/storefront-layered-navigation-filtered.png){width="700" zoomable="yes"}

_示例：显示无结果的可筛选样本值_

![无结果的可过滤样本值](./assets/storefront-product-attribute-filter-no-results.png){width="700" zoomable="yes"}

以下说明说明了如何使用可过滤属性设置基本的分层导航。 有关带价格步骤的高级分层导航，请参阅 [价格导航](navigation-layered.md#configure-price-navigation).

## 步骤1：设置属性属性

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. 浏览或使用过滤搜索查找列表中的属性，并在编辑模式下打开该属性。

   ![按列输入搜索词以使用过滤搜索](./assets/attribute-search.png){width="700" zoomable="yes"}

1. 在左侧面板中，选择 **[!UICONTROL Storefront Properties]** 并设置 **[!UICONTROL Use In Layered Navigation]** 更改为以下任一项：

   - `Filterable (with results)`  — 分层导航仅包括那些可找到匹配产品的过滤器。 任何已应用于列表中显示的所有产品的属性值仍应显示为可用过滤器。 可用过滤器列表中省略计数为零(0)产品匹配的属性值。 过滤列表仅包含与过滤器匹配的产品。 仅当选定的过滤器更改了显示的内容时，才会更新产品列表。

   - `Filterable (no results)`  — 分层导航包括所有可用属性值及其产品数的过滤器，包括零(0)产品匹配的产品。 如果属性值是样本，则该值将显示为过滤器，但会被划掉。 此选项不支持价格分层筛选，因此不会影响价格筛选。

1. 设置 **[!UICONTROL Use In Search Results Layered Navigation]** 到 `Yes`.

   ![店面属性](./assets/attribute-storefront-properties.png){width="600" zoomable="yes"}

1. 对要包括在分层导航中的每个属性重复这些步骤。

>[!NOTE]
>
>此 [!UICONTROL Position] 字段默认呈灰显状态，因此您必须先保存属性，然后才能修改此设置。

## 第2步：将类别设置为锚点

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. 在类别树中，选择要使用分层导航的类别。

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Display Settings]** 分区和设置 **[!UICONTROL Anchor]** 到 `Yes`.

   ![类别显示设置](./assets/category-layered-navigation-anchor.png){width="600" zoomable="yes"}

1. 单击 **[!UICONTROL Save]**.

## 第3步：测试结果

要测试设置，请访问您的商店，然后从主菜单导航到类别。 可过滤属性的选择将显示在类别页的分层导航中。

搜索、筛选和查看显示的产品。

## 从分层导航中删除可过滤属性值

分层导航包括所有可用属性值及其产品计数的过滤器，包括零(0)产品匹配的产品（如下图所示）。

![零筛选器显示](./assets/filterable-attributes-on-plp.png){width="700" zoomable="yes"}

这种结果可能会使客户难以选择首选产品，并且无需在前端显示&#x200B;&#x200B;0个产品的属性值。

您可以使用以下步骤从分层导航中删除0 Products的可过滤属性值：

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. 浏览或使用过滤搜索查找列表中的属性，并在编辑模式下打开该属性。

1. 下 _[!UICONTROL Attribute Information]_，单击&#x200B;**[!UICONTROL Storefront Properties]**.

1. 对象 **[!UICONTROL Layered Navigation]**，选择 `Filterable (with results)`.

   ![“属性信息”部分](./assets/storefront-properties-tab.png){width="600" zoomable="yes"}

1. 单击 **[!UICONTROL Save Attribute]**.

## 价格导航

>[!NOTE]
>
>本主题中介绍的价格导航配置有所不同 [实时搜索](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/overview.html).

分层导航中价格导航可用于按价格范围分配产品。 您还可以按间隔拆分每个范围。 有几种方法可计算价格导向：

- 自动（均衡价格范围）
- 自动（均衡产品计数）
- 手动

使用前两种方法可以自动计算导航步骤。 通过手动方法，您可以为价格间隔指定除法限制。 以下示例显示了10个和100个价格导航步骤之间的差异。

迭代拆分提供不同价格范围内产品的最佳分配。 通过迭代拆分，在选择$0.00 -$99的价格范围后，客户可以向下钻取多个价格子范围。 当产品数达到“间隔除法限制”设置的阈值时，价格范围拆分将停止。

## 示例：价格定位步骤

| 价格步进10 | 价格步进100 |
|----------|--------|
| $20.00 - $29.99 (1) | $0.00 - $99.99 (4) |
| $30.00 - $39.99 (2) | $100 - $199.99 (5) |
| $70.00 - $79.99 (1) | $400.00 - $499.99 (2) |
| $100.00 - $109.99 (1) | 700.00美元及以上(1) |
| $120.00 - $129.99 (2) |   |
| $150.00 - $159.99 (1) |   |
| $180.00 - $189.99 (1) |   |
| $420.00 - $429.99 (1) |   |
| $440.00 - $449.99 (1) |   |
| 710.00美元及以上(1) |   |

{style="table-layout:auto"}

## 配置价格导航

>[!IMPORTANT]
>
>正确显示产品及其价格，使产品 _价格过滤器_ 在分层导航中，确保价格的设置显示在 [销售税配置](../configuration-reference/sales/tax.md) 具有相同的值(`Excluding Tax` **或** `Including Tax`)。 对于 _[!UICONTROL Calculation Settings]_，查看&#x200B;**[!UICONTROL Catalog Prices]**值。 和_[!UICONTROL Price Display Settings]_，查看 **[!UICONTROL Display Product Prices in Catalog]** 值。 如果它们的值不同，则分层导航中的价格过滤器可能无法正确过滤和排序产品。

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中，展开 **[!UICONTROL Catalog]** 并选择 **[!UICONTROL Catalog]** 下方。

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 _分层导航_ 部分。

   默认情况下， **[!UICONTROL Display Product Count]** 设置为 `Yes`. 如有必要，请取消选择 **[!UICONTROL Use system value]** 复选框以更改此设置。

   ![分层导航](../configuration-reference/catalog/assets/layered-navigation.png){width="600" zoomable="yes"}

   有关这些配置选项的详细列表，请参见 [分层导航](../configuration-reference/catalog/catalog.md#layered-navigation) 在 _配置引用_.

1. 设置 **[!UICONTROL Price Navigation Steps Calculation]** ，以了解以下部分中的方法之一。

1. 完成后，单击 **[!UICONTROL Save Config]**.

### 方法1：自动（均衡价格范围）

离开 **[!UICONTROL Price Navigation Steps Calculation]** 设置为 `Automatic (Equalize Price Ranges)` （默认）。 此设置使用标准算法进行价格导航。

### 方法2：自动（均衡产品计数）

>[!TIP]
>
>如有必要，请首先取消选择 **[!UICONTROL Use system value]** 复选框以更改这些设置。

1. 设置 **[!UICONTROL Price Navigation Steps Calculation]** 到 `Automatic (equalize product counts)`.

1. 要在多个产品具有相同价格时显示单一价格，请设置 **[!UICONTROL Display Price Interval as One Price]** 到 `Yes`.

1. 对象 **[!UICONTROL Interval Division Limit]**，输入价格范围内产品数量的阈值。

   范围无法进一步拆分，超出此限制。 默认值为 `9`.

   ![自动（均衡产品计数）](../configuration-reference/catalog/assets/layered-navigation-equalize-product-counts.png){width="600" zoomable="yes"}

### 方法3：手动

>[!NOTE]
>
>如有必要，请首先取消选择 **[!UICONTROL Use system value]** 复选框以更改这些设置。

1. 设置 **[!UICONTROL Price Navigation Steps Calculation]** 到 `Manual`.

1. 输入一个值以确定 **[!UICONTROL Default Price Navigation Step]**.

1. 输入 **[!UICONTROL Maximum Number of Price Intervals]** 允许，最多 `100`.

   ![手动](../configuration-reference/catalog/assets/layered-navigation-manual.png){width="600" zoomable="yes"}

## 配置分层导航

>[!NOTE]
>
>此页面中描述的标准配置不同于 [实时搜索](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/overview.html).

分层导航配置确定产品计数是否显示在每个属性后面的括号中，以及价格导航中使用的步骤计算的大小。

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中，展开 _[!UICONTROL Catalog]_部分并选择&#x200B;**[!UICONTROL Catalog]**下方。

1. 展开 _[!UICONTROL Layered Navigation]_部分。

   >[!NOTE]
   >
   >如有必要，请首先取消选择 **[!UICONTROL Use system value]** 复选框以更改这些设置。

1. 要显示为每个属性找到的产品数，请设置 **[!UICONTROL Display Product Count]** 到 `Yes`.

1. 设置 **[!UICONTROL Price Navigation Step Calculation]** 到 `Automatic (equalize price ranges)`.

1. 完成后，单击 **[!UICONTROL Save Config]**.

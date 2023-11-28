---
title: 产品列表
description: 了解如何修改产品列表配置，该配置确定每个页面显示的产品数量，以及使用哪个属性对列表进行排序。
exl-id: 3779d9db-4adb-473b-b9c9-ad066f50b549
feature: Catalog Management, Products, Page Content
source-git-commit: 7ae9955b0283cb7bcd757e7b45fdbc4c3b2181ca
workflow-type: tm+mt
source-wordcount: '795'
ht-degree: 0%

---

# 产品列表

产品清单可以设置为默认显示为列表或网格。 您还可以确定每页显示的产品数量，以及用于对列表进行排序的属性。 产品列表包含一组控件，可用于对产品进行排序、更改列表格式、按属性排序以及从一页前进到下一页。

>[!NOTE]
>
>按产品属性对类别进行排序时，具有相同属性值的产品也会按其属性进行排序 _[!UICONTROL Product ID]_按升序排列。

![显示为网格的产品](./assets/storefront-catalog-page.png){width="700" zoomable="yes"}

## 配置产品列表

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中，展开 **[!UICONTROL Catalog]** 并选择 **[!UICONTROL Catalog]** 下方。

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Storefront]** 部分。

   ![店面配置选项](../configuration-reference/catalog/assets/catalog-storefront.png){width="600" zoomable="yes"}

   有关这些选项的详细列表，请参阅 [店面](../configuration-reference/catalog/catalog.md#storefront) 在 _配置引用_.

   >[!NOTE]
   >
   >正确显示产品及其价格，使产品 _产品按价格排序_，请确保价格的设置显示在 [销售税配置](../configuration-reference/sales/tax.md) 具有相同的值(`Excluding Tax` **或** `Including Tax`)。 对于 _[!UICONTROL Calculation Settings]_，查看&#x200B;**[!UICONTROL Catalog Prices]**值。 和_[!UICONTROL Price Display Settings]_，查看 **[!UICONTROL Display Product Prices in Catalog]** 值。 如果它们的值不同，则分层导航中的价格过滤器可能无法正确过滤和排序产品。

1. 设置默认值 **[!UICONTROL List Mode]** 更改为以下任一项：

   - `Grid Only`
   - `List Only`
   - `Grid (default) / List`
   - `List (default / Grid`

1. 对象 **[!UICONTROL Products per Page on Grid Allowed Values]**，输入以网格格式显示时要每页显示的产品数。

   要输入一组值，请用逗号分隔每个数字。

1. 对象 **[!UICONTROL Products per Page on Grid Default Value]**，输入每页显示在网格中的默认产品数。

1. 对象 **[!UICONTROL Products per Page on List Allowed Values]**，输入在列表格式中显示时要每个页面显示的产品数。

   要输入一组值，请用逗号分隔每个数字。

1. 对象 **[!UICONTROL Products per page on List Default Value]**，输入每个页面在列表中显示的默认产品数量。

1. 设置 **[!UICONTROL Product Listing Sorted by]** 到最初用于对列表进行排序的默认属性。

1. 要允许客户选择列出所有产品，请设置 **[!UICONTROL Allow All Products on Page]** 到 `Yes`.

1. 如果要在客户浏览目录列表时保留所有分页设置，请设置 **[!UICONTROL Remember Category Pagination]** 到 `Yes`.

   启用此设置可确保当购物者从一个类别浏览到另一个类别时，列表或网格中显示的产品数会保留。 默认情况下，此字段设置为 `No` 因为它使用更多缓存存储，并且可能影响搜索引擎对页面进行索引的方式。

1. 如果使用 [平面目录](catalog-flat.md) (**不推荐**)，请执行以下操作：

   - 要显示产品的平面类别列表，请设置 **[!UICONTROL Use Flat Catalog Category]** 到 `Yes`.

   - 要显示平面产品清单，请设置 **[!UICONTROL Use Flat Catalog Product]** 到 `Yes`.

1. 如果要允许类别和产品URL中的媒体资产使用动态引用，请设置 **[!UICONTROL Allow Dynamic Media URLs in Products and Categories]** 到 `Yes`.

1. 完成后，单击 **[!UICONTROL Save Config]**.

## 页面控件

| 控件 | 描述 |
|--- |--- |
| [!UICONTROL View As] | 以网格或列表格式显示产品。 |
| [!UICONTROL Sort By] | 更改列表的排序顺序。 |
| [!UICONTROL Show Per Page] | 确定每页显示的产品数量。 |
| 分页链接 | 导航链接到其他页面。 |

{style="table-layout:auto"}

## 分页控件

“分页”设置显示在列表的顶部和底部，并控制产品清单的分页链接的格式。 您可以设置控件中显示的链接数量，并配置下一个和上一个链接。 要显示分页链接，列表中必须存在比产品列表配置中每页允许的更多的产品。

![分页控件](./assets/storefront-pagination-controls.png){width="700" zoomable="yes"}

### 店面分页控件

| 控件 | 描述 |
|--- |--- |
| ![显示网格](./assets/controls-pagination-list-grid.png) | [!UICONTROL View As]  — 以Grid或List格式显示列表。 |
| ![排序方式](./assets/control-pagination-sort-by.png) | [!UICONTROL Sort By]  — 更改列表的排序顺序。 此 _[!UICONTROL Used for Sorting in Product Listing]_storefront属性确定 [产品属性](../catalog/product-attributes.md) 可用于对列表进行排序。 |
| ![每页显示](./assets/control-pagination-show-per-page.png) | [!UICONTROL Show Per Page]  — 确定每个页面显示的产品数量。 |
| ![分页链接](./assets/control-pagination.png) | 分页链接 — 导航到其他页面的链接。 |

{：style=&quot;table-layout：auto&quot;}

### 配置分页控件

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. 查找要配置的商店视图，并在 **[!UICONTROL Action]** 列，单击 **[!UICONTROL Edit]**.

1. 下 **[!UICONTROL Other Settings]**，展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Pagination]** 部分。

   ![分页](./assets/config-design-pagination.png){width="600" zoomable="yes"}

   有关这些设置的详细信息，请参阅 [设计配置](../content-design/configuration.md).

1. 对象 **[!UICONTROL Pagination Frame]**，输入要在分页控件中显示的链接数。

1. 对象 **[!UICONTROL Pagination Frame Skip]**，输入要在分页控件中显示下一组链接之前预先跳过的链接数。

   例如，如果分页框架有五个链接，而您希望跳转到接下来的五个链接，则您要向前跳过多少个链接？ 如果将值设置为四(`4`)，则上一个集合中的最后一个链接是下一个集合中的第一个链接。

1. 对象 **[!UICONTROL Anchor Text for Previous]**，为上一个链接输入要显示的文本。

   留空将使用默认箭头。

1. 对象 **[!UICONTROL Anchor Text for Next]**，输入要在下一个链接中显示的文本。 留空将使用默认箭头。

1. 完成后，单击 **[!UICONTROL Save Configuration]**.

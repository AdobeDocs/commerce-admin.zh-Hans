---
title: '[!UICONTROL Catalog] &amp；gt； [!UICONTROL Catalog]'
description: 查看Commerce管理员的[!UICONTROL Catalog] &amp；gt； [!UICONTROL Catalog]页面上的配置设置。
exl-id: fc25ae80-aaa7-42c4-bba2-f03d3caa7970
feature: Configuration, Catalog Management
source-git-commit: 20f97d6ab391b7f5675d6790ab2ec5d24e9dda21
workflow-type: tm+mt
source-wordcount: '3261'
ht-degree: 0%

---

# [!UICONTROL Catalog] > [!UICONTROL Catalog]

{{config}}

## [!UICONTROL Product Fields Auto-Generation]

![产品字段自动生成](./assets/catalog-product-fields-auto-generation.png)<!-- zoom -->

<!-- [Product Fields Auto-Generation](https://experienceleague.adobe.com/zh-hans/docs/commerce-admin/catalog/products/product-workspace#default-field-values) -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Mask for SKU] | 全局 | 根据其他字段中的占位符值和输入的任何附加文本确定SKU字段的默认值。 默认占位符： <br/>产品名称 — `{{name}}` |
| [!UICONTROL Mask for Meta Title] | 全局 | 根据其他字段中的占位符值和输入的任何其他文本确定元标题字段的默认值。 默认占位符： <br/>产品名称 — `{{name}}` |
| [!UICONTROL Mask for Meta Keywords] | 全局 | 根据其他字段中的占位符值和输入的任何其他文本确定&#x200B;_元关键字_&#x200B;字段的默认值。 默认占位符： <br/>产品名称 — `{{name}}` |
| [!UICONTROL Mask for Meta Description] | 全局 | 根据其他字段中的占位符值和输入的任何其他文本确定元描述字段的默认值。 默认占位符： <br/>产品名称 — `{{name}}` <br/>描述 — `{{description}}` |

{style="table-layout:auto"}

## [!UICONTROL Product Reviews]

![产品评论](./assets/catalog-product-reviews.png)<!-- zoom -->

<!-- [Product Reviews](https://experienceleague.adobe.com/zh-hans/docs/commerce-admin/marketing/merchandising/product-reviews/product-reviews) -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Enabled] | 商店视图 | 启用产品审查。 选项： `Yes` / `No` |
| [!UICONTROL Allow Guests to Write Reviews] | 网站 | 确定客户是否必须在您的商店中开立帐户才能编写产品评论。 |

{style="table-layout:auto"}

## [!UICONTROL Storefront]

![店面](./assets/catalog-storefront.png)<!-- zoom -->

<!-- [Storefront](https://experienceleague.adobe.com/zh-hans/docs/commerce-admin/catalog/catalog/navigation/navigation-product-listings) -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL List Mode] | 商店视图 | 确定搜索结果列表的格式。 选项： <br/>**`Grid Only`**— 将列表设置为行和列的网格。 每个产品都显示在网格的单个单元格中。<br/>**`List Only`** — 将列表与每个产品一起格式化为单独的一行。 <br/>**`Grid (default / List)`**— 默认情况下，产品显示在网格视图中，并且可以切换到“列表”视图。<br/>**`List (default / Grid)`** — 默认情况下，产品会显示在列表视图中，并且可以切换到“网格”视图。 |
| [!UICONTROL Products per Page on Grid Allowed Values] | 商店视图 | 确定在网格视图中显示的产品数。 要提供选项选择，请输入多个值，值之间用逗号分隔。 |
| [!UICONTROL Products per Page on Grid Default Value] | 商店视图 | 确定网格视图中默认每页显示的产品数。 |
| [!UICONTROL Products per Page on List Allowed Values] | 商店视图 | 确定在列表视图中显示的产品数。 要提供选项选择，请输入多个值，值之间用逗号分隔。 |
| [!UICONTROL Products per Page on List Default Value] | 商店视图 | 确定在列表视图中默认每页显示的产品数。 |
| 产品列表排序方式 | 商店视图 | 确定搜索结果列表的排序顺序。 选项的选择由类别的显示设置以及设置为`Used for Sorting in Product Listing`的可用属性决定。 默认值设置为`Use All Available Attributes`，通常包括最佳值、名称和价格。 此设置不适用于[!DNL Live Search] [产品列表页面小组件](https://experienceleague.adobe.com/zh-hans/docs/commerce/live-search/live-search-storefront/plp-styling)。 |
| [!UICONTROL Allow All Products per Page] | 商店视图 | 如果设置为`Yes`，则在“每页显示”控件中包含`ALL`选项。 |
| [!UICONTROL Remember Category Pagination] | 全局 | 如果设置为`Yes`，则保存当前类别分页值，因为客户在[产品列表](../../catalog/navigation-product-listings.md)中从一个类别浏览到另一个类别。 保存该值将使用更多缓存存储，并且可能会影响搜索引擎为页面编制索引的方式。 选项： `Yes` / `No` （默认） |
| [!UICONTROL Use Flat Catalog Category] | 全局 | 启用[平面类别结构](../../catalog/catalog-flat.md)（不推荐）。 选项： `Yes` / `No` |
| [!UICONTROL Use Flat Catalog Product] | 全局 | 启用平整产品结构。 （不推荐）选项： `Yes` / `No` |
| [!UICONTROL Swatches per Product] | 商店视图 | 确定每个产品可用的样本数。 默认： `16` |
| [!UICONTROL Show Swatches in Product List] | 商店视图 | 确定色板是否显示在“产品列表”中。 选项： `Yes` / `No` |
| [!UICONTROL Show Swatch Tooltip] | 商店视图 | 确定是否显示样本工具提示。 选项： `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Product Alerts]

![产品警报](./assets/catalog-product-alerts.png)<!-- zoom -->

<!-- [Product Alerts](https://experienceleague.adobe.com/zh-hans/docs/commerce-admin/inventory/configuration/product-alerts/alert-setup) -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Allow Alerts When Product Price Changes] | 商店视图 | 确定电子邮件警报是否可用于产品价格更改。 选项： `Yes` / `No` |
| [!UICONTROL Price Alert Email Template] | 商店视图 | 标识用于产品价格更改电子邮件提醒的模板。 默认模板： `Product price alert` |
| [!UICONTROL Allow Alert When Product Comes Back in Stock] | 网站 | 确定客户是否可以选择在产品重新上架时收到警报。 选项： `Yes` / `No` |
| [!UICONTROL Stock Alert Email Template] | 商店视图 | 标识用于库存警报电子邮件通知的模板。 默认模板： `Product stock alert` |
| [!UICONTROL Alert Email Sender] | 商店视图 | 确定显示为产品警报电子邮件发件人的商店联系人。 选项： `General Contact` / `Sales Representative` / `Customer Support` / `Custom Email` |

{style="table-layout:auto"}

## [!UICONTROL Product Alerts Run Settings]

![产品警报运行设置](./assets/catalog-product-alerts-run-settings.png)<!-- zoom -->

<!-- [Product Alerts Run Settings](https://experienceleague.adobe.com/zh-hans/docs/commerce-admin/inventory/configuration/product-alerts/alert-setup) -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Frequency] | 全局 | 选择发送产品警报的频率。 选项： `Daily` / `Weekly` / `Monthly` |
| [!UICONTROL Start Time] | 全局 | 选择产品警报流程在一天中的哪个时间开始。 此时间应在执行任何价格或库存更新之后。 |
| [!UICONTROL Error Email Recipient] | 全局 | 确定在产品警报过程中发生错误时应接收电子邮件通知的人员（通常是商店管理员）的电子邮件地址。 |
| [!UICONTROL Error Email Sender] | 全局 | 选择电子邮件为`from`的角色。 |
| [!UICONTROL Error Email Template] | 全局 | 选择用于产品警报错误通知的电子邮件模板。 |

{style="table-layout:auto"}

## [!UICONTROL Product Image Placeholders]

![产品图像占位符](./assets/catalog-product-image-placeholders.png)<!-- zoom -->

<!-- [Product Image Placeholders](https://experienceleague.adobe.com/zh-hans/docs/commerce-admin/catalog/products/digital-assets/product-image-config#image-placeholders) -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Base Image] | 商店视图 | 标识为基本映像选择的占位符文件。 |
| [!UICONTROL Small Image] | 商店视图 | 标识为小图像选择的占位符文件。 |
| [!UICONTROL Swatch] | 商店视图 | 标识为样本选择的占位符文件。 |
| [!UICONTROL Thumbnail] | 商店视图 | 标识为缩略图选择的占位符文件。 |
| [!UICONTROL Choose File] |  | 导航到文件并将其作为类型的占位符图像上传。 |

{style="table-layout:auto"}

## [!UICONTROL Recently Viewed/Compared Products]

![最近查看/比较的产品](./assets/catalog-recently-viewed-and-compared-products.png)<!-- zoom -->

<!-- Recently Viewed/Compared Products](https://experienceleague.adobe.com/zh-hans/docs/commerce-admin/stores-sales/shopper-tools/products-viewed-compared) -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Synchronize widget products with backend storage] | 全局 | 确定产品小部件信息（如产品ID）与数据库的同步。 这允许在其他设备上重复使用信息。 |
| [!UICONTROL Show for Current] | 网站 | 限制在当前网站上显示的产品。 选项： `Website` / `Store` / `Store View` |
| [!UICONTROL Default Recently Viewed Products Count] | 商店视图 | 确定列表中最近查看的产品的最大数量。 |
| [!UICONTROL Default Recently Compared Products Count] | 商店视图 | 确定列表中显示的最近比较产品的最大数量。 |
| [!UICONTROL Lifetime of products in Recently Viewed Widget] | 全局 | 确定已查看的产品在“最近查看的项目”列表中显示的时长（以秒为单位）。 |
| [!UICONTROL Lifetime of products in Recently Compared Widget] | 全局 | 确定最近比较的列表中显示所比较产品的时间（以秒为单位）。 |

{style="table-layout:auto"}

## [!UICONTROL Product Video]

![产品视频](./assets/catalog-product-video.png)<!-- zoom -->

<!-- [Product Videos](https://experienceleague.adobe.com/zh-hans/docs/commerce-admin/catalog/products/digital-assets/product-video) -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL YouTube API key] | 商店视图 | 指定连接到YouTube服务器所需的API密钥。 |
| [!UICONTROL Autostart base video] | 商店视图 | 要在页面加载后自动启动视频，请将设置为`Yes`。 |
| [!UICONTROL Show related video] | 商店视图 | 要显示相关视频，请设置为`Yes`。 |
| [!UICONTROL Auto restart video] | 商店视图 | 要启用自动重播视频，请设置为`Yes`。 |

{style="table-layout:auto"}

## [!UICONTROL Price]

![价格](./assets/catalog-price.png)<!-- zoom -->

<!--Price](https://experienceleague.adobe.com/zh-hans/docs/commerce-admin/catalog/products/pricing/catalog-price-scope) -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Catalog Price Scope] | 全局 | 确定基本货币的范围。 选项： `Global` / `Website` |
| [!UICONTROL Default Product Price] | 全局 | ![Adobe Commerce](../../assets/adobe-logo.svg)(仅限Adobe Commerce)定义默认产品价格（如果适用）。 |

{style="table-layout:auto"}

## [!UICONTROL Layered Navigation]

>[!NOTE]
>
>此部分中描述的标准搜索配置与[实时搜索](https://experienceleague.adobe.com/docs/commerce/live-search/overview.html?lang=zh-Hans)不同。

<!-- [Layered Navigation - Automatic (equalize price ranges)](https://experienceleague.adobe.com/zh-hans/docs/commerce-admin/catalog/catalog/navigation/navigation-layered#configure-layered-navigation) -->

![分层导航 — 自动（均衡价格范围）](./assets/layered-navigation-equalize-price-range.png)<!-- zoom -->

![分层导航 — 自动（均衡产品计数）](./assets/layered-navigation-equalize-product-counts.png)<!-- zoom -->

![分层导航 — 手动](./assets/layered-navigation-manual.png)<!-- zoom -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Display Product Count] | 商店视图 | 确定产品计数是否显示在每个属性、价格范围和类别之后。 选项： `Yes` / `No` |
| [!UICONTROL Price Navigation Step Calculation] | 商店视图 | 确定用于确定[价格导航步骤](../../catalog/navigation-layered.md#configure-price-navigation)的方法。 选项： <br/>`Automatic (equalize price ranges)` — 根据组中产品的价格范围进行计算。 <br/>`Automatic (equalize product counts)` — 根据组中的产品数进行计算。 设置组中最小产品数量的阈值，以防止将产品划分为较小的组。 <br/>`Manual` — 使用您为价格间隔输入的除数限制。 |
| [!UICONTROL Default Price Navigation Step] | 商店视图 | 确定每个步骤中包含的产品数量。 |
| [!UICONTROL Maximum Number of Price Intervals] | 商店视图 | 建立对分层导航中显示的价格间隔数量的限制。 |

{style="table-layout:auto"}

## [!UICONTROL Category Permissions]

{{ee-feature}}

![类别权限](./assets/catalog-category-permissions.png)<!-- zoom -->

<!-- [Category Permissions](https://experienceleague.adobe.com/zh-hans/docs/commerce-admin/catalog/categories/category-permissions) -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Enable] | 全局 | 激活类别限制。 默认情况下，使用此功能会限制所有类别。 选项： `Yes` / `No` |
| [!UICONTROL Allow Browsing Category] | 网站 | 确定允许浏览类别的人员。 选项： <br/>`Yes, for Everyone` — 允许所有访客和客户浏览类别。 <br/>`Yes, for Specified Customer Groups` — 仅允许所选客户组的成员浏览类别。 <br/>`No, Redirect to Landing Page` — 拒绝对类别的访问，并重定向到所选页面。 |
| [!UICONTROL Display Product Prices] | 网站 | 控制类别的产品价格的显示。 选项： <br/>`Yes, for Everyone` — 允许每个人查看类别中产品的价格。 <br/>`Yes, for Specified Customer Groups` — 仅允许所选客户组的成员查看类别中的产品价格。 <br/>`No` — 关闭该类别的产品价格显示。 |
| [!UICONTROL Allow Adding to Cart] | 网站 | 确定谁可以从类别中购买产品。 选项： <br/>`Yes, for Everyone` — 允许每个人将该类别中的产品放入其购物车。 <br/>`Yes, for Specified Customer Groups` — 仅允许所选客户组的成员将产品从类别放入其购物车。 <br/>`No` — 不允许任何人将类别中的产品放入其购物车。 |
| [!UICONTROL Disallow Catalog Search by] | 网站 | 标识不允许在类别中搜索产品的客户组。 |

{style="table-layout:auto"}

## [!UICONTROL Search Engine Optimization]

![搜索引擎优化](./assets/catalog-search-engine-optimization.png)<!-- zoom -->

<!-- [Search Engine Optimization](https://experienceleague.adobe.com/zh-hans/docs/commerce-admin/catalog/products/settings/product-search-engine-optimization) -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Popular Search Terms] | 商店视图 | 确定存储中是否实施了&#x200B;_常用搜索词_。 此设置不适用于使用[实时搜索](https://experienceleague.adobe.com/docs/commerce/live-search/overview.html?lang=zh-Hans)的商店。 选项： `Enable` / `Disable` |
| [!UICONTROL Product URL Suffix] | 商店视图 | 确定是否将后缀（如html或htm）应用于产品URL。 如果使用后缀，请不要在后缀前添加句点，因为它会自动应用。 |
| [!UICONTROL Category URL Suffix] | 商店视图 | 确定是否将后缀（如html或htm）应用于类别URL。 如果使用后缀，请不要在后缀前添加句点，因为它会自动应用。 |
| [!UICONTROL Use Categories Path for Product URLs] | 商店视图 | 确定店面的产品URL中是否包含类别路径。 这样做会导致多个URL指向同一页面，这可能会影响搜索排名。 若要了解更多信息，请参阅[Canonical meta标记](../../merchandising-promotions/meta-data.md#canonical-meta-tag)。 |
| [!UICONTROL Create Permanent Redirect for URLs if URL Key Changed] | 商店视图 | 确定每当URL键发生更改时是否自动创建永久重定向。 实施后，默认情况下会选中产品URL密钥字段下方的创建旧URL的自定义重定向复选框。 选项： `Yes` / `No` |
| [!UICONTROL Generate "category/product" URL Rewrites] | 全局 | 确定Adobe Commerce在保存包含许多已分配产品的类别时，是否生成数据并将其保存到重写表中。  <br/><br/>更改此选项不会影响Adobe Commerce中产品URL的解析方式，因为无论此设置如何，系统都会自动解析产品URL。 <br/><br/>选项： `Yes` / `No` <br/><br/>**_重要信息：_**&#x200B;将此生成的数据保存到URL重写表中可能会降低性能。 有关详细信息，请参阅[自动产品重定向](../../merchandising-promotions/url-redirect-product-automatic.md)。 |
| [!UICONTROL Apply transliteration for product URL] | 商店视图 | 确定在创建或更新产品URL时是否应用音译。 选项： `Yes` / `No`。 默认设置为`Yes`。 <br/><br/>对于某些用例，应禁用音译。 例如，如果您以中文经营在线商店，SEO最佳实践建议产品URL与产品名称匹配。 将选项设置为`No`可允许在产品URL中使用中文字符，而不是ASCII等效字符。 |
| [!UICONTROL Page Title Separator] | 商店视图 | 标识用于分隔浏览器标题栏中类别名称和子类别的字符。 |
| [!UICONTROL Use Canonical Link Meta Tag for Categories] | 商店视图 | 如果有多个URL指向同一类别页面，则此选项使用规范meta标记来标识搜索引擎应索引的类别URL。 URL包含使用meta标记的类别的全名。 这减少了重复内容并改善了SEO。 选项： `Yes` / `No` |
| [!UICONTROL Use Canonical Link Meta Tag for Products] | 商店视图 | 如果有多个URL指向同一产品页面，则此选项使用规范meta标记来标识搜索引擎应索引的产品URL。 URL包含使用meta标记的产品全名。 这减少了重复内容并改善了SEO。 选项： `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Category Top Navigation]

![类别顶部导航](./assets/catalog-category-top-navigation.png)<!-- zoom -->

<!-- Category Top Navigation](https://experienceleague.adobe.com/zh-hans/docs/commerce-admin/catalog/catalog/navigation/navigation-top) -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Maximal Depth] | 全局 | 确定顶部导航中的子类别级别数。 默认值`0`对级别数没有限制。 |

{style="table-layout:auto"}

## [!UICONTROL Catalog Search]

您可以使用Adobe Commerce支持的[[!DNL Live Search]](https://experienceleague.adobe.com/docs/commerce/live-search/overview.html?lang=zh-Hans)或第三方搜索引擎服务配置目录搜索。 按照安装说明操作。

### Adobe Commerce与[!DNL Live Search]

安装Live Search后， Catalog Search包含以下配置设置：

![实时搜索的目录搜索](./assets/catalog-search-live-search.png)<!-- zoom -->

<!-- [Catalog Search for Live Search](https://experienceleague.adobe.com/zh-hans/docs/commerce-admin/catalog/catalog/search/search-configuration) -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Minimal Query Length] | 商店视图 | 目录搜索中允许的最小字符数。 为此选项设置的值必须与Elasticsearch搜索引擎配置中设置的相应范围兼容。 例如，如果您在Adobe Commerce中将此值设置为`2`，请更新搜索引擎中的值。 |
| [!UICONTROL Maximum Query Length] | 商店视图 | 目录搜索中允许的最大字符数。 为此选项设置的值必须与Elasticsearch搜索引擎配置中设置的相应范围兼容。 例如，如果在Adobe Commerce中将此值设置为300，则更新搜索引擎中的值。 |
| [!UICONTROL Number of top search results to cache] | 商店视图 | 要缓存以加快响应的常用搜索词和结果的数量。 再次输入值`0`将缓存所有搜索词和结果。 默认值： `100` |
| [!UICONTROL Autocomplete Limit] | 商店视图 | 确定[店面弹出框]页面中可用的最大行数。 默认值可以在安装Live Search时更改，并稍后通过更改此配置设置进行更新。 默认值： `8` |

{style="table-layout:auto"}

### 第三方搜索引擎

Adobe Commerce支持OpenSearch和Elasticsearch。 Adobe Commerce版本2.3.7-p3、2.4.3-p2、2.4.4及更高版本支持OpenSearch服务。 云基础架构项目上的Adobe Commerce不支持Elasticsearch 7.11及更高版本。 内部安装仍支持Elasticsearch。

>[!IMPORTANT]
>
>- 由于Elasticsearch 7将于2023年8月宣布终止支持，Adobe建议所有Adobe Commerce客户迁移到OpenSearch 2.x搜索引擎。 有关升级期间迁移搜索引擎的信息，请参阅&#x200B;_升级指南_&#x200B;中的[迁移到OpenSearch](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/prepare/opensearch-migration.html?lang=zh-Hans)。
>- 在版本2.4.4和2.4.3-p2中，所有标记为Elasticsearch的字段也适用于OpenSearch。 当版本2.4.6中引入对Elasticsearch 8.x的支持时，创建了新标签以区分Elasticsearch和OpenSearch配置。 但是，两者的配置选项是相同的。

![目录搜索配置选项](./assets/catalog-search-opensearch.png){zoomable="yes"}

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Minimal Query Length] | 商店视图 | 目录搜索中允许的最小字符数。 为该选项设置的值必须与OpenSearch或Elasticsearch配置中设置的相应范围兼容。 例如，如果您在Adobe Commerce中将此值设置为`2`，则还必须更新搜索引擎配置中的值。 默认值： `3` |
| [!UICONTROL Maximum Query Length] | 商店视图 | 目录搜索中允许的最大字符数。 为该选项设置的值必须与OpenSearch或Elasticsearch配置中设置的相应范围兼容。 例如，如果您在Adobe Commerce中将此值设置为`300`，则必须更新搜索引擎配置中的值。 默认值： `128` |
| [!UICONTROL Number of top search results to cache] | 商店视图 | 要缓存以加快响应的常用搜索词和结果的数量。 再次输入值`0`将缓存所有搜索词和结果。 默认值： `100` |
| [!UICONTROL Enable EAV Indexer] | 全局 | 确定是否启用或禁用Product EAV索引器。 此功能可提高索引速度并限制索引器不被第三方扩展使用。 默认选项： `Yes`已启用 |
| [!UICONTROL Autocomplete Limit] | 商店视图 | 搜索自动完成的搜索字段下方显示的最大搜索查询数。 限制此数量可提高搜索性能并减小显示的列表大小。 默认值： `8` |
| 搜索引擎 | 全局 | 标识处理目录数据请求所需的搜索引擎。 OpenSearch和Elasticsearch的搜索引擎配置选项相同。 选项： `OpenSearch`或`Elasticsearch` |
| [!UICONTROL OpenSearch Server Hostname] | 全局 | 指定OpenSearch或Elasticsearch主机服务器的名称。 |
| [!UICONTROL OpenSearch Server Port] | 全局 | 指定OpenSearch或Elasticsearch使用的服务器端口号。 默认值： `9200` |
| [!UICONTROL OpenSearch Index Prefix] | 全局 | 分配前缀以标识OpenSearch或Elasticsearch索引。 默认值： `magento2` |
| [!UICONTROL Enable OpenSearch HTTP Auth] | 全局 | 如果启用，在访问OpenSearch或Elasticsearch服务器之前，会使用HTTP身份验证提示输入用户名和密码。 选项： `Yes` / `No` |
| [!UICONTROL OpenSearch HTTP Username] | 全局 | 当&#x200B;_启用Elasticsearch HTTP身份验证_&#x200B;设置为`Yes`时，指定OpenSearch或Elasticsearch HTTP身份验证的用户名。 |
| [!UICONTROL OpenSearch HTTP Password] | 全局 | 当&#x200B;_启用Elasticsearch HTTP身份验证_&#x200B;设置为`Yes`时，指定OpenSearch或Elasticsearch HTTP身份验证的密码。 |
| [!UICONTROL OpenSearch Server Timeout] | 全局 | 确定对OpenSearch或Elasticsearch服务器的请求超时之前的秒数。 默认值： `15` |
| [!UICONTROL Test Connection] |  | 验证OpenSearch或Elasticsearch连接。 |
| [!UICONTROL Enable Search Recommendations] | 商店视图 | 确定当搜索未返回任何结果且显示在搜索结果页面的`Related search terms`部分下时，是否提供搜索推荐。 选项： `Yes` / `No` <br/>当设置为“是”时，将显示&#x200B;_[!UICONTROL Search Recommendations Count]_&#x200B;和&#x200B;_[!UICONTROL Shows Results Count for Each Recommendation]_&#x200B;的其他选项。 |
| [!UICONTROL Search Recommendations Count] | 商店视图 | 指定作为推荐提供的搜索词的数量。 默认情况下，显示的数量不超过5个。 |
| [!UICONTROL Show Results Count for Each Recommendation] | 商店视图 | 当设置为`Yes`时，为建议的搜索推荐找到的产品数显示在括号中。 选项： `Yes` / `No` |
| [!UICONTROL Enable Search Suggestions] | 商店视图 | 确定是否显示搜索建议以查找常见的拼写错误。 启用后，将针对未返回任何结果且显示在&#x200B;**搜索结果**&#x200B;页面的`Did you mean`部分下的任何请求提供搜索建议。 搜索建议可能会影响搜索的性能。 当设置为`Yes`时，为“启用搜索推荐”和相关字段显示其他选项。 选项： `Yes` / `No` |
| [!UICONTROL Search Suggestions Count] | 商店视图 | 确定提供的搜索建议数。 例如： `2` |
| [!UICONTROL Show Results Count for Each Suggestion] | 商店视图 | 确定是否显示每个建议的搜索结果数。 根据主题，编号通常显示在建议后的括号中。 选项： `Yes` / `No` |
| [!UICONTROL Minimum Terms to Match] | 商店视图 | 指定一个值，该值对应于查询中搜索结果应匹配以便返回的术语数。 这可确保为购物者提供最佳结果相关性。 百分比值与数字相关，如果需要，可以向下舍入并用作查询中要匹配的最小术语数。 该值可以是负整数或正整数、负百分比或正百分比、两个值的组合或多个组合。 若要了解详细信息，请参阅OpenSearch文档中的[minimum_should_match参数](https://opensearch.org/docs/latest/query-dsl/minimum-should-match/)。 |

## [!UICONTROL Downloadable Product Options]

![可下载的产品选项](./assets/catalog-downloadable-product-options.png)<!-- zoom -->

<!-- [Downloadable Product Options](https://experienceleague.adobe.com/zh-hans/docs/commerce-admin/catalog/products/types/product-create-downloadable#configure-the-download-options) -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Order Item Status to Enable Downloads] | 网站 | 确定订单在下载可用之前必须具备的状态。 选项： `Pending` / `Invoiced` |
| [!UICONTROL Default Maximum Number of Downloads] | 网站 | 确定客户可用的默认下载次数。 |
| [!UICONTROL Shareable] | 网站 | 确定客户是否必须登录其帐户才能访问下载链接。 选项： <br/>**是** — 允许通过电子邮件发送链接，然后可以与其他人共享。 <br/>**否** — 需要客户登录其帐户才能访问下载链接。 |
| [!UICONTROL Default Sample Title] | 商店视图 | 所有示例文件的默认标题。 |
| [!UICONTROL Default Link Title] | 商店视图 | 所有可下载标题的默认链接。 |
| [!UICONTROL Opens Links in New Window] | 网站 | 确定下载链接是否会在新的浏览器窗口中打开。 选项： `Yes` / `No` |
| [!UICONTROL Use Content Disposition] | 商店视图 | 确定指向可下载内容的链接在浏览器窗口中如何作为电子邮件附件或内联链接投放。 选项： <br/>**`Attachment`**— 下载链接作为电子邮件附件传送。<br/>**`Inline`** — 下载链接作为网页上的内联链接提供。 |
| [!UICONTROL Disable Guest Checkout if Cart Contains Downloadable Items] | 网站 | 确定购买可下载产品的来宾是否必须注册帐户并登录才能完成结帐过程。 选项： <br/>**`Yes`**— 如果购物车包含可下载的产品，则访客必须注册帐户或登录到现有帐户才能完成购买。<br/>**`No`** — 下载链接作为电子邮件正文中的内联链接投放。 <br/> _&#x200B;**注意：**&#x200B;_&#x200B;仅当“可共享”设置为`Yes`时，才能对下载的产品进行访客签出。 |

{style="table-layout:auto"}

## [!UICONTROL Date & Time Custom Options]

![日期和时间自定义选项](./assets/catalog-date-time-custom-options.png)<!-- zoom -->

<!-- Date & Time Custom Options](https://experienceleague.adobe.com/zh-hans/docs/commerce-admin/catalog/product-attributes/attributes-input-types#date-and-time-options) -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Use JavaScript Calendar] | 商店视图 | 确定是否将JavaScript日历用作日期字段的输入控件。 选项： `Yes` / `No` <br/>如果设置为`No`，则日期字段的每个部分都将显示一个单独的下拉列表。 |
| [!UICONTROL Date Fields Order] | 商店视图 | 建立三个日期字段的顺序。 选项： `Day` / `Month` / `Year` |
| [!UICONTROL Time Format] | 商店视图 | 将时间格式设置为12或24小时时钟。 选项： `12h AM/PM` / `24h` |
| [!UICONTROL Year Range] | 商店视图 | 定义显示在&#x200B;_年_&#x200B;字段中的年的开始和结束范围。 必须以YYYY格式输入值。 |

{style="table-layout:auto"}

## [!UICONTROL Catalog Events]

{{ee-feature}}

![目录事件](./assets/catalog-events.png)<!-- zoom -->

<!-- [Catalog Events](https://experienceleague.adobe.com/zh-hans/docs/commerce-admin/marketing/promotions/events/events-private-sales) -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Enable Catalog Events Functionality] | 网站 | 确定是否启用事件模块。 |
| [!UICONTROL Enable Catalog Event Widget on Frontend] | 商店视图 | 确定店面中是否有事件小部件。 这是一个静态块，其中包含有关网站中事件的信息。 |
| [!UICONTROL Number of Events to be Displayed in the Event Slider Widget] | 商店视图 | 确定在类别页面上的事件滑块构件中显示的事件数。 要覆盖，请使用`limit="x"`变量。 |
| [!UICONTROL Events to Scroll per Click in Event Slider Widget] | 商店视图 | 确定在CMS页面（如主页）上的事件滑块构件中显示的事件数。 要覆盖，请使用`scroll="x"`变量。 |

{style="table-layout:auto"}

## [!UICONTROL Rule-Based Product Relations]

{{ee-feature}}

![基于规则的产品关系](./assets/catalog-rule-based-product-relations.png)<!-- zoom -->

<!-- [Rule-Based Product Relations](https://experienceleague.adobe.com/zh-hans/docs/commerce-admin/marketing/promotions/product-relationships/product-related-rules) -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Maximum Number of Products in Related Products List] | 全局 | 确定&#x200B;_相关产品_&#x200B;列表中可以显示的最大产品数。 |
| [!UICONTROL Show Related Products] | 全局 | 确定商店中显示的相关产品列表。 它可以是在“产品信息”中手动选择的列表、为响应产品关系规则而生成的列表，也可以是两者的组合。 选项： `Both Selected and Rule-Based` / `Selected Only` / `Rule-Based Only` |
| [!UICONTROL Rotation Mode for Products in Related Products List] | 全局 | 确定&#x200B;_相关产品_&#x200B;列表中的产品出现的顺序。 选项： `Do not rotate` / `Shuffle` |
| [!UICONTROL Maximum Number of Products in Cross-Sell Product List] | 全局 | 确定交叉销售列表中可以显示的产品的最大数量。 |
| [!UICONTROL Show Cross-Sell Products] | 全局 | 确定商店中显示的交叉销售产品列表。 它可以是在“产品信息”中手动选择的列表、为响应产品关系规则而生成的列表，也可以是两者的组合。 选项： `Both Selected and Rule-Based` / `Selected Only` / `Rule-Based Only` |
| [!UICONTROL Rotation Mode for Products in Cross-Sell Products List] | 全局 | 确定“交叉销售产品”列表中产品的显示顺序。 选项：不旋转/随机播放 |
| [!UICONTROL Maximum Number of Products in Upsell Product List] | 全局 | 确定在&#x200B;_追加销售产品_&#x200B;列表中可以显示的最大产品数。 |
| [!UICONTROL Show Upsell Products] | 全局 | 确定商店中显示的追加销售产品列表。 它可以是在“产品信息”中手动选择的列表、为响应产品关系规则而生成的列表，也可以是两者的组合。 选项： `Both Selected and Rule-Based` / `Selected Only` / `Rule-Based Only` |
| [!UICONTROL Rotation Mode for Products in Upsell Product List] | 全局 | 确定追加销售产品列表中产品的显示顺序。 选项： `Do not rotate` / `Shuffle` |

{style="table-layout:auto"}

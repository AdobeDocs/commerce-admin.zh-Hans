---
title: 配置目录搜索
description: 了解如何为应用商店配置目录搜索。
exl-id: b4f22bce-39e2-4269-99a4-eb2d647df939
feature: Catalog Management, Search
source-git-commit: 1f84bf9ab20aeccacf56eab396b2778140964d17
workflow-type: tm+mt
source-wordcount: '755'
ht-degree: 0%

---

# 配置目录搜索

目录搜索配置有两种变体。 第一种方法描述以下情况下可用的设置： [实时搜索](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/overview.html) 已安装。 第二种方法描述使用进行的本机Adobe Commerce的配置设置 [Elasticsearch][1]{：target=&quot;_blank&quot;}.

## 方法1：Adobe Commerce与 [!DNL Live Search]

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中，展开 **[!UICONTROL Catalog]** 并选择 **[!UICONTROL Catalog]** 下方。

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Catalog Search]** 部分。

   ![实时搜索的目录搜索](../configuration-reference/catalog/assets/catalog-search-live-search.png){width="600" zoomable="yes"}

   有关这些选项的详细列表，请参阅 [包含Live Search的Adobe Commerce](../configuration-reference/catalog/catalog.md#adobe-commerce-with-live-search) 在 _配置引用_.

1. 要限制搜索查询文本的长度和字数，请为 **[!UICONTROL Minimal Query Length]** 和 **[!UICONTROL Maximum Query Length]**.

1. 要限制为获得更快响应而缓存的常用搜索结果数量，请为 **[!UICONTROL Number of top search results to cache]**.

   默认值为 `100`. 输入值 `0` 第二次输入时缓存所有搜索词和结果。

1. 要更改返回结果的最大可用行数，请执行以下操作： [店面弹出式](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/live-search-storefront/quick-tour.html)，请输入其他 **[!UICONTROL Autocomplete Limit]** 值。

   限制行数可提高搜索性能并减小返回列表的大小。 默认值为 `8` 行。

## 方法2：带有Elasticsearch的Commerce

>[!IMPORTANT]
>
>由于 [!DNL Elasticsearch 7] 2023年8月终止支持公告，建议所有Adobe Commerce客户迁移到OpenSearch 2.x搜索引擎。 有关在产品升级期间迁移搜索引擎的信息，请参阅 [迁移到OpenSearch](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/prepare/opensearch-migration.html) 在 _升级指南_.

{{beta2-updates}}

### 步骤1：配置常规搜索选项

>[!NOTE]
>
>对于Elasticsearch，不支持开箱即用的按后缀搜索。 例如，如果关键字只包含SKU的端部，则按SKU搜索可能不会返回预期结果。

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中，展开 **[!UICONTROL Catalog]** 并选择 **[!UICONTROL Catalog]** 下方。

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Catalog Search]** 部分。

   ![Elasticsearch设置](../configuration-reference/catalog/assets/catalog-search-elasticsearch.png){width="600" zoomable="yes"}

   有关这些选项的详细信息，请参阅 [带有Elasticsearch的Adobe Commerce](../configuration-reference/catalog/catalog.md#adobe-commerce-with-elasticsearch) 在 _配置引用_.

1. 要限制搜索查询文本的长度和字数，请为 **[!UICONTROL Minimal Query Length]** 和 **[!UICONTROL Maximum Query Length]**.

   >[!IMPORTANT]
   >
   >为此最小和最大范围设置的值必须与Elasticsearch搜索引擎配置中设置的相应范围兼容。 例如，如果将这些值设置为 `2` 和 `300` 在Commerce中，更新搜索引擎中的相应值。

1. 要限制为获得更快响应而缓存的常用搜索结果数量，请为 **[!UICONTROL Number of top search results to cache]**.

   默认值为 `100`. 输入值 `0` 第二次输入时缓存所有搜索词和结果。

1. 如果要启用或禁用Product EAV索引器，请设置 **[!UICONTROL Enable EAV Indexer]**.

   此功能可提高索引速度并限制索引器不被第三方扩展使用。

1. 要限制搜索自动完成显示的搜索结果的最大数量，请设置以下内容的数量 **[!UICONTROL Autocomplete Limit]**.

   限制此数量可提高搜索性能并减小显示的列表大小。 默认值为 `8`.

### 步骤2：配置Elasticsearch连接

>[!IMPORTANT]
>
>此 **[!UICONTROL Search Engine]**， **[!UICONTROL Elasticsearch Server Hostname]**， **[!UICONTROL Elasticsearch Server Port]**， **[!UICONTROL Elasticsearch Index Prefix]**， **[!UICONTROL Enable Elasticsearch HTTP Auth]**、和 **[!UICONTROL Elasticsearch Server Timeout]** 字段是在安装或升级Commerce时配置的。 只有在升级或修改Elasticsearch时，才应更改这些值。

1. 对象 **[!UICONTROL Search Engine]**，接受默认值 `Elasticsearch 7`.

   所有Commerce安装均需要Elasticsearch7.6.x。

1. 对象 **[!UICONTROL Elasticsearch Server Hostname]**，接受安装Commerce时配置的默认值。

   在此示例中，默认值为 `elasticsearch.internal`.

1. 对象 **[!UICONTROL Elasticsearch Server Port]**，接受安装Commerce时配置的默认值。

   在此示例中，默认值为 `9200`.

1. 对象 **[!UICONTROL Elasticsearch Index Prefix]**，输入前缀以标识Elasticsearch索引。

   默认值为 `magento2`.

1. 要使用HTTP身份验证提示输入用户名和密码以访问Elasticsearch服务器，请设置 **[!UICONTROL Enable Elasticsearch HTTP Auth]** 到 `Yes`.

1. 对象 **[!UICONTROL Elasticsearch Server Timeout]**，输入系统超时前的秒数。

   默认值为 `15`.

1. 要验证配置，请单击 **[!UICONTROL Test Connection]**.

### 步骤3：配置建议和建议

>[!NOTE]
>
>搜索建议和建议可能会影响服务器性能。

1. 要提供推荐，请设置 **[!UICONTROL Enable Search Recommendations]** 到 `Yes` 并执行以下操作：

   - 对象 **[!UICONTROL Search Recommendation Count]**，输入要提供的推荐数量。

   - 要显示为每个推荐找到的结果数，请设置 **[!UICONTROL Show Results Count for Each Recommendation]** 到 `Yes`.

1. 设置 **[!UICONTROL Enable Search Suggestions]** 到 `Yes` 并执行以下操作：

   - 对象 **[!UICONTROL Search Suggestions Count]**，输入要提供的搜索建议数量。

   - 要显示每个建议找到的结果数，请设置 **[!UICONTROL Show Results for Each Suggestion]** 到 `Yes`.

### 步骤4：配置匹配的最少搜索词

要控制查询中搜索结果应匹配以返回的最小搜索词数，请为 **[!UICONTROL Minimum Terms to Match]**. 指定此值可确保购物者获得最佳结果相关性。 有关接受值的列表，请参见 [minimum_should_match参数](https://www.elastic.co/guide/en/elasticsearch/reference/current/query-dsl-minimum-should-match.html) 在Elasticsearch文档中。

完成后，单击 **[!UICONTROL Save Config]**.

[1]: https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/search-engine/overview.html
[2]: https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/search/overview-search.html

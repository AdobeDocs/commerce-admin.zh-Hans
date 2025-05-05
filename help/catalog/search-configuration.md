---
title: 配置目录搜索
description: 了解如何为应用商店配置目录搜索。
exl-id: b4f22bce-39e2-4269-99a4-eb2d647df939
feature: Catalog Management, Search
source-git-commit: 5da244a548b15863fe31b5df8b509f8e63df27c2
workflow-type: tm+mt
source-wordcount: '773'
ht-degree: 0%

---

# 配置目录搜索

目录搜索配置有两种变体。 第一种方法描述了安装[实时搜索](https://experienceleague.adobe.com/docs/commerce/live-search/overview.html?lang=zh-Hans)时可用的设置。 第二种方法描述了使用[OpenSearch](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/search-engine/overview.html?lang=zh-Hans){:target="_blank"}的本机Adobe Commerce的配置设置。

>[!NOTE]
>
>有关云基础架构项目，请参阅&#x200B;[_Commerce on Cloud Infrastructure指南_](https://experienceleague.adobe.com/zh-hans/docs/commerce-cloud-service/user-guide/configure/service/opensearch)中的其他说明。

## 方法1：使用[!DNL Live Search]的Adobe Commerce

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧面板中，展开&#x200B;**[!UICONTROL Catalog]**&#x200B;并在下面选择&#x200B;**[!UICONTROL Catalog]**。

1. 展开&#x200B;**[!UICONTROL Catalog Search]**&#x200B;部分的![扩展选择器](../assets/icon-display-expand.png)。

   ![实时搜索的目录搜索](../configuration-reference/catalog/assets/catalog-search-live-search.png){width="600" zoomable="yes"}

   有关这些选项的详细列表，请参阅&#x200B;_配置引用_&#x200B;中的[带有Live Search的Adobe Commerce](../configuration-reference/catalog/catalog.md#adobe-commerce-with-live-search)。

1. 要限制搜索查询文本的长度和字数，请为&#x200B;**[!UICONTROL Minimal Query Length]**&#x200B;和&#x200B;**[!UICONTROL Maximum Query Length]**&#x200B;设置一个值。

1. 若要限制要缓存以加快响应的常用搜索结果数量，请为&#x200B;**[!UICONTROL Number of top search results to cache]**&#x200B;设置数量。

   默认值为`100`。 再次输入值`0`将缓存所有搜索词和结果。

1. 要更改[店面弹出窗口](https://experienceleague.adobe.com/docs/commerce/live-search/live-search-storefront/quick-tour.html?lang=zh-Hans)中返回的结果可用的最大行数，请输入其他&#x200B;**[!UICONTROL Autocomplete Limit]**&#x200B;值。

   限制行数可提高搜索性能并减小返回列表的大小。 默认值为`8`行。

## 方法2：使用OpenSearch的Commerce

>[!IMPORTANT]
>
>- 由于[!DNL Elasticsearch 7]将于2023年8月终止支持公告，建议所有Adobe Commerce客户迁移到OpenSearch 2.x搜索引擎。 有关在产品升级期间迁移搜索引擎的信息，请参阅&#x200B;_升级指南_&#x200B;中的[迁移到OpenSearch](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/prepare/opensearch-migration.html?lang=zh-Hans)。
>- 在版本2.4.4和2.4.3-p2中，所有标记为Elasticsearch的字段也适用于OpenSearch。 当版本2.4.6中引入对Elasticsearch 8.x的支持时，创建了新标签以区分Elasticsearch和OpenSearch配置。 但是，两者的配置选项是相同的。

### 步骤1：配置常规搜索选项

>[!NOTE]
>
>使用OpenSearch和Elasticsearch时，不提供对按后缀进行搜索的现成支持。 例如，如果关键字只包含SKU的端部，则按SKU搜索可能不会返回预期结果。

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧面板中，展开&#x200B;**[!UICONTROL Catalog]**&#x200B;并在下面选择&#x200B;**[!UICONTROL Catalog]**。

1. 展开&#x200B;**[!UICONTROL Catalog Search]**&#x200B;部分的![扩展选择器](../assets/icon-display-expand.png)。

   ![搜索引擎设置](../configuration-reference/catalog/assets/catalog-search-opensearch.png){zoomable="yes"}

   有关这些选项的详细信息，请参阅&#x200B;_配置引用_&#x200B;中的[具有本机搜索的Adobe Commerce](../configuration-reference/catalog/catalog.md#adobe-commerce-with-native-search)。

1. 要限制搜索查询文本的长度和字数，请为&#x200B;**[!UICONTROL Minimal Query Length]**&#x200B;和&#x200B;**[!UICONTROL Maximum Query Length]**&#x200B;设置一个值。

   >[!IMPORTANT]
   >
   >为此最小和最大范围设置的值必须与搜索引擎配置中设置的相应范围兼容。 例如，如果您在Commerce中将这些值设置为`2`和`300`，请更新搜索引擎中的相应值。

1. 若要限制要缓存以加快响应的常用搜索结果数量，请为&#x200B;**[!UICONTROL Number of top search results to cache]**&#x200B;设置数量。

   默认值为`100`。 再次输入值`0`将缓存所有搜索词和结果。

1. 如果要启用或禁用Product EAV索引器，请设置&#x200B;**[!UICONTROL Enable EAV Indexer]**。

   此功能可提高索引速度并限制索引器不被第三方扩展使用。

1. 要限制为搜索自动完成显示的搜索结果的最大数目，请为&#x200B;**[!UICONTROL Autocomplete Limit]**&#x200B;设置一个数量。

   限制此数量可提高搜索性能并减小显示的列表大小。 默认值为`8`。

### 步骤2：配置OpenSearch连接

>[!IMPORTANT]
>
>在安装或升级Commerce时配置了&#x200B;**[!UICONTROL Search Engine]**、**[!UICONTROL OpenSearch Server Hostname]**、**[!UICONTROL OpenSearch Server Port]**、**[!UICONTROL OpenSearch Index Prefix]**、**[!UICONTROL Enable OpenSearch HTTP Auth]**&#x200B;和&#x200B;**[!UICONTROL OpenSearch Server Timeout]**&#x200B;字段。 只有在升级或修改OpenSearch时，才应更改这些值。

1. 对于&#x200B;**[!UICONTROL Search Engine]**，选择`OpenSearch`。

1. 对于&#x200B;**[!UICONTROL OpenSearch Server Hostname]**，接受在安装Commerce时配置的默认值。

1. 对于&#x200B;**[!UICONTROL OpenSearch Server Port]**，接受在安装Commerce时配置的默认值。

   在此示例中，默认值为`9200`。

1. 对于&#x200B;**[!UICONTROL OpenSearch Index Prefix]**，请输入前缀以标识Elasticsearch索引。

   默认值为`magento2`。

1. 要使用HTTP身份验证提示输入用户名和密码以访问OpenSearch服务器，请将&#x200B;**[!UICONTROL Enable OpenSearch HTTP Auth]**&#x200B;设置为`Yes`。

1. 对于&#x200B;**[!UICONTROL OpenSearch Server Timeout]**，输入系统超时前的秒数。

   默认值为`15`。

1. 要验证配置，请单击&#x200B;**[!UICONTROL Test Connection]**。

### 步骤3：配置建议和建议

>[!NOTE]
>
>搜索建议和建议可能会影响服务器性能。

1. 要提供推荐，请将&#x200B;**[!UICONTROL Enable Search Recommendations]**&#x200B;设置为`Yes`并执行以下操作：

   - 对于&#x200B;**[!UICONTROL Search Recommendation Count]**，输入要提供的推荐数量。

   - 要显示为每个推荐找到的结果数，请将&#x200B;**[!UICONTROL Show Results Count for Each Recommendation]**&#x200B;设置为`Yes`。

1. 将&#x200B;**[!UICONTROL Enable Search Suggestions]**&#x200B;设置为`Yes`并执行以下操作：

   - 对于&#x200B;**[!UICONTROL Search Suggestions Count]**，输入要提供的搜索建议数。

   - 要显示每个建议找到的结果数，请将&#x200B;**[!UICONTROL Show Results for Each Suggestion]**&#x200B;设置为`Yes`。

### 步骤4：配置匹配的最少搜索词

要控制查询中搜索结果应匹配以返回的最小术语数，请为&#x200B;**[!UICONTROL Minimum Terms to Match]**&#x200B;指定一个值。 指定此值可确保购物者获得最佳结果相关性。 有关接受值的列表，请参阅OpenSearch文档中的[minimum_should_match参数](https://opensearch.org/docs/latest/query-dsl/minimum-should-match/)。

完成后，单击&#x200B;**[!UICONTROL Save Config]**。

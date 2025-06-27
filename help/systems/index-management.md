---
title: 索引管理
description: 了解索引管理，包括触发重新索引和最佳实践的操作。
exl-id: cbb249a2-b957-44fe-bf81-df795a8fd5d1
feature: System, Configuration
badgePaas: label="仅限PaaS" type="Informative" url="https://experienceleague.adobe.com/zh-hans/docs/commerce/user-guides/product-solutions" tooltip="仅适用于云项目(Adobe管理的PaaS基础架构)和内部部署项目上的Adobe Commerce 。"
source-git-commit: 422fce6c2676f7c760c1a97b67fbd0f45d65e19c
workflow-type: tm+mt
source-wordcount: '1296'
ht-degree: 0%

---

# 索引管理

每当一个或多个项目发生更改时，Adobe Commerce和Magento Open Source会自动重新索引。 触发重新索引的操作包括价格更改、创建目录或购物车价格规则、添加新类别等。 为了优化性能，Commerce使用索引器将数据累积到特殊表中。 随着数据的变化，必须更新索引表，或重新编制索引。 Commerce会作为后台进程重新索引，并且您的存储将在这些进程中保持可访问状态。

重新索引数据可加快处理速度，并减少客户必须等待的时间。 例如，如果您将某个项目的价格从$4.99更改为$3.99，Commerce会对数据进行重新索引以显示商店中的价格变化。 如果没有索引，Commerce将不得不动态计算每个产品的价格；处理购物车价格规则、捆绑定价、折扣、分层定价等。 加载产品价格可能需要比客户愿意等待的时间更长的时间。

索引器可以设置为在保存时或按计划更新。 所有索引都可以使用任一选项，但Customer Grid除外，它仅在保存时支持。 在保存时索引时，Commerce会在保存操作时启动重新索引。 “索引管理”页完成更新并刷新缓存，在一两分钟之内出现重新索引消息。 按照计划重新索引时，重新索引将按照计划作为cron作业运行。 如果[cron作业](cron.md)不可用于更新任何变为无效的索引器，则会显示系统消息。 在重新索引过程中，您的存储仍可访问。

>[!NOTE]
> 使用实时搜索、目录服务或产品推荐的Adobe Commerce商家可以选择使用基于[SaaS的价格索引器](https://experienceleague.adobe.com//en/docs/commerce/price-indexer/price-indexing?lang=zh-Hans)。

当需要重新索引时，将在页面顶部显示通知。 根据重新索引模式和您执行的潜在操作，将清除索引和消息。 有关索引的更多详细信息，请参阅&#x200B;_PHP开发人员指南_&#x200B;中的[应用程序如何实现索引](https://developer.adobe.com/commerce/php/development/components/indexing/#how-the-application-implements-indexing)。

![索引管理 — 操作](./assets/index-management.png){width="700" zoomable="yes"}

- 对于平面产品目录，索引管理的呈现方式略有不同。
- 为避免在多个Admin用户更新触发自动重新索引的对象时出现问题，建议您将所有索引器设置为[cron作业](cron.md)按计划运行。 否则，每次保存对象时，任何具有相互依赖关系的对象都可能导致死锁。 死锁的症状包括高CPU使用率和MySQL错误。 作为最佳实践，建议您使用计划索引。
- ![Adobe Commerce](../assets/adobe-logo.svg)(仅限Adobe Commerce)默认情况下，系统记录管理员操作，如重新编制索引，并可在[操作日志报告](action-log-report.md)中查看。 可以在应用商店的高级管理员设置的[管理员操作日志记录](action-log.md)中配置操作日志记录。

## 重新索引的最佳实践

在Commerce中，重新索引和缓存有不同的用途。 索引可以跟踪数据库信息，以提高搜索性能、加快存储前端的数据检索速度等等。 [缓存](cache-management.md)保存加载的数据、图像、格式等，以提高加载和访问店面的性能。

- 通常，在Commerce中更新数据时想要重新索引。
- 如果您有一个或多个商店，则可能需要将索引器（如类别和产品）设置为计划的cron作业，因为可能会重新索引循环。 您可能希望在非高峰时间按计划设置重新索引。
- 重新索引时，您不需要同时执行刷新缓存。
- 对于新的Commerce安装，您必须刷新缓存并重新索引。
- 刷新缓存和重新索引不会刷新计算机的Web浏览器缓存。 完成店面的更新后，清除浏览器缓存。

## 更改索引模式

>[!IMPORTANT]
>
>对于使用[Adobe Commerce B2B](https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html?lang=zh-Hans)并将Elasticsearch设置为全文(`catalogsearch_fulltext`)索引器的存储：在批量权限发生更改或“权限”索引器处于“已计划”模式时，必须重新运行全文索引。

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Index Management]**。

1. 选中要更改的每个索引器的复选框。

1. 将&#x200B;**[!UICONTROL Actions]**&#x200B;设置为以下项之一：

   - `Update on Save`
   - `Update by Schedule`
   - `Invalidate index`

   >[!IMPORTANT]
   >
   >只能使用`Update on Save`重新编制客户网格的索引。 此索引&#x200B;**_不_**&#x200B;支持`Update by Schedule`。

1. 单击&#x200B;**[!UICONTROL Submit]**&#x200B;以将更改应用于每个选定的索引器。

   **索引管理列**

   | 列 | 描述 |
   | ------ |---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   | [!UICONTROL Indexer] | 索引器的名称。 |
   | [!UICONTROL Description] | 索引器的描述。 |
   | [!UICONTROL Mode] | 指示每个索引器的当前更新模式。 选项： <br/>**[!UICONTROL Update on Save]**— 将索引设置为在保存实体更改时更新。 该等实体包括产品、类别及客户。 保存操作完成后，一系列步骤开始捕获更改并更新索引。 “索引管理”页会在一两分钟内更新并刷新重新索引消息。<br/>**[!UICONTROL Update on Schedule]** — 索引设置为根据[cron作业](cron.md)按计划更新。 cron作业包括重新索引的时间表间隔，在运行时将更新写入索引。 |
   | [!UICONTROL Schedule Status] | 显示计划状态更新。 |
   | [!UICONTROL Status] | 显示以下项之一： <br/>**[!UICONTROL Ready]**— 索引是最新的。<br/>**[!UICONTROL Suspended]** — 重新索引已暂停。 <br/>**[!UICONTROL Processing]**— 当前正在重新编制索引。<br/>**[!UICONTROL Reindex Required]** — 已做出需要重新索引的更改，但无法自动更新索引器。 检查[cron](cron.md)是否可用且配置是否正确。 |
   | [!UICONTROL Updated] | 指示上次更新索引的日期和时间。 |

   {style="table-layout:auto"}

## 使用命令行重新索引

Commerce使用命令行提供了其他重新索引选项。 有关完整的详细信息和命令选项，请参阅&#x200B;_配置指南_&#x200B;中的[重新索引](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/manage-indexers.html?lang=zh-Hans#reindex){:target="blank"}。

## 索引触发事件

## 重新索引触发器

| 索引类型 | 重新索引事件 |
| ---------- | ---------------- |
| [!UICONTROL Product Prices] | 添加客户组<br/>更改配置设置 |
| [!UICONTROL Flat catalog product data] | 添加商店<br/>添加商店群组<br/>添加、编辑或删除属性（用于搜索和筛选） |
| [!UICONTROL Flat catalog category data] | 添加商店<br/>添加商店群组<br/>添加、编辑或删除属性（用于搜索和筛选） |
| [!UICONTROL Catalog category/product index] | 添加、编辑或删除产品（单次、成批和导入）<br/>更改产品与类别的关系<br/>添加、编辑或删除类别<br/>添加或删除商店<br/>删除商店群组<br/>删除网站 |
| [!UICONTROL Catalog search index] | 添加、编辑或删除产品（单次、成批和导入）<br/>添加或删除商店<br/>删除商店组<br/>删除网站 |
| [!UICONTROL Stock status index] | 更改清单配置设置。 |
| [!UICONTROL Category permissions index] | 添加商店<br/>添加商店组<br/>添加、删除或更新属性（用于搜索和筛选） |

{style="table-layout:auto"}

>[!IMPORTANT]
>
>不再建议将使用平面目录作为最佳实践。 据悉，继续使用此功能会导致性能下降和其他索引问题。 有关详细信息，请参阅[使用平面目录产品](../catalog/catalog-flat.md)。

## 索引操作和控件

| 操作 | 结果 | 控件 |
| ------ | ------ | -------- |
| 创建商店、新客户组或`Actions that Cause a Full Reindex`中列出的任何操作 | 完全重新索引 | 完全重新索引按照您的Adobe Commerce或Magento Open Source cron作业确定的时间表执行。 |
| 批量加载项目(Commerce导入/导出、直接SQL查询以及任何其他直接添加、更改或删除数据的方法) | 部分重新索引（仅对更改的项目重新索引） | 频率由您的Commerce cron作业决定。 |
| 更改范围（例如，从全局更改为网站） | 部分重新索引（仅对更改的项目重新索引） | 频率由您的Commerce cron作业决定。 |

{style="table-layout:auto"}

## 触发完全重新索引的事件

| 索引器 | 事件 |
| ------- | ----- |
| [!UICONTROL Catalog Category Flat Indexer] | 创建网站商店<br/>创建网站商店视图<br/>创建或删除以下任意属性：<br/> — 可在高级搜索中搜索或显示<br/> — 可筛选<br/> — 可在搜索中筛选<br/> — 用于排序<br/>将现有属性更改为上述任何属性。<br/>启用平面类别店面选项 |
| [!UICONTROL Catalog Product Flat Indexer] | 创建Web商店<br>创建Web商店视图<br/>创建或删除以下任意属性：<br/> — 可在高级搜索中搜索或可见<br> — 可筛选<br> — 可在搜索中筛选<br/> — 用于排序<br/>将现有属性更改为上述任何属性。<br/>启用平面类别店面选项 |
| [!UICONTROL Stock status indexer] | 当系统配置中的以下&#x200B;_目录库存选项_&#x200B;发生更改时： <br/>`Stock Options` — 显示缺货产品<br/>`Product Stock Options` — 管理库存 |
| [!UICONTROL Price Indexer] | 添加客户组。<br/>当系统配置中的以下任何目录库存选项更改时：<br/>`Stock Options` — 显示缺货产品<br/>`Product Stock Options` — 管理库存<br/>`Price` — 目录价格范围 |
| [!UICONTROL Category or Product Indexer] | 创建或删除商店视图<br/>删除商店<br/>删除网站 |

{style="table-layout:auto"}

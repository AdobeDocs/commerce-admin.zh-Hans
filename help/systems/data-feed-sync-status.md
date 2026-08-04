---
title: 在Commerce中监控数据馈送同步状态
description: 跟踪导出。 诊断 [!DNL Catalog Service]、 [!DNL Live Search]、 [!DNL Product Recommendations]和 [!DNL Adobe Commerce Optimizer Connector]的同步问题。
feature: Products, Customers, Data Import/Export
role: Admin
level: Beginner
exl-id: 4e1b9da0-450c-4488-8693-1938a948e792
TQID: https://experienceleague.adobe.com/Y8vYxKS-8iX-bCLSJpAiJOItWlJk348bSMWfk1Cgpbg
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
  - id: f42e0a1a-0d79-488d-a83f-f2c30672b137
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 424b379815ffbf818c2490d0195bf0bf7dd51ab7
workflow-type: tm+mt
source-wordcount: 1664
ht-degree: 0%

---


# 数据馈送同步状态监控

通过[!UICONTROL Data Feed Sync Status]页面，Commerce管理员可在管理区域中监控产品和类别数据馈送的导出运行状况。

## 受众和可用性 {#audience}

对于拥有以下服务之一的有效许可证的Commerce商家，无需支付额外费用，即可使用“数据馈送同步状态”页面：

- [[!DNL Product Recommendations v6.0.0]](https://experienceleague.adobe.com/zh-hans/docs/commerce/product-recommendations/guide-overview)
- [[!DNL Live Search v4.1.0]](https://experienceleague.adobe.com/zh-hans/docs/commerce/live-search/overview)
- [[!DNL Catalog Service v1.17]](https://experienceleague.adobe.com/zh-hans/docs/commerce/catalog-service/guide-overview)
- [[!DNL Adobe Commerce Optimizer Connector]](https://experienceleague.adobe.com/zh-hans/docs/commerce/aco-optimizer-connector/overview)

受支持的Commerce服务配置中会自动提供“数据馈送同步状态”页面。 在Adobe Commerce on Cloud Infrastructure和内部部署中，如果在启用符合条件的服务或连接器后缺少页面，请按照以下手动安装说明操作。 对于产品管理的SaaS体验，请勿使用“编辑器”安装过程。

## 访问同步状态页面 {#access-data-feed-sync-status-page}

从管理区域，导航到&#x200B;**[!UICONTROL System]** > **[!UICONTROL Data Transfer]** > **[!UICONTROL Data Feed Sync Status]**。

![数据馈送同步状态页面汇总了数据馈送导出活动](assets/data-feed-sync-status.png){width="600" zoomable="yes"}

>[!NOTE]
>
> 此页面仅报告导出状态。 成功状态表示数据导出成功，但不会确认数据在连接的服务中是否可用。 有关详细信息，请参阅[确认连接的服务中的数据](#confirm-data-in-connected-services)。

## 可用的导出信息源

可以从“数据同步状态”页面管理的可用导出馈送的列表取决于连接的Commerce服务。

- **对于已配置Commerce服务的[!DNL Adobe Commerce on Cloud, On Premises, and Commerce as a Cloud Service]：**，请参阅&#x200B;_SaaS数据导出指南_&#x200B;中的[支持的馈送](https://experienceleague.adobe.com/zh-hans/docs/commerce/saas-data-export/reference/feed-table-reference#supported-feeds)。

- 对于使用[!DNL Adobe Commerce Optimizer Connector]配置的Adobe Commerce云或内部部署：**，请参阅&#x200B;_Adobe Commerce Optimizer连接器指南_中的[支持的源](https://experienceleague.adobe.com/zh-hans/docs/commerce/aco-optimizer-connector/reference/connector-reference#supported-feeds)。**


## 数据馈送同步状态摘要 {#data-feed-sync-status-summary}

摘要网格会列出每个馈送及其导出计数。

| 字段 | 描述 |
| ----------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **馈送名称** | 实体或实体的一部分（产品、产品价格）的信息源索引器。 |
| **Source记录** | 需要同步的Commerce记录数。 可能会超过管理网格计数，因为馈送项目具有作用域（例如，存储视图代码）。 |
| **已成功发送记录** | 从Commerce成功提交到配置的服务端点的信息源项目数。 这不会确认下游摄取或目录可用性。 如果发生同步错误，此数字可能小于源记录数。 |
| **个失败的记录** | 未能发送到连接的Commerce服务的记录数。 |
| **操作** | 选择&#x200B;**[!UICONTROL Details]**&#x200B;以查看信息源的同步活动。 |

## 数据馈送同步状态详细信息 {#data-feed-sync-status-details}

从摘要页面中，选择一个信息源名称或选择&#x200B;**[!UICONTROL Details]**&#x200B;以查看每个信息源项目的导出状态：

![带有馈送项状态报告的数据馈送同步状态详细信息页面](assets/data-feed-sync-status-details.png){width="600" zoomable="yes"}

| 字段 | 描述 |
| ---------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **馈送项目ID** | 用于系统用途的自动生成的标识符 |
| **实体ID** | 源实体的唯一标识符（产品ID、类别ID等） |
| **馈送标识符** | 馈送项目的唯一标识符。 例如，产品信息源的SKU和商店视图代码。 值因馈送而异。 |
| **导出状态** | 信息源项的[同步状态](#export-status-types)，带有颜色编码的指示器 |
| **上次同步日期** | Commerce最近一次导出尝试或提交的日期和时间。 此时间戳无法确认下游可用性。 |
| **是否删除实体？** | 指示实体是否已在Adobe Commerce中删除。 仅当同步失败时，才会显示已删除的项目。 |
| **请求ID** | 同步请求的唯一ID。 在排除实体更新故障时将其提供给支持人员。 |
| **错误** | 同步失败的详细信息 |

您可以使用以下控件管理视图：

- [!UICONTROL Mass Action]为选定的馈送项目计划重新同步
- [!UICONTROL Filters]和[!UICONTROL Columns]
- [!UICONTROL Default View]创建和保存筛选视图，并在视图之间切换

### 信息源运行状况指示器 {#feed-health-indicators}

| **指示器** | **描述** |
| ------------- | --------------- |
| 索引器状态 | <ul><li>**就绪**：索引器是最新的。 无需重新索引。</li><li>**需要重新索引**： Source数据已更改。 运行重新索引以捕获最近的更改。</li><li>**正在处理**：正在编制索引。</li></ul> |
| Changelog积压 | <ul><li>**所有已同步**：没有待处理的更改。</li><li>积压中的&#x200B;**项**：等待处理的挂起更改数。 超过1,000个项目的积压可能表示性能问题。</li></ul> |
| 索引器模式 | <ul><li>**计划模式**（推荐）：索引器按计划运行，这降低了数据丢失的风险。</li><li>**保存时更新**（实时）：在页面上显示为警告。 实时模式不符合预期，并且会增加负载下数据丢失的风险。</li></ul> |

>[!TIP]
>
> 要了解有关索引处理的详细信息，请参阅[索引管理](index-management.md)主题。

### 导出状态类型 {#export-status-types}

| **状态** | **描述** | **需要操作** |
| ----------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------------ |
| **已提交至服务** | 已成功从Commerce提交信息源项目以进行下游处理。 | 无 |
| **失败，将重试** | 发送失败，但系统将尝试重新发送。 | 监控分辨率 |
| **失败，需要注意** | 由于应用程序或数据错误而失败。 | 调查并解决[!UICONTROL Error]列中的问题 |
| **正在等待提交** | 在更改日志中检测到更改，但尚未处理。 | 正常处理状态 |

## 监测数据馈送状态

当您更新Commerce数据库中与产品和类别相关的实体时，系统会根据您的信息源配置将数据传输到Commerce服务。 您可以从[!UICONTROL Data Feed Sync Status]摘要页面监视导出活动及其当前状态。

>[!IMPORTANT]
>
> 完成数据同步所需的时间因目录大小、更新的数据量以及外部服务性能而异。

当成功发送的数量与信息源的源数量匹配时，并且没有任何项目等待提交或失败，则Commerce已完成该信息源的导出。 使用相应的仪表板来[确认下游可用性](#confirm-data-in-connected-services)。

>[!NOTE]
>
> Adobe还提供了命令行界面工具和系统日志，开发人员和系统集成人员可以使用这些工具和日志来管理和跟踪同步操作。 有关详细信息，请参阅[SaaS数据导出指南](https://experienceleague.adobe.com/zh-hans/docs/commerce/saas-data-export/overview)。

### 管理失败的导出 {#manage-failed-exports}

要检查失败的导出并计划重新同步，请执行以下操作：

1. 从摘要页面中，查找包含失败记录的信息源。
1. 选择&#x200B;**[!UICONTROL Details]**。
1. 查看[!UICONTROL Error]列中的错误消息。
1. 使用复选框选择要重新同步的记录。
1. 从[!UICONTROL Mass Action]菜单中，选择&#x200B;**[!UICONTROL Schedule Resync]**，选择&#x200B;**[!UICONTROL Submit]**，并确认操作。
1. 在详细信息页面上监视状态更改。

系统会自动重试某些故障。

#### 何时手动重新同步 {#resync-feed-items}

在以下情况下手动重新同步：

- 身份验证或权限错误（401或403状态代码）持续存在
- 您修复了导致有效负载错误的数据格式问题
- 外部服务配置或端点已更改
- 已部署影响数据导出的自定义项

### 确认连接的服务中的数据 {#confirm-data-in-connected-services}

要在导出完成后验证端到端同步，请使用以下方法之一。 有关此页上的导出状态限制，请参阅上面的[注释](#export-status-scope)。

- 具有Commerce服务的&#x200B;**[!DNL Adobe Commerce as a Cloud Service]：**&#x200B;请检查适用的[数据管理仪表板](data-dashboard.md)以确认下游可用性。
- **使用Adobe Commerce Optimizer Connector的云或本地Adobe Commerce**：首先检查Commerce管理员导出状态，然后在[!DNL Commerce Optimizer Studio]中检查[数据同步页面](https://experienceleague.adobe.com/zh-hans/docs/commerce/optimizer/setup/data-sync)
- **[!DNL Adobe Commerce Optimizer]（独立）：**&#x200B;数据未从Commerce后端导出。 使用[!DNL Commerce Optimizer Studio]中的[数据同步页面](https://experienceleague.adobe.com/zh-hans/docs/commerce/optimizer/setup/data-sync)确认数据可用性。

>[!TIP]
>
> 要了解有关数据同步过程的更多信息，请参阅&#x200B;*SaaS数据导出指南*&#x200B;中的[将数据与SaaS数据导出同步](https://experienceleague.adobe.com/zh-hans/docs/commerce/saas-data-export/data-synchronization/data-sync-manage#view-and-manage-the-synchronization-process)。

## 最佳实践 {#best-practices}

- 每天查看摘要页面，查看具有高失败率的信息源。
- 每周检查关键信息源（如产品和价格）的详细信息。
- 每月跟踪导出成功趋势以确定重复出现的问题。

## 常见问题疑难解答 {#troubleshoot-common-issues}

| 问题 | 症状 | 要做什么 |
| ---------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| 高失败率 | 许多记录显示&#x200B;*失败，需要注意*&#x200B;状态 | <ul><li>检查外部服务状态和配置</li><li>查看[!UICONTROL Error]列中模式的错误消息</li><li>解决基础问题后，请参阅[管理和重新同步失败的导出](#manage-failed-exports)</li><li>如果需要，请联系外部服务支持</li></ul> |
| 导出性能缓慢 | 更改日志积压过多或状态更新缓慢 | <ul><li>检查[信息源运行状况指示器](#feed-health-indicators)的索引器和积压状态</li><li>如果显示&#x200B;**需要重新索引**，请重新运行索引</li><li>监测外部服务响应时间</li><li>尽可能在非高峰时间安排导出</li><li>审查系统资源和性能</li></ul> |
| 身份验证失败 | [!UICONTROL Error]列中的401或403状态代码 | <ul><li>验证API凭据和令牌</li><li>检查外部服务帐户权限</li><li>续订过期的令牌或联系您的服务提供商</li><li>凭据恢复后，[重新同步受影响的记录](#manage-failed-exports)</li></ul> |
| “缺少数据馈送：同步状态”页 | 启用连接的服务后，**[!UICONTROL Data Feed Sync Status]**&#x200B;未列在&#x200B;**[!UICONTROL System]** > **[!UICONTROL Data Transfer]**&#x200B;下 | <ul><li>对于Commerce as a Cloud Service，请确认已启用符合条件的服务（请参阅[受众和可用性](#audience)）</li><li>仅适用于Commerce云端或内部部署，[手动安装扩展](#install-the-extension)</li></ul> |

Adobe Commerce on Cloud Infrastructure或内部部署：确认已启用符合条件的服务或Adobe Commerce Optimizer Connector；如果仍缺少页面，请按照手动安装说明操作。
ACCS或Adobe Commerce Optimizer：请勿手动安装该模块；请使用产品管理的同步体验或联系相应的服务支持团队。

## 安装扩展 {#install-the-extension}

仅当您启用符合条件的服务后，“管理”区域中缺少[!UICONTROL Data Feed Sync Status]页面时，Adobe Commerce on Cloud或内部部署才需要手动安装。 查看[受众和可用性](#audience)。

### 先决条件

- Adobe Commerce 2.4.4+。 有关详细要求，请参阅[系统要求](https://experienceleague.adobe.com/zh-hans/docs/commerce-operations/installation-guide/system-requirements)。
- [Adobe Commerce数据导出扩展](https://experienceleague.adobe.com/zh-hans/docs/commerce/saas-data-export/reference/manage-extension)，版本103.4.15或更高版本
- 具有从Adobe Commerce存储库下载所需包的权限的身份验证密钥。 若要创建身份验证密钥并获取必要的包访问权限，请参阅[获取身份验证密钥](https://experienceleague.adobe.com/zh-hans/docs/commerce-operations/installation-guide/prerequisites/authentication-keys)。 有关云安装，请参阅[Commerce on Cloud Infrastructure指南](https://experienceleague.adobe.com/zh-hans/docs/commerce-on-cloud/user-guide/develop/authentication-keys)。
- 访问Adobe Commerce应用程序服务器的命令行。

### 安装步骤

使用编辑器添加`magento/module-data-exporter-status`模块：

```shell
composer require magento/module-data-exporter-status
```

有关详细的安装步骤，请参阅以下指南：

- [在云基础架构上安装Adobe Commerce的扩展](https://experienceleague.adobe.com/zh-hans/docs/commerce-on-cloud/user-guide/configure-store/extensions)
- [在Adobe Commerce内部部署上安装扩展](https://experienceleague.adobe.com/zh-hans/docs/commerce-operations/installation-guide/tutorials/extensions)

>[!MORELIKETHIS]
>
> - [数据管理仪表板](data-dashboard.md)
> - [SaaS数据导出指南](https://experienceleague.adobe.com/zh-hans/docs/commerce/saas-data-export/overview)

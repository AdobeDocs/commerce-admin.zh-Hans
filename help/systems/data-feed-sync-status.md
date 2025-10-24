---
title: 数据馈送同步状态监控
description: 监视数据导出同步，并识别 [!DNL Catalog Service]、 [!DNL Live Search]和 [!DNL Product Recommendations]的馈送处理出现的任何问题或延迟。
feature: Products, Customers, Data Import/Export
badgePaas: label="仅限PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="仅适用于云项目(Adobe管理的PaaS基础架构)和内部部署项目上的Adobe Commerce 。"
source-git-commit: 4cc5f5842e772ead9785b8280557a7b5b8f26419
workflow-type: tm+mt
source-wordcount: '1458'
ht-degree: 0%

---


# 数据馈送同步状态监控

Adobe Commerce管理员可以使用Commerce管理员中的“数据馈送同步状态”页面，监控从Adobe Commerce导出到连接的Commerce服务的数据的同步状态。

![具有馈送项状态报告的数据馈送同步状态详细信息页面](assets/data-feed-sync-status.png)

此页面提供数据导出馈送的运行状况和性能的实时分析，这些数据导出馈送将产品和类别数据从Commerce传输到外部服务，如[!DNL Product Recommendations]、[!DNL Live Search]和[!DNL Catalog Service]。

同步状态页面仅显示导出状态。 成功状态表示数据导出成功，并且最终可在连接的Commerce服务中使用。 使用[数据管理仪表板](data-dashboard.md)查看实体同步的实际状态。

监控信息源状态有助于确保数据一致性，并可迅速解决导出过程中出现的任何问题。 管理员可以：

* **查看所有数据馈送的同步状态**
* **识别并排除信息源处理中的错误**
* **访问单个信息源项目的详细状态信息**

将跟踪以下信息源的状态：

* 产品信息源
* 产品属性信息源
* 类别信息源
* 产品覆盖信息源
* 产品价格信息源
* 产品变型信息源

>[!TIP]
>
>要了解有关数据同步过程的更多信息，请参阅[SaaS数据导出指南](https://experienceleague.adobe.com/en/docs/commerce/saas-data-export/data-synchronization)中的&#x200B;*将数据与SaaS数据导出同步*。

## 安装扩展

所有拥有以下Commerce服务的有效许可证的Commerce商家都可使用“数据馈送状态”页面：

* [[!DNL Product Recommendations v6.0.0+]](https://experienceleague.adobe.com/en/docs/commerce/product-recommendations/guide-overview)
* [[!DNL Live Search v4.1.0+]](https://experienceleague.adobe.com/en/docs/commerce/live-search/guide-overview)
* 具有有效许可证的[[!DNL Catalog Service v1.17+]](https://experienceleague.adobe.com/en/docs/commerce/catalog-service/guide-overview)。

**要求**

* PHP 8.1、8.2、8.3或8.4
* Adobe Commerce 2.4.4+
* [Adobe Commerce数据导出扩展](https://experienceleague.adobe.com/en/docs/commerce/saas-data-export/manage-extension)，版本103.4.15或更高版本
* 访问[repo.magento.com](https://repo.magento.com)

  若要生成密钥并获取必要的权限，请参阅[获取您的身份验证密钥](https://experienceleague.adobe.com/en/docs/commerce-operations/installation-guide/prerequisites/authentication-keys)。 有关云安装，请参阅[Commerce on Cloud Infrastructure指南](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/develop/authentication-keys)。

* 访问Adobe Commerce应用程序服务器的命令行。

### 安装步骤

使用编辑器添加`magento/module-data-exporter-status`模块：

```shell
composer require magento/module-data-exporter-status
```

有关详细的安装步骤，请参阅以下指南：

* 在云基础架构上的Adobe Commerce上[安装扩展](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/configure-store/extensions)

* [在本地安装Adobe Commerce扩展](https://experienceleague.adobe.com/en/docs/commerce-operations/installation-guide/tutorials/extensions)

## 访问“数据馈送状态”页面

从Commerce管理员访问Commerce管理员的数据馈送状态页面，其地址为&#x200B;**[!DNL System]** >数据传输> **[!DNL Data Feed Sync Status]**。

![数据馈送同步状态页面汇总了数据馈送导出活动](assets/data-feed-sync-status.png)

数据馈送状态监控提供两个界面：

* [数据馈送同步状态摘要页面](#data-feed-sync-status-summary)列出了可用的馈送和当前状态
* [数据馈送同步状态 — 详细信息页面](#data-feed-sync-status-details)显示有关选定馈送的详细信息。

## 数据馈送同步状态摘要

“馈送同步状态摘要”页面提供了有关数据馈送导出活动的信息，其中包括以下信息：

| 字段 | 描述 |
|-------|-------------|
| **馈送名称** | 负责同步特定实体或其部件的信息源索引器的名称，例如产品或产品价格。 |
| **Source记录** | 可从Commerce数据库导出的记录数。 由于每个信息源项目都属于特定范围（例如“商店视图”代码），因此该数量可以大于Commerce管理员中显示的记录数。 |
| **已成功发送记录** | 成功传输到Commerce SaaS以供进一步处理的记录数。 如果在传输期间发生错误，则表示已成功传输到外部服务的记录数。 |
| **个失败的记录** | 导出失败并需要注意的记录数。 |
| **操作** | 选择&#x200B;**[!UICONTROL Details]**&#x200B;以查看信息源的同步活动。 |

## 数据馈送同步状态详细信息

在数据馈送状态摘要页面中，单击馈送名称或使用[!DNL View Details]操作访问有关馈送中各个记录的详细信息。

![[!UICONTROL Data Feed Sync Status - Details]页具有信息源项状态报告](assets/data-feed-sync-status-details.png)

详细信息视图为每个馈送项目提供以下信息：

| 字段 | 描述 |
|-------|-------------|
| **馈送项目ID** | 信息源记录的内部标识符 |
| **实体ID** | 源实体ID（产品ID、类别ID等） |
| **导出状态** | 馈送项的[同步状态](#export-status-types)。 带有颜色编码指示器的导出尝试的当前状态 |
| **上次同步日期** | 上次将记录发送到Commerce服务的时间戳 |
| **是否删除实体？** | 指示实体或其部件（例如产品或产品价格）是否已在Adobe Commerce中删除。 只有在同步过程中发生错误时，才会显示项目。 |
| **请求ID** | 同步请求的唯一标识符。 提供此ID以支持对特定实体更新进行故障诊断。 |
| **错误** | 如果馈送项目无法同步，则提供详细的错误信息。 |

您可以使用以下控件管理视图：

* [!DNL Mass Action]为选定的馈送项目计划重新同步
* [!DNL Filters]
* [!DNL Default View]创建和保存筛选视图，并在视图之间切换
* [!DNL Columns]显示和隐藏表中的列。

### 信息源运行状况指示器

在每个馈送详细信息页面的顶部，关键运行状况指示器提供每个馈送的系统状态：

#### 索引器状态

* **有效**：数据已同步；不需要重新索引。
* **无效**：原始数据已更改；应更新索引。
* **正在处理**：正在编制索引。

>[!TIP]
>
>要了解有关索引处理的详细信息，请参阅[索引管理](https://experienceleague.adobe.com/en/docs/commerce-admin/systems/tools/index-management)主题。

#### Changelog积压

* **所有已同步**：没有待处理的更改
* 积压中的&#x200B;**项**：等待处理的挂起更改数

### 导出状态类型

系统提供状态指示器，帮助您快速识别问题：

#### 状态类别

| **状态** | **描述** | **需要操作** |
|--------|-----------|-------------|
| **已提交至服务** | 信息源项目已成功导出到Commerce服务。 | 无 |
| **失败，将重试** | 临时失败。 系统将自动重试。 | 监控分辨率 |
| **失败，需要注意** | 由于应用程序或数据错误而失败。 | 调查并解决[!DNL Error]列中的问题 |
| **正在等待提交** | 已排队等候导出，但尚未处理。 | 正常处理状态 |

## 监测数据馈送状态

当您更新Commerce数据库中的产品和类别相关实体时，系统会根据您的信息源配置将数据传输到Commerce服务。 您可以从数据馈送同步状态摘要页面实时监视此过程。

>[!IMPORTANT]
>
>完成数据同步所需的时间因目录大小、更新的数据量以及外部服务性能而异。

如果成功发送的记录数与源记录数匹配，则表示同步已完成，并且所有数据都已成功传输。

>[!NOTE]
>
>Adobe还提供了命令行界面工具和系统日志，开发人员和系统集成人员可以使用这些工具和日志来管理和跟踪同步操作。 有关详细信息，请参阅[SaaS数据导出指南](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/saas-data-export/overview)。

### 管理失败的导出

要查看失败导出的详细信息并采取纠正措施，请执行以下操作：

1. 在“馈送同步状态”页面中，查找包含失败记录的馈送。
1. 单击&#x200B;**[!DNL Details]**。

1. 查看特定失败原因的错误消息。

1. 使用批量操作计划失败项目的重新同步操作。

### 重新同步失败的数据

您可以使用[!DNL Actions]页面上的[!DNL Data Feed Sync Status - Details]菜单手动重新同步失败或有问题的数据馈送。

当系统自动重试某些类型的故障时，在以下情况下可能需要手动干预：

* 您注意到身份验证或权限错误（401、403状态代码）。
* 解决导致有效负载错误的数据格式问题后。
* 以下是对外部服务配置或端点的更新。
* 您正在部署影响数据导出过程的自定义项。

通过主动监控馈送状态并及时解决故障，您可以维护整个Commerce生态系统的数据一致性和可靠性。

#### 手动重新同步馈送项目

如果需要重新同步特定馈送项目，请执行以下操作：

1. **选择记录**：使用复选框选择需要注意的失败记录。
2. **选择操作**：从批量操作下拉列表中选择&#x200B;**[!DNL Schedule Resync]**。
3. **确认**：单击&#x200B;**[!DNL Submit]**&#x200B;并确认重新同步操作。
4. **监视结果**：检查成功消息并监视状态更改。

## 最佳实践

### 定期监测

1. **每日检查**：每天查看概述页面，查看任何显示高失败率的馈送
1. **每周深入分析**：检查关键信息源（产品、价格）的详细状态
1. **每月分析**：跟踪导出成功率和性能趋势

### 工作流疑难解答

1. **识别问题**：查找错误和高失败计数
1. **检查索引器运行状况**：确保索引器有效并且积压可管理
1. **查看错误详细信息**：单击失败记录以查看特定错误消息
1. **计划重新同步**：使用批量操作重试失败的导出
1. **监视器分辨率**：验证重新同步的项目是否显示成功状态

### 修复常见问题

#### 高失败率

**症状**：大量记录显示“失败，需要注意”状态

**可能的原因**：

* 外部服务配置更改
* 数据格式不兼容
* 身份验证或权限问题

**解决步骤**：

1. 检查外部服务状态和配置
1. 查看错误消息以了解模式
1. 验证身份验证凭据
1. 如果需要，请联系外部服务支持

#### 导出性能缓慢

**症状**：更改日志积压过多，状态更新缓慢

**可能的原因**：

* 索引器性能问题
* 高数据量
* 外部服务速率限制

**解决步骤**：

1. 检查索引器状态，如果无效则重新运行
2. 监测外部服务响应时间
3. 考虑在非高峰时间安排导出
4. 审查系统资源和性能

#### 身份验证失败

**症状**： 401或403状态代码

**解决步骤**：

1. 验证API凭据和令牌
1. 检查外部服务帐户权限
1. 续订过期的身份验证令牌
1. 有关访问问题，请与服务提供商联系

>[!MORELIKETHIS]
>
>* [数据管理仪表板](https://experienceleague.adobe.com/en/docs/commerce-admin/systems/data-transfer/data-dashboard)
>* [SaaS数据导出指南](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/saas-data-export/overview)

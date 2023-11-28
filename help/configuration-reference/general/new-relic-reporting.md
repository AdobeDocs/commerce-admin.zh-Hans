---
title: ’[!UICONTROL General] &gt； [!UICONTROL New Relic Reporting]’
description: 查看 [!UICONTROL General] &gt； [!UICONTROL New Relic Reporting] 商务管理员页面。
exl-id: d6bf4810-81a3-420d-abc9-9b87c1e92551
feature: Configuration, System, Reporting
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 1%

---

# [!UICONTROL General] > [!UICONTROL New Relic Reporting]

{{config}}

## [!UICONTROL General]

![常规](./assets/new-relic-reporting-general.png)<!-- zoom -->

<!-- [General](https://docs.magento.com/user-guide/reports/new-relic-reporting.html) -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Enable New Relic Integration] | 商店视图 | 确定您的商店是否可用于 [!DNL New Relic] 报表。 选项： `Yes` / `No` |
| [!UICONTROL New Relic API URL] | 商店视图 | 部署New Relic API的URL。 例如： `https://api.newrelic.com/deployments.xml` |
| 分析API URL | 商店视图 | 从中部署分析API的URL。 使用百分比符号(%)表示您的帐户ID。 例如： `https://insights-collector.newrelic.com/v1/accounts/%s/events` |
| [!UICONTROL New Relic Account ID] | 商店视图 | 分配给您的帐户ID [!DNL New Relic] 帐户。 |
| [!UICONTROL New Relic Application ID] | 商店视图 | 分配给您的的应用程序ID [!DNL New Relic] 帐户，用于Commerce集成。 |
| [!UICONTROL New Relic API Key] | 商店视图 | 分配给您的用于访问 [!DNL New Relic] API。 |
| [!UICONTROL Insights API Key] | 商店视图 | 分配给您的用于获取Insights访问权限的键。 |
| [!UICONTROL New Relic Application Name] | 商店视图 | 您分配给您的姓名 [!DNL New Relic] 集成。 |
| [!UICONTROL Send Adminhtml and Frontend as Separate Apps] | 商店视图 | 一个选项，用于将为店面和管理员收集的报表数据作为单独的应用程序发送到New Relic。 此选项要求为输入名称 [!UICONTROL New Relic Application Name]. 该功能会将带下划线的应用程序名称附加到收集的应用程序数据中。 例如： `MyStore_Adminhtml`， `MyStore_frontend` |

{：style=&quot;table-layout：auto&quot;}

## [!UICONTROL Cron]

![Cron](./assets/new-relic-reporting-cron.png)<!-- zoom -->

<!-- Cron](https://docs.magento.com/user-guide/system/cron.html) -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Enable Cron] | 商店视图 | 确定 [!DNL New Relic] 报告可以通过以下方式按计划运行 [Cron](../../systems/cron.md). 选项： `Yes` / `No` |

{：style=&quot;table-layout：auto&quot;}

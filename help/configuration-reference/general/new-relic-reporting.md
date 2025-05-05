---
title: '[!UICONTROL General] &amp；gt； [!UICONTROL New Relic Reporting]'
description: 查看Commerce管理员的[!UICONTROL General] &amp；gt； [!UICONTROL New Relic Reporting]页面上的配置设置。
exl-id: d6bf4810-81a3-420d-abc9-9b87c1e92551
feature: Configuration, System, Reporting
source-git-commit: 5a4417373f6dc720e8e14f883c27348a475ec255
workflow-type: tm+mt
source-wordcount: '241'
ht-degree: 0%

---

# [!UICONTROL General] > [!UICONTROL New Relic Reporting]

{{config}}

>[!NOTE]
>这些配置选项不适用于云基础架构上的Adobe Commerce。
>
>如果您在Pro计划中，New Relic已[预配置并默认启用](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/monitor/new-relic/new-relic-service.html?lang=zh-Hans)。 如果您在入门计划中，则必须完成作为设置过程一部分的[New Relic配置步骤](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/monitor/new-relic/account-management.html?lang=zh-Hans#configure-new-relic-for-starter-environment)。

## [!UICONTROL General]

![常规](./assets/new-relic-reporting-general.png)<!-- zoom -->

<!-- [General](https://experienceleague.adobe.com/zh-hans/docs/commerce-admin/start/reporting/new-relic-reporting) -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Enable New Relic Integration] | 商店视图 | 确定您的存储是否可与[!DNL New Relic]报表一起使用。 选项： `Yes` / `No` |
| [!UICONTROL New Relic API URL] | 商店视图 | 部署New Relic API的URL。 例如： `https://api.newrelic.com/deployments.xml` |
| 分析API URL | 商店视图 | 从中部署分析API的URL。 使用百分比符号(%)表示您的帐户ID。 例如： `https://insights-collector.newrelic.com/v1/accounts/%s/events` |
| [!UICONTROL New Relic Account ID] | 商店视图 | 分配给您[!DNL New Relic]帐户的帐户ID。 |
| [!UICONTROL New Relic Application ID] | 商店视图 | 为Commerce集成分配给您[!DNL New Relic]帐户的应用程序ID。 |
| [!UICONTROL New Relic API Key] | 商店视图 | 分配给您的用于获取[!DNL New Relic] API访问权限的密钥。 |
| [!UICONTROL Insights API Key] | 商店视图 | 分配给您的用于获取Insights访问权限的键。 |
| [!UICONTROL New Relic Application Name] | 商店视图 | 您分配给[!DNL New Relic]集成的名称。 |
| [!UICONTROL Send Adminhtml and Frontend as Separate Apps] | 商店视图 | 一个选项，用于将为店面和管理员收集的报表数据作为单独的应用程序发送到New Relic。 此选项要求为[!UICONTROL New Relic Application Name]输入名称。 该功能会将带下划线的应用程序名称附加到收集的应用程序数据中。 例如： `MyStore_Adminhtml`，`MyStore_frontend` |

{style="table-layout:auto"}

## [!UICONTROL Cron]

![Cron](./assets/new-relic-reporting-cron.png)<!-- zoom -->

<!-- Cron](https://experienceleague.adobe.com/zh-hans/docs/commerce-admin/systems/tools/cron) -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Enable Cron] | 商店视图 | 确定是否可以使用[Cron](../../systems/cron.md)按计划运行[!DNL New Relic]报告。 选项： `Yes` / `No` |

{style="table-layout:auto"}

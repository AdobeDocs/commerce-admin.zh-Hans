---
title: “[!DNL New Relic]报告”
description: 了解Adobe Commerce在云基础架构上帐户可用的 [!DNL New Relic] 报告，包括New Relic APM服务的软件。
exl-id: 65d08bda-da01-4dcf-9d92-189d4d303c76
role: Admin, Leader
feature: System
source-git-commit: 0651a2489a396ab142b60a8678d6c7590fd5f9ee
workflow-type: tm+mt
source-wordcount: '1382'
ht-degree: 0%

---

# [!DNL New Relic]报告

[New Relic][1]是一项软件分析服务，可帮助您分析和改进应用程序交互。 云基础架构上的Adobe Commerce帐户包括[!DNL New Relic APM]服务的软件。 有关详细信息，请参阅《云基础架构上的New Relic指南》_Commerce_&#x200B;中的[Cloud Service][4]。

## 步骤1：注册[!DNL New Relic]帐户

1. 转到[[!DNL New Relic]][1]网站并注册帐户。

   您还可以注册免费试用帐户。

1. 按照网站上的说明进行操作。 出现提示时，首先选择要安装的产品。

1. 当您在帐户中时，找到完成 Commerce 配置所需的以下凭据：

   | 选择 | 描述 |
   | ------ | ----------- |
   | 帐户 ID | 在您的[!DNL New Relic]帐户仪表板中，帐户ID是URL中位于以下位置后的数字： `/accounts` |
   | 应用程序Id | 在您的[!DNL New Relic]帐户信息板中，单击&#x200B;**[!UICONTROL New Relic APM]**。 在菜单中，选择&#x200B;**[!UICONTROL Applications]**。 然后，选择您的应用程序。 应用程序 ID 是以下之后的 URL 中的数字： `/applications/` |
   | 新遗物 API 密钥 | 在您的[!DNL New Relic]帐户信息板中，单击&#x200B;**[!UICONTROL Account Settings]**。 在左侧的“集成”下的菜单中，选择&#x200B;**[!UICONTROL Data Sharing]**。 您可以在此页面创建、重新生成或删除您的API密钥。 |
   | 分析API密钥 | 在您的[!DNL New Relic]帐户信息板中，单击&#x200B;**[!UICONTROL Insights]**。 在左侧“管理”下的菜单中，选择&#x200B;**[!UICONTROL API Keys]**。 您的分析API密钥将显示在此页面上。 如有必要，请单击“插入密钥”旁边的加号(**+**)来生成密钥。 |

   {style="table-layout:auto"}

## 步骤2：在服务器上安装[!DNL New Relic]代理

要使用[!DNL New Relic APM Pro]收集和传输数据，必须在服务器上安装PHP代理。

1. 提示选择Web代理时，单击&#x200B;**PHP**。

1. 要在服务器上设置PHP代理，请按照说明操作。

   如果您需要帮助，请参阅[适用于PHP的New Relic][3]。

1. 确保cron在您的服务器上运行。

   要了解更多信息，请参阅开发人员文档中的[配置和运行cron][5]。

## 步骤3：配置存储

>[!NOTE]
>这些配置选项不适用于云基础架构上的Adobe Commerce。
>
>如果您在Pro计划中，New Relic已[预配置并默认启用](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/monitor/new-relic/new-relic-service.html)。 如果您在入门计划中，则必须完成作为设置过程一部分的[New Relic配置步骤](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/monitor/new-relic/account-management.html#configure-new-relic-for-starter-environment)。

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在展开&#x200B;**[!UICONTROL General]**&#x200B;的左侧导航面板中，选择&#x200B;**[!UICONTROL New Relic Reporting]**&#x200B;并执行以下操作：

   ![New Relic报表配置](./assets/new-relic-reporting-general.png){width="600"}

   * 将&#x200B;**[!UICONTROL Enable New Relic Integration]**&#x200B;设置为`Yes`。

   * 在&#x200B;**[!UICONTROL Insights API URL]**&#x200B;中，将百分比(`%`)符号替换为您的New Relic帐户ID。

   * 输入您的&#x200B;**[!UICONTROL New Relic Account ID]**。

   * 输入您的&#x200B;**[!UICONTROL New Relic Application ID]**。

   * 输入您的&#x200B;**[!UICONTROL New Relic API Key]**。

   * 输入您&#x200B;**[!UICONTROL Insights API Key]**。

1. 为&#x200B;**[!UICONTROL New Relic Application Name]**&#x200B;输入一个名称以标识供内部参考的配置。

1. （可选）对于&#x200B;**[!UICONTROL Send Adminhtml and Frontend as Separate Apps]**，选择`Yes`以将店面和管理员的收集数据作为单独的应用程序发送到New Relic。

   此选项要求为&#x200B;**[!UICONTROL New Relic Application Name]**&#x200B;输入名称。

   >[!NOTE]
   >
   >启用此功能可减少误报[!DNL New Relic]警报的数量，并允许严格配置监控和警报以获得前端性能。 New Relic接收单独的应用程序数据文件，其应用程序名称附加到`Adminhtml`和前端之后。 例如： `MyStore_Adminhtml`

1. 完成后，单击&#x200B;**[!UICONTROL Save Config]**。

## 步骤4：为[!DNL New Relic]报表启用Cron

1. 展开&#x200B;**[!UICONTROL Cron]**&#x200B;部分的![扩展选择器](../assets/icon-display-expand.png)。

   ![New Relic Cron配置](./assets/new-relic-reporting-cron.png){width="600"}

1. 将&#x200B;**[!UICONTROL Enable Cron]**&#x200B;设置为`Yes`。

1. 完成后，单击&#x200B;**[!UICONTROL Save Config]**。

## [!DNL New Relic]个查询

[!DNL New Relic Insights]数据基于[!DNL New Relic Query Language] (NRQL)中编写的语句以及您可能包含的任何自定义参数。 数据可以从临时查询返回，也可以通过保存到仪表板的查询返回。 若要了解详细信息，请参阅[!DNL New Relic]文档中的[NRQL引用][6]。

### 管理事件

#### 活动管理员用户

返回活动的管理员用户数。

    SELECT uniqueCount(AdminId)
    FROM Transaction
    WHERE appName=&#39;&lt;your_app_name>&#39; SINCE 15分钟前

#### 当前活动的管理员用户

返回活动管理员用户的名称。

    SELECT uniques(AdminName)
    FROM Transaction
    WHERE appName=&#39;&lt;your_app_name>&#39; SINCE 15分钟前

#### 最近的管理活动

返回最近的管理员操作数。

    SELECT count(AdminId)
    FROM Transaction
    WHERE appName =&#39;&lt;your_app_name>&#39; FACET AdminName自1天前

#### 最新管理活动

返回有关最近管理员操作的详细信息，包括管理员用户名、持续时间和应用程序名称。

    选择“管理员名称”、“持续时间”、“来自事务的名称”其中 appName=&#39;&lt;your_app_name>“和”管理员名称“不为空
    和”管理员名称！&lt;/your_app_name>
    
    = “不适用”限制 50

### Cron 事件

#### 类别计数

返回指定时间段内按类别划分的应用程序事件数。

    从Cron
    中选择AVERAGE(CatalogCategoryCount)
    其中CatalogCategoryCount不为NULL
    且appName = &#39;&lt;your_app_name>&#39;时序2分钟

#### 当前目录计数

返回指定时间段内按类别列出的目录中的平均应用程序事件数。

    从 Cron 中选择平均值（CatalogCategoryCount）
    FROM Cron
    其中 CatalogCategoryCount 不为 NULL
    且 CatalogCategoryCount >
    0 且 APPName = &#39;&lt;your_app_name>&#39; 自 2 分钟前 限制 1
&lt;/your_app_name>
#### 活性产品

返回指定时间段内按产品划分的应用程序事件数。

    从Cron
    中选择AVERAGE(CatalogProductActiveCount)
    其中CatalogProductActiveCount不为NULL
    且appName =“&lt;your_app_name>”时序2分钟

#### 活动产品计数

返回指定时间段内按产品划分的活动应用程序事件的平均数量。

    从Cron
    中选择AVERAGE(CatalogProductActiveCount)
    其中CatalogProductActiveCount不为NULL
    且CatalogProductActiveCount > 0
    AND appName = &#39;&lt;your_app_name>&#39;，2分钟前限制1

#### 可配置的产品

返回指定时间段内可配置产品的平均应用程序事件数。

    从Cron
    中选择AVERAGE(CatalogProductConfigurableCount)
    其中CatalogProductConfigurableCount不为NULL
    且appName = &#39;&lt;your_app_name>&#39;时序2分钟

#### 可配置产品计数

返回指定时间段内按可配置产品划分的应用程序事件的平均数量。

    从Cron
    中选择AVERAGE(CatalogProductConfigurableCount)
    其中CatalogProductConfigurableCount不为NULL
    且CatalogProductConfigurableCount > 0
    AND appName = &#39;&lt;your_app_name>&#39;，2分钟前限制1

#### 产品计数（全部）

返回所有产品的应用程序事件总数。

    从Cron
    中选择AVERAGE(CatalogProductCount)
    其中CatalogProductCount不为NULL
    且appName = &#39;&lt;your_app_name>&#39;时序2分钟

#### 当前产品计数（全部）

返回指定时间段内所有产品的平均应用程序事件数。

    从Cron
    中选择AVERAGE(CatalogProductCount)
    其中CatalogProductCount不为NULL
    且CatalogProductCount > 0
    且appName = &#39;&lt;your_app_name>&#39;，2分钟前限制1

#### 客户计数

返回按客户划分的应用程序事件的平均数。

从Cron
    中选择    AVERAGE(CustomerCount)
    其中CustomerCount不为NULL
    且CustomerCount > 0&lt;
    且appName = &#39;&lt;your_app_name>&#39;时序2分钟

#### 当前客户计数

返回指定时间段内的平均客户数。

从Cron
    中选择    AVERAGE(CustomerCount)
    其中CustomerCount不为NULL
    且CustomerCount > 0
    且appName = &#39;&lt;your_app_name>&#39;自2分钟前限制1

#### 模块状态

返回在指定时间段内启用、禁用或安装应用程序模块的平均次数。

    SELECT average(ModulesDisabled)， average(ModulesEnabled)， average
    (ModulesInstalled)
    FROM Cron&lt;
    WHERE appName = &#39;&lt;your_app_name>&#39; TIMESERIES 2分钟

#### 当前模块状态

返回在指定时间段内启用、禁用或安装模块的平均次数。

    SELECT average(ModulesDisabled)， average(ModulesEnabled)， average
    (ModulesInstalled)
    FROM Cron
    WHERE appName = &#39;&lt;your_app_name>&#39; SINCE 2分钟前LIMIT 1

#### 网站和商店计数

返回指定时间段内按网站和商店划分的应用程序事件平均数。

    SELECT average(StoreViewCount)， average(WebsiteCount)
    FROM Cron
    WHERE appName = &#39;&amp;amp；lt；your_app_name&amp;amp；gt；&#39; TIMESERIES 2分钟

#### 当前网站和商店计数

返回指定时间段内当前应用程序事件的平均数量。

    SELECT average(StoreViewCount)， average(WebsiteCount)
    FROM Cron
    WHERE appName = &#39;&lt;your_app_name>&#39; SINCE 2分钟前LIMIT 1

#### Cron — 来自事件的所有数据

返回所有应用程序事件数据。

    从Cron
    中选择*
    WHERE appName = &#39;&lt;your_app_name>&#39;

### 客户

#### 活动客户计数

返回指定时间段内的活跃客户数。

    SELECT uniqueCount(CustomerId)
    FROM Transaction
    WHERE appName = &#39;&lt;your_app_name>&#39;，从15分钟前开始

#### 活跃客户

返回指定时间段内活跃客户的名称。

    SELECT uniques(CustomerName)
    FROM Transaction
    WHERE appName=&#39;&lt;your_app_name>&#39; SINCE 15分钟前

#### 主要客户

返回指定时间段内排名最前的客户。

    SELECT count(CustomerId)
    FROM Transaction
    WHERE appName = &#39;&lt;your_app_name>&#39; FACET CustomerName自1天前

#### 最近的管理活动

返回近期活动的定义数量的记录，包括客户名称和访问持续时间。

    选择“客户名称”、“持续时间”、“事务中的名称”，其中 appName=&#39;&lt;your_app_name>&#39;
    AND CustomerName 不为 null
    和“CustomerName！”&lt;/your_app_name>
    
    = “不适用”限制 50

### 订单

#### 下订单数量

返回在指定时间段内下达的订单数。

    选择计数（订单）
    FROM 交易自 1 天前

#### 总订单值

返回在指定时间段内订购的行项目总数。

    选择 SUM（订单值）
    FROM 交易自 1 天前

#### 订购的订单项总数

返回在指定时间段内订购的行项目总数。

    SELECT sum(lineItemCount)
    FROM Transaction SINCE LATER 1天前


[1]: https://newrelic.com/
[3]: https://docs.newrelic.com/docs/agents/php-agent/getting-started/new-relic-php
[4]: https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/monitor/new-relic/new-relic-service.html
[5]: https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html
[6]: https://docs.newrelic.com/docs/insights/new-relic-insights/using-new-relic-query-language/nrql-reference

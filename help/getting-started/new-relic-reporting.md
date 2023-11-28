---
title: " [!DNL New Relic] 报告"
description: ' [!DNL New Relic] 了解在云架构上可用于 Adobe Systems 商务的帐户报告，其中包括新 RELIC APM 服务的软件。'
exl-id: 65d08bda-da01-4dcf-9d92-189d4d303c76
role: Admin, Leader
feature: System
source-git-commit: e9a7645aed0e3b48bf565b04cdb6a31ce5d39ca0
workflow-type: tm+mt
source-wordcount: '1361'
ht-degree: 0%

---

# [!DNL New Relic] 报告

[New Relic][1] 是一项软件分析服务，可帮助您分析和改进应用程序交互。 在云基础架构上使用Adobe Commerce的客户包括适用于以下产品的软件： [!DNL New Relic APM] 服务。 有关更多信息，请参阅 [New Relic服务][4] 在 _云基础架构上的Commerce指南_.

## 第1步：注册 [!DNL New Relic] 帐户

1. 转到 [[!DNL New Relic]][1] 网站并注册帐户。

   您还可以注册免费试用帐户。

1. 按照网站上的说明操作。 出现提示时，选择要首先安装的产品。

1. 在您的帐户中，找到完成商务配置所需的以下凭据：

   | 选项 | 描述 |
   | ------ | ----------- |
   | 帐户 ID | 来自您的 [!DNL New Relic] account dashboard中，Account ID是URL中位于以下位置之后的数字： `/accounts` |
   | 应用程序Id | 来自您的 [!DNL New Relic] 帐户仪表板，单击 **[!UICONTROL New Relic APM]**. 在菜单中，选择 **[!UICONTROL Applications]**. 然后，选择您的应用程序。 应用程序ID是URL中位于以下位置后的数字： `/applications/` |
   | New Relic API密钥 | 来自您的 [!DNL New Relic] 帐户仪表板，单击 **[!UICONTROL Account Settings]**. 在左侧的“集成”下的菜单中，选择 **[!UICONTROL Data Sharing]**. 您可以在此页面创建、重新生成或删除您的API密钥。 |
   | 分析API密钥 | 来自您的 [!DNL New Relic] 帐户仪表板，单击 **[!UICONTROL Insights]**. 在左侧的“管理”下的菜单中，选择 **[!UICONTROL API Keys]**. 您的分析API密钥将显示在此页面上。 如有必要，请单击加号(**+**)来生成密钥。 |

   {style="table-layout:auto"}

## 步骤2：安装 [!DNL New Relic] 服务器上的代理

使用 [!DNL New Relic APM Pro] 要收集和传输数据，必须在服务器上安装PHP代理。

1. 提示选择Web代理时，单击 **PHP**.

1. 要在服务器上设置PHP代理，请按照说明操作。

   如果您需要帮助，请参阅 [适用于PHP的New Relic][3].

1. 确保cron在您的服务器上运行。

   要了解更多信息，请参阅 [配置和运行cron][5] 在开发人员文档中。

## 步骤3：配置存储

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧导航面板中，其中 **[!UICONTROL General]** 已展开，请选择 **[!UICONTROL New Relic Reporting]** 并执行以下操作：

   ![New Relic报表配置](./assets/new-relic-reporting-general.png){width="600"}

   * 设置 **[!UICONTROL Enable New Relic Integration]** 到 `Yes`.

   * 在 **[!UICONTROL Insights API URL]**，替换百分比(`%`New Relic )符号。

   * 输入您的 **[!UICONTROL New Relic Account ID]**.

   * 输入您的 **[!UICONTROL New Relic Application ID]**.

   * 输入您的 **[!UICONTROL New Relic API Key]**.

   * 输入您 **[!UICONTROL Insights API Key]**.

1. 对象 **[!UICONTROL New Relic Application Name]**，输入名称以标识配置以供内部引用。

1. （可选）对于 **[!UICONTROL Send Adminhtml and Frontend as Separate Apps]**，选择 `Yes` 将店面和管理员的收集数据作为单独的应用程序发送到New Relic。

   此选项要求输入 **[!UICONTROL New Relic Application Name]** 的名称。

   >[!NOTE]
   >
   >启用此功能可减少误报次数 [!DNL New Relic] 警报，允许严格配置监控和警报，以获得前端性能。 New Relic接收单独的应用程序数据文件，并在文件中附加应用程序名称 `Adminhtml` 以及前端。 例如： `MyStore_Adminhtml`

1. 完成后，单击 **[!UICONTROL Save Config]**.

## 步骤4：为启用Cron [!DNL New Relic] 报告

1. 展开 ![ 区域选择器 ](../assets/icon-display-expand.png) **[!UICONTROL Cron]** 扩展。

   ![New Relic Cron配置](./assets/new-relic-reporting-cron.png){width="600"}

1. 设置 **[!UICONTROL Enable Cron]** 到 `Yes`.

1. 完成后，单击 **[!UICONTROL Save Config]**.

## [!DNL New Relic] 查询

[!DNL New Relic Insights] 数据基于写入的语句 [!DNL New Relic Query Language] (NRQL)以及您可能包含的任何自定义参数。 数据可以从临时查询返回，也可以通过保存到仪表板的查询返回。 要了解更多信息，请参阅 [NRQL引用][6] 在 [!DNL New Relic] 文档。

### 管理事件

#### 活动管理员用户

返回活动的管理员用户数。

    选择独特计数(AdminId)
    FROM事务
    其中appName=&#39;&lt;your_app_name>&#39;从15分钟前开始

#### 当前活动的管理员用户

返回活动管理员用户的名称。

    从事务 
     中选择独特（AdminName） 
     ，其中 appName = &#39;&lt;your_app_name>&#39; 自15分钟前 
 &lt;/your_app_name>
#### 最近的管理活动

返回最近的管理员操作数。

    选择计数（管理员ID）
    FROM事务
    其中appName =&#39;&lt;your_app_name>&#39; FACET AdminName自1天前

#### 最新管理活动

返回有关最近管理操作的详细信息，包括管理员用户名、持续时间和应用程序名称。

    选择 AdminName，duration，来自 appName = &#39;&lt;your_app_name>&#39; 且 ADMINNAME 不为 NULL 
     和 AdminName&lt;/your_app_name>的事务 
     中的名称 
     ！= &quot;N/A&quot; 限制50

### Cron 事件

#### 类别计数

返回指定时间段内按类别列出的应用程序事件数。

    SELECT average(CatalogCategoryCount)
    来自Cron
    其中CatalogCategoryCount不为空
    和appName = &#39;&lt;your_app_name>&#39;时间表2分钟

#### 当前目录计数

返回指定时间段内按类别列出的目录中的平均应用程序事件数。

    SELECT average(CatalogCategoryCount)
    来自Cron
    其中CatalogCategoryCount不为空
    AND CatalogCategoryCount > 0
    和appName = &#39;&lt;your_app_name>&#39;自2分钟前限制1

#### 活动的产品

返回指定时间段内按产品划分的应用程序事件数。

    SELECT average(CatalogProductActiveCount)
    来自Cron
    其中CatalogProductActiveCount不为空
    和appName = &#39;&lt;your_app_name>&#39;时间表2分钟

#### 活动产品计数

返回指定时间段内按产品划分的活动应用程序事件的平均数量。

    SELECT average(CatalogProductActiveCount)
    来自Cron
    其中CatalogProductActiveCount不为空
    并且CatalogProductActiveCount > 0
    和appName = &#39;&lt;your_app_name>&#39;自2分钟前限制1

#### 可配置的产品

返回指定时间段内可配置产品的平均应用程序事件数。

    SELECT average(CatalogProductConfigurableCount)
    来自Cron
    其中CatalogProductConfigurableCount不为空
    和appName = &#39;&lt;your_app_name>&#39;时间表2分钟

#### 可配置产品计数

返回指定时间段内按可配置产品划分的应用程序事件的平均数量。

    SELECT average(CatalogProductConfigurableCount)
    来自Cron
    其中CatalogProductConfigurableCount不为空
    AND CatalogProductConfigurableCount > 0
    和appName = &#39;&lt;your_app_name>&#39;自2分钟前限制1

#### 产品计数（全部）

返回所有产品的应用程序事件总数。

    SELECT average(CatalogProductCount)
    来自Cron
    其中CatalogProductCount不为空
    和appName = &#39;&lt;your_app_name>&#39;时间表2分钟

#### 当前产品计数（全部）

返回指定时间段内所有产品的平均应用程序事件数。

    SELECT average(CatalogProductCount)
    来自Cron
    其中CatalogProductCount不为空
    并且CatalogProductCount > 0
    和appName = &#39;&lt;your_app_name>&#39;自2分钟前限制1

#### 客户计数

返回按客户划分的应用程序事件的平均数。

    SELECT average(CustomerCount)
    来自Cron
    其中CustomerCount不为空
    并且CustomerCount > 0&lt;
    和appName = &#39;&lt;your_app_name>&#39;时间表2分钟

#### 当前客户计数

返回指定时间段内的平均客户数。

    SELECT average(CustomerCount)
    来自Cron
    其中CustomerCount不为空
    并且CustomerCount > 0
    和appName = &#39;&lt;your_app_name>&#39;自2分钟前限制1

#### 模块状态

返回在指定时间段内启用、禁用或安装应用程序模块的平均次数。

    SELECT average(ModulesDisabled)， average(ModulesEnabled)， average
    （已安装模块）
    来自Cron&lt;
    其中appName = &#39;&lt;your_app_name>&#39;时间表2分钟

#### 当前模块状态

返回在指定时间段内启用、禁用或安装模块的平均次数。

    SELECT average(ModulesDisabled)， average(ModulesEnabled)， average
    （已安装模块）
    来自Cron
    其中appName = &#39;&lt;your_app_name>&#39;自2分钟前限制1

#### 网站和商店计数

返回指定时间段内按网站和商店划分的应用程序事件平均数。

    SELECT average(StoreViewCount)， average(WebsiteCount)
    来自Cron
    WHERE appName = &#39;&amp;lt；your_app_name&amp;gt；&#39; TIMESERIES 2分钟

#### 当前网站和商店计数

返回指定时间段内当前应用程序事件的平均数量。

    SELECT average(StoreViewCount)， average(WebsiteCount)
    来自Cron
    其中appName = &#39;&lt;your_app_name>&#39;自2分钟前限制1

#### Cron — 来自事件的所有数据

返回所有应用程序事件数据。

    选择*
    来自Cron
    其中appName = &#39;&lt;your_app_name>’

### 客户

#### 活动客户计数

返回指定时间段内的活跃客户数。

    SELECT uniqueCount(CustomerId)
    FROM事务
    其中appName = &#39;&lt;your_app_name>&#39;从15分钟前开始

#### 活跃客户

返回指定时段期间活动客户的名称。

    从事务 
     中选择独特（CustomerName） 
     ，其中 appName = &#39;&lt;your_app_name>&#39; 自15分钟前 
 &lt;/your_app_name>
#### 主要客户

返回指定时间段内排名最前的客户。

    SELECT count(CustomerId)
    FROM事务
    其中appName = &#39;&lt;your_app_name>&#39; FACET CustomerName自1天前起

#### 最近的管理活动

返回最近活动记录的定义数量，包括客户名称和访问的持续时间。

    选择 CustomerName，duration，来自 appName = &#39;&lt;your_app_name>&#39; 
     且 CustomerName 不为 NULL 
     和 CustomerName&lt;/your_app_name>的事务 
     中的名称 
     ！= &quot;N/A&quot; 限制50

### 订单

#### 订购数量

返回指定时段中的订购次数。

    SELECT count(Order)
    自1天前开始的FROM事务

#### 总订单值

返回在指定时间段内订购的行项目总数。

    SELECT sum(orderValue)
    自1天前开始的FROM事务

#### 订购的行项目总数

返回在指定时间段内订购的行项目总数。

    SELECT sum(lineItemCount)
    自1天前开始的FROM事务


[1]: https://newrelic.com/
[3]: https://docs.newrelic.com/docs/agents/php-agent/getting-started/new-relic-php
[4]: https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/monitor/new-relic/new-relic-service.html
[5]: https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html
[6]: https://docs.newrelic.com/docs/insights/new-relic-insights/using-new-relic-query-language/nrql-reference

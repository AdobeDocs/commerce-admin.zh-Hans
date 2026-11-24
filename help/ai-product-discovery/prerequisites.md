---
title: AI产品发现先决条件
description: 查看目录扩充和PDP扩充要求，并将共享扩充扩展安装在云基础架构或内部部署上的Adobe Commerce上。
role: Admin, Developer
source-git-commit: 9e234eb68fe34171d9e5cf95e8cdab5c31825492
workflow-type: tm+mt
source-wordcount: '505'
ht-degree: 0%
---
# 先决条件

在使用目录扩充或PDP扩充之前，请确认适用于每个部署的要求，然后完成您的Commerce平台的设置。

## 所有部署的要求 {#all-deployments}

| 要求 | 应用于 | 详细信息 |
| --- | --- | --- |
| 在Edge进行优化 | PDP扩充 | 必需。 Edge中的优化可将扩充的产品数据交付给AI代理。 请参阅[Edge优化指南](https://experienceleague.adobe.com/zh-hans/docs/brand-visibility/using/resources/optimize-at-edge/fastly-byocdn)。 |
| 日志转发 | 两个工作流 | 可选。 根据代理流量启用扩充推荐。 如果没有它，您仍然可以手动选择产品或产品页面。 请参阅[日志转发指南](https://experienceleague.adobe.com/zh-hans/docs/brand-visibility/using/log-forwarding/log-forwarding-overview)。 |
| 可爬网店面 | 目录扩充 | 对于基于抓取的建议，此为必需字段。 面向LLM和代理的机器人必须能够访问您的产品页面。 |
| [!DNL Adobe Admin Console]访问权限 | 目录扩充 | 必需。 在安装期间，[!DNL Adobe Commerce]检查您的组织是否已签署GenAI骑士或选择退出基础人工智能服务。 |

<!--
TBD (SME): The Optimize at Edge guide is a Brand Visibility reference, not a Commerce setup guide. Add Commerce-specific Optimize at Edge setup instructions (this might be automated by GA).
TBD (SME): Confirm whether the Admin Console and GenAI rider check also applies to PDP enrichment.
-->

## 设置您的Commerce平台 {#set-up}

>[!BEGINTABS]

>[!TAB 云基础架构或内部部署上的 Commerce]

对于云基础结构或内部部署上的[!DNL Adobe Commerce]，请安装共享扩充扩展，该扩展支持目录扩充和PDP扩充。

**开始之前：**

- PHP 8.3或更高版本上的[!DNL Adobe Commerce] 2.4.7或更高版本。 请参阅[发行说明](release-notes.md)。
- [!DNL Adobe IMS]组织。 如果您的组织没有集成概述，请参阅[Adobe IMS集成概述](https://experienceleague.adobe.com/zh-hans/docs/commerce-admin/start/admin/ims/adobe-ims-integration-overview)。 目录扩充使用登录管理员用户的IMS访问令牌。 仅使用Commerce用户名和密码登录不会提供此令牌。
- 对Commerce应用程序服务器的命令行访问权限，以及从`repo.magento.com`下载包的权限。

**安装并验证：**

1. 如果既未启用[!DNL Live Search]也未启用[!DNL Product Recommendations]，请从您的Commerce项目目录添加[!DNL Catalog Service]：

   ```bash
   composer require magento/catalog-service --no-update
   composer update magento/catalog-service
   ```

   [!DNL Catalog Service]自动与[!DNL Live Search]和[!DNL Product Recommendations]一起安装，因此如果任一服务已启用，请跳过此步骤。

1. 如果尚未为其他Commerce服务配置此项，请使用API密钥和SaaS数据空间配置[Commerce服务连接器](https://experienceleague.adobe.com/zh-hans/docs/commerce/user-guides/integration-services/saas)。

1. 添加共享扩充扩展：

   ```bash
   composer require magento/module-catalog-enrichment --no-update
   composer update magento/module-catalog-enrichment
   ```

1. 部署更改：

   - **云基础架构：**&#x200B;提交更改并将更改推送到`composer.json`和`composer.lock`。
   - **内部部署：**&#x200B;升级应用程序并清除缓存：

     ```bash
     bin/magento setup:upgrade
     bin/magento cache:clean
     ```

1. 在Admin中，转到&#x200B;**[!UICONTROL System]** > **[!UICONTROL Data Transfer]** > **[!UICONTROL Data Feed Sync Status]**，并确认Commerce导出目录数据。

   成功发送的产品记录数应与源记录匹配，无失败或等待提交。 对于失败的记录，请查看错误详细信息，解决问题，并计划重新同步受影响的记录。

1. 前往&#x200B;**[!UICONTROL System]** > **[!UICONTROL Data Transfer]** > **[!UICONTROL Data Management Dashboard]**，并确认预期的目录数据在[!DNL Catalog Service]中可用。

有关状态详细信息和疑难解答，请参阅[监视数据馈送状态](/help/systems/data-feed-sync-status.md#monitor-data-feed-status)。

>[!TAB Adobe Commerce as a Cloud Service]

对于[!DNL Adobe Commerce as a Cloud Service]，在帐户设置期间为您处理[!DNL Catalog Service]的安装、目录扩充和PDP扩充。

完成所有部署[&#128279;](#all-deployments)的要求，这些要求适用于您计划使用的工作流。

<!-- TBD (SME): Confirm whether merchants on Adobe Commerce as a Cloud Service should verify catalog data on the Data Management Dashboard, and whether the IMS and Admin Console requirements apply. -->

>[!ENDTABS]

## 下一步 {#next-step}

[配置扩充设置](settings.md)以将您的Commerce实例连接到AI产品发现。

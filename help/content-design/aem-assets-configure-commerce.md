---
title: 安装和配置Experience Manager Assets集成
description: 了解如何安装和配置 [!DNL AEM Assets Integration for Adobe Commerce]
feature: CMS, Media
exl-id: 2f8b3165-354d-4b7b-a46e-1ff46af553aa
source-git-commit: da98c253d0d3f773551c7b58b5eedbb1db622ac6
workflow-type: tm+mt
source-wordcount: '1261'
ht-degree: 0%

---

# 安装和配置适用于Commerce的AEM Assets集成

{{$include /help/_includes/aem-assets-integration-beta-note.md}}

通过将扩展添加到AEM Assets应用程序、连接到Commerce SaaS服务、电子Adobe I/O事件服务并连接到Commerce，安装和配置适用于Commerce的Commerce集成。

## 系统要求

**软件要求**

- Adobe Commerce 2.4.5+
- PHP 8.1、8.2和8.3
- Composer： 2.x

**配置要求**

- 必须将Adobe Commerce配置为使用[Adobe IMS身份验证](/help/getting-started/adobe-ims-config.md)。
- 帐户配置和权限
   - [Commerce cloud项目管理员](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/project/user-access) — 安装所需的扩展，并通过管理员或命令行配置Commerce应用程序服务器
   - [Commerce管理员](https://experienceleague.adobe.com/en/docs/commerce-admin/start/guide-overview) — 更新商店配置并管理Commerce用户帐户

## 配置概述

通过完成以下任务启用集成：

1. [安装AEM Assets集成扩展(`aem-assets-integration`)](#install-the-aem-assets-integration-extension)。
1. [配置Commerce Service Connector](#configure-the-commerce-services-connector)，将您的Adobe Commerce实例与支持在Adobe Commerce和AEM Assets之间传输数据的服务连接起来。
1. [为Commerce配置Adobe I/O事件](#configure-adobe-io-events-for-commerce)
1. [获取API访问的身份验证凭据](#get-authentication-credentials-for-api-access)

## 安装AEM Assets集成扩展

>[!BEGINSHADEBOX]

**预修课程**

- 访问[repo.magento.com](https://repo.magento.com/admin/dashboard)以安装扩展。 有关密钥生成和获取必要的权限，请参阅[获取您的身份验证密钥](https://experienceleague.adobe.com/en/docs/commerce-operations/installation-guide/prerequisites/authentication-keys)。 有关云安装，请参阅[云基础架构上的Commerce指南](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/authentication-keys)

- 访问Adobe Commerce应用程序服务器的命令行。

>[!ENDSHADEBOX]

在运行AEM Assets 2.4.4或更高版本的Adobe Commerce上安装最新版本的Adobe Commerce集成扩展(`aem-assets-integration`)。 AEM资产集成是作为[repo.magento.com](https://repo.magento.com/admin/dashboard)存储库中的编辑器中继包提供的。

>[!BEGINTABS]

>[!TAB 云基础架构]

使用此方法为Commerce Cloud实例安装[!DNL AEM Assets Integration]扩展。

1. 在本地工作站上，转到云基础架构项目上Adobe Commerce的项目目录。

   >[!NOTE]
   >
   >有关在本地管理Commerce项目环境的信息，请参阅《云基础架构用户指南》_上的_ Adobe Commerce中的[使用CLI管理分支](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/cli-branches)。

1. 请查看环境分支，以使用Adobe Commerce Cloud CLI进行更新。

   ```shell
   magento-cloud environment:checkout <environment-id>
   ```

1. 添加适用于Commerce的AEM Assets集成扩展。

   ```shell
   composer require "magento/aem-assets-integration" "<version-tbd>" --no-update
   ```

1. 更新包依赖关系。

   ```shell
   composer update "magento/aem-assets-integration"
   ```

1. 提交和推送`composer.json`和`composer.lock`文件的代码更改。

1. 添加、提交并将`composer.json`和`composer.lock`文件的代码更改推送到云环境。

   ```shell
   git add -A
   git commit -m "Install AEM Assets Integration extension for Adobe Commerce"
   git push origin <branch-name>
   ```

   推送更新将启动[Commerce云部署流程](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/deploy/process)以应用更改。 从[部署日志](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/test/log-locations#deploy-log)中检查部署状态。

>[!TAB 内部部署]

使用此方法为内部部署实例安装[!DNL AEM Assets Integration]扩展。

1. 使用编辑器将AEM Assets Integration for Commerce扩展添加到您的项目中：

   ```shell
   composer require "magento/aem-assets-integration" --no-update
   ```

1. 更新依赖项并安装扩展：

   ```shell
   composer update  "magento/aem-assets-integration"
   ```

1. 升级Adobe Commerce：

   ```shell
   bin/magento setup:upgrade
   ```

1. 清除缓存：

   ```shell
   bin/magento cache:clean
   ```

   >[!TIP]
   >
   >在某些情况下，特别是在部署到生产环境时，您可能希望避免清除编译的代码，因为这样可能需要一些时间。 在进行任何更改之前，请确保备份系统。

>[!ENDTABS]

## 配置Commerce服务连接器

Commerce服务连接器支持在Commerce实例、资产规则引擎服务和其他支持服务之间进行数据同步和通信。

>[!NOTE]
>
>Commerce服务连接器设置是使用[Adobe Commerce SaaS服务](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/user-guides/integration-services/saas#availableservices)所需的一次性进程。 如果您已经为其他服务配置了连接器，则可以通过选择&#x200B;**[!UICONTROL Systems]** > [!UICONTROL Services] > **[!UICONTROL Commerce Services Connector]**&#x200B;从Commerce管理员中查看现有配置。

要在您的Adobe Commerce实例与支持AEM Assets集成的服务之间传输数据，请使用以下内容配置Commerce服务连接器：

- 使用用于身份验证的生产和沙盒API密钥配置Commerce实例。
- 指定用于安全云存储的数据空间（SaaS标识符）。
- 登录用于访问AEM Assets的同一IMS组织，以建立数据集与Adobe Experience Platform之间的连接。

有关详细说明，请参阅[Commerce Services Connector](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/user-guides/integration-services/saas#organizationid)。

配置Commerce服务连接器时，系统会生成SaaS项目和数据库ID。 在租户新用户引导过程中，您需要这些ID。

用于AEM Assets集成的![SaaS项目和数据空间ID](assets/aem-saas-project-config.png){width="600" zoomable="yes"}

## 为Commerce配置Adobe I/O事件

AEM Assets集成使用Adobe I/O事件服务在Commerce实例和Experience Cloud之间发送自定义事件数据。 事件数据用于协调AEM Assets集成的工作流。

>[!BEGINSHADEBOX]

**预修课程**

- 确保已启用RabbitMQ并监听事件。
   - [本地Adobe Commerce的RabbitMQ设置](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/configure/service/rabbitmq)
   - 云基础架构上Adobe Commerce的[RabbitMQ设置](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/configure/service/rabbitmq)

>[!ENDSHADEBOX]

>[!NOTE]
>
>有关CommerceAdobe I/O事件的详细信息，请参阅Adobe Developer网站上的[CommerceAdobe I/O事件](https://developer.adobe.com/commerce/extensibility/events/)文档。

设置需要以下步骤。

1. 通过在应用程序服务器和管理员中配置Adobe I/O事件，启用Commerce事件框架。
1. 通过使用Adobe Commerce规则引擎服务API配置连接，在Assets和AEM Assets之间启用数据同步。
1. 在管理员中启用AEM Assets集成。

### 启用Commerce事件框架

使用有关部署Commerce项目的环境的说明，启用Commerce事件框架。

>[!BEGINTABS]

>[!TAB 云基础架构]

1. 从[!DNL Store Settings Configuration]菜单启用Adobe I/O事件服务。

   1. 从管理员转到&#x200B;**[!UICONTROL Stores]** > [!UICONTROL Settings] > **[!UICONTROL Configuration]** > **[!UICONTROL Adobe Services]** > **Adobe I/O活动**。

   1. 展开&#x200B;**[!UICONTROL Commerce events]**。

   1. 将&#x200B;**[!UICONTROL Enabled]**&#x200B;设置为`Yes`。

      ![Adobe I/O事件Commerce管理员配置 — 启用Commerce事件](assets/aem-enable-io-event-admin-config.png){width="600" zoomable="yes"}

      >[!NOTE]
      >
      >[启用cron](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/#check-cron-and-message-queue-configuration)，以便Commerce可以向API端点发送事件来管理集成的通信和工作流。

1. 更新云项目配置。

   1. 将`app/etc/config.php`文件添加到您的工作存储库：

   ```shell
   git add app/etc/config.php
   ```

   1. 运行`composer info magento/ece-tools`命令以确定您的ece-tools版本。 如果版本小于`2002.1.13`，则[更新到最新版本](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/dev-tools/ece-tools/update-package)。

   1. 在`.magento.env.yaml`文件中启用事件：

      ```yaml
      stage:
         global:
            ENABLE_EVENTING: true
      ```

   1. 提交更新的文件并将其推送到云环境。

>[!TAB 内部部署]

1. 从[!DNL Store Settings Configuration]菜单启用Adobe I/O事件服务。

   1. 从管理员转到&#x200B;**[!UICONTROL Stores]** > [!UICONTROL Settings] > **[!UICONTROL Configuration]** > **[!UICONTROL Adobe Services]** > **Adobe I/O活动**。

   1. 展开&#x200B;**[!UICONTROL Commerce events]**。

   1. 将&#x200B;**[!UICONTROL Enabled]**&#x200B;设置为`Yes`。

      ![Adobe I/O事件Commerce管理员配置 — 启用Commerce事件](assets/aem-enable-io-event-admin-config.png){width="600" zoomable="yes"}

      >[!NOTE]
      >
      >[启用cron作业](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/#check-cron-and-message-queue-configuration)，以便Commerce能够发送事件来管理AEM资源和Commerce之间的通信和工作流。

>[!ENDTABS]

## 获取API访问的身份验证凭据

适用于Commerce的AEM Assets集成需要OAuth身份验证凭据，才能允许通过API访问Commerce实例。 在租户新用户引导期间，您需要这些凭据向Commerce规则引擎服务注册Assets项目，并提交API请求以管理Adobe Commerce和AEM Assets之间的资源。

通过将集成添加到Commerce实例并激活它，可生成凭据。

### 将集成添加到Commerce环境

1. 从管理员中，转到&#x200B;**系统** >扩展> **集成**，然后单击&#x200B;**添加新集成**。

1. 输入有关集成的信息。

   在&#x200B;**常规**&#x200B;部分中，仅指定集成&#x200B;**名称**&#x200B;和&#x200B;**电子邮件**。 为有权访问部署Commerce和Experience Manager Assets的组织的Adobe IMS帐户使用电子邮件。

   适用于Commerce管理员配置的![AEM Assets集成](assets/aem-add-commerce-integration.png){width="600" zoomable="yes"}

1. 单击&#x200B;**确认身份**&#x200B;以验证您的身份。

   系统会使用您的AdobeID向Experience Cloud进行身份验证，以验证您的身份。

1. 配置API资源。

   1. 从左侧面板中，单击&#x200B;**[!UICONTROL API]**。
E
   1. 选择外部媒体资源&#x200B;**[!UICONTROL Catalog > Inventory > Products > External Media]**。

   API资源的![管理员集成配置](assets/aem-commerce-integration-api-resources.png){width="600" zoomable="yes"}

1. 单击&#x200B;**[!UICONTROL Save]**。

### 生成凭据

在“集成”页面上，通过单击Assets集成的&#x200B;**激活**&#x200B;来生成OAuth身份验证凭据。 您需要这些凭据才能在Assets规则引擎服务中注册Commerce项目，并提交API请求以管理Adobe Commerce和AEM Assets之间的资源。

1. 在“集成”页面中，单击&#x200B;**[!UICONTROL Activate]**&#x200B;以生成凭据。

   为Assets集成![激活Commerce配置](assets/aem-activate-commerce-integration.png){width="600" zoomable="yes"}

1. 保存使用者密钥和访问令牌的凭据以供将来使用。

![用于验证API请求的OAuth凭据](./assets/aem-commerce-integration-credentials.png){width="600" zoomable="yes"}

1. 单击&#x200B;**[!UICONTROL Done]**。

>[!NOTE]
>
>您还可以使用Adobe Commerce API生成身份验证凭据。 有关此过程的详细信息，以及有关Adobe Commerce基于OAuth的身份验证的更多信息，请参阅Adobe Developer文档中的[基于OAuth的身份验证](https://developer.adobe.com/commerce/webapi/get-started/authentication/gs-authentication-oauth/)。

---
title: 为Commerce管理员配置Experience Cloud集成
description: 了解如何配置Commerce项目以通过Experience Cloud启用管理员访问权限。
hide: false
hidefromtoc: false
feature: Integration
role: Admin, Leader
exl-id: b2522d25-8255-4219-98b5-4b764430dea2
source-git-commit: 8278d725a7377b865c118b86a57702cd2be43238
workflow-type: tm+mt
source-wordcount: '1011'
ht-degree: 0%

---

# 配置与Commerce管理员的Experience Cloud集成

通过将CommerceExperience Cloud配置为使用Commerce Admin Unified Experience和Commerce Events扩展，开始使用Commerce与管理员的应用程序集成。


## 先决条件

- 必须将Adobe Commerce配置为使用[Adobe IMS身份验证](../getting-started/adobe-ims-config.md)
- 帐户设置和权限 — 管理员必须具有[Adobe业务配置文件](https://helpx.adobe.com/cn/enterprise/kb/introducing-adobe-profiles.html#:~:text=Adobe%20profiles%20help%20you%20manage,under%20the%20same%20email%20address)，并且有权访问以下资源以配置Experience Cloud集成：
   - [Adobe Admin Console](https://helpx.adobe.com/cn/enterprise/admin-guide.html) — 为组织添加和管理Adobe用户和开发人员帐户
   - [Adobe Developer Console](https://developer.adobe.com/developer-console/docs/guides/getting-started/) — 具有开发人员或系统管理员访问权限，可创建App Builder项目并生成连接凭据和项目配置以使用Adobe I/O事件服务
   - [云基础架构项目上的Commerce](https://experienceleague.adobe.com/docs/commerce-cloud-service/start/onboarding.html?lang=zh-Hans#get-started-with-the-project-web-interface) — 使用Adobe Commerce CLI安装所需模块并配置Commerce应用程序服务器
   - [Commerce管理员](https://experienceleague.adobe.com/docs/commerce-admin/start/guide-overview.html?lang=zh-Hans) — 更新商店配置并管理Commerce用户帐户

## 配置概述

通过完成以下任务启用集成：

1. [检查Commerce环境和应用程序配置](#check-the-commerce-environment-and-application-configuration)。

1. [启用Commerce Admin Unified Experience扩展](#enable-the-commerce-admin-unified-experience-extension)。

1. [为Commerce](#set-up-adobe-io-events)设置Adobe I/O事件。

1. [测试集成](#test-the-integration)。

## 检查Commerce环境和应用程序配置

在配置Experience Cloud集成之前，请验证您的项目和Commerce应用程序是否符合要求。

1. 在本地工作站上，转到Commerce项目的项目目录。

1. 请查看实例的环境分支以与Experience Cloud集成。

1. 验证是否已启用Adobe IMS。

   - 使用环境的[SSH访问URL](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/secure-connections.html?lang=zh-Hans)连接到Commerce应用程序服务器。

   - 在命令行中，使用Adobe Commerce CLI检查IMS模块状态。

     ```bash
     bin/magento admin:adobe-ims:status
     ```

   如果未启用该模块，则[使用IMS集成项目的组织和凭据启用它](../getting-started/adobe-ims-config.md#step-3-enable-the-adminadobeims-module)。

1. 验证管理员用户是否可以使用其Adobe ID登录Commerce管理员。

   - 转到Commerce管理员URL。

   - 如果您已登录，请注销。

   - 确保重定向管理员用户，以使用其Adobe ID登录。

     ![Adobe Commerce使用Adobe ID登录](./assets/admin-adobeid-login.png){width="600" zoomable="yes"}

1. 从本地工作站上的云项目目录中，验证是否已安装Commerce Admin Unified Experience扩展。

   ```bash
   composer show *unified-experience*
   ```

   如果已安装扩展，则Composer会返回扩展名称和描述。

   ```
   magento/module-unified-experience <version> Commerce module responsible for integration with Adobe Experience Cloud
   ```

   如果未安装该扩展，请使用Composer进行安装。 然后，提交更改并重新部署云环境。

   ```
   composer require magento/module-unified-experience
   composer update
   ```

## 启用Commerce管理统一体验

启用Commerce Admin Unified Experience扩展，然后通过Experience Cloud登录。

>[!NOTE]
>
>这些说明显示了Commerce Cloud项目管理员如何使用Adobe Commerce CLI启用该扩展。 Commerce管理员用户还可以通过更新[Commerce商店配置设置](admin-unified-experience-integration-manage.md#from-the-commerce-admin)来启用该扩展。

1. 从本地工作站上云项目环境的根目录中，使用[magento-cloud CLI工具](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/dev-tools/cloud-cli/cloud-cli-overview.html?lang=zh-Hans)登录到Commerce应用程序服务器。

   ```bash
   magento-cloud ssh
   ```

1. 使用Adobe Commerce CLI启用`magento/module-unified-experience`扩展：

   ```bash
   bin/magento config:set admin/unified_experience/enabled 1
   Admin Unified Experience integration is enabled
   ```

1. 清除缓存。

   ```bash
   bin/magento cache:clean
   ```

## 为Commerce设置Adobe I/O事件

启用Experience Cloud集成后，Adobe I/O事件服务会将Commerce事件数据发送到Experience Cloud，以管理管理员对Commerce项目的访问权限。 服务设置需要启用Commerce扩展(`magento/commerce-eventing`)的Adobe I/O事件并在Admin中配置Adobe I/O事件服务。

### 启用Commerce事件

启用Commerce Events扩展(`magento/commerce-eventing`)，将自定义事件数据从Commerce应用程序发送到Adobe I/O事件服务。

>[!NOTE]
>
>对于Commerce 2.4.6及更高版本，默认情况下会安装Commerce Events扩展。 对于使用Commerce 2.4.5的Commerce项目，请首先使用Composer来[安装扩展](https://developer.adobe.com/commerce/extensibility/events/installation/#install-adobe-io-modules-on-commerce)，然后启用它。

1. 从本地Commerce项目开发环境中，将以下配置添加到`.magento.env.yaml`文件。

   ```yaml
   stage:
     global:
       ENABLE_EVENTING: true
     deploy:
       CRON_CONSUMERS_RUNNER:
         cron_run: true
         max_messages: 0
         consumers: []
   ```

1. 添加、提交更新的`.magento.env.yaml file`并将其部署到云环境。

>[!TIP]
>
>有关使用`.magento.env.yaml`文件配置和管理环境变量的详细信息，请参阅[为部署配置环境变量](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/env/configure-env-yaml.html?lang=zh-Hans)。

### 配置Commerce事件集成

通过完成以下任务来配置Commerce事件集成。 有关详细说明，请参阅[CommerceAdobe I/O活动](https://developer.adobe.com/commerce/extensibility/events/project-setup/)开发人员文档。

1. [创建一个App Builder项目](https://developer.adobe.com/commerce/extensibility/events/project-setup/)以从Commerce实例接收事件数据。

   您需要来自App Builder项目的凭据和配置数据，才能在Commerce管理员中配置集成。

1. 配置Adobe Commerce以使用Adobe I/O事件。

   - [更新Adobe I/O事件服务的存储区配置设置](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/#begin-configuring-events-on-commerce)。

   - [配置事件提供程序以发送Commerce事件](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/#create-an-event-provider-and-complete-the-commerce-configuration)。

1. [更新App Builder项目以从Commerce实例](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/#subscribe-and-register-events)接收事件数据。

   请勿注册或订阅来自Commerce实例的事件。 在为App Builder应用程序配置事件提供程序时，事件注册将推送到Commerce项目。

   将事件提供程序连接到App Builder项目后，订阅`observer.uex_commerce_instance_update`事件并保存更改。

1. 要建立连接，请通过事件提供程序向使用者发送事件。

   - 从本地云项目目录中的命令行，[使用SSH连接到Commerce应用程序服务器](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/secure-connections.html?lang=zh-Hans#connect-to-a-remote-environment)。

     ```bash
     magento-cloud ssh
     ```

   - 通过使用Adobe Commerce CLI检查Admin Unified Experience扩展的状态来发送事件数据。

     ```bash
     bin/magento bin/magento admin:uex:status
     ```

### 测试集成

确认Commerce管理员可以登录Experience Cloud以查看可用的Commerce项目，并访问每个项目的管理员和店面。

1. [使用与CommerceExperience Cloud关联的Adobe ID和组织登录到Instance](https://experiencecloud.adobe.com/library)。

   ![从Experience Cloud主页访问Commerce项目](./assets/admin-uex-home-page.png){width="600" zoomable="yes"}

1. 通过选择&#x200B;**[!UICONTROL Commerce]**&#x200B;查看可用的Commerce项目。

   用于Experience Cloud的![Commerce项目工作区](./assets/admin-uex-commerce-projects-home.png){width="600" zoomable="yes"}

1. 通过选择&#x200B;**[!UICONTROL Open]**&#x200B;打开实例的管理员。

   已启用Experience Cloud集成的![Commerce管理员视图](./assets/admin-dashboard.png){width="600" zoomable="yes"}

1. 验证您是否可以按预期执行管理任务。

   Commerce管理员中的工作流应遵循相同的流程。 如果在启用Experience Cloud集成后遇到工作流更改或错误，请与Commerce系统管理员联系或[提交Adobe支持票证](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html?lang=zh-Hans#submit-ticket)。

配置Experience Cloud集成后，请验证是否正确配置了管理员帐户，以通过Experience Cloud访问Commerce项目。 请参阅[管理管理员用户](/help/getting-started/admin-unified-experience-integration-manage.md#manage-admin-user-accounts)。

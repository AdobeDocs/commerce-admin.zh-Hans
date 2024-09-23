---
title: 设置AEM Assets集成
description: 了解设置Adobe Commerce与AEM Assetsas a Cloud Service之间的集成的要求和步骤。
feature: CMS, Media, Configuration, Integration
source-git-commit: df21ea9a797a4f11d0104cf34134ced3bbabbdf4
workflow-type: tm+mt
source-wordcount: '241'
ht-degree: 0%

---


# 设置AEM Assets集成

通过设置AEM Assets环境并安装和配置适用于Commerce的AEM Assets集成，启用高级资源管理功能。

当集成处于活动状态时，管理员可以使用Experience Manager Assetsas a Cloud Service作为资产创建和管理的单一真实来源，并作为中央数字资产管理工具(DAM)为Commerce项目创建、管理、组织和分发资产。

## 要求

- Adobe Commerce 2.4.5+
   - PHP 8.1、8.2和8.3
   - Composer： 2.x
- Adobe Experience Manager已配置[Adobe Experience Manager Assetsas a Cloud Service](https://experienceleague.adobe.com/zh-hans/docs/experience-manager-cloud-service/content/assets/overview)
- 配置集成的Adobe Commerce用户必须具有对配置了AEM Assets项目的[IMS组织](https://experienceleague.adobe.com/en/docs/core-services/interface/administration/organizations#concept_EA8AEE5B02CF46ACBDAD6A8508646255)的访问权限。

## 设置集成

>[!BEGINSHADEBOX]

**先决条件**

设置AEM Assets集成需要管理权限来自定义应用程序和环境配置。

- 对在其中配置了Cloud Manageras a Cloud Service环境的AEM Assets程序的管理访问权限。
- 对Adobe Commerce环境的管理访问权限，以及检索或生成身份验证所需的API密钥的能力。

>[!ENDSHADEBOX]

启用Commerce与Experience Manager Assets的集成需要三个步骤：

1. [配置您的Experience Manager Assets项目以管理Commerce资源](aem-assets-configure-aem.md)。

1. [安装Experience Manager Assets集成扩展并配置Adobe Commerce](aem-assets-configure-aem.md)。

1. [启用资源同步](aem-assets-setup-synchronization.md)。

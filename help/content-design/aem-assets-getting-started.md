---
title: 为Commerce设置AEM Assets集成
description: 了解如何使用您的 [!DNL Commerce] 实例载入Experience Manager Assets，以访问要在您的商店中使用的无数媒体资源。
feature: CMS, Media, Configuration
source-git-commit: c109edc9d9277baafd61da1df0f1917f07089353
workflow-type: tm+mt
source-wordcount: '256'
ht-degree: 0%

---

# 为Commerce设置AEM Assets集成

设置AEM Assets集成需要管理权限来自定义应用程序和环境配置。

- 对配置Cloud Manager as a Cloud Service环境的AEM Assets程序的管理访问权限。

- 对Adobe Commerce环境的管理访问权限，以及检索或生成身份验证所需的API密钥的能力。

## 使用该集成的要求

要利用此集成，企业必须满足以下要求：

- Adobe Commerce、AEM Assets和[AEM Dynamic Media](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/assets/dynamic/administering-dynamic-media)的活动许可证。

- Adobe Commerce 2.4.5+

   - PHP 8.1、8.2和8.3
   - Composer： 2.x

- Adobe Experience Manager已配置[Adobe Experience Manager Assets as a Cloud Service](https://experienceleague.adobe.com/zh-hans/docs/experience-manager-cloud-service/content/assets/overview)

- 配置集成的Adobe Commerce用户必须具有对配置了AEM Assets项目的[IMS组织](https://experienceleague.adobe.com/en/docs/core-services/interface/administration/organizations#concept_EA8AEE5B02CF46ACBDAD6A8508646255)的访问权限。

## 主要优势

- **无额外费用** — 此集成免费提供给符合授权要求的商家。

- **官方Adobe解决方案** — 由Adobe开发、维护和完全支持，确保稳定性并与未来的平台增强功能保持一致。

- **Adobe托管支持模型** — 协助和故障排除直接由Adobe处理，可让您高枕无忧并简化问题解决。

## 后续步骤

启用Commerce与Experience Manager Assets的集成需要三个步骤：

1. [配置您的AEM资源项目以管理Adobe Commerce资源](aem-assets-configure-aem.md)。

1. [安装AEM资产集成扩展并配置Adobe Commerce](aem-assets-configure-aem.md)。

1. [启用资源同步](aem-assets-setup-synchronization.md)。

---
title: 适用于Commerce的Experience Manager Assets集成
description: 了解如何将Experience Manager Assets与您的 [!DNL Commerce] 实例集成，以访问要在您的商店中使用的无数媒体资源。
feature: CMS, Media, Configuration, Integration
source-git-commit: d91ba86b77ef91e849d1737628b575f2309376b8
workflow-type: tm+mt
source-wordcount: '432'
ht-degree: 0%

---

# 适用于Commerce的Experience Manager Assets集成

{{$include /help/_includes/aem-assets-integration-beta-note.md}}

Commerce与Adobe Experience Manager (AEM) Assets之间的集成将AEM as a Digital Asset Management (DAM)系统的强大功能与Adobe Commerce整合在一起，以增强电子商务体验。 此集成利用AEM强大的资产管理功能，提供无缝、可扩展且高效的方式来跨商业商店管理和交付资产。

**主要功能**

- **集中式资产管理**

   - **AEM Assets as a Single Source of Truth**-AEM Assets用作所有数字资产的中央存储库，确保所有电子商务平台都有权访问品牌上批准的资产。

   - **批量资产管理** — 借助AEM强大的资产管理功能，组织可以高效地管理大量资产。 这使营销人员和商家能够有效地为新产品线映射大量图像。

- **个性化的Commerce体验** — 在AEM中使用GenAI服务，组织可以为个性化电子商务体验生成数百万种产品变体。 营销人员和商家可以使用这些图像为产品发布和季节性活动创建动态店面，从而增强参与度并提高转化率。

- **自动资源匹配** — 该集成包括规则引擎服务，该服务基于SKU或其他关键属性自动将AEM中的资源与Adobe Commerce中的产品匹配。 该服务可确保最新的产品资产和变体始终在电子商务商店中可用。 它还减少了管理资产所需的手动工作，为更具战略意义的活动腾出了时间。

- **简化的流程**
   - **从Commerce启用并配置集成** — 管理员和开发人员可以使用熟悉的工具和流程从Adobe Commerce安装和配置集成。
   - **动态更新** — 使用资产管理系统中的最新更改保持产品图像最新。 这些自动更新可确保Commerce店面始终具有最新的产品信息。
   - **高效的目录管理** — 通过自动清理和刷新资产简化了产品目录的维护。

## 集成Commerce和Experience Manager Assets

>[!BEGINSHADEBOX]

**先决条件**

- 必须将Adobe Commerce配置为具有分配的组织ID的[Commerce管理员与Adobe ID](/help/getting-started/adobe-ims-config.md)的集成。
- 必须将Experience Manager Assets作为产品分配给相同的组织ID。
- 配置集成的用户必须在同一组织中拥有一个帐户，该帐户具有访问Adobe Commerce和Experience Manager Assets的管理权限。

>[!ENDSHADEBOX]

通过完成以下任务启用Commerce与Experience Manager Assets的集成：

1. [配置您的Experience Manager Assets项目以管理Commerce资源](aem-assets-configure-aem.md)

1. [安装Experience Manager Assets集成扩展并配置Adobe Commerce](aem-assets-configure-commerce.md)

1. [启用资源同步](aem-assets-setup-synchronization.md)

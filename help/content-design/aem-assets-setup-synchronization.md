---
title: 启用资源同步
description: 了解如何连接Adobe Commerce和Experience Manager Assets项目，以启用这两个系统之间的资源同步。
feature: CMS, Media
exl-id: cc3ae56b-f1c8-4c96-a284-bcd726ce2bab
source-git-commit: 508e9e1d23a4b6e70ada22e2a22c0dcd401393a9
workflow-type: tm+mt
source-wordcount: '417'
ht-degree: 0%

---

# 启用资源同步

>[!BEGINSHADEBOX]

**先决条件**

- [配置AEM Experience Manager Assets以管理Commerce资源](#aem-assets-configure-aem)
- [安装并配置Commerce的AEM Assets集成](#aem-assets-configure-commerce.md)以添加该扩展并生成使用该扩展所需的凭据和连接。

>[!ENDSHADEBOX]

在此启用过程中，您可以通过提供AEM创作环境的项目和环境ID来注册租户ID。 这些ID可标识您正在连接到的AEM Assets项目，并提供凭据以启用Commerce和AEM Assets之间的通信和工作流。

识别AEM assets项目后，您可以选择用于在Adobe Commerce和AEM Assets之间同步资源的匹配规则。

适用于Commerce的AEM Assets集成支持两个匹配规则，用于在Adobe Commerce和AEM Assets之间同步资产。

- **按产品SKU匹配** — 这是根据产品的库存单位(SKU)匹配资产的默认匹配规则。 SKU是每个产品的唯一标识符。 此规则将资源元数据中的SKU与Commerce产品SKU相匹配，以确保将资源与正确的产品相关联。

- **自定义匹配** — 此匹配规则适用于需要自定义匹配逻辑的更复杂方案或特定业务要求。 要使用此规则，您必须在Adobe Developer App Builder中实施自定义代码以定义如何将资源与产品匹配。 更多详细信息即将推出……

对于初始载入，使用默认`Match by product sku`规则。 如果需要，您可以稍后更改匹配规则。

## 启用集成

1. 获取[AEM Assets创作环境](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/authoring/quick-start)的项目和环境ID。

   1. 打开AEM Sites控制台，然后选择&#x200B;**[!UICONTROL Assets]**。

   1. 从URL：<br>`https://author-p[Program ID]-e[EnvironmentID].adobeaemcloud.com/`|复制并保存项目和环境ID

1. 从Commerce管理员中，打开AEM Assets集成配置。

   1. 选择&#x200B;**[!UICONTROL Store]** >配置> **[!UICONTROL CATALOG]** > **[!UICONTROL Catalog]**。

   1. 展开&#x200B;**[!UICONTROL Experience Manager Assets integration]**。

      ![AEM Assets集成启用该集成](assets/aem-assets-integration-enable-config.png){width="600" zoomable="yes"}

1. 通过输入&#x200B;**[!UICONTROL Program ID]**&#x200B;和&#x200B;**[!UICONTROL Environment ID]**&#x200B;标识要连接到的Experience Manager Assets项目。

1. 添加OAUTH凭据以通过选择&#x200B;**[[!UICONTROL Commerce integration]](aem-assets-configure-commerce.md#add-the-integration-to-the-commerce-environment)**&#x200B;来验证Adobe Commerce和ARES服务之间的API请求，例如`Assets integration`。

1. 通过将&#x200B;**[!UICONTROL Enable integration]**&#x200B;设置为`Yes`，允许Commerce接受来自AEM Assets的传入更新。

   启用集成后，您可以配置资产匹配规则。

   ![AEM Assets集成选择资源匹配规则](assets/aem-assets-config-matching-rule.png){width="600" zoomable="yes"}

1. 为资产同步定义匹配规则。

   1. 选择&#x200B;**[!UICONTROL Match by product SKU]**。

   1. 添加在&#x200B;**[!UICONTROL Match by product SKU attribute name]**&#x200B;字段`commerce:skus`中为AEM Assets产品SKU定义的[Commerce元数据字段名称](aem-assets-configure-aem.md#configure-metadata)。

1. 通过选择&#x200B;**[!UICONTROL Save Config]**&#x200B;应用配置并启动同步过程。

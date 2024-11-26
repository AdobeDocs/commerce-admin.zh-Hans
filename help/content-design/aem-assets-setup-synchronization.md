---
title: 启用资源同步
description: 了解如何连接Adobe Commerce和Experience Manager Assets项目，以启用这两个系统之间的资源同步。
feature: CMS, Media
exl-id: cc3ae56b-f1c8-4c96-a284-bcd726ce2bab
source-git-commit: e069f0a99ed9289b22cafe06fe2f787912cbba23
workflow-type: tm+mt
source-wordcount: '356'
ht-degree: 0%

---

# 启用资源同步

在启用过程中，您将使用项目的项目和环境ID为AEM创作环境注册租户ID。 这些ID可标识您正在连接到的AEM Assets项目，并提供凭据以启用Commerce和AEM Assets环境之间的通信。

识别AEM assets项目后，您可以选择匹配规则以在Adobe Commerce和AEM Assets之间同步资源。

- **[!UICONTROL Match by product SKU]** — 将资源元数据中的SKU与[Commerce产品SKU](https://experienceleague.adobe.com/en/docs/commerce-operations/operational-playbook/glossary#sku)匹配的默认规则，以确保资源与正确的产品关联。

- **[!UICONTROL Custom match]** — 匹配规则，用于需要自定义匹配逻辑的更复杂方案或特定业务要求。 实施自定义匹配需要在Adobe Developer App Builder中开发自定义代码以定义资源与产品的匹配方式。 更多详细信息即将推出……

对于初始载入，使用默认的&#x200B;*按产品SKU匹配*&#x200B;规则。

## 先决条件

- [配置AEM Experience Manager Assets以管理Commerce资源](#aem-assets-configure-aem)
- [安装并配置Commerce的AEM Assets集成](#aem-assets-configure-commerce.md)以添加该扩展并生成使用该扩展所需的凭据和连接。

## 配置连接

1. 获取[AEM Assets创作环境](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/authoring/quick-start)项目和环境ID。

   1. 打开AEM Sites控制台并选择&#x200B;**[!UICONTROL Assets]**。

   1. 从URL：<br>`https://author-p[Program ID]-e[EnvironmentID].adobeaemcloud.com/`|复制并保存项目和环境ID

1. 从Commerce管理员中，打开AEM Assets集成配置。

   1. 转到&#x200B;**[!UICONTROL Store]** >配置> **[!UICONTROL ADOBE SERVICES]** > **[!UICONTROL AEM Assets Integration]**。

      ![AEM Assets集成启用该集成](assets/aem-assets-integration-enable-config.png){width="600" zoomable="yes"}

1. 进入AEM Assets环境&#x200B;**[!UICONTROL Program ID]**&#x200B;和&#x200B;**[!UICONTROL Environment ID]**。

1. 输入**[!UICONTROL Asset Selector IMS Client ID]。

   [IMS ID](../getting-started/adobe-ims-config.md)允许您将AEM Assets与页面生成器集成。

1. 选择[[!UICONTROL Commerce integration]](aem-assets-configure-commerce.md#add-the-integration-to-the-commerce-environment)**以在Commerce和资源匹配服务之间验证请求。

1. 通过将&#x200B;**[!UICONTROL Integration enabled]**&#x200B;设置为`Yes`，允许Commerce接受来自AEM Assets的传入更新。

   启用集成后，配置资产匹配规则。

   ![AEM Assets集成选择资源匹配规则](assets/aem-assets-config-matching-rule.png){width="600" zoomable="yes"}

1. 为资产同步定义匹配规则。

   1. 选择&#x200B;**[!UICONTROL Match by product SKU]**。

   1. 添加在&#x200B;**[!UICONTROL Match by product SKU attribute name]**&#x200B;字段`commerce:skus`中为AEM Assets产品SKU定义的[Commerce元数据字段名称](aem-assets-configure-aem.md#configure-metadata)。

   ![AEM Assets集成选择资源匹配规则](assets/aem-assets-config-matching-rule.png){width="600" zoomable="yes"}

1. 选择&#x200B;**[!UICONTROL Save Config]**&#x200B;以应用更新并启动资产同步

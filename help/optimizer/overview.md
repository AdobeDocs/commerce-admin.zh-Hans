---
title: Merchanding Services概述
description: 了解为Adobe Commerce as a Cloud Service实例配置了CCDM的目录配置、推销、报告和监控工具。
recommendations: noCatalog
badgeSaas: label="仅限SaaS" type="Positive" url="https://experienceleague.adobe.com/zh-hans/docs/commerce/user-guides/product-solutions" tooltip="仅适用于使用CCDM设置的Adobe Commerce as a Cloud Service实例（Adobe管理的SaaS基础架构）。"
exl-id: f9516d4c-fbae-4db2-a1a9-cda3684a8122
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
  - id: de2e2e68-c5d7-4efe-be7b-27528698f06b
    internal-label: Commerce as a Cloud Service
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: a6a5a899ba60097bd6baf2a5de14063a0af2f313
workflow-type: tm+mt
source-wordcount: '710'
ht-degree: 0%
---
# 带有CCDM的促销服务概述

使用可组合目录数据模型(CCDM)设置的Adobe Commerce as a Cloud Service实例在Adobe Unified Experience的[Commerce Admin中提供目录配置、推销、报告和监视工具。](../getting-started/admin-unified-experience.md) CCDM就是支持Adobe Commerce Optimizer的同一个目录基础。

借助Merchandising Services，您可以：

- 使用您的Adobe Commerce as a Cloud Service实例中的目录数据来支持店面体验。
- 配置目录视图和策略以定义店面产品分类。
- 跨所有目录视图应用促销规则或针对特定视图对其进行定制。
- 配置产品推荐、搜索Facet和同义词。
- 通过成功量度和搜索绩效报告审查店面绩效。
- 监视目录同步和捕获的店面事件。

Commerce Foundation仍然是产品和价格的真实来源，并继续管理购物车、结账和其他事务操作。

## 快速导览

>[!BEGINTABS]

>[!TAB 目录配置]

配置可用于店面的目录上下文。

- **目录视图** — 组合目录源、策略和价格手册以定义店面可以检索的产品和定价。 查看[目录视图](./setup/catalog-view.md)。
- **目录层** — 覆盖所选的产品属性而不更改源数据。 将AEM Assets用于产品图像时，AEM-Assets层通过产品可视化图表应用。 查看[目录层](./setup/catalog-layer.md)。
- **专用目录视图** — 启用目录保护在检索目录视图的数据时需要有效的签名令牌。 查看[专用目录视图](./setup/private-catalog-view.md)。

>[!TAB 策略]

策略根据产品属性过滤通过目录视图提供的产品。 例如，策略可以将分类限制为特定品牌或产品类别。

策略确定可用的产品分类。 它们不会取代“目录保护”，后者控制对专用目录视图的访问。

>[!TAB 促销]

配置购物者如何发现产品以及如何在可用分类中促销产品。

- **机会** — 审查产品性能、购物者行为和搜索趋势，以确定促销改进领域。
- **推荐** — 在Commerce管理中创建和管理推荐单位。 推荐使用目录数据和汇总购物者行为来建议相关产品，例如“查看了此产品的客户也查看了此产品”。
- **促销规则** — 控制产品促销和排名方式。 规则可以应用于所有目录视图或针对特定视图进行定制。 请参阅[创建促销规则](https://experienceleague.adobe.com/zh-hans/docs/commerce/optimizer/merchandising/rules/add#create-a-rule)。
- **彩块化** — 配置购物者用于按品牌、大小或价格等属性缩小产品结果的过滤器。
- **同义词** — 关联等效的搜索词以帮助购物者查找使用相同概念的不同单词的产品。
- **设置** — 配置搜索和促销选项，包括价格彩块化、语言和高级搜索。

策略确定哪些产品可通过目录视图使用。 促销规则控制该分类中产品的促销和排名方式。

有关如何匹配和排名搜索结果的详细信息，请参阅[搜索匹配和排名](./manage-results/search-relevance-matching.md)。

>[!TAB 报告]

使用报告审查店面活动并告知促销决策。

- **成功量度** — 根据店面活动查看收入、转化、参与、客户获取和跳出率。
- **搜索性能** — 查看购物者使用的搜索词及其性能，以识别优化产品发现的区域。

报告取决于实施收集的店面活动数据。

>[!TAB 系统配置]

监控目录同步和Storefront事件收集，以调查数据可用性和实施问题。

- **目录同步** — 查看从Commerce Foundation传输的目录数据的同步状态。
- **事件** — 查看产品发现、建议和报告所使用的捕获的店面事件。 使用“事件”页可帮助验证行为数据收集并调查缺失或意外事件。

>[!ENDTABS]
<!--
Watch the following video for a high-level overview of [!DNL Adobe Commerce Optimizer]:

>[!VIDEO](https://video.tv.adobe.com/v/3450226)
-->

## 确认实例使用CCDM

1. 通过Unified Shell登录到Commerce管理员，然后选择预期的Adobe Commerce as a Cloud Service实例。
1. 确认CCDM促销页面（如目录视图和策略）在实例导航中可用。
1. 如果这些页面不可用，请确认您选择了正确的实例并且正在使用Unified Shell。

   联系Adobe支持或Commerce配置团队以验证实例的CCDM配置状态。

实例的“就绪”状态表示已配置实例，但本身并不确认它使用CCDM。


---
title: 按角色列出的目录促销任务
description: 查找面向使用配置了CCDM的Adobe Commerce as a Cloud Service实例的管理员、开发人员和销售人员的任务指南。
role: Admin, Developer
recommendations: noCatalog
badgeSaas: label="仅限SaaS" type="Positive" url="https://experienceleague.adobe.com/zh-hans/docs/commerce/user-guides/product-solutions" tooltip="仅适用于使用CCDM设置的Adobe Commerce as a Cloud Service实例（Adobe管理的SaaS基础架构）。"
TQID: 'https://experienceleague.adobe.com/0PmobUkdEWspxuRSaIPL8vS1ojDDZ3gw-L-3SfPmJAg'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
  - id: de2e2e68-c5d7-4efe-be7b-27528698f06b
    internal-label: Commerce as a Cloud Service
feature_v2:
  - id: cc04bd17-78d5-5120-8c3d-1b8a57e49280
    internal-label: Integration
  - id: dec06508-d41f-555a-87e8-29e8bcdfa95a
    internal-label: Recommendations
  - id: e8818fe6-9c8b-4bc0-9ef8-377a10b7bc75
    internal-label: Architecture
  - id: f37757d8-3174-5335-b977-1161792f965d
    internal-label: Personalization
subfeature_v2:
  - id: f8ddfd3b-6194-46e8-a176-0e918039be56
    internal-label: Cloud architecture
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: dba482e5-29a8-4127-afa2-c4b913512ef8
    internal-label: Data and analytics
  - id: df401a2a-327d-468c-a5e4-b7b7ccd071a0
    internal-label: Data integration
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
source-git-commit: 742236e7fdb26c56a80f66a44b0a4960210f4dac
workflow-type: tm+mt
source-wordcount: '548'
ht-degree: 0%
---

# 按角色分类促销任务

使用本任务参考查找有关在Adobe Commerce as a Cloud Service实例中配置目录数据、集成店面、管理促销和审查性能的指导，这些实例使用可组合目录数据模型(CCDM)进行设置。

责任因实施而异。 以下部分按通常执行任务的角色对任务进行分组。

- 管理员在Commerce Foundation中管理产品、价格和B2B配置。
- 开发人员配置店面集成并验证目录请求和行为数据收集。
- 促销人员可以配置产品发现和推荐，并使用报告为促销决策提供信息。

通过本机Adobe Commerce as a Cloud Service集成，产品和价格数据同步到CCDM。 无需单独的连接器安装或App Builder应用程序。

## 准备目录和店面

完成适用于您的实施的任务。 可以手动创建B2C目录视图。 B2B目录视图、策略和价格手册是根据Commerce Foundation中的B2B配置生成的。

| 任务 | 描述 | 资源 |
| --- | --- | --- |
| **配置产品和价格** | 在Commerce Foundation中管理产品和价格。 定价数据将作为价格手册同步到CCDM；请勿在CCDM中单独制定价格。 | [产品列表](../catalog/products-list.md)、[创建产品](../catalog/product-create.md)、[价格范围](../catalog/catalog-price-scope.md)和[高级定价](../catalog/pricing-advanced.md) |
| **配置商店视图** | 在Commerce Foundation中配置店面所需的店面视图和本地化产品数据。 | [存储视图](../stores-purchase/store-views.md) |
| **设置B2B共享目录和公司** | 对于B2B实施，请先在Commerce Foundation中配置共享目录和公司关系，然后再查看生成的目录配置。 | [共享目录](../b2b/catalog-shared.md)和[公司](../b2b/account-companies.md) |
| **配置B2C目录查看和策略** | 创建目录视图并选择定义可用产品分类的策略。 将适用的同步价格帐簿与每个视图关联。 | [目录视图](./setup/catalog-view.md) |
| **查看B2B目录视图** | 确认本机同步已生成预期的目录视图、策略和价格手册。 在Commerce Foundation中管理底层B2B配置，而不是手动创建重复结构。 | [B2B目录视图](./setup/catalog-view.md#b2b-catalog-views) |
| **配置店面** | 配置店面以请求所需的目录上下文。 对于自定义或其他店面集成，请查看适用的目录请求标头。 | [店面配置](https://experienceleague.adobe.com/en/tools/commerce-storefront/setup/configuration/commerce-configuration/) |

在配置促销之前，请确认店面返回预期的产品和价格。 测试添加到购物车、购物车和结账功能，验证交易定价是否与预期的Commerce Foundation配置匹配。

## 配置促销和审查性能

| 任务 | 描述 | 资源 |
| --- | --- | --- |
| **配置产品发现** | 设置促销规则、彩块化和同义词。 规则可以应用于所有目录视图或针对特定视图进行定制。 | [促销概述](./merchandising/overview.md) |
| **查看搜索设置** | 查看您的实施的搜索配置和可用的语义搜索选项。 | [促销设置](./settings.md)和[语义搜索](./setup/semantic-search.md) |
| **配置推荐** | 创建推荐单元并验证店面是否收集实施所需的行为数据。 | [推荐概述](./merchandising/recommendations/overview.md) |
| **审核绩效** | 使用成功量度和搜索绩效报告来评估店面活动并告知促销决策。 | [成功量度](./manage-results/success-metrics.md)和[搜索性能](./manage-results/search-performance.md) |

## 后续步骤

在配置推销和审查绩效后，继续根据需要监控和调整您的规则、彩块化和推荐，以优化店面体验。

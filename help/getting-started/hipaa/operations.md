---
title: 操作
description: 迁移到适用于HIPAA的产品并使用辅助暂存环境进行故障排除的指南。
exl-id: 058b43de-1cee-4557-b2e3-87ee7422bf9b
badgePaas: label="仅限PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="仅适用于云项目(Adobe管理的PaaS基础架构)和内部部署项目上的Adobe Commerce 。"
source-git-commit: 77e7eb00e9f8d5af6361059c287707993180c4c4
workflow-type: tm+mt
source-wordcount: '528'
ht-degree: 0%

---

# 操作

使用这些指南了解如何迁移到Adobe Commerce的HIPAA就绪服务以及使用`staging_for_support`环境进行故障排除。

## 迁移

从非HIPAA Commerce产品迁移到为HIPAA做好准备的产品时，客户必须遵循以下准则：

1. **删除现有的数据空间**：在迁移之前，必须删除所有现有的数据空间，以防止敏感数据和非敏感数据在Adobe Commerce SaaS层中共存。 创建支持票证以删除数据空间。
1. **配置新环境**：只有在删除数据空间之后，才应配置新HIPAA Commerce实例中的[Commerce Services Connector](https://experienceleague.adobe.com/en/docs/commerce/user-guides/integration-services/saas)安装程序。 只有在删除旧的数据空间后，才应使用新的HIPAA SaaS环境。 Commerce服务连接器的设置会自动触发创建新的SaaS数据空间。
1. **迁移策略**：删除SaaS数据空间是一个不可逆的过程，将删除您的所有目录数据和相关配置。 如果您想要结转任何旧数据或配置，则必须实施迁移策略。 这一战略是商人的责任。 只有在完成迁移数据备份（如果适用）后，才应创建用于删除现有数据空间的支持票证。

>[!NOTE]
>要删除现有数据空间，客户必须创建一个名为“HIPAA迁移：删除SaaS数据空间”的Adobe Commerce支持票证，提供其`MAGEID`，并提供需要删除的SaaS项目ID。

## Adobe Commerce支持疑难解答

Adobe Commerce HIPAA就绪产品附带一个额外的`staging_for_support`环境，供Adobe Commerce支持团队用于故障排除目的。

客户必须确保`staging_for_support`环境：

- 不包含任何敏感数据，如但不限于受保护的健康信息(PHI)。
- 不得用于任何生产活动。
- 不能为`staging_for_support`指定不同的名称，以避免混淆。
- 使用生产环境中的代码和配置保持最新，以确保在尽可能接近生产的环境中执行故障排除。

## Commerce服务

- **不符合HIPAA要求的Commerce服务** — 客户不得使用Adobe Commerce服务，例如实时搜索、产品推荐、支付服务、Sales Channels或Commerce Intelligence，因为它们不符合HIPAA要求。 客户应仅使用[支持HIPAA的服务](overview.md)。

- **数据连接** — 只有[数据连接](https://experienceleague.adobe.com/en/docs/commerce/data-connection/overview)扩展中的后台收集器符合HIPAA要求。 客户不应将PHI发送到不符合HIPAA要求的数据连接服务，例如店面活动和Audience Activation。 客户必须确保禁用店面数据收集。

- **目录服务** — 根据设计，[目录服务](https://experienceleague.adobe.com/en/docs/commerce/catalog-service/overview)不处理PHI，因此它超出了HIPAA就绪性审核和合规性的范围。 客户有责任确保他们根据自己对用例的评估并在咨询法律顾问的情况下使用此服务。 客户还不应通过联合服务使用目录服务，以避免将PHI传递到不符合HIPAA要求的服务的风险。

- **SaaS数据导出** — 应将[SaaS数据导出](https://experienceleague.adobe.com/en/docs/commerce/saas-data-export/overview)服务配置为仅发送Adobe Commerce中支持HIPAA的组件的数据。

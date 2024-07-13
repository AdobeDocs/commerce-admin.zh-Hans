---
title: 'Inventory management指南 [!DNL Inventory Management] 指南'
description: 有关Adobe Commerce和Magento Open Source管理员的 [!DNL Inventory Management] 的全面信息，包括迁移和配置。
seo-title: Adobe Commerce Inventory Management Guide
seo-description: Describes how to use the [!DNL Inventory Management] module in Adobe Commerce or Magento Open Source.
exl-id: 8013bc13-b057-4ad7-bbed-ee00c2f6e4eb
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 0%

---

# [!DNL Inventory Management]指南概述

本指南适用于Adobe Commerce和Magento Open Source的管理员。 它提供了有关启用此模块的详细信息，包括其功能的配置和管理。 它假定您对核心[!DNL Commerce]配置和功能有基本的了解。

[!DNL Inventory Management]有两个管理员区域：

- 管理员：使用此区域可访问配置UI和报表。
- 命令行界面：使用此工具执行安装和后端配置任务。

本指南涵盖：

| 主题 | 描述 |
| ------- | ----------- |
| [简介](introduction.md) | [!DNL Inventory Management]功能概述，您可以使用这些功能管理多个位置的库存，以便您的Commerce商店准确反映实际盘点。 |
| [发行说明](release-notes.md) | 查看发行说明以了解有关所有[!DNL Inventory Management]版本的信息。 |
| 清单基础知识 | 了解有关管理库存的基础知识：[库存和来源](sources-stocks.md)、[来源选择和预留](selection-reservations.md)、[订单和预留状态](order-status.md)以及[产品类型](product-types.md) |
| 快速入门 | 了解[!DNL Inventory Management]模块以及它如何适合您的Commerce实例和商店操作： [Commerce升级](migrate.md)、[模块安装和更新](install-update.md)、[商家源类型](merchant-sourcing.md)和[源结构更改](expand-restructure.md) |
| [配置](configuration.md) | 了解[!DNL Inventory Management]选项的配置，这些选项决定源可用性、店面产品和订单装运。 |
| [管理源](sources-manage.md) | 了解来源以及它们如何定义管理和发运产品库存以进行订单履行或提供服务的物理位置。 |
| [管理库存](stocks-manage.md) | 了解如何使用库存表示销售渠道来源的虚拟汇总产品库存。 |
| [管理数量](quantities-manage.md) | 了解如何为新产品分配来源和数量或更改现有产品。 |
| [管理订单和装运](shipments.md) | 了解用于通过装运流程管理库存数量的其他[!DNL Inventory Management]功能和选项。 |
| [CLI引用](cli.md) | 了解[!DNL Inventory Management]模块提供的用于管理清单数据和配置设置的命令。 |

{style="table-layout:auto"}

## 开发人员信息

有关模块体系结构、API和算法自定义的详细信息，请参阅开发人员文档中的[[!DNL Inventory Management]](https://developer.adobe.com/commerce/webapi/rest/inventory/)。

## Commerce文档

{{docs-links}}

## 故障排除和支持

如果您需要本指南中未涉及的信息或问题，请使用以下资源：

- [大量预订不一致](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-8/mdva-30112-magento-patch-large-number-reservation-inconsistencies.html)
- [库存不一致问题](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-14/mdva-33281-magento-patch-inventory-inconsistency-issues.html)
- [未删除的样本清单达到“0”](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-17/mdva-34850-swatches-not-strike-through-inventory-reaches-0.html)
- 安装清单后[库存状态不正确](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/stock-status-incorrect-after-magento-inventory-install.html)
- [支持票证](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html#submit-ticket) — 提交票证以接收其他帮助。

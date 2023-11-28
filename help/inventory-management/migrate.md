---
title: ’[!DNL Commerce] 升级
description: 了解Adobe Commerce和Magento Open Source升级如何影响目录和 [!DNL Inventory Management] 配置。
exl-id: ba640b91-0f29-46df-bfd9-1c43433a751f
feature: Inventory, Upgrade
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '721'
ht-degree: 0%

---

# [!DNL Commerce] 升级

如果您在以前的版本中使用了单一来源清单，此信息将提供有关现有目录和清单配置的新增功能和更改的详细信息。

[!DNL Inventory Management] Adobe Commerce和Magento Open Source包括的功能、增强功能和开发人员支持，可增强和更新所有产品库存管理并添加新功能。 所有功能均开箱即用，包括来源选择算法和并发结帐，以将订货量与来源和订单履行相匹配。 根据您的网站、商店和商家类型，您可以创建额外的库存和来源，分配库存数量等。 有关完整信息，请参阅 [Inventory management](introduction.md).

安装Magento Open Source2.4.x或Adobe Commerce 2.4.x时，会发生以下初始更改：

- [Inventory management](enable.md) 在全局商店或产品级别启用。 “管理库存”选项可以启用或禁用对库存数量的跟踪、对汇总的可销售数量的计算，以及用于跟踪从采购到发票和发运的预留管理。 您可以禁用此选项，以使用ERP和其他第三方服务来管理库存、订单和发运。 有关其他信息，请参阅 [!DNL Inventory Management] 模块如下所示。

- A [默认源](sources-manage.md) 和 [默认库存](stocks-manage.md) 将添加到系统。 请勿禁用或删除这些默认值。 [!DNL Commerce] 将现有和新导入的产品分配给这些默认值。

  >[!IMPORTANT]
  >
  >强烈建议不要使用“默认库存”和“默认来源”，因为它们是 `CatalogInventory` 模块，该模块现已弃用。 建议您改为创建和使用自定义库存和来源。

   - 库存提供汇总、虚拟的可销售数量，并带有保留以跟踪购物车和订单，确保并发结帐。

   - 您的目录中的所有现有产品都会分配到“默认来源”。 在添加新源之前，产品界面不会发生更改。 如果您只从一个位置发运产品，则不存在其它来源差异。 您可以创建自定义 [源](sources-add.md) 和 [分配数量](quantities-manage.md) 每个装运地点。

   - 您可以将源配置为取车地点和 [分配数量](quantities-manage.md) 为那个源头着想。

   - 您的网站将分配给默认库存。 您可以创建自定义 [库存](stocks-add.md) 连接销售渠道（网站）和来源（位置）。

- 其他 [配置选项](configuration.md) 将添加到您的产品和全局商店。 一些现有配置选项会收到更新的选项和行为：

   - 通知以下数量将发送通知并从可销售数量中扣除。

   - 缺货阈值支持正金额、零金额和负金额。 启用延交订单后，正金额将被忽略，视为零（或无限）。

   - 延交订单支持零（无限）和负金额。 启用时，以下通知数量不会从可销售数量中扣除。

- 新保留跟踪潜在销售额，在订单发运时转换为数量扣减额。 您从不直接访问或创建预留。 [!DNL Commerce] 通过订单、发运和贷项通知单在后台创建和管理预订。

- [订单和发运](shipments.md) 包括使用来源选择算法来建议发运的新功能，并支持来自多个来源的部分发运以履行订单。

- 新建 [导入/导出特征](inventory-import-export.md) 允许您为目录中的所有SKU成批添加来源、更新库存数量以及设置库存状态（缺货）。 这些功能允许您修改一个、选定或所有源。

- 通过Product Grid页面新增的批量选项支持批量 [分配和取消分配源](bulk-assignment.md)、和 [将库存转移到来源](inventory-transfer.md).

- [!DNL Inventory Management] 支持B2B目录。 当前，所有B2B产品都必须分配给“默认来源”和“默认库存”。

## [!DNL Commerce Order Management] 和 [!DNL Inventory Management]

[Commerce Order Management (MCOM)][1] 与不兼容 [!DNL Inventory Management]. 安装后，MCOM模块提供所有清单管理功能 [!DNL Commerce]，包括单一来源和多来源管理、库存、预订等。 此 [!DNL Inventory Management] 模块默认处于禁用状态。

MCOM为高级全渠道订单管理、全球库存和多源、从商店到仓库的履行以及集中化客户服务提供了广泛的功能和服务。 有关完整的功能列表，请参见 [MCOM功能列表][2].

[!DNL Inventory Management] 扩展现有 [!DNL Commerce] 功能中增加了用于跟踪在制品订单、现有库存、库存可用库存以及用于扩展开发的API的选项。

## [!DNL Inventory Management] 模块

您可能希望禁用 [!DNL Inventory Management] 模块至：

- 加快当前位于Adobe Commerce或Magento Open Source2.0/2.1/2.2/2.3上的商户的升级并迁移到2.4.x。

- 使用自定义或第三方库存和订单管理模块。

- 使用 [!DNL Order Management System] 用于库存管理。 当前连接器不支持 [!DNL Inventory Management] 界面。 对于升级到Adobe Commerce 2.4.0的OMS商户，必须禁用这些模块。

有关完整的详细信息，请参阅 [安装和更新](install-update.md).

[1]: https://omsdocs.magento.com/
[2]: https://omsdocs.magento.com/en/getting-started/feature-list/

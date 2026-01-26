---
title: '[!DNL Commerce]升级'
description: 了解Adobe Commerce和Magento Open Source升级如何影响目录和 [!DNL Inventory Management] 配置。
exl-id: ba640b91-0f29-46df-bfd9-1c43433a751f
feature: Inventory, Upgrade
source-git-commit: cace9d1de00955494d8bc607c017778ff7df4806
workflow-type: tm+mt
source-wordcount: '720'
ht-degree: 0%

---

# [!DNL Commerce]升级

如果您在以前的版本中使用了单一来源清单，此信息将提供有关现有目录和清单配置的新增功能和更改的详细信息。

适用于Adobe Commerce和Magento Open Source的[!DNL Inventory Management]包括增强和更新所有产品库存管理和添加新功能的功能、增强功能和开发人员支持。 所有功能均开箱即用，包括“Source选择算法”和“并发结账”，以将订货量匹配到来源和订单履行。 根据您的网站、商店和商家类型，您可以创建额外的库存和来源，分配库存数量等。 有关完整信息，请参阅[Inventory management](introduction.md)。

安装Magento Open Source 2.4.x或Adobe Commerce 2.4.x时，会发生以下初始更改：

- 在全局商店或产品级别启用[Inventory management](enable.md)。 “管理库存”选项可以启用或禁用对库存数量的跟踪、对汇总的可销售数量的计算，以及用于跟踪从采购到发票和发运的预留管理。 您可以禁用此选项，以使用ERP和其他第三方服务来管理库存、订单和发运。 有关其他信息，请参阅下面的[!DNL Inventory Management]模块。

- 将[默认Source](sources-manage.md)和[默认Stock](stocks-manage.md)添加到系统中。 请勿禁用或删除这些默认值。 [!DNL Commerce]将现有和新导入的产品分配给这些默认值。

  >[!IMPORTANT]
  >
  >强烈建议不要使用默认Stock和默认Source，因为它们是`CatalogInventory`模块的一部分，该模块现已弃用。 建议您改为创建和使用自定义库存和来源。

   - 库存提供汇总、虚拟的可销售数量，并带有保留以跟踪购物车和订单，确保并发结帐。

   - 您的目录中的所有现有产品都会分配给默认Source。 在添加新源之前，产品界面不会发生更改。 如果您只从一个位置发运产品，则不存在其它来源差异。 您可以为每个装运位置创建自定义[源](sources-add.md)和[分配数量](quantities-manage.md)。

   - 您可以将来源配置为取车地点，并为该来源[分配数量](quantities-manage.md)。

   - 您的网站将分配给默认库存。 您可以创建自定义[库存](stocks-add.md)以连接销售渠道（网站）和来源（位置）。

- 其他[配置选项](configuration.md)添加到您的产品和全局存储。 一些现有配置选项会收到更新的选项和行为：

   - 通知以下数量将发送通知并从可销售数量中扣除。

   - 缺货阈值支持正金额、零金额和负金额。 启用延交订单后，正金额将被忽略，视为零（或无限）。

   - 延交订单支持零（无限）和负金额。 启用时，以下通知数量不会从可销售数量中扣除。

- 新保留跟踪潜在销售额，在订单发运时转换为数量扣减额。 您从不直接访问或创建预留。 [!DNL Commerce]通过订单、装运和贷项通知单在后台创建和管理预订。

- [订单和发运](shipments.md)包括使用Source选择算法推荐发运的新功能，并支持来自多个来源的部分发运来完成订单。

- 新的[导入/导出功能](inventory-import-export.md)允许您成批添加源、更新库存数量以及设置目录中所有SKU的库存状态（缺货/缺货）。 这些功能允许您修改一个、选定或所有源。

- 通过产品网格页面新建的批量选项支持批量[分配和取消分配源](bulk-assignment.md)以及[将库存转移到源](inventory-transfer.md)。

- [!DNL Inventory Management]支持B2B目录。 当前，所有B2B产品都必须分配给默认Source和默认库存。

## [!DNL Commerce Order Management]和[!DNL Inventory Management]

[Commerce Order Management (MCOM)](https://commerce-docs.github.io/oms-documentation-archive/)与[!DNL Inventory Management]不兼容。 安装后，MCOM模块会为[!DNL Commerce]提供所有库存管理功能，包括单一来源和多来源管理、库存、预留等。 默认情况下，[!DNL Inventory Management]模块处于禁用状态。

MCOM为高级全渠道订单管理、全球库存和多源、从商店到仓库的履行以及集中化客户服务提供了广泛的功能和服务。 有关完整的功能列表，请参阅[MCOM功能列表](https://commerce-docs.github.io/oms-documentation-archive/getting-started/feature-list/)。

[!DNL Inventory Management]扩展了现有[!DNL Commerce]功能，并增加了用于跟踪进程内订单、现有库存、库存可用库存和扩展开发的API的选项。

## [!DNL Inventory Management]模块

您可能要禁用[!DNL Inventory Management]模块以：

- 加快当前位于Adobe Commerce或Magento Open Source 2.0/2.1/2.2/2.3上的商户的升级并迁移到2.4.x。

- 使用自定义或第三方库存和订单管理模块。

- 使用[!DNL Order Management System]进行库存管理。 当前连接器不支持[!DNL Inventory Management]接口。 对于升级到Adobe Commerce 2.4.0的OMS商户，必须禁用这些模块。

有关完整的详细信息，请参阅[安装和更新](install-update.md)。

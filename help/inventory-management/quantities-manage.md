---
title: 管理库存数量
description: 了解如何为新产品分配来源和数量或更改现有产品。
exl-id: b3d4a4c0-725a-4e62-854f-efb6a5709f73
feature: Inventory, Products
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 0%

---

# 管理库存数量

以下信息详细说明了如何为新产品分配来源和数量或更改现有产品。

创建产品时，在创建产品期间分配来源和数量。 请参阅 [创建产品](../catalog/product-create.md) 以获取完整说明。 这些页包含每个源的源和数量的单源和多源信息。

首次访问已升级的 [!DNL Commerce] 替换为 [!DNL Inventory Management]，则所有产品和数量都将分配给“默认来源”。 通过.csv文件导入新产品时，它们也会被分配到“默认来源”。

单一来源和多来源商家可以更新每个产品或批量更新来源、库存数量和阈值。

- 单一来源商家可以更新默认来源的产品数量。 此数量是可供销售的产品总数。

- 多来源商家可以为每个地点（仓库、商店、卸货发货人等）为每个产品分配多个来源和数量。 建议您在设置产品库存量之前添加源。

向产品添加来源和数量时，可以通过Product Grid查看金额。 如果您有大量源，请将鼠标悬停在 _[!UICONTROL Quantity per Source]_查看包含当前数量的完整可滚动源列表。

![每个来源的产品数量](assets/inventory-product-quantity.png){width="600" zoomable="yes"}

您可以使用以下选项将库存分配给产品：

- [按产品分配源](sources-assign-per-product.md)  — 在目录中为每个产品手动分配源。

- [按产品分配数量](quantities-assign-per-product.md)  — 按来源将现有库存量添加至产品。 此信息特定于多源商家。

- [批量分配和取消分配源](bulk-assignment.md)  — 将来源作为成批活动分配给选定的产品。 使用 [将库存转移到来源](inventory-transfer.md) 选项。

- [将库存转移至来源](inventory-transfer.md)  — 将所有库存从一个来源来源成批转移至目标来源。

- [导入和导出数量](inventory-import-export.md)  — 使用导入和导出功能更新具有来源和库存数量的多个产品SKU。

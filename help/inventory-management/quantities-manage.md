---
title: 管理库存数量
description: 了解如何为新产品分配来源和数量或更改现有产品。
exl-id: b3d4a4c0-725a-4e62-854f-efb6a5709f73
feature: Inventory, Products
TQID: https://experienceleague.adobe.com/ykiHTLnzZGtJrRdp2wZvlL7YLbEb7iAiYlcbY8K7IX8
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 325
ht-degree: 0%

---

# 管理库存数量

以下信息详细说明了如何为新产品分配来源和数量或更改现有产品。

创建产品时，在创建产品期间分配来源和数量。 有关完整说明，请参阅[创建产品](../catalog/product-create.md)。 这些页包含每个源的源和数量的单源和多源信息。

首次访问具有[!DNL Inventory Management]的已升级[!DNL Commerce]时，所有产品和数量都会分配给默认Source。 通过.csv文件导入新产品时，它们也会分配到默认的Source。

单一来源和多来源商家可以更新每个产品或批量更新来源、库存数量和阈值。

- 单一来源商家可以更新默认Source的产品数量。 此数量是可供销售的产品总数。

- 多来源商家可以为每个地点（仓库、商店、卸货发货人等）为每个产品分配多个来源和数量。 建议您在设置产品库存量之前添加源。

向产品添加来源和数量时，可以通过Product Grid查看金额。 如果源数太多，请将鼠标悬停在&#x200B;_[!UICONTROL Quantity per Source]_上以查看包含当前数量的源的可滚动完整列表。

每个源的![产品数量](assets/inventory-product-quantity.png){width="600" zoomable="yes"}

您可以使用以下选项将库存分配给产品：

- [为每个产品分配源](sources-assign-per-product.md) — 在目录中为每个产品手动分配源。

- [为每个产品分配数量](quantities-assign-per-product.md) — 将现有库存量添加到每个来源的产品。 此信息特定于多源商家。

- [批量分配和取消分配源](bulk-assignment.md) — 将源作为批量操作分配给所选产品。 如果要转移库存并移除来源，请使用[将库存转移到Source](inventory-transfer.md)选项。

- [将库存转移到Source](inventory-transfer.md) — 将所有库存从一个来源来源批量转移到目标来源。

- [导入和导出数量](inventory-import-export.md) — 使用导入和导出功能更新具有来源和库存数量的多个产品SKU。

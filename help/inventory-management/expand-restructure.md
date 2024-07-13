---
title: 扩展和重组库存
description: 了解如何扩展到多来源商户或减少到单来源商户。
exl-id: 880474e3-6533-4b2f-adf7-4312787ff736
feature: Inventory, Configuration
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 0%

---

# 扩展和重组库存

随着您的业务增长和变化，[!DNL Inventory Management]将支持您的需求。 您可以轻松展开到多来源商家，或展开到单来源商家。

## 展开至多源

单一来源商家可以增加新的商店、仓库、卸货船等。 扩展只需要少量添加和库存更新，即可扩展到多源：

1. 为每个新位置添加[自定义源](sources-add.md)。

   您仅对捆绑包产品使用默认Source。

1. 根据需要为新源添加[自定义库存](stocks-add.md)。

   例如，您可能希望为每个网站、国家/地区、区域设置或其他方法创建库存。 您可以将来源分配给自定义库存。 对于捆绑包产品，您只使用“默认库存”。

1. 为您的产品更新[源分配和数量](quantities-manage.md)。

   您还可以使用[批量操作工具](bulk-assignment.md)和[导入 — 导出](inventory-import-export.md)功能来快速添加源和产品数据。

## 重构为单一源

对于希望将在线销售减少到一个运送地点的多来源商家，请修改您的来源、库存和数量以进行更新：

1. 禁用[自定义源](sources-disable.md)。

1. 将产品库存转移到您的默认Source。

   建议使用批量操作。 请参阅[将库存转移到Source](inventory-transfer.md)。

1. 将所有网站分配给[默认库存](stocks-manage.md)。

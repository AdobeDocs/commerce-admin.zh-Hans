---
title: 管理库存库存
description: 了解如何使用库存表示销售渠道来源的虚拟汇总产品库存。
exl-id: 076b1325-2de4-46d3-9976-d900bd2cef47
TQID: https://experienceleague.adobe.com/IeG1bA1etAjxiDjSWY83GLNugllHT1mUrZBde45Ha8g
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 524
ht-degree: 0%

---

# 管理库存

库存代表您的销售渠道（网站）来源的虚拟汇总产品库存。 根据您的站点配置，库存可能会分配给一个或多个销售渠道。 每个销售渠道只能分配一个库存，单个库存可以分配给多个销售渠道。 通过库存，您可以修改在订单通过销售渠道访问时所使用的来源优先顺序。

您首先会看到一个不能删除或禁用的“默认库存”。 您只能向库存添加其他销售渠道。 唯一分配的源是默认Source。 此库存由单一来源商家、第三方集成和进口产品使用。

销售渠道指销售库存的实体。 默认情况下，[!DNL Commerce]将商店网站作为销售渠道提供。 可以扩展销售渠道以支持其他渠道，如B2B客户组和商店视图。 每个销售渠道只能关联到一个Stock。

- **Sales Channel支持** — 销售渠道目前包含现成的网站。 您可以扩展销售渠道以包括自定义选项，如B2B客户组和商店视图。 每个销售渠道只能分配一个库存。 单个库存可以分配给多个销售渠道。
- **映射到源** — 每个库存可以分配一个或多个启用或禁用的源，从而计算每个产品的虚拟汇总库存。
- **优先级订单履行** — 完成订单时，Source选择算法的现成优先级算法使用股票的来源列表（从上到下）。

下图可帮助定义库存如何与自行车店商家的“来源”和“销售渠道”相关联。

![图，例如商店的库存](assets/diagram-stock.png){width="600" zoomable="yes"}

## 山地自行车和商店的示例库存

所有商店都以默认库存开始。 由于以下原因，它必须保持为`Enabled`：

- 在导入新产品时，使用此功能，自动将产品分配给默认来源和库存，以便立即访问[!DNL Inventory Management]。
- 您不能将默认Source以外的其他源添加到此库存。
- 它是单一来源商家、捆绑产品和分组产品的必需和使用项。

对于多来源商家，请创建和配置库存，以最适合您的商店和订单履行。 当您将新库存分配给销售渠道时，该销售渠道中任何预先存在的库存都将被取消分配。

对于多商店安装，默认库存最初分配给[主网站](../stores-purchase/stores.md#add-websites){target="_blank"}和默认商店。 在&#x200B;**[!UICONTROL Products]**&#x200B;网格视图中，为已启用和禁用的产品显示正确的库存和数量。

![管理库存](assets/inventory-stock.png){width="600" zoomable="yes"}

## 按钮栏

| 按钮 | 描述 |
|--|--|
| [!UICONTROL Add New Stock] | 打开&#x200B;_[!UICONTROL New Stock]_&#x200B;表单，该表单用于输入新的库存库存，以将库存映射到销售渠道。 |

## 管理Stock列描述

| 列 | 描述 |
|--|--|
| [!UICONTROL ID] | 为股票条目生成的唯一数字ID。 |
| [!UICONTROL Name] | 标识库存库存的唯一名称。 |
| [!UICONTROL Sales Channels] | 通过将库存作为&#x200B;_销售渠道_&#x200B;分配给特定网站来定义库存的范围。 |
| [!UICONTROL Assigned sources] | 分配给库存的供应所有产品数量的来源。 |
| [!UICONTROL Action] | **[!UICONTROL Edit]** — 在编辑模式下打开库存库存记录。 |

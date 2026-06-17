---
title: 商家来源类型
description: 根据您企业中的位置或来源数量，了解这两种来源类型。
exl-id: ec928929-5826-4504-9fd0-84256b37cb39
feature: Inventory, Products
TQID: https://experienceleague.adobe.com/-ABDMLnAibksuQGkdEM683g8JwcUSt2DQERC0WJnQiM
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 486
ht-degree: 0%

---

# 商家来源类型

[!DNL Commerce]支持所有规模企业的[!DNL Inventory Management]，包括单个商店，一个网站到一个网站、商店、仓库和托运人的国际网络。 根据您业务中的位置或来源数量，所有使用Adobe Commerce或Magento Open Source的商家都属于两种类型。

- 单一来源商户从一个位置发运产品。 在您开始向安装添加自定义源和股票之前，您被视为单一来源商家/模式。

- 多来源商家从多个位置发运产品，如实体店、仓库、卸货商和配送中心。 在为每个位置添加自定义来源后，您将自动成为多来源贸易商。

## 单一来源商家

单一来源商户只有一个位置，用于管理现有库存量并履行订单。 通常，您有多个网站（或销售渠道）从同一目录、库存和位置销售产品。

例如，您有一个网站或多站点实施，美国、德国、法国和巴西的网站都从一个大型仓库中提取产品。 此单一来源管理所有库存数量、发运和退货，而不管哪个销售渠道接收订单。

要开始使用，请执行以下操作：

- 根据需要为商店清单配置[全局和产品设置](configuration.md)。

- 使用单个库存库位的信息更新[默认Source](sources-manage.md)。 不需要创建其他源。

- 更新[默认库](stocks-manage.md)。 确保选择您的所有网站作为销售渠道。 添加新网站时，[!DNL Commerce]会自动将其添加到默认库存。 不需要创建附加库存。

>[!NOTE]
>
>随着业务的扩展，添加其他源和库存，并更新您的[!DNL Inventory Management]配置以成为多源商人。 有关所有详细信息，请参阅[展开并重构库存](expand-restructure.md)。

## 多源商家

多来源商家具有一个网站或多站点实施，并管理现有库存量和通过多个位置完成订单。

例如，您有一个多站点实施，其中包含美国、德国、法国和巴西的网站。 您的业务包括位于这些国家/地区的多个仓库和商店，以及管理所有库存并完成订单的托运人服务。 这些位置和网站成为[!DNL Commerce]中的资源和库存。 您可以为美洲创建一个库存，为欧洲创建一个库存，根据区域设置和位置分配网站和来源。 在每个网站上购物的客户只能访问来自指定来源的可销售库存。

要开始使用，请执行以下操作：

- 根据需要配置商店清单的全局设置。

- 为您的库存库位（仓库、商店、分发中心和卸货发货人）添加[自定义源](sources-add.md)。

- 为每个区域添加[自定义库存](stocks-add.md)以映射具有多个来源的网站。 按位置优先级重新排序每个库存中的来源，这有助于您完成订单。

- 将来源分配给产品，添加每个地点的数量。

- 完成每个产品有关数量阈值、延交订单等的任何进一步配置。

---
title: ' [!DNL Inventory Management]简介'
description: 了解如何使用 [!DNL Inventory Management]  for [!DNL Commerce] 管理跨来源和库存的库存、计算可销售数量、跟踪预留和支持订单履行。 使用管理员配置设置并生成报告，并使用命令行界面进行设置和后台更改。
exl-id: 6a7dd27e-248f-4c40-b2db-0d70529422a1
TQID: https://experienceleague.adobe.com/7v-G-DZEki7y-4HSmq-rJxsmu6vih26jRYYCRRUF-XY
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 125a49f740639bce0ced8063074ca43d627c0eac
workflow-type: tm+mt
source-wordcount: 371
ht-degree: 0%

---

# [!DNL Inventory Management]简介

[!DNL Commerce]的[!DNL Inventory Management]可帮助商家跨一个或多个网站以及物理或虚拟产品位置管理库存。 它提供了管理和命令行界面中的工具，用于配置库存、跟踪现有量和汇总可销售数量、在结账期间保护库存以及支持订单履行。 您可以将[!DNL Inventory Management]用于单个来源或多来源网络，包括仓库、商店、提货地点、卸货发货人和其他履行地点。

## 使用[!DNL Inventory Management]的方法

- **管理员：**&#x200B;设置库存选项并生成库存报告。
- **命令行接口：**&#x200B;运行安装程序命令并在后台应用清单更改。
- **配置范围：**&#x200B;全局配置清单设置、按源或按产品。

## 主要功能

[!DNL Inventory Management]功能包括：

- 对于其库存源自单个来源或多个来源的商家具有不同的配置
- 用于跟踪分配来源中汇总的可销售数量的库存
- 并发签出保护
- 支持基于距离或优先级的履行建议的装运匹配算法

>[!NOTE]
>
>这些功能是通过社区工程计划作为[Inventory management](https://github.com/magento/inventory)（以前为MSI）项目的一部分开发的。<br/>
>
>[!DNL Inventory Management]模块随Magento Open Source和Adobe Commerce一起安装，默认启用所有功能。 有关模块版本中包含的更改的信息，请参阅[发行说明](release-notes.md)。

## 基本术语

在使用[!DNL Inventory Management]时，请务必了解以下术语：

[!UICONTROL Sources]表示存储和发运可用产品的物理位置。 有关示例和图表，请参阅[库存和源](sources-stocks.md)。 （任何位置都可以指定为虚拟产品的来源。）

[!UICONTROL Stocks]将销售渠道（当前仅限于网站）映射到来源位置和现有库存。 一个库存可以映射到多个销售渠道，但一个销售渠道只能分配给一个库存。

[!UICONTROL Aggregate Salable Quantity]是可以通过Sales Channel销售的总虚拟库存。 金额会在分配给库存的所有来源中进行计算。

当客户将产品添加到购物车并完成结帐时，[!UICONTROL Reservations]跟踪从可销售数量中扣除的金额。 订单发运时，保留会清除并从特定来源库存数量中扣减发运额。

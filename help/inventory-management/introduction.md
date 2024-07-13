---
title: Inventory management简介
description: 了解如何使用 [!DNL Inventory Management] 功能管理多个位置的库存，以便您的 [!DNL Commerce] 商店准确地反映实际盘点。
exl-id: 6a7dd27e-248f-4c40-b2db-0d70529422a1
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '360'
ht-degree: 0%

---

# Inventory management简介

[!DNL Commerce]的[!DNL Inventory Management]为您提供了用于管理产品库存的工具。 只有一家商店到多个仓库、商店、提货地点、卸货托运人等的商家可以使用这些功能来维护销售数量，并处理发运以完成订单。 您可以跟踪库存数量，为所有网站的客户提供准确的可销售库存量，并根据距离或优先级根据建议进行发货。 您还可以按来源和产品全局配置首选产品配置（适用于所有商店和产品）。 这些功能会随着您的业务增长而增加，允许您通过一些额外设置从单个仓库或复杂的运输网络工作。

[!DNL Inventory Management]功能包括：

- 对于其库存源自单个来源和多个来源的商家具有不同的配置
- 用于通过分配的来源跟踪可用汇总数量的库存
- 并发签出保护
- 装运匹配算法

>[!NOTE]
>
>这些功能是通过社区工程计划作为[Inventory management](https://github.com/magento/inventory)（以前为MSI）项目的一部分开发的。<br/>
>
>[!DNL Inventory Management]模块随Magento Open Source和Adobe Commerce一起安装，默认启用所有功能。 有关模块版本中包含的更改的信息，请参阅[发行说明](release-notes.md)。

## 基本术语

在使用[!DNL Inventory Management]时，请务必了解以下术语：

[!UICONTROL **源**]&#x200B;表示存储和发运可用产品的物理位置。 这些地点可包括仓库、实体店、配送中心和卸货托运人。 （任何位置都可以指定为虚拟产品的来源。）

[!UICONTROL **库存**]&#x200B;将销售渠道（当前仅限于网站）映射到来源位置和现有库存。 一个库存可以映射到多个销售渠道，但一个销售渠道只能分配给一个库存。

[!UICONTROL **汇总可销售数量**]&#x200B;是可以通过销售渠道销售的虚拟库存总数。 金额会在分配给库存的所有来源中进行计算。

当客户将产品添加到购物车并完成结帐时，[!UICONTROL **预留**]&#x200B;跟踪从可销售数量中扣除的金额。 订单发运时，保留会清除并从特定来源库存数量中扣减发运额。

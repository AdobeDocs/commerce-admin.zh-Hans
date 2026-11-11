---
title: 价格手册
description: 了解如何从[!DNL Adobe Commerce]中的目录和定价数据映射价格手册。
role: Admin, Developer
recommendations: noCatalog
badgeSaas: label="仅限SaaS" type="Positive" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="仅适用于使用CCDM设置的Adobe Commerce as a Cloud Service实例（Adobe管理的SaaS基础架构）。"
TQID: 'https://experienceleague.adobe.com/8gpl-l6oQebTnrt-00-n1FEdKnzqhTQi3hRz4lrGQoE'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
  - id: de2e2e68-c5d7-4efe-be7b-27528698f06b
    internal-label: Commerce as a Cloud Service
feature_v2:
  - id: 3033d2ab-c1d2-5b52-b865-72d9e5ad2c37
    internal-label: Currency
  - id: 58c984c2-e237-5c50-9718-500e40d1e82c
    internal-label: Merchandising
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
source-git-commit: 1041abe0e7d7c1212a717d5fd03180ce7fd32958
workflow-type: tm+mt
source-wordcount: '603'
ht-degree: 0%
---
# 价格手册

价格手册定义跨客户层和市场的目录来源的产品价格。 它们支持父价目表和子价目表的层次结构。

![价格手册层次结构](../assets/price-book-hier.png)

## 重要概念

| 术语 | 描述 |
| ------ | ------------- |
| **价格手册** | 逻辑分组，定义目录来源的价格；例如，特定区域或客户层，用于管理产品价格。 |
| **备用价格手册** | 层次结构中最顶层的价格手册。 它没有父级，并且是&#x200B;*仅*&#x200B;价格手册，它定义了自身及其所有子级价格手册的货币。<br/><br/>如果在创建价格手册期间（通过API）未定义任何父项，则会创建一个新的备用价格手册。 |
| **父价格手册** | 一个更高级别的价格手册，如果子价格手册中没有明确设置价格，则子价格手册可以从中继承价格。 |
| **层次结构深度** | 最多三个级别（回退 — >子级 — >孙级）<br/><br/>在摄取时未强制执行。 |
| **货币** | 仅为后备价格手册定义。 由所有子价格手册继承。<br/><br/>如果在创建后备价格手册期间（通过API）未指定货币，则该货币将默认为USD。 |
| **产品价格** | 特定价格手册中分配给产品(SKU)的特定价格。 |
| **折扣** | 折扣在产品价格中定义。 未继承。 |

## 价格手册实施

在将Adobe Commerce as a Cloud Service与可组合目录数据模型(CCDM)结合使用时，价格手册会从目录和定价数据中进行映射。 它们不会手动创建。

从较高层面来看，映射为：

- **存储视图→目录源** — 存储视图产品数据（包括本地化的属性）映射到目录源。
- **网站→价格手册或价格手册** — 网站定价映射到适用的价格手册或价格手册。
- **客户组定价→价格手册条目** — 客户组定价映射到相关的价格条目。

在Adobe Commerce配置中维护源目录、网站和定价配置，然后通过配置可用的价格手册在相关目录视图中分配映射的价格手册。 如果未分配价格手册，目录视图将使用默认价格手册。

目录视图使用可用的价格手册配置及其目录数据和策略来确定促销体验，包括产品返回的价格。

>[!NOTE]
>
>对于Commerce B2B，系统会根据共享目录配置为每个目录视图创建并分配一个价格手册。 您无需为这些视图配置价格手册可用性。

## 结帐定价

价格手册支持销售和店面目录体验。 Commerce Core将继续处理购物车和结账事宜。 仅在CCDM中可用的价格不会自动成为结账使用的价格。

将价格与Commerce核心配置保持一致，并在实施验证过程中测试显示的价格、购物车、促销和结账。

## 查看价格手册

目录数据同步完成后，在&#x200B;**[!UICONTROL Catalog views]**&#x200B;工作区中查看可用的价格手册及其ID。

1. 转到&#x200B;_存储设置_，然后单击&#x200B;**[!UICONTROL Catalog views]**。

1. 单击&#x200B;**[!UICONTROL Create catalog view]**。

1. 查看目录视图配置的&#x200B;**[!UICONTROL Price Books]**&#x200B;部分中可用的价格簿。

   ![价格簿名称和ID](../assets/price-book-name-ids.png)

## 配置价格手册可用性

通过在Commerce管理员的“目录视图”工作区中配置可用的价格手册，将映射的价格手册与目录视图关联。

>[!NOTE]
>
>专用目录视图（启用了[!UICONTROL Catalog Protection]的视图）只能引用一个价格手册。

1. 从&#x200B;**[!UICONTROL Catalog views]**&#x200B;工作区中，选择要配置的目录视图。

1. 在&#x200B;**[!UICONTROL Price Books]**&#x200B;部分中，选择目录视图支持的商店可用的价格手册。

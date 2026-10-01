---
title: '[!UICONTROL Stores]菜单'
description: Commerce管理员包括[!UICONTROL Stores]菜单，通过菜单可访问用于设置商店层次结构、配置、库存、税和属性的工具。
exl-id: b9d8ea6b-5b4b-42af-b74d-7afa48ccf2ff
TQID: https://experienceleague.adobe.com/LEoQUYqvin2UfF55kCMUiEUh8YungghN-VuEwUOu7gY
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
    internal-label: Accounts
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
    internal-label: Order Management System
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: bc4baccc4b40fb7ecdc7f489bfaf3c797881db88
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 0%
---
# [!UICONTROL Stores]菜单

通过&#x200B;_[!UICONTROL Stores]_&#x200B;菜单，您可以访问不太常使用，但在Adobe Commerce或Magento Open Source安装过程中被引用的设置。 这些功能包括设置商店层次结构、配置、销售和订单设置、税和货币、产品属性、产品审核评级以及客户组。

>[!BEGINTABS]

>[!TAB Adobe Commerce]

仅[!BADGE PaaS]{type=Informative url="https://experienceleague.adobe.com/zh-hans/docs/commerce/user-guides/product-solutions" tooltip="仅适用于云项目（Adobe管理的PaaS基础架构）和内部部署项目上的Adobe Commerce 。"}

![管理员 — 商店菜单](./assets/stores-menu.png){width="500" zoomable="yes"}

>[!TAB Adobe Commerce as a Cloud Service]

仅[!BADGE SaaS]{type=Positive url="https://experienceleague.adobe.com/zh-hans/docs/commerce/user-guides/product-solutions" tooltip="仅适用于Adobe Commerce as a Cloud Service和Adobe Commerce Optimizer项目（Adobe管理的SaaS基础架构）。"}

![管理员 — 商店菜单](./assets/stores-menu-accs.png){width="500" zoomable="yes"}

>[!ENDTABS]

## 显示[!UICONTROL Stores]菜单

在&#x200B;_管理员_&#x200B;侧边栏上，单击&#x200B;**[!UICONTROL Stores]**。

## 主要部分

### [!UICONTROL Settings]

在Adobe Commerce或Magento Open Source安装中管理[网站、商店和商店视图](stores.md#store-and-site-structure)的层次结构，以及所有[配置设置](../configuration-reference/guide-overview.md)。 此外，您还可以设置销售的[条款和条件](terms-and-conditions.md)，并管理[订单状态设置](order-status.md#custom-order-status)。

### [!UICONTROL Inventory]

[管理和创建库存](../inventory-management/introduction.md)以将您的销售渠道或网站链接到[来源](../inventory-management/sources-manage.md)。 库存提供汇总的可销售产品数量。 单个Source商户使用默认股票，而多Source商户使用其他自定义股票。

### [!UICONTROL Taxes]

管理您商店中所有类型的[税务功能](taxes.md)，设置商店的税则，定义客户和产品税分类，以及管理税区和税率。 您也可以将税率数据导入您的商店。

### [!UICONTROL Currency]

管理在您的商店中接受作为付款的[货币](currency.md)的汇率，并自定义出现在产品价格和销售文档中的货币符号。

### [!UICONTROL Attributes]

管理用于[客户](../customers/attribute-properties.md)或[产品信息](../catalog/attribute-product-create.md)、退货和产品分级的属性。 您可以创建属性、编辑现有属性和管理[属性集](../catalog/attribute-sets.md)。

### [!UICONTROL Other Settings]

管理[奖励汇率](../merchandising-promotions/reward-exchange-rates.md)、[礼品包装](cart-configuration.md#gift-wrap)和[礼品注册表](../merchandising-promotions/gift-registries.md)的其他设置。

## [!DNL Adobe Commerce Optimizer]集成

安装[!DNL Adobe Commerce Optimizer Connector]后，您可以同步网站并将视图数据存储到[!DNL Adobe Commerce Optimizer]。 网站范围控制[价格同步](stores.md#step-1-create-a-website)（价格和价格手册）。 商店视图范围控制[产品同步](store-views.md#add-a-store-view) （产品和产品属性）。

有关[!UICONTROL All Stores]网格上显示的同步状态指示器，请参阅[Adobe Commerce Optimizer同步状态](store-views.md#optimizer-sync-status)。 有关连接器设置和配置行为，请参阅&#x200B;*Commerce连接器指南*&#x200B;中的[自定义Adobe Commerce Optimizer范围导出配置](https://experienceleague.adobe.com/zh-hans/docs/commerce/aco-optimizer-connector/get-started#customize-the-commerce-scopes-export-configuration)。

如果已安装[!DNL Adobe Commerce Optimizer Connector for B2B]，则还会同步可用B2B共享目录的数据。 请参阅[管理目录视图](../b2b/catalog-views-manage.md)。

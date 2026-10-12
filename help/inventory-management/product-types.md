---
title: 产品类型
description: 了解[!DNL Inventory Management]如何支持所有Adobe Commerce和Magento Open Source产品类型的库存和订单管理。
exl-id: c800168a-e8b2-4d72-bd3d-68f46ece8a5e
feature: Inventory, Products
TQID: 'https://experienceleague.adobe.com/3F5vZOseQC7ILpL0j-ksjWP-GW7c0gUN9Zy7hylzzHU'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
    internal-label: Order Management System
  - id: 8dc0e58b-adf0-51bb-8db5-bb36e3e656fb
    internal-label: Inventory
  - id: 4067ab89-2e97-5de1-8d98-de8318461a8d
    internal-label: Products
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: acc7571574eb9c7e96911266897350a77913488e
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 0%
---
# 产品类型

[!DNL Inventory Management]支持Adobe Commerce和Magento Open Source中所有产品类型的库存和订单管理：简单、可配置、虚拟、可下载、捆绑和分组。 来源、库存和运输的选项和要求可能因产品类型而异。

- [单一来源商家](merchant-sourcing.md#single-source-merchants)无需其他更新即可创建和更新产品设置和数量。 所有创建或新导入的产品都会自动分配给默认Source和默认库存，如果启用且有库存，客户将立即可以使用它们。

- [多源商家](merchant-sourcing.md#multi-source-merchants)在创建产品期间或之后分配源、每个源的数量以及设置。 [!DNL Commerce]将所有新导入的产品分配给默认Source，这需要进行额外的编辑以分配源和数量。

| 产品类型 | Shipping和Source选择算法 |
|--|--|
| [[!UICONTROL Simple]](../catalog/product-create-simple.md){target="_blank"} | 在运输时支持SSA建议和覆盖。 |
| [[!UICONTROL Configurable]](../catalog/product-create-configurable.md){target="_blank"} | 在运输时支持SSA建议和覆盖。 |
| [[!UICONTROL Virtual]](../catalog/product-create-virtual.md){target="_blank"} | 始终使用SSA建议。 系统在创建发票时隐式运行算法，并始终使用建议的结果。<br/>您无法调整这些结果。 |
| [[!UICONTROL Downloadable]](../catalog/product-create-downloadable.md){target="_blank"} | 始终使用SSA建议。 系统在创建发票时隐式运行算法，并始终使用建议的结果。 <br/>您无法调整这些结果。 |
| [[!UICONTROL Bundle]](../catalog/product-create-bundle.md){target="_blank"} | 在运输时支持SSA建议和覆盖。 |
| [[!UICONTROL Grouped]](../catalog/product-create-grouped.md){target="_blank"} | 在运输时支持SSA建议和覆盖。 |

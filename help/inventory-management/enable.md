---
title: “启用 [!DNL Inventory Management]"
description: 了解如何启用 [!DNL Inventory Management] 在全局商店或产品级别。
exl-id: 89bd2f8b-b9e4-4b9a-b729-f7bd71f764c9
feature: Inventory, Configuration
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 0%

---

# 启用 [!DNL Inventory Management]

要管理产品库存，请启用 [!DNL Inventory Management] 在全局商店或产品级别。 当 _管理库存_ 选项已启用， [!DNL Inventory Management] 通过配置的库存和来源自动跟踪可用于站点的产品数量。 启用后，每个功能和选项都开始进行跟踪和报告，而无需额外配置。

您的企业以销售速度运行和更新库存。 在客户购物时，您将收到有关每个销售渠道和来源的可用库存的确切、更新信息。 当客户将产品添加到购物车并完成采购时，以及当您管理订单、创建发运和发放退款时，可用可销售数量会按库存更新。 新库存或转移库存的到达者会向您的来源更新，可立即在线销售。 延交订单最多可完成指定的阈值，无无限订单或额外配置。 而且，您可以输入并完成一个或多个来源中带有建议的部分或全部发运，从而完全控制订单履行和现有库存。

>[!NOTE]
>
>默认情况下， [!DNL Inventory Management] 安装或升级时启用 [!DNL Commerce]. 根据您的业务需求，您可能需要启用或禁用跟踪的 [!DNL Inventory Management] 范围 [!DNL Commerce].

此设置在单源清单和多源清单中的工作方式：

- 使用 [!DNL Inventory Management]，启用 _[!UICONTROL Manage Stock]_.

- [!UICONTROL Manage Stock] 产品级配置的设置会覆盖商店配置。

- 要使用Order Management或第三方服务（如ERP），请禁用 [!UICONTROL Manage Stock].

- 如果产品级配置使用系统默认值，则应用商店配置将覆盖。

替换为 [!DNL Inventory Management] 已启用，请参阅以下内容以配置所有设置：

- [配置全局选项](global-options.md)  — 影响整个目录的设置，视为系统默认设置。

- [配置产品选项](product-options.md)  — 覆盖全局选项的特定产品的设置。

## 启用或禁用 [!DNL Inventory Management]

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中，展开 **[!UICONTROL Catalog]** 并选择 **[!UICONTROL Inventory]**.

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) _产品股票期权_ 和配置：

   ![产品股票期权](assets/config-catalog-inventory-product-stock-options.png){width="600" zoomable="yes"}

   - 要管理库存并使用所有，请执行以下操作 [!DNL Commerce] 功能，设置 **[!UICONTROL Manage Stock]** 到 `Yes` （默认）。

   - 禁用 [!DNL Inventory Management]，取消选择 **[!UICONTROL Use system value]** 复选框和设置 **[!UICONTROL Manage Stock]** 到 `No`.

1. 完成后，单击 **[!UICONTROL Save Config]**.

## 管理商店库存

请参阅 [配置全局选项](global-options.md).

## 管理产品的库存

请参阅 [配置产品选项](product-options.md).

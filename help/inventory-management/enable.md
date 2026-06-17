---
title: 启用 [!DNL Inventory Management]
description: 了解如何在全局商店或产品级别启用 [!DNL Inventory Management] 。
exl-id: 89bd2f8b-b9e4-4b9a-b729-f7bd71f764c9
feature: Inventory, Configuration
TQID: https://experienceleague.adobe.com/evCX34nY-m7WQnZt3xw7ng6-It7Xlf5DTanjKbP1fCk
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157id: dac87252-6066-4d6e-a9d2-f6d84c323de7id: f42e0a1a-0d79-488d-a83f-f2c30672b137
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 337
ht-degree: 0%

---

# 启用[!DNL Inventory Management]

要管理产品库存，请在全局商店或产品级别启用[!DNL Inventory Management]。 启用&#x200B;_管理库存_&#x200B;选项后，[!DNL Inventory Management]通过配置的库存和来源自动跟踪可用于站点的产品数量。 启用后，每个功能和选项都开始进行跟踪和报告，而无需额外配置。

您的企业以销售速度运行和更新库存。 在客户购物时，您将收到有关每个销售渠道和来源的可用库存的确切、更新信息。 当客户将产品添加到购物车并完成采购时，以及当您管理订单、创建发运和发放退款时，可用可销售数量会按库存更新。 新库存或转移库存的到达者会向您的来源更新，可立即在线销售。 延交订单最多可完成指定的阈值，无无限订单或额外配置。 而且，您可以输入并完成一个或多个来源中带有建议的部分或全部发运，从而完全控制订单履行和现有库存。

>[!NOTE]
>
>默认情况下，在安装或升级[!DNL Commerce]时启用[!DNL Inventory Management]。 根据您的业务需求，您可能需要在[!DNL Commerce]中启用或禁用跟踪的[!DNL Inventory Management]。

此设置在单源清单和多源清单中的工作方式：

- 要使用[!DNL Inventory Management]，请启用&#x200B;_[!UICONTROL Manage Stock]_。

- 产品级别配置中的[!UICONTROL Manage Stock]设置会覆盖商店配置。

- 要使用Order Management或第三方服务（如ERP），请禁用[!UICONTROL Manage Stock]。

- 如果产品级配置使用系统默认值，则应用商店配置将覆盖。

启用[!DNL Inventory Management]后，请参阅以下内容以配置所有设置：

- [配置全局选项](global-options.md) — 影响整个目录的设置被视为系统默认设置。

- [配置产品选项](product-options.md) — 覆盖全局选项的特定产品的设置。

## 启用或禁用[!DNL Inventory Management]

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧面板中，展开&#x200B;**[!UICONTROL Catalog]**&#x200B;并选择&#x200B;**[!UICONTROL Inventory]**。

1. 展开![扩展选择器](../assets/icon-display-expand.png) _产品股票期权_&#x200B;并配置：

   ![产品股票期权](assets/config-catalog-inventory-product-stock-options.png){width="600" zoomable="yes"}

   - 要管理库存并使用所有[!DNL Commerce]功能，请将&#x200B;**[!UICONTROL Manage Stock]**&#x200B;设置为`Yes`（默认值）。

   - 要禁用[!DNL Inventory Management]，请取消选中&#x200B;**[!UICONTROL Use system value]**&#x200B;复选框并将&#x200B;**[!UICONTROL Manage Stock]**&#x200B;设置为`No`。

1. 完成后，单击&#x200B;**[!UICONTROL Save Config]**。

## 管理商店库存

请参阅[配置全局选项](global-options.md)。

## 管理产品的库存

请参阅[配置产品选项](product-options.md)。

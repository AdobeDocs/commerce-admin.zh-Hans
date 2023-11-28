---
title: 创建多来源装运
description: 了解多源商家如何创建和发送发货。
exl-id: d2995139-0fc3-4379-a4ec-b0d38ed566bb
feature: Inventory, Shipping/Delivery
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 0%

---

# 创建多来源装运

替换为 [!DNL Inventory Management]，在拥有库存时发送一个或多个装运。 要根据需要生成附加发运，请使用建议的或人工输入的数量和来源重复这些说明。 这些说明详细说明多来源商家如何发送货物。 单一来源商户无需这些额外步骤即可发送货物(请参阅 [创建装运](../stores-purchase/shipments.md#create-a-shipment){target="_blank"} （在核心用户指南中）。

在创建发运时，请为已计算的建议使用来源选择算法。 遵循并使用这些建议，或设置每个来源的金额，从而生成自定义发运。 您可以控制每个订单的转出库存，设置要扣减的金额，发送一个或多个发运，并在库存可用时交付库存和延交订单。 对于订单中的每个行项目，输入要从来源数量中扣除的金额。

您可能希望将部分发运发送至：

- 在库存到达时完成延交订单

- 跨来源平衡库存扣减额

在输入发运时，现有库存量将减去输入的金额。 实际上，保留将转换为实际数量扣减。

## 创建装运

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. 找到订单并以视图模式打开。

1. 如果订单已付费、已开票并且准备发运，请单击 **[!UICONTROL Ship]**.

1. 为每个源完成发送产品的源选择：

   - 要查看送货建议，请单击 **[!UICONTROL Source Selection Algorithm]** 并选择算法。

     | 算法 | 描述 |
     |--|--|
     | [源优先级](source-priority-algorithm.md) | 根据分配给库存的来源订单建议来源发运。 |
     | [距离优先级](distance-priority-algorithm.md) | 建议根据实际距离或最短交货时间，从距离发运地址最近的来源发运。 |

     >[!IMPORTANT]
     >
     >将距离优先级算法用于装运时，路由和数据不会返回所选的 [计算模式](distance-priority-algorithm.md) （驾驶、骑车或行走）对于装运，SSA默认为“来源优先级”。 建议您同时设置 [每个库存的源的优先级](stocks-prioritize-sources.md).


   - 对象  **[!UICONTROL Select a Source to Ship from]**，选择要发送装运的源。

   - 对于每个行项目，请保留建议的数量或在 **[!UICONTROL Qty to Deduct]**. 此值指定从所选源的库存中扣除的金额。

   - 单击 **[!UICONTROL Proceed to Shipment]**.

     ![选择来源并输入数量](assets/shipment-adobe-shipping-sources.png){width="350" zoomable="yes"}

1. 查看 _[!UICONTROL New Shipment]_页面，并根据需要输入任何其他更改。

   此 _[!UICONTROL Inventory]_部分显示来源、产品发运、订购总数量和要发运的数量。

   ![发运的库存详细信息，例如部分发运](assets/inventory-shipment-details.png){width="350" zoomable="yes"}

1. 单击 **[!UICONTROL Submit Shipment]** 完成。

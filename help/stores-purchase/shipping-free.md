---
title: 免运费
description: 了解如何为您的商店设置免费送货选项。
exl-id: 3ce69583-0f7f-4c23-b3e3-7d2502bc1bca
feature: Shipping/Delivery
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '395'
ht-degree: 0%

---

# 免运费

_免运费_&#x200B;是您可以提供的最有效的促销活动之一。 可以基于最低购买量或设置为[购物车价格规则](../merchandising-promotions/price-rules-cart.md)，该规则会在满足一组条件时应用。 如果两者适用于同一顺序，则配置设置优先于购物车规则。

>[!NOTE]
>
>检查您的配送承运人配置，了解免费配送可能需要的任何其他设置。

## 步骤1：配置免费送货

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧面板中，展开&#x200B;**[!UICONTROL Sales]**&#x200B;并选择&#x200B;**[!UICONTROL Delivery Methods]**。

1. 展开&#x200B;**[!UICONTROL Free Shipping]**&#x200B;部分的![扩展选择器](../assets/icon-display-expand.png)。

   >[!NOTE]
   >
   >如有必要，请首先取消选中&#x200B;**[!UICONTROL Use system value]**&#x200B;复选框以更改以下设置，如所述。

1. 将&#x200B;**[!UICONTROL Enabled]**&#x200B;设置为`Yes`。

1. 对于&#x200B;**[!UICONTROL Title]**，请输入在结帐期间标识免费送货方法的标题以及描述该方法的&#x200B;**[!UICONTROL Method Name]**。

1. 对于&#x200B;**[!UICONTROL Minimum Order Amount]**，请输入符合免费送货条件的最小总值。

   >[!TIP]
   >
   >若要使用[表费率](shipping-table-rate.md)的免运费，请将&#x200B;_[!UICONTROL Minimum Order Amount]_&#x200B;设得过高，使其永远不满足。 使用此高值可阻止免费送货生效，除非由价格规则触发。

1. 设置&#x200B;**[!UICONTROL Include Tax to Amount]**：

   - `Yes` — 计算最小订单金额时包括税（小计+税 — 折扣）。
   - `No` — 在计算最小订单金额（小计 — 折扣）时不含税。

   ![免费送货](../configuration-reference/sales/assets/delivery-methods-free-shipping.png){width="600" zoomable="yes"}

1. 对于&#x200B;**[!UICONTROL Displayed Error Message]**，输入免费送货不可用时要显示的消息。

1. 设置&#x200B;**[!UICONTROL Ship to Applicable Countries]**：

   - `All Allowed Countries` — 来自您商店配置中指定的所有[国家/地区](../getting-started/store-details.md#country-options)的客户都可以使用免费送货。

   - `Specific Countries` — 选择此值后，将显示&#x200B;_[!UICONTROL Ship to Specific Countries]_&#x200B;列表。 选择列表中可使用免费送货的每个国家/地区。

1. 设置&#x200B;**[!UICONTROL Show Method if Not Applicable]**：

   - `Yes` — 始终显示免费送货方法，即使不适用也是如此。
   - `No` — 仅在适用的情况下显示免费送货方法。

1. 对于&#x200B;**[!UICONTROL Sort Order]**，输入数字，该数字用于确定结帐期间免费送货在交货方式列表中的位置。

   `0` =第一，`1` =第二，`2` =第三，依此类推。

1. 单击&#x200B;**[!UICONTROL Save Config]**。

## 步骤2：在承运人配置中启用免运费

确保完成您计划用于免费配送的每个承运人所需的任何配置。 例如，如果您的[UPS配置](ups.md)已完成，请更新以下设置以启用和配置免费送货。

1. 在&#x200B;_[!UICONTROL Delivery Methods]_&#x200B;配置中，展开&#x200B;**[!UICONTROL UPS]**&#x200B;部分的![扩展选择器](../assets/icon-display-expand.png)。

1. 将&#x200B;**[!UICONTROL Free Method]**&#x200B;设置为`UPS Ground`或您要指定免费送货的其他类型。

1. 若要要求免费送货的最低订单，请将&#x200B;**[!UICONTROL Enable Free Shipping Threshold]**&#x200B;设置为`Enable`。

   如果选择使用最小订单，请为&#x200B;**[!UICONTROL Free Shipping Amount Threshold]**&#x200B;输入所需金额。

1. 单击&#x200B;**[!UICONTROL Save Config]**。

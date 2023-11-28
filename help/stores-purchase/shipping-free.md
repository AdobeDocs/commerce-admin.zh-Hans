---
title: 免运费
description: 了解如何为您的商店设置免费送货选项。
exl-id: 3ce69583-0f7f-4c23-b3e3-7d2502bc1bca
feature: Shipping/Delivery
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 0%

---

# 免运费

_免运费_ 是最有效的促销活动之一。 它可以基于最低购买，也可以设置为 [购物车价格规则](../merchandising-promotions/price-rules-cart.md) 中所有规则的URL值。 如果两者适用于同一顺序，则配置设置优先于购物车规则。

>[!NOTE]
>
>检查您的配送承运人配置，了解免费配送可能需要的任何其他设置。

## 步骤1：配置免费送货

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中，展开 **[!UICONTROL Sales]** 并选择 **[!UICONTROL Delivery Methods]**.

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Free Shipping]** 部分。

   >[!NOTE]
   >
   >如有必要，请首先取消选择 **[!UICONTROL Use system value]** 复选框，以按所述更改以下设置。

1. 设置 **[!UICONTROL Enabled]** 到 `Yes`.

1. 对象 **[!UICONTROL Title]**，输入在结账期间标识免费送货方法的标题和 **[!UICONTROL Method Name]** 描述它。

1. 对象 **[!UICONTROL Minimum Order Amount]**，输入符合免运费条件的最小总值。

   >[!TIP]
   >
   >使用免费送货服务 [表费率](shipping-table-rate.md)，使 _[!UICONTROL Minimum Order Amount]_太高了，根本就没见过。 使用此高值可阻止免费送货生效，除非由价格规则触发。

1. 设置 **[!UICONTROL Include Tax to Amount]**：

   - `Yes`  — 计算最小订单金额时包括税（小计+税 — 折扣）。
   - `No`  — 在计算最小订单金额时不包括税（小计 — 折扣）。

   ![免费送货](../configuration-reference/sales/assets/delivery-methods-free-shipping.png){width="600" zoomable="yes"}

1. 对象 **[!UICONTROL Displayed Error Message]**，输入在免费配送服务不可用时显示的消息。

1. 设置 **[!UICONTROL Ship to Applicable Countries]**：

   - `All Allowed Countries`  — 来自所有客户的客户 [国家/地区](../getting-started/store-details.md#country-options) 在您的商店配置中指定的服务可使用免费送货。

   - `Specific Countries`  — 选择该值后， _[!UICONTROL Ship to Specific Countries]_列表出现。 选择列表中可使用免费送货的每个国家/地区。

1. 设置 **[!UICONTROL Show Method if Not Applicable]**：

   - `Yes`  — 始终显示“免运费”方法，即使不适用。
   - `No`  — 仅在适用的情况下显示“免运费”方法。

1. 对象 **[!UICONTROL Sort Order]**，输入数字，以便在结帐期间确定免费送货在交货方式列表中的位置。

   `0` =第一个， `1` =秒， `2` =第三，依此类推。

1. 单击 **[!UICONTROL Save Config]**.

## 步骤2：在承运人配置中启用免运费

确保完成您计划用于免费配送的每个承运人所需的任何配置。 例如，如果您的 [UPS配置](ups.md) 否则，请更新以下设置以启用和配置免费送货。

1. 在 _[!UICONTROL Delivery Methods]_配置，展开 ![扩展选择器](../assets/icon-display-expand.png) 该&#x200B;**[!UICONTROL UPS]**部分。

1. 设置 **[!UICONTROL Free Method]** 到 `UPS Ground` 或者您要指定免费送货的其他类型。

1. 要要求提供免费配送的最低订单，请设置 **[!UICONTROL Enable Free Shipping Threshold]** 到 `Enable`.

   如果您选择使用最小订单，请输入 **[!UICONTROL Free Shipping Amount Threshold]**.

1. 单击 **[!UICONTROL Save Config]**.

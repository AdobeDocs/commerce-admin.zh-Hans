---
title: 统一费率运费
description: 了解如何为您的商店设置统一费率配送选项。
exl-id: a6874509-a79b-42ab-aa93-d70d18fc33f6
feature: Shipping/Delivery
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '551'
ht-degree: 0%

---

# 统一费率运费

_统一费率_&#x200B;是固定的、预定义的费用，可以按项目或按装运应用。 统一费率是一种简单的运输解决方案，尤其是与某些承运人提供的统一费率包装一起使用时。 启用后，_统一费率_&#x200B;在结账期间显示为选项。 由于未指定特定运营商，因此您可以使用您选择的运营商。

## 设置统一费率运送

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧面板中，展开&#x200B;**[!UICONTROL Sales]**&#x200B;并选择&#x200B;**[!UICONTROL Delivery Methods]**。

1. 展开![扩展选择器](../assets/icon-display-expand.png) **平均速率**&#x200B;部分。

   ![统一费率](../configuration-reference/sales/assets/delivery-methods-flat-rate.png){width="600" zoomable="yes"}

   有关这些配置设置的详细说明，请参阅&#x200B;_配置参考指南_&#x200B;中的[固定速率](../configuration-reference/sales/delivery-methods.md#flat-rate)。

1. 将&#x200B;**[!UICONTROL Enabled]**&#x200B;设置为`Yes`。

   统一税率在购物车的“估计运费和税”分区以及结帐期间的“运费”分区中显示为一个选项。

1. 为统一费率方法输入描述性&#x200B;**[!UICONTROL Title]**。

1. 输入要在购物车中计算出的费率旁边显示的&#x200B;**方法名称**。

   默认方法名称为`Fixed`。 如果您收取手续费，则可以将此文本更改为`Plus Handling`或其他合适的内容。

1. 要说明如何使用统一费率运费，请将&#x200B;**Type**&#x200B;设置为以下项之一：

   - `None` — 禁用付款类型。 “统一费率”选项在购物车中列出，但费率为零，这与免运费相同。
   - `Per Order` — 对整个订单收取单一固定费用。
   - `Per Item` — 对每个项目收取单一统一费率。 比率乘以购物车中的项目数，而不考虑是存在相同项目还是不同项目的多个数量。

1. 输入统一费率配送要收取的&#x200B;**价格**。

1. 根据您的要求配置手续费选项。

   手续费是可选的，显示为添加到运输成本中的额外费用。 如果要包括手续费，请执行以下操作：

   - 对于&#x200B;**计算手续费**，请选择要用于计算手续费的方法：

      - `Fixed`
      - `Percent`

   - 对于&#x200B;**手续费**，根据您选择用于计算金额的方法输入要收取的金额。

     例如，如果费用基于固定费用，则以小数形式输入金额，如`4.90`。 但是，如果手续费基于装运成本的百分比，则按百分比输入金额。 例如，如果您收取运费的6%，则输入值为`6`。

1. 如果需要，请更改&#x200B;**显示的错误消息**。

   此文本框预设了默认消息，但您可以输入在“统一费率传送”不可用时要显示的其它消息。

1. 设置&#x200B;**发货到适用的国家/地区**：

   - `All Allowed Countries` — 来自您商店配置中指定的所有[国家/地区](../getting-started/store-details.md#country-options)的客户都可以使用此交付方法。
   - `Specific Countries` — 选择此选项时，将显示&#x200B;_发送到特定国家/地区_&#x200B;列表。 选择列表中可使用此投放方法的每个国家/地区。

1. 设置&#x200B;**Show方法（如果不适用）**：

   - `Yes` — 始终显示统一费率方法，即使不适用也是如此。
   - `No` — 仅在适用的情况下显示统一费率方法。

1. 对于&#x200B;**[!UICONTROL Sort Order]**，输入一个数字以确定在结帐期间与其他交货方法一起列出统一费率发运时显示的顺序。

   `0` =第一，`1` =第二，`2` =第三，依此类推。

1. 单击&#x200B;**[!UICONTROL Save Config]**。

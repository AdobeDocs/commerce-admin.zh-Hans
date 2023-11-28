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

_统一费率_ 是一种预定义的固定费用，可用于每项物料或每次发运。 统一费率是一种简单的运输解决方案，尤其是与某些承运人提供的统一费率包装一起使用时。 启用时， _统一费率_ 在签出期间显示为选项。 由于未指定特定运营商，因此您可以使用您选择的运营商。

## 设置统一费率运送

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中，展开 **[!UICONTROL Sales]** 并选择 **[!UICONTROL Delivery Methods]**.

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **统一费率** 部分。

   ![统一费率](../configuration-reference/sales/assets/delivery-methods-flat-rate.png){width="600" zoomable="yes"}

   有关每个配置设置的详细说明，请参阅 [统一费率](../configuration-reference/sales/delivery-methods.md#flat-rate) 在 _配置参考指南_.

1. 设置 **[!UICONTROL Enabled]** 到 `Yes`.

   统一税率在购物车的“估计运费和税”分区以及结帐期间的“运费”分区中显示为一个选项。

1. 输入描述性 **[!UICONTROL Title]** 对于“统一速率”方法。

1. 输入 **方法名称** 显示在购物车中计算的费率旁边。

   默认方法名称为 `Fixed`. 如果您收取手续费，则可以将此文本更改为 `Plus Handling`或其他适当的内容。

1. 要描述如何使用统一费率配送，请设置 **类型** 更改为以下任一项：

   - `None`  — 禁用付款类型。 “统一费率”选项在购物车中列出，但费率为零，这与免运费相同。
   - `Per Order`  — 对整个订单收取单一统一费率。
   - `Per Item`  — 对每个项目收取单一统一费率。 比率乘以购物车中的项目数，而不考虑是存在相同项目还是不同项目的多个数量。

1. 输入 **价格** 要按固定费率收取运费。

1. 根据您的要求配置手续费选项。

   手续费是可选的，显示为添加到运输成本中的额外费用。 如果要包括手续费，请执行以下操作：

   - 对象 **计算手续费**，选择要用于计算手续费的方法：

      - `Fixed`
      - `Percent`

   - 对象 **手续费**，根据您选择用于计算金额的方法，输入要收取的金额。

     例如，如果费用基于固定费用，则以小数形式输入金额，如 `4.90`. 但是，如果手续费基于装运成本的百分比，则按百分比输入金额。 例如，如果要收取发运成本的6%，则输入值为 `6`.

1. 如果需要，请更改 **显示的错误消息**.

   此文本框预设了默认消息，但您可以输入在“统一费率传送”不可用时要显示的其它消息。

1. 设置 **发运至适用的国家/地区**：

   - `All Allowed Countries`  — 来自所有客户的客户 [国家/地区](../getting-started/store-details.md#country-options) 在商店配置中指定的可使用此投放方法。
   - `Specific Countries`  — 选择此选项时， _发运至特定国家/地区_ 列表出现。 选择列表中可使用此投放方法的每个国家/地区。

1. 设置 **显示方法（如果不适用）**：

   - `Yes`  — 始终显示“统一费率”方法，即使不适用。
   - `No`  — 仅在适用的情况下显示“统一费率”方法。

1. 对象 **[!UICONTROL Sort Order]**，请输入一个数字以确定在结帐期间与其他交货方法一起列出统一费率发运时的显示顺序。

   `0` =第一个， `1` =秒， `2` =第三，依此类推。

1. 单击 **[!UICONTROL Save Config]**.

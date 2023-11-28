---
title: 银行转帐
description: 了解如何将银行转帐设置为商店的离线付款方式。
exl-id: 34b2163c-2edd-4741-b002-3d8fb561fc78
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 0%

---

# 银行转帐

Adobe Commerce和Magento Open Source允许您接受从客户银行帐户转账并存入您的商家银行帐户的付款。

**_要配置银行转帐付款，请执行以下操作：_**

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中，展开 **[!UICONTROL Sales]** 并选择 **[!UICONTROL Payment Methods]**.

1. 下 _其他支付方式_，展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Bank Transfer Payment]** 部分。

   ![银行转帐付款](../configuration-reference/sales/assets/payment-methods-bank-transfer-payment.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >如有必要，请先清除 **[!UICONTROL Use system value]** 复选框以更改这些设置。

1. 要激活银行转帐，请设置 **[!UICONTROL Enabled]** 到 `Yes`.

1. 对象 **[!UICONTROL Title]**，输入在结账时标识银行转帐支付方式的标题。

1. 设置 **[!UICONTROL New Order Status]** 到 `Pending` 直到付款获得批准。

1. 设置 **[!UICONTROL Payment from Applicable Countries]** 更改为以下任一项：

   - `All Allowed Countries`  — 来自所有客户的客户 [国家/地区](../getting-started/store-details.md#country-options) 在商店配置中指定的可使用此付款方式。

   - `Specific Countries`  — 选择此选项后， _[!UICONTROL Payment from Specific Countries]_列表出现。 要选择多个国家/地区，请按住Ctrl键(PC)或Command键(Mac)并单击每个选项。

1. 输入 **[!UICONTROL Instructions]** 客户必须遵循这些规则才能设置银行转帐。

   根据银行所在的国家/地区和银行要求，您可以包括以下信息：

   - 银行帐户名称
   - 银行帐号
   - 银行代号
   - 银行名称
   - 银行地址

1. 设置 **[!UICONTROL Minimum Order Total]** 和 **[!UICONTROL Maximum Order Total]** 付款方式所需的金额。

   >[!NOTE]
   >
   >如果合计在最小或最大合计值之间，或者与最小或最大合计值完全匹配，则订单合格。

1. 对象 **[!UICONTROL Sort Order]**，请输入一个数字，以确定此项目在结账时显示的付款方式列表中的位置。

   此数字相对于其他支付方式。 (`0` =第一个， `1` =秒， `2` =第三，依此类推。)

1. 完成后，单击 **[!UICONTROL Save Config]**.

---
title: 应用商店积分
description: 商店管理员可将商店点数申请至购买。
exl-id: 97b6b206-71db-435c-8736-a781437bb0b4
feature: Customers, Storefront
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '321'
ht-degree: 0%

---

# 应用商店积分

{{ee-feature}}

商店管理员可以查看客户帐户的信用余额和历史记录，还可以将商店信用应用于购买。

![客户信用余额和历史记录](assets/store-credit-balance-history.png){width="600" zoomable="yes"}

## 查看贷方余额

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. 在网格中查找客户。

1. 在 _操作_ 列，单击 **[!UICONTROL Edit]**.

1. 滚动 _[!UICONTROL Customer View]_页面并查看&#x200B;**[!UICONTROL Store Credit Balance]**在底部。

![商店贷方余额](assets/store-credit-balance.png){width="600" zoomable="yes"}

## 更新商店贷方余额

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Customers]** > _操作_ > **[!UICONTROL All Customers]**.

1. 在网格中查找客户。

1. 在 _操作_ 列，单击 **[!UICONTROL Edit]**.

1. 在左侧面板中，选择 **[!UICONTROL Store Credit]**.

1. 选择要与余额关联的网站（店面）。

1. 对象 **[!UICONTROL Update Balance]**&#x200B;中，输入新值。

1. 要通知客户余额更新，请选择 **[!UICONTROL Notify Customer by Email]** 复选框，然后从中选择商店视图 **[!UICONTROL Send Email Notification From the Following Store View]**.

1. 输入 **[!UICONTROL Comment]** 有关更改的信息。

1. 更新完成后，单击 **[!UICONTROL Save and Continue Edit]** 或 **[!UICONTROL Save Customer]**.

更新的余额应显示在 **[!UICONTROL Balance History]**.

## 以商店管理员身份将贷方余额应用于订单

作为商店管理员，您可以代表客户执行各种操作，包括提交订单。 当您 [创建订单](../stores-purchase/customer-account-create-order.md)，则可以申请应付给客户的商店贷方余额。 可用余额显示在 _付款和送货信息_ 部分。 选择 **[!UICONTROL Use Store Credit]** 复选框，以应用余额；如果订单总额较小，则应用余额的一部分。

![将商店贷方余额应用于订单](assets/store-credit-apply.png){width="500" zoomable="yes"}

## 在结账期间应用商店积分

如果地点有贷方余额，客户可以在将订单放在店面之前将商店贷方应用于订单余额。

1. 客户查看可用商店贷项的金额。

   时段 _审核与支付_ 步骤，可用数量显示在 _[!UICONTROL Store Credit]_.

1. 要将金额应用于订单，请单击 **[!UICONTROL Use Store Credit]**.

   >[!INFO]
   >
   >订单总额会重新计算，并且应用的商店积分金额会显示在 _[!UICONTROL Order Summary]_.

   ![存储应用于订单的贷方余额](assets/store-credit-checkout.png){width="700" zoomable="yes"}

1. 准备就绪后，单击 **[!UICONTROL Place Order]**.

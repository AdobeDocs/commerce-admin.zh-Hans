---
title: 即时购买
description: 了解即时购买，以及它如何快速结帐给注册的客户帐户。
exl-id: f299f364-d7e3-4567-8c7b-955129011a19
feature: Checkout
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 0%

---

# 即时购买

_即时购买_ 允许客户使用保存在其帐户中的信息来加速结账过程。 启用后， _即时购买_ 按钮显示在页面上 _添加到购物车_ 按钮，用于符合要求的客户。

![显示即时购买选项的产品页面](./assets/storefront-checkout-instant-purchase.png){width="700" zoomable="yes"}

## 客户要求

- 客户是 [已登录](../customers/customer-sign-in.md) 到他们的账户里。

- 客户帐户具有 [默认帐单和送货地址](../customers/account-dashboard-address-book.md).

- 至少一个 [配送方式](delivery.md) 适用于默认送货地址中指定的国家/地区。

- 客户帐户具有 [存储付款](../stores-purchase/stored-payment-methods.md) 启用了保险库的方法。

  以下支付方式可用于提供对已保存信用卡信息的安全访问：

   - [Braintree信用卡](braintree.md) (如果启用了3D Secure，则即时购买不能与Braintree信用卡一起使用。)
   - [已启用PayPal的Braintree](braintree.md)
   - [PayPal Payflow Pro](paypal-payflow-pro.md)

## 店面即时购买

1. 在店面，客户转到要购买项目的产品页面。

1. 选择所需的选项并单击 **[!UICONTROL Instant Purchase]**.

   ![用于确认即时购买的确认对话框](./assets/storefront-checkout-instant-purchase-confirmation.png){width="500" zoomable="yes"}

1. 查看 **[!UICONTROL Instant Purchase Confirmation]** 信息和点击次数 **[!UICONTROL OK]** 以完成交易。

   产品页顶部将显示确认消息和订单编号。

## 配置即时购买

### 步骤1：打开配置页面

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

### 步骤2：配置支付方式保管库

您可以将即时购买功能与Adobe Commerce和Magento Open Source的Braintree或支付服务结合使用。 必须启用保险存储，购物者才能使用“即时购买”功能。

了解如何配置支付方式并为Braintree或支付服务启用保险存储：

- [Braintree](braintree.md)
- [Payment Service文档](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/guide-overview.html)

### 步骤3：启用即时购买

1. 在左侧面板中的 _[!UICONTROL Sales]_部分，选择&#x200B;**[!UICONTROL Sales]**.

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Instant Purchase]** 部分。

1. 如果此项更改针对的是特定的商店视图， [选择商店视图](../configuration-reference/scope-change.md#set-the-scope) 配置适用的位置。

   出现提示时，单击 **[!UICONTROL OK]** 以继续。

1. 设置 **[!UICONTROL Enabled]** 到 `Yes`.

1. 输入 **[!UICONTROL Button Text]** 要显示在按钮上的内容。

   可以更改每个商店视图或语言的按钮文本。 默认情况下，按钮文本为 `Instant Purchase`.

   ![配置 — 即时购买选项](../configuration-reference/sales/assets/sales-instant-purchase.png){width="600" zoomable="yes"}

   有关每个配置设置的详细说明，请参阅 [即时购买](../configuration-reference/sales/sales.md#instant-purchase) 在 _配置参考指南_.

1. 单击 **[!UICONTROL Save Config]**.

1. 提示更新缓存时，单击 **[!UICONTROL Cache Management]** 并按照说明刷新缓存。

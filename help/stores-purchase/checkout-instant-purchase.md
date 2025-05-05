---
title: 即时购买
description: 了解即时购买，以及它如何快速结帐给注册的客户帐户。
exl-id: f299f364-d7e3-4567-8c7b-955129011a19
feature: Checkout
source-git-commit: 5da244a548b15863fe31b5df8b509f8e63df27c2
workflow-type: tm+mt
source-wordcount: '396'
ht-degree: 0%

---

# 即时购买

_即时购买_&#x200B;允许客户使用保存在其帐户中的信息来加速结帐过程。 启用后，_即时购买_&#x200B;按钮会显示在产品页面上&#x200B;_添加到购物车_&#x200B;按钮的下方，供符合要求的客户使用。

显示![包含“即时购买”选项的产品页面](./assets/storefront-checkout-instant-purchase.png){width="700" zoomable="yes"}

## 客户要求

- 客户已[登录其帐户](../customers/customer-sign-in.md)。

- 客户帐户具有[默认帐单和送货地址](../customers/account-dashboard-address-book.md)。

- 在默认送货地址中指定的国家/地区至少有一个[送货方法](delivery.md)可用。

- 客户帐户具有已启用保管库的[存储付款](../stores-purchase/stored-payment-methods.md)方法。

  以下支付方式可用于提供对已保存信用卡信息的安全访问：

   - [Braintree信用卡](braintree.md) (如果启用了3D Secure，即时购买不能与Braintree信用卡一起使用。)
   - [启用了PayPal的Braintree](braintree.md)
   - [PayPal Payflow Pro](paypal-payflow-pro.md)

## 店面即时购买

1. 在店面，客户转到要购买项目的产品页面。

1. 选择所需的选项并单击&#x200B;**[!UICONTROL Instant Purchase]**。

   ![用于确认即时购买的确认对话框](./assets/storefront-checkout-instant-purchase-confirmation.png){width="500" zoomable="yes"}

1. 查看&#x200B;**[!UICONTROL Instant Purchase Confirmation]**&#x200B;信息并单击&#x200B;**[!UICONTROL OK]**&#x200B;以完成交易。

   产品页顶部将显示确认消息和订单编号。

## 配置即时购买

### 步骤1：打开配置页面

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

### 步骤2：配置支付方式保管库

您可以将即时购买功能与Braintree结合使用，也可以将支付服务用于Adobe Commerce和Magento Open Source。 必须启用保险存储，购物者才能使用“即时购买”功能。

了解如何为Braintree或支付服务配置支付方式并启用保险存储：

- [Braintree](braintree.md)
- [付款服务文档](https://experienceleague.adobe.com/docs/commerce/payment-services/guide-overview.html?lang=zh-Hans)

### 步骤3：启用即时购买

1. 在左侧面板的&#x200B;_[!UICONTROL Sales]_&#x200B;部分下，选择&#x200B;**[!UICONTROL Sales]**。

1. 展开&#x200B;**[!UICONTROL Instant Purchase]**&#x200B;部分的![扩展选择器](../assets/icon-display-expand.png)。

1. 如果此更改针对特定的存储视图，请[选择应用配置的存储视图](../configuration-reference/scope-change.md#set-the-scope)。

   出现提示时，单击&#x200B;**[!UICONTROL OK]**&#x200B;继续。

1. 将&#x200B;**[!UICONTROL Enabled]**&#x200B;设置为`Yes`。

1. 输入要显示在按钮上的&#x200B;**[!UICONTROL Button Text]**。

   可以更改每个商店视图或语言的按钮文本。 默认情况下，按钮文本为`Instant Purchase`。

   ![配置 — 即时购买选项](../configuration-reference/sales/assets/sales-instant-purchase.png){width="600" zoomable="yes"}

   有关这些配置设置的详细说明，请参阅&#x200B;_配置参考指南_&#x200B;中的[即时购买](../configuration-reference/sales/sales.md#instant-purchase)。

1. 单击&#x200B;**[!UICONTROL Save Config]**。

1. 提示更新缓存时，单击系统消息中的&#x200B;**[!UICONTROL Cache Management]**，然后按照说明刷新缓存。

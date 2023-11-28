---
title: 来自Adobe的扩展
description: 查看由Adobe发布的Adobe Commerce扩展和Magento Open Source相关信息。
exl-id: 86338edc-c32a-41c8-9594-6aec26f53ac6
feature: Extensions
source-git-commit: c22ad5c3220f14588131d6b29a88dab3c5347681
workflow-type: tm+mt
source-wordcount: '1026'
ht-degree: 0%

---

# 来自Adobe的扩展

本主题介绍由Adobe发布的Adobe Commerce扩展和Magento Open Source扩展的相关信息。 扩展为管理员和店面添加了功能、功能、服务和集成。 其中一些扩展是通过Magento Open Source社区贡献开发的。 某些扩展需要单独安装，而其他扩展则默认安装。

## 已安装的扩展

有一些扩展会自动与Adobe Commerce或Magento Open Source一起安装。

### [!DNL Inventory Management]

[!DNL Commerce] [[!DNL Inventory Management]](../inventory-management/introduction.md) 通过并发结账保护和发货匹配算法，跨一个或多个地点和销售渠道提供增强的库存和发货管理。 跟踪库存数量，向客户提供准确的可销售库存量，并根据建议或人工选择发运以控制整个库存。 按源和产品全局配置管理设置。

>[!NOTE]
>
>此扩展是作为 [[!DNL Inventory Management]](https://github.com/magento/inventory) （以前称为MSI）项目。

[!DNL Inventory Management] 安装，默认启用所有功能。 无需执行其他步骤即可启用这些清单功能。 欲知关于 [!DNL Inventory Management] 功能，请参见 [[!DNL Inventory Management] 用户指南](../inventory-management/guide-overview.md).

### Braintree

PayPal和Gene Commerce共同开发了Commerce 2.4.x商店的官方Braintree扩展。 这些更新包括了PayLater选项，改善了旨在促进转化的结账体验，这些选项可在购物和结账期间自动向消费者显示相关的PayLater消息和按钮。

默认情况下，会安装此扩展，但需要 [Braintree帐户](https://www.braintreepayments.com/) 要为您的存储启用的管理员中的和配置。 要确定使用Braintree处理事务处理时适用的费用，请检查 [Braintree定价](https://www.braintreepayments.com/braintree-pricing).

有关管理员中Braintree配置的信息，请参阅 [Braintree](../stores-purchase/braintree.md) 中的主题 _销售和购买体验指南_.

### Google reCAPTCHA

Google reCAPTCHA与标准CAPTCHA相比，为店面和管理员UI提供了更高级别的安全性，并让您能够：

- 验证客户何时创建帐户、检索密码、登录到其帐户或联系您的公司。
- 增强管理员用户登录时的安全性。

它可以减少输入验证码时可能的用户错误，并鼓励在结账期间不添加障碍的购物车转换。 [启用和配置reCAPTCHA](../systems/security-google-recaptcha.md) 使用不可见或交互式检查来增强对的安全访问 [!DNL Commerce] 管理员和店面。

### 双重身份验证

此 [!DNL Commerce] 管理员提供对您的商店、订单和客户数据的所有访问权限。 [双重身份验证](../systems/security-two-factor-authentication.md) （2FA或TFA）除了标准登录名和密码之外，还需要其他身份验证才能访问 [!DNL Commerce] 管理所有设备。 该扩展支持多个身份验证器，包括Google Authenticator、Authy、 [!DNL Duo]和U2F键。 此身份验证仅适用于管理员用户。 它不适用于店面客户。

默认情况下，将启用这些功能。 每个Admin用户必须安装和配置一个受支持的身份验证器。

>[!NOTE]
>
>为管理员启用了Identity Management服务(IMS)Adobe身份验证的Adobe Commerce商店已禁用本机Commerce 2FA。 使用Adobe凭据登录到管理员的用户不需要重新验证许多管理员任务。 当管理员用户登录到其当前会话时，身份验证由Adobe IMS处理。 请参阅 [AdobeIdentity Management服务(IMS)集成概述](./adobe-ims-integration-overview.md).

## 要添加扩展

此 [[!DNL Commerce Marketplace]](https://marketplace.magento.com/) 是用于扩展的应用程序和服务的全球电子商务资源 [!DNL Commerce] 具有强大新特性和功能的解决方案。 Adobe通过以下方式发布多个扩展： [!DNL Marketplace] 您可在Adobe Commerce或Magento Open Source存储中安装和配置的插件，以提供增强的集成和功能。

### [!DNL Live Search]

![Adobe Commerce](../assets/adobe-logo.svg) 仅限Adobe Commerce

此 [!DNL Live Search] 该扩展可将您的商店连接到Live Search服务，该服务是Adobe Commerce的一个免费搜索平台，可无缝地使销售商能够为客户提供人工智能增强的搜索体验。 Intelligent Faceting采用Adobe的人工智能Adobe Sensei构建，通过删除有关分面/过滤的手动操作，帮助商家事半功倍。

请参阅 [Live Search用户指南](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/guide-overview.html) 以了解更多信息。

### [!DNL Product Recommendations]

![Adobe Commerce](../assets/adobe-logo.svg) 仅限Adobe Commerce

此 [!DNL Product Recommendations] 扩展可将您的商店连接到Product Recommendations服务，这是一个功能强大的营销工具，可用于提高转化率、收入和参与度。 [!DNL Product Recommendations] 由Adobe Commerce构建，并由经过战场考验的人工智能Adobe Sensei驱动，因此您可以放心地推动参与和转化。 此功能免除了向每位购物者提供相关产品推荐所需的手动工作。

请参阅 [[!DNL Product Recommendations] 用户指南](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/guide-overview.html?lang=en) 以了解更多信息。

### [!DNL Catalog Service]

此 [!DNL Catalog Service] 使您能够为客户提供优化的产品体验，同时提高性能、改进可扩展性和提高转化率。 请参阅 [[!DNL Catalog Service] 用户指南](https://experienceleague.adobe.com/docs/commerce-merchant-services/catalog-service/guide-overview.html) 以了解更多信息。

### [!DNL Payment Services]

[!DNL Payment services] Adobe Commerce和Magento Open Source是完全集成的支付解决方案，它简化了管理支付的过程，并为您的客户提供按其方式付款的机会。 在Adobe Commerce Admin中安全地协调所有支付和交易数据 — 允许您在一个地方管理订单和支付，同时实现无缝结账。 请参阅 [[!DNL Payment Services] 用户指南](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/guide-overview.html) 以了解更多信息。

### [!DNL Quick Checkout]

[!DNL Quick Checkout] ，Adobe Commerce可提供无缝的结账体验，旨在将一次性访客购物者转化为忠诚的帐户持有者。
请参阅 [[!DNL Quick Checkout] 用户指南](https://experienceleague.adobe.com/docs/commerce-merchant-services/quick-checkout/overview.html) 以了解更多信息。

### [!DNL Store Fulfillment]

适用于Adobe Commerce和Magento Open Source的商店履行功能可提供卓越的在线购买功能、店内取货(BOPIS)客户体验，并通过移动设备提供全面的履行工作流程，从而最大限度地提高员工的工作效率。 请参阅 [[!DNL Store Fulfillment] 用户指南](https://experienceleague.adobe.com/docs/commerce-merchant-services/store-fulfillment/guide-overview.html) 以了解更多信息。

### [!DNL Amazon Sales Channel]

此 [!DNL Amazon Sales Channel] for Adobe Commerce允许您将Amazon Seller Central列表数据库与 [!DNL Commerce] 在Commerce Admin中编入产品目录并管理Amazon列表和销售情况。 请参阅 [[!DNL Amazon Sales] 指南用户指南](https://experienceleague.adobe.com/docs/commerce-channels/amazon/guide-overview.html) 以了解更多信息。

### [!DNL Channel Manager]

[!DNL Channel Manager] 通过将Adobe Commerce或Magento Open Source产品目录与Walmart Marketplace集成，您可以提高销售额、吸引新客户、简化运营并节省时间。 安装和配置扩展后，您的员工可以从 [!DNL Commerce Admin]. 请参阅 [[!DNL Channel Manager] 用户指南](https://experienceleague.adobe.com/docs/commerce-channels/channel-manager/guide-overview.html) 以了解更多信息。

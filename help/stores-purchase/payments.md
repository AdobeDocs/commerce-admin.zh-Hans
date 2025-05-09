---
title: 付款概览
description: 了解Adobe Commerce和Magento Open Source本机支持的支付方法和服务。
exl-id: 474bf6df-96e2-4db3-ad3c-1804b5de33b0
feature: Payments
source-git-commit: 489c72652693a15ffe1c745277bbaa9da084dcba
workflow-type: tm+mt
source-wordcount: '753'
ht-degree: 0%

---

# 付款概览

Adobe Commerce和Magento Open Source支持各种支付方法和服务。 这包括多种离线支付方式，包括支票或汇票支付和货到付款(COD)。 此外，还有许多在线支付解决方案和网关的本机集成，包括Braintree作为供应商捆绑开发的扩展。

>[!TIP]
>
>适用于Adobe Commerce和Magento Open Source的Payment Services提供了一个可立即投入使用的自助服务解决方案，包括沙盒测试和简单的设置，用于提供强大而安全的支付处理。 要了解有关此功能强大的工具集以及它如何为您提供insight和控制您为购买者创建最佳体验所需的更多信息，请参阅[Payment Services用户指南](https://experienceleague.adobe.com/docs/commerce/payment-services/guide-overview.html?lang=zh-Hans)。 这是[Adobe Commerce as a Cloud Service](https://experienceleague.adobe.com/zh-hans/docs/commerce/cloud-service/overview)中的默认支付解决方案。

>[!NOTE]
>
>查看[PCI合规性准则](../getting-started/compliance-pci.md)，该准则概括了支付卡行业(PCI)为接受通过信用卡通过Internet付款的企业设定的要求。

## 2.4中的更改

仅[!BADGE PaaS]{type=Informative url="https://experienceleague.adobe.com/zh-hans/docs/commerce/user-guides/product-solutions" tooltip="仅适用于云项目(Adobe管理的PaaS基础架构)和内部部署项目上的Adobe Commerce 。"}

2.4.x版本中删除了一些支付集成和捆绑的扩展，并将其移至Commerce Marketplace。 您可以在[Commerce Marketplace](https://marketplace.magento.com/extensions/payments-security.html){:target="_blank"}中找到最新的官方付款集成扩展。

- **Amazon Pay**&#x200B;和&#x200B;**Klarna**： Adobe Commerce和Magento Open Source版本2.4.0到2.4.3包含这些供应商开发的扩展。 从2.4.4版本开始，核心版本不再捆绑这些扩展，必须从Commerce Marketplace安装和更新这些扩展。 通过Marketplace，还可以访问扩展开发人员提供的当前文档。

  如果已启用并配置其中任一捆绑扩展，则必须在升级2.4.4过程中更新您的composer.json文件并管理以后的扩展更新。 有关详细信息，请参阅&#x200B;_升级指南_&#x200B;中的[升级模块](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html?lang=zh-Hans)。

- **Worldpay**、**Eway**、**CyberSource**&#x200B;和&#x200B;**Authorize.Net**：有关从这些付款集成进行安全过渡的详细信息，请参阅[DevBlog](https://community.magento.com/t5/Magento-DevBlog/Deprecation-of-Magento-core-payment-integrations/ba-p/426445){:target="_blank"}。

## 离线支付方式

Adobe Commerce和Magento Open Source包括多种内置的离线支付方式，它们不需要第三方支付处理公司的服务：

- [零小计签出](zero-subtotal-checkout.md)
- [货到付款](cash-on-delivery.md)
- [银行转帐付款](bank-transfer.md)
- [支票/汇票](check-money-order.md)
- [采购订单](purchase-order.md)
- [帐户付款](../b2b/enable-basic-features.md#configure-payment-on-account) ![Adobe Commerce B2B](../assets/b2b.svg)(适用于Adobe Commerce B2B)

## 在线支付方式

Adobe Commerce和Magento Open Source支持在世界各地提供商户服务的众多支付解决方案。 与将控制权转移到另一个地点以完成交易的支付解决方案不同，支付网关使您能够直接从您的商店接受信用卡支付，而无需客户离开您的地点。

### 推荐的解决方案

- [付款服务](https://experienceleague.adobe.com/docs/commerce/payment-services/guide-overview.html?lang=zh-Hans)
- 仅[!BADGE PaaS]{type=Informative url="https://experienceleague.adobe.com/zh-hans/docs/commerce/user-guides/product-solutions" tooltip="仅适用于云项目(Adobe管理的PaaS基础架构)和内部部署项目上的Adobe Commerce 。"} [PayPal Express签出](paypal-express-checkout.md)
- 仅[!BADGE PaaS]{type=Informative url="https://experienceleague.adobe.com/zh-hans/docs/commerce/user-guides/product-solutions" tooltip="仅适用于云项目(Adobe管理的PaaS基础架构)和内部部署项目上的Adobe Commerce 。"} [Braintree](braintree.md)

### 其他PayPal支付解决方案

仅[!BADGE PaaS]{type=Informative url="https://experienceleague.adobe.com/zh-hans/docs/commerce/user-guides/product-solutions" tooltip="仅适用于云项目(Adobe管理的PaaS基础架构)和内部部署项目上的Adobe Commerce 。"}

有关PayPal付款方式选项的更多信息，请参阅[PayPal付款解决方案](paypal.md)。

#### 多功能PayPal解决方案

仅[!BADGE PaaS]{type=Informative url="https://experienceleague.adobe.com/zh-hans/docs/commerce/user-guides/product-solutions" tooltip="仅适用于云项目(Adobe管理的PaaS基础架构)和内部部署项目上的Adobe Commerce 。"}

- [PayPal支付高级](paypal-payments-advanced.md)
- [PayPal Payments Pro](paypal-payments-pro.md)
- [PayPal支付标准](paypal-payments-standard.md)

#### PayPal支付网关

仅[!BADGE PaaS]{type=Informative url="https://experienceleague.adobe.com/zh-hans/docs/commerce/user-guides/product-solutions" tooltip="仅适用于云项目(Adobe管理的PaaS基础架构)和内部部署项目上的Adobe Commerce 。"}

- [PayPal Payflow Pro](paypal-payflow-pro.md)
- [PayPal Payflow链接](paypal-payflow-link.md)

## 欺诈防护

仅[!BADGE PaaS]{type=Informative url="https://experienceleague.adobe.com/zh-hans/docs/commerce/user-guides/product-solutions" tooltip="仅适用于云项目(Adobe管理的PaaS基础架构)和内部部署项目上的Adobe Commerce 。"}

欺诈保护服务和过滤器会在处理交易之前检查已提交的订单，以检测欺诈性订单并保护您免于费用退回。 Adobe Commerce和Magento Open Source支持以下防欺诈解决方案：

- [PayPal欺诈管理过滤器](paypal.md#paypal-fraud-management-filters)

- [市场上的欺诈保护解决方案][1]

>[!NOTE]
>
>为了支持安全合规性更新，从2.4.0版本开始，从Commerce中删除了显着防欺诈功能。 如果您在2.3.x或以前的版本中使用了Signifyd集成，建议您过渡到[Signifyd欺诈和按存储容量使用计费保护扩展](https://marketplace.magento.com/signifyd-module-connect.html){:target="_blank"}。 请确保根据供应商指南维护扩展的更新。

## 资源疑难解答

仅[!BADGE PaaS]{type=Informative url="https://experienceleague.adobe.com/zh-hans/docs/commerce/user-guides/product-solutions" tooltip="仅适用于云项目(Adobe管理的PaaS基础架构)和内部部署项目上的Adobe Commerce 。"}

有关解决付款问题的帮助，请参阅[支持知识库](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/overview.html?lang=zh-Hans)。

[1]: https://marketplace.magento.com/catalogsearch/result?q=fraud%20protection

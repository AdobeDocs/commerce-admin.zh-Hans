---
title: 付款概览
description: 了解Adobe Commerce和Magento Open Source本机支持的支付方法和服务。
exl-id: 474bf6df-96e2-4db3-ad3c-1804b5de33b0
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '647'
ht-degree: 0%

---

# 付款概览

Adobe Commerce和Magento Open Source支持各种支付方法和服务，您可以提供这些方法和服务，以便更轻松地结账和为客户提供方便。 此列表包括多种离线支付方式，包括支票或汇票支付和货到付款(COD)。 此外，还有许多在线支付解决方案和网关的本机集成，包括作为供应商开发的捆绑扩展的Braintree。

>[!TIP]
>
>适用于Adobe Commerce和Magento Open Source的Payment Services提供了一个可立即投入使用的自助服务解决方案，包括沙盒测试和简单的设置，用于提供强大而安全的支付处理。 要详细了解这个功能强大的工具集以及它如何为您提供所需的洞察信息和控制，以便为买家创造最佳体验，请参阅 [Payment Services用户指南](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/guide-overview.html).

>[!NOTE]
>
>查看 [PCI合规性指南](../getting-started/compliance-pci.md) 该法规概述了支付卡行业(PCI)对通过互联网接受信用卡付款的企业提出的要求。

## 2.4中的更改

2.4.x版本中删除了一些支付集成和捆绑的扩展，并将其移至Commerce Marketplace。 您可以在以下位置找到最新的官方支付集成扩展： [Commerce Marketplace](https://marketplace.magento.com/extensions/payments-security.html){：target=&quot;_blank&quot;}.

- **Amazon Pay** 和 **克拉尔纳**：Adobe Commerce和Magento Open Source版本2.4.0到2.4.3中包含这些供应商开发的扩展。 从2.4.4版本开始，核心版本不再捆绑这些扩展，必须从Commerce Marketplace安装和更新这些扩展。 通过Marketplace，还可以访问扩展开发人员提供的当前文档。

  如果已启用并配置其中任一捆绑扩展，则必须在升级2.4.4过程中更新您的composer.json文件并管理以后的扩展更新。 请参阅 [升级模块](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html) 在 _升级指南_ 以了解更多信息。

- **Worldpay**， **Eway**， **网络资源**、和 **Authorize.Net**：有关从这些支付集成进行安全过渡的详细信息，请参阅 [DevBlog](https://community.magento.com/t5/Magento-DevBlog/Deprecation-of-Magento-core-payment-integrations/ba-p/426445){：target=&quot;_blank&quot;}.

## 离线支付方式

Adobe Commerce和Magento Open Source包括多种内置的离线支付方式，它们不需要第三方支付处理公司的服务：

- [零小计签出](zero-subtotal-checkout.md)
- [货到付款](cash-on-delivery.md)
- [银行转帐付款](bank-transfer.md)
- [支票/汇票](check-money-order.md)
- [采购订单](purchase-order.md)
- [分期付款](../b2b/enable-basic-features.md#configure-payment-on-account) ![适用于Adobe Commerce的B2B](../assets/b2b.svg) (适用于Adobe Commerce的B2B中提供)

## 在线支付方式

Adobe Commerce和Magento Open Source支持在世界各地提供商家服务的众多支付解决方案。 与将控制权转移到另一个地点以完成交易的支付解决方案不同，支付网关使您能够直接从您的商店接受信用卡支付，而无需客户离开您的地点。

### 推荐的解决方案

- [支付服务](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/guide-overview.html)
- [PayPal Express签出](paypal-express-checkout.md)
- [Braintree](braintree.md)

### 其他PayPal支付解决方案

请参阅 [PayPal支付解决方案](paypal.md) 有关PayPal支付方式选项的更多信息。

#### 多功能PayPal解决方案

- [PayPal支付高级](paypal-payments-advanced.md)
- [PayPal Payments Pro](paypal-payments-pro.md)
- [PayPal支付标准](paypal-payments-standard.md)

#### PayPal支付网关

- [PayPal Payflow Pro](paypal-payflow-pro.md)
- [PayPal Payflow链接](paypal-payflow-link.md)

## 欺诈防护

欺诈保护服务和过滤器会在处理交易之前检查已提交的订单，以检测欺诈性订单并保护您免于费用退回。 Adobe Commerce和Magento Open Source支持以下防欺诈解决方案：

- [PayPal欺诈管理过滤器](paypal.md#paypal-fraud-management-filters)

- [Marketplace上的防欺诈解决方案][1]

>[!NOTE]
>
>为了支持安全合规性更新，从2.4.0版本开始，从Commerce中删除了显着欺诈防护。 如果您已在2.3.x或之前的版本中使用Signifyd集成，建议您转换为 [显着的欺诈和按存储容量使用计费保护扩展](https://marketplace.magento.com/signifyd-module-connect.html){：target=&quot;_blank&quot;}. 请确保根据供应商指南维护扩展的更新。

## 资源疑难解答

如需排查付款问题的帮助，请参阅 [支持知识库](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/overview.html?lang=en).

[1]: https://marketplace.magento.com/catalogsearch/result?q=fraud%20protection

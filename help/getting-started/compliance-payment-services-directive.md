---
title: PSD2合规性
description: 了解可能影响您商店的《支付服务指令》(PSD2)的要求。
exl-id: efe94cac-a170-48df-88cf-36019ca52951
feature: Compliance
source-git-commit: 3ff5807fd0a3ebf2e9d4f9c085852dd7777a1103
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 0%

---

# PSD2合规性

从2019年9月14日开始，欧盟要求欧盟和英国的所有商户遵守支付服务指令(PSD2)的[强客户身份验证](https://www.cardinalcommerce.com/content-hub/mandates/psd2-sca/understanding-psd2-sca) (SCA)要求。 鼓励所有其他国家的商家遵守PSD2作为最佳做法。

>[!NOTE]
>
>本主题仅供参考，不应理解为法律建议。 要确定您的企业是否以及如何遵守任何法律义务，请咨询您的法律顾问。

强客户身份验证是PSD2的关键组件，它需要以下两项条件：

- 只有客户才有的东西（密码或PIN）
- 只有客户知道的事情（通过电话或密钥库生成的唯一安全令牌）
- 只有客户才有的东西（生物特征认证，例如指纹或面部识别）

欧洲银行可能会拒绝不符合要求的支付。 但是，仍可接受低风险和低价值交易，以及定期订阅中的后续付款。

由于此重大更改并确保客户付款不被拒绝，Adobe为原生[!DNL Commerce]付款集成引入了以下更改和建议。

| 付款方式 | 合规性要求 |
|--- |--- |
| [PayPal](../stores-purchase/paypal.md) | 对于大多数PayPal解决方案，无需采取任何操作即可符合PSD2，因为这些要求由PayPal处理。 有关特定解决方案的信息，请参阅每个PayPal主题顶部的说明。 |
| [Braintree](../stores-purchase/braintree.md) | 从2.4.0中到已安装的扩展的转换开始，在随附的Braintree支付模块中处理这些要求，并且无需执行任何操作即可符合PSD2。 <br /><br />**_注意：_**&#x200B;要遵守在以前版本中使用核心集成的PSD2，请执行下列操作之一：<br/> — （推荐）从[[!DNL Adobe Commerce Marketplace]](https://marketplace.magento.com/catalogsearch/result/?q=braintree#q=braintree&amp;idx=m2_cloud_prod_default_products&amp;p=0&amp;nR%5Bvisibility_search%5D%5B%3D%5D%5B0%5D=1)安装官方Braintree支付集成扩展{：target=&quot;_blank&quot;}。<br/> — 在[!DNL Commerce]配置中启用并配置Braintree付款方法。<br/><br/>这些早期的核心集成支持3D Secure 2.0验证。 但是，在JavaScript SDK v2上运行的Braintree实施不支持3D Secure 2.0。 |
| 其他 | 对于所有其他付款集成，请检查[[!DNL Commerce Marketplace]](https://marketplace.magento.com/extensions/payments-security/payment-integration.html?_ga=2.108129217.2105547619.1564067043-238341041.1564067043){：target=&quot;_blank&quot;}上可用的扩展。 请要求您的支付提供商推荐一种可支持PSD2要求的解决方案。 |

{style="table-layout:auto"}

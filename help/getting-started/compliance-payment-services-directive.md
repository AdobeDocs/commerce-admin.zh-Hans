---
title: PSD2合规性
description: 了解可能影响您商店的《支付服务指令》(PSD2)的要求。
exl-id: efe94cac-a170-48df-88cf-36019ca52951
feature: Compliance
TQID: https://experienceleague.adobe.com/paVa-tpYYzrINAPRFs4TOzbp4b4CLJDlxqNlL1gzp2Q
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: b5f00040-57a0-4a6d-a39e-383b1936c2c9id: ba9e5be9-7de1-4f71-a5d2-baead0e425eeid: c32adafa-ed01-4b31-997e-2413013911b0id: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2: id: f0ca7b10-ef6c-4ee4-b63f-030819bdd1f3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: cc72dcf1-72e1-48cc-b434-e7c27d62d67cid: d095671a-1355-40aa-8b5f-06c33c68080bid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 396
ht-degree: 0%

---

# PSD2合规性

从2019年9月14日开始，欧盟要求欧盟和英国的所有商户遵守支付服务指令(PSD2)的[强客户身份验证](https://www.cardinalcommerce.com/content-hub/mandates/psd2-sca/understanding-psd2-sca) (SCA)要求。 我们鼓励所有其他国家的商家遵循PSD2作为最佳实践。

>[!NOTE]
>
>本主题仅供参考，不应理解为法律建议。 要确定您的企业是否以及如何遵守任何法律义务，请咨询您的法律顾问。

强客户身份验证是PSD2的关键组件，需要以下两项操作：

- 只有客户才有的东西（密码或PIN）
- 只有客户知道的事情（通过电话或密钥库生成的唯一安全令牌）
- 只有客户才有的东西（生物特征认证，例如指纹或面部识别）

欧洲银行可能会拒绝不符合要求的支付。 但是，仍可接受低风险和低价值交易，以及定期订阅中的后续付款。

由于此重大更改并确保客户付款不被拒绝，Adobe为原生[!DNL Commerce]付款集成引入了以下更改和建议。

| 付款方式 | 合规性要求 |
|--- |--- |
| [PayPal](../stores-purchase/paypal.md) | 对于大多数PayPal解决方案，无需采取任何操作即可符合PSD2，因为这些要求由PayPal处理。 有关特定解决方案的信息，请参阅每个PayPal主题顶部的说明。 |
| [Braintree](../stores-purchase/braintree.md) | 从2.4.0中已安装的扩展过渡开始，在随附的Braintree Payments模块中处理相关要求，无需执行任何操作即可符合PSD2。 <br /><br />**_注意:_**&#x200B;为了遵循PSD2，在以前的版本中使用核心集成，请执行下列操作之一： <br/> — （推荐）从[[!DNL Adobe Commerce Marketplace]](https://marketplace.magento.com/catalogsearch/result/?q=braintree#q=braintree&idx=m2_cloud_prod_default_products&p=0&nR%5Bvisibility_search%5D%5B%3D%5D%5B0%5D=1){:target="_blank"}安装官方的Braintree付款集成扩展。<br/> — 在[!DNL Commerce]配置中启用并配置Braintree付款方法。<br/><br/>这些早期的核心集成支持3D Secure 2.0验证。 但是，在JavaScript SDK v2上运行的Braintree实施不支持3D Secure 2.0。 |
| 其他 | 对于所有其他付款集成，请检查[[!DNL Commerce Marketplace]](https://marketplace.magento.com/extensions/payments-security/payment-integration.html?_ga=2.108129217.2105547619.1564067043-238341041.1564067043){:target="_blank"}上的可用扩展。 请让您的支付提供商推荐一种可支持PSD2要求的解决方案。 |

{style="table-layout:auto"}

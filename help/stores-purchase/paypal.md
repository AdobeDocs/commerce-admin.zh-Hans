---
title: PayPal支付解决方案
description: 了解您商店提供的PayPal支付解决方案集成。
exl-id: d447b98e-d30c-4759-9ae0-94ccbeed9ba4
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '1230'
ht-degree: 0%

---

# PayPal支付解决方案

PayPal是在线支付领域的全球领先企业，也是客户在线支付的快速、安全方式。 可用的PayPal解决方案的选择因商家所在位置而异。 PayPal Express Checkout和PayPal Payments Standard可用于全球各地。 若要了解更多信息，请参阅[按国家/地区列出的PayPal解决方案](#paypal-solutions-by-country)。

>[!IMPORTANT]
>
>**PSD2要求：** <br/>
>从2019年9月14日开始，欧洲银行可能会拒绝不符合[PSD2](../getting-started/compliance-payment-services-directive.md)要求的支付。 对于大多数PayPal解决方案，无需采取任何操作即可遵守PSD2，因为这些要求由PayPal处理。

## PayPal商业帐户

若要在商店中提供PayPal作为付款方式，您必须拥有PayPal [商业帐户][1]和/或[PayPal Payflow帐户][2]。 在每个PayPal解决方案的描述中指定帐户要求。 你的PayPal商家帐户还用于管理任何应用于从你的商店购买的[欺诈过滤器](#paypal-fraud-management-filters)。

使用PayPal Express Checkout或Express Checkout for Payflow Pro的客户必须具有PayPal购买者帐户。 当商家启用&#x200B;_PayPal帐户（可选）_&#x200B;时，PayPal支付标准（某些国家/地区的网站支付标准）可以直接使用或通过买方帐户使用。 默认情况下，此参数处于启用状态，以便客户可以选择输入其信用卡信息或使用PayPal创建买方帐户。 禁用后，客户必须先创建PayPal购买者帐户，然后才能进行购买。

Website Payments Pro、Website Payments Pro Payflow Edition、Payflow Pro Gateway和Payflow Link要求客户在结账时输入信用卡信息。

## PayPal Credit和PayLater

PayPal PayLater让您的客户能够快速获得融资，以便他们现在购买并随时间付款，您无需支付额外费用。 当客户选择PayPal信用额度选项时，您无需支付费用，您只需支付正常的PayPal交易费用。 若要了解详细信息，请参阅[PayPal网站][3]。

在广告宣传融资时，提高销售额。 PayPal通过PayPal PayLater提供融资，帮助浏览器成为买家。 您的客户可以随着时间的推移而付费，而您则可获得前期付款，无需支付额外费用。 使用PayPal免费的横幅广告，在客户通过PayPal结帐时将PayPal融资作为付款选项进行广告。 PayPal Advertising计划已被证明可生成额外购买并可将平均购买量增加15%或更多。

您可以在结帐期间轻松地将免费现成的横幅广告添加到网站页面，并将&#x200B;_PayPal点数_&#x200B;按钮添加到购物车，以提醒客户随时可以获取融资。

>[!NOTE]
>
>从2.4.3版本开始，在包括PayPal的部署中支持PayPal PayLater。 此功能允许购物者以每两周一次分期付款的方式支付订单，而不是在购买时支付全额。 弃用PayPal信用体验。

对于美国商家，[PayPal Express Checkout](paypal-express-checkout.md)付款选项默认启用PayPal信用。 若要为此付款方法禁用它，请参阅[PayPal Express结帐配置](paypal-express-checkout.md#features)的&#x200B;_功能_&#x200B;部分。

对于其他PayPal支付解决方案，默认情况下将禁用PayPal点数，但可以在支付方式配置中启用它以支持解决方案：

- [预付款支付](paypal-payments-advanced.md)
- [Payments Pro](paypal-payments-pro.md)
- [支付标准](paypal-payments-standard.md)
- [Payflow Pro](paypal-payflow-pro.md)
- [Payflow链接](paypal-payflow-link.md)

>[!IMPORTANT]
>
>在为商店配置PayPal点数或PayPal PayLater之前，请确保在您的PayPal商家帐户中启用它。

## 集成的PayPal解决方案

借助PayPal和Adobe Commerce，您可以接受所有主要借记卡和信用卡付款。 PayPal提供额外的便利，无需额外工作，因为即使您的客户没有PayPal帐户，也可以使用PayPal支付购买费用。

>[!NOTE]
>
>您一次不能在商店中启用多个PayPal方法，但PayPal Express Checkout除外。 PayPal Express Checkout可以与其他PayPal支付方式一起使用，但PayPal Payments Standard除外。 如果更改付款解决方案，则前一种方法将被禁用。

### PayPal Express签出

[PayPal Express签出](paypal-express-checkout.md)

### PayPal多功能一体支付解决方案

在美国，PayPal提供以下符合PCI标准的解决方案，以满足您不断增长的业务需求。

- [PayPal支付高级](paypal-payments-advanced.md)
- [PayPal Payments Pro](paypal-payments-pro.md)
- [PayPal支付标准](paypal-payments-standard.md)

![PayPal多功能一体支付解决方案](./assets/paypal-all-in-one.png){width="600" zoomable="yes"}

### PayPal支付网关

支付网关是由授权信用卡或直接支付处理的电子商务应用服务提供商提供的商家服务。 它们在客户和银行之间充当中介机构。

支付网关可用于在线和离线环境。 可以通过电话、在线或移动应用程序接受付款。 该交易被发送到服务提供商的处理系统，然后发送到客户的银行进行验证和确认。 如果确认，则商家接收付款而不与客户的银行账户直接联系。

支付网关有两种类型：直接支付网关和托管支付网关。

- 直接支付网关允许用户在商店网站上输入其卡详细信息。
- 托管支付网关将用户重定向到商店网站外部的托管支付页面。

支付网关为交易涉及的所有各方提供安全和保护。

PayPal为您的企业提供了两种支付网关解决方案供您选择。 您可以让PayPal在其安全支付网站上托管您的结账，也可以通过可自定义的解决方案控制整个支付体验。

- [PayPal Payflow Pro](paypal-payflow-pro.md)
- [PayPal Payflow链接](paypal-payflow-link.md)

![设置PayPal付款网关](./assets/paypal-payment-gateway.png){width="600" zoomable="yes"}

## PayPal欺诈管理过滤器

PayPal欺诈管理过滤器使得检测和响应欺诈性交易更容易，并且可以配置为标记、保留以供审核或拒绝风险较高的付款。 与Commerce [订单状态](order-status.md)值相关的操作已根据欺诈筛选设置进行更改：

| 操作 | 结果 |
| --- | --- |
| [!UICONTROL Review] | 可疑的订单在发出订单时收到状态&#x200B;_付款审核_。 您可以在管理员或PayPal端查看订单并批准，或取消付款。 当您单击&#x200B;**[!UICONTROL Accept Payment]**&#x200B;或&#x200B;**[!UICONTROL Deny Payment]**&#x200B;时，不会为订单创建新的交易记录。 <br/><br/>如果您在PayPal网站上更改交易状态，则必须单击管理员订单页面中的&#x200B;**[!UICONTROL Get Payment Update]**&#x200B;以应用更改。 如果您单击&#x200B;**[!UICONTROL Accept Payment]**&#x200B;或&#x200B;**[!UICONTROL Deny Payment]**，则将应用在PayPal站点上所做的更改。 |
| [!UICONTROL Deny] | 客户不能下可疑订单，因为PayPal拒绝了相应的交易。 <br/><br/>若要拒绝管理员付款，请单击页面右上角的&#x200B;**[!UICONTROL Deny Payment]**。 订单状态更改为`Canceled`，交易记录已还原，并在客户帐户上释放资金。 相应的信息已添加到订单视图的&#x200B;_[!UICONTROL Comments History]_部分。 |
| [!UICONTROL Flag] | 可疑订单在放置时获得状态`Processing`。 相应的交易在商户交易列表中标有标志。 |

{style="table-layout:auto"}

## 按国家/地区列出的PayPal解决方案

| 国家/地区 | PayPal支付解决方案 |
|--- |--- |
| 澳大利亚 | [!DNL PayPal Website Payments Standard]<br/>[[!DNL PayPal Payflow Pro]](paypal-payflow-pro.md)<br/>[!DNL PayPal Website Payments Pro Hosted Solution]<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| 加拿大 | [!DNL PayPal Website Payments Standard]<br/>[!DNL PayPal Website Payments Pro]<br/>[[!DNL PayPal Payflow Pro]](paypal-payflow-pro.md)<br/>[[!DNL PayPal Payflow Link]](paypal-payflow-link.md) （包括Express Checkout）<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| 法国 | [!DNL PayPal Integral Evolution]<br/>[!DNL PayPal Website Payments Standard]<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| 德国 | [[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| 中国香港特别行政区 | [!DNL PayPal Website Payments Pro Hosted Solution]<br/>[!DNL PayPal Website Payments Standard]<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| 意大利 | [!DNL PayPal ProPay]<br/>[[!DNL Pal Payments Standard]](paypal-payments-standard.md)<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| 日本 | [!DNL PayPal Website Payments Plus]<br/>[!DNL PayPal Website Payments Standard]<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| 新西兰 | [[!DNL PayPal Payflow Pro]](paypal-payflow-pro.md)<br/>[!DNL PayPal Website Payments Standard]<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| 西班牙 | [!DNL PayPal Pasarela Integral]<br/>[!DNL PayPal Website Payments Standard]<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| 英国 | [!DNL PayPal Payments Pro Hosted Solution] （包括Express Checkout）<br/>[[!DNL PayPal Payments Standard]](paypal-payments-standard.md)<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| 美国 | [[!DNL PayPal Payments Advanced]](paypal-payments-advanced.md) （包括Express签出）<br/>[[!DNL PayPal Payments Pro]](paypal-payments-pro.md) （包括Express签出）<br/>[[!DNL PayPal Payments Standard+]](paypal-payments-standard.md)<br/>[[!DNL PayPal Payflow Pro]](paypal-payflow-pro.md) （包括Express签出）<br/>[[!DNL PayPal Payflow Link]](paypal-payflow-link.md) （包括Express签出）<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |

{style="table-layout:auto"}

### 其他国家

PayPal Express Checkout和PayPal Website Payments Standard在以下国家/地区提供：

- 阿根廷
- 奥地利
- 比利时
- 巴西
- 保加利亚
- 智利
- 哥斯达黎加
- 塞浦路斯
- 捷克共和国
- 丹麦
- 多米尼加共和国
- 厄瓜多尔尔
- 爱沙尼亚
- 芬兰
- 法属圭亚那
- 直布罗陀
- 希腊
- 瓜德罗普
- 匈牙利
- 冰岛
- 印度
- 印度尼西亚
- 爱尔兰
- 以色列
- 牙买加
- 拉脱维亚
- 列支敦士登
- 立陶宛
- 卢森堡
- 马来西亚
- 马耳他
- 马提尼克岛
- 墨西哥
- 荷兰
- 挪威
- 菲律宾
- 波兰
- 葡萄牙
- 留尼汪
- 罗马尼亚
- 圣马力诺
- 新加坡
- 斯洛伐克
- 斯洛文尼亚
- 南非
- 韩国
- 瑞典
- 瑞士
- 台湾
- 泰国
- 土耳其
- 阿拉伯联合酋长国
- 乌拉圭
- 委内瑞拉
- 越南


[1]: https://manager.paypal.com/
[2]: https://developer.paypal.com/docs/payflow/payflow-gateway/
[3]: https://www.paypal.com/us/business/buy-now-pay-later

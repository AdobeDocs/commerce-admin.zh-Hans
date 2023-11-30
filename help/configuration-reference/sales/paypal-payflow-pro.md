---
title: ’[!UICONTROL Sales] &gt； [!UICONTROL Payment Methods] &gt；  [!UICONTROL PayPal Payflow Pro]’
description: 在中查看配置设置 [!UICONTROL PayPal Payflow Pro] 部分，位于 [!UICONTROL Sales] &gt； [!UICONTROL Payment Methods] 商务管理员页面。
exl-id: 2aae038b-15c0-452a-98bc-4d97efbb60f6
feature: Configuration, Payments
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '650'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Payment Methods] >  [!UICONTROL PayPal Payflow Pro]

>[!IMPORTANT]
>
>**PSD2要求：** <br/>
>从2019年9月14日起，欧洲银行可能会拒绝未满足要求的支付 [PSD2](../../getting-started/compliance-payment-services-directive.md) 要求。 为了遵守PSD2， [!DNL PayPal Payflow Pro] 必须与 [!DNL Cardinal Commerce]. 要了解更多信息，请参阅 [3D Secure for Payflow](https://developer.paypal.com/api/nvp-soap/payflow/3d-secure-overview/).

{{config}}

## [!UICONTROL Required Settings]

![必需的设置](./assets/paypal-payflow-pro-settings.png)<!-- zoom -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Email Associated with PayPal Merchant Account] | 网站 | （可选）与您的PayPal商家帐户关联的任何电子邮件地址。 电子邮件地址区分大小写，且必须与帐户中的地址完全匹配。 |
| [!UICONTROL Partner] | 网站 | 您的PayPal合作伙伴ID（如果适用）。 |
| [!UICONTROL Vendor] | 网站 | 您的PayPal用户登录名。 |
| 用户 | 网站 | 您PayPal帐户中其他用户的ID。 |
| [!UICONTROL Password] | 网站 | 与您的PayPal商家帐户关联的密码。 |
| [!UICONTROL Test Mode] | 网站 | 启用后，将在测试环境中运行PayPal Payflow Pro。 当您准备好在生产模式下“上线”时，请关闭测试模式。 选项： `Yes` / `No` |
| [!UICONTROL Use Proxy] | 网站 | 当服务器防火墙阻止直接访问PayPal服务器时，可以使用代理重定向流量。 如果适用，则标识用于与PayPal服务器建立连接的代理服务器。 选项： `Yes` / `No` <br/><br/>如果启用，请设置代理选项： <br/>**`Proxy Host`**— 代理主机的IP地址。<br/>**`Proxy Port`**  — 代理端口的编号。 |
| [!UICONTROL Enable this Solution] | 网站 | 确定PayPal Payflow Pro是否作为付款方式提供给您的客户。 |
| [!UICONTROL Enable PayPal Credit] | 网站 | 确定客户是否可以将PayPal信用作为付款选项。 |

{style="table-layout:auto"}

## [!UICONTROL Advertise PayPal Credit]

![广告PayPal点数](./assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit.png)<!-- zoom -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Publisher ID] | 网站 | 与您的PayPal信用帐户关联的发布者ID。 |
| [!UICONTROL Get Publisher ID from PayPal] |  | 从PayPal获取您的发布者ID。 |
| [!UICONTROL Home Page] | 网站 | 确定 [!DNL PayPal Credit] 标题栏目中。 选项： <br/>**`Display`**— 确定[!DNL PayPal Credit] 横幅会显示在您商店的主页上。 选项： `Yes` / `No`<br/>**`Position`**  — 确定 [!DNL PayPal Credit] 标题栏目中。 选项：标题（中心）/侧栏（右） <br/>**`Size`**— 确定 [!DNL PayPal Credit] 标题栏目中。 选项： `190 x 100` / `234 x 60` / `300 x 50` / `468 x 60` / `728 x 90` /` 800 x 66` |
| [!UICONTROL Catalog Category Page] | 网站 | 确定 [!DNL PayPal Credit] 类别页面上的横幅。 选项： (与 [!UICONTROL Home Page]) |
| [!UICONTROL Catalog Product Page] | 网站 | 确定 [!DNL PayPal Credit] 产品页面上的横幅。 选项： (与 [!UICONTROL Home Page]) |
| [!UICONTROL Checkout Cart Page] | 网站 | 确定 [!DNL PayPal Credit] 购物车页面上的横幅。 选项： (与 [!UICONTROL Home Page]) |

{style="table-layout:auto"}

## [!UICONTROL Basic Settings - PayPal Payflow Pro]

![基本设置](./assets/payment-methods-paypal-payflow-pro-basic-settings.png)<!-- zoom -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Title] | 商店视图 | 在结帐期间将PayPal Payflow Pro标识为付款方法的名称。 |
| [!UICONTROL Sort Order] | 商店视图 | 一个数字，用于在结账期间与其他支付方式一起列出时，确定PayPal Payflow Pro显示的顺序。 |
| [!UICONTROL Payment Action] | 网站 | 确定PayPal在提交订单时执行的操作。 选项： <br/>**`Authorization`**— 批准购买，但保留资金。 该金额在商户将该金额“扣押”前不予提取。<br/>**`Sale`**  — 采购金额已获授权并立即从客户账户中提取。 |
| **[!UICONTROL Credit Card Settings]** |  |  |
| [!UICONTROL Allowed Credit Cart Types] | 网站 | 确定客户在结帐期间可用的信用卡。 选择每个受支持的卡片。 选项： `American Express` （需要额外协议）/ `Visa` / `MasterCard` / `Discover` / `JCB` |

{style="table-layout:auto"}

## [!UICONTROL Advanced Settings]

![高级设置](./assets/payment-methods-paypal-payflow-pro-advanced-settings.png)<!-- zoom -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| 在购物车上显示 | 商店视图 | 确定PayPal Express结帐在购物车中是否显示为付款选项。 选项：是（推荐）/否 |
| [!UICONTROL Payment Action Applicable From] | 网站 | 确定适用的国家/地区选择的范围。 选项：所有允许的国家/地区/特定国家/地区 |
| [!UICONTROL Countries Payment Applicable From] | 网站 | 标识接受付款的每个国家/地区。 只有帐单地址在选定国家/地区的客户才能使用此付款方法进行购买。 |
| [!UICONTROL Debug Mode] | 网站 | 在日志文件中记录您的商店和PayPal支付系统之间发送的消息。 选项： `Yes` / `No` <br/><br/>**_注意：_**日志文件存储在服务器上，只有开发人员才能访问。 根据PCI数据安全标准，信用卡信息不会记录在日志文件中。 |
| [!UICONTROL Enable SSL Verification] | 网站 | 启用主机安全证书的验证。 选项： `Yes` / `No` |
| [!UICONTROL Transfer Cart Line Items] | 网站 | 显示PayPal网站上客户购物车中行项目的完整摘要。 选项： `Yes` / `No` |
| [!UICONTROL Skip Order Review Step] | 网站 | 确定客户是否可以从PayPal网站完成交易，或者是否需要返回您的商店并在提交订单之前完成订单审核步骤。 选项： `Yes` / `No` |

{style="table-layout:auto"}

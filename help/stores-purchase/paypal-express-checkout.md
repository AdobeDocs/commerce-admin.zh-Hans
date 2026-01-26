---
title: PayPal Express签出
description: 了解如何在您的商店中将PayPal Express结帐设置为在线付款解决方案。
exl-id: 0cd90306-cf47-4a5f-8994-6ae96904ae2f
feature: Payments
badgePaas: label="仅限PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="仅适用于云项目(Adobe管理的PaaS基础架构)和内部部署项目上的Adobe Commerce 。"
source-git-commit: cace9d1de00955494d8bc607c017778ff7df4806
workflow-type: tm+mt
source-wordcount: '3111'
ht-degree: 0%

---

# PayPal Express签出

PayPal Express Checkout使您的客户能够通过信用卡或个人PayPal帐户的安全性进行支付，从而帮助提高销售额。 在结账过程中，客户将被重定向到安全的PayPal网站以完成付款信息。 然后，客户将返回到您的商店以完成剩余的结账过程。 选择“快速结帐”会将您熟悉的PayPal按钮添加到您的商店，据报这将会增加销售额。

>[!IMPORTANT]
>
>**PSD2要求：** <br/>
>从2019年9月14日起，欧洲银行可能会拒绝不符合[PSD2](../getting-started/compliance-payment-services-directive.md)要求的支付。 PayPal Express Checkout无需执行任何操作即可符合PSD2，因为所有要求都由PayPal处理。

具有当前PayPal帐户的客户只需单击&#x200B;_[!UICONTROL Check out with PayPal]_&#x200B;按钮，即可一步完成购买。 Express Checkout可以作为独立解决方案使用，也可以与其中一个PayPal多功能一体解决方案一起使用。 如果您已经在网上接受信用卡，则可以提供“快速结帐”作为额外选项，以吸引喜欢使用PayPal付款的新客户。

>[!NOTE]
>
>PayPal已停止支持通过PayPal Express Checkout销售数字商品，并建议使用[PayPal Payments Standard](paypal-payments-standard.md)或其他PayPal支付网关处理任何包含[虚拟产品](../catalog/product-create-virtual.md)的订单。

## 要求

- 商家： [企业PayPal帐户](https://www.paypal.com/webapps/mpp/how-to-sell-online)
- 客户：[个人PayPal帐户](https://www.paypal.com/webapps/mpp/buying-online)

## 快速签出工作流

与其他付款方法不同，PayPal Express结帐允许客户在通常结帐工作流程开始时从产品页面、迷你购物车和购物车结帐。

1. **客户下订单** — 客户单击/点按&#x200B;_[!UICONTROL Check out with PayPal]_&#x200B;按钮。
1. **客户被重定向到PayPal网站** — 客户被重定向到PayPal网站以完成交易。
1. **客户登录到其PayPal帐户** — 客户必须登录到其PayPal帐户才能完成交易。 付款系统使用来自其PayPal帐户的账单和运送信息。
1. **客户返回结帐页面** — 客户将被重定向回商店中的结帐页面以查看订单。
1. **客户下订单** — 客户下订单，并将订单信息提交给PayPal。
1. **PayPal结算交易** - PayPal接收订单并结算交易。

>[!NOTE]
>
>PayPal Express Checkout不支持具有多个地址的订单。

## 上下文签出

PayPal的&#x200B;_In-Context Checkout_&#x200B;使在线付款变得前所未有的简单。 在经过简单的一键或两键式无缝结账期间，客户不会忘记您的商店。 上下文结帐功能在Mac和PC上同样运行良好，在台式计算机、平板电脑和移动设备上提供一致的体验。 要了解更多信息，请参阅[在Express Checkout中进行In-Context Checkout](https://www.paypal.com/rs/webapps/mpp/express-checkout)。

![PayPal上下文签出演示](./assets/storefront-paypal-in-context.png){width="700" zoomable="yes"}

[_PayPal in-context签出演示_](https://demo.paypal.com/us/demo/navigation?merchant=bigbox&page=incontextProductCheckout)

当您为[!DNL PayPal Express Checkout]配置存储时，可以启用此选项。

## 配置PayPal帐户

在Commerce管理员中设置PayPal Express签出之前，必须在PayPal网站上配置商家帐户。

1. 在[manager.paypal.com](https://manager.paypal.com/)登录到您的PayPal高级帐户。

1. 转到&#x200B;**[!UICONTROL Service Settings]** > **[!UICONTROL Hosted Checkout Pages]** > **[!UICONTROL Set Up]**&#x200B;并进行以下设置：

   - **[!UICONTROL AVS]**： `No`
   - **[!UICONTROL CSC]**： `No`
   - **[!UICONTROL Enable Secure Token]**： `Yes`

1. 单击&#x200B;**[!UICONTROL Save Changes]**。

1. 设置另一个用户（由PayPal推荐）：

   - 转到[manager.paypal.com](https://manager.paypal.com/)并登录您的帐户。

   - 要设置另一个用户，请按照说明操作。

   - 单击&#x200B;**[!UICONTROL Update]**。

## 在Commerce中设置PayPal Express签出

您可以同时激活两个PayPal解决方案：PayPal Express Checkout，以及一体化解决方案。 如果启用其他解决方案，则会自动停用以前使用的解决方案。

>[!NOTE]
>
>随时单击&#x200B;**[!UICONTROL Save Config]**&#x200B;以保存进度。

### 步骤1：开始配置

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧面板中，展开&#x200B;**[!UICONTROL Sales]**&#x200B;并选择&#x200B;**[!UICONTROL Payment Methods]**。

1. 如果您的安装有多个网站、商店或视图，请将&#x200B;**[!UICONTROL Store View]**&#x200B;设置为要应用此配置的商店视图。

1. 在&#x200B;_[!UICONTROL Merchant Location]_&#x200B;部分中，选择您的公司所在的&#x200B;**[!UICONTROL Merchant Country]**。

   此设置确定配置中显示的PayPal解决方案的选择。

   ![商家国家/地区](../configuration-reference/sales/assets/payment-methods-merchant-location.png){width="600" zoomable="yes"}

1. 在&#x200B;_[!UICONTROL Recommended Solutions]_&#x200B;下，单击&#x200B;**[!UICONTROL Configure]**&#x200B;的&#x200B;**[!UICONTROL PayPal Express Checkout]**。

   ![配置PayPal Express签出](./assets/paypal-express-checkout.png){width="600"}

### 步骤2：启用并连接您的PayPal帐户

1. 如果需要，请展开![扩展选择器](../assets/icon-display-expand.png) **[!UICONTROL Required PayPal Settings]**&#x200B;部分。

   ![连接你的PayPal帐户](./assets/paypal-express-required.png){width="600" zoomable="yes"}

1. 连接帐户以进行测试或生产：

   - 对于测试（开发）模式，请单击&#x200B;**[!UICONTROL Sandbox Credentials]**&#x200B;并输入您的[PayPal沙盒](https://developer.paypal.com/docs/api-basics/sandbox/)凭据。
   - 对于生产模式，请单击&#x200B;**[!UICONTROL Connect with PayPal]**&#x200B;并输入您的生产帐户凭据。

   验证连接后，您可以继续。

1. 将&#x200B;**[!UICONTROL Enable this Solution]**&#x200B;设置为`Yes`。

1. 要启用[PayPal In-Context签出](#in-context-checkout)：

   - 将&#x200B;**[!UICONTROL Enable In-Context Checkout Experience]**&#x200B;设置为`Yes`。

   - 输入您的PayPal **[!UICONTROL Merchant Account ID]**。

     您的商户帐户ID在您的PayPal企业帐户配置文件中。

>[!NOTE]
>
>此付款选项默认启用[PayPal点数](paypal.md#paypal-credit-and-pay-later)。

### 步骤3：完成所需的PayPal设置

1. 如果需要，请展开![扩展选择器](../assets/icon-display-expand.png) **[!UICONTROL Express Checkout]**&#x200B;部分。

   ![PayPal Express签出所需的设置](./assets/paypal-express-settings.png){width="600" zoomable="yes"}

1. （可选）输入&#x200B;**[!UICONTROL Email Associated with PayPal Merchant Account]**。

   >[!IMPORTANT]
   >
   >电子邮件地址区分大小写。 要接收付款，您输入的电子邮件地址必须与在PayPal商家帐户中指定的电子邮件地址匹配。

   如果您没有PayPal帐户，请单击&#x200B;**[!UICONTROL Start accepting payments via PayPal]**。

1. 将&#x200B;**[!UICONTROL API Authentication Methods]**&#x200B;设置为以下项之一：

   - `API Signature` — 此PayPal身份验证方法最易于实施，它基于您的用户名、密码以及标识您帐户的唯一字符和数字字符串。 API签名凭据不会过期。
   - `API Certificate` — 此PayPal身份验证方法基于您的用户名、密码和可下载的证书，因此更加安全。 API凭据将在三年后过期，必须续订。

   如有必要，请完成以下操作：

   - **[!UICONTROL API Username]**
   - **[!UICONTROL API Password]**
   - **[!UICONTROL API Signature]**

1. 如果您使用的是来自沙盒帐户的凭据，请将&#x200B;**[!UICONTROL Sandbox Mode]**&#x200B;设置为`Yes`。

   在沙盒中测试配置时，仅使用PayPal推荐的[信用卡号](https://www.paypalobjects.com/en_AU/vhelp/paypalmanager_help/credit_card_numbers.htm)。 当您准备好进入生产环境时，请返回配置并将沙盒模式设置为`No`并连接到您的生产PayPal帐户。

1. 如果您的系统使用代理服务器在Commerce和PayPal支付系统之间建立连接，请将&#x200B;**[!UICONTROL API Uses Proxy]**&#x200B;设置为`Yes`并完成以下操作：

   - **[!UICONTROL Proxy Host]**
   - **[!UICONTROL Proxy Port]**

在此一系列步骤结束时，已完成所需的PayPal设置。 您可以继续使用基本设置和高级设置，或单击&#x200B;**[!UICONTROL Save Config]**&#x200B;并稍后返回以调整配置

### 步骤4：设置广告PayPal Credit/广告PayPal PayLater（可选）

从2.4.3版本开始，在包括PayPal的部署中支持PayPal PayLater。 此功能允许购物者以每两周一次分期付款的方式支付订单，而不是在购买时支付全额。 弃用PayPal信用体验。

将&#x200B;**[!UICONTROL Enable PayPal PayLater Experience]**&#x200B;设置为以下项之一：

- `Yes` — 设置广告PayPal PayLater
- `No` — 设置广告PayPal点数

>[!NOTE]
>
>**[!UICONTROL Enable PayPal PayLater Experience]**&#x200B;设置不会禁用[!DNL PayPal PayLater]功能，也不会从店面删除&#x200B;**_[!UICONTROL PayPal PayLater]_**&#x200B;按钮。 要禁用店面上的&#x200B;**_[!UICONTROL PayPal PayLater]_**&#x200B;和&#x200B;**_[!UICONTROL PayPal Credit]_**&#x200B;按钮，您必须为`PayPal Credit`设置（**[!UICONTROL Disable Funding Options]**&#x200B;下的[!UICONTROL Advanced Settings]）选择[!UICONTROL Frontend Experience Settings]值。

#### 广告PayPal点数

1. 展开![部分的](../assets/icon-display-expand.png)扩展选择器&#x200B;**[!UICONTROL Advertise PayPal Credit]**。

1. 若要获取帐户信息，请单击&#x200B;**[!UICONTROL Get Publisher ID from PayPal]**&#x200B;并按照说明操作。

1. 输入您的&#x200B;**[!UICONTROL Publisher ID]**。

   ![广告PayPal点数](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit.png){width="600" zoomable="yes"}

1. 展开![部分的](../assets/icon-display-expand.png)扩展选择器&#x200B;**[!UICONTROL Home Page]**。

1. 若要在页面上放置横幅，请将&#x200B;**[!UICONTROL Display]**&#x200B;设置为`Yes`。

1. 将&#x200B;**[!UICONTROL Position]**&#x200B;设置为以下项之一：

   - `Header (center)`
   - `Sidebar (right)`

1. 将&#x200B;**[!UICONTROL Size]**&#x200B;设置为以下项之一：

   - `190 x 100`
   - `234 x 60`
   - `300 x 50`
   - `468 x 60`
   - `728 x 90`
   - `800 x 66`

   ![通告PayPal点数主页设置](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit-home-page.png){width="600" zoomable="yes"}

1. 展开![扩展选择器](../assets/icon-display-expand.png)其余部分并重复上述步骤：

   - [!UICONTROL Catalog Category Page]
   - [!UICONTROL Catalog Product Page]
   - [!UICONTROL Checkout Cart Page]

#### 广告PayPal PayLater

1. 展开![部分的](../assets/icon-display-expand.png)扩展选择器&#x200B;**[!UICONTROL Advertise PayPal PayLater]**。

1. 将&#x200B;**[!UICONTROL Enable PayPal PayLater]**&#x200B;设置为`Yes`。

1. 展开![部分的](../assets/icon-display-expand.png)扩展选择器&#x200B;**[!UICONTROL Home Page]**。

1. 若要在页面上放置横幅，请将&#x200B;**[!UICONTROL Display]**&#x200B;设置为`Yes`。

1. 将&#x200B;**[!UICONTROL Position]**&#x200B;设置为以下项之一：

   - `Header (center)`
   - `Sidebar`

1. 将&#x200B;**[!UICONTROL Style Layout]**&#x200B;设置为以下项之一：

   - `Text`
   - `Flex`

1. 仅对于[!UICONTROL Style Layout] **[!UICONTROL Text]**，将&#x200B;**[!UICONTROL Logo Type]**&#x200B;设置为以下项之一：

   - `Primary`
   - `Alternative`
   - `Inline`
   - `None`

1. 仅对于[!UICONTROL Style Layout] **[!UICONTROL Text]**，将&#x200B;**[!UICONTROL Logo Position]**&#x200B;设置为以下项之一：

   - `Left`
   - `Right`
   - `Top`

1. 仅对于[!UICONTROL Style Layout] **[!UICONTROL Text]**，将&#x200B;**[!UICONTROL Text Color]**&#x200B;设置为以下项之一：

   - `Black`
   - `White`
   - `Monochrome`
   - `Grayscale`

1. 仅对于[!UICONTROL Style Layout] **[!UICONTROL Text]**，将&#x200B;**[!UICONTROL Text Size]**&#x200B;设置为以下项之一：

   - `10px`
   - `11px`
   - `12px`
   - `13px`
   - `14px`
   - `15px`
   - `16px`

1. 仅对于[!UICONTROL Style Layout] **[!UICONTROL Flex]**，将&#x200B;**[!UICONTROL Ratio]**&#x200B;设置为以下项之一：

   - `1x1`
   - `1x4`
   - `8x1`
   - `20x1`

1. 仅对于[!UICONTROL Style Layout] **[!UICONTROL Flex]**，将&#x200B;**[!UICONTROL Color]**&#x200B;设置为以下项之一：

   - `Blue`
   - `Black`
   - `White`
   - `White No Border`
   - `Gray`
   - `Monochrome`
   - `Grayscale`

   ![通告PayPal点数主页设置](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-paylater-home-page.png){width="600" zoomable="yes"}

1. 展开![扩展选择器](../assets/icon-display-expand.png)其余部分并重复上述步骤：

   - [!UICONTROL Catalog Product Page]
   - [!UICONTROL Checkout Cart Page]
   - [!UICONTROL Checkout Payment Step]
   - [!UICONTROL Catalog Category Page]

### 步骤5：完成基本设置

1. 展开![部分的](../assets/icon-display-expand.png)扩展选择器&#x200B;**[!UICONTROL Basic Settings - PayPal Express Checkout]**。

   ![基本设置](../configuration-reference/sales/assets/payment-methods-paypal-express-checkout-basic-settings.png){width="600" zoomable="yes"}

1. 对于&#x200B;**[!UICONTROL Title]**，输入在结帐时标识此付款方式的标题。

   建议对所有商店视图使用标题&#x200B;_PayPal_。

1. 如果您提供多种付款方式，请输入&#x200B;**[!UICONTROL Sort Order]**&#x200B;的数字，以确定与其他付款方式一起列出时PayPal快速结帐的出现顺序。

   此数字相对于其他支付方式。 （`0` =第一，`1` =第二，`2` =第三，依此类推。）

1. 将&#x200B;**[!UICONTROL Payment Action]**&#x200B;设置为以下项之一：

   - `Authorization` — 批准购买并暂停资金。 在商户捕获&#x200B;_金额_&#x200B;之前，不撤消该金额。
   - `Sale` — 已授权并立即从客户帐户中收回购买金额。
   - `Order` — 未在PayPal的客户余额、银行帐户或信用卡中获取或授权订单金额。 订单付款活动表示PayPal付款系统与商家之间的协议。 它使商家能够在长达29天的时间内，从客户买方帐户中获取一个或多个最高至订购总额的金额。 在订购资金后，商家可以在接下来的29天内随时抓获这些资金。 只能通过创建一张或多张发票从Commerce管理员处获取订单金额。

1. 要在产品页面上显示&#x200B;_[!UICONTROL Check out with PayPal]_&#x200B;按钮，请将&#x200B;**[!UICONTROL Display on Product Details Page]**&#x200B;设置为`Yes`。

1. 如果付款活动设置为`Order`，请完成以下操作

   - **[!UICONTROL Authorization Honor Period (days)]** — 确定主要授权保持有效的时间。 该值应等于您的PayPal商家帐户中的相应值。 您的PayPal商家帐户中的默认值为`3`。 要增加此数量，您必须联系PayPal。 授权在美国太平洋时间最后一天的晚上11:49失效。

   - **[!UICONTROL Order Valid Period (days)]** — 确定订单保持有效的时间。 订单无效后，您将无法再为其创建发票。 指定等于PayPal商家帐户中的订单有效期间值的值。 您的PayPal商家帐户中的默认值为`29`。 要更改此号码，您必须联系PayPal。

   - **[!UICONTROL Number of Child Authorizations]** — 指定单个订单的最大授权数量，该数量决定了您可以为订单创建的联机部分发票的最大数量。 此值应等于您的PayPal商家帐户中的相应设置。 您的PayPal帐户中的默认子授权数为`1`。 要增加此数量，您必须联系PayPal。

### 步骤6：完成高级设置

1. 展开![部分的](../assets/icon-display-expand.png)扩展选择器&#x200B;**[!UICONTROL Advanced Settings]**。

   ![高级设置 — PayPal Express签出](../configuration-reference/sales/assets/payment-methods-paypal-express-checkout-advanced-settings.png){width="600" zoomable="yes"}

1. 将&#x200B;**[!UICONTROL Display on Shopping Cart]**&#x200B;设置为`Yes`。

1. 将&#x200B;**[!UICONTROL Payment Applicable From]**&#x200B;设置为以下项之一：

   - `All Allowed Countries` — 来自您商店配置中指定的所有国家/地区的客户可以使用此付款方式。
   - `Specific Countries` — 选择此选项后，将显示&#x200B;_[!UICONTROL Payment from Specific Countries]_&#x200B;列表。 要选择多个国家/地区，请按住Ctrl键(PC)或Command键(Mac)并单击每个项目。

1. 要将与付款系统的通信写入日志文件，请将&#x200B;**[!UICONTROL Debug Mode]**&#x200B;设置为`Yes`。

   PayPal Payments Advanced的日志文件是`_payflow_advanced.log`。

   >[!NOTE]
   >
   >根据PCI数据安全标准，信用卡信息不会记录在日志文件中。

1. 要启用主机真实性验证，请将&#x200B;**[!UICONTROL Enable SSL Verification]**&#x200B;设置为`Yes`。

1. 要显示PayPal网站中按行项目的客户订单的完整摘要，请将&#x200B;**[!UICONTROL Transfer Cart Line Items]**&#x200B;设置为`Yes`。

1. 要在摘要中包含最多十个配送选项，请将&#x200B;**[!UICONTROL Transfer Shipping Options]**&#x200B;设置为`Yes`。 （仅当将行项目设置为转移时，才会显示此选项。）

1. 要确定用于PayPal接受按钮的图像类型，请将&#x200B;**[!UICONTROL Shortcut Buttons Flavor]**&#x200B;设置为以下项之一：

   - `Dynamic` - （推荐）显示可从PayPal服务器动态更改的图像。
   - `Static` — 显示无法动态更改的特定图像。

1. 若要允许没有PayPal帐户的客户使用此方法购物，请将&#x200B;**[!UICONTROL Enable PayPal Guest Checkout]**&#x200B;设置为`Yes`。

1. 将&#x200B;**[!UICONTROL Require Customer's Billing Address]**&#x200B;设置为以下项之一：

   - `Yes` — 所有购买均需要客户的帐单地址。
   - `No` — 任何购买均不需要客户的帐单地址。
   - `For Virtual Quotes Only` — 仅需要客户的虚拟报价帐单地址。

   >[!NOTE]
   >
   >必须通过PayPal技术支持为商户帐户启用此功能。

1. （可选）设置&#x200B;**[!UICONTROL Billing Agreement Signup]**&#x200B;以允许客户在客户帐户中没有可用的有效帐单协议时，与您在PayPal支付系统中的商店签署[帐单协议](paypal-billing-agreements.md)：

   - `Auto` — 客户可以在快速结帐流程中签署帐单协议，或使用其他付款方式。
   - `Ask Customer` — 客户可以决定是否在Express Checkout流程中签署帐单协议。
   - `Never` — 客户无法在Express结帐流程中签署帐单协议。

   >[!NOTE]
   >
   >商家必须要求[PayPal商家技术支持](https://developer.paypal.com/support/)在其帐户中启用帐单协议。 仅在PayPal确认您的商户帐户已启用帐单协议后，_帐单协议注册_&#x200B;参数才启用。

1. 要允许客户从PayPal网站完成交易而不返回商店进行订单审核，请将&#x200B;**[!UICONTROL Skip Order Review Step]**&#x200B;设置为`Yes`。

1. 根据存储需要，完成其他部分：

   - [PayPall记帐协议设置](#paypal-billing-agreement-settings)
   - [结算报表设置](#settlement-report-settings)
   - [前端体验设置](#frontend-experience-settings)
   - [自定义智能按钮](#customize-smart-buttons)
   - [功能](#features)

1. 完成后，单击&#x200B;**[!UICONTROL Save Config]**。

#### PayPal计费协议设置

[计费协议](paypal-billing-agreements.md)是商家与客户之间签订的销售协议，已通过PayPal授权可与多个订单一起使用。 在结账过程中，“帐单协议”付款选项仅对已与贵公司签订帐单协议的客户显示。 在PayPal授权协议后，支付系统会颁发一个唯一的参考ID以标识与协议关联的每个订单。 与采购订单类似，客户与您的公司之间可以设置的帐单协议数没有限制。

1. 展开![部分的](../assets/icon-display-expand.png)扩展选择器&#x200B;**[!UICONTROL PayPal Billing Agreement Settings]**。

   ![帐单协议设置](../configuration-reference/sales/assets/payment-methods-paypal-express-checkout-billing-agreement-settings.png){width="600" zoomable="yes"}

1. 将&#x200B;**[!UICONTROL Enabled]**&#x200B;设置为`Yes`。

1. 对于&#x200B;**[!UICONTROL Title]**，输入在结帐期间标识PayPal帐单协议方法的标题。

1. 如果您提供多种付款方式，请在&#x200B;**[!UICONTROL Sort Order]**&#x200B;字段中输入一个数字，以确定在结账过程中与其他付款方式一起列出帐单协议时显示的顺序。

1. 将&#x200B;**[!UICONTROL Payment Action]**&#x200B;设置为以下项之一：

   - `Authorization` — 批准购买并暂停资金。 该金额在商户将该金额“扣押”前不予提取。
   - `Sale` — 已授权并立即从客户帐户中收回购买金额。

1. 将&#x200B;**[!UICONTROL Payment Applicable From]**&#x200B;设置为以下项之一：

   - `All Allowed Countries` — 来自您商店配置中指定的所有国家/地区的客户可以使用此付款方式。
   - `Specific Countries` — 选择此选项后，将显示&#x200B;_[!UICONTROL Payment from Specific Countries]_&#x200B;列表。 要选择多个国家/地区，请按住Ctrl键(PC)或Command键(Mac)并单击每个国家/地区。

1. 若要在日志文件中记录与付款系统的通信，请将&#x200B;**[!UICONTROL Debug Mode]**&#x200B;设置为`Yes`。

   >[!NOTE]
   >
   >日志文件存储在服务器上，只有开发人员才能访问。 根据PCI数据安全标准，信用卡信息不会记录在日志文件中。

1. 要启用SSL验证，请将&#x200B;**[!UICONTROL Enable SSL Verification]**&#x200B;设置为`Yes`。

1. 要在PayPal支付页面上显示客户订单中每个行项目的摘要，请将&#x200B;**[!UICONTROL Transfer Cart Line Items]**&#x200B;设置为`Yes`。

1. 要允许客户从其客户帐户的仪表板启动帐单协议，请将&#x200B;**[!UICONTROL Allow in Billing Agreement Wizard]**&#x200B;设置为`Yes`。

#### 结算报表设置

1. 展开![部分的](../assets/icon-display-expand.png)扩展选择器&#x200B;**[!UICONTROL Settlement Report Settings]**。

   ![结算报告设置](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-settlement-report-settings.png){width="600" zoomable="yes"}

1. 对于&#x200B;**[!UICONTROL SFTP Credentials]**，执行以下操作：

   - 如果您已注册PayPal安全FTP服务器，请输入以下SFTP登录凭据：

      - 登录
      - 密码

   - 要在网站上使用Express Checkout在&#x200B;_上线_&#x200B;之前运行测试报告，请将&#x200B;**[!UICONTROL Sandbox Mode]**&#x200B;设置为`Yes`。

   - 输入&#x200B;**[!UICONTROL Custom Endpoint Hostname or IP Address]**。

     默认情况下，值为： `reports.paypal.com`

   - 输入保存报告的&#x200B;**[!UICONTROL Custom Path]**。

     默认情况下，值为： `/ppreports/outgoing`

1. 要根据计划生成报表，请完成&#x200B;**[!UICONTROL Scheduled Fetching]**&#x200B;设置：

   - 将&#x200B;**[!UICONTROL Enable Automatic Fetching]**&#x200B;设置为`Yes`。

   - 将&#x200B;**[!UICONTROL Schedule]**&#x200B;设置为以下项之一：

      - `Daily`
      - `Every 3 Days`
      - `Every 7 Days`
      - `Every 10 Days`
      - `Every 14 Days`
      - `Every 30 Days`
      - `Every 40 Days`

     PayPal会将每个报表保留45天。

   - 如果要生成报告，请将&#x200B;**[!UICONTROL Time of Day]**&#x200B;设置为小时、分钟和秒。

#### 前端体验设置

使用前端体验设置选择要在您的网站上显示的PayPal徽标，并自定义您的PayPal商家页面的外观。

1. 展开![部分的](../assets/icon-display-expand.png)扩展选择器&#x200B;**[!UICONTROL Frontend Experience Settings]**。

   ![前端体验设置](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-frontend-experience-settings1.png){width="600" zoomable="yes"}

1. 选择要显示在应用商店的PayPal块中的&#x200B;**[!UICONTROL PayPal Product Logo]**。

   PayPal徽标有四种样式和两种尺寸：

   - `No Logo`
   - `We Prefer PayPal (150 x 60 or 150 x 40)`
   - `Now Accepting PayPal (150 x 60 or 150 x 40)`
   - `Payments by PayPal (150 x 60 or 150 x 40)`
   - `Shop Now Using PayPal (150 x 60 or 150 x 40)`

1. 要自定义PayPal商家页面的外观，请执行以下操作：

   - 输入要应用于PayPal商家页面的&#x200B;**[!UICONTROL Page Style]**&#x200B;的名称：

      - `paypal` — 使用PayPal页面样式。
      - `primary` — 使用您在帐户配置文件中标识为&#x200B;_primary_&#x200B;样式的页面样式。
      - `your_custom_value` — 使用在您的帐户配置文件中指定的自定义付款页面样式。

   - 对于&#x200B;**[!UICONTROL Header Image URL]**，输入要显示在付款页左上角的图像URL。 最大文件大小为750像素宽x 90像素高。

     >[!NOTE]
     >
     >PayPal建议将映像驻留在安全(https)服务器上。 否则，浏览器可能会警告&#x200B;_该页面包含安全和非安全项目_。

   - 要设置页面的颜色，请为以下各项输入六个字符的十六进制代码（不带`#`符号）：

      - **[!UICONTROL Header Background Color]** — 签出页面标题的背景颜色。
      - **[!UICONTROL Header Border Color]** — 标题周围两像素边框的颜色。
      - **[!UICONTROL Page Background Color]** — 结账页面以及标题和付款表单周围的背景颜色。

#### 自定义智能按钮

_智能支付按钮_&#x200B;功能允许您自定义PayPal按钮，该按钮可以显示在“结帐”、“产品详细信息”、“购物车”和“迷你购物车”页面上。 PayPal的内部研究表明，默认选项具有高度可识别性，可能会提高购买率，但它们的默认设置可能与你的商店风格不符。 您可以选择：

- PayPal按钮的大小、颜色和形状
- 显示在PayPal按钮上的文本
- 显示多个按钮时的布局（水平或垂直）

若要自定义按钮，请展开以下每个部分的![扩展选择器](../assets/icon-display-expand.png)并调整设置：

- **[!UICONTROL Checkout Page]**
- **[!UICONTROL Product Pages]**
- **[!UICONTROL Cart Page]**
- **[!UICONTROL Mini Cart]**

![签出页面设置](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-frontend-experience-settings2.png){width="600" zoomable="yes"}

**_为每种页面类型配置按钮显示:_**

1. 展开![扩展选择器](../assets/icon-display-expand.png)部分。

1. 将&#x200B;**[!UICONTROL Customize Button]**&#x200B;设置为`Yes`。

1. 要设置PayPal在智能支付按钮上显示的文本，请将&#x200B;**[!UICONTROL Label]**&#x200B;设置为以下任一项：

   - `Checkout` - PayPal结帐
   - `Pay` - PayPal结帐
   - `Buy Now` — 立即使用PayPal购买
   - `PayPal` - Paypal
   - `Installment` - Paypal
   - `Credit` - PayPal点数

1. 将&#x200B;**[!UICONTROL Layout]**&#x200B;设置为以下项之一：

   - `Vertical` — （默认）垂直显示PayPal智能按钮。 无论是否选择&#x200B;**[!UICONTROL Enable Guest Checkout]**，购买者都必须登录PayPal或创建PayPal帐户。
   - `Horizontal` — 水平显示PayPal智能按钮。 选择&#x200B;**[!UICONTROL Enable Guest Checkout]**&#x200B;后，**[!UICONTROL Pay with Debit Card or Credit Card]**&#x200B;按钮将显示在PayPal弹出窗口中。 否则，购买者必须登录到PayPal或创建PayPal帐户。

1. 将&#x200B;**[!UICONTROL Size]**&#x200B;设置为以下项之一：

   - `Medium` - 250 x 35像素。
   - `Large` - 350 x 40像素。
   - `Responsive` — （默认）调整到容器的宽度。 最小宽度为100像素，最大宽度为500像素。 高度会根据宽度进行动态调整。

1. 将&#x200B;**[!UICONTROL Shape]**&#x200B;设置为以下项之一：

   - `Pill` — （默认）按钮的形状像药丸（中间较长，两端弯曲）。
   - `Rectangle` — 矩形中的方形形状，不带曲线。

1. 将&#x200B;**[!UICONTROL Color]**&#x200B;设置为以下项之一：

   - `Gold` （默认）
   - `Blue`
   - `Silver`
   - `Black`

#### 功能

功能设置允许您禁用与此PayPal解决方案相关的特定功能。

1. 展开![部分的](../assets/icon-display-expand.png)扩展选择器&#x200B;**[!UICONTROL Features]**。

   ![签出页面设置](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-frontend-experience-settings3.png){width="600" zoomable="yes"}

1. 设置&#x200B;**[!UICONTROL Disable Funding Options]**&#x200B;以确定在&#x200B;_结帐_&#x200B;页面上显示哪些其他PayPal融资选项。

   选定的选项未显示在&#x200B;_签出_&#x200B;页面上。 仅当PayPal支持商店货币和买方地点时，才会显示未选择的选项。 选项包括：

   - PayPal点数
   - 文莫
   - PayPal来宾结帐信用卡图标
   - Elektronisches Lastschriftverfahren — 德国ELV

---
title: PayPal Express签出
description: 了解如何在您的商店中将PayPal Express结帐设置为在线付款解决方案。
exl-id: 0cd90306-cf47-4a5f-8994-6ae96904ae2f
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '3113'
ht-degree: 0%

---

# PayPal Express签出

PayPal Express Checkout使您的客户能够通过信用卡或个人PayPal帐户的安全性进行支付，从而帮助提高销售额。 在结账过程中，客户将被重定向到安全的PayPal网站以完成付款信息。 然后，客户将返回到您的商店以完成剩余的结账过程。 选择“快速结帐”会将您熟悉的PayPal按钮添加到您的商店，据报这将会增加销售额。

>[!IMPORTANT]
>
>**PSD2要求：** <br/>
>从2019年9月14日起，欧洲银行可能会拒绝未满足要求的支付 [PSD2](../getting-started/compliance-payment-services-directive.md) 要求。 PayPal Express Checkout无需执行任何操作即可符合PSD2，因为所有要求都由PayPal处理。

具有当前PayPal帐户的客户只需单击 _[!UICONTROL Check out with PayPal]_按钮。 Express Checkout可以作为独立解决方案使用，也可以与其中一个PayPal多功能一体解决方案一起使用。 如果您已经在网上接受信用卡，则可以提供“快速结帐”作为额外选项，以吸引喜欢使用PayPal付款的新客户。

>[!NOTE]
>
>PayPal已弃用对通过PayPal Express Checkout销售数字商品的支持，并建议使用 [PayPal支付标准](paypal-payments-standard.md) 或其他PayPal支付网关以处理任何订单，包括 [虚拟产品](../catalog/product-create-virtual.md).

## 要求

- 商家： [企业PayPal帐户][1]
- 客户： [个人PayPal帐户][2]

## 快速签出工作流

与其他付款方法不同，PayPal Express结帐允许客户在通常结帐工作流程开始时从产品页面、迷你购物车和购物车结帐。

1. **客户下单**  — 客户单击/点按 _[!UICONTROL Check out with PayPal]_按钮。
1. **客户被重定向到PayPal网站**  — 客户将被重定向到PayPal网站以完成交易。
1. **客户登录到其PayPal帐户**  — 客户必须登录到其PayPal帐户才能完成交易。 付款系统使用来自其PayPal帐户的账单和运送信息。
1. **客户返回到结帐页面**  — 客户将被重定向回商店中的结账页面，以便查看订单。
1. **客户下单**  — 客户下订单，并将订单信息提交到PayPal。
1. **PayPal结算交易** - PayPal接收订单并结算交易。

>[!NOTE]
>
>PayPal Express Checkout不支持具有多个地址的订单。

## 上下文签出

PayPal的 _In-Context签出_ 使得在线支付变得前所未有的容易。 在经过简单的一键或两键式无缝结账期间，客户不会忘记您的商店。 上下文结帐功能在Mac和PC上同样运行良好，在台式计算机、平板电脑和移动设备上提供一致的体验。 要了解更多信息，请参阅 [在Express Checkout中进行上下文检出][5].

![PayPal上下文检出演示](./assets/storefront-paypal-in-context.png){width="700" zoomable="yes"}

[_PayPal上下文检出演示_][6]

在为配置存储时 [!DNL PayPal Express Checkout]，则可以启用此选项。

## 配置PayPal帐户

在商务管理员中设置PayPal Express签出之前，必须在PayPal网站上配置商家帐户。

1. 登录您的PayPal高级帐户，网址为 [manager.paypal.com][3].

1. 转到 **[!UICONTROL Service Settings]** > **[!UICONTROL Hosted Checkout Pages]** > **[!UICONTROL Set Up]** 并进行以下设置：

   - **[!UICONTROL AVS]**: `No`
   - **[!UICONTROL CSC]**: `No`
   - **[!UICONTROL Enable Secure Token]**: `Yes`

1. 单击 **[!UICONTROL Save Changes]**.

1. 设置另一个用户（由PayPal推荐）：

   - 转到 [manager.paypal.com][3] 并登录到您的帐户。

   - 要设置另一个用户，请按照说明操作。

   - 单击 **[!UICONTROL Update]**.

## 在Commerce中设置PayPal Express签出

您可以同时激活两个PayPal解决方案：PayPal Express Checkout，以及一体化解决方案。 如果启用其他解决方案，则会自动停用以前使用的解决方案。

>[!NOTE]
>
>单击 **[!UICONTROL Save Config]** 以保存进度。

### 步骤1：开始配置

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中，展开 **[!UICONTROL Sales]** 并选择 **[!UICONTROL Payment Methods]**.

1. 如果您的安装有多个网站、商店或视图，请设置 **[!UICONTROL Store View]** 到要应用此配置的商店视图。

1. 在 _[!UICONTROL Merchant Location]_部分，选择&#x200B;**[!UICONTROL Merchant Country]**公司所在的位置。

   此设置确定配置中显示的PayPal解决方案的选择。

   ![商家国家/地区](../configuration-reference/sales/assets/payment-methods-merchant-location.png){width="600" zoomable="yes"}

1. 下 _[!UICONTROL Recommended Solutions]_，单击&#x200B;**[!UICONTROL Configure]**对象&#x200B;**[!UICONTROL PayPal Express Checkout]**.

   ![配置PayPal Express签出](./assets/paypal-express-checkout.png){width="600"}

### 步骤2：启用并连接您的PayPal帐户

1. 如果需要，请展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Required PayPal Settings]** 部分。

   ![连接您的PayPal帐户](./assets/paypal-express-required.png){width="600" zoomable="yes"}

1. 连接帐户以进行测试或生产：

   - 对于测试（开发）模式，单击 **[!UICONTROL Sandbox Credentials]** 并输入您的 [PayPal沙盒][7] 凭据。
   - 对于生产模式，单击 **[!UICONTROL Connect with PayPal]** 并输入您的生产帐户凭据。

   验证连接后，您可以继续。

1. 设置 **[!UICONTROL Enable this Solution]** 到 `Yes`.

1. 要启用 [PayPal上下文结帐](#in-context-checkout)：

   - 设置 **[!UICONTROL Enable In-Context Checkout Experience]** 到 `Yes`.

   - 输入您的贝宝 **[!UICONTROL Merchant Account ID]**.

     您的商户帐户ID在您的PayPal企业帐户配置文件中。

>[!NOTE]
>
>[PayPal点数](paypal.md#paypal-credit-and-pay-later) 默认对此付款选项启用。

### 步骤3：完成所需的PayPal设置

1. 如果需要，请展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Express Checkout]** 部分。

   ![PayPal Express签出所需的设置](./assets/paypal-express-settings.png){width="600" zoomable="yes"}

1. （可选）输入 **[!UICONTROL Email Associated with PayPal Merchant Account]**.

   >[!IMPORTANT]
   >
   >电子邮件地址区分大小写。 要接收付款，您输入的电子邮件地址必须与在PayPal商家帐户中指定的电子邮件地址匹配。

   如果您没有PayPal帐户，请单击 **[!UICONTROL Start accepting payments via PayPal]**.

1. 设置 **[!UICONTROL API Authentication Methods]** 更改为以下任一项：

   - `API Signature`  — 此PayPal身份验证方法最易于实施，它基于您的用户名、密码以及标识您的帐户的唯一字符和数字字符串。 API签名凭据不会过期。
   - `API Certificate`  — 此PayPal身份验证方法基于您的用户名、密码和可下载的证书，因此更加安全。 API凭据将在三年后过期，必须续订。

   如有必要，请完成以下操作：

   - **[!UICONTROL API Username]**
   - **[!UICONTROL API Password]**
   - **[!UICONTROL API Signature]**

1. 如果您使用的是来自沙盒帐户的凭据，请设置 **[!UICONTROL Sandbox Mode]** 到 `Yes`.

   在沙盒中测试配置时，仅使用 [信用卡号码][4] 由PayPal推荐。 当您准备好进入生产环境时，请返回到配置并将沙盒模式设置为 `No` 并连接到您的生产PayPal帐户。

1. 如果您的系统使用代理服务器在Commerce和PayPal支付系统之间建立连接，请设置 **[!UICONTROL API Uses Proxy]** 到 `Yes` 并完成以下操作：

   - **[!UICONTROL Proxy Host]**
   - **[!UICONTROL Proxy Port]**

在此一系列步骤结束时，已完成所需的PayPal设置。 您可以继续使用基本设置和高级设置，也可以单击 **[!UICONTROL Save Config]** 并稍后返回以调整配置

### 步骤4：设置广告PayPal Credit/广告PayPal PayLater（可选）

从2.4.3版本开始，在包括PayPal的部署中支持PayPal PayLater。 此功能允许购物者以每两周一次分期付款的方式支付订单，而不是在购买时支付全额。 弃用PayPal信用体验。

设置 **[!UICONTROL Enable PayPal PayLater Experience]** 更改为以下任一项：

- `Yes`  — 设置广告PayPal PayLater
- `No`  — 设置广告PayPal信用

>[!NOTE]
>
>此 **[!UICONTROL Enable PayPal PayLater Experience]** 设置不会禁用 [!DNL PayPal PayLater] 功能且未移除 **_[!UICONTROL PayPal PayLater]_** 店面的按钮。 禁用两者 **_[!UICONTROL PayPal PayLater]_** 和 **_[!UICONTROL PayPal Credit]_** 按钮时，您必须选择 `PayPal Credit` 的值 **[!UICONTROL Disable Funding Options]** 设置([!UICONTROL Advanced Settings] 下 [!UICONTROL Frontend Experience Settings])。

#### 广告PayPal点数

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Advertise PayPal Credit]** 部分。

1. 要获取您的帐户信息，请单击 **[!UICONTROL Get Publisher ID from PayPal]** 然后按照说明操作。

1. 输入您的 **[!UICONTROL Publisher ID]**.

   ![广告PayPal点数](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit.png){width="600" zoomable="yes"}

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Home Page]** 部分。

1. 要在页面上放置横幅，请设置 **[!UICONTROL Display]** 到 `Yes`.

1. 设置 **[!UICONTROL Position]** 更改为以下任一项：

   - `Header (center)`
   - `Sidebar (right)`

1. 设置 **[!UICONTROL Size]** 更改为以下任一项：

   - `190 x 100`
   - `234 x 60`
   - `300 x 50`
   - `468 x 60`
   - `728 x 90`
   - `800 x 66`

   ![广告PayPal点数主页设置](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit-home-page.png){width="600" zoomable="yes"}

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 其余部分并重复上述步骤：

   - [!UICONTROL Catalog Category Page]
   - [!UICONTROL Catalog Product Page]
   - [!UICONTROL Checkout Cart Page]

#### 广告PayPal PayLater

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Advertise PayPal PayLater]** 部分。

1. 设置 **[!UICONTROL Enable PayPal PayLater]** 到 `Yes`.

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Home Page]** 部分。

1. 要在页面上放置横幅，请设置 **[!UICONTROL Display]** 到 `Yes`.

1. 设置 **[!UICONTROL Position]** 更改为以下任一项：

   - `Header (center)`
   - `Sidebar`

1. 设置 **[!UICONTROL Style Layout]** 更改为以下任一项：

   - `Text`
   - `Flex`

1. 对象 [!UICONTROL Style Layout] **[!UICONTROL Text]** 仅限，设置 **[!UICONTROL Logo Type]** 更改为以下任一项：

   - `Primary`
   - `Alternative`
   - `Inline`
   - `None`

1. 对象 [!UICONTROL Style Layout] **[!UICONTROL Text]** 仅限，设置 **[!UICONTROL Logo Position]** 更改为以下任一项：

   - `Left`
   - `Right`
   - `Top`

1. 对象 [!UICONTROL Style Layout] **[!UICONTROL Text]** 仅限，设置 **[!UICONTROL Text Color]** 更改为以下任一项：

   - `Black`
   - `White`
   - `Monochrome`
   - `Grayscale`

1. 对象 [!UICONTROL Style Layout] **[!UICONTROL Text]** 仅限，设置 **[!UICONTROL Text Size]** 更改为以下任一项：

   - `10px`
   - `11px`
   - `12px`
   - `13px`
   - `14px`
   - `15px`
   - `16px`

1. 对象 [!UICONTROL Style Layout] **[!UICONTROL Flex]** 仅限，设置 **[!UICONTROL Ratio]** 更改为以下任一项：

   - `1x1`
   - `1x4`
   - `8x1`
   - `20x1`

1. 对象 [!UICONTROL Style Layout] **[!UICONTROL Flex]** 仅限，设置 **[!UICONTROL Color]** 更改为以下任一项：

   - `Blue`
   - `Black`
   - `White`
   - `White No Border`
   - `Gray`
   - `Monochrome`
   - `Grayscale`

   ![广告PayPal点数主页设置](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-paylater-home-page.png){width="600" zoomable="yes"}

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 其余部分并重复上述步骤：

   - [!UICONTROL Catalog Product Page]
   - [!UICONTROL Checkout Cart Page]
   - [!UICONTROL Checkout Payment Step]
   - [!UICONTROL Catalog Category Page]

### 步骤5：完成基本设置

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Basic Settings - PayPal Express Checkout]** 部分。

   ![基本设置](../configuration-reference/sales/assets/payment-methods-paypal-express-checkout-basic-settings.png){width="600" zoomable="yes"}

1. 对象 **[!UICONTROL Title]**，输入在结账时标识此付款方式的标题。

   建议您使用标题 _PayPal_ 所有商店视图。

1. 如果您提供多种支付方式，请输入一个数字 **[!UICONTROL Sort Order]** 确定与其他支付方式一起列出时PayPal Express Checkout出现的顺序。

   此数字相对于其他支付方式。 (`0` =第一个， `1` =秒， `2` =第三，依此类推。)

1. 设置 **[!UICONTROL Payment Action]** 更改为以下任一项：

   - `Authorization`  — 批准购买并暂停资金。 该款项于到期前不会提取。 _已捕获_ 是商贩送的。
   - `Sale`  — 采购金额已获授权并立即从客户账户中提取。
   - `Order`  — 在PayPal的客户余额、银行帐户或信用卡中，不捕获或授权订单金额。 订单付款活动表示PayPal付款系统与商家之间的协议。 它使商家能够在长达29天的时间内，从客户买方帐户中获取一个或多个最高至订购总额的金额。 在订购资金后，商家可以在接下来的29天内随时抓获这些资金。 只能通过创建一个或多个发票从Commerce管理员处捕获订单金额。

1. 要显示 _[!UICONTROL Check out with PayPal]_产品页面上的按钮，设置&#x200B;**[!UICONTROL Display on Product Details Page]**到 `Yes`.

1. 如果付款活动设置为 `Order`，完成以下操作

   - **[!UICONTROL Authorization Honor Period (days)]**  — 确定主要授权保持有效的时间。 该值应等于您的PayPal商家帐户中的相应值。 您的PayPal商家帐户中的默认值为 `3`. 要增加此数量，您必须联系PayPal。 授权于最后一天美国太平洋时间晚上11:49失效。

   - **[!UICONTROL Order Valid Period (days)]**  — 确定订单保持有效的时间。 订单无效后，您将无法再为其创建发票。 指定等于PayPal商家帐户中的订单有效期间值的值。 您的PayPal商家帐户中的默认值为 `29`. 要更改此号码，您必须联系PayPal。

   - **[!UICONTROL Number of Child Authorizations]**  — 指定单个订单的最大授权数量，该数量确定您可以为订单创建的联机部分发票的最大数量。 此值应等于您的PayPal商家帐户中的相应设置。 PayPal帐户中的默认子授权数量为 `1`. 要增加此数量，您必须联系PayPal。

### 步骤6：完成高级设置

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Advanced Settings]** 部分。

   ![高级设置 — PayPal Express签出](../configuration-reference/sales/assets/payment-methods-paypal-express-checkout-advanced-settings.png){width="600" zoomable="yes"}

1. 设置 **[!UICONTROL Display on Shopping Cart]** 到 `Yes`.

1. 设置 **[!UICONTROL Payment Applicable From]** 更改为以下任一项：

   - `All Allowed Countries`  — 来自您商店配置中指定的所有国家/地区的客户均可以使用此付款方法。
   - `Specific Countries`  — 选择此选项后， _[!UICONTROL Payment from Specific Countries]_列表出现。 要选择多个国家/地区，请按住Ctrl键(PC)或Command键(Mac)并单击每个项目。

1. 要将与支付系统的通信写入日志文件，请设置 **[!UICONTROL Debug Mode]** 到 `Yes`.

   PayPal Payments Advanced的日志文件为 `_payflow_advanced.log`.

   >[!NOTE]
   >
   >根据PCI数据安全标准，信用卡信息不会记录在日志文件中。

1. 要启用主机真实性验证，请设置 **[!UICONTROL Enable SSL Verification]** 到 `Yes`.

1. 要显示PayPal站点中按行项目列出的客户订单的完整汇总，请设置 **[!UICONTROL Transfer Cart Line Items]** 到 `Yes`.

1. 要在摘要中包含最多十个配送选项，请设置 **[!UICONTROL Transfer Shipping Options]** 到 `Yes`. （仅当将行项目设置为转移时，才会显示此选项。）

1. 要确定用于PayPal接受按钮的图像类型，请设置 **[!UICONTROL Shortcut Buttons Flavor]** 更改为以下任一项：

   - `Dynamic`  — （推荐）显示可从PayPal服务器动态更改的图像。
   - `Static`  — 显示无法动态更改的特定图像。

1. 要允许没有PayPal帐户的客户使用此方法购物，请设置 **[!UICONTROL Enable PayPal Guest Checkout]** 到 `Yes`.

1. 设置 **[!UICONTROL Require Customer's Billing Address]** 更改为以下任一项：

   - `Yes`  — 所有购买都需要客户的账单地址。
   - `No`  — 任何购买均不需要客户的账单地址。
   - `For Virtual Quotes Only`  — 仅需要客户的虚拟报价单帐单地址。

   >[!NOTE]
   >
   >必须通过PayPal技术支持为商户帐户启用此功能。

1. （可选）设置 **[!UICONTROL Billing Agreement Signup]** 允许客户签署 [billing agreement（计费协议）](paypal-billing-agreements.md) 客户帐户中无可用的有效帐单协议时，在PayPal支付系统中与您的商店联系：

   - `Auto`  — 客户可以在快速结帐流程中签署帐单协议，或使用其他付款方式。
   - `Ask Customer`  — 客户可以决定是否在Express Checkout流程中签署计费协议。
   - `Never`  — 客户无法在Express Checkout流程中签署计费协议。

   >[!NOTE]
   >
   >商家必须询问 [PayPal商家技术支持](https://developer.paypal.com/support/) 以在其帐户中启用开单协议。 此 _帐单协议注册_ 仅在PayPal确认您的商户帐户已启用开单协议后才启用参数。

1. 要允许客户从PayPal网站完成交易，而无需返回到您的商店进行订单审核，请设置 **[!UICONTROL Skip Order Review Step]** 到 `Yes`.

1. 根据存储需要，完成其他部分：

   - [PayPall记帐协议设置](#paypal-billing-agreement-settings)
   - [结算报表设置](#settlement-report-settings)
   - [前端体验设置](#frontend-experience-settings)
   - [自定义智能按钮](#customize-smart-buttons)
   - [功能](#features)

1. 完成后，单击 **[!UICONTROL Save Config]**.

#### PayPal计费协议设置

A [billing agreement（计费协议）](paypal-billing-agreements.md) 是商家与客户之间签订的销售协议，该协议已获得PayPal授权用于多个订单。 在结账过程中，“帐单协议”付款选项仅对已与贵公司签订帐单协议的客户显示。 在PayPal授权协议后，支付系统会颁发一个唯一的参考ID以标识与协议关联的每个订单。 与采购订单类似，客户与您的公司之间可以设置的帐单协议数没有限制。

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL PayPal Billing Agreement Settings]** 部分。

   ![帐单协议设置](../configuration-reference/sales/assets/payment-methods-paypal-express-checkout-billing-agreement-settings.png){width="600" zoomable="yes"}

1. 设置 **[!UICONTROL Enabled]** 到 `Yes`.

1. 对象 **[!UICONTROL Title]**，输入在结账期间标识PayPal计费协议方法的标题。

1. 如果您提供多种支付方式，请在 **[!UICONTROL Sort Order]** 确定在结帐期间与其他付款方法一起列出帐单协议时显示的顺序的字段。

1. 设置 **[!UICONTROL Payment Action]** 更改为以下任一项：

   - `Authorization`  — 批准购买并暂停资金。 该金额在商户将该金额“扣押”前不予提取。
   - `Sale`  — 采购金额已获授权并立即从客户账户中提取。

1. 设置 **[!UICONTROL Payment Applicable From]** 更改为以下任一项：

   - `All Allowed Countries`  — 来自您商店配置中指定的所有国家/地区的客户均可以使用此付款方法。
   - `Specific Countries`  — 选择此选项后， _[!UICONTROL Payment from Specific Countries]_列表出现。 要选择多个国家/地区，请按住Ctrl键(PC)或Command键(Mac)并单击每个国家/地区。

1. 要在日志文件中记录与支付系统的通信，请设置 **[!UICONTROL Debug Mode]** 到 `Yes`.

   >[!NOTE]
   >
   >日志文件存储在服务器上，只有开发人员才能访问。 根据PCI数据安全标准，信用卡信息不会记录在日志文件中。

1. 要启用SSL验证，请设置 **[!UICONTROL Enable SSL Verification]** 到 `Yes`.

1. 要在PayPal支付页面上显示客户订单中每个行项目的汇总，请设置 **[!UICONTROL Transfer Cart Line Items]** 到 `Yes`.

1. 要允许客户从其客户帐户的控制板启动计费协议，请设置 **[!UICONTROL Allow in Billing Agreement Wizard]** 到 `Yes`.

#### 结算报表设置

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Settlement Report Settings]** 部分。

   ![结算报表设置](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-settlement-report-settings.png){width="600" zoomable="yes"}

1. 对象 **[!UICONTROL SFTP Credentials]**，请执行以下操作：

   - 如果您已注册PayPal安全FTP服务器，请输入以下SFTP登录凭据：

      - 登录
      - 密码

   - 要在之前运行测试报告，请执行以下操作 _上线_ 在您的网站上使用Express Checkout，设置 **[!UICONTROL Sandbox Mode]** 到 `Yes`.

   - 输入 **[!UICONTROL Custom Endpoint Hostname or IP Address]**.

     默认情况下，该值为： `reports.paypal.com`

   - 输入 **[!UICONTROL Custom Path]** 保存报告的位置。

     默认情况下，该值为： `/ppreports/outgoing`

1. 要根据计划生成报表，请完成 **[!UICONTROL Scheduled Fetching]** 设置：

   - 设置 **[!UICONTROL Enable Automatic Fetching]** 到 `Yes`.

   - 设置 **[!UICONTROL Schedule]** 更改为以下任一项：

      - `Daily`
      - `Every 3 Days`
      - `Every 7 Days`
      - `Every 10 Days`
      - `Every 14 Days`
      - `Every 30 Days`
      - `Every 40 Days`

     PayPal会将每个报表保留45天。

   - 设置 **[!UICONTROL Time of Day]** 到您希望生成报告时的小时、分钟和秒。

#### 前端体验设置

使用前端体验设置选择要在您的网站上显示的PayPal徽标，并自定义您的PayPal商家页面的外观。

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Frontend Experience Settings]** 部分。

   ![前端体验设置](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-frontend-experience-settings1.png){width="600" zoomable="yes"}

1. 选择 **[!UICONTROL PayPal Product Logo]** 出现在你商店的PayPal区块中。

   PayPal徽标有四种样式和两种尺寸：

   - `No Logo`
   - `We Prefer PayPal (150 x 60 or 150 x 40)`
   - `Now Accepting PayPal (150 x 60 or 150 x 40)`
   - `Payments by PayPal (150 x 60 or 150 x 40)`
   - `Shop Now Using PayPal (150 x 60 or 150 x 40)`

1. 要自定义PayPal商家页面的外观，请执行以下操作：

   - 输入 **[!UICONTROL Page Style]** 要应用到您的PayPal商家页面的：

      - `paypal`  — 使用PayPal页面样式。
      - `primary`  — 使用您标识为 _主要_ 帐户个人资料中的样式。
      - `your_custom_value`  — 使用在您的帐户配置文件中指定的自定义付款页面样式。

   - 对象 **[!UICONTROL Header Image URL]**，输入要显示在付款页面左上角的图像的URL。 最大文件大小为750像素宽x 90像素高。

     >[!NOTE]
     >
     >PayPal建议将映像驻留在安全(https)服务器上。 否则，浏览器可能会警告 _该页面包含安全和非安全项目_.

   - 要设置页面的颜色，请输入六个字符的十六进制代码，而不是 `#` 符号，表示下列各项：

      - **[!UICONTROL Header Background Color]**  — 签出页面标题的背景颜色。
      - **[!UICONTROL Header Border Color]**  — 标题周围两像素边框的颜色。
      - **[!UICONTROL Page Background Color]**  — 结账页面以及标题和付款表单周围的背景颜色。

#### 自定义智能按钮

此 _智能支付按钮_ 功能允许您自定义PayPal按钮，该按钮可显示在“结帐”、“产品详细信息”、“购物车”和“迷你购物车”页面上。 PayPal的内部研究表明，默认选项具有高度可识别性，可能会提高购买率，但它们的默认设置可能与你的商店风格不符。 您可以选择：

- PayPal按钮的大小、颜色和形状
- 显示在PayPal按钮上的文本
- 显示多个按钮时的布局（水平或垂直）

要自定义按钮，请展开 ![扩展选择器](../assets/icon-display-expand.png) 并调整设置：

- **[!UICONTROL Checkout Page]**
- **[!UICONTROL Product Pages]**
- **[!UICONTROL Cart Page]**
- **[!UICONTROL Mini Cart]**

![签出页面设置](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-frontend-experience-settings2.png){width="600" zoomable="yes"}

**_要为每种页面类型配置按钮显示，请执行以下操作：_**

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 部分。

1. 设置 **[!UICONTROL Customize Button]** 到 `Yes`.

1. 要设置PayPal在智能支付按钮上显示的文本，请设置 **[!UICONTROL Label]** 更改为以下任一项：

   - `Checkout` - PayPal结账
   - `Pay` - PayPal结账
   - `Buy Now`  — 使用PayPal立即购买
   - `PayPal` - PayPal
   - `Installment`  - PayPal
   - `Credit` - PayPal信用

1. 设置 **[!UICONTROL Layout]** 更改为以下任一项：

   - `Vertical`  — （默认）垂直显示PayPal智能按钮。 购买者必须登录到PayPal或创建一个PayPal帐户，无论 **[!UICONTROL Enable Guest Checkout]** 已选中。
   - `Horizontal`  — 水平显示PayPal智能按钮。 时间 **[!UICONTROL Enable Guest Checkout]** ，则 **[!UICONTROL Pay with Debit Card or Credit Card]** 按钮将显示在PayPal弹出窗口中。 否则，购买者必须登录到PayPal或创建PayPal帐户。

1. 设置 **[!UICONTROL Size]** 更改为以下任一项：

   - `Medium` - 250像素x 35像素。
   - `Large` - 350像素x 40像素。
   - `Responsive`  — （默认）调整到容器的宽度。 最小宽度为100像素，最大宽度为500像素。 高度会根据宽度进行动态调整。

1. 设置 **[!UICONTROL Shape]** 更改为以下任一项：

   - `Pill`  — （默认）按钮的形状类似药丸（中间较长，两端弯曲）。
   - `Rectangle`  — 方形形状，不带曲线，在矩形中。

1. 设置 **[!UICONTROL Color]** 更改为以下任一项：

   - `Gold` （默认）
   - `Blue`
   - `Silver`
   - `Black`

#### 功能

功能设置允许您禁用与此PayPal解决方案相关的特定功能。

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Features]** 部分。

   ![签出页面设置](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-frontend-experience-settings3.png){width="600" zoomable="yes"}

1. 设置 **[!UICONTROL Disable Funding Options]** 以确定其他哪些PayPal融资选项显示在 _结帐_ 页面。

   所选的选项不会显示在 _结帐_ 页面。 仅当PayPal支持商店货币和买方地点时，才会显示未选择的选项。 选项包括：

   - PayPal点数
   - 文莫
   - PayPal来宾结帐信用卡图标
   - Elektronisches Lastschriftverfahren — 德国ELV

[1]: https://www.paypal.com/webapps/mpp/how-to-sell-online
[2]: https://www.paypal.com/webapps/mpp/buying-online
[3]: https://manager.paypal.com/
[4]: https://www.paypalobjects.com/en_AU/vhelp/paypalmanager_help/credit_card_numbers.htm
[5]: https://www.paypal.com/rs/webapps/mpp/express-checkout
[6]: https://demo.paypal.com/us/demo/navigation?merchant=bigbox&amp;amp;page=incontextProductCheckout
[7]: https://developer.paypal.com/docs/api-basics/sandbox/

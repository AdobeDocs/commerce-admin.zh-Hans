---
title: PayPal支付标准
description: 了解如何在您的商店中将PayPal Payments Standard设置为在线支付解决方案。
exl-id: b4024dac-34d7-4f1a-ad9d-0fc406194609
feature: Payments
badgePaas: label="仅限PaaS" type="Informative" url="https://experienceleague.adobe.com/zh-hans/docs/commerce/user-guides/product-solutions" tooltip="仅适用于云项目(Adobe管理的PaaS基础架构)和内部部署项目上的Adobe Commerce 。"
source-git-commit: cace9d1de00955494d8bc607c017778ff7df4806
workflow-type: tm+mt
source-wordcount: '2081'
ht-degree: 0%

---

# PayPal支付标准

[PayPal Payments Standard](https://developer.paypal.com/docs/paypal-payments-standard/mobile-paypal-payments-standard/)是接受在线付款的最简单方式。 只需在商店中添加结帐按钮，即可为客户提供信用卡和PayPal付款的便利。

>[!NOTE]
>
>对于美国以外的商家，它称为&#x200B;_PayPal Website Payments Standard_。

借助PayPal Payments Standard，您可以在移动设备上刷卡。 这里没有月费，你可以通过eBay支付。 支持的信用卡包括Visa、MasterCard、Discover和American Express。 此外，客户可以直接从其个人PayPal帐户付款。 PayPal支付标准可在PayPal全球参考列表上的所有国家/地区使用。

>[!IMPORTANT]
>
>**PSD2要求：** <br/>
>从2019年9月14日起，欧洲银行可能会拒绝不符合[PSD2](../getting-started/compliance-payment-services-directive.md)要求的支付。 PayPal Payments Standard无需采取任何操作即可符合PSD2，因为所有要求都由PayPal处理。

## 商家要求

- [PayPal企业帐户](https://www.paypal.com/webapps/mpp/how-to-sell-online)

## 签出工作流

对于客户，如果其个人PayPal帐户上的信用卡信息是最新的，则PayPal Payments Standard仅需一步即可完成。

1. **客户下订单** — 客户单击/点按&#x200B;_立即付款_&#x200B;按钮以完成购买。

1. **PayPal处理交易** — 客户将被重定向到PayPal网站以完成交易。

## 设置PayPal Payments Standard

>[!NOTE]
>
>PayPal Payments Standard不能与任何其他PayPal方法（包括快速结账）同时使用。 如果您更改支付解决方案，则以前使用的支付解决方案将被禁用。

>[!TIP]
>
>随时单击&#x200B;**[!UICONTROL Save Config]**&#x200B;以保存进度。

### 步骤1：开始配置

此设置方法假定您拥有现有的PayPal帐户。

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧面板中，展开&#x200B;**[!UICONTROL Sales]**&#x200B;并选择&#x200B;**[!UICONTROL Payment Methods]**。

1. 如果您的Commerce安装有多个网站、商店或视图，请将&#x200B;**[!UICONTROL Store View]**&#x200B;设置为要应用此配置的商店视图。

1. 在&#x200B;_[!UICONTROL Merchant Location]_&#x200B;部分中，选择您的公司所在的&#x200B;**[!UICONTROL Merchant Country]**。

   此设置确定配置中显示的PayPal解决方案的选择。

   ![商家国家/地区](../configuration-reference/sales/assets/payment-methods-merchant-location.png){width="600" zoomable="yes"}

1. 展开&#x200B;**[!UICONTROL PayPal All-in-One Payment Solutions]**&#x200B;并单击&#x200B;**[!UICONTROL Configure]**&#x200B;的&#x200B;**[!UICONTROL Payments Standard]**。

   ![PayPal支付标准](./assets/paypal-payments-standard.png){width="700" zoomable="yes"}

### 步骤2：启用并连接您的PayPal帐户

![PayPal支付标准配置](./assets/paypal-payments-display.png){width="600" zoomable="yes"}

1. 连接帐户以进行测试或生产：

   - 对于测试（开发）模式，请单击&#x200B;**[!UICONTROL Sandbox Credentials]**&#x200B;并输入您的[PayPal沙盒](https://developer.paypal.com/docs/api-basics/sandbox/)凭据。
   - 对于生产模式，请单击&#x200B;**[!UICONTROL Connect with PayPal]**&#x200B;并输入您的生产帐户凭据。

   验证连接后，您可以继续。

1. 将&#x200B;**[!UICONTROL Enable this Solution]**&#x200B;设置为`Yes`。

1. 如果要为客户提供点数[PayPal](paypal.md#paypal-credit-and-pay-later)，请将&#x200B;**[!UICONTROL Enable PayPal Credit]**&#x200B;设置为`Yes`。

### 步骤3：完成支付标准设置

1. 展开![部分的](../assets/icon-display-expand.png)扩展选择器&#x200B;**[!UICONTROL Payments Standard]**。

   ![必需的设置](../configuration-reference/sales/assets/payment-methods-paypal-payments-standard-required.png){width="600" zoomable="yes"}

1. 输入&#x200B;**[!UICONTROL Email Associated with your PayPal Merchant Account]**。

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

1. 如果您的系统使用代理服务器在Adobe Commerce或Magento Open Source与PayPal支付系统之间建立连接，请将&#x200B;**[!UICONTROL API Uses Proxy]**&#x200B;设置为`Yes`并完成以下操作：

   - **[!UICONTROL Proxy Host]**
   - **[!UICONTROL Proxy Port]**

### 步骤4：设置广告PayPal Credit/广告PayPal PayLater（可选）

从2.4.3版本开始，在包括PayPal的部署中支持PayPal PayLater。 此功能允许购物者以每两周一次分期付款的方式支付订单，而不是在购买时支付全额。 弃用PayPal信用体验。

将&#x200B;**[!UICONTROL Enable PayPal PayLater Experience]**&#x200B;设置为以下项之一：

- `Yes` — 设置广告PayPal PayLater
- `No` — 设置广告PayPal点数

#### 广告PayPal点数

1. 展开![部分的](../assets/icon-display-expand.png)扩展选择器&#x200B;**[!UICONTROL Advertise PayPal Credit]**。

   ![通告PayPal点数主页设置](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit-home-page.png){width="600" zoomable="yes"}

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

1. 展开![扩展选择器](../assets/icon-display-expand.png)其余部分并重复上述步骤：

   - **[!UICONTROL Catalog Category Page]**
   - **[!UICONTROL Catalog Product Page]**
   - **[!UICONTROL Checkout Cart Page]**

#### 广告PayPal PayLater

1. 展开![部分的](../assets/icon-display-expand.png)扩展选择器&#x200B;**[!UICONTROL Advertise PayPal PayLater]**。

1. 将&#x200B;**[!UICONTROL Enable PayPal PayLater]**&#x200B;设置为`Yes`。

1. 展开![部分的](../assets/icon-display-expand.png)扩展选择器&#x200B;**[!UICONTROL Home Page]**。

   ![通告PayPal点数主页设置](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-paylater-home-page.png){width="600" zoomable="yes"}

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

1. 展开![扩展选择器](../assets/icon-display-expand.png)其余部分并重复上述步骤：

   - **[!UICONTROL Catalog Product Page]**
   - **[!UICONTROL Checkout Cart Page]**
   - **结帐付款步骤**
   - **[!UICONTROL Catalog Category Page]**

### 步骤5：完成基本设置

1. 展开![部分的](../assets/icon-display-expand.png)扩展选择器&#x200B;**[!UICONTROL Basic Settings - PayPal Website Payments Standard]**。

   ![基本设置](./assets/paypal-payments-basic.png){width="600" zoomable="yes"}

1. 对于&#x200B;**[!UICONTROL Title]**，输入在结帐时标识此付款方式的标题。

   建议对所有商店视图使用标题&#x200B;_PayPal_。

1. 如果您提供多种支付方式，请输入&#x200B;**[!UICONTROL Sort Order]**&#x200B;的数字，以确定与其他支付方式一起列出时PayPal支付标准出现的顺序。

   此数字相对于其他支付方式。 （`0` =第一，`1` =第二，`2` =第三，依此类推。）

1. 将&#x200B;**[!UICONTROL Payment Action]**&#x200B;设置为以下项之一：

   - `Authorization` — 批准购买并暂停资金。 该金额在商户缴获前不会提取。
   - `Sale` — 已授权并立即从客户帐户中收回购买金额。

1. 要在产品页面上显示&#x200B;_[!UICONTROL Check out with PayPal]_&#x200B;按钮，请将&#x200B;**[!UICONTROL Display on Product Details Page]**&#x200B;设置为`Yes`。

### 步骤6：完成高级设置

1. 展开![部分的](../assets/icon-display-expand.png)扩展选择器&#x200B;**[!UICONTROL Advanced Settings]**。

   ![高级设置](../configuration-reference/sales/assets/payment-methods-paypal-payment-standard-advanced.png){width="600" zoomable="yes"}

1. 若要使购物车和迷你购物车均可使用PayPal支付标准，请将&#x200B;**[!UICONTROL Display on Shopping Cart]**&#x200B;设置为`Yes`。

1. 将&#x200B;**[!UICONTROL Payment from Applicable Countries]**&#x200B;设置为以下项之一：

   - `All Allowed Countries` — 来自您商店配置中指定的所有[国家/地区](../getting-started/store-details.md#country-options)的客户都可以使用此付款方式。
   - `Specific Countries` — 选择此选项后，将显示&#x200B;_[!UICONTROL Payment from Specific Countries]_&#x200B;列表。 要选择多个国家/地区，请按住Ctrl键(PC)或Command键(Mac)并单击每个选项。

1. 若要在日志文件中记录与付款系统的通信，请将&#x200B;**[!UICONTROL Debug Mode]**&#x200B;设置为`Yes`。

   >[!NOTE]
   >
   >日志文件存储在服务器上，只有开发人员才能访问。 根据PCI数据安全标准，信用卡信息不会记录在日志文件中。

1. 要启用SSL验证，请将&#x200B;**[!UICONTROL Enable SSL Verification]**&#x200B;设置为`Yes`。

1. 若要在PayPal支付页面上显示订单中每个行项目的摘要，请将&#x200B;**[!UICONTROL Transfer Cart Line Items]**&#x200B;设置为`Yes`。

   要在摘要中包含最多十个配送选项，请将&#x200B;**[!UICONTROL Transfer Shipping Options]**&#x200B;设置为`Yes`。 （仅当将行项目设置为转移时，才会显示此选项。）

1. 要确定用于PayPal接受按钮的图像类型，请将&#x200B;**[!UICONTROL Shortcut Buttons Flavor]**&#x200B;设置为以下项之一：

   - `Dynamic` - （推荐）显示可从PayPal服务器动态更改的图像。
   - `Static` — 显示无法动态更改的特定图像。

1. 要允许没有PayPal帐户的客户使用此方法购买，请将&#x200B;**[!UICONTROL Enable PayPal Guest Checkout]**&#x200B;设置为`Yes`。

1. 将&#x200B;**[!UICONTROL Require Customer's Billing Address]**&#x200B;设置为以下项之一：

   - `Yes` — 需要所有购买的客户帐单地址。
   - `No` — 任何购买均不需要客户帐单地址。
   - `For Virtual Quotes Only` — 仅需要虚拟报价的客户帐单地址。

1. 要允许客户在客户帐户中没有可用的有效帐单协议时与您的商店签订[PayPal帐单协议](paypal-billing-agreements.md)，请将&#x200B;**[!UICONTROL Billing Agreement Signup]**&#x200B;设置为以下项之一：

   - `Auto` — 客户可以在快速结帐流程中签署帐单协议，或使用其他付款方式。
   - `Ask Customer` — 客户可以决定是否在Express Checkout工作流中签署帐单协议。
   - `Never` — 客户无法在Express Checkout工作流中签署帐单协议。

   >[!NOTE]
   >
   >商家必须请求PayPal商家技术支持以在其帐户中启用帐单协议。 只有在PayPal确认您的商户帐户已启用帐单协议后，才能启用&#x200B;_帐单协议注册_&#x200B;参数。

1. 要允许客户从PayPal网站完成交易而不返回商店进行订单审核，请将&#x200B;**[!UICONTROL Skip Order Review Step]**&#x200B;设置为`Yes`。

### 步骤7：完成并保存配置设置

1. 根据存储需要，完成以下部分：

   - [PayPal计费协议设置](#paypal-billing-agreement-settings)
   - [结算报表设置](#settlement-report-settings)
   - [前端体验设置](#frontend-experience-settings)

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

   - 要在使用Express Checkout在您的网站上正式启用之前运行测试报告，请将&#x200B;**[!UICONTROL Sandbox Mode]**&#x200B;设置为`Yes`。

   - 输入&#x200B;**[!UICONTROL Custom Endpoint Hostname or IP Address]**。

     默认情况下，值为`reports.paypal.com`。

   - 输入保存报告的&#x200B;**[!UICONTROL Custom Path]**。

     默认情况下，值为`/ppreports/outgoing`。

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

使用&#x200B;_[!UICONTROL Frontend Experience Settings]_&#x200B;选择要在您的网站上显示的PayPal徽标，并自定义PayPal商家页面的外观。

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

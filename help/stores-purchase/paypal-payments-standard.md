---
title: PayPal支付标准
description: 了解如何在您的商店中将PayPal Payments Standard设置为在线支付解决方案。
exl-id: b4024dac-34d7-4f1a-ad9d-0fc406194609
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '2073'
ht-degree: 0%

---

# PayPal支付标准

[PayPal支付标准][4] 是接受在线支付的最简单方式。 只需在商店中添加结帐按钮，即可为客户提供信用卡和PayPal付款的便利。

>[!NOTE]
>
>对于美国以外的商家而言，这被称为 _PayPal网站支付标准_.

借助PayPal Payments Standard，您可以在移动设备上刷卡。 这里没有月费，你可以通过eBay支付。 支持的信用卡包括Visa、MasterCard、Discover和American Express。 此外，客户可以直接从其个人PayPal帐户付款。 PayPal支付标准可在PayPal全球参考列表上的所有国家/地区使用。

>[!IMPORTANT]
>
>**PSD2要求：** <br/>
>从2019年9月14日起，欧洲银行可能会拒绝未满足要求的支付 [PSD2](../getting-started/compliance-payment-services-directive.md) 要求。 PayPal Payments Standard无需采取任何操作即可符合PSD2，因为所有要求都由PayPal处理。

## 商家要求

- [PayPal企业帐户][1]

## 签出工作流

对于客户，如果其个人PayPal帐户上的信用卡信息是最新的，则PayPal Payments Standard仅需一步即可完成。

1. **客户下单**  — 客户单击/点按 _立即付款_ 按钮完成购买。

1. **PayPal处理事务**  — 客户将被重定向到PayPal网站以完成交易。

## 设置PayPal Payments Standard

>[!NOTE]
>
>PayPal Payments Standard不能与任何其他PayPal方法（包括快速结账）同时使用。 如果您更改支付解决方案，则以前使用的支付解决方案将被禁用。

>[!TIP]
>
>单击 **[!UICONTROL Save Config]** 以保存进度。

### 步骤1：开始配置

此设置方法假定您拥有现有的PayPal帐户。

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中，展开 **[!UICONTROL Sales]** 并选择 **[!UICONTROL Payment Methods]**.

1. 如果您的Commerce安装有多个网站、商店或视图，请设置 **[!UICONTROL Store View]** 到要应用此配置的商店视图。

1. 在 _[!UICONTROL Merchant Location]_部分，选择&#x200B;**[!UICONTROL Merchant Country]**公司所在的位置。

   此设置确定配置中显示的PayPal解决方案的选择。

   ![商家所在国家/地区](../configuration-reference/sales/assets/payment-methods-merchant-location.png){width="600" zoomable="yes"}

1. 展开 **[!UICONTROL PayPal All-in-One Payment Solutions]** 并单击 **[!UICONTROL Configure]** 对象 **[!UICONTROL Payments Standard]**.

   ![PayPal支付标准](./assets/paypal-payments-standard.png){width="700" zoomable="yes"}

### 步骤2：启用并连接您的PayPal帐户

![PayPal支付标准配置](./assets/paypal-payments-display.png){width="600" zoomable="yes"}

1. 连接帐户以进行测试或生产：

   - 对于测试（开发）模式，单击 **[!UICONTROL Sandbox Credentials]** 并输入您的 [PayPal沙盒][3] 凭据。
   - 对于生产模式，单击 **[!UICONTROL Connect with PayPal]** 并输入您的生产帐户凭据。

   验证连接后，您可以继续。

1. 设置 **[!UICONTROL Enable this Solution]** 到 `Yes`.

1. 如果您想提供 [PayPal点数](paypal.md#paypal-credit-and-pay-later) 对于客户，设置 **[!UICONTROL Enable PayPal Credit]** 到 `Yes`.

### 步骤3：完成支付标准设置

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Payments Standard]** 部分。

   ![必需的设置](../configuration-reference/sales/assets/payment-methods-paypal-payments-standard-required.png){width="600" zoomable="yes"}

1. 输入 **[!UICONTROL Email Associated with your PayPal Merchant Account]**.

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

   在沙盒中测试配置时，仅使用 [信用卡号码][2] 由PayPal推荐。 当您准备好进入生产环境时，请返回到配置并将沙盒模式设置为 `No` 并连接到您的生产PayPal帐户。

1. 如果您的系统使用代理服务器在Adobe Commerce或Magento Open Source与PayPal支付系统之间建立连接，请设置 **[!UICONTROL API Uses Proxy]** 到 `Yes` 并完成以下操作：

   - **[!UICONTROL Proxy Host]**
   - **[!UICONTROL Proxy Port]**

### 步骤4：设置广告PayPal Credit/广告PayPal PayLater（可选）

从2.4.3版本开始，在包括PayPal的部署中支持PayPal PayLater。 此功能允许购物者以每两周一次分期付款的方式支付订单，而不是在购买时支付全额。 弃用PayPal信用体验。

设置 **[!UICONTROL Enable PayPal PayLater Experience]** 更改为以下任一项：

- `Yes`  — 设置广告PayPal PayLater
- `No`  — 设置广告PayPal信用

#### 广告PayPal点数

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Advertise PayPal Credit]** 部分。

   ![广告PayPal点数主页设置](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit-home-page.png){width="600" zoomable="yes"}

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

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 其余部分并重复上述步骤：

   - **[!UICONTROL Catalog Category Page]**
   - **[!UICONTROL Catalog Product Page]**
   - **[!UICONTROL Checkout Cart Page]**

#### 广告PayPal PayLater

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Advertise PayPal PayLater]** 部分。

1. 设置 **[!UICONTROL Enable PayPal PayLater]** 到 `Yes`.

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Home Page]** 部分。

   ![广告PayPal点数主页设置](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-paylater-home-page.png){width="600" zoomable="yes"}

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

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 其余部分并重复上述步骤：

   - **[!UICONTROL Catalog Product Page]**
   - **[!UICONTROL Checkout Cart Page]**
   - **结帐付款步骤**
   - **[!UICONTROL Catalog Category Page]**

### 步骤5：完成基本设置

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Basic Settings - PayPal Website Payments Standard]** 部分。

   ![基本设置](./assets/paypal-payments-basic.png){width="600" zoomable="yes"}

1. 对象 **[!UICONTROL Title]**，输入在结账时标识此付款方式的标题。

   建议您使用标题 _PayPal_ 所有商店视图。

1. 如果您提供多种支付方式，请输入一个数字 **[!UICONTROL Sort Order]** 确定与其他支付方式一起列出时PayPal Payments Standard的显示顺序。

   此数字相对于其他支付方式。 (`0` =第一个， `1` =秒， `2` =第三，依此类推。)

1. 设置 **[!UICONTROL Payment Action]** 更改为以下任一项：

   - `Authorization`  — 批准购买并暂停资金。 该金额在商户缴获前不会提取。
   - `Sale`  — 采购金额已获授权并立即从客户账户中提取。

1. 要显示 _[!UICONTROL Check out with PayPal]_产品页面上的按钮，设置&#x200B;**[!UICONTROL Display on Product Details Page]**到 `Yes`.

### 步骤6：完成高级设置

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Advanced Settings]** 部分。

   ![高级设置](../configuration-reference/sales/assets/payment-methods-paypal-payment-standard-advanced.png){width="600" zoomable="yes"}

1. 要使PayPal Payments Standard可从购物车和迷你购物车中使用，请设置 **[!UICONTROL Display on Shopping Cart]** 到 `Yes`.

1. 设置 **[!UICONTROL Payment from Applicable Countries]** 更改为以下任一项：

   - `All Allowed Countries`  — 来自所有客户的客户 [国家/地区](../getting-started/store-details.md#country-options) 在商店配置中指定的可使用此付款方式。
   - `Specific Countries`  — 选择此选项后， _[!UICONTROL Payment from Specific Countries]_列表出现。 要选择多个国家/地区，请按住Ctrl键(PC)或Command键(Mac)并单击每个选项。

1. 要在日志文件中记录与支付系统的通信，请设置 **[!UICONTROL Debug Mode]** 到 `Yes`.

   >[!NOTE]
   >
   >日志文件存储在服务器上，只有开发人员才能访问。 根据PCI数据安全标准，信用卡信息不会记录在日志文件中。

1. 要启用SSL验证，请设置 **[!UICONTROL Enable SSL Verification]** 到 `Yes`.

1. 要在PayPal支付页面上的订单中显示每个行项目的汇总，请设置 **[!UICONTROL Transfer Cart Line Items]** 到 `Yes`.

   要在摘要中包含最多十个配送选项，请设置 **[!UICONTROL Transfer Shipping Options]** 到 `Yes`. （仅当将行项目设置为转移时，才会显示此选项。）

1. 要确定用于PayPal接受按钮的图像类型，请设置 **[!UICONTROL Shortcut Buttons Flavor]** 更改为以下任一项：

   - `Dynamic`  — （推荐）显示可从PayPal服务器动态更改的图像。
   - `Static`  — 显示无法动态更改的特定图像。

1. 要允许没有PayPal帐户的客户使用此方法购买，请设置 **[!UICONTROL Enable PayPal Guest Checkout]** 到 `Yes`.

1. 设置 **[!UICONTROL Require Customer's Billing Address]** 更改为以下任一项：

   - `Yes`  — 所有购买都需要客户帐单地址。
   - `No`  — 任何购买均不需要客户账单地址。
   - `For Virtual Quotes Only`  — 仅需要虚拟报价的客户帐单地址。

1. 要允许客户进入 [PayPal计费协议](paypal-billing-agreements.md) 客户帐户中无可用的有效帐单协议时，使用您的商店，设置 **[!UICONTROL Billing Agreement Signup]** 更改为以下任一项：

   - `Auto`  — 客户可以在快速结帐流程中订立帐单协议，或者使用其他付款方式。
   - `Ask Customer`  — 客户可以决定是否在“快速结帐”工作流中签署帐单协议。
   - `Never`  — 客户在快速结帐工作流中无法签署帐单协议。

   >[!NOTE]
   >
   >商家必须请求PayPal商家技术支持以在其帐户中启用帐单协议。 此 _帐单协议注册_ 只有在PayPal确认您的商户帐户已启用开单协议后，才能启用参数。

1. 要允许客户从PayPal网站完成交易，而无需返回到您的商店进行订单审核，请设置 **[!UICONTROL Skip Order Review Step]** 到 `Yes`.

### 步骤7：完成并保存配置设置

1. 根据存储需要，完成以下部分：

   - [PayPal计费协议设置](#paypal-billing-agreement-settings)
   - [结算报表设置](#settlement-report-settings)
   - [前端体验设置](#frontend-experience-settings)

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

   - 要在使用Express Checkout在您的网站上正式启用之前运行测试报告，请设置 **[!UICONTROL Sandbox Mode]** 到 `Yes`.

   - 输入 **[!UICONTROL Custom Endpoint Hostname or IP Address]**.

     默认情况下，该值为 `reports.paypal.com`.

   - 输入 **[!UICONTROL Custom Path]** 保存报告的位置。

     默认情况下，该值为 `/ppreports/outgoing`.

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

使用 _[!UICONTROL Frontend Experience Settings]_选择要在您的网站上显示的PayPal徽标，以及自定义您的PayPal商家页面的外观。

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

[1]: https://www.paypal.com/webapps/mpp/how-to-sell-online
[2]: https://www.paypalobjects.com/en_AU/vhelp/paypalmanager_help/credit_card_numbers.htm
[3]: https://developer.paypal.com/docs/api-basics/sandbox/
[4]: https://developer.paypal.com/docs/paypal-payments-standard/mobile-paypal-payments-standard/

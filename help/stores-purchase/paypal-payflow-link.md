---
title: PayPal Payflow链接
description: 了解如何在您的商店中将PayPal Payflow Link设置为在线支付解决方案。
exl-id: dba4057e-1fea-4a23-8594-cc85f619d664
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '2172'
ht-degree: 0%

---

# PayPal Payflow链接

PayPal Payflow Link仅适用于美国和加拿大的商家。 客户无需拥有个人PayPal帐户，即可在PayPal托管的表单中输入其信用卡信息。 此信息绝不会存储在Adobe Commerce或Magento Open Source服务器上。 “工资流链接”不能用于从管理员创建的订单。

在线和离线退款均支持贷项通知单。 但是，不支持多个在线退款。

>[!IMPORTANT]
>
>**PSD2要求：** <br/>
>从2019年9月14日起，欧洲银行可能会拒绝未满足要求的支付 [PSD2](../getting-started/compliance-payment-services-directive.md) 要求。 为了符合PSD2，PayPal Payflow Link必须与Cardinal Commerce集成。 要了解更多信息，请参阅 [3D Secure for Payflow](https://developer.paypal.com/api/nvp-soap/payflow/3d-secure-overview/).

## 要求

- [PayPal企业帐户][1] PayPal Payflow Pro网关将PayPal中的商户帐户与商户网站链接，同时充当网关和商户帐户。

- 如果您管理多个Commerce网站，则必须为每个网站拥有单独的PayPal商家帐户。

## 客户工作流程

1. **客户前往结帐**  — 在结账过程中，客户选择使用PayPal Payflow链接付款并输入信用卡信息。 客户无需拥有个人PayPal帐户。
1. **客户选择“立即付款”**  — 客户点击“立即付款”按钮提交订单。
1. **客户输入信用卡信息**  — 客户在PayPal托管的表单上输入信用卡信息。 如果客户单击 _取消付款_ 链接，则客户会返回到结账的“支付信息”阶段，并且订单状态将更改为 _已取消_.
1. **客户提交订单**  — 信用卡信息直接提交给PayPal，不会保留在Commerce网站的任何位置。

## 订单工作流

1. **PayPal接收请求** - PayPal收到客户的“立即付款”请求。
1. **PayPal验证付款信息** - PayPal验证信用卡信息，并分配适当的状态：
   - **付款已验证：** 如果验证， _待处理付款_ 状态最初分配给订单，直到结算交易记录。
   - **正在处理**  — 交易成功。
   - **待处理付款**  — 系统未收到PayPal的响应。
   - **已取消**  — 由于某种原因，该事务未成功。
   - **可疑欺诈**  — 交易并未通过某些 [PayPal欺诈过滤器](paypal.md#paypal-fraud-management-filters). 系统接收来自PayPal的响应，指出欺诈服务正在审查交易。
   - **取消付款：** 如果客户单击 _取消付款_ 链接，则客户会返回到结账的“支付信息”阶段，并且订单状态将更改为 _已取消_.
1. **客户被重定向到确认页面**   — 如果交易成功完成，客户将被重定向到您商店中的订单确认页面。 如果由于任何原因事务处理失败，则结账页面上会显示一条错误消息，并指示客户重复结账过程。 这些情况由PayPal管理。
1. **商家履行订单**  — 商户如常开具发票并发送订单。

## 配置PayPal帐户

1. 登录 [PayPal商业帐户][2].

1. 配置 [托管的签出页面][4] 使用以下设置使用PayPal管理器：

   - 下 **[!UICONTROL Security Options]**，请完成以下设置：

     **[!UICONTROL AVS]**: `No`

     **[!UICONTROL CSC]**: `No`

     **[!UICONTROL Enable Secure Token]**: `Yes`

   - 选择 **[!UICONTROL Customize]**，然后选择 **[!UICONTROL Layout C]**.

     布局C仅显示信用卡和借记卡字段，并且可以在您的网站上设置框架或用作独立的弹出窗口。 大小固定在490 x 565像素，为错误消息留出额外空间。 在某些系统上，此设置更正了透明重定向的问题。

1. 配置设置完成后，单击 **[!UICONTROL Save and Publish]**.

1. 设置一个额外的用户（由PayPal推荐）：

   - 在主菜单的第二行中，单击 **[!UICONTROL Manage Users]**.

   - 若要向帐户中添加其他用户，请单击 **[!UICONTROL Add User]**.

   - 填写以下部分中的必填字段 _添加用户_ 表单：

      - [!UICONTROL Admin Confirmation]
      - [!UICONTROL User Information]
      - [!UICONTROL User Login Information]
      - [!UICONTROL Assign Privilege to User]

   - 单击 **[!UICONTROL Update]**.

## 设置PayPal Payflow链接

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

1. 展开 **[!UICONTROL PayPal Payment Gateways]** （如果需要），然后单击 **[!UICONTROL Configure]** 对象 **[!UICONTROL Payflow Link]**.

   ![Payflow链接 — 配置](./assets/payflow-link.png){width="600" zoomable="yes"}

### 步骤2：完成所需的PayPal设置

![必需的PayPal设置 — PayPal Payflow链接](./assets/payflow-required-link.png){width="600" zoomable="yes"}

1. （可选）输入 **[!UICONTROL Email Associated with your PayPal Merchant Account]**.

   >[!IMPORTANT]
   >
   >电子邮件地址区分大小写。 要接收付款，电子邮件地址必须与在您的PayPal商家帐户中指定的电子邮件地址匹配。

1. 输入以下凭据之一，用于登录到PayPal商家帐户：

   - **[!UICONTROL Partner]**  — 您的PayPal合作伙伴ID。
   - **[!UICONTROL User]**  — 在您的PayPal帐户中设置的另一个用户的ID。
   - **[!UICONTROL Vendor]**  — 您的PayPal用户登录名。

1. 输入 **[!UICONTROL Password]** 与您的PayPal帐户关联的帐户。

1. 要运行测试事务，请设置 **[!UICONTROL Test Mode]** 到 `Yes`.

   在沙盒中测试配置时，仅使用 [信用卡号码][3] 由PayPal推荐。 当您准备好进入生产环境时，请返回到配置并将测试模式设置为 `No`.

1. 如果您的系统使用代理服务器建立与PayPal系统的连接，请设置 **[!UICONTROL Test Mode]** 到 `Yes` 并执行以下操作：

   - 输入IP地址 **[!UICONTROL Proxy Host]**.

   - 输入 **[!UICONTROL Proxy Port]**.

     当服务器防火墙阻止直接访问PayPal服务器时，将使用代理。 在这种情况下，使用第三方服务器来中继流量。

1. 设置 **[!UICONTROL Enable Payflow Link]** 到 `Yes`.

1. 如果要启用 [PayPal Express签出](paypal-express-checkout.md) 客户选项，设置 **[!UICONTROL Enable Express Checkout]** 到 `Yes`.

1. 如果您想提供 [PayPal点数](paypal.md#paypal-credit-and-pay-later) 对于客户，设置 **[!UICONTROL Enable PayPal Credit]** 到 `Yes`.

### 步骤3：设置广告PayPal Credit/广告PayPal PayLater（可选）

从2.4.3版本开始，在包括PayPal的部署中支持PayPal PayLater。 此功能允许购物者以每两周一次分期付款的方式支付订单，而不是在购买时支付全额。 弃用PayPal信用体验。

设置 **[!UICONTROL Enable PayPal PayLater Experience]** 更改为以下任一项：

- `Yes`  — 设置广告PayPal PayLater
- `No`  — 设置广告PayPal信用

#### 广告PayPal点数

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Advertise PayPal Credit]** 部分。

   ![广告PayPal点数](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit.png){width="600" zoomable="yes"}

1. 要获取您的帐户信息，请单击 **[!UICONTROL Get Publisher ID from PayPal]** 然后按照说明操作。

1. 输入您的 **[!UICONTROL Publisher ID]**.

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Home Page]** 部分。

   ![广告PayPal点数主页设置](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit-home-page.png){width="600" zoomable="yes"}

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

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 其余部分，并为主页配置重复上述步骤：

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
   - **[!UICONTROL Checkout Payment Step]**
   - **[!UICONTROL Catalog Category Page]**

### 步骤4：完成基本设置

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Basic Settings - PayPal Payflow Link]** 部分。

   ![基本设置 — PayPal Payflow链接](../configuration-reference/sales/assets/payment-methods-paypal-payflow-link-basic-settings.png){width="600" zoomable="yes"}

1. 对象 **[!UICONTROL Title]**，输入在结账期间标识PayPal Payflow Link的标题。

   建议您使用标题 _借记卡或信用卡_.

1. 如果您提供多种支付方式，请输入一个数字 **[!UICONTROL Sort Order]** 确定与其它付款方法一起列出时“工资流链接”的显示顺序。

   此数字相对于其他支付方式。 (`0` =第一个， `1` =秒， `2` =第三，依此类推。)

1. 设置 **[!UICONTROL Payment Action]** 更改为以下任一项：

   - `Authorization`  — 批准购买并暂停资金。 该金额在商户缴获前不会提取。
   - `Sale`  — 采购金额已获授权并立即从客户账户中提取。

### 步骤5：完成高级设置

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Advanced Settings]** 部分。

   ![高级设置 — PayPal Payflow链接](../configuration-reference/sales/assets/payment-methods-paypal-payflow-link-advanced-settings.png){width="600" zoomable="yes"}

1. 设置 **[!UICONTROL Payment Applicable From]** 更改为以下任一项：

   - `All Allowed Countries`  — 来自所有客户的客户 [国家/地区](../getting-started/store-details.md#country-options) 在商店配置中指定的可使用此付款方式。
   - `Specific Countries`  — 选择此选项后， _[!UICONTROL Payment from Specific Countries]_列表出现。 按住Ctrl键并选择列表中客户可在您的商店购买产品的每个国家/地区。

1. 要将与支付系统的通信写入日志文件，请设置 **[!UICONTROL Debug Mode]** 到 `Yes`.

   >[!NOTE]
   >
   >根据PCI数据安全标准，信用卡信息不会记录在日志文件中。

1. 要启用主机真实性验证，请设置 **[!UICONTROL Enable SSL Verification]** 到 `Yes`.

1. 如果您希望客户能够更正信用卡背面输入的3位数CVV安全代码，请设置 **[!UICONTROL CVV Entry is Editable]** 到 `Yes`.

1. 要要求客户输入CVV代码，请设置 **[!UICONTROL Require CVV Entry]** 到 `Yes`.

1. 要向客户发送付款确认，请设置 **[!UICONTROL Send Email Confirmation]** 到 `Yes`.

1. 要确定在交易期间与PayPal服务器交换信息所用的方法，请设置 **[!UICONTROL URL method for Cancel URL and Return URL]** 更改为以下任一项：

   - `GET`  — 检索进程结果的信息（默认方法）。
   - `POST`  — 向数据处理流程提供数据块，例如输入到表单中的数据。

   此 _取消Url_ 和 _返回URL_ 请参阅客户在PayPal服务器上完成或取消结帐流程中的付款部分后返回的页面

1. 根据存储需要，完成以下部分：

   - [结算报表设置](#settlement-report-settings)
   - [前端体验设置](#frontend-experience-settings)

#### 结算报表设置

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Settlement Report Settings]** 部分。

   ![结算报表设置 — PayPal Payflow Pro](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-settlement-report-settings.png){width="600" zoomable="yes"}

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

   ![前端体验设置 — PayPal Payflow Pro](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-frontend-experience-settings1.png){width="600" zoomable="yes"}

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

### 步骤6：完成PayPal Express结帐的基本设置

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Basic Settings - PayPal Express Checkout]** 部分。

   ![基本设置](../configuration-reference/sales/assets/payment-methods-paypal-payflow-link-express-checkout-basic-settings.png){width="600" zoomable="yes"}

1. 对象 **[!UICONTROL Title]**，输入在结账时标识此付款方式的标题。

   将标题设置为 _PayPal_ 建议每个商店视图使用。

1. 如果您提供多种支付方式，请输入一个数字 **[!UICONTROL Sort Order]** 确定与其他支付方式一起列出时PayPal Express Checkout出现的顺序。

   此数字相对于其他支付方式。 (`0` =第一个， `1` =秒， `2` =第三，依此类推。)

1. 设置 **[!UICONTROL Payment Action]** 更改为以下任一项：

   - `Authorization`  — 批准购买并暂停资金。 该款项于到期前不会提取。 _已捕获_ 是商贩送的。
   - `Sale`  — 采购金额已获授权并立即从客户账户中提取。

1. 要显示 _[!UICONTROL Check out with PayPal]_产品页面上的按钮，设置&#x200B;**[!UICONTROL Display on Product Details Page]**到 `Yes`.

### 步骤7：完成PayPal Express签出的高级设置

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Advanced Settings]** 部分。

   ![高级设置](../configuration-reference/sales/assets/payment-methods-paypal-payflow-link-express-checkout-advanced-settings.png){width="600" zoomable="yes"}

1. 设置 **[!UICONTROL Display on Shopping Cart]** 到 `Yes`.

1. 设置 **[!UICONTROL Payment Applicable From]** 更改为以下任一项：

   - `All Allowed Countries`  — 来自您商店配置中指定的所有国家/地区的客户均可以使用此付款方法。
   - `Specific Countries`  — 选择此选项后， _[!UICONTROL Payment from Specific Countries]_列表出现。 要选择多个国家/地区，请按住Ctrl键(PC)或Command键(Mac)并单击每个项目。

1. 要将与支付系统的通信写入日志文件，请设置 **[!UICONTROL Debug Mode]** 到 `Yes`.

   >[!NOTE]
   >
   >根据PCI数据安全标准，信用卡信息不会记录在日志文件中。

1. 要启用主机真实性验证，请设置 **[!UICONTROL Enable SSL Verification]** 到 `Yes`.

1. 要显示PayPal站点中按行项目列出的客户订单的完整汇总，请设置 **[!UICONTROL Transfer Cart Line Items]** 到 `Yes`.

1. 要允许客户从PayPal网站完成交易，而无需返回到您的商店进行订单审核，请设置 **[!UICONTROL Skip Order Review Step]** 到 `Yes`.

1. 完成后，单击 **[!UICONTROL Save Config]**.

[1]: https://www.paypal.com/webapps/mpp/how-to-sell-online
[2]: https://manager.paypal.com/
[3]: https://www.paypalobjects.com/en_AU/vhelp/paypalmanager_help/credit_card_numbers.htm
[4]: https://developer.paypal.com/docs/payflow/integration-guide/configure-hosted-checkout/#configuring-hosted-pages-using-paypal-manager

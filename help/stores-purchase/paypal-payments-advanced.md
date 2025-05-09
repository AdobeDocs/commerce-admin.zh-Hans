---
title: PayPal支付高级
description: 了解如何在您的商店中将PayPal Payments Advanced设置为在线支付解决方案。
exl-id: 018dd999-2f17-4650-8f61-624809ae76c6
feature: Payments
badgePaas: label="仅限PaaS" type="Informative" url="https://experienceleague.adobe.com/zh-hans/docs/commerce/user-guides/product-solutions" tooltip="仅适用于云项目(Adobe管理的PaaS基础架构)和内部部署项目上的Adobe Commerce 。"
source-git-commit: cd5b5ebec6e72ab4ba9de775bcfe8f8a89fbbb93
workflow-type: tm+mt
source-wordcount: '2161'
ht-degree: 0%

---

# PayPal支付高级

[PayPal Payments Advanced][4]是符合[PCI标准的](../getting-started/compliance-pci.md)解决方案，允许客户在不离开网站的情况下通过借记卡或信用卡付款。 它包括一个嵌入式签出页面，可以自定义该页面以创建无缝且安全的签出体验。

即使客户没有PayPal帐户，也可以通过PayPal安全支付网关进行购买。 接受信用卡包括美国和英国的Visa、MasterCard、Switch/Maestro和Solo信用卡。 为了方便起见，PayPal Express结帐包含在PayPal Payments Advanced中。

>[!IMPORTANT]
>
>**PSD2要求：** <br/>
>从2019年9月14日起，欧洲银行可能会拒绝不符合[PSD2](../getting-started/compliance-payment-services-directive.md)要求的支付。 为了符合PSD2的要求，PayPal Payments Advanced必须集成到第三方插件中。 若要了解详细信息，请参阅[Payflow的3-D安全](https://developer.paypal.com/api/nvp-soap/payflow/3d-secure-mpi/)。

>[!NOTE]
>
>PayPal Payments Advanced不能用于从商店管理员创建的订单。

## 要求

- [PayPal企业帐户][1]
- 如果您管理多个Adobe Commerce和Magento Open Source网站，则必须为每个网站拥有单独的PayPal商家帐户。

## 签出工作流

1. **客户选择付款方式** — 在结帐时，客户选择使用PayPal付款进行预付款。 此时将显示“立即付款”按钮，而不是“下订单”按钮。

1. **立即支付** — 客户点击/点按&#x200B;_立即支付_，此时会显示PayPal托管的表单。 客户输入卡信息，并对卡进行验证。 如果成功，则会显示订单确认页面。

   **使用PayPal付款** — 该表单还包括&#x200B;_使用PayPal付款_&#x200B;按钮，该按钮可将客户重定向到PayPal网站，以便使用PayPal Express结帐付款。

1. **故障排除** — 如果事务因任何原因失败，则结帐页面上会显示错误消息，并指示客户重试。 任何问题均由PayPal管理。

## 订单处理工作流

使用PayPal Payments Advanced处理订单的方式与任何常规PayPal订单相同。 系统会为订单开票和发运，并为在线和离线退款生成贷项通知单。 但是，使用PayPal Payments Advanced支付的订单不能获得多个在线退款。

1. **客户下订单** — 在结账的最后阶段，客户点击“下订单”按钮。

1. **PayPal响应** - PayPal评估该请求。 如果发现有效，则PayPal处理该交易。

1. **Commerce设置订单状态** - Commerce从PayPal接收响应，并将订单状态设置为以下任一项：

   - **正在处理** — 事务成功。
   - **待处理付款** — 系统未收到来自PayPal的任何响应。
   - **已取消** — 由于某些原因，该事务未成功
   - **可疑欺诈** — 交易未通过某些[PayPal欺诈过滤器](paypal.md#paypal-fraud-management-filters)。 系统接收来自PayPal的响应，指出欺诈服务正在审查交易。

1. **商家履行订单** — 商家发票并发送订单。

## 配置PayPal帐户

在Commerce中设置PayPal Payments Advanced之前，必须在PayPal网站上配置您的帐户。

1. 登录到您的[PayPal企业帐户][2]。

1. 转到&#x200B;**[!UICONTROL Service Settings]** > **[!UICONTROL Hosted Checkout Pages]** > **[!UICONTROL Set Up Menu]**&#x200B;并完成以下设置：

   - **[!UICONTROL AVS]**： `No`
   - **[!UICONTROL CSC]**： `No`
   - **[!UICONTROL Enable Secure Token]**： `Yes`

1. **[!UICONTROL Save]**&#x200B;设置。

   >[!NOTE]
   >
   >如果您有多个Commerce网站，则必须为每个网站创建单独的PayPal支付高级帐户。

1. 当系统提示您创建布局时，请执行以下操作：

   - 在页面顶部，单击&#x200B;**[!UICONTROL Customize]**。

   - 选择&#x200B;**[!UICONTROL Layout C]**。

   - 单击&#x200B;**[!UICONTROL Save and Publish]**。

1. 设置另一个用户（由PayPal推荐）：

   - 登录到您的[PayPal企业帐户][2]。

   - 要设置另一个用户，请按照说明操作。

   - **[!UICONTROL Save]**&#x200B;更改。

## 设置Commerce中的PayPal高级支付

>[!NOTE]
>
>您可以同时启用两个PayPal解决方案：快速结帐，以及任何一体化或支付网关解决方案。 如果您更改支付解决方案，则以前使用的支付解决方案将被禁用。

>[!TIP]
>
>随时单击&#x200B;**[!UICONTROL Save Config]**&#x200B;以保存进度。

### 步骤1：开始配置

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧面板中，展开&#x200B;**[!UICONTROL Sales]**&#x200B;并选择&#x200B;**[!UICONTROL Payment Methods]**。

1. 如果您的Commerce安装有多个网站、商店或视图，请将&#x200B;**[!UICONTROL Store View]**&#x200B;设置为要应用此配置的商店视图。

1. 在&#x200B;_[!UICONTROL Merchant Location]_&#x200B;部分中，选择您的公司所在的&#x200B;**[!UICONTROL Merchant Country]**。

   此设置确定配置中显示的PayPal解决方案的选择。

   ![商家国家/地区](../configuration-reference/sales/assets/payment-methods-merchant-location.png){width="600" zoomable="yes"}

1. 展开&#x200B;**[!UICONTROL PayPal All-in-One Payment Solution]**&#x200B;并单击&#x200B;**[!UICONTROL Payments Advanced]**&#x200B;的&#x200B;**[!UICONTROL Configure]**。

   ![PayPal预付款项](./assets/paypal-payments-advanced.png){width="600" zoomable="yes"}

### 第2步：完成所需的设置

1. 如果需要，展开![扩展选择器](../assets/icon-display-expand.png) **[!UICONTROL Required PayPal Settings]**&#x200B;部分。

   ![高级必需设置 — PayPal付款高级](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-required.png){width="600" zoomable="yes"}

1. （可选）输入&#x200B;**[!UICONTROL Email Associated with your PayPal Merchant Account]**。

   >[!IMPORTANT]
   >
   >电子邮件地址区分大小写。 要接收付款，电子邮件地址必须与在您的PayPal商家帐户中指定的电子邮件地址匹配。

   如果您没有PayPal帐户，请单击&#x200B;**[!UICONTROL Start accepting payments via PayPal]**。

1. 输入以下凭据之一，用于登录到PayPal商家帐户：

   - **[!UICONTROL Partner]** — 您的PayPal合作伙伴ID。
   - **[!UICONTROL Vendor]** — 您的PayPal用户登录名。
   - **[!UICONTROL User]** — 在您的PayPal帐户中设置的另一个用户的ID。

1. 输入与您的PayPal帐户关联的&#x200B;**[!UICONTROL Password]**。

1. 要运行测试事务，请将&#x200B;**[!UICONTROL Test Mode]**&#x200B;设置为`Yes`。

   在沙盒中测试配置时，仅使用PayPal推荐的[信用卡号][3]。 当您准备好进入生产环境时，请返回到配置并将测试模式设置为`No`。

1. 如果您的系统使用代理服务器建立与PayPal系统的连接，请将&#x200B;**[!UICONTROL Use Proxy]**&#x200B;设置为`Yes`并执行以下操作：

   - 输入&#x200B;**[!UICONTROL Proxy Host]**&#x200B;的IP地址。

   - 输入&#x200B;**[!UICONTROL Proxy Port]**&#x200B;的端口号。

     当服务器防火墙阻止直接访问PayPal服务器时，将使用代理。 在这种情况下，使用第三方服务器来中继流量。

1. 将&#x200B;**[!UICONTROL Enable this Solution]**&#x200B;设置为`Yes`。

1. 如果要为客户提供点数[PayPal](paypal.md#paypal-credit-and-pay-later)，请将&#x200B;**[!UICONTROL Enable PayPal Credit]**&#x200B;设置为`Yes`。

### 步骤3：设置广告PayPal Credit/广告PayPal PayLater（可选）

从2.4.3版本开始，在包括PayPal的部署中支持PayPal PayLater。 此功能允许购物者以每两周一次分期付款的方式支付订单，而不是在购买时支付全额。 弃用PayPal信用体验。

将&#x200B;**[!UICONTROL Enable PayPal PayLater Experience]**&#x200B;设置为以下项之一：

- `Yes` — 设置广告PayPal PayLater
- `No` — 设置广告PayPal点数

#### 广告PayPal点数

1. 展开&#x200B;**[!UICONTROL Advertise PayPal Credit]**&#x200B;部分的![扩展选择器](../assets/icon-display-expand.png)。

   ![广告PayPal点数](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit.png){width="600" zoomable="yes"}

1. 若要获取帐户信息，请单击&#x200B;**[!UICONTROL Get Publisher ID from PayPal]**&#x200B;并按照说明操作。

1. 输入您的&#x200B;**[!UICONTROL Publisher ID]**。

1. 展开&#x200B;**[!UICONTROL Home Page]**&#x200B;部分的![扩展选择器](../assets/icon-display-expand.png)。

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

   - **[!UICONTROL Catalog Category Page]**
   - **[!UICONTROL Catalog Product Page]**
   - **[!UICONTROL Checkout Cart Page]**

#### 广告PayPal PayLater

1. 展开&#x200B;**[!UICONTROL Advertise PayPal PayLater]**&#x200B;部分的![扩展选择器](../assets/icon-display-expand.png)。

1. 将&#x200B;**[!UICONTROL Enable PayPal PayLater]**&#x200B;设置为`Yes`。

1. 展开&#x200B;**[!UICONTROL Home Page]**&#x200B;部分的![扩展选择器](../assets/icon-display-expand.png)。

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

   - **[!UICONTROL Catalog Product Page]**
   - **[!UICONTROL Checkout Cart Page]**
   - **[!UICONTROL Checkout Payment Step]**
   - **[!UICONTROL Catalog Category Page]**

### 步骤4：完成基本设置

1. 如果需要，展开![扩展选择器](../assets/icon-display-expand.png) **[!UICONTROL Basic Settings - PayPal Payments Advanced]**&#x200B;部分。

   ![PayPal付款高级基本设置](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-basic-settings.png){width="600" zoomable="yes"}

1. 若要在结帐时识别PayPal Payments Advanced，请输入&#x200B;**[!UICONTROL Title]**。

   建议您使用标题&#x200B;_借记卡或信用卡_。

1. 如果您提供多种付款方式，请输入&#x200B;**[!UICONTROL Sort Order]**&#x200B;的数字，以确定在结帐期间与其他付款方式一起列出时，PayPal付款高级的显示顺序。

   此数字相对于其他支付方式。 （`0` =第一，`1` =第二，`2` =第三，依此类推。）

1. 将&#x200B;**[!UICONTROL Payment Action]**&#x200B;设置为以下项之一：

   - `Authorization` — 批准购买，但保留资金。 在商户捕获&#x200B;_金额_&#x200B;之前，不撤消该金额。
   - `Sale` — 已授权并立即从客户帐户中收回购买金额。

### 步骤5：完成高级设置

1. 展开&#x200B;**[!UICONTROL Advanced Settings]**&#x200B;部分的![扩展选择器](../assets/icon-display-expand.png)。

   ![高级设置 — 高级PayPal支付](./assets/paypal-payments-advanced2.png){width="600" zoomable="yes"}

1. 将&#x200B;**[!UICONTROL Payment Applicable From]**&#x200B;设置为以下项之一：

   - `All Allowed Countries` — 来自您商店配置中指定的所有[国家/地区](../getting-started/store-details.md#country-options)的客户都可以使用此付款方式。
   - `Specific Countries` — 选择此选项后，将显示&#x200B;_[!UICONTROL Payment from Specific Countries]_&#x200B;列表。 按住Ctrl键(PC)或Command键(Mac)，然后选择客户可在您的商店中购买产品的每个国家/地区。

1. 要将与付款系统的通信写入日志文件，请将&#x200B;**[!UICONTROL Debug Mode]**&#x200B;设置为`Yes`。

   PayPal Payments Advanced的日志文件是`payments_payflow_advanced.log`。

   >[!NOTE]
   >
   >根据PCI数据安全标准，信用卡信息不会记录在日志文件中。

1. 要启用主机真实性验证，请将&#x200B;**[!UICONTROL Enable SSL Verification]**&#x200B;设置为`Yes`。

1. 若要允许客户更正信用卡背面输入的3位数CVV安全代码，请将&#x200B;**[!UICONTROL CVV Entry is Editable]**&#x200B;设置为`Yes`。

1. 若要要求客户输入CVV代码，请将&#x200B;**[!UICONTROL Require CVV Entry]**&#x200B;设置为`Yes`。

1. 若要向客户发送付款确认，请将&#x200B;**[!UICONTROL Send Email Confirmation]**&#x200B;设置为`Yes`。

1. 要确定在交易期间与PayPal服务器交换信息的方法，请将&#x200B;**[!UICONTROL URL method for Cancel URL and Return URL]**&#x200B;设置为以下任一项：

   - `GET` — （默认）检索进程结果的信息。
   - `POST` — 向数据处理流程提供数据块，例如输入到表单中的数据。

   _取消URL_&#x200B;和&#x200B;_返回URL_&#x200B;是指客户在PayPal服务器上完成或取消结帐流程中的付款部分后返回的页面。

1. 根据存储需要，完成以下部分：

   - [结算报表设置](#settlement-report-settings)
   - [前端体验设置](#frontend-experience-settings)

#### 结算报表设置

1. 展开&#x200B;**[!UICONTROL Settlement Report Settings]**&#x200B;部分的![扩展选择器](../assets/icon-display-expand.png)。

   ![PayPal结算报告设置](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-settlement-report-settings.png){width="600" zoomable="yes"}

1. 对于&#x200B;**[!UICONTROL SFTP Credentials]**，执行以下操作：

   - 如果您已注册PayPal的安全FTP服务器，请输入以下SFTP登录凭据：

      - 登录
      - 密码

   - 要在上线前运行测试报告，请将&#x200B;**[!UICONTROL Sandbox Mode]**&#x200B;设置为`Yes`。

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

1. 展开&#x200B;**[!UICONTROL Frontend Experience Settings]**&#x200B;部分的![扩展选择器](../assets/icon-display-expand.png)。

   ![PayPal前端体验设置](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-frontend-experience-settings.png){width="600" zoomable="yes"}

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

### 步骤6：完成PayPal Express签出的基本设置

1. 展开&#x200B;**[!UICONTROL Basic Settings - PayPal Express Checkout]**&#x200B;部分的![扩展选择器](../assets/icon-display-expand.png)。

   ![PayPal Express签出基本设置](../configuration-reference/sales/assets/payment-methods-paypal-advanced-express-checkout-basic-settings.png){width="600" zoomable="yes"}

1. 对于&#x200B;**[!UICONTROL Title]**，输入在结帐时标识此付款方式的标题。

   建议将每个商店视图的标题设置为&#x200B;_PayPal_。

1. 如果您提供多种付款方式，请输入&#x200B;**[!UICONTROL Sort Order]**&#x200B;的数字，以确定与其他付款方式一起列出时PayPal快速结帐的出现顺序。

   此数字相对于其他支付方式。 （`0` =第一，`1` =第二，`2` =第三，依此类推。）

1. 将&#x200B;**[!UICONTROL Payment Action]**&#x200B;设置为以下项之一：

   - `Authorization` — 批准购买并暂停资金。 在商户捕获&#x200B;_金额_&#x200B;之前，不撤消该金额。
   - `Sale` — 已授权并立即从客户帐户中收回购买金额。

1. 要在产品页面上显示&#x200B;_[!UICONTROL Check out with PayPal]_&#x200B;按钮，请将&#x200B;**[!UICONTROL Display on Product Details Page]**&#x200B;设置为`Yes`。

### 步骤7：完成高级设置 — PayPal Express签出

1. 展开&#x200B;**[!UICONTROL Advanced Settings]**&#x200B;部分的![扩展选择器](../assets/icon-display-expand.png)。

   ![PayPal Express签出高级设置](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-express-checkout-advanced.png){width="600" zoomable="yes"}

1. 若要使PayPal Express从购物车和迷你购物车中均可结帐，请将&#x200B;**[!UICONTROL Display on Shopping Cart]**&#x200B;设置为`Yes`。

1. 将&#x200B;**[!UICONTROL Payment Applicable From]**&#x200B;设置为以下项之一：

   - `All Allowed Countries` — 来自您商店配置中指定的所有[国家/地区](../getting-started/store-details.md#country-options)的客户都可以使用此付款方式。
   - `Specific Countries` |选择此选项后，将显示&#x200B;_从特定国家/地区付款列表_。 按住Ctrl键(PC)或Command键(Mac)，并单击列表中客户可在您的商店购买产品的国家/地区。

1. 要将与付款系统的通信写入日志文件，请将&#x200B;**[!UICONTROL Debug Mode]**&#x200B;设置为`Yes`。

   >[!NOTE]
   >
   >根据[PCI数据安全标准](../getting-started/compliance-pci.md)，在日志文件中未记录信用卡信息。

1. 要启用主机真实性验证，请将&#x200B;**[!UICONTROL Enable SSL Verification]**&#x200B;设置为`Yes`。

1. 要显示PayPal网站中客户订单明细项目的完整摘要，请将&#x200B;**[!UICONTROL Transfer Cart Line Items]**&#x200B;设置为`Yes`。

1. 要允许客户从PayPal网站完成交易而不返回商店进行订单审核，请将&#x200B;**[!UICONTROL Skip Order Review Step]**&#x200B;设置为`Yes`。

1. 完成后，单击&#x200B;**[!UICONTROL Save Config]**。

[1]: https://www.paypal.com/webapps/mpp/how-to-sell-online
[2]: https://manager.paypal.com/
[3]: https://www.paypalobjects.com/en_AU/vhelp/paypalmanager_help/credit_card_numbers.htm
[4]: https://developer.paypal.com/docs/payflow/gs-ppa-hosted-pages/

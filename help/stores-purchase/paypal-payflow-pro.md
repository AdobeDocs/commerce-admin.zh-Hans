---
title: PayPal Payflow Pro
description: 了解如何在您的商店中将PayPal Payflow Pro设置为在线支付解决方案。
exl-id: c720b33c-44e1-4954-b5be-38932393a43c
feature: Payments
badgePaas: label="仅限PaaS" type="Informative" url="https://experienceleague.adobe.com/zh-hans/docs/commerce/user-guides/product-solutions" tooltip="仅适用于云项目(Adobe管理的PaaS基础架构)和内部部署项目上的Adobe Commerce 。"
source-git-commit: cace9d1de00955494d8bc607c017778ff7df4806
workflow-type: tm+mt
source-wordcount: '2212'
ht-degree: 0%

---

# PayPal Payflow Pro

PayPal Payflow Pro网关（以前称为&#x200B;_Verisign_）面向美国、加拿大、澳大利亚和新西兰的客户提供。 与其他PayPal支付方式不同，商户每月收取固定费用，并且每笔交易都收取固定费用，无论数量多少。

![使用PayPal签出](./assets/storefront-cart-paypal.png){width="700" zoomable="yes"}

>[!IMPORTANT]
>
>**PSD2要求：** <br/>
>从2019年9月14日起，欧洲银行可能会拒绝不符合[PSD2](../getting-started/compliance-payment-services-directive.md)要求的支付。 为了符合PSD2的要求，PayPal Payflow Pro必须集成到第三方插件中。 若要了解详细信息，请参阅[Payflow的3-D安全](https://developer.paypal.com/api/nvp-soap/payflow/3d-secure-mpi/)。

## 要求

- [PayPal企业帐户](https://www.paypal.com/webapps/mpp/how-to-sell-online) - PayPal Payflow Pro网关将PayPal上的商家帐户与商家网站链接，同时充当网关和商家帐户。

- 如果您管理多个Adobe Commerce和Magento Open Source网站，则必须为每个网站拥有单独的PayPal商家帐户。

## 客户工作流程

1. **客户前往结帐** — 在结帐过程中，客户选择使用PayPal Payflow Pro付款，并输入信用卡信息。 客户无需拥有个人PayPal帐户。 但是，根据商家所在国家/地区，客户也可以使用个人PayPal帐户支付订单。
1. **客户提交订单** — 客户提交订单，并将订单信息发送到PayPal进行处理。 客户不会离开您网站的结账页面。
1. **PayPal完成交易** — 在发出订单时接受付款。 根据配置中指定的付款活动，将创建销售订单或销售订单和发票。

## 在线订单处理工作流

1. **管理员提交联机发票** — 商店管理员提交联机发票，并因此创建相应的交易和发票。
1. **PayPal接收交易** — 订单信息已发送到PayPal。 已生成交易记录和发票。 您可以在您的[PayPal商家帐户](https://manager.paypal.com/)中查看所有Payflow Pro Gateway交易记录。

>[!NOTE]
>
>PayPal Payflow Pro不支持部分发票和部分退款。

## 配置PayPal帐户

1. 登录到您的[PayPal企业帐户](https://manager.paypal.com/)。

1. 使用以下设置使用PayPal管理器配置[托管签出页面](https://developer.paypal.com/docs/payflow/integration-guide/configure-hosted-checkout/#configuring-hosted-pages-using-paypal-manager)：

   - 在&#x200B;**[!UICONTROL Choose your settings]**&#x200B;下，将&#x200B;**[!UICONTROL Transaction Process Mode]**&#x200B;设置为`Live`。

   - 在&#x200B;**[!UICONTROL Display options on payment page]**&#x200B;下，将&#x200B;**取消URL方法**&#x200B;设置为`POST`。

   - 在&#x200B;**[!UICONTROL Billing Information]**&#x200B;下，选中必填字段和可编辑字段的卡片安全代码&#x200B;**[!UICONTROL CSC]**&#x200B;复选框。

   - 在&#x200B;**[!UICONTROL Payment Confirmation]**&#x200B;下，将&#x200B;**[!UICONTROL Return URL Method]**&#x200B;设置为`POST`。

   - 在&#x200B;**[!UICONTROL Security Options]**&#x200B;下，完成以下设置：

      - **[!UICONTROL AVS]**： `No`
      - **[!UICONTROL CSC]**： `No`
      - **[!UICONTROL Enable Secure Token]**： `Yes`

   - 选择&#x200B;**[!UICONTROL Customize]**，然后选择&#x200B;**[!UICONTROL Layout C]**。

     布局C仅显示信用卡和借记卡字段，并且可以在您的网站上设置框架或用作独立的弹出窗口。 大小固定在490 x 565像素，为错误消息留出额外空间。 在某些系统上，此设置更正了透明重定向的问题。

1. 配置设置完成后，单击&#x200B;**[!UICONTROL Save and Publish]**。

1. 在PayPal管理器菜单中，选择&#x200B;**[!UICONTROL Account Administration]**。

1. 在&#x200B;**[!UICONTROL Manage Security]**&#x200B;下，单击&#x200B;**[!UICONTROL Transaction Settings]**&#x200B;并执行以下操作：

   - 将&#x200B;**[!UICONTROL Allow reference transactions]**&#x200B;设置为`Yes`。

   - 单击&#x200B;**[!UICONTROL Confirm]**。

     >[!NOTE]
     >
     >如果您有多个Commerce网站，则必须为每个网站创建单独的PayPal支付高级帐户。

1. 设置另一个用户（由PayPal推荐）：

   - 在主菜单的第二行中，单击&#x200B;**[!UICONTROL Manage Users]**。

   - 若要向帐户添加其他用户，请单击&#x200B;**[!UICONTROL Add User]**。 该链接位于“管理用户”标题的正上方。

   - 填写&#x200B;_[!UICONTROL Add User]_&#x200B;表单以下部分中的必填字段：

      - [!UICONTROL Admin Confirmation]
      - [!UICONTROL User Information]
      - [!UICONTROL User Login Information]
      - [!UICONTROL Assign Privilege to User]

   - 单击&#x200B;**[!UICONTROL Update]**。

1. 确保注销您的PayPal帐户。

## 在Commerce中设置PayPal Payflow Pro

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

1. 展开&#x200B;**[!UICONTROL PayPal Payment Gateways]** （如果需要）并单击&#x200B;**[!UICONTROL Configure]**&#x200B;的&#x200B;**[!UICONTROL Payflow Pro]**。

   ![配置 — Payflow Pro](./assets/payflow-pro.png){width="600" zoomable="yes"}

### 步骤2：完成所需的PayPal设置

![必需的设置 — PayPal Payflow Pro](./assets/payflow-pro-required-a.png){width="600" zoomable="yes"}

1. （可选）输入&#x200B;**[!UICONTROL Email Associated with your PayPal Merchant Account]**。

   >[!IMPORTANT]
   >
   >电子邮件地址区分大小写。 要接收付款，电子邮件地址必须与在您的PayPal商家帐户中指定的电子邮件地址匹配。

1. 输入以下凭据之一，用于登录到PayPal商家帐户：

   - **[!UICONTROL Partner]** — 您的PayPal合作伙伴ID。
   - **[!UICONTROL User]** — 如果您在帐户中设置了一个或多个其他用户，则此值是有权处理交易的用户的ID。 但是，如果尚未设置其他用户，**[!UICONTROL USER]**&#x200B;与&#x200B;**[!UICONTROL Vendor]**&#x200B;的值相同。
   - **[!UICONTROL Vendor]** — 您在注册帐户时创建的商家登录ID。

1. 输入与您的PayPal帐户关联的&#x200B;**[!UICONTROL Password]**。

1. 要运行测试事务，请将&#x200B;**[!UICONTROL Test Mode]**&#x200B;设置为`Yes`。

   在沙盒中测试配置时，仅使用PayPal推荐的[信用卡号](https://www.paypalobjects.com/en_AU/vhelp/paypalmanager_help/credit_card_numbers.htm)。 当您准备好进入生产环境时，请返回到配置并将测试模式设置为`No`。

1. 如果您的系统使用代理服务器建立与PayPal系统的连接，请将&#x200B;**[!UICONTROL Use Proxy]**&#x200B;设置为`Yes`并执行以下操作：

   - 输入&#x200B;**[!UICONTROL Proxy Host]**&#x200B;的IP地址。

   - 输入&#x200B;**[!UICONTROL Proxy Port]**&#x200B;的端口号。

     当服务器防火墙阻止直接访问PayPal服务器时，将使用代理。 在这种情况下，使用第三方服务器来中继流量。

1. 将&#x200B;**[!UICONTROL Enable this Solution]**&#x200B;设置为`Yes`。

1. 如果要为客户提供点数[PayPal](paypal.md#paypal-credit-and-pay-later)，请将&#x200B;**[!UICONTROL Enable PayPal Credit]**&#x200B;设置为`Yes`。

1. 如果要安全地存储客户付款/信用卡详细信息，以便客户不必每次都重新输入付款信息，请将&#x200B;**[!UICONTROL Vault Enabled]**&#x200B;设置为`Yes`。

### 步骤3：设置广告PayPal Credit/广告PayPal PayLater（可选）

从2.4.3版本开始，在包括PayPal的部署中支持PayPal PayLater。 此功能允许购物者以每两周一次分期付款的方式支付订单，而不是在购买时支付全额。 弃用PayPal信用体验。

将&#x200B;**[!UICONTROL Enable PayPal PayLater Experience]**&#x200B;设置为以下项之一：

- `Yes` — 设置广告PayPal PayLater
- `No` — 设置广告PayPal点数

#### 广告PayPal点数

1. 展开![部分的](../assets/icon-display-expand.png)扩展选择器&#x200B;**[!UICONTROL Advertise PayPal Credit]**。

   ![广告PayPal点数](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit.png){width="600" zoomable="yes"}

1. 若要获取帐户信息，请单击&#x200B;**[!UICONTROL Get Publisher ID from PayPal]**&#x200B;并按照说明操作。

1. 输入您的&#x200B;**[!UICONTROL Publisher ID]**。

1. 展开![部分的](../assets/icon-display-expand.png)扩展选择器&#x200B;**[!UICONTROL Home Page]**。

   ![通告PayPal点数主页设置](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit-home-page.png){width="600" zoomable="yes"}

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

1. 展开![扩展选择器](../assets/icon-display-expand.png)其余部分，对主页设置重复上述步骤：

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
   - **[!UICONTROL Checkout Payment Step]**
   - **[!UICONTROL Catalog Category Page]**

### 步骤4：完成基本设置

1. 展开![部分的](../assets/icon-display-expand.png)扩展选择器&#x200B;**[!UICONTROL Basic Settings - PayPal Payflow Pro]**。

   ![基本设置 — PayPal Payflow Pro_](../configuration-reference/sales/assets/payment-methods-paypal-payflow-pro-basic-settings.png){width="600" zoomable="yes"}

1. 对于&#x200B;**[!UICONTROL Title]**，输入在结帐时标识PayPal Payflow Pro的标题。

   建议您使用标题&#x200B;_借记卡或信用卡_。

1. 如果提供多种付款方式，请输入&#x200B;**[!UICONTROL Sort Order]**&#x200B;的数字，以确定与其他付款方式一起列出时Payflow Pro出现的顺序。

   此数字相对于其他支付方式。 （`0` =第一，`1` =第二，`2` =第三，依此类推。）

1. 将&#x200B;**[!UICONTROL Payment Action]**&#x200B;设置为以下项之一：

   - `Authorization` — 批准购买并暂停资金。 该金额在商户缴获前不会提取。
   - `Sale` — 已授权并立即从客户帐户中收回购买金额。

1. 对于&#x200B;**[!UICONTROL Credit Card Settings]**，选择您接受在您的商店中付款的信用卡。

   要选择多个卡，请按住Ctrl键(PC)或Command键(Mac)并单击每个卡。

   >[!NOTE]
   >
   >美国运通需要额外的协议。

### 步骤5：完成高级设置

1. 展开![部分的](../assets/icon-display-expand.png)扩展选择器&#x200B;**[!UICONTROL Advanced Settings]**。

   ![高级设置 — PayPal Payflow Pro](../configuration-reference/sales/assets/payment-methods-paypal-payflow-pro-advanced-settings.png){width="600" zoomable="yes"}

1. 将&#x200B;**[!UICONTROL Payment Applicable From]**&#x200B;设置为以下项之一：

   - `All Allowed Countries` — 来自您商店配置中指定的所有[国家/地区](../getting-started/store-details.md#country-options)的客户都可以使用此付款方式。
   - `Specific Countries` — 选择此选项后，将显示&#x200B;_[!UICONTROL Payment from Specific Countries]_&#x200B;列表。 按住Ctrl键(PC)或Command键(Mac)，然后选择客户可在您的商店中购买产品的每个国家/地区。

1. 要将与付款系统的通信写入日志文件，请将&#x200B;**[!UICONTROL Debug Mode]**&#x200B;设置为`Yes`。

   >[!NOTE]
   >
   >根据PCI数据安全标准，信用卡信息不会记录在日志文件中。

1. 要启用主机真实性验证，请将&#x200B;**[!UICONTROL Enable SSL Verification]**&#x200B;设置为`Yes`。

1. 若要要求客户输入CVV代码，请将&#x200B;**[!UICONTROL Require CVV Entry]**&#x200B;设置为`Yes`。

1. 根据存储需要，完成以下部分：

   - [CVV和AVS设置](#cvv-and-avs-settings)
   - [结算报表设置](#settlement-report-settings)
   - [前端体验设置](#frontend-experience-settings)

#### CVV和AVS设置

要确定当地址验证系统标识不匹配时何时应拒绝事务，请指定如何处理各种情况。

1. 展开![部分的](../assets/icon-display-expand.png)扩展选择器&#x200B;**[!UICONTROL CVV and AVS Settings]**。

   ![CVV和AVS设置 — PayPal Payflow Pro](./assets/payflow-pro-cvv-avs.png){width="600" zoomable="yes"}

1. 要拒绝基于不匹配的街道不匹配的事务，请将&#x200B;**[!UICONTROL AVS Street Does Not Match]**&#x200B;设置为`Yes`。

1. 要拒绝基于不匹配邮政编码的事务，请将&#x200B;**[!UICONTROL AVS Zip Does Not Match]**&#x200B;设置为`Yes`。

1. 要拒绝基于不匹配国家/地区标识符的事务，请将&#x200B;**[!UICONTROL International AVS Indicator Does Not Match]**&#x200B;设置为`Yes`。

1. 要拒绝基于不匹配CVV代码的事务，请将&#x200B;**[!UICONTROL International Card Security Code Does Not Match]**&#x200B;设置为`Yes`。

#### 结算报表设置

1. 展开![部分的](../assets/icon-display-expand.png)扩展选择器&#x200B;**[!UICONTROL Settlement Report Settings]**。

   ![结算报告设置 — PayPal Payflow Pro](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-settlement-report-settings.png){width="600" zoomable="yes"}

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

使用前端体验设置选择要在您的网站上显示的PayPal徽标，并自定义您的PayPal商家页面的外观。

1. 展开![部分的](../assets/icon-display-expand.png)扩展选择器&#x200B;**[!UICONTROL Frontend Experience Settings]**。

   ![前端体验设置 — PayPal Payflow Pro](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-frontend-experience-settings1.png){width="600" zoomable="yes"}

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

### 步骤6：完成PayPal Express结帐的基本设置

1. 展开![部分的](../assets/icon-display-expand.png)扩展选择器&#x200B;**[!UICONTROL Basic Settings - PayPal Express Checkout]**。

   ![快速签出基本设置](../configuration-reference/sales/assets/payment-methods-paypal-payments-pro-express-checkout-basic-settings.png){width="600" zoomable="yes"}

1. 对于&#x200B;**[!UICONTROL Title]**，输入在结帐时标识此付款方式的标题。

   建议将每个商店视图的标题设置为&#x200B;_PayPal_。

1. 如果您提供多种付款方式，请输入&#x200B;**[!UICONTROL Sort Order]**&#x200B;的数字，以确定与其他付款方式一起列出时PayPal快速结帐的出现顺序。

   此数字相对于其他支付方式。 （`0` =第一，`1` =第二，`2` =第三，依此类推。）

1. 将&#x200B;**[!UICONTROL Payment Action]**&#x200B;设置为以下项之一：

   - `Authorization` — 批准购买并暂停资金。 在商户捕获&#x200B;_金额_&#x200B;之前，不撤消该金额。
   - `Sale` — 已授权并立即从客户帐户中收回购买金额。

1. 要在产品页面上显示&#x200B;_[!UICONTROL Check out with PayPal]_&#x200B;按钮，请将&#x200B;**[!UICONTROL Display on Product Details Page]**&#x200B;设置为`Yes`。

### 步骤7：完成PayPal Express签出的高级设置

1. 展开![部分的](../assets/icon-display-expand.png)扩展选择器&#x200B;**[!UICONTROL Advanced Settings]**。

   ![快速签出高级设置](../configuration-reference/sales/assets/payment-methods-paypal-payments-pro-express-checkout-advanced-settings.png){width="600" zoomable="yes"}

1. 将&#x200B;**[!UICONTROL Display on Shopping Cart]**&#x200B;设置为`Yes`。

1. 将&#x200B;**[!UICONTROL Payment Applicable From]**&#x200B;设置为以下项之一：

   - `All Allowed Countries` — 来自您商店配置中指定的所有国家/地区的客户可以使用此付款方式。
   - `Specific Countries` — 选择此选项后，将显示&#x200B;_[!UICONTROL Payment from Specific Countries]_&#x200B;列表。 要选择多个国家/地区，请按住Ctrl键(PC)或Command键(Mac)并单击每个项目。

1. 要将与付款系统的通信写入日志文件，请将&#x200B;**[!UICONTROL Debug Mode]**&#x200B;设置为`Yes`。

   >[!NOTE]
   >
   >根据PCI数据安全标准，信用卡信息不会记录在日志文件中。

1. 要启用主机真实性验证，请将&#x200B;**[!UICONTROL Enable SSL Verification]**&#x200B;设置为`Yes`。

1. 要显示PayPal网站中按行项目的客户订单的完整摘要，请将&#x200B;**[!UICONTROL Transfer Cart Line Items]**&#x200B;设置为`Yes`。

1. 要允许客户从PayPal网站完成交易而不返回商店进行订单审核，请将&#x200B;**[!UICONTROL Skip Order Review Step]**&#x200B;设置为`Yes`。

1. 完成后，单击&#x200B;**[!UICONTROL Save Config]**。

### 步骤8：添加Google reCAPTCHA

为了更好地保护PayPal Payflow Pro结账，请启用Google reCAPTCHA。 它包含使用可点击界面或验证客户的不可见检查来运行reCAPTCHA的选项。 建议使用不可见选项来提高销售转化率并保护您的商店。 有关详细信息，请参阅[Google reCAPTCHA](../systems/security-google-recaptcha.md)。

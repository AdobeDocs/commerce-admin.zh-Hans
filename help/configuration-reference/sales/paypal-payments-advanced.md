---
title: '[!UICONTROL Sales] &amp；gt； [!UICONTROL Payment Methods] &amp；gt； [!UICONTROL PayPal Payments Advanced]'
description: 查看Commerce管理员的[!UICONTROL Sales] &amp；gt； [!UICONTROL Payment Methods]页面上[!UICONTROL PayPal Payments Advanced]部分中的配置设置。
exl-id: c9159408-fbdf-4146-8292-9952cd5d01fa
feature: Configuration, Payments
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '1280'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Payment Methods] > [!UICONTROL PayPal Payments Advanced]

>[!IMPORTANT]
>
>**PSD2要求：** <br/>
>从2019年9月14日起，欧洲银行可能会拒绝不符合[PSD2](../../getting-started/compliance-payment-services-directive.md)要求的支付。 为了符合PSD2，[!DNL PayPal Payments Advanced]必须与[!DNL Cardinal Commerce]集成。 若要了解详细信息，请参阅[Payflow的3-D安全](https://developer.paypal.com/api/nvp-soap/payflow/3d-secure-overview/)。

{{config}}

## [!UICONTROL Required Settings]

![必需的设置](./assets/payment-methods-paypal-payments-advanced-required.png)<!-- zoom -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Email Associated with PayPal Merchant Account] | 网站 | （可选）与您的PayPal商家帐户关联的任何电子邮件地址。 电子邮件地址区分大小写，且必须与帐户中的地址完全匹配。 |
| [!UICONTROL Partner] | 网站 | 您的PayPal合作伙伴ID（如果适用）。 |
| [!UICONTROL Vendor] | 网站 | 您的PayPal用户登录名。 |
| 用户 | 网站 | 您PayPal帐户中其他用户的ID。 |
| [!UICONTROL Password] | 网站 | 与您的PayPal商家帐户关联的密码。 |
| [!UICONTROL Test Mode] | 网站 | 启用后，将在测试环境中运行PayPal Payments Advanced。 当您准备好在生产模式下“上线”时，请关闭测试模式。 选项： `Yes` / `No` |
| [!UICONTROL Use Proxy] | 网站 | 当服务器防火墙阻止直接访问PayPal服务器时，可以使用代理重定向流量。 如果适用，则标识用于与PayPal服务器建立连接的代理服务器。 选项： `Yes` / `No` <br/><br/>如果启用，请设置选项： <br/>**`Proxy Host`**— 代理主机的IP地址。<br/>**`Proxy Port`** — 代理端口数。 |
| [!UICONTROL Enable this Solution] | 网站 | 确定PayPal付款高级是否作为付款方式提供给您的客户。 |
| [!UICONTROL Enable PayPal Credit] | 网站 | 确定客户是否可以将PayPal信用作为付款选项。 |

{style="table-layout:auto"}

## [!UICONTROL Advertise PayPal Credit]

![广告PayPal点数](./assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit.png)<!-- zoom -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Publisher ID] | 网站 | 与您的PayPal信用帐户关联的发布者ID。 |
| [!UICONTROL Get Publisher ID from PayPal] |  | 从PayPal获取您的发布者ID。 |
| [!UICONTROL Home Page] | 网站 | 确定主页上[!DNL PayPal Credit]横幅的位置和大小。 选项： <br/>**`Display`**— 确定商店的主页上是否显示[!DNL PayPal Credit]横幅。 选项： `Yes` / `No`<br/>**`Position`** — 确定[!DNL PayPal Credit]横幅在主页上的位置。 选项： Header （居中） / Sidebar （右） <br/>**`Size`**— 确定主页上[!DNL PayPal Credit]横幅的大小。 选项： `190 x 100` / `234 x 60` / `300 x 50` / `468 x 60` / `728 x 90` /` 800 x 66` |
| [!UICONTROL Catalog Category Page] | 网站 | 确定类别页面上[!DNL PayPal Credit]横幅的位置和大小。 选项： （与[!UICONTROL Home Page]相同） |
| [!UICONTROL Catalog Product Page] | 网站 | 确定产品页面上[!DNL PayPal Credit]横幅的位置和大小。 选项： （与[!UICONTROL Home Page]相同） |
| [!UICONTROL Checkout Cart Page] | 网站 | 确定购物车页面上[!DNL PayPal Credit]横幅的位置和大小。 选项： （与[!UICONTROL Home Page]相同） |

{style="table-layout:auto"}

## [!UICONTROL Basic Settings]

![基本设置](./assets/payment-methods-paypal-payments-advanced-basic-settings.png)<!-- zoom -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Title] | 商店视图 | 在结帐期间将PayPal Payments Advanced标识为付款方法的名称。 |
| [!UICONTROL Sort Order] | 商店视图 | 在结帐期间与其他付款方法一起列出时，确定PayPal付款高级显示顺序的编号。 |
| [!UICONTROL Payment Action] | 网站 | 确定PayPal在提交订单时执行的操作。 选项： <br/>**`Authorization`**— 批准购买，但保留资金。 该金额在商户将该金额“扣押”前不予提取。<br/>**`Sale`** — 已授权并立即从客户帐户中收回购买金额。 |

{style="table-layout:auto"}

## [!UICONTROL Advanced Settings]

![高级设置](./assets/paypal-advanced-settings2.png)<!-- zoom -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Payment Applicable From] | 网站 | 确定适用的国家/地区选择的范围。 选项： `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Countries Payment Applicable From] | 网站 | 标识接受付款的每个国家/地区。 只有帐单地址在选定国家/地区的客户才能使用此付款方法进行购买。 |
| [!UICONTROL Debug Mode] | 网站 | 在日志文件中记录您的商店和支付系统之间发送的消息。 选项： `Yes` / `No` <br/><br/>**_注意：_**&#x200B;日志文件存储在服务器上，只有开发人员才能访问。 根据PCI数据安全标准，信用卡信息不会记录在日志文件中。 |
| [!UICONTROL Enable SSL Verification] | 网站 | 确定是否在事务发生之前验证主机上的安全通道。 选项： `Yes` / `No` |
| [!UICONTROL CVV Entry is Editable] | 网站 | 确定客户在输入CVV后是否可以对其进行编辑。 选项： `Yes` / `No` |
| [!UICONTROL Require CVV Entry] | 网站 | 确定是否要求客户输入其信用卡背面的CVV代码。 选项： `Yes` / `No` |
| [!UICONTROL Send Email Confirmation] | 网站 | 确定客户是否收到付款的电子邮件确认。 选项： `Yes` / `No` |
| [!UICONTROL URL Method for Cancel URL and Return URL] | 网站 | 确定在交易期间用于与PayPal服务器交换信息的方法。 选项： <br/>**`GET`**— 检索由进程产生的信息。 （这是默认方法。）<br/>**`POST`** — 将数据块（如输入到表单中的数据）发送到数据处理过程。 |

{style="table-layout:auto"}

## [!UICONTROL Settlement Report Settings]

![结算报告设置](./assets/payment-methods-paypal-payments-advanced-settlement-report-settings.png)<!-- zoom -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| **[!UICONTROL SFTP Credentials]** |  |  |
| [!UICONTROL Login] | 网站 | 登录PayPal安全FTP服务器所需的用户名。 |
| [!UICONTROL Password] | 网站 | 登录PayPal安全FTP服务器所需的密码。 |
| [!UICONTROL Sandbox Mode] | 网站 | 启用后，将在生产环境中“上线”之前在测试环境中运行报告。 选项： `Yes` / `No` |
| [!UICONTROL Custom Endpoint Hostname or IP-Address] | 网站 | 管理结算报表的URL。 默认值： `reports.paypal.com` |
| [!UICONTROL Custom Path] | 网站 | 结算报表在服务器上保存的路径。 默认值： `/ppreports/outgoing` |
| **[!UICONTROL Scheduled Fetching]** |  |  |
| [!UICONTROL Enable Automatic Fetching] | 网站 | 启用后，将按计划自动获取结算报表。 选项： `Yes` / `No` |
| [!UICONTROL Schedule] | 全局 | 确定PayPal生成结算报表的频率。 选项： `Daily` / `Every 3 days` / `Every 7 days` / `Every 10 days` / `Every 14 days` / `Every 30 days` / `Every 40 days` |
| [!UICONTROL Time of Day] | 全局 | 确定生成结算报告的小时、分钟和秒。 |

{style="table-layout:auto"}

## [!UICONTROL Frontend Experience Settings]

![前端体验设置](./assets/payment-methods-paypal-payments-advanced-frontend-experience-settings.png)<!-- zoom -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL PayPal Product Logo] | 商店视图 | 确定您商店中显示的PayPal徽标。 两种尺寸共有四种基本样式。 选项： `No Logo` / `We prefer PayPal (150 x 60)` / `We prefer PayPal (150 x 40)` / `Now accepting PayPal (150 x 60)` / `Now accepting PayPal (150 x 40)` / `Payments by PayPal (150 x 60)` / `Payments by PayPal (150 x 40)` / `Shop now using (150 x 60)` / `Shop now using (150 x 40)` |
| **[!UICONTROL PayPal Merchant Pages Style]** |  |  |
| [!UICONTROL Page Style] | 商店视图 | 确定PayPal商家页面的外观。 允许的值： <br/>**`paypal`**— 使用PayPal页面样式。<br/>**`primary`** — 使用您在帐户配置文件中标识为“primary”样式的页面样式。 <br/>**`your_custom_value`**— 使用在您的帐户配置文件中指定的自定义付款页面样式。 |
| [!UICONTROL Header Image URL] | 商店视图 | 出现在签出页面左上角的图像的URL。 最大大小为750 x 90像素。 <br/><br/>**_注意：_**&#x200B;PayPal建议将映像存储在安全(https)服务器上。 否则，客户的浏览器可能会警告“页面包含安全和非安全项目。” |
| [!UICONTROL Header Image Background Color] | 商店视图 | 签出页面上页眉的背景颜色的六字符[十六进制颜色](https://en.wikipedia.org/wiki/Web_colors)代码。 您可以使用大写和小写字符输入代码。 |
| [!UICONTROL Header Image Border Color] | 商店视图 | 标头周围两像素边框的六字符十六进制颜色代码。 |
| [!UICONTROL Page Background Color] | 商店视图 | 用于结账页面的背景颜色的六字符十六进制颜色代码，显示在页眉和付款表单后面。 |

{style="table-layout:auto"}

## [!UICONTROL Basic Settings - PayPal Express Checkout]

![PayPal Express签出基本设置](./assets/payment-methods-paypal-advanced-express-checkout-basic-settings.png)<!-- zoom -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Title] | 商店视图 | 在结帐期间标识PayPal Express结帐付款方法的名称。 |
| [!UICONTROL Sort Order] | 商店视图 | 当在结帐过程中与其他付款方法一起列出时，确定PayPal Express结帐顺序的编号。 在列表顶部输入`0`。 |
| [!UICONTROL Payment Action] | 网站 | 确定PayPal在收到订单时执行的操作。 选项： <br/>**`Authorization`**— 批准购买，但保留资金。 该金额在商户将该金额“扣押”前不予提取。<br/>**`Sale`** — 已授权并立即从客户帐户中收回购买金额。 <br/>**`Order`**— 表示与PayPal之间的协议，该协议允许商家在定义的时间段内从客户的买方帐户中捕获一个或多个金额，最多可捕获订购的总额。 最长可为29天。 必须从Commerce管理员生成一张或多张发票才能获取资金。 |
| [!UICONTROL URL Display on Product Details Page] | 商店视图 | 确定“使用PayPal结帐”按钮是否显示在产品页面上。 选项： `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL PayPal Express Checkout - Advanced Settings]

![PayPal Express签出高级设置](./assets/payment-methods-paypal-payments-advanced-express-checkout-advanced.png)<!-- zoom -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Display on Shopping Cart] | 商店视图 | 确定PayPal Express结帐在购物车中是否显示为付款选项。 选项： `Yes` （推荐） / `No` |
| [!UICONTROL Payment Action Applicable From] | 网站 | 确定适用的国家/地区选择的范围。 选项： `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Countries Payment Applicable From] | 网站 | 标识接受付款的每个国家/地区。 只有帐单地址在选定国家/地区的客户才能使用此付款方法进行购买。 |
| [!UICONTROL Debug Mode] | 网站 | 在日志文件中记录您的商店和PayPal支付系统之间发送的消息。 选项： `Yes` / `No` <br/><br/>**_注意：_**&#x200B;日志文件存储在服务器上，只有开发人员才能访问。 根据PCI数据安全标准，信用卡信息不会记录在日志文件中。 |
| [!UICONTROL Enable SSL Verification] | 网站 | 启用主机安全证书的验证。 选项： `Yes` / `No` |
| [!UICONTROL Transfer Cart Line Items] | 网站 | 显示PayPal网站上客户购物车中行项目的完整摘要。 选项： `Yes` / `No` |
| [!UICONTROL Skip Order Review Step] | 网站 | 确定客户是否可以从PayPal网站完成交易，或者是否需要返回您的商店并在提交订单之前完成订单审核步骤。 选项： `Yes` / `No` |

{style="table-layout:auto"}

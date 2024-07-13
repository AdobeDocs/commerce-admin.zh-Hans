---
title: '[!UICONTROL Sales] &amp；gt； [!UICONTROL Payment Methods] &amp；gt； [!UICONTROL PayPal Express Checkout]'
description: 查看Commerce管理员的[!UICONTROL Sales] &amp；gt； [!UICONTROL Payment Methods]页面上[!UICONTROL PayPal Express Checkout]部分中的配置设置。
exl-id: aae5b1d9-f47e-447a-b40c-924f8d2ee824
feature: Configuration, Payments
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '1702'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Payment Methods] > [!UICONTROL PayPal Express Checkout]

>[!IMPORTANT]
>
>**PSD2要求：** <br/>
>从2019年9月14日起，欧洲银行可能会拒绝不符合[PSD2](../../getting-started/compliance-payment-services-directive.md)要求的支付。 PayPal Express Checkout无需执行任何操作即可符合PSD2，因为所有要求都由PayPal处理。

{{config}}

## [!UICONTROL Required PayPal Settings]

![PayPal Express签出必需的设置](./assets/paypal-express-required-settings.png)<!-- zoom -->

<!-- [PayPal Express Checkout Required Settings](../../stores-purchase/paypal-express-checkout.html) -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Enable this Solution] | 网站 | 激活[!DNL PayPal Express Checkout]作为客户可用的付款方式。 选项： `Yes` / `No` |
| [!UICONTROL Enable In-Context Checkout Experience] | 网站 | 激活简化的PayPal In-Context Checkout作为客户可用的付款方式。 选项： `Yes` / `No` |
| [!UICONTROL Enable PayPal Credit] | 网站 | 启用PayPal点数功能，允许客户立即购买但稍后付款。 你可以提前付钱，但客户有更多时间付钱。 选项： `Yes` / `No` |

{style="table-layout:auto"}

### [!UICONTROL Express Checkout]

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Email Associated with PayPal Merchant Account] | 网站 | 指定您在建立PayPal商家帐户时指定的电子邮件地址。 电子邮件地址区分大小写，且必须与PayPal系统中的电子邮件地址完全匹配。 |
| [!UICONTROL API Authentication Methods] | 网站 | 确定用于API身份验证的方法。 选项： <br/>**`API Signature`**— 在表单中显示&#x200B;_[!UICONTROL API Signature]_字段。<br/>**`API Certificate`**— 在表单中显示_[!UICONTROL API Certificate]_&#x200B;字段。 |
| [!UICONTROL API Username] | 网站 | 与您的PayPal商家帐户关联的API用户名。 |
| [!UICONTROL API Password] | 网站 | 与您的PayPal商家帐户关联的API密码。 |
| [!UICONTROL API Signature] | 网站 | 与您的PayPal商家帐户关联的API签名。 |
| [!UICONTROL API Certificate] | 网站 | 浏览以上传API证书。 |
| [!UICONTROL Get Credentials from PayPal] |  | 从PayPal获取您的API凭据。 |
| [!UICONTROL Sandbox Credentials] |  | 从PayPal获取您的沙盒凭据。 |
| [!UICONTROL Sandbox Mode] | 网站 | 要在测试环境中运行PayPal Express签出，请输入您的沙盒API凭据，并将其设置为`Yes`。 选项： `Yes` / `No` |
| [!UICONTROL API Uses Proxy] | 网站 | 如果您的系统使用代理服务器在Commerce和PayPal系统之间建立连接，请将此参数设置为`Yes`。 选项： `Yes` / `No` |
| [!UICONTROL Proxy Host] | 网站 | 如果API使用代理，这会指定代理主机的IP地址。 |
| [!UICONTROL Proxy Port] | 网站 | 如果API使用代理，这会指定代理主机使用的端口。 |

{style="table-layout:auto"}

### [!UICONTROL Advertise PayPal Credit]

![广告PayPal点数](./assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit.png)<!-- zoom -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Publisher ID] | 网站 | 与您的PayPal信用帐户关联的发布者ID。 |
| [!UICONTROL Get Publisher ID from PayPal] |  | 从PayPal获取您的发布者ID。 |
| [!UICONTROL Home Page] | 网站 | 确定主页上[!DNL PayPal Credit]横幅的位置和大小。 选项： <br/>**显示** — 在商店的主页上显示[!DNL PayPal Credit]横幅。 选项： `Yes` / `No` <br/>**位置** — 确定主页上[!DNL PayPal Credit]横幅的位置。 选项： Header （居中） / Sidebar （右） <br/>**大小** — 确定主页上[!DNL PayPal Credit]横幅的大小。 选项： `190 x 100` / `234 x 60` / `300 x 50` / `468 x 60` / `728 x 90` /` 800 x 66` |
| [!UICONTROL Catalog Category Page] | 网站 | 确定类别页面上[!DNL PayPal Credit]横幅的位置和大小。 选项： （与[!UICONTROL Home Page]相同） |
| [!UICONTROL Catalog Product Page] | 网站 | 确定产品页面上[!DNL PayPal Credit]横幅的位置和大小。 选项： （与[!UICONTROL Home Page]相同） |
| [!UICONTROL Checkout Cart Page] | 网站 | 确定购物车页面上[!DNL PayPal Credit]横幅的位置和大小。 选项： （与[!UICONTROL Home Page]相同） |

{style="table-layout:auto"}

## [!UICONTROL Basic Settings]

![基本设置](./assets/payment-methods-paypal-express-checkout-basic-settings.png)<!-- zoom -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Title] | 商店视图 | 在结帐期间标识PayPal Express结帐付款方法的名称。 |
| [!UICONTROL Sort Order] | 商店视图 | 在结帐期间与其他付款方法一起列出时，用于确定PayPal Express结帐顺序的编号。 在列表顶部输入`0`。 |
| [!UICONTROL Payment Action] | 网站 | 确定PayPal在收到订单时执行的操作。 选项： <br/>**`Authorization`**— 批准购买，但保留资金。 该金额在商户将该金额“扣押”前不予提取。<br/>**`Sale`** — 已授权并立即从客户帐户中收回购买金额。 <br/>**`Order`**— 表示与PayPal之间的协议，该协议允许商家在定义的时间段内从客户的买方帐户中捕获一个或多个金额，最多可捕获订购的总额。 最长可为29天。 必须从Commerce管理员生成一张或多张发票才能获取资金。 |
| [!UICONTROL Display on Product Details Page] | 商店视图 | 确定“使用PayPal结帐”按钮是否显示在产品页面上。 选项包括：`Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Advanced Settings]

![高级设置](./assets/payment-methods-paypal-express-checkout-advanced-settings.png)<!-- zoom -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Display on Shopping Cart] | 商店视图 | 确定PayPal Express结帐在购物车中是否显示为付款选项。 选项： `Yes` （推荐PayPal） / `No` |
| [!UICONTROL Payment Action Applicable From] | 网站 | 确定适用的国家/地区选择的范围。 选项： `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Countries Payment Applicable From] | 网站 | 标识接受付款的每个国家/地区。 只有帐单地址在选定国家/地区的客户才能使用此付款方法进行购买。 |
| [!UICONTROL Debug Mode] | 网站 | 在日志文件中记录您的商店和支付系统之间发送的消息。 选项： `Yes` / `No` <br/><br/>**_注意：_**日志文件存储在服务器上，只有开发人员才能访问。 根据PCI数据安全标准，信用卡信息不会记录在日志文件中。 |
| [!UICONTROL Enable SSL Verification] | 网站 | 启用主机安全证书的验证。 选项： `Yes` / `No` |
| [!UICONTROL Transfer Cart Line Items] | 网站 | 显示PayPal网站上客户购物车中行项目的完整摘要。 选项： `Yes` / `No` |
| [!UICONTROL Transfer Shipping Options] | 网站 | 包括PayPal网站上最多十个送货选项。 选项： `Yes` / `No` |
| [!UICONTROL Shortcut Buttons Flavor] | 商店视图 | 确定用于PayPal接受按钮的图像类型。 选项： <br/>**`Dynamic`**- （推荐）显示可从PayPal服务器动态更改的图像。<br/>**`Static`** — 显示无法动态更改的静态图像。 |
| [!UICONTROL Enable PayPal Guest Checkout] | 网站 | 允许没有PayPal帐户的客户通过PayPal Express结帐进行购买。 选项： `Yes` / `No` |
| [!UICONTROL Require Customer's Billing Address] | 网站 | 确定是否要求客户帐单地址。 选项： `Yes` / `No` / `For Virtual Quotes Only` |
| [!UICONTROL Billing Agreement Signup] | 网站 | 确定客户能否与您的商店签订[帐单协议](../../stores-purchase/paypal-billing-agreements.md)。 选项： <br/>**`Auto`**— 客户可以在Express Checkout期间注册帐单协议。<br/>**`Ask Customer`** — 询问客户是否要注册计费协议。 <br/>**`Never`**— 不向客户提供注册计费协议的选项。 |
| [!UICONTROL Skip Order Review Step] | 网站 | 确定客户是否可以从PayPal网站完成交易，或者是否需要返回您的商店并在提交订单之前完成订单审核步骤。 选项： `Yes` / `No` |

{style="table-layout:auto"}

### [!UICONTROL Billing Agreement Settings]

![帐单协议设置](./assets/payment-methods-paypal-express-checkout-billing-agreement-settings.png)<!-- zoom -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Enabled] | 网站 | 启用后，客户在结帐期间将看到帐单协议作为付款选项。 选项： `Yes` / `No` |
| [!UICONTROL Title] | 商店视图 | 在结账期间显示为付款选项的PayPal计费协议选项的标签。 |
| [!UICONTROL Sort Order] | 商店视图 | 确定在结账期间将计费协议与其他支付方法一起列出的顺序。 |
| [!UICONTROL Payment Action] | 网站 | 确定PayPal如何管理交易：选项： <br/>**授权** — 批准购买，但保留资金。 该金额在商户将该金额“扣押”前不予提取。 <br/>**Sale** — 已授权并立即从客户帐户中收回购买金额。 |
| [!UICONTROL Payment Applicable From] | 网站 | 确定适用的国家/地区选择的范围。 选项：所有允许的国家/地区/特定国家/地区 |
| [!UICONTROL Countries Payment Applicable From] | 网站 | 标识接受付款的每个国家/地区。 只有帐单地址在选定国家/地区的客户才能使用此付款方法进行购买。 |
| [!UICONTROL Debug Mode] | 网站 | 在日志文件中记录与支付系统的通信。 选项： `Yes` / `No` <br/><br/>**_注意：_**日志文件存储在服务器上，只有开发人员才能访问。 根据PCI数据安全标准，信用卡信息不会记录在日志文件中。 |
| [!UICONTROL Enable SSL Verification] | 网站 | 启用验证步骤，确保事务通过加密的SSL通道进行。 选项： `Yes` / `No` |
| [!UICONTROL Transfer Cart Line Items] | 网站 | 启用后，会在PayPal支付页面上显示购物车中的行项目摘要。 选项： `Yes` / `No` |
| [!UICONTROL Allow in Billing Agreement Wizard] | 网站 | 启用后，客户可以从其客户帐户的仪表板启动计费协议。 |

{style="table-layout:auto"}

### [!UICONTROL Settlement Report Settings]

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
| [!UICONTROL Schedule] | 网站 | 确定PayPal生成结算报表的频率。 选项： `Daily` / `Every 3 days` / `Every 7 days` / `Every 10 days` / `Every 14 days` / `Every 30 days` / `Every 40 days` |
| [!UICONTROL Time of Day] | 网站 | 确定生成结算报告的小时、分钟和秒。 |

{style="table-layout:auto"}

### [!UICONTROL Frontend Experience Settings]

![前端体验设置 — PayPal商家页面样式](./assets/payment-methods-paypal-payments-advanced-frontend-experience-settings1.png)<!-- zoom -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL PayPal Product Logo] | 商店视图 | 确定您商店中显示的PayPal徽标。 两种尺寸共有四种基本样式。 选项： `No Logo` / `We prefer PayPal (150 x 60)` / `We prefer PayPal (150 x 40)` / `Now accepting PayPal (150 x 60)` / `Now accepting PayPal (150 x 40)` / `Payments by PayPal (150 x 60)` / `Payments by PayPal (150 x 40)` / `Shop now using (150 x 60)` / `Shop now using (150 x 40)` |
| **[!UICONTROL PayPal Merchant Pages Style]** |  |  |
| [!UICONTROL Page Style] | 商店视图 | 确定PayPal商家页面的外观。 允许的值： **`paypal`** — 使用PayPal页面样式。 <br/>**`primary`**— 使用您在帐户配置文件中标识为“primary”样式的页面样式。<br/>**`your_custom_value`** — 使用在您的帐户配置文件中指定的自定义付款页面样式。 |
| [!UICONTROL Header Image URL] | 商店视图 | 出现在签出页面左上角的图像的URL。 最大大小为750 x 90像素。 <br/><br/>**_注意：_**PayPal建议将映像存储在安全(https)服务器上。 否则，客户的浏览器可能会警告“页面包含安全和非安全项目。” |
| [!UICONTROL Header Image Background Color] | 商店视图 | 签出页面上页眉的背景颜色的六字符[十六进制颜色](https://en.wikipedia.org/wiki/Web_colors)代码。 您可以使用大写和小写字符输入代码。 |
| [!UICONTROL Header Image Border Color] | 商店视图 | 标头周围双像素边框的六字符[十六进制颜色](https://en.wikipedia.org/wiki/Web_colors)代码。 |
| [!UICONTROL Page Background Color] | 商店视图 | 显示在页眉和付款表单后面的结账页面背景颜色的六字符[十六进制颜色](https://en.wikipedia.org/wiki/Web_colors)代码。 |

{style="table-layout:auto"}

#### [!UICONTROL Customize Smart Buttons (Basic)]

![前端体验设置 — 自定义智能按钮](./assets/payment-methods-paypal-payments-advanced-frontend-experience-settings2.png)<!-- zoom -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Customize Button] | 商店视图 | 确定是否可自定义PayPal智能按钮以匹配商店的布局和主题。 您可以将这些更改单独应用到“结帐”页面、“产品”页面、“购物车”页面和“迷你购物车”中。 |
| [!UICONTROL Label] | 商店视图 | PayPal在“智能支付”按钮上显示的文本。 选项： <br/>**`Checkout`**（显示为“PayPal结帐”）<br/>**`Pay`** （显示为“使用PayPal付款”）<br/>**`Buy Now`**（显示为“使用PayPal立即购买”）<br/>**`PayPal`** （显示为“PayPal”）<br/>**`Installment`**（显示为“PayPal”）<br/>**`Credit`** （显示为“PayPal CREDIT”） |
| [!UICONTROL Layout] | 商店视图 | 确定是垂直还是水平显示PayPal智能按钮。 选项： <br/>**`Vertical`**— 无论是否选择“启用来宾结帐”，购买者都必须登录PayPal或创建PayPal帐户。<br/>**`Horizontal`** — 选择“启用来宾签出”时，会在PayPal弹出窗口中显示&#x200B;**`Pay with Debit Card or Credit Card`**&#x200B;按钮。 否则，购买者必须登录到PayPal或创建PayPal帐户。 |
| [!UICONTROL Size] | 商店视图 | 设置智能支付按钮的大小。 选项： <br/>**`Medium`**- 250像素x 35像素<br/>**`Large`** - 350像素x 40像素&#x200B;<br/>**`Responsive`**— （默认）调整到容器的宽度。 最小宽度为100像素，最大宽度为500像素。 高度会根据宽度进行动态调整。 |
| [!UICONTROL Shape] | 商店视图 | 设置智能支付按钮的形状。 选项： `Pill` （默认） / `Rectangle` |
| [!UICONTROL Color] | 商店视图 | 设置智能支付按钮的颜色。 选项： `Gold` （默认） / `Blue` / `Silver` / `Black` |

{style="table-layout:auto"}

#### [!UICONTROL Customize Smart Buttons (Features)]

![前端体验设置 — 自定义智能按钮（功能）](./assets/payment-methods-paypal-payments-advanced-frontend-experience-settings3.png)<!-- zoom -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Disable Funding Options] | 商店视图 | 确定“结帐”页面上显示的其他PayPal融资选项。 所选选项永远不会显示在“结帐”页面上。 仅当PayPal支持商店货币和买方地点时，才会显示未选定的选项。 选项： `PayPal Credit` / `PayPal Guest Checkout` `Credit Card Icons` / `Elektronisches Lastschriftverfahren - German ELV` |

{style="table-layout:auto"}

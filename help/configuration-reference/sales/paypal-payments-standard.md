---
title: ’[!UICONTROL Sales] &gt； [!UICONTROL Payment Methods] &gt； [!UICONTROL PayPal Payments Standard]’
description: 在中查看配置设置 [!UICONTROL PayPal Payments Standard] 部分，位于 [!UICONTROL Sales] &gt； [!UICONTROL Payment Methods] 商务管理员页面。
exl-id: 846d9b6f-92b9-4610-b894-625f67f4cff8
feature: Configuration, Payments
source-git-commit: 76bd1b1af9b55d69bd98209d70fb5518f190a3e1
workflow-type: tm+mt
source-wordcount: '1314'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Payment Methods] > [!UICONTROL PayPal Payments Standard]

>[!IMPORTANT]
>
>**PSD2要求：**<br/>
>从2019年9月14日起，欧洲银行可能会拒绝未满足要求的支付 [PSD2](../../getting-started/compliance-payment-services-directive.md) 要求。 无需执行任何操作 [!DNL PayPal Payments Standard] 以符合PSD2，因为所有要求都由PayPal处理。

{{config}}

## [!UICONTROL Required Settings]

![必需的设置](./assets/payment-methods-paypal-payments-standard-required.png)<!-- zoom -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Email Associated with PayPal Merchant Account] | 网站 | （可选）与您的PayPal商家帐户关联的任何电子邮件地址。 电子邮件地址区分大小写，且必须与帐户中的地址完全匹配。 |
| [!UICONTROL Partner] | 网站 | 您的PayPal合作伙伴ID（如果适用）。 |
| [!UICONTROL Vendor] | 网站 | 您的PayPal用户登录名。 |
| 用户 | 网站 | 您PayPal帐户中其他用户的ID。 |
| [!UICONTROL Password] | 网站 | 与您的PayPal商家帐户关联的密码。 |
| [!UICONTROL Test Mode] | 网站 | 启用后，将在测试环境中运行PayPal Payments Pro。 当您准备好在生产模式下“上线”时，请关闭测试模式。 选项： `Yes` / `No` |
| [!UICONTROL Use Proxy] | 网站 | 当服务器防火墙阻止直接访问PayPal服务器时，可以使用代理重定向流量。 如果适用，则标识用于与PayPal服务器建立连接的代理服务器。 选项： `Yes` / `No` <br/><br/>如果启用，请设置以下选项： <br/>**`Proxy Host`**— 代理主机的IP地址。<br/>**`Proxy Port`**  — 代理端口的编号。 |
| [!UICONTROL Enable this Solution] | 网站 | 确定PayPal Payments Pro是否作为付款方式提供给您的客户。 |
| [!UICONTROL Enable PayPal Credit] | 网站 | 确定客户是否可以将PayPal信用作为付款选项。 |

{：style=&quot;table-layout：auto&quot;}

## 广告PayPal点数

![广告PayPal点数](./assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit.png)<!-- zoom -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Publisher ID] | 网站 | 与您的PayPal信用帐户关联的发布者ID。 |
| [!UICONTROL Get Publisher ID from PayPal] |  | 从PayPal获取您的发布者ID。 |
| [!UICONTROL Home Page] | 网站 | 确定 [!DNL PayPal Credit] 标题栏目中。 选项： <br/>**`Display`**— 确定 [!DNL PayPal Credit] 横幅会显示在您商店的主页上。 选项： `Yes` / `No`<br/>**`Position`**  — 确定 [!DNL PayPal Credit] 标题栏目中。 选项： `Header (center)` / `Sidebar (right)` <br/>**`Size`**— 确定 [!DNL PayPal Credit] 标题栏目中。 选项： `190 x 100` / `234 x 60` / `300 x 50` / `468 x 60` / `728 x 90` /` 800 x 66` |
| [!UICONTROL Catalog Category Page] | 网站 | 确定 [!DNL PayPal Credit] 类别页面上的横幅。 选项： (与 [!UICONTROL Home Page]) |
| [!UICONTROL Catalog Product Page] | 网站 | 确定 [!DNL PayPal Credit] 产品页面上的横幅。 选项： (与 [!UICONTROL Home Page]) |
| [!UICONTROL Checkout Cart Page] | 网站 | 确定 [!DNL PayPal Credit] 购物车页面上的横幅。 选项： (与 [!UICONTROL Home Page]) |

{：style=&quot;table-layout：auto&quot;}

## [!UICONTROL Basic Settings - PayPal Payments Standard]

![基本设置](./assets/paypal-standard-basic-settings.png)<!-- zoom -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Title] | 商店视图 | 在结帐期间将PayPal Payments Pro标识为付款方法的名称。 |
| [!UICONTROL Sort Order] | 商店视图 | 一个数字，用于在结账过程中与其他支付方式一起列出PayPal Payments Pro时确定显示顺序。 |
| [!UICONTROL Payment Action] | 网站 | 确定PayPal在提交订单时执行的操作。 选项： <br/>**`Authorization`**— 批准购买，但保留资金。 该金额在商户将该金额“扣押”前不予提取。<br/>**`Sale`**  — 采购金额已获授权并立即从客户账户中提取。 |
| [!UICONTROL Credit Card Settings] |  |  |
| [!UICONTROL Allowed Credit Cart Types] | 网站 | 确定客户在结帐期间可用的信用卡。 选择每个受支持的卡片。 选项： `American Express` （需要额外协议）/ `Visa` / `MasterCard` / `Discover` / `JCB` |

{：style=&quot;table-layout：auto&quot;}

## [!UICONTROL Advanced Settings]

![高级设置](./assets/payment-methods-paypal-payment-standard-advanced.png)<!-- zoom -->

| 字段 | 范围 | 描述 |
|--- |--- |--- |
| [!UICONTROL Display on Shopping Cart] | 商店视图 | 确定PayPal Express结帐在购物车中是否显示为付款选项。 选项： `Yes` （推荐） / `No` |
| [!UICONTROL Payment Action Applicable From] | 网站 | 确定适用的国家/地区选择的范围。 选项： `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Countries Payment Applicable From] | 网站 | 标识接受付款的每个国家/地区。 只有帐单地址在选定国家/地区的客户才能使用此付款方法进行购买。 |
| [!UICONTROL Debug Mode] | 网站 | 在日志文件中记录您的商店和PayPal支付系统之间发送的消息。 选项： `Yes` / `No` <br/><br/>**_注意：_**日志文件存储在服务器上，只有开发人员才能访问。 根据PCI数据安全标准，信用卡信息不会记录在日志文件中。 |
| [!UICONTROL Enable SSL Verification] | 网站 | 启用主机安全证书的验证。 选项： `Yes` / `No` |
| [!UICONTROL Transfer Cart Line Items] | 网站 | 显示PayPal网站上客户购物车中行项目的完整摘要。 选项： `Yes` / `No` |
| [!UICONTROL Transfer Shipping Options] | 网站 | 包括PayPal网站上最多十个送货选项。 选项： `Yes` / `No` |
| [!UICONTROL Shortcut Buttons Flavor] | 商店视图 | 确定用于PayPal接受按钮的图像类型。 选项： <br/>**`Dynamic`**— （推荐）显示可从PayPal服务器动态更改的图像。<br/>**`Static`**  — 显示无法动态更改的静态图像。 |
| [!UICONTROL Enable PayPal Guest Checkout] | 网站 | 允许没有PayPal帐户的客户通过PayPal Express结帐进行购买。 选项： `Yes` / `No` |
| [!UICONTROL Require Customer's Billing Address] | 网站 | 确定是否要求客户帐单地址。 选项： `Yes` / `No` / `For Virtual Quotes Only` |
| [!UICONTROL Billing Agreement Signup] | 网站 | 确定客户是否能够输入 [billing agreement（计费协议）](../../stores-purchase/paypal-billing-agreements.md) 你的店里。 选项： <br/>**`Auto`**— 客户可以在快速结帐期间注册账单协议。<br/>**`Ask Customer`**  — 询问客户是否希望注册计费协议。 <br/>**`Never`**— 不向客户提供注册计费协议的选项。 |
| [!UICONTROL Skip Order Review Step] | 网站 | 确定客户是否可以从PayPal网站完成交易，或者是否需要返回您的商店并在提交订单之前完成订单审核步骤。 选项： `Yes` / `No` |

{：style=&quot;table-layout：auto&quot;}

## [!UICONTROL Billing Agreement Setting]

![帐单协议设置](./assets/payment-methods-paypal-express-checkout-billing-agreement-settings.png)<!-- zoom -->

| 字段 | 范围 | 描述 |
|--- |--- |--- |
| [!UICONTROL Enabled] | 网站 | 启用后，客户在结帐期间将看到帐单协议作为付款选项。 选项： `Yes` / `No` |
| [!UICONTROL Title] | 商店视图 | 在结账期间显示为付款选项的PayPal计费协议选项的标签。 |
| [!UICONTROL Sort Order] | 商店视图 | 确定在结账期间将计费协议与其他支付方法一起列出的顺序。 |
| [!UICONTROL Payment Action] | 网站 | 确定PayPal管理事务的方式：选项： <br/>**`Authorization`**— 批准购买，但保留资金。 该金额在商户将该金额“扣押”前不予提取。<br/>**`Sale`**  — 采购金额已获授权并立即从客户账户中提取。 |
| [!UICONTROL Payment Applicable From] | 网站 | 确定适用的国家/地区选择的范围。 选项： `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Countries Payment Applicable From] | 网站 | 标识接受付款的每个国家/地区。 只有帐单地址在选定国家/地区的客户才能使用此付款方法进行购买。 |
| [!UICONTROL Debug Mode] | 网站 | 在日志文件中记录与支付系统的通信。 选项： `Yes` / `No` <br/><br/>**_注意：_**日志文件存储在服务器上，只有开发人员才能访问。 根据PCI数据安全标准，信用卡信息不会记录在日志文件中。 |
| [!UICONTROL Enable SSL Verification] | 网站 | 启用验证步骤，确保事务通过加密的SSL通道进行。 选项： `Yes` / `No` |
| [!UICONTROL Transfer Cart Line Items] | 网站 | 启用后，会在PayPal支付页面上显示购物车中的行项目摘要。 选项： `Yes` / `No` |
| [!UICONTROL Allow in Billing Agreement Wizard] | 网站 | 启用后，客户可以从其客户帐户的仪表板启动计费协议。 |

{：style=&quot;table-layout：auto&quot;}

## [!UICONTROL Settlement Report Settings]

![结算报表设置](./assets/payment-methods-paypal-payments-advanced-settlement-report-settings.png)<!-- zoom -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Login] | 网站 | 登录PayPal安全FTP服务器所需的用户名。 |
| [!UICONTROL Password] | 网站 | 登录PayPal安全FTP服务器所需的密码。 |
| [!UICONTROL Sandbox Mode] | 网站 | 启用后，将在生产环境中“上线”之前在测试环境中运行报告。 选项： `Yes` / `No` |
| [!UICONTROL Custom Endpoint Hostname or IP-Address] | 网站 | 管理结算报表的URL。 默认值： `reports.paypal.com` |
| [!UICONTROL Custom Path] | 网站 | 结算报表在服务器上保存的路径。 默认值： `/ppreports/outgoing` |
| [!UICONTROL Scheduled Fetching] |  |  |
| [!UICONTROL Enable Automatic Fetching] | 网站 | 启用后，将按计划自动获取结算报表。 选项： `Yes` / `No` |
| [!UICONTROL Schedule] | 全局 | 确定PayPal生成结算报表的频率。 选项： `Daily` / `Every 3 days` / `Every 7 days` / `Every 10 days` / `Every 14 days` / `Every 30 days` / `Every 40 days` |
| [!UICONTROL Time of Day] | 全局 | 确定生成结算报告的小时、分钟和秒。 |

{：style=&quot;table-layout：auto&quot;}

## [!UICONTROL Frontend Experience Settings]

![前端体验设置](./assets/payment-methods-paypal-payments-advanced-frontend-experience-settings.png)<!-- zoom -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL PayPal Product Logo] | 商店视图 | 确定您商店中显示的PayPal徽标。 两种尺寸共有四种基本样式。 选项： `No Logo` / `We prefer PayPal (150 x 60)` / `We prefer PayPal (150 x 40)` / `Now accepting PayPal (150 x 60)` / `Now accepting PayPal (150 x 40)` / `Payments by PayPal (150 x 60)` / `Payments by PayPal (150 x 40)` / `Shop now using (150 x 60)` / `Shop now using (150 x 40)` |
| [!UICONTROL PayPal Merchant Pages Style] |  |  |
| [!UICONTROL Page Style] | 商店视图 | 确定PayPal商家页面的外观。 允许的值： <br/>**`paypal`**— 使用PayPal页面样式。<br/>**`primary`**  — 使用您在帐户配置文件中标识为“primary”样式的页面样式。 <br/>**`your_custom_value`**— 使用在您的帐户配置文件中指定的自定义付款页面样式。 |
| [!UICONTROL Header Image URL] | 商店视图 | 出现在签出页面左上角的图像的URL。 最大大小为750 x 90像素。 <br/><br/>**_注意：_**PayPal建议将映像存储在安全(https)服务器上。 否则，客户的浏览器可能会警告“页面包含安全和非安全项目。” |
| [!UICONTROL Header Image Background Color] | 商店视图 | 六个字符 [十六进制颜色](https://en.wikipedia.org/wiki/Web_colors) 结账页面上标题的背景颜色代码。 您可以使用大写和小写字符输入代码。 |
| [!UICONTROL Header Image Border Color] | 商店视图 | 标头周围两像素边框的六字符十六进制颜色代码。 |
| [!UICONTROL Page Background Color] | 商店视图 | 用于结账页面的背景颜色的六字符十六进制颜色代码，显示在页眉和付款表单后面。 |

{：style=&quot;table-layout：auto&quot;}

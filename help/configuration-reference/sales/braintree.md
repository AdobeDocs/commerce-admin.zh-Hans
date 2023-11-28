---
title: ’[!UICONTROL Sales] &gt； [!UICONTROL Payment Methods] &gt； [!UICONTROL Braintree]’
description: 查看的配置设置 [!UICONTROL Braintree] 部分，位于 [!UICONTROL Sales] &gt； [!UICONTROL Payment Methods] 商务管理员页面。
exl-id: cf08bc4d-8d88-45e7-af71-f1ff90023766
feature: Configuration, Payments
source-git-commit: 1f84bf9ab20aeccacf56eab396b2778140964d17
workflow-type: tm+mt
source-wordcount: '2330'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Payment Methods] > [!UICONTROL Braintree]

>[!IMPORTANT]
>
>**Commerce 2.4迁移：**<br/>
>对于2.4.0之前的Adobe Commerce和Magento Open SourceBraintree版本，建议商家从 [Commerce Marketplace](https://marketplace.magento.com/catalogsearch/result/?q=braintree) 以替换核心集成。 从2.4.0开始，该扩展现已包含在核心版本中。
><br/><br/>
>迁移到Commerce 2.4时，商家需要卸载Marketplace上分发的扩展(`paypal/module-braintree` 或 `gene/module-braintree`)并更新任何代码自定义设置，以使用 `PayPal_Braintree` 命名空间而不是 `Magento_Braintree`. 来自Commerce捆绑扩展和Commerce Marketplace上分发的扩展的配置设置会保留。 使用这些扩展版本进行的付款将正常捕获、失效或退款。
><br/><br/>
>如果您要升级到Commerce 2.4.0，并且在之前的2.3.x版本中未使用推荐的Commerce Marketplace扩展，则多地址功能在2.4.0版本的Braintree中不起作用。 当购物者选择 _交货至多个地址_ ，则不会显示Braintree支付方式。 之前推荐用于2.3.x的Commerce Marketplace扩展存在此多地址问题。

{{config}}

{{beta2-updates}}

## [!UICONTROL Basic Braintree Settings]

![基本Braintree设置](./assets/payment-methods-braintree-basic-config.png)<!-- zoom -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Title] | 商店视图 | 默认值： `Credit Card` (Braintree) |
| [!UICONTROL Environment] | 商店视图 | 选项： `Sandbox` / `Production` |
| [!UICONTROL Payment Action] | 商店视图 | 确定Braintree在处理付款时执行的操作。 选项： <br/>**`Authorize`**— 客户信用卡上的资金已获得授权，但未从帐户中转账。 将在您的商店管理员中创建订单。 您可以稍后捕获销售并创建发票。<br/>**`Intent Sale`** (以前 `Authorize and Capture` 在较早版本中) — 客户信用卡上的资金由Braintree授权和获取，并在您的商店管理员中创建订单和发票。 |
| [!UICONTROL Sandbox Merchant ID] | 商店视图 | 这是您整个沙盒网关帐户的唯一标识符。 也称为 _公共ID_ 或 _生产ID_，您的商家ID对于生产和沙盒网关而言是不同的。 此字段在以下情况下显示： _[!UICONTROL Environment]_字段设置为 `Sandbox`. |
| [!UICONTROL Sandbox Public Key] | 商店视图 | 这是用户特定的公共标识符，用于限制对加密数据的访问。 与您的沙盒Braintree网关关联的每个用户都有自己的沙盒公钥。 此字段在以下情况下显示： _[!UICONTROL Environment]_字段设置为 `Sandbox`. |
| [!UICONTROL Sandbox Private Key] | 商店视图 | 这是特定于用户的私有标识符，用于限制对加密数据的访问。 与您的沙盒Braintree网关关联的每个用户都有自己的沙盒私钥。 此字段在以下情况下显示： _[!UICONTROL Environment]_字段设置为 `Sandbox`. |
| [!UICONTROL Merchant ID] | 商店视图 | 这是您整个网关帐户的唯一标识符，包括您的网关中可能存在的多个商家帐户。 也称为 _公共ID_ 或 _生产ID_，您的商家ID对于生产和沙盒网关而言是不同的。 此字段在以下情况下显示： _[!UICONTROL Environment]_字段设置为 `Production`. |
| [!UICONTROL Public Key] | 商店视图 | 这是用户特定的公共标识符，用于限制对加密数据的访问。 与您的Braintree网关关联的每个用户都有自己的公钥。 此字段在以下情况下显示： _[!UICONTROL Environment]_字段设置为 `Production`. |
| [!UICONTROL Private Key] | 商店视图 | 这是特定于用户的私有标识符，用于限制对加密数据的访问。 与您的Braintree网关关联的每个用户都有自己的私钥。 此字段在以下情况下显示： _[!UICONTROL Environment]_字段设置为 `Production`. |
| [!UICONTROL Enable Card Payments] | 网站 | 确定Braintree信用卡付款方式是否适用于您的客户。 选项： `Yes` / `No` |
| [!UICONTROL Enable Vault for Card Payments] | 网站 | 启用后，将为客户付款信息提供安全存储，这样客户就不必在每次购买时都重新输入其信用卡信息。 选项： `Yes` / `No` |
| [!UICONTROL Enable Vault CVV Reverification] | 网站 | 启用后，将对Braintree帐户中的CVV规则设置进行验证。 选项： `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Advanced Braintree Settings]

![Braintree高级设置](./assets/payment-methods-braintree-advanced-config.png){width="550" zoomable="yes"}

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Vault Title] | 网站 | 参考的描述性标题，用于标识存储客户卡信息的存储库。 |
| [!UICONTROL Merchant Account ID] | 网站 | 要与此网站中的Braintree交易关联的商家帐户ID。 如果留空，则使用您Braintree帐户中的默认商家帐户。 |
| [!UICONTROL Skip Fraud Checks on Admin Orders] | 网站 | 阻止将事务作为的一部分发送以供评估 [!DNL Advanced Fraud Tools] 检查，仅当将设置为时，才会对通过管理员下达的订单进行检查 `Yes`.<br/>选项： `Yes` / `No` |
| [!UICONTROL Bypass Fraud Protection Threshold] | 网站 | `Advanced Fraud Protection` 当达到或超过阈值时，将绕过检查。 将此字段留空将禁用此选项。 |
| [!UICONTROL Debug] | 网站 | 确定Braintree系统和商店之间的通信是否记录在日志文件中。 选项： `Yes` / `No` |
| [!UICONTROL CVV Verification] | 网站 | 确定是否要求客户提供信用卡背面的三位数安全代码。 选项： `Yes` / `No` |
| [!UICONTROL Send Card Line Items] | 网站 | 发送所有付款方法的购物车行项目。 选项： `Yes` / `No` |
| [!UICONTROL Credit Card Types] | 网站 | 指定您接受作为通过Braintree付款的每种信用卡。 按住不放 `Ctrl` (或 `Command` (在Mac上)以选择卡片组合。 选项： `American Express` / `Visa` / `MasterCard` / `Discover` / `JCB` / `Diners` / `Maestro International` |
| [!UICONTROL Sort Order] | 网站 | 确定结帐期间Braintree与其他支付方式一起列出的顺序。 |

## [!UICONTROL Braintree Webhooks Settings]

![BraintreeWebhook设置](./assets/payment-methods-braintree-webhooks-config.png)<!-- zoom -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Enable Webhook] | 网站 | 启用webhook功能以防范欺诈、ACH支付和本地支付方法。 选项： `Yes` / `No` |
| [!UICONTROL Fraud Protection URL] | 网站 | Braintree将此URL作为 [!UICONTROL Webhook Destination URL]. **此URL必须安全且可公开访问。** |
| [!UICONTROL Fraud Protection Approve Order Status] | 网站 | 当Braintree批准欺诈防护时，选定的订单状态将分配给Commerce订单。 此状态用于更新使用ACH支付方式以及订单转入以下支付方式的订单的状态 `SETTLED` Braintree中。 |
| [!UICONTROL Fraud Protection Reject Order Status] | 网站 | 当Braintree拒绝欺诈保护时，选定的订单状态将分配给商务订单。 此状态用于更新使用ACH支付方式的订单的状态以及何时 `SETTLEMENT` 是 `DECLINED` Braintree中。 |

{style="table-layout:auto"}

## [!UICONTROL Country Specific Settings]

![特定于国家/地区的设置](./assets/payment-methods-braintree-country-specific-config.png)<!-- zoom -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Payment from Applicable Countries] | 网站 | 确定您是接受所有国家/地区的Braintree处理的付款，还是仅接受特定国家/地区的付款。 选项： `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | 网站 | 如果适用，请确定您接受Braintree处理付款的特定国家/地区。 |
| [!UICONTROL Country Specific Credit Card Types] | 网站 | 标识Braintree处理的付款按国家/地区接受的信用卡。 将为每个国家/地区保存记录。 选项： <br/>**`Country`**— 选择国家。<br/>**`Allowed Card Types`**  — 选择从国家/地区接受为通过Braintree付款的每个信用卡。 <br/>**`Add`**— 添加线路以允许使用不同国家/地区的信用卡。<br/>**`Action`**  — 删除国家/地区允许的信用卡记录。 |

{style="table-layout:auto"}

## [!UICONTROL ACH through Braintree]

![ACH通过Braintree](./assets/payment-methods-braintree-ach-config.png)<!-- zoom -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Enabled ACH Direct Debit] | 网站 | 确定 [!DNL ACH Direct Debit] 通过Braintree作为付款方式包括在内。 选项： `Yes` / `No` |
| [!UICONTROL Sort Order] | 网站 | 确定以下顺序 [!DNL ACH Direct Debit] 在结账期间与其他支付方式一起列出。 |

{style="table-layout:auto"}

## [!UICONTROL Apple Pay through Braintree]

![Apple通过Braintree支付](./assets/payment-methods-braintree-applepay-config.png)<!-- zoom -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Enable ApplePay through Braintree] | 网站 | 确定是否通过Braintree将Apple Pay作为付款方式包括在内。 选项： `Yes` / `No` <br/><br/> 域必须 [首先在Braintree帐户中验证](https://developer.paypal.com/braintree/docs/guides/apple-pay/configuration/javascript/v3). |
| [!UICONTROL Payment Action] | 网站 | 确定Braintree在处理付款时执行的操作。 选项： <br/>**`Authorize`**— 客户卡上的资金已获授权，但不会从客户帐户转账。 将在您的商店管理员中创建订单。 您可以稍后捕获销售并创建发票。<br/>**`Intent Sale`**  — 客户卡上的资金由Braintree授权和获取，并在您的商店管理员中创建订单和发票。 **_注意：_** 这是 `Authorize and Capture` （在2.3.x及更早版本中）。 |
| [!UICONTROL Merchant Name] | 商店视图 | 在ApplePay弹出窗口中向客户显示的标签。 |
| [!UICONTROL Sort Order] | 网站 | 确定在结账过程中Apple Pay与其他支付方式一起列出的顺序。 |

{style="table-layout:auto"}

## [!UICONTROL Local Payment Methods]

![本地支付方式](./assets/payment-methods-braintree-local-payment-config.png)<!-- zoom -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Enabled Local Payment Methods] | 网站 | 确定是否通过Braintree将本地付款方法作为付款方法包括在内。 选项： `Yes` / `No` |
| [!UICONTROL Title] | 网站 | 在结账支付方式部分显示的标签。 默认值： `Local Payments` |
| [!UICONTROL Allowed Payment Method] | 网站 | 选择要启用的本地付款方式。 选项： `Bancontact` / `EPS` / `giropay` / `iDeal` / `Klarna Pay Now` / `SOFORT` / `MyBank` / `P24` / `SEPA/ELV Direct Debit` （尚未支持） |
| [!UICONTROL Sort Order] | 网站 | 确定结帐期间本地支付方式与其他支付方式一起列出的顺序。 |

{style="table-layout:auto"}

>[!NOTE]
>
>捆绑的Braintree扩展不支持 [Braintree开发人员文档](https://developer.paypal.com/braintree/docs/guides/local-payment-methods/overview). 其他本地支付方法正在开发中，将在未来版本中提供支持。

## [!UICONTROL GooglePay through Braintree]

![GooglePay通过Braintree](./assets/payment-methods-braintree-googlepay-config.png)<!-- zoom -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Enabled GooglePay through Braintree] | 网站 | 确定 [!DNL Google Pay] 通过Braintree将付款作为付款方式包括在内。 选项： `Yes` / `No` |
| [!UICONTROL Payment Action] | 网站 | 确定Braintree在处理付款时执行的操作。 选项： <br/>**`Authorize`**— 客户卡上的资金已获授权，但不会从客户帐户转账。 将在您的商店管理员中创建订单。 您可以稍后捕获销售并创建发票。<br/>**`Intent Sale`**  — 客户卡上的资金由Braintree授权和获取，并在您的商店管理员中创建订单和发票。 **_注意：_** 这是 `Authorize and Capture` （在2.3.x及更早版本中）。 |
| [!UICONTROL Button Color] | 网站 | 确定 [!DNL Google Pay] 按钮。 选项： `White` / `Black` |
| [!UICONTROL Merchant ID] | 商店视图 | 必须在此处输入由Google提供的ID。 |
| [!UICONTROL Accepted Cards] | 网站 | 选择客户可用于下达订单的卡类型 [!DNL Google Pay]. |
| [!UICONTROL Sort Order] | 网站 | 确定在结账过程中Google Pay与其他支付方式一起列出的顺序。 |

{style="table-layout:auto"}

## [!UICONTROL Venmo through Braintree]

![Venmo通过Braintree](./assets/payment-methods-braintree-venmo-config.png)<!-- zoom -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Enable Venmo through Braintree] | 网站 | 确定 [!DNL Venmo] 通过Braintree作为付款方式包括在内。 选项： `Yes` / `No` |
| [!UICONTROL Payment Action] | 网站 | 确定Braintree在处理付款时执行的操作。 选项： <br/>**`Authorize`**— 客户卡上的资金已获授权，但不会从客户帐户转账。 将在您的商店管理员中创建订单。 您可以稍后捕获销售并创建发票。<br/>**`Intent Sale`**  — 客户卡上的资金由Braintree授权和获取，并在您的商店管理员中创建订单和发票。 **_注意：_** 这是  _授权和捕获_ （在2.3.x及更早版本中）。 |
| [!UICONTROL Sort Order] | 网站 | 确定在结帐期间将Venmo与其他付款方法一起列出的顺序。 |

{style="table-layout:auto"}

## [!UICONTROL PayPal through Braintree]

![通过Braintree的PayPal](./assets/payment-methods-braintree-paypal-config.png){width="550" zoomable="yes"}

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Enable PayPal through Braintree] | 网站 | 确定是否通过Braintree将PayPal作为付款方式包括在内。 选项： `Yes` / `No` |
| [!UICONTROL Enable PayPal Credit through Braintree] | 网站 | 确定是否通过Braintree将PayPal点数作为付款方式包括在内。 选项： `Yes` / `No`. 此字段在以下情况下可见： `Enable PayPal through Braintree` 设置为 `Yes` |
| [!UICONTROL Enable PayPal PayLater through Braintree] | 网站 | 确定是否通过Braintree将PayPal PayLater作为付款方式包括在内。 选项： `Yes` / `No`. 此字段在以下情况下可见： `Enable PayPal through Braintree` 设置为 `Yes` |
| [!UICONTROL Title] | 商店视图 | 在结帐期间通过Braintree给客户来标识PayPal的标签。 默认值： `PayPal` |
| [!UICONTROL Vault Enabled] | 网站 | 启用后，为客户支付信息提供安全存储，因此客户不必在每次购买时都重新输入其PayPal信息。 选项： `Yes` / `No` |
| [!UICONTROL Sort Order] | 网站 | 一个数字，用于确定PayPal在结账过程中通过Braintree时与其他支付方式一起列出的顺序。 |
| [!UICONTROL Override Merchant Name] | 商店视图 | 可用于为每个商店视图标识商家的替代名称。 |
| [!UICONTROL Payment Action] | 网站 | 确定PayPal在处理付款时通过Braintree执行的操作。 选项： <br/>**`Authorize`**— 客户卡上的资金已获授权，但不会从客户帐户转账。 将在您的商店管理员中创建订单。 您可以稍后捕获销售并创建发票。<br/>**`Authorize and Capture`**  — 客户卡上的资金由PayPal通过Braintree授权和获取，并在您的商店管理员中创建订单和发票。 |
| [!UICONTROL Payment from Applicable Countries] | 网站 | 确定您是否接受由PayPal通过所有国家/地区的Braintree处理的付款，或仅接受特定国家/地区的付款。 选项： `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | 网站 | 如果适用，请确定您接受Braintree处理付款的特定国家/地区。 |
| [!UICONTROL Require Customer's Billing Address] | 网站 | 确定是否要求客户的帐单地址来提交订单。 选项： `Yes` / `No` |
| [!UICONTROL Debug] | 网站 | 确定PayPal通过Braintree系统和您的商店之间的通信是否记录在日志文件中。 选项： `Yes` / `No` |
| [!UICONTROL Display on Shopping Cart] | 网站 | 确定PayPal按钮是否出现在 [迷你购物车](../../stores-purchase/cart-configuration.md#mini-cart) 在 [购物车](../../stores-purchase/cart.md) 页面。 选项： `Yes` / `No` |

{style="table-layout:auto"}

### [!UICONTROL Styling]

![PayPal样式](./assets/payment-methods-braintree-paypal-styling.png)<!-- zoom -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Location] | 网站 | 确定PayPal按钮和消息在店面中的呈现位置。 选项： `Mini-Cart and Cart Page` / `Checkout Page` / `Product Page` |

{style="table-layout:auto"}

**[!UICONTROL Mini-Cart and Cart Page]**

此部分中的选项和设置因 _[!UICONTROL Location]_字段。

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL PayPal Button Type] | 网站 | 将按钮设置为以下三种类型之一： `PayPal Button` / `PayPal Pay Later Button` / `PayPal Credit Button` |

**[!UICONTROL PayPal Button]**

此部分中的选项和设置因在 _[!UICONTROL PayPal Button Type]_字段。

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Show PayPal Button] | 网站 | 确定PayPal按钮在选定位置的位置。 选项： `Yes` / `No` |
| [!UICONTROL Button Label] | 网站 | 确定PayPal按钮的标签。 选项： `Paypal` / `Checkout` / `Buy Now` / `Pay` |
| [!UICONTROL Color] | 网站 | 确定PayPal按钮的颜色。 选项： `Blue` / `Black` / `Gold` / `Silver` |
| [!UICONTROL Shape] | 网站 | 确定PayPal按钮的形状。 选项： `Pill` / `Rectangle` |
| [!UICONTROL Size] | 网站 | 确定PayPal按钮的大小。 选项： `Medium` / `Large` / `Responsive` |

{style="table-layout:auto"}

**[!UICONTROL PayLater Messaging]**

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Show PayLater Messaging] | 网站 | 在选定位置启用PayLater消息传送。 选项： `Yes` / `No`. 启用后，它会显示可用优惠的PayLater消息([限制适用](https://developer.paypal.com/docs/checkout/pay-later/us/))。 |
| [!UICONTROL Message Layout] | 网站 | 确定PayLater消息布局。 选项： `Text` / `Flex` |
| [!UICONTROL Logo] | 网站 | 确定用于PayPal按钮的徽标类型。 选项： `Inline` / `Primary` / `Alternative` / `None` |
| [!UICONTROL Logo Position] | 网站 | 确定PayPal按钮的徽标位置。 选项： `Left` / `Right` / `Top` |
| [!UICONTROL Text Color] | 网站 | 确定PayPal按钮的文本颜色。 选项： `Black` / `White` / `Monochrome` / `Grayscale` |

{style="table-layout:auto"}

设置这些选项后，您可以看到PayPal按钮和PayLater消息的预览。 可以使用以下控件来应用设置或重置值：

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Apply] | 网站 | 存储按钮和PayLater消息传递的选定样式设置，并将它们应用到当前位置和当前按钮类型。 |
| [!UICONTROL Apply to All Buttons] | 网站 | 存储按钮和PayLater消息值的选定样式设置并将它们应用于所有按钮类型和位置。 |
| [!UICONTROL Reset to Recommended Defaults] | 网站 | 将样式设置返回到按钮和PayLater消息传递的推荐默认值，并将它们应用于所有按钮类型和位置。 |

{style="table-layout:auto"}

## 3d安全验证设置

![3D安全验证设置](./assets/payment-methods-braintree-3d-secure-verify-config.png)<!-- zoom -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL 3D Secure Verification] | 网站 | 确定在客户注册方案（例如）时，事务处理是否必须通过额外的验证流程 _通过VISA验证_. 选项： `Yes` / `No` |
| [!UICONTROL Always request 3DS] | 网站 | 始终针对所有事务质询3D Secure请求。 选项： `Yes` / `No` |
| [!UICONTROL Threshold Amount] | 网站 | 确定单个订单上授权处理的最大订单金额。 如果订单金额超过此阈值金额，则Braintree拒绝授权。 |
| [!UICONTROL Verify for Applicable Countries] | 网站 | 确定必须验证付款的国家/地区。 选项： `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Verify for Specific Countries] | 网站 | 如果适用，请指明必须对其进行Braintree付款验证的特定国家/地区。 |

{style="table-layout:auto"}

## [!UICONTROL Dynamic Descriptors]

![动态描述符](./assets/payment-methods-braintree-dynamic-config.png)<!-- zoom -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Name] | 商店视图 | 名称描述符分为两部分，以星号(*)分隔。 描述符的第一部分标识公司或DBA，第二部分标识产品。 例如： `company*myproduct`  <br/><br/>描述符的公司和产品部分的长度可以通过以下方式进行分配，组合长度最多为22个字符： <br/>**`Option 1`**— 公司必须包含三个字符/产品最多可包含18个字符<br/>**`Option 2`**  — 公司长度必须为7个字符/产品长度最多为14个字符 <br/>**`Option 3`**— 公司必须为12个字符/产品最多可包含9个字符 |
| [!UICONTROL Phone] | 商店视图 | 电话描述符的长度必须为10到14个字符，并且只能包含数字、破折号、圆括号和句点。 例如： `9999999999` `(999) 999-9999` `999.999.9999` |
| [!UICONTROL URL] | 商店视图 | URL描述符表示您的域名，最长可为13个字符。 例如： `company.com` |

{style="table-layout:auto"}

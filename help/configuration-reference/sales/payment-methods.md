---
title: '[!UICONTROL Sales] &amp；gt； [!UICONTROL Payment Methods]'
description: 查看Commerce管理员的[!UICONTROL Sales] &amp；gt； [!UICONTROL Payment Methods]页面上的配置设置。
exl-id: 6545b980-c8ef-460a-a884-d5315f5ad513
feature: Configuration, Payments
source-git-commit: 489c72652693a15ffe1c745277bbaa9da084dcba
workflow-type: tm+mt
source-wordcount: '1772'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Payment Methods]

>[!TIP]
>
>适用于Adobe Commerce和Magento Open Source的Payment Services提供了一个可立即投入使用的自助服务解决方案，包括沙盒测试和简单的设置，用于提供强大而安全的支付处理。 要了解有关此功能强大的工具集以及它如何为您提供insight和控制您为购买者创建最佳体验所需的更多信息，请参阅&#x200B;[_Payment Services用户指南_](https://experienceleague.adobe.com/docs/commerce/payment-services/guide-overview.html?lang=zh-Hans)。

{{config}}

## [!UICONTROL Merchant Location]

仅[!BADGE PaaS]{type=Informative url="https://experienceleague.adobe.com/zh-hans/docs/commerce/user-guides/product-solutions" tooltip="仅适用于云项目(Adobe管理的PaaS基础架构)和内部部署项目上的Adobe Commerce 。"}

![商家位置](./assets/payment-methods-merchant-location.png)<!-- zoom -->

<!-- [Merchant Location](https://experienceleague.adobe.com/zh-hans/docs/commerce-admin/start/setup/store-details#merchant-location) -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Merchant Country] | 网站 | 标识商家注册开展业务的国家/地区。 |

{style="table-layout:auto"}

## 推荐的解决方案

对于刚开始接受PayPal帐户或信用卡在线付款的商家，建议使用以下付款解决方案，以提供一种简单的方式。 随着您的业务增长，您可以将其与其他PayPal支付解决方案相结合。

- [支付服务](payment-services.md)
- 仅[!BADGE PaaS]{type=Informative url="https://experienceleague.adobe.com/zh-hans/docs/commerce/user-guides/product-solutions" tooltip="仅适用于云项目(Adobe管理的PaaS基础架构)和内部部署项目上的Adobe Commerce 。"} [PayPal Express签出](paypal-express-checkout.md)
- 仅[!BADGE PaaS]{type=Informative url="https://experienceleague.adobe.com/zh-hans/docs/commerce/user-guides/product-solutions" tooltip="仅适用于云项目(Adobe管理的PaaS基础架构)和内部部署项目上的Adobe Commerce 。"} [Braintree](braintree.md)

>[!NOTE]
>
>2.4.x版本中删除了一些支付集成和捆绑的扩展，并将其移至Commerce Marketplace。 您可以在[Commerce Marketplace](https://marketplace.magento.com/extensions/payments-security.html){:target="_blank"}中找到最新的官方付款集成扩展。
><br/>
>**Amazon Pay**&#x200B;和&#x200B;**Klarna**： Adobe Commerce和Magento Open Source版本2.4.0到2.4.3包含这些供应商开发的扩展。 从2.4.4版本开始，核心版本不再捆绑这些扩展，必须从Commerce Marketplace安装和更新这些扩展。 通过Marketplace，还可以访问扩展开发人员提供的当前文档。
><br/>
>如果已启用并配置其中任一捆绑扩展，则必须在2.4.4升级过程中更新`composer.json`文件并管理以后的扩展更新。 有关详细信息，请参阅&#x200B;_升级指南_&#x200B;中的[升级模块](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html?lang=zh-Hans)。<br/>
><br/>
>**Worldpay**、**Eway**、**CyberSource**&#x200B;和&#x200B;**Authorize.Net**：有关从这些付款集成进行安全过渡的详细信息，请参阅[DevBlog](https://community.magento.com/t5/Magento-DevBlog/Deprecation-of-Magento-core-payment-integrations/ba-p/426445){:target="_blank"}。

## 其他PayPal方法

仅[!BADGE PaaS]{type=Informative url="https://experienceleague.adobe.com/zh-hans/docs/commerce/user-guides/product-solutions" tooltip="仅适用于云项目(Adobe管理的PaaS基础架构)和内部部署项目上的Adobe Commerce 。"}

PayPal提供各种支付解决方案，可满足各种规模的企业以及世界各地从事商业活动的企业的需求。 PayPal让您能够接受所有主要借记卡和信用卡的付款。 PayPal提供了额外的便利性，无需额外付费，因为即使没有PayPal账户的客户也可以使用PayPal支付购买费用。

### PayPal多功能一体机方法

仅[!BADGE PaaS]{type=Informative url="https://experienceleague.adobe.com/zh-hans/docs/commerce/user-guides/product-solutions" tooltip="仅适用于云项目(Adobe管理的PaaS基础架构)和内部部署项目上的Adobe Commerce 。"}

- [PayPal支付高级](paypal-payments-advanced.md)
- [PayPal Payments Pro](paypal-payments-pro.md)
- [PayPal支付标准](paypal-payments-standard.md)

### PayPal支付网关

仅[!BADGE PaaS]{type=Informative url="https://experienceleague.adobe.com/zh-hans/docs/commerce/user-guides/product-solutions" tooltip="仅适用于云项目(Adobe管理的PaaS基础架构)和内部部署项目上的Adobe Commerce 。"}

- [PayPal Payflow Pro](paypal-payflow-pro.md)（包括快速结帐）
- [PayPal Payflow链接](paypal-payflow-link.md)（包括快速结帐）

## 基本支付方式

Commerce内置以下支付方法，不使用第三方支付提供商处理交易。 许多基本支付方式是离线管理，而不是在线管理。

### [!UICONTROL Check / Money Order]

![支票/汇票](./assets/payment-methods-check-money-order.png)<!-- zoom -->

<!-- [Check / Money Order](https://experienceleague.adobe.com/zh-hans/docs/commerce-admin/stores-sales/payments/offline/check-money-order) -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Enabled] | 网站 | 确定客户是否可以通过支票或汇票付款。 选项： `Yes` / `No` |
| [!UICONTROL Title] | 商店视图 | 客户在结帐时看到的此付款方法的名称。 |
| [!UICONTROL New Order Status] | 网站 | 确定分配给支票或汇票所付订单的初始[订单状态](../../stores-purchase/order-status.md)。 默认值： `Pending` |
| [!UICONTROL Payment from Applicable Countries] | 网站 | 确定您接受支票或汇票付款的国家/地区。 选项： `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | 网站 | 标识您接受支票或汇票付款的特定国家/地区。 |
| [!UICONTROL Make Check Payable to] | 商店视图 | 应向其支付支票和汇票的实体的名称。 |
| [!UICONTROL Send Check to] | 商店视图 | 应发送支票和汇票的街道地址或邮政信箱。 |
| [!UICONTROL Minimum Order Total] | 网站 | 可以通过支票或汇票支付的最小订单金额。 |
| [!UICONTROL Maximum Order Total] | 网站 | 可以通过支票或汇票支付的最大订单金额。 <br/><br/>**_注意：_**&#x200B;如果订单总计在最小或最大订单总计之间，或者与最小或最大订单总计匹配，则订单符合条件。 |
| [!UICONTROL Sort Order] | 网站 | 在结账过程中与其他支付方式一起列出时，将按支票或汇票确定支付顺序的编号。 输入`0`以将其放在列表顶部。 |

{style="table-layout:auto"}

### [!UICONTROL Bank Transfer Payment]

![银行转帐付款](./assets/payment-methods-bank-transfer-payment.png)<!-- zoom -->

<!-- [Bank Transfer Payment](https://experienceleague.adobe.com/zh-hans/docs/commerce-admin/stores-sales/payments/offline/bank-transfer) -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Enabled] | 网站 | 确定客户是否可以通过将付款从其银行直接转移到您的商家帐户来进行支付。 选项： `Yes` / `No` |
| [!UICONTROL Title] | 商店视图 | 客户在结帐时看到的此付款方法的名称。 |
| [!UICONTROL New Order Status] | 网站 | 确定分配给银行转帐支付的订单的初始订单状态。 默认值： `Pending` |
| [!UICONTROL Payment from Applicable Countries] | 网站 | 确定接受银行转帐付款的国家/地区。 选项： `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | 网站 | 标识接受银行转帐付款的特定国家/地区。 |
| [!UICONTROL Minimum Order Total] | 网站 | 银行转帐可支付的最小订单金额。 |
| [!UICONTROL Maximum Order Total] | 网站 | 银行转帐可以支付的最大订单金额。 <br/><br/>**_注意：_**&#x200B;如果订单总计在最小或最大订单总计之间，或者与最小或最大订单总计匹配，则订单符合条件。 |
| [!UICONTROL Sort Order] | 网站 | 在结帐期间与其他支付方式一起列出时，确定按银行转帐支付的订单的编号。 输入`0`以将其放在列表顶部。 |

{style="table-layout:auto"}

### [!UICONTROL Payment on Account]

{{b2b-feature}}

![帐户付款](./assets/payment-methods-payment-on-account.png)<!-- zoom -->

<!-- [Payment on Account](https://experienceleague.adobe.com/zh-hans/docs/commerce-admin/b2b/enable-basic-features#configure-payment-on-account) -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Enabled] | 网站 | 确定公司是否可以使用公司信用进行购买。 选项： `Yes` / `No` |
| [!UICONTROL Title] | 商店视图 | 客户在结帐时看到的此付款方法的名称。 |
| [!UICONTROL New Order Status] | 网站 | 确定计入公司帐户的新订单的状态。 选项： `Pending (default)` / `Processing` / `Suspected Fraud` |
| [!UICONTROL Payment from Applicable Countries] | 网站 | 确定允许公司将购买费用计入其帐户的国家/地区。 选项： `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | 网站 | 确定公司可以将购买费用计入其帐户的特定国家/地区。 |
| [!UICONTROL Minimum Order Total] | 网站 | 指定可从公司帐户中扣除的最小订单金额。 |
| [!UICONTROL Maximum Order Total] | 网站 | 可从公司帐户中扣除的最大订单金额。 <br/><br/>**_注意：_**&#x200B;如果订单总计在最小或最大订单总计之间，或者与最小或最大订单总计匹配，则订单符合条件。 |
| [!UICONTROL Sort Order] | 网站 | 一个数字，它确定在结账过程中与其他支付方式一起列出时显示的分期付款订单。 输入`0`以将其放在列表顶部。 |

{style="table-layout:auto"}

>[!NOTE]
>
>具有[多个送货地址](../../stores-purchase/shipping-settings.md#multiple-addresses)的订单不支持帐户付款，并且未出现在付款选项中。

### [!UICONTROL Cash On Delivery Payment]

![货到付款](./assets/payment-methods-cash-on-delivery-payment.png)<!-- zoom -->

<!-- [Cash On Delivery Payment](../../stores-purchase/cash-on-delivery.html) -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Enabled] | 网站 | 确定客户是否可以通过将付款从其银行直接转移到您的商家帐户来进行支付。 选项： `Yes` / `No` |
| [!UICONTROL Title] | 商店视图 | 客户在结帐时看到的此付款方法的名称。 |
| [!UICONTROL New Order Status] | 网站 | 确定分配给银行转帐支付的订单的初始订单状态。 默认值： `Pending` |
| [!UICONTROL Payment from Applicable Countries] | 网站 | 确定接受银行转帐付款的国家/地区。 选项： `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | 网站 | 标识接受银行转帐付款的特定国家/地区。 |
| [!UICONTROL Minimum Order Total] | 网站 | 指定银行转帐可支付的最小订单金额。 |
| [!UICONTROL Maximum Order Total] | 网站 | 银行转帐可以支付的最大订单金额。 <br/><br/>**_注意：_**&#x200B;如果订单总计在最小或最大订单总计之间，或者与最小或最大订单总计匹配，则订单符合条件。 |
| [!UICONTROL Sort Order] | 网站 | 在结帐期间与其他支付方式一起列出时，确定按银行转帐支付的订单的编号。 输入`0`以将其放在列表顶部。 |

{style="table-layout:auto"}

### [!UICONTROL Zero Subtotal Checkout]

![零小计签出](./assets/payment-methods-zero-subtotal-checkout.png)<!-- zoom -->

<!-- [Zero Subtotal Checkout](../../stores-purchase/zero-subtotal-checkout.html) -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Title] | 商店视图 | 结帐期间用于此付款方法的名称。 默认值：无需付款信息 |
| [!UICONTROL Enabled] | 网站 | 确定零小计签出是否可供商店管理员管理小计为零的订单（例如已征税的订单），但折扣已将金额减少为零。 选项： `Yes` / `No` |
| [!UICONTROL New Order Status] | 网站 | 确定分配给订单的初始订单状态，这些订单已处理为“零小计结帐”。 默认值： `Pending` |
| [!UICONTROL Payment from Applicable Countries] | 网站 | 确定可以应用零小计结帐的国家/地区。 选项： `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | 网站 | 标识可以对其应用零小计结账的特定国家/地区。 |
| [!UICONTROL Sort Order] | 网站 | 在结账过程中与其他支付方式一起列出时，将会显示一个数字，用于决定标题（如“无需支付信息”）的顺序。 输入`0`以将其放在列表顶部。 |

{style="table-layout:auto"}

## [!UICONTROL Payment actions]

仅[!BADGE PaaS]{type=Informative url="https://experienceleague.adobe.com/zh-hans/docs/commerce/user-guides/product-solutions" tooltip="仅适用于云项目(Adobe管理的PaaS基础架构)和内部部署项目上的Adobe Commerce 。"}

付款操作是按付款方式&#x200B;_配置的_。 付款活动确定获取资金的时间以及为销售订单创建发票的时间。

有关各个配置选项的完整列表，请参阅每个单独支付方式主题的基本设置部分。

| 付款操作 | 描述 |
|--- |---|
| [!UICONTROL Authorization] | 批准购买，但保留资金。 该金额在商户缴获前不会提取。 |
| [!UICONTROL Authorize] | 授权订单总额的采购员帐户，但不获取付款。 通过创建发票来获取付款。 授权订单可以失效或取消。 |
| [!UICONTROL Authorize and Capture] | 为订单总额授权采购员帐户并获取付款。 系统会自动创建发票。 您可以通过贷项通知单退回捕获的资金。 一旦获取了付款，您就无法取消订单。 |
| [!UICONTROL Charge on shipment] | 在Commerce中创建发票时，Amazon会收到捕获请求并向客户收取费用。 |
| [!UICONTROL Charge on order] | Amazon将创建发票，并在下订单时向客户收费。 |
| [!UICONTROL Not Capture] | 提交发票时，系统不会捕获付款。 假定您稍后通过Commerce获取付款。 完成的发票中有一个“捕获”按钮。 在捕获之前，您可以取消发票。 捕获后，您可以创建贷项通知单并撤消发票。 |
| [!UICONTROL Order] | 表示与PayPal签署的协议，该协议允许商家在定义的时间段（最多29天）内，从客户的买方帐户中获取一个或多个最高达订单总金额的金额。 |
| [!UICONTROL Sale] | 采购金额已获授权并立即从客户帐户中提取。 |

{style="table-layout:auto"}

>[!NOTE]
>
>请勿选择&#x200B;_[!UICONTROL Not Capture]_&#x200B;选项，除非您确定稍后将通过Commerce捕获付款。 在使用“捕获”按钮捕获付款之前，您无法创建贷项通知单。

## [!UICONTROL Purchase Order]

![采购订单](./assets/payment-methods-purchase-order.png)<!-- zoom -->

<!-- [Purchase Order](../../stores-purchase/purchase-order.html) -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Enabled] | 网站 | 确定客户是否可以按采购订单(PO)付款。 选项： `Yes` / `No` |
| [!UICONTROL Title] | 商店视图 | 在结帐期间向客户显示的此付款方法的名称。 |
| [!UICONTROL New Order Status] | 网站 | 确定分配给订单支付的初始[订单状态](../../stores-purchase/order-status.md)。 默认值：挂起 |
| [!UICONTROL Payment from Applicable Countries] | 网站 | 确定接受PO付款的国家/地区。 选项： `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | 网站 | 确定您接受PO付款的特定国家/地区。 |
| [!UICONTROL Minimum Order Total] | 网站 | PO可以支付的最小订单金额。 |
| [!UICONTROL Maximum Order Total] | 网站 | PO可以支付的最大订单金额。 <br/><br/>**_注意：_**&#x200B;如果订单总计在最小或最大订单总计之间，或者与最小或最大订单总计匹配，则订单符合条件。 |
| [!UICONTROL Sort Order] | 网站 | 在结帐期间与其他付款方法一起列出时，确定按PO付款的订单的编号。 输入`0`以将其放在列表顶部。 |

{style="table-layout:auto"}

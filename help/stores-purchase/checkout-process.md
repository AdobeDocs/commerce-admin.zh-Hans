---
title: 结账流程和选项
description: 了解Adobe Commerce和Magento Open Source结帐流程如何收集完成交易所需的信息，以及“结帐”页面如何引导客户完成流程的每个步骤。
exl-id: f503643b-a0bb-4763-9831-d592afb2c323
feature: Checkout
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '1097'
ht-degree: 0%

---

# 结账流程和选项

当结账过程开始时，交易转移到安全、加密的渠道。 挂锁符号显示在浏览器的地址栏中，并且URL会从 `http` 到 `https`.

## 进程

结帐流程的目标是收集完成事务处理所需的信息。 此 _结帐_ 页面将引导客户完成此流程的每个步骤。 登录到其帐户的客户可以快速完成结帐，因为许多信息都已在他们的帐户中。 与使用采购订单的公司帐户关联的客户的工作流略有不同。

### 配送

结账流程的第一步是让客户填写送货地址信息，并选择送货方式。 如果客户有帐户，则系统会自动输入送货地址，但如有需要，可以更改送货地址。

![Adobe Commerce](../assets/adobe-logo.svg) (仅限Adobe Commerce)收件人和发件人的街道地址格式由 [客户地址属性](../customers/address-attributes.md). 输入验证设置确定可在送货地址中使用的有效字符。

结帐流程的每个步骤均在页面顶部的进度栏后面显示，“订单摘要”会显示目前输入的信息。

![结账过程中的送货页面](./assets/storefront-checkout-step1-shipping.png){width="600" zoomable="yes"}

#### 发送到其他地址

1. 如果通讯簿中有附加条目，客户将查找要发运订单的地址。

1. 要选择地址，请单击 **[!UICONTROL Ship Here]**.

#### 添加地址

1. 在底部 _[!UICONTROL Shipping Address]_部分，客户点击&#x200B;**[!UICONTROL + New Address]**.

1. 完成 _[!UICONTROL Shipping Address]_表单。

   默认情况下，客户的名字和姓氏最初显示在表单中。

   ![“送货地址”表单包含姓名和地址信息](./assets/storefront-checkout-step1-shipping-add-new-address.png){width="600" zoomable="yes"}

1. 要将新地址保存在通讯簿中，客户将选中表单底部的复选框。

1. 点击次数 **[!UICONTROL Save Address]**.

   新地址现在被选为送货地址。

   ![系统会自动在送货页面中选择保存的地址](./assets/storefront-checkout-step1-shipping-new-address-selected.png){width="600" zoomable="yes"}

#### 选择配送方式

1. 在列表中 [配送](delivery.md) 方法，客户会选择想要使用的选项。

   ![配送页显示配送方式选项](./assets/storefront-checkout-step1-shipping-methods.png){width="600" zoomable="yes"}

1. 点击次数 **[!UICONTROL Next]** 以继续。

### 复查和付款 — 正常订单

在结账流程的第二步中，客户选择 [支付方式](payments.md)，并将带有促销代码的任何优惠券应用于购买。 所有信息都可以进行审核和编辑（如果需要）。 如果启用，客户必须在下订单前同意销售条款和条件。

>[!NOTE]
>
>虽然Commerce允许配置多个优惠券代码，但客户只能将一个优惠券代码应用于购物车。 (请参阅 [优惠券代码](../merchandising-promotions/price-rules-cart-coupon.md) 以了解更多信息。)

![结账时复查和支付页面](./assets/storefront-checkout-step2-payment-review.png){width="700" zoomable="yes"}

### 复查和付款 — 采购订单

![Adobe Commerce B2B](../assets/b2b.svg) (仅适用于Adobe Commerce B2B)

当客户与已启用此功能的公司关联时 [采购订单](../b2b/purchase-order-flow.md)，则所有订单都将作为采购订单处理。 可用的支付方式由公司帐户设置决定。

1. 客户选择付款方式。

   使用时 _分期付款_ 方法， [!UICONTROL Custom Reference Number] 字段可用于引用发票编号。

1. 客户点击 **[!UICONTROL Place Purchase Order]**.

   已下达采购订单。

如果公司已设置 [审批规则](../b2b/account-dashboard-approval-rules.md)，则采购订单将经过审批流程。 否则，将立即处理它。

![采购订单审核和付款](./assets/checkout-storefront-step2-b2b.png){width="700" zoomable="yes"}

### 订单汇总中显示的项目数

管理员用户可以在结账时更改订单摘要中显示的最大项目数，以简化产品的显示。 默认情况下，此值设置为10。

![在订单汇总中显示的项目数](./assets/order-summary.png){width="700" zoomable="yes"}

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中，展开 **[!UICONTROL Sales]** 并选择 **[!UICONTROL Checkout]**.

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Checkout Options]** 部分。

1. 对象 **[!UICONTROL Maximum Number of Items to Display in Order Summary]**，输入要显示的最大项目数。

1. 单击 **[!UICONTROL Save Config]**.

   通过此更新，结帐期间显示的订单汇总将限制为指定的物料数量。

### 订单确认

订单确认会在下单后显示。 对于已注册的客户，该页面包括订单编号，该编号带有指向客户帐户的链接，以及用于生成收据的链接。 注册客户将收到通过电子邮件发送的订单确认和跟踪信息。 我们鼓励来宾创建帐户来跟踪订单。 注册客户可以通过单击链接来生成收据。

订单确认页面也称为 _成功_ 页面，Analytics程序使用它来跟踪转化。

![“订单确认”页显示成功消息和订单编号](./assets/storefront-checkout-confirmation-customer.png){width="700" zoomable="yes"}

## 签出选项

签出选项控制签出页面的各种属性，包括布局。 您可以配置一些选项来限制结帐，包括允许访客结帐以及强制实施条款和条件协议。 此外，还有用于在结账过程中控制信息显示的选项。

![配置 — 签出选项](./assets/checkout-checkout-options.png){width="700" zoomable="yes"}

有关每个配置设置的详细说明，请参阅 [签出选项](../configuration-reference/sales/checkout.md#checkout-options) 在 _配置参考指南_.

### 更改签出选项

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.
1. 在左侧面板上，展开 **[!UICONTROL Sales]** 并选择 **[!UICONTROL Checkout]**.
1. 根据需要设置以下任一选项。
1. 单击 **[!UICONTROL Save Config]**.

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Checkout Options]** 部分。

1. 如果设置适用于特定的商店视图， [选择商店视图](../configuration-reference/scope-change.md#set-the-scope) 配置适用的位置。

   出现提示时，单击 **[!UICONTROL OK]** 以继续。

1. 设置签出选项。

1. 单击 **[!UICONTROL Save Config]**.

### 可用的签出选项

| 字段 | [范围](../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Enable Onepage Checkout] | 商店视图 | 确定 [单页签出](checkout-one-page.md) 是默认的签出格式。 选项：是/否 |
| [!UICONTROL Allow Guest Checkout] | 商店视图 | 确定来宾是否可以通过 [不注册即签出](checkout-guest.md) 以取得你商店的帐户。 选项： `Yes` / `No` |
| [!UICONTROL Enable Terms and Conditions] | 商店视图 | 确定是否要求客户同意 [条款和条件](terms-and-conditions.md) 购买前完成销售。 选项： `Yes` / `No` |
| [!UICONTROL Display Billing Address On] | 商店视图 | 确定结帐时帐单地址的位置。 选项： `Payment Method` / `Payment Page` |
| [!UICONTROL Maximum Number of Items to Display in Order Summary] | 商店视图 | 确定结帐期间可在“订单摘要”中显示的最大项目数。 默认为 `10`. |
| [!UICONTROL Enable Address Search] | 网站 | ![Adobe Commerce](../assets/adobe-logo.svg) (仅限Adobe Commerce)确定客户是否可以使用 [地址搜索](checkout-address-search.md) 功能 _配送_，和 _审核与支付_ 步骤。 启用此函数后，使用 _[!UICONTROL Number of Customer Addresses Limit]_设置签出期间激活此功能所需的已保存地址数。 选项： `Yes` / `No` |
| [!UICONTROL Number of Customer Addresses Limit] | 网站 | ![Adobe Commerce](../assets/adobe-logo.svg) (仅限Adobe Commerce)当地址搜索为 **[!UICONTROL Enabled]**，确定在签出期间激活此功能所需的已保存地址数。 当客户的已保存地址数达到或超过此数量时，只有默认地址会呈现在 _配送_ 和 _审核与支付_ 步骤。 客户可以使用搜索功能更改所选地址。 默认值为10。 |

{style="table-layout:auto"}

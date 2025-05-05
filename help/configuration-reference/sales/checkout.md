---
title: '[!UICONTROL Sales] &amp；gt； [!UICONTROL Checkout]'
description: 查看Commerce管理员的[!UICONTROL Sales] &amp；gt； [!UICONTROL Checkout]页面上的配置设置。
exl-id: a912beb0-37a9-407b-83bd-dc6cd0554dc4
feature: Configuration, Checkout
source-git-commit: 5a4417373f6dc720e8e14f883c27348a475ec255
workflow-type: tm+mt
source-wordcount: '646'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Checkout]

{{config}}

## [!UICONTROL Checkout Options]

![签出选项](./assets/checkout-checkout-options.png)<!-- zoom -->

<!--[Checkout Options](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/point-of-purchase/checkout/checkout-process#checkout-options) -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|------------------------------------------------------------------|--- |----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable Guest Checkout Login] | 商店视图 | 启用此设置以允许未经身份验证的用户（店面和API）查询电子邮件地址是否已与客户帐户关联。 如果输入的电子邮件地址已注册到客户帐户，则可以使用此功能增强来宾的签出工作流，方法是显示登录提示，但代价是向未经身份验证的用户公开信息。  选项： `Yes` / `No` |
| [!UICONTROL Enable Onepage Checkout] | 商店视图 | 确定[单页签出](../../stores-purchase/checkout-process.md#checkout-options)是否为默认签出格式。 选项： `Yes` / `No` |
| [!UICONTROL Allow Guest Checkout] | 商店视图 | 确定访客是否可以在未向应用商店注册[&#128279;](../../stores-purchase/checkout-guest.md)帐户的情况下进行签出。 选项： `Yes` / `No` |
| [!UICONTROL Enable Terms and Conditions] | 商店视图 | 确定客户在购买之前是否需要同意销售的[条款和条件](../../stores-purchase/terms-and-conditions.md)。 选项： `Yes` / `No` |
| [!UICONTROL Display Billing Address On] | 商店视图 | 确定结帐时帐单地址的位置。 选项： `Payment Method` / `Payment Page` |
| [!UICONTROL Maximum Number of Items to Display in Order Summary] | 商店视图 | 确定结帐期间可在&#x200B;_订单摘要_&#x200B;中显示的最大项目数。 默认值为`10`。 |
| [!UICONTROL Enable Address Search] | 网站 | ![Adobe Commerce](../../assets/adobe-logo.svg)(仅限Adobe Commerce)确定客户是否可以将[地址搜索](../../stores-purchase/checkout-address-search.md)功能用于送货以及查看和付款步骤。 启用此功能后，请使用“客户地址数限制”来设置结账期间激活此功能所需的已保存地址数。 选项： `Yes` / `No` |
| 客户地址数限制 | 网站 | ![Adobe Commerce](../../assets/adobe-logo.svg)(仅限Adobe Commerce)启用地址搜索后，将确定在签出期间激活此功能所需的已保存地址数。 当客户的已保存地址数达到或超过该数字时，将在&#x200B;_送货_&#x200B;和&#x200B;_审核和付款_&#x200B;步骤中仅呈现默认地址。 客户可以使用搜索功能更改所选地址。 默认值为`10`。 |

{style="table-layout:auto"}

## [!UICONTROL Shopping Cart]

![购物车](./assets/checkout-shopping-cart.png)<!-- zoom -->

<!--[Shopping Cart](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/point-of-purchase/cart/cart-configuration) -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Quote Lifetime (days)] | 网站 | 确定报价价格[&#128279;](../../stores-purchase/cart-configuration.md#quote-lifetime)的生命周期（以天为单位）。 |
| [!UICONTROL After Adding a Product Redirect to Shopping Cart] | 商店视图 | 确定将产品添加到购物车后是否立即显示[购物车页面](../../stores-purchase/cart-configuration.md#redirect-to-cart)。 选项： `Yes` / `No` |
| [!UICONTROL Number of Items to Display Pager] | 商店视图 | 确定在触发寻呼机之前购物车中的项目数。 默认值： `20` |
| [!UICONTROL Show Cross-sell Items in the Shopping Cart] | 商店视图 | 指示购物车中是否显示[交叉销售项目](../../catalog/related-products-up-sells-cross-sells.md#cross-sells)，从而为客户提供额外的销售选项。 选项： `Yes` （默认） / `No` |
| [!UICONTROL Grouped Product Image] | 商店视图 | 确定为购物车中分组的[产品](../../catalog/product-create-grouped.md)显示的[缩略图](../../stores-purchase/cart-configuration.md#cart-thumbnails)图像。 选项： `Product Thumbnail Itself` / `Parent Product Thumbnail` |
| [!UICONTROL Configurable Product Image] | 商店视图 | 确定为购物车中的可配置产品显示的[缩略图](../../stores-purchase/cart-configuration.md#cart-thumbnails)图像。 选项： `Product Thumbnail Itself` / `Parent Product Thumbnail` |
| [!UICONTROL Preview Quote Lifetime (minutes)] | 商店视图 | 确定从购物车中预览报价时报价的最大保留时间（以分钟为单位）。 |
| [!UICONTROL Enable Clear Shopping Cart] | 网站 | 确定购物车是否会在单次操作中为用户显示用于清除购物车内容的选项。 选项： `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL My Cart Link]

![我的购物车链接](./assets/checkout-my-cart-link.png)<!-- zoom -->

<!-- [*My Cart Link*](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/point-of-purchase/cart/cart-configuration#mini-cart) -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Display Cart Summary] | 网站 | 确定“我的购物车”链接后括号中显示的值。 选项： `Display number of items in cart` / `Display item quantities` |

{style="table-layout:auto"}

## 迷你购物车

![迷你购物车](./assets/checkout-mini-cart.png)<!-- zoom -->

<!-- [*Mini Cart*](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/point-of-purchase/cart/cart-configuration#mini-cart) -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Display Mini Cart] | 商店视图 | 确定在单击标题中的购物车图标时，迷你购物车是否显示在商店页面上。 迷你购物车的显示取决于主题。 选项： `Yes` / `No` |
| [!UICONTROL Number of Items to Display Scrollbar] | 商店视图 | 确定在触发滚动条之前可在迷你购物车中显示的项目数。 默认： `5` |
| [!UICONTROL Maximum Number of Items to Display] | 商店视图 | 确定迷你购物车中可以显示的项目的最大数量。 默认： `10` |

{style="table-layout:auto"}

## [!UICONTROL Payment Failed Emails]

![付款失败的电子邮件](./assets/checkout-payment-failed-emails.png)<!-- zoom -->

<!-- [*Payment Failed Emails*](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/point-of-purchase/checkout/checkout-payment-failed-emails) -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Payment Failed Email Receiver] | 商店视图 | 标识接收“付款失败”电子邮件的商店联系人。 默认接收器： `General Contact` |
| [!UICONTROL Payment Failed Email Sender] | 商店视图 | 标识显示为“付款失败”电子邮件消息发送者的商店联系人。 默认发件人： `General Contact` |
| [!UICONTROL Payment Failed Template] | 商店视图 | 标识用于支付失败的电子邮件的模板。 默认模板： `Payment Failed` |
| [!UICONTROL Send Payment Failed Copy To] | 商店视图 | 提供接收付款失败电子邮件副本的任何人的电子邮件地址。 用逗号分隔多个地址。 |
| [!UICONTROL Send Payment Failed Copy Method] | 商店视图 | 指示用于发送副本的电子邮件方法。 选项： <br />**`Bcc`**— 通过在发送给客户的同一电子邮件的标头中包含收件人来发送礼貌性密件。 客户看不到密件抄送收件人。<br />**`Separate Email`** — 将副本作为单独的电子邮件发送。 |

{style="table-layout:auto"}

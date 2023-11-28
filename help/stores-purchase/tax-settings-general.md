---
title: 税务配置设置
description: 了解如何配置基本税设置，包括税种、计算和默认纳税目标。
exl-id: e32747f9-20d0-4717-9cee-aa1bcffebb65
feature: Taxes
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '1052'
ht-degree: 0%

---

# 税务配置设置

以下说明将指导您完成Commerce实例的基本税务配置。 在设置您的税务之前，请确保您熟悉 [区域设置](store-localize.md#step-3-change-the-locale-of-the-store-view). 然后，根据您的要求完成税务配置。

管理员 [权限](../systems/permissions.md) 可以设置为限制 [访问](../systems/permissions-user-roles.md) 以税收资源，基于业务 _需要知道_. 要创建有权访问税设置的管理员角色，请选择销售/税和系统/税资源。 如果为不同于默认发运原点的区域设置网站，则还必须允许角色访问系统/发运资源。 配送设置确定用于目录价格的商店税率。

## 配置常规税务设置

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 对于多站点配置，设置 **[!UICONTROL Store View]** 到作为配置目标的网站和商店。

1. 在左侧面板中，展开 **[!UICONTROL Sales]** 并选择 **[!UICONTROL Tax]**.

1. 完成以下配置设置。

   如有必要，请清除 **[!UICONTROL Use system value]** 任何灰显设置的复选框。

### [!UICONTROL Tax Classes]

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Tax Classes]** 部分。

   ![税分类](../configuration-reference/sales/assets/tax-tax-classes.png){width="600" zoomable="yes"}

   - **用于装运的税类**  — 设置为相应的类。 默认类为： `None` 和 `Taxable Goods`
   - **赠品选项的税分类** — ![Adobe Commerce](../assets/adobe-logo.svg) (仅限Adobe Commerce)设置为相应的类。 默认类为： `None` 和 `Taxable Goods`
   - **产品的默认税分类**  — 设置为相应的类。 默认类为： `None` 和 `Taxable Goods`
   - **客户的默认税分类**  — 设置为相应的类。 默认类为： `Retail Customer` 和 `Wholesale Customer`

1. 完成后，单击 **[!UICONTROL Save Config]**.

### [!UICONTROL Calculation Settings]

1. 展开 **[!UICONTROL Calculation Settings]** 部分。

   ![计算设置](../configuration-reference/sales/assets/tax-calculation-settings.png){width="600" zoomable="yes"}

1. 设置 **[!UICONTROL Tax Calculation Method Based On]** 更改为以下任一项：

   - `Unit Price`  — 每个产品的价格
   - `Row Total`  — 订单中行项目的合计，减去折扣
   - `Total`  — 订单总计

1. 设置 **[!UICONTROL Tax Calculation Based On]** 更改为以下任一项：

   - `Shipping Address`  — 要发运订单的地址
   - `Billing Address`  — 客户或公司的帐单地址
   - `Shipping Origin`  — 指定为 [原点](shipping-settings.md#point-of-origin) （适用于您的商店）

1. 设置 **[!UICONTROL Catalog Prices]** 到 `Excluding Tax` 或 `Including Tax`.

1. 设置 **[!UICONTROL Shipping Prices]** 到 `Excluding Tax` 或 `Including Tax`.

1. 设置 **[!UICONTROL Apply Customer Tax]** 下列其中一项厘定税项是否适用于原价或贴现价： `After Discount` 或 `Before Discount`

1. 设置 **[!UICONTROL Apply Discount on Prices]** ，以确定折扣是否包括税或不包括税： `Excluding Tax` 或 `Including Tax`

1. 设置 **[!UICONTROL Apply Tax On]** 到 `Custom price if available` 或 `Original price only`.

1. 设置 **[!UICONTROL Enable Cross-Border Trade]** 更改为以下任一项：

   - `Yes`  — 在不同税率间使用一致的定价。 如果目录价格包含税，则选择此设置将固定价格，而不考虑客户的税率。
   - `No`  — 按税率更改价格。

   >[!IMPORTANT]
   >
   >如果 [跨境贸易](#cross-border-price-consistency) 启用时，利润率会按税率变化。 利润由公式(`Revenue - CustomerVAT - CostOfGoodsSold`)。 要促进跨境贸易，必须将价格设为含税。

### [!UICONTROL Default Tax Destination Calculation]

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Default Tax Destination Calculation]** 部分。

   ![默认纳税目标计算](../configuration-reference/sales/assets/tax-default-tax-destination-calculation.png){width="600" zoomable="yes"}

1. 指定 **[!UICONTROL Default Country]** 用于计税。

1. 如果适用，请指定 **[!UICONTROL Default State]** 用于计税。

1. 如果适用，请指定 **[!UICONTROL Default Post Code]** 用于计税。

1. 完成后，单击 **[!UICONTROL Save Config]**.

### [!UICONTROL Price Display Settings]

>[!IMPORTANT]
>
>某些与价格显示相关的设置组合（包括和排除税）可能会让客户感到困惑。 要避免触发警告消息，请参阅 [推荐的设置](taxes.md#warning-messages).

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Price Display Settings]** 部分。

   ![价格显示设置](../configuration-reference/sales/assets/tax-price-display-settings.png){width="600" zoomable="yes"}

1. 设置 **[!UICONTROL Display Product Prices in Catalog]** 更改为以下任一项：

   - `Excluding Tax`  — 店面中显示的目录价格不含税。
   - `Including Tax`  — 仅当税则与税源匹配，或者客户地址与税则匹配时，店面中的目录价格才包括税。 客户在购物车中创建帐户、登录或使用估算税和送货工具后，可能会发生此情况。
   - `Including and Excluding Tax`  — 在店面中显示的目录价格在含税和不含税的情况下均显示。

1. 设置 **[!UICONTROL Display Shipping Prices]** 到 `Excluding Tax`， `Including Tax`，或 `Including and Excluding Tax`.

1. 完成后，单击 **[!UICONTROL Save Config]**.

### [!UICONTROL Shopping Cart Display Settings]

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Shopping Cart Display Settings]** 部分。

   ![购物车显示设置](../configuration-reference/sales/assets/tax-shopping-cart-display-settings.png){width="600" zoomable="yes"}

1. 对于以下每个设置，根据您的商店和区域设置要求，选择您希望税和价格在购物车中的显示方式：

   - 设置 **[!UICONTROL Display Prices]** 到 `Excluding Tax`， `Including Tax`，或 `Including and Excluding Tax`.

   - 设置 **[!UICONTROL Display Subtotal]** 到 `Excluding Tax`， `Including Tax`，或 `Including and Excluding Tax`.

   - 设置 **[!UICONTROL Display Shipping Amount]** 到 `Excluding Tax`， `Including Tax`，或 `Including and Excluding Tax`.

   - ![Adobe Commerce](../assets/adobe-logo.svg) (仅限Adobe Commerce)设置 **[!UICONTROL Display Gift Wrapping Prices]** 到 `Excluding Tax`， `Including Tax`，或 `Including and Excluding Tax`.

   - ![Adobe Commerce](../assets/adobe-logo.svg) (仅限Adobe Commerce)设置 **[!UICONTROL Display Printed Card Prices]** 到 `Excluding Tax`， `Including Tax`，或 `Including and Excluding Tax`.

1. 将以下显示选项设置为 `Yes` 或 `No`，根据您的需求：

   - **[!UICONTROL Include Tax in Order Total]**
   - **[!UICONTROL Display Full Tax Summary]**
   - **[!UICONTROL Display Zero Tax Subtotal]**

1. 完成后，单击 **[!UICONTROL Save Config]**.

### [!UICONTROL Orders, Invoices, Credit Memos Display Settings]

1. 展开 ![扩展](../assets/icon-display-expand.png) 该 **[!UICONTROL Orders, Invoices, Credit Memos Display Settings]** 部分。

   ![订单、发票、贷项通知单显示设置](../configuration-reference/sales/assets/tax-orders-invoices-credit-memos-display-settings.png){width="600" zoomable="yes"}

1. 指定价格和税在订单、发票和贷项通知单中的显示方式：

   - 设置 **[!UICONTROL Display Prices]** 到 `Excluding Tax`， `Including Tax`，或 `Including and Excluding Tax`.

   - 设置 **[!UICONTROL Display Subtotal]** 到 `Excluding Tax`， `Including Tax`，或 `Including and Excluding Tax`.

   - 设置 **[!UICONTROL Display Shipping Amount]** 到 `Excluding Tax`， `Including Tax`，或 `Including and Excluding Tax`.

   - ![Adobe Commerce](../assets/adobe-logo.svg) (仅限Adobe Commerce)设置 **[!UICONTROL Display Gift Wrapping Prices]** 到 `Excluding Tax`， `Including Tax`，或 `Including and Excluding Tax`.

   - ![Adobe Commerce](../assets/adobe-logo.svg) (仅限Adobe Commerce)设置 **[!UICONTROL Display Printed Card Prices]** 到 `Excluding Tax`， `Including Tax`，或 `Including and Excluding Tax`.

1. 将以下显示选项设置为 `Yes` 或 `No`，根据您的要求：

   - **[!UICONTROL Include Tax in Order Total]**
   - **[!UICONTROL Display Full Tax Summary]**
   - **[!UICONTROL Display Zero Tax Subtotal]**

1. 完成后，单击 **[!UICONTROL Save Config]**.

### [!UICONTROL Fixed Product Taxes]

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Fixed Product Taxes]** 部分。

   ![固定产品税](../configuration-reference/sales/assets/tax-fixed-product-taxes.png){width="600" zoomable="yes"}

1. 设置 **[!UICONTROL Enable FPT]** 到 `Yes` 或 `No`，根据您的要求。

1. 如果启用了FPT，请指定FPT显示选项：

   - **[!UICONTROL Display Prices in Product Lists]**
   - **[!UICONTROL Display Price On Product view Page]**
   - **[!UICONTROL Display Prices in Sales Modules]**
   - **[!UICONTROL Display Prices in Emails]**

   - `Including FPT Only`  — 显示的价格包括固定产品税。 FPT金额不会单独显示。
   - `Including FPT and FPT description`  — 显示的价格包括固定产品税。 FPT金额将单独显示。
   - `Excluding FPT. Including FPT description and final price`  — 显示的价格不包括固定产品税。 FPT金额将单独显示。
   - `Excluding FPT`  — 显示的价格不包括固定产品税。 FPT金额不会单独显示。

1. 设置 **[!UICONTROL Apply Discounts to FPT]** 到 `Yes` 或 `No`，根据您的要求。

1. 设置 **[!UICONTROL FPT Tax Configuration]** 以确定FPT的计算方式。

   - `Not Taxed`  — 如果您的税务管辖区不对FPT征税，请选择此选项。 （例如，加利福尼亚。）
   - `Taxed`  — 如果您的税务管辖区对FPT征税，请选择此选项。 （例如，加拿大。）
   - `Loaded and Displayed with Tax`  — 如果在应用税之前将FPT添加到订单合计，请单击此选项。 （例如，欧盟国家。）

1. 设置 **[!UICONTROL Include FPT in Subtotal]** 到 `Yes` 或 `No`，根据您的要求。

1. 完成后，单击 **[!UICONTROL Save Config]**.

## 跨境价格一致性

跨境贸易（也称为价格一致性）支持欧盟(EU)和其他商家，他们想要为税率与商店税率不同的客户维持一致价格。

跨地区和地域运营的商家可以通过将税包含在产品价格中来显示单一价格。 定价干净整洁，不受各国税制和税率的影响。 这些设置要求安装计税扩展 [市场](../getting-started/commerce-marketplace.md)，例如 _顶点云_.

>[!NOTE]
>
>启用跨境贸易后，利润率会按税率变化。 利润由以下公式确定：<br>
>`Revenue - CustomerVAT - CostOfGoodsSold`

**_要实现跨境价格一致性，请执行以下操作：_**

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 对于多站点配置，设置 **[!UICONTROL Store View]** 到作为配置目标的网站和商店。

1. 在左侧面板中，展开 **[!UICONTROL Sales]** 并选择 **[!UICONTROL Tax]**.

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Calculation Settings]** 部分。

1. 设置 **[!UICONTROL Catalog Prices]** 到 `Including Tax`.

1. 要实现跨境价格一致性，请设置 **[!UICONTROL Enable Cross Border Trade]** 到 `Yes`.

   ![启用跨境贸易设置](./assets/cross-border-calculations-settings.png){width="600" zoomable="yes"}

1. 完成后，单击 **[!UICONTROL Save Config]**.

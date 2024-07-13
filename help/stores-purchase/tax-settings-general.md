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

以下说明将指导您完成Commerce实例的基本税务配置。 在设置税务之前，请确保您熟悉[区域设置](store-localize.md#step-3-change-the-locale-of-the-store-view)的税务要求。 然后，根据您的要求完成税务配置。

管理员[权限](../systems/permissions.md)可设置为根据业务&#x200B;_需要知道_&#x200B;而限制[对税务资源的访问权限](../systems/permissions-user-roles.md)。 要创建有权访问税设置的管理员角色，请选择销售/税和系统/税资源。 如果为不同于默认发运原点的区域设置网站，则还必须允许角色访问系统/发运资源。 配送设置确定用于目录价格的商店税率。

## 配置常规税务设置

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 对于多站点配置，将&#x200B;**[!UICONTROL Store View]**&#x200B;设置为配置目标的网站和商店。

1. 在左侧面板中，展开&#x200B;**[!UICONTROL Sales]**&#x200B;并选择&#x200B;**[!UICONTROL Tax]**。

1. 完成以下配置设置。

   如有必要，请清除任何灰显设置的&#x200B;**[!UICONTROL Use system value]**&#x200B;复选框。

### [!UICONTROL Tax Classes]

1. 展开&#x200B;**[!UICONTROL Tax Classes]**&#x200B;部分的![扩展选择器](../assets/icon-display-expand.png)。

   ![税类](../configuration-reference/sales/assets/tax-tax-classes.png){width="600" zoomable="yes"}

   - 运费的&#x200B;**税类** — 设置为相应的类。 默认类为： `None`和`Taxable Goods`
   - 赠品选项的&#x200B;**税类** — ![Adobe Commerce](../assets/adobe-logo.svg)(仅限Adobe Commerce)设置为相应的类。 默认类为： `None`和`Taxable Goods`
   - **产品的默认税类** — 设置为相应的类。 默认类为： `None`和`Taxable Goods`
   - **客户的默认税类** — 设置为相应的类。 默认类为： `Retail Customer`和`Wholesale Customer`

1. 完成后，单击&#x200B;**[!UICONTROL Save Config]**。

### [!UICONTROL Calculation Settings]

1. 展开&#x200B;**[!UICONTROL Calculation Settings]**&#x200B;部分。

   ![计算设置](../configuration-reference/sales/assets/tax-calculation-settings.png){width="600" zoomable="yes"}

1. 将&#x200B;**[!UICONTROL Tax Calculation Method Based On]**&#x200B;设置为以下项之一：

   - `Unit Price` — 每个产品的价格
   - `Row Total` — 订单中的行项目总数，减去折扣
   - `Total` — 订单总计

1. 将&#x200B;**[!UICONTROL Tax Calculation Based On]**&#x200B;设置为以下项之一：

   - `Shipping Address` — 将发送订单的地址
   - `Billing Address` — 客户或公司的帐单地址
   - `Shipping Origin` — 指定为商店的[原点](shipping-settings.md#point-of-origin)的地址

1. 将&#x200B;**[!UICONTROL Catalog Prices]**&#x200B;设置为`Excluding Tax`或`Including Tax`。

1. 将&#x200B;**[!UICONTROL Shipping Prices]**&#x200B;设置为`Excluding Tax`或`Including Tax`。

1. 将&#x200B;**[!UICONTROL Apply Customer Tax]**&#x200B;设置为以下项之一，以确定税应用于原始价格还是折扣价格： `After Discount`或`Before Discount`

1. 将&#x200B;**[!UICONTROL Apply Discount on Prices]**&#x200B;设置为以下项之一，以确定折扣是否含税： `Excluding Tax`或`Including Tax`

1. 将&#x200B;**[!UICONTROL Apply Tax On]**&#x200B;设置为`Custom price if available`或`Original price only`。

1. 将&#x200B;**[!UICONTROL Enable Cross-Border Trade]**&#x200B;设置为以下项之一：

   - `Yes` — 在不同税率间使用一致的定价。 如果目录价格包含税，则选择此设置将固定价格，而不考虑客户的税率。
   - `No` — 按税率更改价格。

   >[!IMPORTANT]
   >
   >如果启用了[跨境贸易](#cross-border-price-consistency)，则利润率会按税率变化。 利润由公式(`Revenue - CustomerVAT - CostOfGoodsSold`)确定。 要促进跨境贸易，必须将价格设为含税。

### [!UICONTROL Default Tax Destination Calculation]

1. 展开&#x200B;**[!UICONTROL Default Tax Destination Calculation]**&#x200B;部分的![扩展选择器](../assets/icon-display-expand.png)。

   ![默认纳税目标计算](../configuration-reference/sales/assets/tax-default-tax-destination-calculation.png){width="600" zoomable="yes"}

1. 为税务计算指定&#x200B;**[!UICONTROL Default Country]**。

1. 如果适用，请为计税指定&#x200B;**[!UICONTROL Default State]**。

1. 如果适用，请为计税指定&#x200B;**[!UICONTROL Default Post Code]**。

1. 完成后，单击&#x200B;**[!UICONTROL Save Config]**。

### [!UICONTROL Price Display Settings]

>[!IMPORTANT]
>
>某些与价格显示相关的设置组合（包括和排除税）可能会让客户感到困惑。 要避免触发警告消息，请参阅[推荐的设置](taxes.md#warning-messages)。

1. 展开&#x200B;**[!UICONTROL Price Display Settings]**&#x200B;部分的![扩展选择器](../assets/icon-display-expand.png)。

   ![价格显示设置](../configuration-reference/sales/assets/tax-price-display-settings.png){width="600" zoomable="yes"}

1. 将&#x200B;**[!UICONTROL Display Product Prices in Catalog]**&#x200B;设置为以下项之一：

   - `Excluding Tax` — 店面中显示的目录价格不含税。
   - `Including Tax` — 仅当税则与税源匹配或客户地址与税则匹配时，店面中的目录价格才包括税。 客户在购物车中创建帐户、登录或使用估算税和送货工具后，可能会发生此情况。
   - `Including and Excluding Tax` — 店面中显示的目录价格会同时显示含税和不含税。

1. 将&#x200B;**[!UICONTROL Display Shipping Prices]**&#x200B;设置为`Excluding Tax`、`Including Tax`或`Including and Excluding Tax`。

1. 完成后，单击&#x200B;**[!UICONTROL Save Config]**。

### [!UICONTROL Shopping Cart Display Settings]

1. 展开&#x200B;**[!UICONTROL Shopping Cart Display Settings]**&#x200B;部分的![扩展选择器](../assets/icon-display-expand.png)。

   ![购物车显示设置](../configuration-reference/sales/assets/tax-shopping-cart-display-settings.png){width="600" zoomable="yes"}

1. 对于以下每个设置，根据您的商店和区域设置要求，选择您希望税和价格在购物车中的显示方式：

   - 将&#x200B;**[!UICONTROL Display Prices]**&#x200B;设置为`Excluding Tax`、`Including Tax`或`Including and Excluding Tax`。

   - 将&#x200B;**[!UICONTROL Display Subtotal]**&#x200B;设置为`Excluding Tax`、`Including Tax`或`Including and Excluding Tax`。

   - 将&#x200B;**[!UICONTROL Display Shipping Amount]**&#x200B;设置为`Excluding Tax`、`Including Tax`或`Including and Excluding Tax`。

   - ![Adobe Commerce](../assets/adobe-logo.svg)(仅限Adobe Commerce)将&#x200B;**[!UICONTROL Display Gift Wrapping Prices]**&#x200B;设置为`Excluding Tax`、`Including Tax`或`Including and Excluding Tax`。

   - ![Adobe Commerce](../assets/adobe-logo.svg)(仅限Adobe Commerce)将&#x200B;**[!UICONTROL Display Printed Card Prices]**&#x200B;设置为`Excluding Tax`、`Including Tax`或`Including and Excluding Tax`。

1. 根据您的需要，将以下显示选项设置为`Yes`或`No`：

   - **[!UICONTROL Include Tax in Order Total]**
   - **[!UICONTROL Display Full Tax Summary]**
   - **[!UICONTROL Display Zero Tax Subtotal]**

1. 完成后，单击&#x200B;**[!UICONTROL Save Config]**。

### [!UICONTROL Orders, Invoices, Credit Memos Display Settings]

1. 展开&#x200B;**[!UICONTROL Orders, Invoices, Credit Memos Display Settings]**&#x200B;部分的![扩展](../assets/icon-display-expand.png)。

   ![订单、发票、贷项通知单显示设置](../configuration-reference/sales/assets/tax-orders-invoices-credit-memos-display-settings.png){width="600" zoomable="yes"}

1. 指定价格和税在订单、发票和贷项通知单中的显示方式：

   - 将&#x200B;**[!UICONTROL Display Prices]**&#x200B;设置为`Excluding Tax`、`Including Tax`或`Including and Excluding Tax`。

   - 将&#x200B;**[!UICONTROL Display Subtotal]**&#x200B;设置为`Excluding Tax`、`Including Tax`或`Including and Excluding Tax`。

   - 将&#x200B;**[!UICONTROL Display Shipping Amount]**&#x200B;设置为`Excluding Tax`、`Including Tax`或`Including and Excluding Tax`。

   - ![Adobe Commerce](../assets/adobe-logo.svg)(仅限Adobe Commerce)将&#x200B;**[!UICONTROL Display Gift Wrapping Prices]**&#x200B;设置为`Excluding Tax`、`Including Tax`或`Including and Excluding Tax`。

   - ![Adobe Commerce](../assets/adobe-logo.svg)(仅限Adobe Commerce)将&#x200B;**[!UICONTROL Display Printed Card Prices]**&#x200B;设置为`Excluding Tax`、`Including Tax`或`Including and Excluding Tax`。

1. 根据您的要求，将以下显示选项设置为`Yes`或`No`：

   - **[!UICONTROL Include Tax in Order Total]**
   - **[!UICONTROL Display Full Tax Summary]**
   - **[!UICONTROL Display Zero Tax Subtotal]**

1. 完成后，单击&#x200B;**[!UICONTROL Save Config]**。

### [!UICONTROL Fixed Product Taxes]

1. 展开&#x200B;**[!UICONTROL Fixed Product Taxes]**&#x200B;部分的![扩展选择器](../assets/icon-display-expand.png)。

   ![固定产品税](../configuration-reference/sales/assets/tax-fixed-product-taxes.png){width="600" zoomable="yes"}

1. 根据您的要求，将&#x200B;**[!UICONTROL Enable FPT]**&#x200B;设置为`Yes`或`No`。

1. 如果启用了FPT，请指定FPT显示选项：

   - **[!UICONTROL Display Prices in Product Lists]**
   - **[!UICONTROL Display Price On Product view Page]**
   - **[!UICONTROL Display Prices in Sales Modules]**
   - **[!UICONTROL Display Prices in Emails]**

   - `Including FPT Only` — 显示价格包括固定产品税。 FPT金额不会单独显示。
   - `Including FPT and FPT description` — 显示价格包括固定产品税。 FPT金额将单独显示。
   - `Excluding FPT. Including FPT description and final price` — 显示价格不包括固定产品税。 FPT金额将单独显示。
   - `Excluding FPT` — 显示价格不包括固定产品税。 FPT金额不会单独显示。

1. 根据您的要求，将&#x200B;**[!UICONTROL Apply Discounts to FPT]**&#x200B;设置为`Yes`或`No`。

1. 设置&#x200B;**[!UICONTROL FPT Tax Configuration]**&#x200B;以确定FPT的计算方式。

   - `Not Taxed` — 如果您的税务管辖区不对FPT征税，请选择此选项。 （例如，加利福尼亚。）
   - `Taxed` — 如果您的税务管辖区对FPT征税，请选择此选项。 （例如，加拿大。）
   - `Loaded and Displayed with Tax` — 如果在应用税之前将FPT添加到订单总计，请单击此选项。 （例如，欧盟国家。）

1. 根据您的要求，将&#x200B;**[!UICONTROL Include FPT in Subtotal]**&#x200B;设置为`Yes`或`No`。

1. 完成后，单击&#x200B;**[!UICONTROL Save Config]**。

## 跨境价格一致性

跨境贸易（也称为价格一致性）支持欧盟(EU)和其他商家，他们想要为税率与商店税率不同的客户维持一致价格。

跨地区和地域运营的商家可以通过将税包含在产品价格中来显示单一价格。 定价干净整洁，不受各国税制和税率的影响。 这些设置要求从[市场](../getting-started/commerce-marketplace.md)安装计税扩展，如&#x200B;_Vertex Cloud_。

>[!NOTE]
>
>启用跨境贸易后，利润率会按税率变化。 利润由以下公式确定：<br>
>`Revenue - CustomerVAT - CostOfGoodsSold`

**_启用跨境价格一致性：_**

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 对于多站点配置，将&#x200B;**[!UICONTROL Store View]**&#x200B;设置为配置目标的网站和商店。

1. 在左侧面板中，展开&#x200B;**[!UICONTROL Sales]**&#x200B;并选择&#x200B;**[!UICONTROL Tax]**。

1. 展开&#x200B;**[!UICONTROL Calculation Settings]**&#x200B;部分的![扩展选择器](../assets/icon-display-expand.png)。

1. 将&#x200B;**[!UICONTROL Catalog Prices]**&#x200B;设置为`Including Tax`。

1. 要启用跨境价格一致性，请将&#x200B;**[!UICONTROL Enable Cross Border Trade]**&#x200B;设置为`Yes`。

   ![启用跨境贸易设置](./assets/cross-border-calculations-settings.png){width="600" zoomable="yes"}

1. 完成后，单击&#x200B;**[!UICONTROL Save Config]**。

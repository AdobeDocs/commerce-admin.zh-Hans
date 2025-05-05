---
title: '[!UICONTROL Sales] &amp；gt； [!UICONTROL Tax]'
description: 查看Commerce管理员的[!UICONTROL Sales] &amp；gt； [!UICONTROL Tax]页面上的配置设置。
exl-id: eb929a6c-adb2-45ac-b6ec-6239938355bf
feature: Configuration, Taxes
source-git-commit: f95e6d22f83b518c64b254f0d98147e3c6ebaf42
workflow-type: tm+mt
source-wordcount: '1305'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Tax]

>[!NOTE]
>
>Adobe Commerce和Magento Open Source版本2.4.0到2.4.3包含由Vertex供应商开发的扩展，该扩展用于与[!UICONTROL Vertex Cloud]集成。 从2.4.4版本开始，此扩展不再与核心版本捆绑在一起，必须从Commerce Marketplace安装和更新。 通过Marketplace，还可以访问扩展开发人员提供的当前文档。
><br><br>
>如果已启用并配置捆绑的扩展，则必须在升级2.4.4的过程中更新您的composer.json文件，并且以后要管理扩展更新。 有关详细信息，请参阅&#x200B;_升级指南_&#x200B;中的[升级模块和扩展](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html)。

{{config}}

## [!UICONTROL Tax Classes]

![税类](./assets/tax-tax-classes.png)<!-- zoom -->

有关更改这些设置的详细信息，请参阅&#x200B;_商店和购买体验指南_&#x200B;中的[税类](../../stores-purchase/tax-class.md)。

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Tax Class for Shipping] | 网站 | 标识用于发运的税分类。 选项包括所有可用的产品税类： `None` / `Taxable Goods` / `Shipping` / `Tax Exempt` |
| [!UICONTROL Tax Class for Gift Options] | 网站 | ![Adobe Commerce](../../assets/adobe-logo.svg)(仅限Adobe Commerce)标识用于赠品选项的默认税类。 |
| [!UICONTROL Default Tax Class for Product] | 全局 | 标识用于产品的默认税分类。 |
| [!UICONTROL Default Tax Class for Customer] | 全局 | 标识用于客户的默认税分类。 |

{style="table-layout:auto"}

## [!UICONTROL Calculation Settings]

![计算设置](./assets/tax-calculation-settings.png)<!-- zoom -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Tax Calculation Method Based On] | 网站 | 确定用于计算订单税的方法。 选项：<br/>**`Unit Price`**— 计税基于每个产品的单价。<br/>**`Row Total`** — 税费计算基于行项目总计。 <br/>**`Total`**— 税费计算基于订单总额。<br/><br/>_&#x200B;**&#x200B;注意：**&#x200B;_如果从Marketplace安装了计税扩展，如&#x200B;_Vertex Cloud_，则扩展服务将列为选项。 |
| [!UICONTROL Tax Calculation Based On] | 网站 | 确定税额计算是基于发运地址、帐单地址还是发运来源。 选项： `Shipping Address` / `Billing Address` / `Shipping Origin` |
| [!UICONTROL Catalog Prices] | 网站 | 确定目录价格是否包含或排除税。 选项： `Excluding Tax` / `Including Tax` |
| [!UICONTROL Shipping Prices] | 网站 | 确定装运价格中包含或排除税。 选项： `Excluding Tax` / `Including Tax` |
| [!UICONTROL Apply Customer Tax] | 网站 | 确定税在折扣之前或之后应用。 选项： `Before Discount` / `After Discount` |
| [!UICONTROL Apply Discount on Prices] | 网站 | 确定折扣价是否包括或不包括税。 选项： `Excluding Tax` / `Including Tax` |
| [!UICONTROL Apply Tax On] | 网站 | 确定税额是应用于原始价格还是自定义价格（如果可用）。 选项： `Custom price if available` / `Original price only` |
| [!UICONTROL Enable Cross Border Trade] | 网站 | 启用后，会跨具有不同税率的区域应用一致的定价。 选项： `Yes` / `No` <br/><br/>**_注意：_**&#x200B;使用跨境贸易将按税率调整利润率。 |

{style="table-layout:auto"}

## [!UICONTROL Default Tax Destination Calculation]

![默认纳税目标计算](./assets/tax-default-tax-destination-calculation.png)<!-- zoom -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Default Country] | 商店视图 | 确定计税所依据的国家/地区。 |
| [!UICONTROL Default State] | 商店视图 | 确定计税所依据的省/市/自治区。 星号(*)可用作通配符来指示选定国家/地区内的所有状态。 |
| [!UICONTROL Default Post Code] | 商店视图 | 标识计算税额所依据的邮政编码或邮政编码。 星号(*)可用作通配符，以指示选定州内的所有邮政编码。 |

{style="table-layout:auto"}

## [!UICONTROL Price Display Settings]

![价格显示设置](./assets/tax-price-display-settings.png)<!-- zoom -->

有关更改这些设置的详细信息，请参阅&#x200B;_商店和购买体验指南_&#x200B;中的[配置价格显示设置](../../stores-purchase/display-settings.md#configure-price-display-settings)。

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Display Product Prices in Catalog] | 商店视图 | 确定目录中所发布的产品价格是包含还是排除税，或显示两个版本价格；一个包含税，另一个不含税。 选项： `Excluding Tax` / `Including Tax` / `Including and Excluding Tax` <br/><br/>**_注意：_**&#x200B;如果将“显示产品价格”字段设置为`Including Tax`，则仅当存在与税源匹配的税则或存在与税则匹配的客户地址时，才会显示税。 可触发匹配的事件包括客户帐户创建、登录，或购物车中使用税务和运输估计工具。 |
| [!UICONTROL Display Shipping Prices] | 商店视图 | 确定配送价格是否包含税或不含税，或显示两个版本的配送价格；一个包含税，另一个不含税。 选项： `Excluding Tax` / `Including Tax` / `Including and Excluding Tax` |

{style="table-layout:auto"}

## [!UICONTROL Shopping Cart Display Settings]

![购物车显示设置](./assets/tax-shopping-cart-display-settings.png)<!-- zoom -->

有关更改这些设置的详细信息，请参阅&#x200B;_商店和购买体验指南_&#x200B;中的[配置购物车显示设置](../../stores-purchase/display-settings.md#step-2-configure-shopping-cart-display-settings)。

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Display Prices] | 商店视图 | 确定购物车价格是包含还是不包含税，或者显示两个版本的价格；一个包含税，另一个不含税。 选项： `Excluding Tax` / `Including Tax` / `Including and Excluding Tax` |
| [!UICONTROL Display Subtotal|Store View] | 确定购物车小计是否包含或排除税，或显示小计的两个版本；一个包含税，另一个不含税。 选项： `Excluding Tax` / `Including Tax` / `Including and Excluding Tax` |
| [!UICONTROL Display Shipping Amount] | 商店视图 | 确定购物车配送金额是否含税或不含税，或显示配送金额的两个版本；一个含税，另一个不含税。 选项： `Excluding Tax` / `Including Tax` / `Including and Excluding Tax` |
| [!UICONTROL Additionally Show Order Total Without Tax] | 商店视图 | 确定购物车中是否显示包含不含税总金额的额外行。 选项： `Yes` / `No` |
| [!UICONTROL Display Full Tax Summary] | 商店视图 | 确定购物车是否包含完整的税务汇总。 选项： `Yes` / `No` |
| [!UICONTROL Display Zero Tax Subtotal] | 商店视图 | 确定税为零时购物车是否包含税小计。 选项： `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Orders, Invoices, Credit Memos Display Settings]

![订单、发票、贷项通知单显示设置](./assets/tax-orders-invoices-credit-memos-display-settings.png)<!-- zoom -->

有关更改这些设置的详细信息，请参阅&#x200B;_存储和购买体验指南_&#x200B;中的[配置订单、发票和贷项通知单显示设置](../../stores-purchase/display-settings.md#step-3-configure-order-invoice-and-credit-memo-display-settings)。

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Display Prices] | 商店视图 | 确定销售单据上的价格是否包括或不包括税，或者每个单据是否显示两个版本的价格；一个含税，另一个不含税。 选项： `Excluding Tax` / `Including Tax` / `Including and Excluding Tax` |
| [!UICONTROL Display Subtotal] | 商店视图 | 确定销售单据的小计是否包括或不包括税，或者每个单据是否显示小计的两个版本；一个包含税，另一个不含税。 选项： `Excluding Tax` / `Including Tax` / `Including and Excluding Tax` |
| [!UICONTROL Display Shipping Amount] | 商店视图 | 确定销售单据上的发运金额是否包括或不包括税，或者每个单据是否显示小计的两个版本；一个包含税，另一个不含税。 选项： `Excluding Tax` / `Including Tax` / `Including and Excluding Tax` |
| [!UICONTROL Additionally Show Order Total Without Tax] | 商店视图 | 确定在销售单据上是否显示附加行，其中包含不含税的总金额。 选项： `Yes` / `No` |
| [!UICONTROL Display Full Tax Summary] | 商店视图 | 确定销售单据上是否显示完整的税汇总。 选项： `Yes` / `No` |
| [!UICONTROL Display Zero Tax Subtotal] | 商店视图 | 确定不计税时销售单据上出现的小计部分。 选项： `Yes` / `No` |
| [!UICONTROL Display Gift Wrapping Prices] | 商店视图 | ![Adobe Commerce](../../assets/adobe-logo.svg)(仅限Adobe Commerce)确定小计中是否包含礼品包装价格。 选项： `Excluding Tax` / `Including Tax` / `Including and Excluding Tax` |
| [!UICONTROL Display Printed Card Prices] | 商店视图 | ![Adobe Commerce](../../assets/adobe-logo.svg)(仅限Adobe Commerce)确定小计中是否包含打印卡价格。 选项： `Excluding Tax` / `Including Tax` / `Including and Excluding Tax` |

{style="table-layout:auto"}

## [!UICONTROL Fixed Product Taxes]

![固定产品税](./assets/tax-fixed-product-taxes.png)<!-- zoom -->

有关更改这些设置的详细信息，请参阅&#x200B;_商店和购买体验指南_&#x200B;中的[固定产品税(FPT)](../../stores-purchase/fixed-product-tax.md)。

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Enable FPT] | 网站 | 确定FPT是否可用。 选项： `Yes` / `No` |
| [!UICONTROL Display Prices in Product Lists] | 网站 | 控制产品列表中FPT的显示。 选项：<br/> **`Including FPT Only`** — 显示价格包括固定产品税。 FPT金额不会单独显示。<br/>**`Including FPT and FPT description`**— 显示价格包括固定产品税。 FPT金额将单独显示。<br/>**`Excluding FPT. Including FPT description and final price`** — 显示价格不包括固定产品税。 FPT金额将单独显示。<br/>**`Excluding FPT`**— 显示价格不包括固定产品税。 FPT金额不会单独显示。 |
| [!UICONTROL Display Prices On Product View Page] | 网站 | 控制产品页面上FPT的显示。 选项：<br/> **`Including FPT Only`** — 显示价格包括固定产品税。 FPT金额不会单独显示。<br/>**`Including FPT and FPT description`**— 显示价格包括固定产品税。 FPT金额将单独显示。<br/>**`Excluding FPT. Including FPT description and final price`** — 显示价格不包括固定产品税。 FPT金额将单独显示。<br/>**`Excluding FPT`**— 显示价格不包括固定产品税。 FPT金额不会单独显示。 |
| [!UICONTROL Display Prices in Sales Modules] | 网站 | 控制购物车和结帐期间FPT的显示。 选项：<br/> **`Including FPT Only`** — 显示价格包括固定产品税。 FPT金额不会单独显示。<br/>**`Including FPT and FPT description`**— 显示价格包括固定产品税。 FPT金额将单独显示。<br/>**`Excluding FPT. Including FPT description and final price`** — 显示价格不包括固定产品税。 FPT金额将单独显示。<br/>**`Excluding FPT`**— 显示价格不包括固定产品税。 FPT金额不会单独显示。 |
| [!UICONTROL Display Prices in Emails] | 网站 | 控制电子邮件中FPT的显示。 选项：<br/> **`Including FPT Only`** — 显示价格包括固定产品税。 FPT金额不会单独显示。<br/>**`Including FPT and FPT description`**— 显示价格包括固定产品税。 FPT金额将单独显示。<br/>**&#x200B;排除FPT。 包括FPT说明和最终价格&#x200B;**— 显示价格不包括固定产品税。 FPT金额将单独显示。<br/>**`Excluding FPT`** — 显示价格不包括固定产品税。 FPT金额不会单独显示。 |
| [!UICONTROL Apply Tax to FPT] | 网站 | 确定是否对FPT金额应用税。 选项： `Yes` / `No` |
| [!UICONTROL Include FPT in Subtotal] | 网站 | 确定FPT是否包含在购物车小计中。 选项： <br/>**`Yes`**— 在购物车小计中包括FPT。<br/>**`No`** - FPT不包含在小计中，而是放置在购物车中的小计之后。 |

{style="table-layout:auto"}

---
title: 分层定价
description: 了解如何使用层定价从产品列表或产品页面提供数量折扣。
exl-id: b5810899-31a6-4288-9acc-09f7f4dfbd43
feature: Catalog Management, Products
source-git-commit: 8d73a3a635c20e636c4b8bde41a4f807d3fd9f2e
workflow-type: tm+mt
source-wordcount: '882'
ht-degree: 0%

---

# 分层定价

分层定价允许您从店面的产品列表或产品页面提供数量折扣。 折扣可应用于特定商店视图或客户组或共享目录。

如果要更新许多产品，则导入层价格更改而不是单独输入它们是最有效的。 有关详细信息，请参阅[导入层价格](../systems/data-import-price-tier.md)。

店面产品页面上的![层价格](./assets/product-price-tier-storefront.png){width="700" zoomable="yes"}

产品页计算数量折扣并显示如下消息：

`Buy 6 for $5.95 each and save 15%`

店面中的价格从最高价到最低价优先。 如果您有数量为`5`的层价格和`10`的层价格，并且客户向购物车中添加了五个、六个、七个、八个或九个项目，则客户将收到数量为`5`的层折扣价格。 当客户添加第十个项目时，为数量`10`层指定的折扣价格将取代数量`5`的层，并且适用`10`的折扣价格。

## 为产品添加价格层

1. 在编辑模式下打开产品。

1. 在&#x200B;_[!UICONTROL Price]_&#x200B;字段下，单击&#x200B;**[!UICONTROL Advanced Pricing]**。

1. 在&#x200B;_[!UICONTROL Tier Price]_&#x200B;部分中，单击&#x200B;**[!UICONTROL Add]**。

   如果要创建包含多个价格的分层，请单击每个额外层的&#x200B;**[!UICONTROL Add]**，以便您可以同时处理所有层。 组内各层网站和客户组或共享目录分配相同，但数量和价格不同。

## 配置价格层

1. 如果您的商店有多个网站，请选择应用层定价的&#x200B;**[!UICONTROL Website]**。

1. 如有必要，请选择&#x200B;**[!UICONTROL Customer Group]**&#x200B;或&#x200B;**[!UICONTROL Shared Catalog]**&#x200B;以限制定价层的可用性(![Adobe Commerce B2B](../assets/b2b.svg)仅适用于[Adobe Commerce B2B](./b2b/../introduction.md))。

1. 对于&#x200B;**[!UICONTROL Qty]**，输入必须订购才能获得折扣的数量。

   - **方法1：**&#x200B;输入固定金额的价格

     将&#x200B;**[!UICONTROL Price]**&#x200B;设置为`Fixed`，然后输入该层上单件产品的调整价格。

     将![层价格作为固定金额](./assets/product-price-tier-fixed.png){width="600" zoomable="yes"}

   - **方法2：**&#x200B;输入百分比形式的价格

     将&#x200B;**[!UICONTROL Price]**&#x200B;设置为`Discount`并输入折扣价格，以产品基本价格的百分比表示。

     例如，对于15%的折扣，请输入数字`15`。 （保存价格时带有两个小数位，如`15.00`。）

     >[!NOTE]
     >
     >要获得折扣价格，定义的百分比是根据&#x200B;_[!UICONTROL Price]_&#x200B;字段中定义的值计算的，而不是根据&#x200B;_[!UICONTROL Special Price]_&#x200B;字段计算的。

     ![层价格百分比](./assets/product-price-tier-discount.png){width="600" zoomable="yes"}

## 完成价格配置

1. 要为不同的网站或客户组添加另一组层定价，请重复上述步骤。

1. 完成后，单击&#x200B;**[!UICONTROL Done]**，然后单击&#x200B;**[!UICONTROL Save]**。

>[!NOTE]
>
>使用以下公式计算&#x200B;**_最终_**&#x200B;产品价格为&#x200B;**_最低_**&#x200B;相关价格： <br/>`Final Price=Min(Regular(Base) Price, Group(Tier) Price, Special Price, Catalog Price Rule) + Sum(Min Price per each required custom option)`

>[!NOTE]
>
>**_固定价格_**&#x200B;产品可自定义选项&#x200B;_不_&#x200B;受组价格、层价格、特殊价格或目录价格规则的影响。

## 为目录价格规则启用层定价

仅[!BADGE SaaS]{type=Positive url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="仅适用于Adobe Commerce as a Cloud Service项目(Adobe管理的SaaS基础架构)。"}

在Commerce的早期版本中，层定价不能与目录价格规则结合使用。 目录规则忽略层价格配置，仅从原始基本价格计算折扣。 通过使用Adobe Commerce as a Cloud Service，您现在可以选择在计算目录价格规则时包含层定价。

要启用此功能，请执行以下操作：

1. 导航到&#x200B;**[!UICONTROL Stores]** > *[!UICONTROL Settings]* > **[!UICONTROL Configuration]** > **[!UICONTROL Sales]** > **[!UICONTROL Sales]** > **[!UICONTROL Promotions]**，并将&#x200B;**[!UICONTROL Apply Catalog Price Rule on Grouped Price]**&#x200B;字段设置为&#x200B;**[!UICONTROL Yes]**。

   ![为目录价格规则启用层定价](../configuration-reference/sales/assets/sales-promotions-settings.png){width="700" zoomable="yes"}

1. 为您要通过目录价格规则定位的每个特定客户组或共享目录（例如`1`、`Wholesale`或商家定义的组）定义数量为`Retail`的层价格。 `ALL GROUPS`客户组和`Default`共享目录不能用于此目的。 对于未定义层价格且数量为`1`的任何组，不启用层定价。

1. 根据需要定义数量大于`1`的其他层价格。 当客户将更多数量的产品添加到购物车时，将照常应用这些额外的层价格。 目录价格规则不适用于这些额外的层级价格。

要说明在购买单个产品时分层定价如何与目录价格规则配合使用，请考虑以下示例：

- 产品的标准基本价格为100美元。
- 为数量为`Wholesale`且固定价格为90美元的`1`客户组定义了层级价格。
- 目录价格规则为`Wholesale`客户组提供10%的折扣。

为目录价格规则启用层定价后，系统将使用以下流程计算最终价格：

1. 在客户登录之前，产品价格显示为100 USD（标准基本价）。

1. 客户作为`Wholesale`组的成员登录后，产品价格将调整为90 USD（`Wholesale`组的层价格）。

1. 应用目录价格规则，在层级价格90美元上提供10%的折扣，最终价格为81美元。

下表汇总了在目录价格规则启用层定价并且目录价格规则为所有客户组提供10%折扣时的价格计算：

产品：标准价格$100（单项采购）

| 客户组 | 层价格（数量=1） | 新基本价格 | 最终价格 |
|---|---|---|---|
| 所有组 | 未配置 | 100美元 | $100 - 10% = $90 |
| 批发 | 固定：85美元 | 85美元 | 85美元 — 10% = 76.50美元 |
| retailer | 20%折扣 | 80美元 | 80美元 — 10% = 72.00美元 |
| VIP | 15%折扣 | 85美元 | 85美元 — 10% = 76.50美元 |

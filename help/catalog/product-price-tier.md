---
title: 分层定价
description: 了解如何使用层定价从产品列表或产品页面提供数量折扣。
exl-id: b5810899-31a6-4288-9acc-09f7f4dfbd43
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '459'
ht-degree: 0%

---

# 分层定价

分层定价允许您从店面的产品列表或产品页面提供数量折扣。 折扣可应用于特定商店视图或客户组或共享目录。

如果要更新许多产品，则导入层价格更改而不是单独输入它们是最有效的。 有关更多信息，请参阅 [导入层价格](../systems/data-import-price-tier.md).

![店面产品页面上的层价格](./assets/product-price-tier-storefront.png){width="700" zoomable="yes"}

产品页计算数量折扣并显示如下消息：

`Buy 6 for $5.95 each and save 15%`

店面中的价格从最高价到最低价优先。 如果您有数量的层价格 `5` 一个用于 `10`，并且客户将五、六、七、八或九件商品添加到购物车时，客户将获得该数量的折扣价格 `5` 层。 当客户添加第十个项目时，为数量指定的折扣价格 `10` 层取代层的 `5`，和折扣价 `10` 适用。

## 为产品添加价格层

1. 在编辑模式下打开产品。

1. 在 _[!UICONTROL Price]_字段，请单击&#x200B;**[!UICONTROL Advanced Pricing]**.

1. 在 _[!UICONTROL Tier Price]_部分，单击&#x200B;**[!UICONTROL Add]**.

   如果要创建多个价格的层级，请单击 **[!UICONTROL Add]** 对于每一个附加层，您都可以同时使用所有层。 组内各层网站和客户组或共享目录分配相同，但数量和价格不同。

## 配置价格层

1. 如果您的商店有多个网站，请选择 **[!UICONTROL Website]** 适用于分层定价。

1. 如有必要，通过选择以下选项限制定价层的可用性 **[!UICONTROL Customer Group]** 或 **[!UICONTROL Shared Catalog]** (![适用于Adobe Commerce的B2B](../assets/b2b.svg) 提供方式 [适用于Adobe Commerce的B2B](./b2b/../introduction.md) 仅限)。

1. 对象 **[!UICONTROL Qty]**，输入必须订购才能获得折扣的数量。

   - **方法1：** 将价格输入为固定金额

     设置 **[!UICONTROL Price]** 到 `Fixed` 并输入该层上某一单位的调整后价格。

     ![将层价格作为固定金额](./assets/product-price-tier-fixed.png){width="600" zoomable="yes"}

   - **方法2：** 输入百分比形式的价格

     设置 **[!UICONTROL Price]** 到 `Discount` 并输入折扣价格，以产品基本价格的百分比表示。

     例如，对于15%的折扣，请输入数字 `15`. (保存价格时带有两个小数位，例如 `15.00`.)

     >[!NOTE]
     >
     >为取得贴现价格，已定义的百分比乃根据已定义于 _[!UICONTROL Price]_ 字段，而不是 _[!UICONTROL Special Price]_ 字段。

     ![以百分比表示的分层价格](./assets/product-price-tier-discount.png){width="600" zoomable="yes"}

## 完成价格配置

1. 要为不同的网站或客户组添加另一组层定价，请重复上述步骤。

1. 完成后，单击 **[!UICONTROL Done]** 然后 **[!UICONTROL Save]**.

>[!NOTE]
>
>此 **_最终_** 产品价格的计算方式为 **_最小值_** 相关价格，使用下列公式： <br/>`Final Price=Min(Regular(Base) Price, Group(Tier) Price, Special Price, Catalog Price Rule) + Sum(Min Price per each required custom option)`

>[!NOTE]
>
>**_固定价格_** 产品可自定义选项包括 _非_ 受组价格、层价格、特殊价格或目录价格规则影响。

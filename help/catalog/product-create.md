---
title: 创建产品
description: 了解可为目录创建的产品类型。
exl-id: ff90bf8a-a64d-403f-bd09-5c8167a36f0b
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '693'
ht-degree: 0%

---

# 创建产品

选择产品类型是创建产品必须执行的首要操作之一。 如果您刚刚开始构建产品目录，则可以创建几个示例产品来试验每种产品类型。 除了基本产品类型外，术语 _复杂产品_ 有时用于引用具有多个选项的产品，例如可用于各种颜色和大小的可配置产品。

>[!NOTE]
>
>要获得更深入的了解，请参阅目录 [导航](navigation.md)，如何设置 [类别](categories.md) 和 [属性](product-attributes.md)和目录 [URL选项](catalog-urls.md) 可用。 了解这些概念后，将许多产品添加到目录的最有效方法是 [导入](../systems/data-import.md) 它们来自CSV文件。

![店面的产品页面](./assets/storefront-product-page.png){width="700" zoomable="yes"}

## 产品类型

**[简单产品](product-create-simple.md)**  — 简单产品是指具有单个SKU的物理项目。 简单产品具有不同的定价和输入控制，这使得销售产品的变体成为可能。 简单产品可与分组、捆绑和可配置产品关联使用。

**[可配置产品](product-create-configurable.md)**  — 可配置产品似乎是一个产品，其中包含每个变体的选项列表。 但是，每个选项代表一个单独的、简单的产品，并具有不同的SKU，这使得能够跟踪每个变体的库存。

**[已分组的产品](product-create-grouped.md)**  — 分组产品将多个独立产品作为一个组呈现。 您可以提供单个产品的变体，也可以针对促销活动对变体进行分组。 这些产品可以单独购买，也可以集体购买。

**[虚拟产品](product-create-virtual.md)**  — 虚拟产品不是有形产品，通常用于服务、会员资格、保修和订购等产品。 虚拟产品可与分组产品和捆绑产品关联使用。

**[捆绑产品](product-create-bundle.md)**   — 捆绑产品使客户可以从一系列选项中“构建自己的产品”。 捆绑包可以是礼品篮、计算机或可自定义的任何其他内容。 捆绑包中的每个项目都是独立的独立产品。

**[可下载的产品](product-create-downloadable.md)**  — 可数字下载的产品由下载的一个或多个文件组成。 这些文件可以驻留在您的服务器上，也可以作为URL提供给任何其他服务器。

**[礼品卡](product-gift-card-create.md)** - ([Adobe Commerce](../landing/home.md#product-editions) 只有)礼品卡有三种。 _虚拟_ 礼品卡通过电子邮件发送。 _物理_ 礼品卡已发送给收件人。 _已合并_ 虚拟和物理相结合的礼品卡。 每个帐户都有一个唯一代码，在结账时可兑换此代码。 礼品卡也可以包含在分组产品中。

## 产品设置

最常用的产品设置和属性显示在页面顶部，其后是自定义属性。 任何其他产品设置都位于页面底部的可展开部分中。

![产品设置](./assets/product-settings.png){width="600" zoomable="yes"}

| 设置 | 描述 |
|--- |--- |
| [[!UICONTROL Sources]](../inventory-management/sources-assign-per-product.md) | (时间 [[!DNL Inventory Management]](../inventory-management/introduction.md) （已启用）列出从中分发产品的源。 |
| [[!UICONTROL Content]](product-content.md) | 用于输入和编辑店面产品页面上显示的主要产品说明。 |
| [[!UICONTROL Configurations]](product-configurations.md) | 列出产品的任何现有变体，并可用于生成变体以与可配置产品类型一起使用。 |
| [[!UICONTROL Product Reviews]](settings-advanced-product-reviews.md) | 列出客户为产品提交的所有审阅。 |
| [[!UICONTROL Search Engine Optimization]](product-search-engine-optimization.md) | 指定搜索引擎用于为产品编制索引的URL键和元数据字段。 |
| [[!UICONTROL Related Products, Up-Sells, and Cross-Sells]](related-products-up-sells-cross-sells.md) | 用于在店面上设置简单的促销块，展示客户可能感兴趣的一系列其他产品。 |
| [[!UICONTROL Customizable Options]](settings-advanced-custom-options.md) | 向产品添加可自定义的选项。 |
| [[!UICONTROL Product in Websites]](settings-basic-websites.md) | 根据商店层次结构确定每个可用产品的网站。 |
| [[!UICONTROL Design]](settings-advanced-design.md) | 用于向产品页面应用不同的主题、更改列布局、确定产品选项出现的位置，以及输入自定义XML代码。 |
| [[!UICONTROL Gift options]](product-gift-options.md) | 用于在产品级别结帐时启用或禁用礼品消息选项。 |
| [[!UICONTROL Product In Shared Catalogs]](../b2b/catalog-shared.md) | ![适用于Adobe Commerce的B2B](../assets/b2b.svg) (适用于 [适用于Adobe Commerce的B2B](../b2b/introduction.md) （仅限）支持使用自定义定价为不同公司维护共享目录。 |
| [[!UICONTROL Downloadable Information]](product-create-downloadable.md#step-5-complete-the-downloadable-information) | 用于定义产品下载的参数。 |

{style="table-layout:auto"}

## 高级定价和库存

要访问高级定价和库存设置，请单击下面的链接 **[!UICONTROL Price]** 和 **[!UICONTROL Quantity]**. 有关更多信息，请参阅 [管理定价](pricing-advanced.md) 和 [Inventory management](../inventory-management/introduction.md).

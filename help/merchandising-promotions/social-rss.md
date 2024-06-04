---
title: 社交媒体和RSS源
description: 了解如何添加社交媒体和其他RSS信息源集成以构建品牌和产品意识。
exl-id: e4a48870-f53e-4848-8faa-8f2aedaf53b7
feature: Merchandising, Communications
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '1162'
ht-degree: 0%

---

# 社交媒体和RSS源

许多商家使用社交媒体和其他数字工具来建立品牌和产品知名度。 您可以通过安装Marketplace扩展或向内容页面添加插件来将商店与社交网络集成。 使用RSS馈送将您的产品信息发布到购物聚合网站，甚至将它们包含在您的新闻稿中。 客户可以订阅您的RSS源，以了解有关新产品和促销的信息。

## 社交网络

通过安装 [Marketplace扩展](../getting-started/commerce-marketplace.md). 此外，您还可以轻松添加社交插件，例如 _点赞_ 按钮添加到可合并到您整个商店页面中的CMS块。

社交网站具有大量插件，可以轻松添加到您的商店中。 此外，Commerce Marketplace上还有许多扩展可用于将您的商店与社交媒体集成。 以下示例显示如何添加Facebook _点赞_ 按钮到您的商店。

>[!NOTE]
>
>Adobe Commerce已删除本机 _Magento社交_ facebook集成，不再支持该扩展。 转到 [Commerce Marketplace](https://marketplace.magento.com/catalogsearch/result/?q=Facebook){：target=&quot;_blank&quot;}以找到Facebook集成的替代扩展。

### 步骤1. 获取按钮代码

1. 在Meta开发人员网站上，转到 [按钮设置](https://developers.facebook.com/docs/plugins/like-button) 页面。

1. 对象 **[!UICONTROL URL to Like]**，输入您希望用户访问的商店页面的URL _点赞_.

   例如，您可以输入商店主页的URL。

1. 选择 **[!UICONTROL Layout]** 按钮。

1. 输入 **[!UICONTROL Width]** 您的网站上按钮和任何关联文本消息可用的像素。

1. 设置 **[!UICONTROL Action Type]** 更改为以下任一项：

   - `Like`
   - `Recommend`

1. 单击 **[!UICONTROL Get Code]** 将生成的代码复制到剪贴板。

### 步骤2. 创建内容块

1. 返回到您的商店管理员。

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Blocks]**.

1. 在右上角，单击 **[!UICONTROL Add New Block]**.

1. 输入描述性 **[!UICONTROL Block Title]** 以供内部参考。

   例如： `Facebook Like Button`.

1. 分配唯一 **[!UICONTROL Identifier]** 到块，使用所有小写字符和下划线而不是空格。

   例如： `facebook_like_button`.

1. 如果您的Commerce实例有多个商店视图，请选择每个 **[!UICONTROL Store View]** 块可用的位置。

1. 根据您的内容工具，将代码片段添加到块内容中：

   - 使用时 [!DNL Page Builder]，添加 [HTML代码](../page-builder/html-code.md) 将从Facebook网站复制的代码片段粘贴到舞台上。 否则，将该代码段粘贴到 **[!UICONTROL Content]** 盒子。

   - 在编辑器中，将您从Facebook网站复制的代码片段粘贴到 **[!UICONTROL Content]** 盒子。

1. 如果块未准备好启用，请设置 **[!UICONTROL Enable Block]** 到 `No`.

1. 完成后，单击 **[!UICONTROL Save Block]**.

### 步骤3. 放置块

1. 添加块，具体取决于您的内容工具：

   - 使用时 [!UICONTROL Page Builder]，请按照说明 [添加块](../page-builder/block.md) 到舞台上。

   - 在 _管理员_ 侧栏，转到 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. 在右上角，单击 **[!UICONTROL Add Widget]** 并执行以下操作：

   - ![Adobe Commerce B2B](../assets/b2b.svg) (仅适用于Adobe Commerce B2B) _设置_ 部分，设置 **[!UICONTROL Type]** 到 `CMS Static Block` 并单击 **[!UICONTROL Continue]**.

   - 验证 **[!UICONTROL Design Theme]** 设置为当前主题。

   - 单击 **[!UICONTROL Continue]**.

1. 在 **[!UICONTROL Storefront Properties]** 部分，执行以下操作：

   - 对象 **[!UICONTROL Widget Title]**，输入标题以供内部参考。

   - 设置 **[!UICONTROL Assign to Store Views]** 到 `All Store Views`，或转到您希望应用程序可用的视图。 要选择多个视图，请按住Ctrl键(PC)或Command键(Mac)并单击每个选项。

   - 在 **[!UICONTROL Sort Order]** 字段来确定块的顺序（如果块被指定在页面上与其他内容元素相同的位置出现）。 顶部的位置是零。

1. 在 _[!UICONTROL Layout Updates]_部分，单击&#x200B;**[!UICONTROL Add Layout Update]**并设置&#x200B;**[!UICONTROL Display On]**到您希望块显示的类别、产品或页面。

   例如，如果您选择 `All Pages` 并将块放置在页眉或页脚中，则该块会出现在商店每个页面的同一位置。

   要将块放置在特定页面上，请执行以下操作：

   - 设置 **[!UICONTROL Display On]** 到 `Specified Page` 并选择 **[!UICONTROL Page]** 您希望块出现的位置。

   - 选择 **[!UICONTROL Block Reference]** 标识页面上要放置块的位置。

   - 接受默认设置 **[!UICONTROL Template]**，设置为 `CMS Static Block Default Template`.

   - 单击 **[!UICONTROL Save and Continue Edit]**.

1. 在左侧的面板中，选择 **[!UICONTROL Widget Options]**.

1. 单击 **[!UICONTROL Select Block…]** 选择您要放置的块。

1. 完成后，单击 **[!UICONTROL Save]**.

1. 出现提示时，按照工作区顶部的说明更新索引和页面缓存。

   构件现在显示在 _[!UICONTROL Widgets]_列表。

### 步骤4. 验证存储中的位置

返回到店面以验证块是否在正确的位置。 要移动块，您可以重新打开构件，尝试使用其他页面或块引用。

## RSS源

RSS (Really Simple Syndication)是一种基于XML的数据格式，用于在线分发信息。 您的客户可以订阅您的RSS源，以了解有关新产品和促销的信息。 RSS馈送还可用于将您的产品信息发布到购物聚合网站，并可包含在新闻稿中。

启用RSS馈送后，对产品、特殊优惠、类别和优惠券所做的任何添加都将自动发送给每个馈送的订阅者。 您发布的所有RSS馈送的链接都位于商店的页脚中。

![RSS馈送图标](./assets/icon-rss.png){width="100"}<br/>

读取RSS馈送所需的软件称为馈送读取器，允许人们订阅标题、博客、播客等。 GoogleReader是众多免费在线提供的信息源阅读器之一。

![示例店面 — RSS源](./assets/storefront-rss-feeds.png){width="700" zoomable="yes"}

### 设置RSS馈送的优点

- 从您的商店或博客下载最新更新
- 浅色广告
- 普通股
- 提升SEO
- 增加销售额

### RSS馈送的类型

| RSS源 | 描述 |
|--- |--- |
| [!UICONTROL Wish List] | 启用后，RSS信息源链接将显示在客户愿望列表页面的顶部。 此外，希望列表共享页面包括一个复选框，允许您包含共享希望列表的信息源的链接。 |
| [!UICONTROL New Products] | 发布添加到目录的新产品的通知。 |
| [!UICONTROL Special Products] | 发布具有特殊定价的任何产品的通知。 |
| [!UICONTROL Coupons / Discounts] | 发布商店中提供的任何特殊优惠券或折扣的通知。 |
| [!UICONTROL Top Level Category] | 发布对目录顶级类别结构所做任何更改的通知，这反映在主菜单中。 |
| [!UICONTROL Customer Order Status] | 使客户能够通过RSS馈送跟踪其订单状态。 启用后，订单上会显示RSS馈送链接。 |

{style="table-layout:auto"}

### 为您的商店设置RSS源

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在右上角，设置 **[!UICONTROL Store View]** 到将提供馈送的视图。

   如果提示您确认，请单击 **[!UICONTROL OK]**.

1. 在左侧面板中，展开 **[!UICONTROL Catalog]** 并选择 **[!UICONTROL RSS Feeds]**.

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Rss Config]** 分区和设置 **[!UICONTROL Enable RSS]** 到 `Enable`.

   ![目录配置 — RSS源](../configuration-reference/catalog/assets/rss-feeds-rss-config.png){width="600" zoomable="yes"}

   如有必要，请清除 **[!UICONTROL Use Default]** 复选框，以更改默认值。

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Wish List]** 分区和设置 **[!UICONTROL Enable RSS]** 到 `Enable`.

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Catalog]** 并将其他信息源设置为 `Enable` 根据需要。

   - **[!UICONTROL New Products]**
   - **[!UICONTROL Special Products]**
   - **[!UICONTROL Coupons/Discounts]**
   - **[!UICONTROL Top Level Category]**

   ![目录 — RSS源设置](../configuration-reference/catalog/assets/rss-feeds-catalog.png){width="600" zoomable="yes"}

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Order]** 分区和设置 **[!UICONTROL Customer Order Status Notification]** 到 `Enable`.

1. 完成后，单击 **[!UICONTROL Save Config]**.

1. 查看店面的结果，带有 `/rss` 页面URL的末尾。


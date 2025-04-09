---
title: 自动重定向
description: 了解如何配置每当产品或类别的URL密钥在Commerce商店中更改时生成的自动重定向。
exl-id: fbde09d3-a1a3-4bac-a850-4c74c99fe714
feature: Categories, Products, Configuration
source-git-commit: d088d5833b9c61e7b1c90a0839fdf38527929ce5
workflow-type: tm+mt
source-wordcount: '542'
ht-degree: 0%

---

# 自动重定向

您的商店可以配置为每当产品或类别的URL密钥更改时自动生成永久重定向。 在“搜索引擎优化”部分中，URL键下方的复选框指示是否启用了永久重定向。 如果您的存储已配置为自动重定向目录URL，则重定向是对URL键的简单更新。 创建自动重定向的过程对于产品和类别都是相同的。

>[!NOTE]
>
>如果启用了自动重定向，并且保存了类别，则所有产品和类别重写都将实时生成，并默认存储在数据库表中。 这可能会导致具有许多已分配产品的类别出现严重的性能问题。 解决方案是更改此默认设置，并在类别保存时跳过为产品生成类别/产品URL重写。 在这种情况下，将仅为规范的产品URL生成产品重写。

## 设置自动重定向

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧面板中，展开&#x200B;**[!UICONTROL Catalog]**&#x200B;并在下面选择&#x200B;**[!UICONTROL Catalog]**。

1. 展开&#x200B;**[!UICONTROL Search Engine Optimization]**&#x200B;部分的![扩展选择器](../assets/icon-display-expand.png)。

   ![目录配置 — 搜索引擎优化](../configuration-reference/catalog/assets/catalog-search-engine-optimization.png){width="600" zoomable="yes"}

1. 将&#x200B;**[!UICONTROL Create Permanent Redirect for URLs if URL Key Changed]**&#x200B;设置为`Yes`。

1. 完成后，单击&#x200B;**[!UICONTROL Save Config]**。


>[!NOTE]
>
> 可以为商店视图或网站范围生成URL重写。 从管理员处设置URL重写范围： **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]****[!UICONTROL Catalog]**>**[!UICONTROL Catalog]**>**[!UICONTROL Search Engine Optimization]**。 在_[!UICONTROL Product URL Rewrite Scope]_&#x200B;字段中选择范围。

## 自动重定向产品URL

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Catalog]** > **[!UICONTROL Products]**。

1. 在列表中查找产品，然后单击以打开记录。

1. 展开&#x200B;**[!UICONTROL Search Engine Optimization]**&#x200B;部分的![扩展选择器](../assets/icon-display-expand.png)。

   ![产品搜索引擎优化 — 永久重定向](./assets/product-search-engine-optimization-create-permanent-redirect.png){width="600" zoomable="yes"}

1. 对于&#x200B;**[!UICONTROL URL Key]**，请执行以下操作：

   - 确保已选中&#x200B;**[!UICONTROL Create Permanent Redirect for old URL]**&#x200B;复选框。 否则，请按照说明[启用自动重定向](url-rewrite.md#configure-url-rewrites)。

   - 根据需要更新&#x200B;**[!UICONTROL URL Key]**，在这些字符之间使用所有小写字符和非尾随连字符，而不是空格。

1. 完成后，单击&#x200B;**[!UICONTROL Save]**。

1. 当提示刷新缓存时，请按照工作区顶部消息中的链接进行操作。

   现在，永久重定向对产品及任何关联的类别URL生效。

## 自动重定向类别URL

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Catalog]** > **[!UICONTROL Categories]**。

1. 在树中查找类别，然后单击以打开记录。

1. 展开![扩展选择器](../assets/icon-display-expand.png) **[!UICONTROL Search Engine Optimization]**&#x200B;部分。

1. 对于&#x200B;**[!UICONTROL URL Key]**，执行以下操作：

   - 确保选中&#x200B;**[!UICONTROL Create Permanent Redirect for old URL]**&#x200B;复选框。 如果没有，请按照说明[启用自动重定向](url-rewrite.md#configure-url-rewrites)。

   - 根据需要更新&#x200B;**[!UICONTROL URL Key]**，在这些字符之间使用所有小写字符和非尾随连字符，而不是空格。

1. 完成后，单击&#x200B;**[!UICONTROL Save]**。

1. 提示刷新缓存时，请按照工作区顶部消息中的链接操作。

   永久重定向现在对类别和任何关联的产品URL有效。

## 跳过为类别保存生成产品URL重写 {#skip-rewrite}

>[!WARNING]
>
>关闭类别/产品URL重写的自动生成会导致永久删除所有现有类别/产品类型URL重写，并且无法恢复。 这可能会导致无法解决的类别/产品类型URL冲突，需要手动更新URL密钥才能解决。

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧面板中，展开&#x200B;**[!UICONTROL Catalog]**&#x200B;并在下面选择&#x200B;**[!UICONTROL Catalog]**。

1. 展开![扩展选择器](../assets/icon-display-expand.png) **[!UICONTROL Search Engine Optimization]**&#x200B;部分。

1. 将&#x200B;**[!UICONTROL Generate "category/product" URL Rewrites]**&#x200B;设置为`No`。

1. 在确认对话框中，单击“**[!UICONTROL OK]**”以确认更改和删除现有URL重写。

   ![关闭类别/产品URL重写 — 确认](./assets/seo-rewrite-off.png){width="350"}

1. 完成后，单击&#x200B;**[!UICONTROL Save Config]**。

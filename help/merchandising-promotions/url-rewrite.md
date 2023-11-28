---
title: URL重写
description: 了解URL重写并使用商务URL重写工具更改与产品、类别或CMS页面关联的URL。
exl-id: 91e65f7f-7e33-4da5-b0a1-538ace56328a
feature: Categories, Products, Configuration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '669'
ht-degree: 0%

---

# URL重写

利用URL重写工具，可更改与产品、类别或CMS页面关联的任何URL。 重写生效后，指向上一个URL的任何链接都会被重定向到新地址。

>[!NOTE]
>
>要同时更新多个或所有产品的URL重写，请参阅 [多个URL重写](url-rewrite-product.md#multiple-url-rewrites).

术语 _重写_ 和 _重定向_ 通常可互换使用，但指的流程略有不同。 URL重写会更改URL在浏览器中的显示方式。 URL重定向会更新存储在服务器中的URL。 URL重定向可以是临时的，也可以是永久的。 您的商店使用URL重写和重定向，以便您轻松更改产品、类别或页面的URL键并保留现有链接。

默认情况下， [自动URL重定向](url-redirect-product-automatic.md) 已为您的商店和启用 **为旧URL创建永久重定向** 复选框位于每个产品的URL键字段下。

{{url-rewrite-skip}}

{{url-rewrite-params}}

![搜索引擎优化 — 创建永久URL重定向](./assets/product-search-engine-optimization-create-permanent-redirect.png){width="600" zoomable="yes"}

## 规范URL

出于SEO目的，最好是每个网页都只有一个不同的URL。

如果您有一个可供多个URL访问的页面，或者您拥有的内容相似的其他页面，Google会将这些页面视为同一页面的重复版本。 Google选择一个URL作为规范版本并进行爬网，而所有其他URL则被视为重复URL，爬网的频率较低。

如果您没有明确告知给Google哪个URL是规范的，则会为您做出选择，或者可能会认为这两者具有相等权重。 这可能会导致不必要的行为，并存在爬网预算无效和分布式反向链接较少的风险。

根据您设置网站的方式，索引中可能会存在您网站的多个版本，包括：

    https://www.example.com
    https://www.example.com/
    http://www.example.com
    https://example.com
    https://www.example.com/index.html

要指定规范页面，请参阅 [Google Search Central文档](https://developers.google.com/search/docs/crawling-indexing/consolidate-duplicate-urls).

## 配置URL重写

启用Web服务器Apache Rewrites是初始Commerce设置的一部分。 Commerce通常使用URL重写来移除文件名 `index.php` ，通常显示在根文件夹之后的URL中。 启用Web服务器重写后，系统会重写每个URL以忽略 `index.php`. 重写操作会删除对搜索引擎或客户没有任何价值的词语，并且不会影响性能或网站排名。

没有Web服务器重写的URL

    http://www.yourdomain.com/magento/index.php/storeview/url-identifier

带有Web服务器重写的URL

    http://www.yourdomain.com/magento/storeview/url-identifier

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中，其中 **[!UICONTROL General]** 已展开，请选择 **[!UICONTROL Web]**.

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Search Engine Optimization]** 部分。

   ![常规配置 — Web搜索引擎优化](../configuration-reference/general/assets/web-search-engine-optimization.png){width="600" zoomable="yes"}

1. 设置 **[!UICONTROL Use Web Server Rewrites]** 按你的喜好去做。

1. 完成后，单击 **[!UICONTROL Save Config]**.

## 创建URL重写

您可以使用URL重写工具创建产品和类别重写，以及商店中任何页面的自定义重写。 重写生效后，指向上一个URL的任何现有链接都会被无缝重定向到新地址。

URL重写可用于添加高值关键字，以改进搜索引擎为产品编制索引的方式。 您还可以使用重写为临时季节性更改或永久更改创建其他URL。 可以为任何有效路径（包括CMS内容页面）创建重写。 在内部，系统始终通过ID引用产品和类别。 无论URL更改的频率如何，ID都保持不变。 以下是您可以使用URL重写的一些方法：

系统URL

    http://www.example.com/catalog/category/id/6

原始URL

    http://www.example.com/peripherals/keyboard.html

重定向的产品URL

    http://www.example.com/ergonomic-keyboard.html

其他类别URL

    http://www.example.com/all-on-sale.html
    http://www.example.com/save-now/spring-sale

![URL重写网格](./assets/url-rewrites.png){width="700" zoomable="yes"}

Commerce提供以下URL重写类型：

* [产品重写](url-rewrite-product.md)
* [类别重写](url-rewrite-category.md)
* [CMS页面重写](url-rewrite-cms-page.md)
* [自定义重写](url-rewrite-custom.md)

## URL重写演示

观看本视频，了解如何管理URL重写：

>[!VIDEO](https://video.tv.adobe.com/v/343751?quality=12&learn=on)

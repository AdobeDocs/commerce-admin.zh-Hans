---
title: 目录和产品URL
description: 了解目录产品的URL格式类型以及如何配置它们。
exl-id: 47405dc6-9b5e-4ca8-87eb-5a222de40793
feature: Catalog Management, Products, Search, Categories
source-git-commit: 1edab49fd8d52a1b7414eb207a21c5c03200e75e
workflow-type: tm+mt
source-wordcount: '909'
ht-degree: 0%

---

# 目录和产品URL

在决定搜索引擎为您的网站编制索引的效果时，分配给产品和类别的URL将发挥重要作用。 在开始构建目录之前，请考虑可用的选项。 要查看当前URL格式，请转到店面并导航到目录中的任何产品。 URL的格式取决于当前配置设置以及用于查找页面的方法。

## URL格式

### 动态URL

动态URL是&#x200B;_动态创建的_，其中可能包含查询字符串，其中包含产品ID、排序顺序以及发出请求的页面的变量。 当客户在您的商店中搜索产品时，生成的URL可能如下所示：

- `http://mystore.com/catalogsearch/result/?q=racer+back`
- `http://mystore.com/women/tops-women.html?style_general=135`

### 静态URL

静态URL是特定页面的固定地址。 静态URL可以显示为搜索引擎友好的格式，也可以按ID引用产品和类别。 这些URL包含人们可能用来查找产品的词语，并需要启用Web服务器重写。 具有静态URL的文件通常用于产品和类别页面、内容页面以及[主题资产](../content-design/theme-assets.md)。

- `http://mystore.com/antonia-racer-tank.html`

## URL组件

### URL键

URL键是描述产品或类别的静态URL的一部分。 创建产品或类别时，将根据名称自动生成初始URL密钥。 要更改URL密钥，请参阅产品信息的[搜索引擎优化](product-search-engine-optimization.md)部分。

>[!NOTE]
>
>默认情况下，带重音符号的特殊字符会在URL键中自动替换为其常规非重音版本。 例如，`ñ`自动替换为`n`。 通过将&#x200B;_[!UICONTROL Search Engine Optimization: Apply transliteration for product URL]_配置选项设置为`No`，可禁用此行为。 请参阅[配置目录URL](#configure-catalog-urls)。

URL键应由小写字符组成，在这些字符之间使用非尾随连字符来分隔单词。 不允许在URL键的开头或结尾使用连字符。 设计良好的“搜索引擎友好”URL键可能包含产品名称和关键字，以改进搜索引擎索引产品的方式。 可以将URL键配置为在URL键发生更改时创建自动重定向。

>[!NOTE]
>
>要扩展URL自定义设置，如本地化的URL，请参阅[URL重写](../merchandising-promotions/url-rewrite.md)以了解更多信息。

### HTML后缀

您的目录可以配置为在类别和产品URL中包含或排除后缀。 人们可能选择使用或忽略后缀的原因有很多。 一些人认为后缀不再有任何用处，并且没有后缀的页面被搜索引擎更有效地索引。 但是，贵公司可能为需要后缀的URL采用了标准化格式。

由于后缀由系统配置控制，因此切勿在类别或产品的URL密钥中直接键入该后缀。 （这样做会导致URL末尾出现双后缀。） 无论您是否决定使用后缀，请保持一致并对所有产品和类别页面使用相同的设置。 以下是带有后缀和不带有后缀的URL示例。

#### 带有HTML后缀的URL

- `http://mystore.com/helena-hooded-fleece.html`
- `http://mystore.com/helena-hooded-fleece.htm`

#### 不带HTML后缀的URL

- `http://mystore.com/helena-hooded-fleece`

### 类别路径

您可以根据自己的偏好将产品URL配置为包含或排除类别路径。 默认情况下，产品URL中不包含类别路径。 但是，嵌套类别将始终在其URL中的店面显示完整的类别路径，以确保类别导航的清晰性和一致性。 以下示例显示了包含和不包含类别路径的相同产品URL。

#### 带类别路径的产品URL

- `http://mystore.com/women/tops-women/hoodies-and-sweatshirts-women/helena-hooded-fleece.html`

#### 没有类别路径的产品URL

- `http://mystore.com/helena-hooded-fleece.html`

要防止搜索引擎索引指向相同内容的多个URL，您可以从URL中排除类别路径。 另一种方法是使用规范元标记让搜索引擎知道要索引的URL和要忽略的URL。 默认情况下，Commerce不在产品URL中包含类别路径。

## 配置目录URL

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧面板中，展开&#x200B;**[!UICONTROL Catalog]**&#x200B;并在下面选择&#x200B;**[!UICONTROL Catalog]**。

1. 展开![扩展选择器](../assets/icon-display-expand.png) **[!UICONTROL Search Engine Optimizations]**&#x200B;部分并设置选项：

   - 将&#x200B;**[!UICONTROL Product URL Suffix]**&#x200B;设置为`html`或`htm`。 输入不带句点的后缀，因为它会自动应用。

   - 将&#x200B;**[!UICONTROL Category URL Suffix]**&#x200B;设置为`html`或`htm`。 输入不带句点的后缀，因为它会自动应用。

   - 将&#x200B;**[!UICONTROL Use Categories Path for Product URLs]**&#x200B;设置为您的首选项。

   ![搜索引擎优化](../configuration-reference/catalog/assets/catalog-search-engine-optimization.png){width="600" zoomable="yes"}

   有关这些选项的详细列表，请参阅&#x200B;_配置引用_&#x200B;中的[搜索引擎优化](../configuration-reference/catalog/catalog.md#search-engine-optimization)。

1. 完成后，单击&#x200B;**[!UICONTROL Save Config]**。

1. 出现提示时，单击系统消息中的&#x200B;**[!UICONTROL Cache Management]**&#x200B;链接并刷新无效缓存。

   ![刷新缓存](./assets/msg-cache-management.png){width="450" zoomable="yes"}

   有关这些选项的更多信息，请参阅[刷新缓存](../systems/cache-management.md#refresh-specific-caches)。

## 配置目录媒体URL格式

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧面板中，展开&#x200B;**[!UICONTROL General]**&#x200B;并选择&#x200B;**[!UICONTROL Web]**。

1. 展开![扩展选择器](../assets/icon-display-expand.png) **[!UICONTROL Url Options]**&#x200B;部分并设置选项：

![Web >常规选项](../configuration-reference/general/assets/web-url-options.png){width="600" zoomable="yes"}

| 字段 | [作用域](../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Add Store Code to URLs] | 全局 | 如果启用了Web服务器重写，则启用此设置会将当前视图的存储代码插入到URL中。 选项： `Yes` / `No` |
| [!UICONTROL Auto-redirect to Base URL] | 全局 | （对于单商店设置）如果您的网站上存在断开的链接，这会将流量重定向到基本URL，而不是重定向到显示“404页面未找到”消息的页面。 选项： `No` / `Yes (302 Found)` / `Yes (301 Moved Permanently)` <br /><br />**_重要信息！_**请勿在多商店设置中使用自动重定向到基本URL。 |
| [!UICONTROL Catalog media URL format] | 全局 | 定义分配给产品和类别的URL格式。 选项： <br />**[!UICONTROL Unique hash per image variant (Legacy mode)]**— 将转换的文件名定义为唯一的哈希值。<br />**[!UICONTROL Image optimization based on query parameters]** — 根据查询参数定义[图像优化](../content-design/media-gallery-image-optimization.md)进程。 |

{style="table-layout:auto"}

---
title: 目录和产品URL
description: 了解目录产品的URL格式类型以及如何配置它们。
exl-id: 47405dc6-9b5e-4ca8-87eb-5a222de40793
feature: Catalog Management, Products, Search, Categories
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '864'
ht-degree: 0%

---

# 目录和产品URL

在决定搜索引擎为您的网站编制索引的效果时，分配给产品和类别的URL将发挥重要作用。 在开始构建目录之前，请考虑可用的选项。 要查看当前URL格式，请转到店面并导航到目录中的任何产品。 URL的格式取决于当前配置设置以及用于查找页面的方法。

## URL格式

### 动态URL

创建动态URL _正在运行_ 并且可能包含一个查询字符串，其中包含产品ID变量、排序顺序变量以及发出请求的页面。 当客户在您的商店中搜索产品时，生成的URL可能如下所示：

- `http://mystore.com/catalogsearch/result/?q=racer+back`
- `http://mystore.com/women/tops-women.html?style_general=135`

### 静态URL

静态URL是特定页面的固定地址。 静态URL可以显示为搜索引擎友好的格式，也可以按ID引用产品和类别。 这些URL包含人们可能用来查找产品的词语，并需要启用Web服务器重写。 具有静态URL的文件通常用于产品和类别页面、内容页面和 [主题资产](../content-design/theme-assets.md).

- `http://mystore.com/antonia-racer-tank.html`

## URL组件

### URL键

URL键是描述产品或类别的静态URL的一部分。 创建产品或类别时，将根据名称自动生成初始URL密钥。 要更改URL键，请参阅 [搜索引擎优化](product-search-engine-optimization.md) 产品信息的部分。

>[!NOTE]
>
>重音特殊字符在URL键中被自动替换为其常规非重音版本。 例如， `ñ` 自动替换为 `n`.

URL键应由小写字符组成，在这些字符之间使用非尾随连字符来分隔单词。 不允许在URL键的开头或结尾使用连字符。 设计良好的“搜索引擎友好”URL键可能包含产品名称和关键字，以改进搜索引擎索引产品的方式。 可以将URL键配置为在URL键发生更改时创建自动重定向。

>[!NOTE]
>
>要扩展URL自定义，例如本地化的URL，请参阅 [URL重写](../merchandising-promotions/url-rewrite.md) 以了解更多信息。

### HTML后缀

您的目录可以配置为在类别和产品URL中包含或排除后缀。 人们可能选择使用或忽略后缀的原因有很多。 一些人认为后缀不再有任何用处，并且没有后缀的页面被搜索引擎更有效地索引。 但是，贵公司可能为需要后缀的URL采用了标准化格式。

由于后缀由系统配置控制，因此切勿在类别或产品的URL密钥中直接键入该后缀。 （这样做会导致URL末尾出现双后缀。） 无论您是否决定使用后缀，请保持一致并对所有产品和类别页面使用相同的设置。 以下是带有后缀和不带有后缀的URL示例。

#### 带HTML后缀的URL

- `http://mystore.com/helena-hooded-fleece.html`
- `http://mystore.com/helena-hooded-fleece.htm`

#### 不带HTML后缀的URL

- `http://mystore.com/helena-hooded-fleece`

### 类别路径

您可以将URL配置为包含或排除类别路径。 默认情况下，类别路径包含在所有类别和产品页面中。 以下示例显示了包含和不包含类别路径的相同产品URL。

#### 具有类别路径的URL

- `http://mystore.com/women/tops-women/hoodies-and-sweatshirts-women/helena-hooded-fleece.html`

#### 没有类别路径的URL

- `http://mystore.com/helena-hooded-fleece.html`

要防止搜索引擎索引指向相同内容的多个URL，您可以从URL中排除类别路径。 另一种方法是使用规范元标记让搜索引擎知道要索引的URL和要忽略的URL。 默认情况下，Commerce不在产品URL中包含类别路径。

## 配置目录URL

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中，展开 **[!UICONTROL Catalog]** 并选择 **[!UICONTROL Catalog]** 下方。

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Search Engine Optimizations]** 并设置以下选项：

   - 设置 **[!UICONTROL Product URL Suffix]** 到 `html` 或 `htm`. 输入不带句点的后缀，因为它会自动应用。

   - 设置 **[!UICONTROL Category URL Suffix]** 到 `html` 或 `htm`. 输入不带句点的后缀，因为它会自动应用。

   - 设置 **[!UICONTROL Use Categories Path for Product URLs]** 按你的喜好去做。

   ![搜索引擎优化](../configuration-reference/catalog/assets/catalog-search-engine-optimization.png){width="600" zoomable="yes"}

   有关这些选项的详细列表，请参阅 [搜索引擎优化](../configuration-reference/catalog/catalog.md#search-engine-optimization) 在 _配置引用_.

1. 完成后，单击 **[!UICONTROL Save Config]**.

1. 出现提示时，单击 **[!UICONTROL Cache Management]** 链接并刷新无效缓存。

   ![刷新缓存](./assets/msg-cache-management.png){width="450" zoomable="yes"}

   有关这些选项的详细信息，请参阅 [刷新缓存](../systems/cache-management.md#refresh-specific-caches).

## 配置目录媒体URL格式

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中，展开 **[!UICONTROL General]** 并选择 **[!UICONTROL Web]**.

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Url Options]** 并设置以下选项：

![Web >常规选项](../configuration-reference/general/assets/web-url-options.png){width="600" zoomable="yes"}

| 字段 | [范围](../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Add Store Code to URLs] | 全局 | 如果启用了Web服务器重写，则启用此设置会将当前视图的存储代码插入到URL中。 选项： `Yes` / `No` |
| [!UICONTROL Auto-redirect to Base URL] | 全局 | （对于单商店设置）如果您的网站上存在断开的链接，这会将流量重定向到基本URL，而不是重定向到显示“404页面未找到”消息的页面。 选项： `No` / `Yes (302 Found)` / `Yes (301 Moved Permanently)` <br /><br />**_重要提示！_**请勿将自动重定向到基本URL用于多存储设置。 |
| [!UICONTROL Catalog media URL format] | 全局 | 定义分配给产品和类别的URL格式。 选项： <br />**[!UICONTROL Unique hash per image variant (Legacy mode)]**— 将转换的文件名定义为唯一的哈希值。<br />**[!UICONTROL Image optimization based on query parameters]**  — 定义 [图像优化](../content-design/media-gallery-image-optimization.md) 根据查询参数进行处理。 |

{style="table-layout:auto"}

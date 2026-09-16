---
title: 搜索词重定向和店面路由
description: 了解如何按部署为Adobe Commerce和Edge Delivery Services选择搜索词重定向、URL重写、Live Search规则或店面路由。
feature: Merchandising, Search
role: Admin, User
level: Intermediate
topic: Commerce, Administration
autotag-review: '2026-09-10T17:42:01.349Z'
TQID: 'https://experienceleague.adobe.com/Vxw3B0zOzLZfAm3qn8gJKHGSNtVhkN2Bfmcauhj0sdM'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
    internal-label: Storefront
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 67a00b294f1946da5795cd8fb7ea9fac1c80edcd
workflow-type: tm+mt
source-wordcount: '970'
ht-degree: 0%
---
# 搜索词重定向和店面路由

搜索词重定向、URL重定向和搜索促销可以解决不同的问题。 使用本指南为由[!DNL Edge Delivery Services]提供支持的标准[!DNL Adobe Commerce]搜索、[!DNL Live Search]和[!DNL Commerce Storefront]选择正确的功能。

## 了解重定向类型

这些功能的不同之处在于，触发行为的内容和购物者看到的内容：

* **搜索词重定向**&#x200B;将输入特定搜索词的购物者发送到指定页面。

* **URL重定向**&#x200B;向新URL发送对旧URL的请求，通常使用HTTP 301或302响应。 浏览器地址栏将更改为新URL。

* **搜索促销**&#x200B;更改了搜索结果中显示的产品或其顺序，但未更改请求的URL。

* **URL重写**&#x200B;将一个URL映射到服务器上的另一个URL。 [!DNL Adobe Commerce] URL重写工具为旧URL创建永久重定向(301)。 有关详细信息，请参阅[URL重写](url-rewrite.md)。

## 选择工艺路线能力

请遵循以下指南来确定符合您要求的功能：

| 要求 | 推荐的功能 |
| --- | --- |
| 将特定查询从标准[!DNL Adobe Commerce]搜索发送到页面 | 在受支持的[管理搜索词](../catalog/search-terms.md)中配置搜索词。 |
| 更改搜索结果中的产品排名或可见性 | 使用[!DNL Live Search] [同义词](https://experienceleague.adobe.com/zh-hans/docs/commerce/live-search/live-search-admin/synonyms/synonyms)或[促销规则](https://experienceleague.adobe.com/zh-hans/docs/commerce/live-search/live-search-admin/rules/rules-add)。 |
| 重定向旧产品、类别或CMS URL | 当适用于您的部署时，请使用Commerce [URL重写](url-rewrite.md)工具。 |
| 重定向[!DNL Edge Delivery Services]路径 | 使用店面或CDN路由。 |
| 店面迁移后保留旧版URL | 创建和测试旧版到新URL重定向映射。 |

## 标准Commerce搜索

通过标准目录搜索，您可以配置搜索词以打开内容页面、类别页面、产品页面或部署支持此功能的外部页面。 当购物者输入的查询（如`gift cards`或`returns`）必须打开促销活动或信息页面时，使用此选项。

若要创建或更新此类型的重定向，请参阅[管理搜索词](../catalog/search-terms.md)。 搜索词配置与URL重写工具不同，因为触发器是购物者的查询，而不是现有URL。

>[!NOTE]
>
>确认店面使用标准目录搜索并支持本机搜索词重定向。 [!DNL Live Search]、[!DNL Adobe Commerce as a Cloud Service]或Headless店面的行为和可用配置可能不同。

## URL重定向和重写

当源是现有URL而不是购物者输入的搜索词时，请使用URL重写。 常见示例包括重定向：

* 旧产品URL到新产品URL。

* 替换类别URL的已停用类别URL。

* 过期的CMS页面URL，指向新的内容页面URL。

对于支持URL重写工具的部署，请转到&#x200B;**[!UICONTROL Marketing]** > **[!UICONTROL SEO & Search]** > **[!UICONTROL URL Rewrites]**&#x200B;以创建重定向。 有关分步指南，请参阅[URL重写](url-rewrite.md)。

>[!NOTE]
>
>[URL重写](url-rewrite.md)主题仅适用于PaaS。 对于[!DNL Adobe Commerce as a Cloud Service]或[!DNL Edge Delivery Services]店面，请改用该店面的路线指南。

## 实时搜索

[!DNL Live Search]替换默认店面搜索体验并提供同义词、彩块化和促销规则等功能。

在需要更改搜索相关性、产品排名或产品可见性时使用[!DNL Live Search]。 当不同的词应返回相似的产品时，请使用同义词。 在必须以不同方式提升、掩埋或排名产品时，应使用促销规则。

不应将[!DNL Live Search]搜索行为视为每个本机Commerce搜索词配置的放置替代行为。 当查询必须导航到内容或活动页面时，在接收请求的店面或边缘路由层中实施重定向。 有关详细信息，请参阅[[!DNL Live Search] 文档](https://experienceleague.adobe.com/zh-hans/docs/commerce/live-search/overview)。

## Edge Delivery Services

对于由[!DNL Edge Delivery Services]提供支持的店面，在店面或边缘路由层中管理重定向。 请勿假设[!DNL Adobe Commerce]管理员URL重写了控制每个请求。

使用文档创作时，在站点的重定向配置中维护重定向映射。 对于在请求到达源之前必须执行的重定向，请使用适当的CDN或边缘配置。 有关相关的SEO指南，请参阅[Commerce店面的SEO指南](https://experienceleague.adobe.com/developer/commerce/storefront/setup/seo/indexing/?lang=zh-Hans)。

## 从Luma迁移

将重定向迁移视为店面迁移的一部分。 保留客户历程和SEO意图，然后为目标店面重新实施路由。

在将流量切换到新店面之前：

1. 导出和清点现有的Luma URL和搜索词登陆页面。

1. 将每个项目分类为搜索词重定向、URL重定向或促销规则。

1. 将每个旧版URL映射到其新店面路径。

1. 在接收请求的层实施每个重定向。

1. 测试状态代码、查询参数、规范URL、区域设置路径和重定向循环。

1. 在启动后监测日志和分析是否存在未解析的旧版URL。

## 重定向疑难解答

当重定向在[!DNL Adobe Commerce]搜索、店面路由和存储视图中的行为与预期不符时，请使用以下检查。

| 问题 | 检查内容 |
| --- | --- |
| 搜索词不会重定向 | 确认店面使用标准目录搜索，搜索查询与配置的搜索词匹配，并且搜索词已分配给正确的店面视图。 如果启用了[!DNL Live Search]，请验证是否已在店面层或边缘层中实施重定向。 |
| 重定向在Luma上不起作用，在Edge Delivery Services上不起作用 | 确认已在[!DNL Edge Delivery Services]店面或CDN路由层中配置重定向。[!DNL Adobe Commerce] 管理员URL重写可能无法收到请求。 |
| Live Search会返回结果而不是重定向 | 使用[!DNL Live Search]规则进行产品排名和可见性。 要导航到内容或营销活动页面，请在店面层或边缘层中配置重定向。 |
| 重定向在一个商店视图中有效，但在另一个商店视图中无效 | 检查分配给搜索词或URL规则的商店视图。 在每个受影响的存储视图中测试完整的区域设置路径和查询。 |

## 有关此主题的更多帮助

* [seo概述和最佳实践](seo-overview.md)

* [店面是什么？](../getting-started/storefront.md)

* [管理搜索词](../catalog/search-terms.md)

* [URL重写](url-rewrite.md)

---
title: 搜索引擎优化
description: 了解适用于Commerce站点的搜索引擎优化(SEO)工具以及实现最佳SEO的最佳实践。
exl-id: ba09159a-1b40-4592-8758-f7072dab4589
feature: Merchandising, Products, Search
TQID: https://experienceleague.adobe.com/cEXR2743G7ZzRSKqb9r344Osipo-R-GlqxNZwC-u-Nk
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 551
ht-degree: 0%

---

# SEO概述

_搜索引擎优化_ (SEO)是微调网站的内容和呈现方式以改进搜索引擎对页面进行索引的方式。 Commerce包含各种功能来支持您持续的SEO工作。

>[!TIP]
>
>对于Adobe Commerce as a Cloud Service，请参阅Commerce Storefront文档中的[SEO准则](https://experienceleague.adobe.com/developer/commerce/storefront/setup/seo/indexing/)

## 元数据

仅[!BADGE PaaS]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="仅适用于云项目（Adobe管理的PaaS基础架构）和内部部署项目上的Adobe Commerce 。"}

了解有关为您的网站和商店添加和增强富含关键字的[元数据](meta-data.md)的详细信息。

## 使用站点地图

仅[!BADGE PaaS]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="仅适用于云项目（Adobe管理的PaaS基础架构）和内部部署项目上的Adobe Commerce 。"}

[站点地图](sitemap-xml.md)改进了搜索引擎对存储进行索引的方式，并设计为查找可能被网页爬虫忽略的页面。 可以将站点地图配置为为所有页面和图像编制索引。

## URL重写

仅[!BADGE PaaS]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="仅适用于云项目（Adobe管理的PaaS基础架构）和内部部署项目上的Adobe Commerce 。"}

通过[URL重写](url-rewrite.md)工具，您可以更改与产品、类别或CMS页面关联的任何URL。

## 搜索引擎机器人

Commerce配置包括用于生成和管理用于为网站编制索引的Web爬虫和机器人的说明的设置。 如果`robots.txt`的请求到达Commerce（而不是物理文件），则会动态路由到robots控制器。 说明是大多数搜索引擎识别和遵循的指令。

默认情况下，Commerce生成的robots.txt文件包含用于Web爬虫的说明，以避免对包含系统内部使用的文件的网站某些部分进行索引。 您可以使用默认设置，或者为所有人或特定搜索引擎定义自己的自定义说明。 网上有许多文章详细探讨了这个主题。

### 自定义说明示例

**允许完全访问**

    用户代理：*
    不允许：

**不允许访问所有文件夹**

    用户代理：*
    不允许： /

**默认指令**

    用户代理： *
    不允许： /index.php/
    不允许： /*?
    不允许： /checkout/
    不允许： /app/
    不允许： /lib/
    不允许： /*.php$
    不允许： /pkginfo/
    不允许： /report/
    不允许： /var/
    不允许： /catalog/
    不允许： /customer/
    不允许： /sendfriend/
    不允许： /review/
    不允许： /*SID=

### 配置`robots.txt`

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**。

1. 在网格的第一行中找到&#x200B;**[!UICONTROL Global]**&#x200B;配置，然后单击&#x200B;**[!UICONTROL Edit]**。

   ![全局设计配置](./assets/design-configuration-grid.png){width="700" zoomable="yes"}

1. 向下滚动并展开![扩展选择器](../assets/icon-display-expand.png) **[!UICONTROL Search Engine Robots]**&#x200B;部分，然后执行以下操作：

   ![设计配置 — 搜索引擎机器人](./assets/design-configuration-search-engine-robots.png){width="600" zoomable="yes"}

   - 将&#x200B;**[!UICONTROL Default Robots]**&#x200B;设置为以下项之一：

     | 选项 | 描述 |
     |------|------------|
     | `INDEX, FOLLOW` | 指示Web爬虫为站点编制索引，并在以后检查是否有更改。 |
     | `NOINDEX, FOLLOW` | 指示Web爬虫避免为网站编制索引，但稍后要检查是否有更改。 |
     | `INDEX, NOFOLLOW` | 指示Web爬虫对网站编制一次索引，但不要关注页面上的任何链接。 |
     | `NOINDEX, NOFOLLOW` | 指示Web爬虫避免为网站编制索引，并且不要关注页面上的任何链接。 |

     {style="table-layout:auto"}

   - 如果需要，请在&#x200B;**[!UICONTROL Edit Custom instruction of robots.txt file]**&#x200B;框中输入自定义说明。 例如，在站点处于开发状态时，您可能希望禁止访问所有文件夹。

   - 若要恢复默认说明，请单击&#x200B;**[!UICONTROL Reset to Default]**。

1. 完成后，单击&#x200B;**[!UICONTROL Save Configuration]**。

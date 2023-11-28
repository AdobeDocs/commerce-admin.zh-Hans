---
title: 搜索引擎优化
description: 了解适用于Commerce网站的搜索引擎优化(SEO)工具以及实现最佳SEO的最佳实践。
exl-id: ba09159a-1b40-4592-8758-f7072dab4589
feature: Merchandising, Products, Search
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '441'
ht-degree: 0%

---

# SEO概述

_搜索引擎优化_ (SEO)是一种微调网站内容和呈现形式的做法，用于改进搜索引擎为页面编制索引的方式。 Commerce包含各种功能来支持您持续的SEO工作。

## 元数据

了解有关添加和增强富含关键词的内容的更多信息 [元数据](meta-data.md) 用于您的网站和商店。

## 使用站点地图

A [网站地图](sitemap-xml.md) 改进了搜索引擎为存储编制索引的方式，并设计为可查找Web爬网程序可能忽略的页面。 可以将站点地图配置为为所有页面和图像编制索引。

## URL重写

此 [URL重写](url-rewrite.md) 工具允许您更改与产品、类别或CMS页面关联的任何URL。

## 搜索引擎机器人

Commerce配置包括用于生成和管理Web爬虫程序以及编制网站索引的机器人的说明的设置。 如果请求 `robots.txt` 到达Commerce（而不是物理文件），它将动态路由到robots控制器。 说明是大多数搜索引擎识别和遵循的指令。

默认情况下，Commerce生成的robots.txt文件包含用于Web Crawler的说明，以避免对包含系统内部使用的文件的网站某些部分进行索引。 您可以使用默认设置，或者为所有人或特定搜索引擎定义自己的自定义说明。 网上有许多文章详细探讨了这个主题。

### 自定义说明示例

**允许完全访问**

    用户代理：*
    不允许：

**禁止访问所有文件夹**

    用户代理：*
    不允许： /

**默认说明**

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

### 配置 `robots.txt`

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. 查找 **[!UICONTROL Global]** 在网格的第一行中配置并单击 **[!UICONTROL Edit]**.

   ![全局设计配置](./assets/design-configuration-grid.png){width="700" zoomable="yes"}

1. 向下滚动并展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Search Engine Robots]** 部分并执行以下操作：

   ![设计配置 — 搜索引擎机器人](./assets/design-configuration-search-engine-robots.png){width="600" zoomable="yes"}

   - 设置 **[!UICONTROL Default Robots]** 更改为以下任一项：

     | 选项 | 描述 |
     |------|------------|
     | `INDEX, FOLLOW` | 指示Web爬网程序为站点编制索引，并在以后检查是否有更改。 |
     | `NOINDEX, FOLLOW` | 指示Web爬网程序避免为站点编制索引，但稍后要检查是否有更改。 |
     | `INDEX, NOFOLLOW` | 指示Web爬网程序对站点编制一次索引，但以后不要检查是否有更改。 |
     | `NOINDEX, NOFOLLOW` | 指示Web爬网程序避免为站点编制索引，并且以后不要回来查看更改。 |

     {style="table-layout:auto"}

   - 如果需要，请在中输入自定义说明 **[!UICONTROL Edit Custom instruction of robots.txt file]** 盒子。 例如，在站点处于开发状态时，您可能希望禁止访问所有文件夹。

   - 要恢复默认说明，请单击 **[!UICONTROL Reset to Default]**.

1. 完成后，单击 **[!UICONTROL Save Configuration]**.

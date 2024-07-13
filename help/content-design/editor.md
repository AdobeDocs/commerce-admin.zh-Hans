---
title: 所见即所得编辑器
description: 了解如何使用编辑器并在_What You See Is What You Get_ (WYSIWYG)视图中处理内容。
exl-id: 209ca9d6-973c-4ad9-b7cd-4fba58dbfbb8
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 0%

---

# 所见即所得编辑器

该编辑器允许您在内容的&#x200B;_所见即所得_ (WYSIWYG)视图中工作时输入和设置格式。 如果您希望直接使用基础HTML代码，则可以轻松更改模式。 编辑器可用于创建[页面](pages.md)、[块](blocks.md)和[产品描述](../catalog/product-content.md)的内容。 处理产品详细信息时，单击&#x200B;**[!UICONTROL Show / Hide Editor]**&#x200B;以访问编辑器。

>[!NOTE]
>
>TinyMCE 5是默认的WYSIWYG编辑器。 对Adobe Commerce和Magento Open Source2.4.5中的TinyMCE 5.10库的更新解决了允许在使用某些类型的URL更新图像或链接时执行任意JavaScript的漏洞。 TinyMCE 3在2.4.0版本中被弃用，在2.4.3版本中被删除。 TinyMCE 4在2.4.4版本中被删除。

![编辑器工具栏](./assets/editor-toolbar.png){width="700" zoomable="yes"}

以下主题提供了有关使用该编辑器的详细信息：

- [插入链接](editor-insert-link.md)
- [插入图像](editor-insert-image.md)
- [插入构件](editor-widget.md)
- [插入变量](editor-insert-variable.md)

## 配置编辑器

所见即所得编辑器默认处于启用状态，可用于编辑CMS页面和块以及产品和类别中的内容。 从配置中，您可以激活或停用编辑器，并选择在产品和类别描述中使用静态而不是[动态](../catalog/catalog-urls.md#dynamic-url)的媒体内容URL。

![WYSIWYG选项](./assets/content-management-wysiwyg-options.png){width="600" zoomable="yes"}

有关所有WYSIWYG选项的详细说明，请参阅&#x200B;_配置引用_&#x200B;中的[内容管理](../configuration-reference/general/content-management.md)。

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧面板中的&#x200B;_[!UICONTROL General]_下，选择&#x200B;**[!UICONTROL Content Management]**。

1. 展开![扩展选择器](../assets/icon-display-expand.png) **[!UICONTROL WYSIWYG Options]**。

1. 将&#x200B;**[!UICONTROL Enable WYSIWYG Editor]**&#x200B;设置为您的首选项。

   默认情况下，该编辑器处于启用状态。

1. 对于使用WYSIWYG编辑器输入的所有[媒体内容](../catalog/catalog-urls.md#static-url)，将&#x200B;**[!UICONTROL Static URLs for Media Content in WYSIWYG]**&#x200B;设置为您的首选项。

1. 完成后，单击&#x200B;**[!UICONTROL Save Config]**。

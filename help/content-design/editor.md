---
title: 所见即所得编辑器
description: 了解如何使用编辑器并在_What You See Is What You Get_ (WYSIWYG)视图中处理内容。
exl-id: 209ca9d6-973c-4ad9-b7cd-4fba58dbfbb8
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 0%

---

# 所见即所得编辑器

利用该编辑器，您可以在中使用时输入和设置格式 _你所见即所得_ （所见即所得）内容视图。 如果您希望直接使用基础HTML代码，则可以轻松更改模式。 编辑器可用于创建内容 [页面](pages.md)， [个块](blocks.md)、和 [产品描述](../catalog/product-content.md). 处理产品详细信息时，单击以访问编辑器 **[!UICONTROL Show / Hide Editor]**.

>[!NOTE]
>
>TinyMCE 5是默认的WYSIWYG编辑器。 对Adobe Commerce和Magento Open Source2.4.5中的TinyMCE 5.10库的更新解决了允许在更新使用某些类型URL的图像或链接时执行任意JavaScript的漏洞。 TinyMCE 3在2.4.0版本中被弃用，在2.4.3版本中被删除。 TinyMCE 4在2.4.4版本中被删除。

![编辑器工具栏](./assets/editor-toolbar.png){width="700" zoomable="yes"}

以下主题提供了有关使用该编辑器的详细信息：

- [插入链接](editor-insert-link.md)
- [插入图像](editor-insert-image.md)
- [插入构件](editor-widget.md)
- [插入变量](editor-insert-variable.md)

## 配置编辑器

所见即所得编辑器默认处于启用状态，可用于编辑CMS页面和块以及产品和类别中的内容。 从配置中，您可以激活或取消激活编辑器，并选择使用静态编辑器，而不是 [动态](../catalog/catalog-urls.md#dynamic-url)、产品和类别描述中媒体内容的URL。

![所见即所得选项](./assets/content-management-wysiwyg-options.png){width="600" zoomable="yes"}

有关所有WYSIWYG选项的详细说明，请参见 [内容管理](../configuration-reference/general/content-management.md) 在 _配置引用_.

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中的 _[!UICONTROL General]_，选择&#x200B;**[!UICONTROL Content Management]**.

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) **[!UICONTROL WYSIWYG Options]**.

1. 设置 **[!UICONTROL Enable WYSIWYG Editor]** 按你的喜好去做。

   默认情况下，该编辑器处于启用状态。

1. 设置 **[!UICONTROL Static URLs for Media Content in WYSIWYG]** 您对所有人的偏好 [媒体内容](../catalog/catalog-urls.md#static-url) 使用WYSIWYG编辑器输入的。

1. 完成后，单击 **[!UICONTROL Save Config]**.

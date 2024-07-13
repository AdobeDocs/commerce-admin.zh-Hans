---
title: 类别 — 内容设置
description: 了解如何使用[!UICONTROL Content]设置来定义类别页面上显示的任何其他内容。
exl-id: 988083e1-0993-4e08-b5e6-8b0855e56467
feature: Catalog Management, Categories, Page Content
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '449'
ht-degree: 0%

---

# 类别 — 内容设置

_[!UICONTROL Content]_设置确定类别页面上出现的任何其他内容。 除了类别产品列表之外，该页面还可以包括图像、描述和CMS块。 您可以使用[[!DNL Page Builder]](../page-builder/introduction.md)内容工具来定义类别描述。

## 在[!DNL Page Builder]中添加类别描述

1. 在编辑模式下打开类别。

1. 向下滚动并展开&#x200B;**[!UICONTROL Content]**&#x200B;部分的![扩展选择器](../assets/icon-display-expand.png)。

   ![类别内容](./assets/category-content.png){width="600" zoomable="yes"}

1. 在&#x200B;**[!UICONTROL Description]**&#x200B;区域的右上方，单击&#x200B;**[!UICONTROL Edit with Page Builder]**。

1. 使用[[!DNL Page Builder]](../page-builder/introduction.md)内容工具[编辑任何现有文本](../page-builder/text.md)并添加其他内容（如果需要）。

## [!DNL Page Builder]预览

当您展开现有类别的&#x200B;_内容_&#x200B;部分时，如果该类别包含使用[!DNL Page Builder]创建的内容，则会显示&#x200B;**[!UICONTROL Description]**&#x200B;内容的预览，就像在类别页面中一样。 单击内容区域可打开[!DNL Page Builder]工作区，您可以在其中进行任何需要的更新。

![描述预览](../page-builder/assets/pb-product-category-content-preview.png){width="500" zoomable="yes"}

默认情况下，产品和类别表单将启用此内容预览。 如果性能因加载预览而受到影响，则可以在[内容管理配置](../configuration-reference/general/content-management.md#advanced-content-tools)设置中禁用预览。

## 在编辑器中添加类别说明

在文本框中只输入纯ASCII字符。 如果从文字处理器粘贴文本，请首先将其保存为纯.TXT文件，以删除任何不可见的控制字符。

有关详细信息，请参阅[WYSIWYG编辑器](../content-design/editor.md)。

1. 在编辑模式下打开类别。

1. 向下滚动并展开&#x200B;**[!UICONTROL Content]**&#x200B;部分的![扩展选择器](../assets/icon-display-expand.png)。

   ![类别内容](./assets/category-content-ce.png){width="500" zoomable="yes"}

1. 输入类别&#x200B;**[!UICONTROL Description]**&#x200B;并根据需要使用[编辑器工具栏](../content-design/editor.md)设置格式。

   您可以拖动右下角来更改文本框的高度。

## 将CMS块添加到类别页面

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Catalog]** > **[!UICONTROL Categories]**。

1. 在类别树中，选择要编辑的类别。

1. 展开&#x200B;**[!UICONTROL Content]**&#x200B;部分的![扩展选择器](../assets/icon-display-expand.png)。

1. 对于&#x200B;**[!UICONTROL Add the CMS block]**，请选择要添加的块。

1. 展开&#x200B;**[!UICONTROL Display Settings]**&#x200B;部分的![扩展选择器](../assets/icon-display-expand.png)。

1. 将&#x200B;**[!UICONTROL Display Mode]**&#x200B;设置为以下项之一：

   - `Static block only`
   - `Static block and products`

1. 完成后，单击&#x200B;**[!UICONTROL Save]**&#x200B;并查看店面上的块显示（需要缓存刷新）。

## 内容设置参考

| 设置 | [作用域](../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Category Image] | 商店视图 | 指定类别页面顶部的图像。 方法： <br/><br/>**[!UICONTROL Upload]**— 将图像文件从本地计算机上载到图库，并将其用作类别图像。<br/><br/>**[!UICONTROL Select from Gallery]** — 提示您从图片库中选择现有图像。 <br/><br/>![Page Builder相机图标](../assets/icon-camera.png) — 将图像文件拖到相机磁贴上，或浏览到图像并从本地文件系统选择它。 |
| [!UICONTROL Description] | 商店视图 | 指定类别页上显示的说明。 <br/><br/>**[!UICONTROL Edit with Page Builder]**— 打开[[!DNL Page Builder] 工作区](../page-builder/workspace.md)，您可以在其中编辑描述。<br/><br/>**[!UICONTROL Show / Hide Editor]** — 在WYSIWYG编辑器和HTML模式之间切换显示。 |
| [!UICONTROL Add CMS Block] | 商店视图 | 将现有[CMS块](../content-design/blocks.md)添加到类别页。 |

{style="table-layout:auto"}

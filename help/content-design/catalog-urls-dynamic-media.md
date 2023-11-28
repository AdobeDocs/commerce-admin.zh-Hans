---
title: Dynamic media URL
description: 了解如何使用Dynamic Media URL作为图像或其他媒体资源的相对引用。
exl-id: 41aabde2-f6cc-4b83-8d56-9753a7aa93e9
feature: CMS, Media
source-git-commit: d3b9b4cd0d12f8d5feb2bad0bf601970f9ee1a36
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 0%

---

# Dynamic media URL

Dynamic Media URL是对图像或其他媒体资源的相对引用。 启用后，可以使用Dynamic Media URL直接链接到服务器上的资产或存储在上的文件。 [内容分发网络](media-storage-content-delivery-network.md). 使用Dynamic Media URL可能会影响目录性能，并且 [编辑者](editor.md#configure-the-editor) 可以配置为使用静态或动态媒体URL。

与所有项目一样 [标记标签](../systems/markup-tags.md)，则指令将用双大括号括起来。 Dynamic Media URL的格式如下所示：

`\{\{media url="path/to/image.jpg"}}`

在店面中呈现页面时，将从保存的HTML内容处理动态URL指令。 每次呈现页面时，都会扫描内容以查找 `\{\{media url="..."}}` 并且每个指令都会替换为相应的媒体URL。

{{$include /help/_includes/directives-caution.md}}

## 配置静态媒体URL

默认情况下，从WYSIWYG编辑器插入到目录中的图像具有相对的动态URL。 如果您希望使用静态URL，可以更改配置设置。

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中的 _[!UICONTROL General]_，选择&#x200B;**[!UICONTROL Content Management]**.

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL WYSIWYG Options]** 部分。

   ![所见即所得选项](./assets/content-management-wysiwyg-options.png){width="600" zoomable="yes"}

1. 设置 **[!UICONTROL Use Static URLs for Media Content in WYSIWYG]** 更改为以下任一项：

   - `Yes`  — 对通过WYSIWYG编辑器插入的媒体内容使用静态URL。 静态URL为绝对路径，如果 [基本URL](../stores-purchase/store-urls.md) ，表示存储区发生了更改。

   - `No`  — （默认）对通过WYSIWYG编辑器插入的媒体内容使用动态URL，根据 `\{\{media url="..."}}` 指令。 动态URL是相对的，如果商店的基本URL发生更改，则不会中断。

1. 完成后，单击 **[!UICONTROL Save Config]**.

---
title: Dynamic media URL
description: 了解如何使用Dynamic Media URL作为图像或其他媒体资源的相对引用。
exl-id: 41aabde2-f6cc-4b83-8d56-9753a7aa93e9
feature: CMS, Media
badgePaas: label="仅限PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="仅适用于云项目(Adobe管理的PaaS基础架构)和内部部署项目上的Adobe Commerce 。"
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 0%

---

# Dynamic media URL

Dynamic Media URL是对图像或其他媒体资源的相对引用。 启用后，Dynamic Media URL可用于直接链接到服务器上的资产或存储在[内容交付网络](media-storage-content-delivery-network.md)上的文件。 使用Dynamic Media URL可能会影响目录性能，可以将[编辑器](editor.md#configure-the-editor)配置为使用静态或Dynamic Media URL。

与所有[标记标记](../systems/markup-tags.md)一样，指令用双大括号括起来。 Dynamic Media URL的格式如下所示：

`\{\{media url="path/to/image.jpg"}}`

在店面中呈现页面时，将从保存的HTML内容处理动态URL指令。 每次呈现页面时，都会扫描内容`\{\{media url="..."}}`，并且每个指令都会替换为相应的媒体URL。

{{$include /help/_includes/directives-caution.md}}

## 配置静态媒体URL

默认情况下，从WYSIWYG编辑器插入到目录中的图像具有相对的动态URL。 如果您希望使用静态URL，可以更改配置设置。

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧面板中的&#x200B;_[!UICONTROL General]_&#x200B;下，选择&#x200B;**[!UICONTROL Content Management]**。

1. 展开&#x200B;**[!UICONTROL WYSIWYG Options]**&#x200B;部分的![扩展选择器](../assets/icon-display-expand.png)。

   ![WYSIWYG选项](./assets/content-management-wysiwyg-options.png){width="600" zoomable="yes"}

1. 将&#x200B;**[!UICONTROL Use Static URLs for Media Content in WYSIWYG]**&#x200B;设置为以下项之一：

   - `Yes` — 对使用WYSIWYG编辑器插入的媒体内容使用静态URL。 静态URL是绝对的，如果存储区的[基本URL](../stores-purchase/store-urls.md)发生更改，则会中断。

   - `No` — （默认）根据`\{\{media url="..."}}`指令，对通过WYSIWYG编辑器插入的媒体内容使用动态URL。 动态URL是相对的，如果商店的基本URL发生更改，则不会中断。

1. 完成后，单击&#x200B;**[!UICONTROL Save Config]**。

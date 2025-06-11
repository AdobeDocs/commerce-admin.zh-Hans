---
title: 媒体集图像优化
description: 了解如何对 [!DNL Commerce] 媒体资源使用图像优化。
exl-id: ba75e90a-406b-4b14-b049-0b78c4a27188
feature: Page Content, Media
badgePaas: label="仅限PaaS" type="Informative" url="https://experienceleague.adobe.com/zh-hans/docs/commerce/user-guides/product-solutions" tooltip="仅适用于云项目(Adobe管理的PaaS基础架构)和内部部署项目上的Adobe Commerce 。"
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 0%

---

# 媒体集图像优化

新[媒体集](media-gallery.md)提供了&#x200B;_图像优化_&#x200B;功能，该功能可提高性能并降低店面上的媒体文件大小。 此优化默认处于启用状态，并可在存储配置设置中进行修改。

## 配置图像优化

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧面板中，展开&#x200B;**[!UICONTROL Advanced]**&#x200B;并选择&#x200B;**[!UICONTROL System]**。

1. 展开![扩展选择器](../assets/icon-display-expand.png) **[!UICONTROL Media Gallery Image Optimization]**&#x200B;并执行以下操作：

   - 将&#x200B;**[!UICONTROL Enable Image Optimization]**&#x200B;设置为`Yes`。
   - 根据需要输入&#x200B;**[!UICONTROL Maximum Width]**&#x200B;和&#x200B;**[!UICONTROL Maximum Height]**&#x200B;值（以像素为单位）。

## 行为

启用媒体集图像优化功能后，会自动将图像的优化副本插入[媒体集](media-gallery.md)中的内容，而不是原始文件。

当配置中的&#x200B;_最大宽度_&#x200B;和&#x200B;_最大高度_&#x200B;值更改时，它会更新之前插入的所有现有优化图像。

媒体集图像优化要求在配置更改时运行`media.gallery.renditions.update`队列使用者以重新生成优化图像。 有关详细信息，请参阅&#x200B;_配置指南_&#x200B;中的[管理消息队列](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html?lang=zh-Hans)。

{{$include /help/_includes/image-optimization-animated-gif-note.md}}

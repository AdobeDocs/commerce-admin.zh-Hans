---
title: 此 [!DNL Media Gallery]
description: 使用介质集来组织和管理服务器上的介质文件。
exl-id: bf730e46-70f3-405c-88cf-62d0a3e8634f
feature: Page Content, Media
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 0%

---

# 此 [!DNL Media Gallery]

借助Adobe Commerce或Magento Open Source 2.4，商家可以使用新的 _增强型_ [!DNL Media Gallery] 组织和管理服务器上的介质文件。 此新 [!DNL Media Gallery] 包含与现有媒体存储相同的功能，但包含改进的用户界面和与的更紧密集成 [Adobe Stock][adobe-stock].

![媒体集网格中显示的图像](./assets/media-gallery-grid.png){width="700" zoomable="yes"}

>[!NOTE]
>
>产品图像已添加到 [_[!UICONTROL Images and Videos]_产品区域](../catalog/product-image.md#upload-an-image) 不受管理 [!DNL Media Gallery]. 仅限中使用的图像_[!UICONTROL Content]_ 产品部分字段在新字段中显示和过滤 [!DNL Media Gallery].

## 启用新的 [!DNL Media Gallery]

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中，展开 **[!UICONTROL Advanced]** 并选择 **[!UICONTROL System]**.

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) **[!UICONTROL Media Gallery]**.

   ![高级配置 —  [!DNL Media Gallery]](./assets/system-media-gallery.png){width="600" zoomable="yes"}

1. 设置 **[!UICONTROL Enable Old Media Gallery]** 到 `No`.

1. 单击 **[!UICONTROL Save Config]**.

1. 出现提示时，单击 **[!UICONTROL Cache Management]** 链接并刷新无效缓存。

   此 [[!UICONTROL Content] 菜单](/help/content-design/content-menu.md) 现在显示新的 _[!UICONTROL Media Gallery]_选项。

>[!NOTE]
>
>新增的完整功能 [!DNL Media Gallery] 需要 `media.gallery.synchronization` 和 `media.content.synchronization` 为初始同步而启动的队列使用者。 请参阅 [管理消息队列](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html) 在 _配置指南_ 以了解更多详细信息。

## 访问新的 [!DNL Media Gallery]

新 [!DNL Media Gallery] 可从“内容”菜单访问，或在 [添加或编辑页面](/help/content-design/page-add.md). 您还可以在以下情况下访问它： [创建或编辑类别](/help/catalog/category-create.md)，或当您 [使用内容编辑器插入图像](/help/content-design/editor-insert-image.md).

要访问新的 [!UICONTROL Media Gallery] 通过 [!UICONTROL Content] 菜单：

- 在 _管理员_ 侧栏，转到 **[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**.

要在添加或编辑页面时访问新的媒体集，请执行以下操作：

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. 单击 **[!UICONTROL Add a New Page]**.

   如果要编辑现有页面，可以使用 _[!UICONTROL Action]_要单击的列&#x200B;**[!UICONTROL Select]**并选择&#x200B;**[!UICONTROL Edit]**.

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Content]** 部分并执行以下操作：

   - 如果您拥有 [已启用页面生成器](../page-builder/setup.md)，展开 **[!UICONTROL Media]** 面板并拖动 **[!UICONTROL Image]** 目标容器的占位符。 然后单击 **[!UICONTROL Select from Gallery]**.

     ![将图像拖到舞台上](./assets/pb-media-image-drag.png){width="600" zoomable="yes"}

   - 如果您拥有 [已启用WYSIWYG编辑器](/help/content-design/editor.md)，单击 **[!UICONTROL Show/Hide Editor]** 然后单击 **[!UICONTROL Insert Image]**.

## [!DNL Media Gallery] 演示

要了解有关 [!DNL Media Gallery]，请观看此视频：

>[!VIDEO](https://video.tv.adobe.com/v/343785?quality=12)

[adobe-stock]: https://stock.adobe.com


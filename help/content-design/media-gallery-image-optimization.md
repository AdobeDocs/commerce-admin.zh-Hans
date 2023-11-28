---
title: 媒体集图像优化
description: 了解如何为您的使用图像优化 [!DNL Commerce] 媒体资产。
exl-id: ba75e90a-406b-4b14-b049-0b78c4a27188
feature: Page Content, Media
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 0%

---

# 媒体集图像优化

新 [媒体集](media-gallery.md) 提供 _图像优化_ 功能，可提高性能并减小店面上的媒体文件大小。 此优化默认处于启用状态，并可在存储配置设置中进行修改。

## 配置图像优化

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中，展开 **[!UICONTROL Advanced]** 并选择 **[!UICONTROL System]**.

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) **[!UICONTROL Media Gallery Image Optimization]** 并执行以下操作：

   - 设置 **[!UICONTROL Enable Image Optimization]** 到 `Yes`.
   - 输入 **[!UICONTROL Maximum Width]** 和 **[!UICONTROL Maximum Height]** 个值（以像素为单位）。

## 行为

启用“媒体集”图像优化功能后，图像的优化副本会自动插入到中的内容中。 [媒体集](media-gallery.md) 而不是原始文件。

当 _最大宽度_ 和 _最大高度_ 值在配置中发生更改，它会更新之前插入的所有现有优化图像。

媒体集图像优化要求 `media.gallery.renditions.update` 当配置更改时，队列使用者正在运行以重新生成优化映像。 请参阅 [管理消息队列](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html) 在 _配置指南_ 以了解更多详细信息。

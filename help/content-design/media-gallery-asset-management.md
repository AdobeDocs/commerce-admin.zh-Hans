---
title: 媒体集资产管理
description: 了解如何管理已上传的媒体文件以及通过Adobe Stock集成获取的资源。
exl-id: 4fc489ae-b1e5-4aa4-832d-cd88c58d103a
feature: Page Content, Media
source-git-commit: a93e96353f4be0e771064cdcfbdf794772386a28
workflow-type: tm+mt
source-wordcount: '475'
ht-degree: 0%

---

# 媒体集资产管理

新的[媒体集](media-gallery.md)提供了用于管理已上传媒体文件的工具，以及通过[Adobe Stock集成](adobe-stock.md)获取的资源。 如果您已保存Adobe Stock [图像预览](adobe-stock-save-preview.md)，则还可以[许可](adobe-stock-license-image.md)新媒体集中的图像。

## 上传资源

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**。

1. 单击&#x200B;**[!UICONTROL Upload Image]**。

1. 选择要上传的文件。

   所选资产会自动上传到所选文件夹（如果未选择文件夹，则上传到存储根目录）。

## 查看资源详细信息

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**。

1. 单击资产下方的三个圆点（![详细信息图标](./assets/media-gallery-asset-menu-icon.png){width="10" zoomable="no"}），然后单击&#x200B;**[!UICONTROL View Details]**。

   ![资源操作](./assets/media-gallery-asset-actions.png){width="600" zoomable="yes"}

   资产详细信息会显示在幻灯片面板上。 其中包括正在使用资产的信息：

   - **[!UICONTROL Categories]**
   - **[!UICONTROL Products]**
   - **[!UICONTROL Pages]**
   - **[!UICONTROL Blocks]**

   ![资源详细信息](./assets/media-gallery-asset-details.png){width="600" zoomable="yes"}

   要查看详细信息，请单击&#x200B;**[!UICONTROL Used In]**&#x200B;链接。 以下示例中的网格显示了使用特定资产的所有类别。

   ![类别网格](./assets/media-gallery-asset-categories.png){width="600" zoomable="yes"}

   也可以从&#x200B;_查看详细信息_&#x200B;部分删除资产。

## 编辑资源

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**。

1. 单击资产下方的三个圆点（![资产菜单图标](./assets/media-gallery-asset-menu-icon.png){width="10" zoomable="no"}），然后单击&#x200B;**[!UICONTROL Edit]**。

   ![编辑资产](./assets/media-gallery-edit-asset.png){width="600" zoomable="yes"}

1. 如果需要，请更改以下元数据值之一：

   - **[!UICONTROL Title]**
   - **[!UICONTROL Description]**
   - **[!UICONTROL Tags/Keywords]**

   此数据将保存到数据库以及文件元数据本身。 目前，支持XMP和IPTC格式。

   您可以下载包含更新后元数据的图像。

## 使用资源

Assets在整个管理员中都可以广泛使用，例如[添加或编辑页面](page-add.md)、[创建或编辑类别](../catalog/category-create.md)或者从内容编辑器[插入图像](editor-insert-image.md)。

1. 从允许您使用媒体资产的区域访问新的媒体集。

1. 选择资产并单击&#x200B;**[!UICONTROL Add Selected]**。

{{$include /help/_includes/image-optimization-animated-gif-note.md}}

## 删除资源

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**。

1. 单击&#x200B;**[!UICONTROL Delete Images...]**，然后选中要删除的每个资产的复选框。

1. 在确认对话框中，单击&#x200B;**[!UICONTROL Delete Image]**。

   ![删除确认](./assets/media-gallery-bulk-delete-confirm.png){width="500" zoomable="yes"}

## 搜索资产

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**。

1. 使用&#x200B;**[!UICONTROL Search by keywords]**&#x200B;输入按关键字/标记执行图像搜索。

   以下示例中的搜索将查找包含特定标记(`mountain`)的资源。

   ![资源搜索](./assets/media-gallery-asset-search.png){width="600" zoomable="yes"}

>[!NOTE]
>
>要了解如何更新图像标记，请参阅&#x200B;_[编辑资产](#edit-an-asset)_&#x200B;部分。

## 筛选资产

>[!NOTE]
>
>_用于_&#x200B;的功能要求在[配置设置](media-gallery-image-optimization.md)中启用[!UICONTROL Media Gallery Image Optimization]。

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**。

1. 单击&#x200B;**[!UICONTROL Filters]**&#x200B;选项卡。

   ![筛选器](./assets/media-gallery-filters.png){width="600" zoomable="yes"}

1. 设置筛选选项。

   您可以根据实体的使用情况筛选资源：

   - **[!UICONTROL Used in Categories]**
   - **[!UICONTROL Used in Products]**
   - **[!UICONTROL Used in Pages]**
   - **[!UICONTROL Used in Blocks]**

   您还可以按&#x200B;**[!UICONTROL Store View]**、**[!UICONTROL License Status]**&#x200B;和&#x200B;**[!UICONTROL Content Status]**&#x200B;筛选资源。 设置&#x200B;**[!UICONTROL Uploaded Date]**&#x200B;和/或&#x200B;**[!UICONTROL Modification Date]**&#x200B;的日期范围，以根据文件日期筛选资源。

1. 单击&#x200B;**[!UICONTROL Apply Filters]**&#x200B;查看结果。

   以下示例中的筛选功能查找在特定类别(`cars`)中使用且已启用的资产。

   ![按类别筛选已启用的Assets](./assets/media-gallery-filter-by-category.png){width="600" zoomable="yes"}

## 查找图像重复项

1. 单击&#x200B;**[!UICONTROL Filters]**&#x200B;选项卡并选择&#x200B;**[!UICONTROL Show duplicates]**&#x200B;复选框。

1. 若要查看结果，请单击&#x200B;**[!UICONTROL Apply Filters]**。

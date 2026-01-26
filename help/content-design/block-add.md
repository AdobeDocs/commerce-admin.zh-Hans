---
title: 添加内容块
description: 创建可在任何页面或其他块中重复使用的自定义内容块。
exl-id: 2f104d77-a1d1-4f10-82ce-014955fe560b
badgePaas: label="仅限PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="仅适用于云项目(Adobe管理的PaaS基础架构)和内部部署项目上的Adobe Commerce 。"
source-git-commit: cace9d1de00955494d8bc607c017778ff7df4806
workflow-type: tm+mt
source-wordcount: '536'
ht-degree: 0%

---

# 添加内容块

可以创建自定义的内容块，然后将其添加到任何页面、页面组，甚至添加到另一个块。 例如，您可以将图像滑块放置在块中，然后将该块放置在主页上。 块工作区使用与[Pages](pages-workspace.md)工作区相同的&#x200B;_基本控件_&#x200B;来帮助您查找可用块并执行日常维护。 块完成后，您可以使用[构件](widget-static-block.md)工具将其放在商店中的特定页面上。

![“块”页显示现有块的网格](./assets/blocks-workspace.png){width="700" zoomable="yes"}

## 创建块

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Blocks]**。

1. 单击右上角的&#x200B;**添加新块**。

   ![新块页面显示选项和内容空间](./assets/block-detail.png){width="500" zoomable="yes"}

1. 如果要更改新块的默认启用状态，请将&#x200B;**启用块**&#x200B;设置为`No`。

1. 分配&#x200B;**块标题**&#x200B;以供内部引用。

1. 为块分配唯一的&#x200B;**标识符**。

   使用带下划线的所有小写字符而不是空格。

1. 选择您希望块可用的每个&#x200B;**[!UICONTROL Store View]**。

1. 使用显示的内容工具集添加块的内容：

   - 如果启用了[页面生成器](../page-builder/introduction.md)，请选择&#x200B;**[!UICONTROL Edit with Page Builder]**&#x200B;以在内容[工作区](../page-builder/workspace.md)中使用页面生成器工具。

     ![页面生成器工作区](./assets/pb-workspace-block.png){width="500" zoomable="yes"}

     >[!NOTE]
     >
     >有关使用页面生成器添加块的信息，请参阅[教程2：块](../page-builder/2-blocks.md)。

   - 使用[编辑器](editor.md)设置文本格式、创建链接以及添加表、图像、视频和音频。

     如果您希望使用HTML代码，请单击&#x200B;**显示/隐藏编辑器**。

     ![块编辑器（隐藏）](./assets/block-editor-hidden.png){width="500" zoomable="yes"}

1. 完成后，单击&#x200B;**[!UICONTROL Save]**&#x200B;箭头并选择&#x200B;**[!UICONTROL Save & Close]**。

   新块将显示在“块”网格的列表底部。

1. 使用[小组件](widget-static-block.md)工具将完成的块放在商店中的特定页面上。

## 删除块

有两种方法可删除自定义块。 您可以将其从&#x200B;_块_&#x200B;网格或编辑块页面中删除。

### 方法1：从块网格中删除块

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Blocks]**。
1. 使用网格上方的筛选器找到块，并选中要删除的一个或多个块的复选框。
1. 在列表的左上角，将&#x200B;**[!UICONTROL Actions]**&#x200B;设置为`Delete`。
1. 要确认操作，请单击&#x200B;**[!UICONTROL OK]**。

### 方法2：从编辑页面中删除块

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Blocks]**。
1. 查找要删除的块。
1. 在块的&#x200B;_操作_&#x200B;列中，单击&#x200B;**[!UICONTROL Select]**&#x200B;并选择&#x200B;**[!UICONTROL Edit]**。
1. 在菜单栏中，单击&#x200B;**[!UICONTROL Delete Block]**。
1. 要确认操作，请单击&#x200B;**[!UICONTROL OK]**。

## 保存菜单

| 命令 | 描述 |
|----------|----------- |
| [!UICONTROL Save] | 保存当前块并继续工作。 |
| [!UICONTROL Save & Duplicate] | 保存并关闭当前块，然后打开新的重复副本。 |
| [!UICONTROL Save & Close] | 保存并关闭当前块，然后返回到块网格。 |

{style="table-layout:auto"}

## 添加灯箱或滑块

- 通过[可以轻松将](../page-builder/slider.md)滑块[[!DNL Page Builder]](../page-builder/introduction.md)添加到您的商店。 可以将滑块设置为自动播放，或使用导航按钮手动控制。

  ![页面生成器滑块](./assets/pb-tutorial3-slider-tee-shirt-promo.png){width="600" zoomable="yes"}

  [[!DNL Commerce Marketplace]](https://marketplace.magento.com/extensions.html?q=lightbox)上也有各种基于jQuery的图像灯箱，有些是免费的。

- 您还可以从[!DNL Commerce Marketplace]下载扩展。 有关其他帮助，请参阅扩展开发人员提供的文档。

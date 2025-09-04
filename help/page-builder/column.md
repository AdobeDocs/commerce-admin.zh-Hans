---
title: 布局 — 列
description: 了解“列”内容类型，该内容类型用于将页面在 [!DNL Page Builder] 阶段划分为多个列。
exl-id: 9701e1b5-3584-4602-9512-051567274f21
feature: Page Builder, Page Content
source-git-commit: 4a3aa2aa32b692341edabd41fdb608e3cff5d8e0
workflow-type: tm+mt
source-wordcount: '1574'
ht-degree: 0%

---

# 布局 — 列

使用&#x200B;_Column_&#x200B;内容类型在[[!DNL Page Builder] 阶段](workspace.md#stage)中将页面划分为多个列。 将列添加到行或选项卡或直接添加到舞台时，列组最初会被分为两列，两列的宽度相等。 您可以根据需要添加或删除列。 可通过拖动两列之间的边框来调整列的大小。 将调整下一列的宽度以填充行、选项卡或舞台中的可用空间。 单列可延伸舞台或其容器的整个宽度。

![添加列](./assets/pb-layout-column-add-drag-placeholder.png){width="600" zoomable="yes"}

{{$include /help/_includes/page-builder-save-timeout.md}}

## 2.4.5版本中的更新

2.4.5版本中更新了页面生成器功能，以便用户现在使用&#x200B;_[!DNL Columns]_&#x200B;作为各个列的父容器。 此新容器还支持背景属性，并且无需将列换行。 它减少了不必要的标记，并对店面显示和体验提供了更精细的控制。

您可以更改[!DNL Columns]容器的布局，方法是在组中其他列的上方或下方拖动一列，然后栈叠这些列。 这打开了各种新的可能布局组合，无需开发人员自定义即可实现这些组合。

观看本视频，了解如何使用[!DNL Columns]容器优化页面布局：

>[!VIDEO](https://video.tv.adobe.com/v/345828?quality=12&learn=on)

## 列工具箱

每列都有一个选项工具箱，当您将鼠标悬停在该容器上时，将会显示这些选项。

| 工具 | 图标 | 描述 |
|--- |--- |--- |
| 移动 | ![移动图标](./assets/pb-icon-move.png){width="25"} | 将列及其内容移动到相对于其他列的另一个位置。 |
| （标签） | 列 | 将当前容器标识为列。 将鼠标悬停在列容器上以显示工具箱。 |
| 设置 | ![设置图标](./assets/pb-icon-settings.png){width="25"} | 打开“编辑列”页，在该页中可以更改容器的属性。 |
| 复制 | ![图标重复](./assets/pb-icon-duplicate.png){width="25"} | 生成当前列的副本。 |
| 移除 | ![删除图标](./assets/pb-icon-remove.png){width="25"} | 删除当前列及其内容。 |

{style="table-layout:auto"}

## 列网格

[网格](workspace.md)可确保内容在列中保持一致，并帮助页面在桌面和移动设备上正确呈现。 有关详细信息，请参阅[配置的](setup.md)高级内容工具[!DNL Page Builder]部分。

![具有一列的行上的网格分区](./assets/pb-layout-column-one-grid.png){width="500" zoomable="yes"}

在以下两列示例中，每个列容器顶部边框的圆括号(6/12)中的数字表示每列的网格划分数以及划分总数。 在本例中，该列是总共12个网格单位中的6个网格单位的宽度。

![具有两列的行上的网格分区](./assets/pb-layout-column-two-grid.png){width="600" zoomable="yes"}

## 添加列

1. 在[!DNL Page Builder]下的&#x200B;_[!UICONTROL Layout]_&#x200B;面板中，将&#x200B;**[!UICONTROL Column]**&#x200B;拖到舞台上。

   ![将列拖到舞台上](./assets/pb-layout-column-add-drag-placeholder.png){width="600" zoomable="yes"}

   列组现在分为两列，两列的宽度相等。 每列都是一个单独的内容容器，并且有自己的一组工具箱选项。

   ![两个相等的列](./assets/pb-layout-columns-two-empty.png){width="600" zoomable="yes"}

1. 在列组的左上角，单击&#x200B;_网格_&#x200B;工具（![网格控件](./assets/pb-icon-grid-control.png)）并根据需要调整网格大小。

   将内容放在网格上有助于使内容保持一致，并在桌面和移动设备上正确呈现页面。 有关详细信息，请参阅[配置的](../configuration-reference/general/content-management.md)高级内容工具[!DNL Page Builder]部分。

   ![两列上的网格分区](./assets/pb-layout-column-two-grid.png){width="600" zoomable="yes"}

## 调整列大小

1. 将鼠标悬停在两列之间的边框上。

   边框加亮，选定列的工具箱出现。

   ![高亮显示两列之间的边框](./assets/pb-column-resize-border.png){width="600" zoomable="yes"}

1. 按住鼠标按钮以显示网格，并将边框拖到网格上的新位置。

   两列的宽度会调整以反映更改。 每列的新宽度显示在标签之后，如`4/12` （12个中的4个）和`8/12` （12个中的8个）。

   ![调整了列大小](./assets/pb-columns-resized-grid.png){width="600" zoomable="yes"}

## 删除列

1. 将鼠标悬停在要删除的列上以显示工具箱，然后选择&#x200B;_删除_ （![删除图标](./assets/pb-icon-remove.png){width="20"} ）图标。

   ![列工具箱](./assets/pb-column-toolbox-remove.png){width="600" zoomable="yes"}

1. 如果该列包含内容，请单击&#x200B;**[!UICONTROL OK]**&#x200B;进行确认。

   若要在将来加速此过程，您可以通过选中&#x200B;**[!UICONTROL Do not show this again]**&#x200B;复选框跳过确认步骤。

   列组现在具有单个列(12/12)和网格。 由于网格仅对列可用，因此可以使用此技术来显示网格。

   ![带有网格的单列](./assets/pb-column-single-grid.png){width="600" zoomable="yes"}

1. 如果希望列组将剩余列扩展为行或舞台的完整宽度：

   - 将鼠标悬停在该列上以显示工具箱，然后选择&#x200B;_设置_ （ ![设置图标](./assets/pb-icon-settings.png){width="20"} ）图标。

   - 向下滚动到&#x200B;_[!UICONTROL Advanced]_&#x200B;部分，并将所有四个&#x200B;**[!UICONTROL Padding]**&#x200B;值设置为`0`。

     ![使用零内边距](./assets/pb-tutorial1-row-settings-advanced-margins-padding-zero.png){width="600" zoomable="yes"}

   - 单击右上角的&#x200B;**[!UICONTROL Save]**&#x200B;以关闭&#x200B;_[!UICONTROL Edit Column]_&#x200B;页面。

1. 单击工作区右上角的&#x200B;_关闭全屏_（![关闭全屏图标](./assets/pb-icon-reduce.png){width="20"}）图标，然后单击右上角的&#x200B;**[!UICONTROL Save]**。

## 更改列设置

1. 将鼠标悬停在该列上以显示工具箱，然后选择&#x200B;_设置_ （ ![设置图标](./assets/pb-icon-settings.png){width="20"} ）图标。

   ![列工具箱](./assets/pb-column-toolbox-settings.png){width="600" zoomable="yes"}

1. 根据需要更改&#x200B;**[!UICONTROL Appearance]**&#x200B;设置。

   - 选择用于确定列相对于其容器的位置的对齐设置。

     | 选项 | 描述 |
     | ------ | ----------- |
     | `Full Height` | 列会扩展其容器的完整高度。 |
     | `Top Aligned` | 列将在其容器顶部对齐。 |
     | `Centered` | 列居中在其容器中间。 |
     | `Bottom Aligned` | 该列在其容器底部对齐。 |

     {style="table-layout:auto"}

   - 如果需要，请为该列输入&#x200B;**[!UICONTROL Minimum Height]**。 例如，可以设置最小高度以匹配背景图像的高度。

   - 如果设置了最小高度，请设置&#x200B;**[!UICONTROL Vertical Alignment]**&#x200B;以控制添加到列（`Top`、`Center`或`Bottom`）的内容容器的位置。

1. 更改列内容的背景。

   - **[!UICONTROL Background Color]** — 通过选择色板、单击拾色器或输入有效的颜色名称或等效的十六进制值来指定颜色。 此设置确定列的背景颜色。

   - **[!UICONTROL Background Image]** — 如果需要，请使用提供的工具选择要应用于列的背景图像：

     | 工具 | 描述 |
     | ------ | ----------- |
     | [!UICONTROL Upload] | 将图像文件从本地计算机上载到图片库，然后将其作为列的背景图像应用。 |
     | [!UICONTROL Select from Gallery] | 提示您从图库中选择现有图像作为列的背景图像。 |
     | ![相机图标](./assets/pb-icon-camera.png){width="25"} | 允许您将图像拖到相机图块或浏览到本地文件系统中的图像。 |

     {style="table-layout:auto"}

   - **[!UICONTROL Background Mobile Image]** — 如果需要，请使用相同的工具选择不同的背景图像以在移动设备上显示。

   - **[!UICONTROL Background Size]** — 更改此设置以确定相对于列宽缩放背景图像的方式：

     | 选项 | 描述 |
     | ------ | ----------- |
     | `Cover` | 背景图像覆盖列的整个宽度。 |
     | `Contain` | 背景图像被限制为内容区域的宽度。 |
     | `Auto` | 应用在当前主题的样式表中指定的默认背景大小。 |

     {style="table-layout:auto"}

   - **[!UICONTROL Background Position]** — 更改此设置以确定图像相对于列的锚点。 选项： `Top Left`、`Top Center`、`Top Right`、`Center Left`、`Center`、`Center Right`、`Bottom Left`、`Bottom Center`或`Bottom Right`

   - **[!UICONTROL Background Attachment]** — 更改此设置以确定背景图像相对于滚动页面的移动方式：

     | 选项 | 描述 |
     | ------ | ----------- |
     | `Scroll` | 背景图像将同步以便在页面滚动时向下移动。 |
     | `Fixed` | （不适用于移动设备）当容器在图像上滚动时，背景图像不会移动，并且会固定到指定的背景位置。 |

     {style="table-layout:auto"}

   - **[!UICONTROL Background Repeat]** — 如果要重复背景图像以填充空间，请更改此设置`Yes`。

1. 根据需要更新&#x200B;_[!UICONTROL Advanced]_&#x200B;设置。

   - 要控制添加到列的内容容器的水平位置，请选择&#x200B;**[!UICONTROL Alignment]**：

     | 选项 | 描述 |
     | ------ | ----------- |
     | `Default` | 应用在当前主题的样式表中指定的对齐默认设置。 |
     | `Left` | 将内容容器沿列容器的左边框对齐，并允许使用指定的任何边距。 |
     | `Center` | 将内容容器对齐列容器的中心，并允许指定的任何边距。 |
     | `Right` | 将内容容器沿列容器的右边框对齐，并允许使用指定的任何边距。 |

     {style="table-layout:auto"}

   - 设置&#x200B;**[!UICONTROL Border]**&#x200B;样式，该样式应用于列容器的所有四面：

     | 选项 | 描述 |
     | ------ | ----------- |
     | `Default` | 应用关联样式表指定的默认边框样式。 |
     | `None` | 不提供任何容器边框的可见指示。 |
     | `Dotted` | 容器边框显示为虚线。 |
     | `Dashed` | 容器边框显示为虚线。 |
     | `Solid` | 容器边框显示为实线。 |
     | `Double` | 容器边框显示为双线。 |
     | `Groove` | 容器边框显示为一条开槽线。 |
     | `Ridge` | 容器边框显示为脊线。 |
     | `Inset` | 容器边框显示为内嵌行。 |
     | `Outset` | 容器边框显示为外线。 |

     {style="table-layout:auto"}

   - 如果设置了除`None`之外的边框样式，请完成边框显示选项：

     | 选项 | 描述 |
     | ------ |------------ |
     | [!UICONTROL Border Color] | 通过选择色板、单击拾色器或输入有效的颜色名称或等效的十六进制值来指定颜色。 |
     | [!UICONTROL Border Width] | 输入边框线条宽度的像素数。 |
     | [!UICONTROL Border Radius] | 输入像素数，以定义用于使边框每个角倒圆角的半径大小。 |

     {style="table-layout:auto"}

   - （可选）从当前样式表中指定要应用于列容器的&#x200B;**[!UICONTROL CSS classes]**&#x200B;的名称。

     用空格分隔多个类名。

   - 输入&#x200B;**[!UICONTROL Margins and Padding]**&#x200B;的值（以像素为单位）以指定列的外部边距和内边距。

     在列容器图中输入每个相应的值。

     | 容器区域 | 描述 |
     | -------------- | ----------- |
     | [!UICONTROL Margins] | 应用于容器所有边的外边缘的空白空间量。 选项： `Top` / `Right` / `Bottom` / `Left` |
     | [!UICONTROL Padding] | 应用于容器所有边的内边缘的空白空间量。 选项： `Top` / `Right` / `Bottom` / `Left` |

     {style="table-layout:auto"}

1. 完成后，单击&#x200B;**[!UICONTROL Save]**&#x200B;以应用设置并返回到[!DNL Page Builder]工作区。

<!-- Last updated from includes: 2023-01-19 14:32:13 -->

---
title: 元素 — 标题
description: 了解标题内容类型，该内容类型用于将标题级别为H1到H6的文本容器添加到 [!DNL Page Builder] 阶段。
exl-id: dc51e7f6-a235-49dc-a978-1419a63fa33e
feature: Page Builder, Page Content
source-git-commit: 4a3aa2aa32b692341edabd41fdb608e3cff5d8e0
workflow-type: tm+mt
source-wordcount: '941'
ht-degree: 0%

---

# 元素 — 标题

标题级别建立一个层次结构，用于组织内容并帮助搜索引擎为每个页面编制索引。 使用&#x200B;_阶段_&#x200B;中的[[!DNL Page Builder] 标题](workspace.md#stage)内容类型将标题级别为H1到H6的文本容器添加到阶段。 根据与当前主题关联的样式表设置标题的格式。

[部分中的](workspace.md)内容标题&#x200B;_[!UICONTROL Content]_字段可用于将H1标题添加到页面顶部。 但是，该字段是以前[!DNL Commerce]版本的旧字段，用于支持旧内容。 此字段未利用[!DNL Page Builder]的高级功能。 建议您将“内容标题”字段留空，并使用[!DNL Page Builder]标题内容类型来向页面添加任何级别的标题。

以下示例显示了使用Luma主题设置格式时，内容标题和标题内容类型的显示方式。

![店面的内容标题和标题级别](./assets/pb-storefront-heading-levels.png){width="700" zoomable="yes"}

您可以将标题从&#x200B;_面板的_&#x200B;元素[!DNL Page Builder]区域拖到舞台上的行、列或选项卡集中。 可以通过舞台上的编辑器工具栏或者使用&#x200B;_设置_ （![设置图标](./assets/pb-icon-settings.png){width="20"} ）控件来控制标题级别和对齐方式。

{{$include /help/_includes/page-builder-save-timeout.md}}

## 标题编辑器

![带工具栏的标题编辑器](./assets/pb-elements-heading-toolbar.png){width="500" zoomable="yes"}

## 标题容器工具箱

与所有内容容器一样，当您将鼠标悬停在该容器上时，将会显示工具箱。

![标题容器工具箱](./assets/pb-elements-heading-toolbox.png){width="500" zoomable="yes"}

| 工具 | 图标 | 描述 |
| --------- | ----------------- | ---------------------- |
| 移动 | ![移动图标](./assets/pb-icon-move.png){width="25"} | 将标题容器移动到页面上的另一个有效位置。 |
| （标签） | 标题 | 将当前容器标识为标题。 |
| 设置 | ![设置图标](./assets/pb-icon-settings.png){width="25"} | 打开“编辑标题”页面，您可以在此页面更改容器的属性。 |
| 隐藏 | ![隐藏图标](./assets/pb-icon-hide.png){width="25"} | 隐藏标题容器。 |
| 显示 | ![显示图标](./assets/pb-icon-show.png){width="25"} | 显示隐藏的标题容器。 |
| 复制 | ![图标重复](./assets/pb-icon-duplicate.png){width="25"} | 复制标题容器。 |
| 移除 | ![删除图标](./assets/pb-icon-remove.png){width="25"} | 从舞台中删除标题容器及其内容。 |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## 添加标题

1. 在[!DNL Page Builder]面板中，展开&#x200B;**[!UICONTROL Elements]**&#x200B;并将&#x200B;**[!UICONTROL Heading]**&#x200B;占位符拖到舞台上的行、列或选项卡集中。

   ![将标题拖到舞台上](./assets/pb-elements-heading-drag.png){width="600" zoomable="yes"}

1. 在编辑器中，在`Edit Heading Text`占位符上输入标题文本。

   默认情况下，为标题文本分配了第二级(H2)标题类型。

   标题编辑器中的![占位符](./assets/pb-elements-header-editor-placeholder.png){width="500" zoomable="yes"}

1. 在工具栏中，选择H1和H6之间的相应标题类型。

1. 根据需要更改对齐方式。

## 编辑标题设置

1. 将鼠标悬停在标题容器上以显示工具箱，然后选择&#x200B;_设置_ （ ![设置图标](./assets/pb-icon-settings.png){width="20"} ）图标。

   ![标题工具箱](./assets/pb-elements-heading-toolbox.png){width="500" zoomable="yes"}

1. 根据需要更新标题内容（**[!UICONTROL Heading Type]**&#x200B;和&#x200B;**[!UICONTROL Heading Text]**）。

   您还可以在标题编辑器中更新此内容。

1. 根据需要更新&#x200B;_[!UICONTROL Advanced]_设置。

   - 要控制标题在父容器中的位置，请选择&#x200B;**[!UICONTROL Alignment]**：

     | 选项 | 描述 |
     | ------ | ----------- |
     | `Default` | 应用在当前主题的样式表中指定的对齐默认设置。 |
     | `Left` | 将列表沿父容器的左边框对齐，并允许使用指定的任何边距。 |
     | `Center` | 将列表与父容器的中心对齐，并允许使用指定的任何边距。 |
     | `Right` | 沿父容器的右边框对齐块，并允许指定的任何边距。 |

     {style="table-layout:auto"}

   - 设置应用于标题容器所有四个侧面的&#x200B;**[!UICONTROL Border]**&#x200B;样式：

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

   - （可选）从当前样式表中指定要应用于容器的&#x200B;**[!UICONTROL CSS classes]**&#x200B;的名称。

     用空格分隔多个类名。

   - 输入&#x200B;**[!UICONTROL Margins and Padding]**&#x200B;的值（以像素为单位）以确定标题容器的外边距和内边距。

     在图表中输入相应的值。

     | 容器区域 | 描述 |
     | -------------- | ----------- |
     | [!UICONTROL Margins] | 应用于容器所有边的外边缘的空白空间量。 选项： `Top` / `Right` / `Bottom` / `Left` |
     | [!UICONTROL Padding] | 应用于容器所有边的内边缘的空白空间量。 选项： `Top` / `Right` / `Bottom` / `Left` |

     {style="table-layout:auto"}

1. 完成后，单击&#x200B;**[!UICONTROL Save]**&#x200B;以应用设置并返回到[!DNL Page Builder]工作区。

## 复制标题

对于具有特定设置的格式化标题，复制标题比使用新占位符重新开始更有效。

1. 将鼠标悬停在标题容器上以显示工具箱，然后选择&#x200B;_复制_ （![复制图标](./assets/pb-icon-duplicate.png){width="20"} ）图标。

   副本会出现在原始文件的正下方。

   ![复制标题容器](./assets/pb-elements-heading-duplicate.png){width="500" zoomable="yes"}

1. 将鼠标悬停在新标题容器上以显示工具箱，然后选择&#x200B;_移动_ （![移动图标](./assets/pb-icon-move.png){width="20"} ）图标。

   ![移动标题](./assets/pb-elements-heading-move.png){width="500" zoomable="yes"}

1. 选择并拖动标题，直到红色基准标记新位置。

   移动标题时，每个容器的顶边框和底边框均显示为虚线。

   ![将重复的标题移动到位置](./assets/pb-elements-heading-move-guideline.png){width="500" zoomable="yes"}

1. 如果要更改标题级别，请单击标题文本，然后在编辑器工具栏中选择新级别。

   ![选择新的标题级别](./assets/pb-elements-heading-change-heading-level.png){width="500" zoomable="yes"}

<!-- Last updated from includes: 2023-09-11 14:30:19 -->

---
title: '[!DNL Page Builder] Workspace'
description: 了解创建基本页面、产品和目录页面、块和动态块时 [!DNL Page Builder] 工作区中可用的工具。
exl-id: 1cd7b300-0a18-490f-bc11-36de3fec13dc
feature: Page Builder, Page Content
source-git-commit: 79dc16dcba239af12793813ae19636bbd7ec49c5
workflow-type: tm+mt
source-wordcount: '1426'
ht-degree: 0%

---

# [!DNL Page Builder] Workspace

启用[[!DNL Page Builder] 后](setup.md)，将修改&#x200B;_[!UICONTROL Content]_&#x200B;部分和内容创建过程以利用CMS [页面](../content-design/page-add.md)、[产品](../catalog/product-content.md)和[类别](../catalog/categories-content-settings.md)页面、[块](../content-design/block-add.md)和[动态块](../content-design/dynamic-blocks.md)的高级[!DNL Page Builder]工具。 此部分包括_&#x200B;内容标题&#x200B;_字段、内容预览和轻松访问全屏[!DNL Page Builder]工作区。

预览为[!DNL Page Builder]的![内容部分](./assets/pb-content-preview.png){width="700" zoomable="yes"}

## 内容标题

由于搜索引擎会查找第一级(H1)标题，因此添加第一级标题是一种确保页面正确编制索引的简单方法。

>[!NOTE]
>
>显示在页面顶部的&#x200B;_[!UICONTROL Content Heading]_&#x200B;字段是一个旧版字段，它支持使用以前的[!DNL Commerce]版本创建的内容。 但是，它不是[!DNL Page Builder]的一部分。 根据与当前主题关联的样式表，[!UICONTROL Content Heading]将格式化为H1标题。 它位于由[!DNL Page Builder]阶段定义的活动内容区域正上方。

为了更好地控制所有级别标题的位置和格式，建议将&#x200B;_[!UICONTROL Content Heading]_&#x200B;字段留空，并使用[!DNL Page Builder] [标题](heading.md)内容类型。

![内容标题和其他标题](./assets/pb-storefront-heading-levels.png){width="700" zoomable="yes"}

## 预览

当您展开&#x200B;_[!UICONTROL Content]_&#x200B;部分并且存在使用[!DNL Page Builder]创建的现有内容时，它将显示内容在页面中显示的预览。 单击&#x200B;**[!UICONTROL Edit with Page Builder]**&#x200B;或内容预览区域以打开[!DNL Page Builder]工作区，您可以在其中进行任何需要的更新。

![产品描述预览](./assets/pb-product-category-content-preview.png){width="500" zoomable="yes"}

>[!NOTE]
>
>对于产品和类别表单，默认情况下将启用此内容预览，但可以禁用它。 如果性能因加载预览而受到影响，则可以在[内容管理配置](../configuration-reference/general/content-management.md#advanced-content-tools)设置中禁用预览。

## Stage

当您从预览中打开[!DNL Page Builder]工作区时，舞台是您可在其中创建和设置内容格式，甚至快速编辑实时内容的主要工作区。 舞台最初是空的，它提供了设计界面，您可以在其中从左侧面板拖动行、列和选项卡。

>[!NOTE]
>
>从2.4.1版本开始，内容编辑现在仅针对[!DNL Page Builder]控制的所有区域进行全屏编辑，即CMS页面、产品和类别页面、块和动态块。 全屏编辑将焦点放在您的内容上，并提供与店面用户体验更匹配的视图。

包含页面内容的![阶段](./assets/pb-workspace-simple-page.png){width="600" zoomable="yes"}

{{$include /help/_includes/page-builder-save-timeout.md}}

## 视区

_视区_&#x200B;是用户看到的网页的可见区域。 在全屏设计模式下，视区按钮显示在[!DNL Page Builder]舞台的上方，当站点用户在店面中看到内容时，它会显示给您。

![视区按钮](./assets/pb-workspace-viewport-buttons.png){width="500" zoomable="yes"}

[!DNL Page Builder]还定义了视区的断点。 断点定义应用特定样式的最小和最大宽度。 [!DNL Page Builder]视区提供了以下内容断点：

- **桌面断点**—`min-width: 1024px`。 此断点将应用为测量1024像素和更宽的视区宽度定义的样式。
- **移动断点**—`max-width: 768px, min-width: 640px`。 这些断点应用为视区宽度定义的样式（介于768像素和640像素之间）。

[!DNL Page Builder]视区提供两种功能：**_内容预览_**&#x200B;和&#x200B;**_断点设置_**。

### 内容预览

默认情况下，[!DNL Page Builder]提供两个视区预览：

- **桌面** — 显示没有预定义宽度的内容预览。 桌面定义的样式（使用断点最小宽度1024像素）仍会应用于页面。 但是，桌面视区宽度由容器内容类型（如行）的设置来定义。 选择桌面视区会显示当浏览器页面宽度为1024像素或更宽时，内容在店面上的样式设置。

  ![最小宽度为1024像素的桌面视区预览](./assets/pb-workspace-viewport-desktop.png){width="500" zoomable="yes"}

- **移动设备** — 以预定义的宽度768像素显示内容预览。 与桌面视区不同，移动设备视区的显示页面内容宽度为768像素，包括为断点宽度定义的样式宽度为768像素（最大值）和640像素（最小值）。

  ![最小宽度为768像素的移动设备视区预览](./assets/pb-workspace-viewport-mobile.png){width="500" zoomable="yes"}

### 断点设置

视区按钮还提供了根据所选视区将不同的断点样式应用于内容类型的选项。 默认情况下，[!DNL Page Builder]为行、列、选项卡、选项卡项、横幅、滑块和幻灯片的&#x200B;_[!UICONTROL Minimum Height]_&#x200B;字段提供断点设置。 当选择移动设备视区，然后打开其中一个内容类型的编辑器时，您可以输入特定于移动设备视区断点的字段值。 允许特定断点设置的内容类型字段在字段右侧显示一个图标，类似于以下行示例：

断点设置的![图标指示器](./assets/pb-workspace-viewport-field-breakpoint.png){width="400"}

## 面板

[!DNL Page Builder]面板位于舞台的左侧，包含可拖到舞台的内容类型。 随即会显示一个特定于内容类型的容器，其中包含选项工具箱。 内容类型在面板中组织如下：

### 布局

[!DNL Page Builder]面板的&#x200B;_[!UICONTROL Layout]_&#x200B;部分用于将行、列或选项卡添加到阶段。 将内容类型从面板拖到舞台上时，会显示一个容器，其中包含特定于内容类型的选项工具箱。

默认情况下，[!DNL Page Builder]阶段为空。 将布局内容类型从面板拖到舞台时，可以将它们放置在页面上的其他布局容器的上面、下面或内部。 只能将行直接添加到阶段。

具有布局内容类型和阶段![&#128279;](./assets/pb-stage-toolbox.png){width="600" zoomable="yes"}的[!DNL Page Builder]面板

| 布局内容类型 | 描述 |
| ------------------- |------------ |
| [行](row.md) | 新行只能从面板拖到舞台上，并位于其他行、选项卡或列组的上方或下方。 您还可以使用“复制”选项来复制现有行。 |
| [列](column.md) | 可以将列从面板拖到舞台上，或者拖到行和选项卡上。 可添加的最大列数由[配置](setup.md)中指定的网格分区数决定。 |
| [选项卡](tabs.md) | 单个选项卡可以从面板拖到舞台上，或者拖到行和列上。 可以从工具箱中添加其他选项卡。 |

{style="table-layout:auto"}

### 元素

使用[!DNL Page Builder]面板的&#x200B;_[!UICONTROL Elements]_&#x200B;部分将文本、标题、按钮、分隔符和HTML代码添加到[[!DNL Page Builder] 阶段](workspace.md#stage)上的任何布局容器中。 将内容类型从面板拖到行或列，或者拖到舞台上的选项卡集时，会显示一个容器。 使用内容类型工具箱访问特定于类型的设置。

具有元素内容类型的![[!DNL Page Builder]面板](./assets/pb-elements.png){width="600" zoomable="yes"}

| 元素内容类型 | 描述 |
| -------------------- | ----------- |
| [文本](text.md) | 向阶段中添加文本容器和编辑器。 |
| [标题](heading.md) | 向阶段添加标题容器。 |
| [按钮](buttons.md) | 将单个按钮或一组按钮的容器添加到舞台中。 |
| [分隔线](divider.md) | 将分隔符的容器添加到舞台中。 |
| [HTML代码](html-code.md) | 向阶段中添加用于HTML代码的容器。 |

{style="table-layout:auto"}

### 媒体

使用[!DNL Page Builder]面板的&#x200B;_[!UICONTROL Media]_&#x200B;部分将图像、视频、横幅、滑块和[!DNL Google Maps]添加到[[!DNL Page Builder] 舞台](workspace.md#stage)上的任何布局容器中。 将媒体内容类型从面板拖到舞台时，会显示一个容器，其中包含特定于内容类型的选项工具箱。

具有媒体内容类型的![[!DNL Page Builder]面板](./assets/pb-media-content-types.png){width="600" zoomable="yes"}

| 媒体内容类型 | 描述 |
| ------------------- | ------------------------------------------ |
| [图像](image.md) | 向舞台添加图像容器。 |
| [视频](video.md) | 向舞台添加视频容器。 |
| [横幅](banner.md) | 向阶段添加横幅容器。 |
| [滑块](slider.md) | 向舞台添加滑块容器。 |
| [映射](map.md) | 向阶段添加[!DNL Google Maps]容器。 |

{style="table-layout:auto"}

### 添加内容

使用[!DNL Page Builder]面板的&#x200B;_[!UICONTROL Add Content]_&#x200B;部分将现有内容添加到[[!DNL Page Builder] 阶段](workspace.md#stage)。 将媒体内容类型从面板拖到舞台时，会显示一个容器。 使用内容类型工具箱访问特定于此类型的_&#x200B;设置&#x200B;_。

具有添加内容类型的![[!DNL Page Builder]面板](./assets/pb-add-content.png){width="600" zoomable="yes"}

| 内容类型 | 描述 |
| ---------------------------------------------------------------- | -------------------------------------------- |
| [块](block.md) | 向阶段中添加现有块。 |
| [动态块](dynamic-block.md) | 向阶段中添加现有动态块。 |
| [产品](products.md) | 向阶段中添加产品列表。 |
| ![仅限Adobe Commerce](../assets/adobe-logo.svg) [产品Recommendations](recommendations.md) | 向阶段添加推荐单位。 |

{style="table-layout:auto"}

## Toolbox

舞台上的每个内容容器都有一个选项工具箱。 这些选项因内容类型而异，但通常包括“移动”、“设置”、“隐藏/显示”、“复制”和“删除”。

### 显示工具箱

将鼠标悬停在容器上以显示工具箱，然后选择一个选项。

![行工具箱选项](./assets/pb-tutorial1-row-toolbox.png){width="600" zoomable="yes"}

### 工具箱选项

| 选项 | 图标 | 描述 |
| --------- | ---------------------------------------- | ------------ |
| 移动 | ![移动图标](./assets/pb-icon-move.png){width="25"} | 将当前内容容器移动到舞台上的另一个位置。 |
| 添加 | ![添加图标](./assets/pb-icon-add.png){width="25"} | 添加子元素，例如按钮、幻灯片或制表符。 |
| （标签） |           | 标识容器内容类型。 |
| 设置 | ![设置图标](./assets/pb-icon-settings.png){width="25"} | 在编辑模式下打开内容容器属性。 |
| 隐藏 | ![隐藏图标](./assets/pb-icon-hide.png){width="25"} | 隐藏当前内容容器。 |
| 显示 | ![显示图标](./assets/pb-icon-show.png){width="25"} | 显示当前内容容器。 |
| 复制 | ![图标重复](./assets/pb-icon-duplicate.png){width="25"} | 制作当前内容容器的副本。 |
| 移除 | ![移除](./assets/pb-icon-remove.png){width="25"} | 从舞台中删除当前内容容器。 |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

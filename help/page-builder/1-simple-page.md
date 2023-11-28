---
title: ’[!DNL Page Builder] 演练第1部分：简单页面
description: 使用示例文件并按照以下步骤在中创建一个简单页面 [!DNL Page Builder] 界面。
exl-id: 2c146241-675f-4d23-9513-1722d5dd3357
feature: Page Builder, Page Content
source-git-commit: 2299beb6c11af801076d3aff0b026d41b9dbd212
workflow-type: tm+mt
source-wordcount: '3311'
ht-degree: 0%

---

# [!DNL Page Builder] 演练第1部分：简单页面

按照此三步练习来熟悉 [!DNL Page Builder] workspace的方法是创建一个简单页面，该页面展示创建自己设计中内容丰富的页面是多么容易。

![简单页面示例](./assets/pb-tutorial1-simple-layout.png){width="700" zoomable="yes"}

>[!NOTE]
>
>这些演练已更新，以反映最近对 [!DNL Page Builder] workspace 2.4.1版本中的工作区。 如果您使用的是较低版本的Adobe Commerce，请使用 [!DNL Page Builder] 演练包含在 [[!DNL Commerce] 2.3用户指南](https://docs.magento.com/user-guide/v2.3/cms/page-builder-learn.html).

## 开始之前

在开始本练习之前，建议您增加 [管理员会话生命周期](../systems/security-admin.md) 以防止会话在您工作时超时。

验证所需的内容管理配置设置：

- 在中启用了WYSIWYG编辑器 [所见即所得选项](../content-design/editor.md#configure-the-editor) 配置。

- [!DNL Page Builder] 在中启用 [高级内容工具](setup.md) 配置。

### 下载演练图像资产

1. 下载 [`simple-page-assets`](./assets/simple-page-assets.zip) 将文件保存到本地系统中。

1. 导航到下载的文件并解压缩文件。

   在Windows系统上，右键单击并选择 **[!UICONTROL Extract All]** 文件。 然后，选择目标文件夹并单击 **[!UICONTROL Extract]**.

   在Mac系统上，只需双击zip文件，然后将提取的文件移动到目标文件夹即可。

   该文件夹包含以下图像文件：

   ![[!DNL Page Builder] 演练文件 — 简单页面资产](./assets/pb-tutorial-simple-page-assets.png){width="500"}

按照顺序执行本演练的三个部分。

## 第1部分：带有横幅的完全出血行

在简单页面练习的这一可选部分中，您将创建一个具有完整出血行和横幅的页面。 该行具有桌面和移动设备的不同背景图像。

![[!DNL Page Builder] 带有横幅的完全出血行](./assets/pb-tutorial1-full-bleed-with-banner.png){width="700" zoomable="yes"}

### 步骤1：创建页面

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. 在右上角，单击 **[!UICONTROL Add New Page]** 并执行以下操作：

   - 要防止在您的存储中发布此页面，请设置 **[!UICONTROL Enable Page]** 到 `No`.

   - 对象 **[!UICONTROL Page Title]**，输入 `Simple Page`.

   ![基本页面设置](./assets/pb-tutorial1-currently-active.png){width="600" zoomable="yes"}

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Design]** 部分。

   请注意 **[!UICONTROL Layout]** 设置为 `Page -- Full Width` 默认情况下。 除了五项标准外 [布局](../content-design/page-layout.md) 选项， [!DNL Page Builder] 为页面、类别和产品添加全宽布局。

1. 如果样本数据可用，请设置 **[!UICONTROL New Theme]** 到 `Magento Luma`. 否则，您可以选择其他可用的主题或将其留空以使用默认主题。

   此 _[!UICONTROL New Theme]_设置可用于覆盖默认主题并将其他主题应用到页面。

   >[!NOTE]
   >
   >全宽布局只能与兼容布局一起使用 [主题](../content-design/themes.md).

   ![页面设计设置](./assets/pb-tutorial1-design-section.png){width="600" zoomable="yes"}

1. 在右上角，单击 **[!UICONTROL Save]**.

   保存页面时，名称 _简单页面_ 显示在页面的左上角。

### 第2步：设置行的格式

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Content]** 部分。

   此操作显示 [!DNL Page Builder] 使用空行预览。

   >[!NOTE]
   >
   >此 [内容标题](workspace.md) 字段是可选的。 默认情况下，根据主题设置标题级别1 (H1)的格式。 在本练习中， _内容标题_ 留空。

   ![空行的页面内容预览](./assets/pb-content-preview-empty.png){width="600" zoomable="yes"}

1. 单击 **[!UICONTROL Edit with Page Builder]** 或位于内容预览区域内。

   在扩展的 [!DNL Page Builder] [工作区](workspace.md)，左侧的面板提供了可用于在阶段中构建内容的内容工具。

1. 将鼠标悬停在空行上以显示工具箱。

   每个内容容器都有一个工具箱，其中包含一组相似的选项。

   ![[!DNL Page Builder] 行工具箱](./assets/pb-layout-page-add-content-row-tools.png){width="600" zoomable="yes"}

1. 在行工具箱中，选择 _设置_ (![“设置”图标](./assets/pb-icon-settings.png){width="20"} 图标。

1. 下 _[!UICONTROL Appearance]_，选择&#x200B;**完全出血**.

   “完全出血”外观设置可将行和背景的内容区域的左右边框扩展到页面的全部宽度。

   ![行设置 — 完全出血](./assets/pb-tutorial1-row-settings-appearance-full-bleed.png){width="600" zoomable="yes"}

1. 向下滚动到 _[!UICONTROL Advanced]_部分并设置全部&#x200B;**[!UICONTROL Margins and Padding]**设置到 `0`.

   此设置可确保横幅扩展行的完整宽度。

   ![行设置 — 边距和边距](./assets/pb-tutorial1-row-settings-advanced-margins-padding-zero.png){width="600" zoomable="yes"}

1. 要保存设置并返回至 [!DNL Page Builder] 工作区，向上滚动到页面顶部，然后单击 **[!UICONTROL Save]** 在右上角。

### 步骤3：添加横幅

>[!NOTE]
>
>[!DNL Page Builder] 具有名为的新内容类型 _横幅_，此步骤中会特别介绍此功能。 之前的 _横幅_ 选项，现在为 _动态块_.

1. 在 [!DNL Page Builder] 面板，展开 **[!UICONTROL Media]** 并拖动 **横幅** 舞台占位符。

   ![将横幅内容类型拖到舞台上](./assets/pb-tutorial1-banner-drag-to-stage.png){width="600" zoomable="yes"}
1. 将鼠标悬停在横幅容器上以显示工具箱。

   >[!NOTE]
   >
   >现在，舞台有两个内容容器，每个容器都有一个单独的工具箱。 由于横幅嵌套在行中，因此请确保您使用的是正确的工具箱。

   除了工具箱， _上传图像_ 和 _从图库中选择_ 其中包含了按钮，以便您可以直接从舞台快速更改横幅。

   ![横幅工具箱](./assets/pb-tutorial1-banner-toolbox.png){width="600" zoomable="yes"}

1. 在“横幅工具箱”中，选择 _设置_ ( ![“设置”图标](./assets/pb-icon-settings.png){width="20"} )图标。

1. 下 _[!UICONTROL Appearance]_，选择&#x200B;**[!UICONTROL Collage Right]**.

   “拼贴右侧”设置将内容放置在横幅的右侧。

   ![横幅外观 — 拼贴右侧](./assets/pb-tutorial1-row-banner-settings-appearance-collage-right.png){width="600" zoomable="yes"}

1. 向下滚动到 _[!UICONTROL Background]_并设置横幅的背景图像：

   - 对象 **[!UICONTROL Background Image]**，单击 **上传**.

     ![横幅背景 — 上传图像](./assets/pb-tutorial1-row-background-image-upload.png){width="600" zoomable="yes"}

     导航到保存提取的简单页面资产的目录，然后选择 `wide-banner-background.jpg` 文件。

     上传图像，并显示上传图像的缩略图。 文件名、图像尺寸和文件大小如下所述。

     ![已上传媒体集中的背景图像](./assets/pb-tutorial1-row-settings-background-image-selected.png){width="600" zoomable="yes"}

   - 对象 **[!UICONTROL Background Mobile Image]**，单击 **上传**.

     在同一文件目录中，选择 `wide-banner-background-mobile.jpg` 文件。

     移动设备使用移动设备背景图像，每当将桌面浏览器窗口的大小调整为移动设备的宽度时，也会使用背景图像。

     ![选择移动设备的示例横幅图像文件](./assets/pb-tutorial1-row-settings-background-mobile-image-selected.png){width="600" zoomable="yes"}

   - 向后滚动到页面顶部，然后单击 **[!UICONTROL Save]** 以保存设置并返回到 [!DNL Page Builder] 工作区。

     背景显示在舞台上，并扩展行的完整宽度。

     ![具有背景图像的横幅](./assets/pb-tutorial1-banner-background.png){width="600" zoomable="yes"}

   请注意行右侧显示的占位符文本。 本文的位置反映了 _拼贴右侧_ 外观设置。

1. 单击占位符文本，然后输入以下消息作为两行：

   `Get fit and look fab in new seasonal styles.`

   `New LUMA yoga collection`

   编辑器工具栏显示在文本框上方。 文本可以直接从舞台输入并设置格式，也可以通过选择 _设置_ 在横幅工具箱中。

   ![从舞台上编辑横幅内容](./assets/pb-tutorial1-banner-stage-text.png){width="600" zoomable="yes"}

1. 对文本应用格式：

   - 选择文本的第一行。 然后，在编辑器工具栏上，位于 **格式**，选择 `Heading 2`.

     ![应用标题2格式](./assets/pb-tutorial1-banner-stage-text-format-line1.png){width="600" zoomable="yes"}

   - 选择第二行文本。 然后，在编辑器工具栏上，位于 **格式**，选择 `Paragraph`.

   格式设置应用与当前主题关联的样式表中的样式。

   ![内容阶段中带格式文本的横幅](./assets/pb-tutorial1-banner-stage-text-format-line2.png){width="600" zoomable="yes"}
__

1. 将鼠标悬停在上面以显示横幅工具箱，选择 _设置_ ( ![“设置”图标](./assets/pb-icon-settings.png){width="20"} )图标，然后滚动到 _[!UICONTROL Content]_部分。

   请注意，您的文本将显示在 _消息文本_ 盒子。 文本可以从舞台输入和编辑，也可以从 _[!UICONTROL Content]_横幅设置的部分。

   ![横幅设置 — 消息文本](./assets/pb-tutorial1-banner-settings-content-message-text.png){width="600" zoomable="yes"}

1. 在中继续 _[!UICONTROL Content]_部分，设置横幅链接和按钮：

   - 设置 **链接** 到 `Category`，然后单击 **[!UICONTROL Select]** 以显示类别树。

   - 选择 `What's New` 作为链接的类别。

     ![横幅内容 — 链接到类别](./assets/pb-tutorial1-banner-settings-link-category-tree.png){width="600" zoomable="yes"}

   - 设置 **[!UICONTROL Show Button]** 到 `Always`.

   - 对象 **[!UICONTROL Button Text]**，输入 `Shop Now` 作为按钮上显示的文本。

   - 对象 **[!UICONTROL Button Type]**，接受 `Primary` 默认。

     当前主题中的按钮样式决定了按钮格式。

1. 设置横幅叠加：

   您可以使用叠加将背景颜色应用到由“外观”设置定义的活动内容区域。 横幅背景图像在横幅全宽范围内保持可见。

   - 设置 **[!UICONTROL Show Overlay]** 到 `Always`.

   - 对象 **[!UICONTROL Overlay Color]**，请执行下列操作之一：

      - 单击颜色方框并选择白色色板。
      - 单击 _无颜色_ 文本框并输入 `White` 或十六进制值 `#ffffff`.

     然后，单击 **[!UICONTROL Apply]**.

     ![横幅设置 — 按钮叠加颜色](./assets/pb-tutorial1-banner-settings-overlay-color.png){width="600" zoomable="yes"}

   - 向后滚动到页面顶部，然后单击 **[!UICONTROL Save]** 以保存设置并返回到 [!DNL Page Builder] 工作区。

     按钮显示在舞台上横幅消息的下方。

     ![内容阶段的横幅（包含文本消息和按钮）](./assets/pb-tutorial1-banner-stage-background-color.png){width="600" zoomable="yes"}

1. 在舞台的右上角，单击 _关闭全屏_ (![“关闭全屏”图标](./assets/pb-icon-reduce.png))图标。

   单击此图标会返回到 _[!UICONTROL Content]_显示预览的页面的部分。

   您可以随时在两种工作区模式之间切换。

1. 在右上角，单击 **[!UICONTROL Save]** 箭头并选择 **[!UICONTROL Save & Close]**.

1. 如果出现提示，请单击 [缓存管理](../systems/cache-management.md) 链接页面顶部的消息，并刷新任何无效缓存。

## 第2部分：包含的行具有两个相等列

在本练习的此部分中，您将向页面中添加一行，并将该行划分为两个相等的列。 然后，将链接图像添加到每一列。 在说明中，每个新行都添加到第一行之前，以使 [!DNL Page Builder] 面板与舞台对齐。 在练习结束时，您可以重新排列行，使其与简单页面示例匹配。

![使用具有两个相等列的包含行的示例页面](./assets/pb-tutorial1-contained-row-with-two-equal-columns.png){width="600" zoomable="yes"}

### 步骤1：添加行

1. 在“页面”网格中，查找 _简单页面_ 您在本练习的第一部分中创建的并选取 **[!UICONTROL Edit]** 在 _[!UICONTROL Action]_列。

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Content]** 部分。

1. 单击 **[!UICONTROL Edit with Page Builder]** 或位于内容预览区域内。

1. 在 [!DNL Page Builder] 下的面板 _[!UICONTROL Layout]_，拖动&#x200B;**[!UICONTROL Row]**舞台占位符，并将其放在横幅上方。

   红色基准线标记两行之间的边界。

   ![在横幅上方添加新行](./assets/pb-tutorial1-row-drag-to-stage.png){width="600" zoomable="yes"}

1. 将鼠标悬停在新行上以显示工具箱，然后选择 _设置_ ( ![“设置”图标](./assets/pb-icon-settings.png){width="20"} )图标。

   ![行工具箱](./assets/pb-tutorial1-row-settings.png){width="600" zoomable="yes"}

1. 下 _[!UICONTROL Appearance]_，接受&#x200B;**包含**默认设置。

   此设置将行的内容区域限制为主题定义的页面宽度。

   ![保留默认包含外观设置](./assets/pb-tutorial1-row-settings-appearance.png){width="600" zoomable="yes"}

1. 在右上角，单击 **[!UICONTROL Save]** 以保存设置并返回到 [!DNL Page Builder] 工作区。

### 第2步：添加列

1. 在 [!DNL Page Builder] 下的面板 _[!UICONTROL Layout]_，拖动&#x200B;**[!UICONTROL Column]**新行的占位符。

   ![将列内容类型拖到舞台上](./assets/pb-tutorial1-column-drag-to-stage.png){width="600" zoomable="yes"}

   该行现在分为两列，每列的宽度相等。 每列都是一个单独的内容容器，并具有自己的专用选项工具箱。

   ![两列宽度相等的行](./assets/pb-tutorial1-columns-equal-width.png){width="600" zoomable="yes"}

1. 在第一列的左上角，单击圆形 _网格_ 控件(![网格控件](./assets/pb-icon-grid-control.png))以显示网格准则。

   网格可确保内容保持一致，并在桌面和移动设备上正确呈现。 有关配置网格大小的信息，请参见 [配置 [!DNL Page Builder]](setup.md#configure-page-builder) 中的部分 [!DNL Page Builder] 设置主题。

   每个列容器顶部边框的圆括号(6/12)中的数字表示每列中的网格划分数，以及行中的划分总数。

   ![显示列的网格大小详细信息](./assets/pb-tutorial1-columns-grid-size.png){width="600" zoomable="yes"}

### 步骤3：添加带有链接的图像

在此步骤中，您将了解如何将图像上传到横幅。

1. 在 [!DNL Page Builder] 面板，展开 **[!UICONTROL Media]** 剖分并拖动 **[!UICONTROL Image]** 第一列的占位符。

   ![将图像内容类型拖到第一列](./assets/pb-tutorial1-column1-media-image-drag.png){width="600" zoomable="yes"}

1. 将示例图像插入占位符。

   ![图像占位符](./assets/pb-tutorial1-column-image-upload.png){width="600" zoomable="yes"}

   对于位于系统上的映像，可以选择以下任一方法：

   - **上传图像文件**：在第一列中，单击 **[!UICONTROL Upload Image]**. 然后，导航到保存提取的简单页面资产的目录，然后选择 `small-banner-1.jpg` 文件。

     ![上传的图像已添加到第一列](./assets/pb-tutorial1-column1-image.png){width="600" zoomable="yes"}

     重复此操作以添加 `small-banner-2.jpg` 文件到第二列。

   - **拖动图像文件**：在您的桌面上，打开简单页面资产文件夹，并将其放在管理员浏览器窗口旁边，您将在其中使用 [!DNL Page Builder] 暂存。 然后，拖动文件 `small-banner-1.jpg` 从简单页面资产文件夹中，并将其放入第一列。

     ![将图像拖到第二列上](./assets/pb-tutorial1-column-image-drag.png){width="600" zoomable="yes"}

     重复此操作以添加 `small-banner-2.jpg` 文件到第二列。

1. 确定目录中的哪个页面要链接到每个图像。

1. 将鼠标悬停在第一列中的图像上以显示工具箱，然后选择 _设置_ ( ![“设置”图标](./assets/pb-icon-settings.png){width="20"} )图标。

   ![图像工具箱](./assets/pb-tutorial1-column1-image-settings.png){width="600" zoomable="yes"}

1. 将图像链接到类别：

   - 向下滚动并设置 **链接** 到 `Category`.

   - 在类别树中，向下钻取并选择 `Men's Hoodies & Sweatshirt` 类别。

   - 在右上角， **[!UICONTROL Save]** 设置并返回到 [!DNL Page Builder] 工作区。

1. 重复上一步骤，将第二列中的图像链接到 _齿轮_ 类别。

1. 在舞台的右上角，单击 _关闭全屏_ (![“关闭全屏”图标](./assets/pb-icon-reduce.png))图标。

   单击此图标会返回到 _[!UICONTROL Content]_显示预览的页面的部分。

1. 在右上角，单击 **[!UICONTROL Save]** 箭头并选择 **[!UICONTROL Save & Close]**.

1. 出现提示时，单击 [缓存管理](../systems/cache-management.md) 链接页面顶部的消息，并刷新任何无效缓存。

## 第3部分：具有不相等列的全宽行

此页面的最后一行包含产品评论中的内容。 添加一个全宽行并将其划分为两个宽度不同的列。 将背景图像添加到第一列，并将匹配的背景颜色应用于行以获得统一的效果。

![具有不同宽度列的完整宽度行示例](./assets/pb-tutorial1-full-width-row-two-unequal-columns.png){width="500"}

### 步骤1：添加行

1. 在“页面”网格中，查找 _简单页面_ 您在本练习的第一部分中创建的并选取 **[!UICONTROL Edit]** 在 _[!UICONTROL Action]_列。

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Content]** 部分。

1. 单击 **[!UICONTROL Edit with Page Builder]** 或位于内容预览区域内。

1. 在 [!DNL Page Builder] 下的面板 _[!UICONTROL Layout]_，拖动&#x200B;**[!UICONTROL Row]**舞台的占位符，并将其放在本练习第二部分中创建的行的上方。

   红色基准线标记两行之间的边界。

   ![添加新行](./assets/pb-tutorial1-add-new-row.png){width="600" zoomable="yes"}

1. 将鼠标悬停在新行上以显示工具箱，然后选择 _设置_ (![“设置”图标](./assets/pb-icon-settings.png){width="20"} )图标。

   ![行工具箱](./assets/pb-tutorial1-row-toolbox.png){width="600" zoomable="yes"}

1. 在“编辑行”页面的下面 _[!UICONTROL Appearance]_，选择&#x200B;**[!UICONTROL Full Width]**.

   此设置将内容区域限制为由主题定义的最大页面宽度。 背景颜色和/或图像不受限制，并会扩展行的完整宽度。

   ![选择“全宽”外观](./assets/pb-tutorial1-row-settings-appearance-full-width.png){width="600" zoomable="yes"}

1. 在 _[!UICONTROL Background]_部分，输入 `#f1f1f1` 作为&#x200B;**[!UICONTROL Background Color]**.

   ![设置背景颜色](./assets/pb-tutorial1-row-settings-background-color.png){width="600" zoomable="yes"}

1. 向下滚动到 _[!UICONTROL Advanced]_部分并设置全部&#x200B;**边距和边距**值到 `0`.

   ![设置边距和边距](./assets/pb-tutorial1-row-settings-advanced-margins-padding-zero.png){width="600" zoomable="yes"}

1. 向后滚动到页面顶部，然后单击 **[!UICONTROL Save]** 以保存设置并返回到 [!DNL Page Builder] 工作区。

   该行的背景颜色现在为淡黄色。

   ![舞台中具有背景颜色的行](./assets/pb-tutorial1-row-background-beige.png){width="600" zoomable="yes"}

### 步骤2：添加不同宽度的列

1. 在 [!DNL Page Builder] 下的面板 _[!UICONTROL Layout]_，拖动&#x200B;**[!UICONTROL Column]**舞台上顶行的占位符。

   ![将列拖到舞台上](./assets/pb-tutorial1-column-drag.png){width="600" zoomable="yes"}

1. 将第一列的右边框拖动到12中的四个(`4/12`)在网格中的位置。

   第二列的大小调整为12的8个(`8/12`)。

   ![调整第一列的大小](./assets/pb-tutorial1-column-first-4.png){width="600" zoomable="yes"}

1. 将鼠标悬停在第一列容器上以显示工具箱，然后选择 _设置_ ( ![“设置”图标](./assets/pb-icon-settings.png){width="20"} )图标。

1. 向下滚动到 _[!UICONTROL Advanced]_部分并设置全部&#x200B;**边距和边距**值到 `0`.

   ![设置边距和边距](./assets/pb-tutorial1-row-settings-advanced-margins-padding-zero.png){width="600" zoomable="yes"}

1. 向后滚动到页面顶部，然后单击 **[!UICONTROL Save]** 以保存设置并返回到 [!DNL Page Builder] 工作区。

### 第3步：在第一列中添加图像

1. 在 [!DNL Page Builder] 面板，展开 **[!UICONTROL Media]** 并拖动 **[!UICONTROL Image]** 内容类型到第一列。

   ![将图像内容类型拖到第一列](./assets/pb-tutorial1-column1-image-drag.png){width="600" zoomable="yes"}

1. 在图像占位符中，单击 **[!UICONTROL Upload Image]**.

   ![上传图像](./assets/pb-tutorial1-column1-image-upload.png){width="600" zoomable="yes"}

1. 导航到保存提取的简单页面资产的目录，然后选择 `review-image.jpg` 文件。

   上传的图像显示在第一列中，并与行的背景颜色无缝混合。

   ![上传的图像已添加到列](./assets/pb-tutorial1-column1-image-uploaded.png){width="600" zoomable="yes"}

### 步骤4：将审核内容添加到第二列

行的第二列应包含客户评论的内容，包括五星级评级图像和格式化的文本消息。

1. 在 [!DNL Page Builder] 面板，展开 **[!UICONTROL Elements]** 部分并拖动 **[!UICONTROL Text]** 内容类型到第二列。

   ![将文本内容类型拖到舞台上](./assets/pb-tutorial1-column2-text-drag.png){width="600" zoomable="yes"}

1. 单击文本元素以显示编辑器工具栏。

1. 在工具栏中，单击 _插入图像_ (![“插入图像”图标](./assets/editor-btn-insert-edit-image.png))图标，并执行以下操作：

   ![在文本中插入图像](./assets/pb-tutorial1-column2-editor-toolbar-insert-image.png){width="600" zoomable="yes"}

   - 在 _[!UICONTROL Insert/edit image]_对话框，单击_&#x200B;查找&#x200B;_( ![“查找”图标](./assets/editor-btn-find-source.png) )图标_[!UICONTROL Source]_ 字段。

     ![插入/编辑图像对话框](./assets/pb-tutorial1-column2-text-insert-edit-image.png){width="600" zoomable="yes"}

   - 在 _[!UICONTROL Select Images]_页面，单击&#x200B;**[!UICONTROL Choose Files]**.

   - 在保存简单页面资产的文件夹中，选择 `rating.png`.

   - 返回页面，双击图像拼贴以将其选中并将其URL插入源字段。

     ![选择页面上的图像](./assets/pb-tutorial1-column2-editor-gallery-select-image.png){width="600" zoomable="yes"}

   - 对象 **[!UICONTROL Image Description]**，输入 `5-Star Rating` 并单击 **[!UICONTROL OK]** 将图像插入到列中。

   - 在编辑器工具栏中，单击 **居中对齐** (![“居中对齐”按钮](./assets/editor-btn-align-center.png))，以将列中的图像居中。

     ![居中的评级图像](./assets/pb-tutorial1-column2-5stars-centered.png){width="600" zoomable="yes"}

1. 将插入点放在五星形图像的后面，按Enter/Return键以开始新行，然后输入以下文本：

   `Awesome Tank!`

   `I'm a long distance runner and it keeps me pretty comfortable, although these companies always act like their shirts are magical and really it's just pretty basic stuff. Still it's a great shirt, and I would recommend it.`

   `Antonia Racer Tank – Reviewed by Allyson`

   文字在键入时居中。

   ![查看在列中居中的文本](./assets/pb-tutorial1-column2-text-unformatted.png){width="600" zoomable="yes"}

1. 设置文本格式：

   - 单击文本第一行中编辑器工具栏上以下位置的任意位置 **格式**，选择 `Heading 2`.

   - 选择剩余的文本，并在下的编辑器工具栏上 **格式**，选择 `Paragraph`.

   根据与主题关联的样式表对文本进行格式设置。

1. 获取图像的尺寸，以便您可以在列中垂直居中对齐内容：

   - 将鼠标悬停在第一列中的图像上以显示工具箱，然后选择 _设置_ (![“设置”图标](./assets/pb-icon-settings.png){width="20"} )图标。

   - 在图像的缩略图下方，记下图像的尺寸。

     ![缩略图下方显示的图像尺寸](./assets/pb-tutorial1-column1-image-dimensions.png){width="600" zoomable="yes"}

   - 在右上角，单击 **关闭**.

1. 将内容垂直居中于第二列：

   - 将鼠标悬停在第二列上以显示工具箱，然后选择 _设置_ (![“设置”图标](./assets/pb-icon-settings.png){width="20"} )图标。

   >[!NOTE]
   >
   >确保选择列容器而不是文本容器以显示正确的工具箱。

   - 对象 **[!UICONTROL Minimum Height]**，输入 `450` 作为第一列中图像的像素高度。

   - 设置 **[!UICONTROL Vertical Alignment]** 到 `Center`.

   ![设置最小高度和垂直对齐方式](./assets/pb-tutorial1-column2-layout-vertical-alignment.png){width="600" zoomable="yes"}

1. 向下滚动到 _[!UICONTROL Advanced]_部分并设置全部&#x200B;**[!UICONTROL Margins and Padding]**值为零( `0` )。

   ![设置边距和边距](./assets/pb-tutorial1-row-settings-advanced-margins-padding-zero.png){width="600" zoomable="yes"}

1. 向后滚动到页面顶部，并在右上角单击 **[!UICONTROL Save]** 以保存设置并返回到 [!DNL Page Builder] 工作区。

   ![阶段上具有审阅内容的行](./assets/pb-tutorial1-row-reviw-content.png){width="600" zoomable="yes"}

### 步骤5：插入目录产品链接

1. 选择 `Antonia Racer Tank` 文本，然后单击 _插入链接_ (![“插入链接”图标](./assets/editor-btn-insert-edit-link.png))图标。

1. 在 _插入链接_ 对话框，请指定指向目录产品的链接：

   - 输入产品 **[!UICONTROL URL]**.

     您可以输入相对或完全限定的URL。 在此示例中输入了以下相对链接：

     `../antonia-racer-tank.html`

   - （可选）对于 **标题**，输入产品名称。

     标题链接属性被某些浏览器用作工具提示。

     ![在文本中插入链接](./assets/pb-tutorial1-text-link-insert.png){width="600" zoomable="yes"}

   - 完成后，单击 **[!UICONTROL OK]** 以保存链接。

     现在，横幅中会突出显示链接的文本。

     ![带有链接文本的横幅](./assets/pb-tutorial1-text-link-highlight.png){width="600" zoomable="yes"}

1. 在舞台的右上角，单击 _关闭全屏_ (![“关闭全屏”图标](./assets/pb-icon-reduce.png))图标。

   单击此图标会返回到 _[!UICONTROL Content]_显示预览的页面的部分。

1. 在右上角，单击 **[!UICONTROL Save]**.

### 步骤6：重新排列行

完成所有三行后，最后一步是重新排列行以匹配原始行 _简单页面_ 示例。 要与原始示例匹配，必须将第一行移至底部，将最后一行移至顶部。

1. 如有必要，请展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Content]** 部分。

1. 单击 **[!UICONTROL Edit with Page Builder]** 或位于内容预览区域内。

1. 将鼠标悬停在舞台上的第一行上以显示工具箱，然后选择 _移动_ ( ![“移动”图标](./assets/pb-icon-move.png))图标。

   ![移动](./assets/pb-tutorial1-row-toolbox-move.png){width="600" zoomable="yes"}

1. 在验证行中的所有内容均已选中时按住鼠标按钮，并将行拖到页面底部红色准则下方的位置。

   >[!NOTE]
   >
   >如果您意外只移动了部分内容（例如图像），则只需将内容移回其所属位置并重试。

   ![在舞台上移动行](./assets/pb-tutorial1-row-toolbox-move-to-position.png){width="600" zoomable="yes"}

1. 重复此过程以将第一行移动到第二位置。

   现在，页面中行的顺序与简单页面示例匹配。

1. 在舞台的右上角，单击 _关闭全屏_ (![“关闭全屏”图标](./assets/pb-icon-reduce.png))图标。

   单击此图标会返回到 _[!UICONTROL Content]_显示预览的页面的部分。

1. 在右上角，单击 **[!UICONTROL Save]** 箭头并选择 **[!UICONTROL Save & Close]**.

1. 如果出现提示，请单击 [缓存管理](../systems/cache-management.md) 链接页面顶部的消息，并刷新任何无效缓存。

您已完成简单页面练习。 保留您创建的工作，以便您稍后可以参考它。

准备就绪后，转到 [第2部分：块](2-blocks.md).

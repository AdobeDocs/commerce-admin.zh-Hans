---
title: '[!DNL Page Builder]演练第2部分：块'
description: 了解使用 [!DNL Page Builder]时简单块和动态块之间的区别。
exl-id: 864a3078-8cb3-4add-bdb7-14189aba535e
feature: Page Builder, Page Content
source-git-commit: 2299beb6c11af801076d3aff0b026d41b9dbd212
workflow-type: tm+mt
source-wordcount: '2073'
ht-degree: 0%

---

# [!DNL Page Builder]演练第2部分：块

以下练习说明了[简单块](../content-design/blocks.md)和[动态块](dynamic-block.md)之间的区别，以及如何使用[!DNL Page Builder]创建每种类型的块。

>[!NOTE]
>
>[!DNL Page Builder]具有名为&#x200B;_Banner_&#x200B;的新内容类型，该内容类型在第一个演练练习中有所介绍，与以前的横幅功能无关。 以前在[内容菜单](../content-design/content-menu.md)中的横幅选项现在是&#x200B;_动态块_。

店面中的![动态块](./assets/pb-tutorial2-dynamic-block-storefront.png){width="700" zoomable="yes"}

本练习假定您已完成[第1部分：简单页面](1-simple-page.md)，包括先决条件和[下载的示例文件](./assets/simple-page-assets.zip)。 按照顺序执行本演练的各个部分。

>[!NOTE]
>
>这些演练已更新，以反映对2.4.1版本中[!DNL Page Builder]工作区的近期更改。 如果您使用的是较早的Adobe Commerce版本，请使用[[!DNL Commerce] 2.3用户指南](https://docs.magento.com/user-guide/v2.3/cms/page-builder-learn.html)中包含的[!DNL Page Builder]练习。

## 第1部分：创建简单块

在本演练练习中，您将创建一个包含[!DNL Google Maps]中内容的简单块。 简单块有时称为&#x200B;_CMS块_&#x200B;或&#x200B;_静态块_，因为内容不会更改。 简单的块非常适用于您可能希望重复使用的内容。

### 步骤1：创建块

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Blocks]**。

1. 单击右上角的&#x200B;**[!UICONTROL Add New Block]**。

1. 对于&#x200B;**[!UICONTROL Block Title]**，输入`Google Map`。

1. 对于&#x200B;**[!UICONTROL Identifier]**，输入`google-map`。

1. 选择要提供块的&#x200B;**[!UICONTROL Store View]**。

   ![块信息](./assets/pb-tutorial2-block-new-google-map.png){width="600" zoomable="yes"}

1. 单击右上角的&#x200B;**[!UICONTROL Save]**。

### 步骤2：添加[!DNL Google Map]

1. 向下滚动到[!DNL Page Builder]内容预览（当前为空）并单击&#x200B;**[!UICONTROL Edit with Page Builder]**。

1. 在[!DNL Page Builder]面板中，展开&#x200B;**[!UICONTROL Media]**&#x200B;并将&#x200B;**[!UICONTROL Map]**&#x200B;占位符拖到舞台上。

   ![将地图拖到舞台](./assets/pb-media-map-drag.png){width="600" zoomable="yes"}

   如果为商店配置了[!DNL Google Maps]，则会显示商店位置的映射。

   ![为您的应用商店配置了Google Map](./assets/pb-tutorial2-google-map.png){width="600" zoomable="yes"}

   如果尚未为您的存储配置[!DNL Google Maps]，则会显示占位符映射。

   ![[!DNL Google Maps]占位符](./assets/pb-tutorial2-media-map-not-configured.png){width="600" zoomable="yes"}

1. 在舞台的右上角，单击&#x200B;_关闭全屏_ （![关闭全屏图标](./assets/pb-icon-reduce.png)）图标。

   单击此图标会返回块的&#x200B;_[!UICONTROL Content]_部分，并显示预览。

1. 单击右上角的&#x200B;**[!UICONTROL Save]**&#x200B;箭头并选择&#x200B;**[!UICONTROL Save & Close]**。

### 步骤3：配置[!DNL Google Maps]

如果已经为您的存储配置了[!DNL Google Maps]，则可以跳过此步骤并继续下一步。

1. 转到[Google Cloud Platform Console](https://console.cloud.google.com/google/maps-apis/overview)。

1. 单击项目下拉列表，然后选择或创建要为其添加API密钥的项目。

1. 要配置API凭据，请按照[!DNL Google Maps]文档中的[说明][1]操作。

1. 将API密钥复制到剪贴板。

1. 返回[!DNL Commerce]管理员并转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧面板中的&#x200B;_[!UICONTROL General]_下，选择&#x200B;**[!UICONTROL Content Management]**。

1. 展开![扩展选择器](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]**。

   ![高级内容工具](../configuration-reference/general/assets/content-management-advanced-content-tools.png){width="600" zoomable="yes"}

   有关[!UICONTROL Content Management Advanced Tools]配置选项的详细信息，请参阅&#x200B;[_配置参考指南_](../configuration-reference/general/content-management.md)。

1. 对于&#x200B;**[!UICONTROL Google Maps API Key]**，粘贴您复制的密钥。

1. 单击&#x200B;**[!UICONTROL Test Key]**。

   如果您的密钥有问题，请返回[!DNL Google Maps]平台网站以解决该问题。 然后，重试。

1. 验证密钥后，单击&#x200B;**[!UICONTROL Save Config]**。

### 步骤4：将块添加到页面

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**。

1. 在网格中，查找您在第一个教程中创建的&#x200B;_[!UICONTROL Simple Page]_，并在_[!UICONTROL Action]_&#x200B;列中选择&#x200B;**[!UICONTROL Edit]**。

1. 展开&#x200B;**[!UICONTROL Content]**&#x200B;部分的![扩展选择器](../assets/icon-display-expand.png)，然后单击&#x200B;**[!UICONTROL Edit with Page Builder]**&#x200B;或内容预览区域内。

1. 在&#x200B;_[!UICONTROL Layout]_下的[!DNL Page Builder]面板中，将&#x200B;**[!UICONTROL Row]**占位符拖到舞台顶部。

   ![将行添加到舞台顶部](./assets/pb-tutorial2-elements-row-drag-top.png){width="600" zoomable="yes"}

1. 在[!DNL Page Builder]面板中，展开&#x200B;**[!UICONTROL Add Content]**&#x200B;并将&#x200B;**[!UICONTROL Block]**&#x200B;占位符拖到新行中。

1. 将鼠标悬停在空的块容器上以显示工具箱，然后选择&#x200B;_设置_ （![设置图标](./assets/pb-icon-settings.png){width="20"} ）图标。

   ![块工具箱](./assets/pb-add-content-block-toolbox.png){width="600" zoomable="yes"}

1. 在“编辑块”页面上，单击&#x200B;**[!UICONTROL Select Block]**。

   ![选择块](./assets/pb-add-content-block-settings-block-select.png){width="600" zoomable="yes"}

1. 在搜索框中，输入`map`，然后按Enter/Return键查找您创建的块。

   ![在列表中查找块](./assets/pb-add-content-block-settings-block-find.png){width="600" zoomable="yes"}

1. 在网格中，单击&#x200B;**[!UICONTROL Select]**&#x200B;以选择[!DNL Google Maps]块。

1. 单击右上角的&#x200B;**[!UICONTROL Save]**&#x200B;以保存设置并返回[!DNL Page Builder]工作区。

1. 在舞台的右上角，单击&#x200B;_关闭全屏_ （![关闭全屏图标](./assets/pb-icon-reduce.png)）图标。

   单击此图标会返回该页面的&#x200B;_[!UICONTROL Content]_部分，并显示预览。

1. 单击右上角的&#x200B;**[!UICONTROL Save]**&#x200B;箭头并选择&#x200B;**[!UICONTROL Save & Close]**。

**恭喜！**&#x200B;您已完成“阻止”练习的第一部分。 请务必保留您的工作以备参考。

## 第2部分：创建动态块

动态块包括确定块出现的位置、时间和对象的逻辑。 在本演练练习中，您将为促销创建一个动态块，该块会在满足价格规则条件时触发，并且仅显示在特定客户区段中。 此示例的结果与第一个练习中创建的横幅类似，但有逻辑控制它何时出现在店面中。

![示例Luma Tee促销活动](./assets/pb-tutorial2-dynamic-block-row-page.png){width="600" zoomable="yes"}

### 第1步：创建新的动态块

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Dynamic Blocks]**。

   ![动态块列表](./assets/pb-tutorial2-block-dynamic-add.png){width="700" zoomable="yes"}

1. 单击右上角的&#x200B;**[!UICONTROL Add Dynamic Block]**。

   ![新建动态块页面](./assets/pb-tutorial2-block-dynamic-new.png){width="600" zoomable="yes"}

1. 完成新动态块的基本设置：

   - 将&#x200B;**[!UICONTROL Enable Dynamic Block]**&#x200B;设置为`Yes`。

   - 对于&#x200B;**[!UICONTROL Dynamic Block Name]**，输入`Tee Shirt Promo`。

   - 将&#x200B;**[!UICONTROL Dynamic Block Type]**&#x200B;设置为`Content Area`并单击&#x200B;**[!UICONTROL Done]**。

     动态块类型确定块在[页面布局](../content-design/page-layout.md)中的放置位置。 在为商店设置动态块时，请考虑页面布局和[主题](../content-design/themes.md)，以便更好地使用可用空间。 有些商店的活动内容区域仅限于固定宽度，而有些商店则扩展了屏幕的全宽。

     ![动态块类型设置](./assets/pb-dynamic-block-type.png){width="600" zoomable="yes"}

   - 对于&#x200B;**[!UICONTROL Customer Segment]**，选中要应用于动态块的每个区段的复选框，然后单击&#x200B;**完成**&#x200B;以保存区段列表。

     对于以下示例，有两个[客户区段](../customers/customer-segments.md)按性别识别注册客户。 此动态块仅会显示在注册女顾客在您的商店中购物时登录到其帐户中。

     ![选择客户区段](./assets/pb-dynamic-block-customer-segment.png){width="600" zoomable="yes"}

### 第2步：完成设置

向下滚动到&#x200B;_[!UICONTROL Content]_部分（显示空的[!DNL Page Builder]内容预览），然后单击&#x200B;**[!UICONTROL Edit with Page Builder]**。 然后，完成以下任务：

**任务1：**&#x200B;添加背景图像

1. 将鼠标悬停在行容器上以显示工具箱，然后选择&#x200B;_设置_ （![设置图标](./assets/pb-icon-settings.png){width="20"} ）图标。

1. 在&#x200B;_[!UICONTROL Appearance]_下，选择&#x200B;**[!UICONTROL Full Bleed]**。

1. 对于&#x200B;**[!UICONTROL Minimum Height]**，输入`400px`。

1. 滚动到&#x200B;_[!UICONTROL Background]_部分，并单击&#x200B;**[!UICONTROL Select from Gallery]**并选择第一个教程中上传的`wide-banner-background.png`图像来设置&#x200B;**[!UICONTROL Background Image]**。

1. 单击右上角的&#x200B;**[!UICONTROL Save]**&#x200B;以应用设置并返回到[!DNL Page Builder]工作区。

   包含图像的![行](./assets/pb-tutorial2-row-image.png){width="600" zoomable="yes"}

**任务2：**&#x200B;添加列

在&#x200B;_[!UICONTROL Layout]_下的[!DNL Page Builder]面板中，将&#x200B;**[!UICONTROL Column]**占位符拖到行上。

![将列类型拖入行](./assets/pb-tutorial2-column-drag.png){width="600" zoomable="yes"}

该行现在分为两列，每列的宽度相等。

**任务3：**&#x200B;添加文本

1. 在[!DNL Page Builder]面板中，展开&#x200B;**[!UICONTROL Elements]**&#x200B;并将&#x200B;**Text**&#x200B;占位符拖到第二列。

   ![将文本框拖到第二列](./assets/pb-tutorial2-column-text-drag.png){width="600" zoomable="yes"}

1. 在编辑器中输入以下三行文本：

   `Even more ways to mix and match.`

   `Buy 3 Luma tees and get a 4th free.`

   `Shop Tees >`

   ![输入列的文本](./assets/pb-tutorial2-column-text-editor.png){width="600" zoomable="yes"}

1. 选择所有三行文本并使用工具栏将&#x200B;**行高**&#x200B;设置为`40px`。

   ![设置行高](./assets/pb-tutorial2-column-text-editor-line-height.png){width="600" zoomable="yes"}

1. 按如下方式设置每行的&#x200B;**[!UICONTROL Font Size]**：

   | 折线图 | 字体大小 |
   |-----| ---------- |
   | 第1行： | `28px` |
   | 第2行： | `24px` |
   | 第3行： | `18px` |

   由于此块可放置在页面上的任何位置，因此请使用默认段落样式，而不是标题级别。 此外，不必担心列中文本尚未正确换行。  

   ![格式化文本](./assets/pb-tutorial2-column-text-editor-text-formatted.png){width="600" zoomable="yes"}

**任务4：**&#x200B;添加链接

在第一个练习中，您已了解如何使用[Button](buttons.md)内容类型来创建链接。 此示例说明如何从编辑器工具栏插入链接。

1. 在另一个浏览器选项卡中，打开店面并导航到将成为链接目标目标的页面。

   您可以使用完全限定的URL或省略对商店域的引用的相对URL。

   完整URL
： `https://mystore.com/women/tops-women/tees-women.html`

   相对URL
： `../women/tops-women/tees-women.html`

1. 返回到[!DNL Page Builder]工作区选项卡和文本编辑器，选择第三行中的`Shop Tees >`文本，然后在编辑器工具栏中选择&#x200B;**粗体** （![粗体按钮](./assets/editor-btn-bold.png)）。

1. 在第三行中仍选择`Shop Tees >`文本的情况下，在编辑器工具栏中选择&#x200B;**插入/编辑链接** （![插入/编辑链接按钮](./assets/pb-icon-add-link.png)）。

   ![插入链接](./assets/pb-tutorial2-column-text-editor-link-insert.png){width="600" zoomable="yes"}

1. 对于&#x200B;**[!UICONTROL URL]**，输入您准备的相对链接。

1. 将&#x200B;**[!UICONTROL Target]**&#x200B;设置为`None`。

   此设置将在同一浏览器窗口中打开页面，而不是打开新选项卡。

1. 对于&#x200B;**[!UICONTROL Title]**，输入`Shop Tees`。

   标题链接属性被某些浏览器用作工具提示。

1. 要保存链接并返回[!DNL Page Builder]工作区，请单击&#x200B;**[!UICONTROL OK]**。

   ![链接详细信息](./assets/pb-tutorial2-column-text-editor-link-insert-detail.png){width="600" zoomable="yes"}

1. 在舞台的右上角，单击&#x200B;_关闭全屏_ （![关闭全屏图标](./assets/pb-icon-reduce.png)）图标。

   单击此图标会返回动态块的&#x200B;_[!UICONTROL Content]_部分，并显示预览。

1. 单击右上角的&#x200B;**[!UICONTROL Save]**。

### 步骤3：添加价格规则

1. 在编辑模式下再次打开&#x200B;_T恤促销活动_&#x200B;动态块。

1. 展开![扩展选择器](../assets/icon-display-expand.png) **[!UICONTROL Related Promotions]**&#x200B;部分并单击&#x200B;**[!UICONTROL Add Cart Price Rules]**。

   ![相关促销活动](./assets/pb-dynamic-blocks-related-promotions.png){width="600" zoomable="yes"}

1. 在&#x200B;_添加相关购物车价格规则_&#x200B;页面上，选中&#x200B;_购买3件T恤衫的复选框，获取第4个免费_&#x200B;价格规则，然后单击&#x200B;**[!UICONTROL Add Selected]**。

   ![添加相关购物车价格规则](./assets/pb-dynamic-block-add-related-cart-price-rules.png){width="600" zoomable="yes"}

   价格规则显示在&#x200B;_相关购物车价格规则_&#x200B;下的&#x200B;_相关促销活动_&#x200B;部分中。 您可以将多个价格规则与一个动态块关联。 但是，这个简单的示例只使用一个。

   ![所选的购物车价格规则](./assets/pb-dynamic-block-related-cart-price-rule-list.png){width="600" zoomable="yes"}

1. 单击右上角的&#x200B;**[!UICONTROL Save]**。

### 步骤4：将动态块添加到页面

1. 在&#x200B;_管理员_&#x200B;侧边栏中，转到&#x200B;**[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**

1. 查找您在[第一次演练练习](1-simple-page.md)中创建的&#x200B;_简单页面_，并以编辑模式将其打开。

1. 展开![扩展选择器](../assets/icon-display-expand.png) **[!UICONTROL Content]**&#x200B;部分并单击&#x200B;**[!UICONTROL Edit with Page Builder]**。

1. 将鼠标悬停在与动态块具有相同图像的顶行上以显示工具箱和&#x200B;_删除_ （![删除图标](./assets/pb-icon-remove.png){width="20"} ）图标。

   要确认从页面中删除该行，请单击&#x200B;**[!UICONTROL OK]** 。

1. 在&#x200B;_[!UICONTROL Layout]_下的[!DNL Page Builder]面板中，将新的&#x200B;**[!UICONTROL Row]**占位符拖到舞台顶部。

1. 在[!DNL Page Builder]面板中，展开&#x200B;**[!UICONTROL Add Content]**&#x200B;并将&#x200B;**[!UICONTROL Dynamic Block]**&#x200B;占位符拖到新行中。

   ![将动态块拖到行上](./assets/pb-dynamic-block-drag.png){width="600" zoomable="yes"}

1. 将鼠标悬停在动态块容器上以显示工具箱并选择&#x200B;_设置_ （![设置图标](./assets/pb-icon-settings.png){width="20"} ）图标。

   ![动态块工具箱](./assets/pb-dynamic-block-settings.png){width="600" zoomable="yes"}

1. 在&#x200B;_[!UICONTROL Edit Dynamic Block]_页面上，单击&#x200B;**[!UICONTROL Select Dynamic Block]**。

   ![选择动态块](./assets/pb-dynamic-block-select.png){width="600" zoomable="yes"}

1. 查找您创建的&#x200B;_[!DNL Tee Shirt Promo]_动态块，然后单击&#x200B;**[!UICONTROL Select]**。

   下面显示了动态块信息的摘要。

   ![动态块信息](./assets/pb-tutorial2-dynamic-block-edit.png){width="600" zoomable="yes"}

1. 接受默认&#x200B;**[!UICONTROL Template]** `Dynamic Block Block Template`。

1. 完成后，单击&#x200B;**[!UICONTROL Save]**&#x200B;保存设置并返回[!DNL Page Builder]工作区。

   页面预览中的![动态块](./assets/pb-tutorial2-dynamic-block-on-page.png){width="600" zoomable="yes"}

1. 在舞台的右上角，单击&#x200B;_关闭全屏_ （![关闭全屏图标](./assets/pb-icon-reduce.png)）图标。

   单击此图标会返回该页面的&#x200B;_[!UICONTROL Content]_部分，并显示预览。

1. 单击右上角的&#x200B;**[!UICONTROL Save]**&#x200B;箭头并选择&#x200B;**[!UICONTROL Save & Close]**。

您已完成“块”练习的第二部分。 请务必保留您的工作以备参考。

## 第3部分：更新动态块

在本练习的最后一部分，就是当页面在您的商店中活动时，编辑动态块。 然后，以客户区段成员的身份登录商店，以显示块。

![店面中的动态块示例](./assets/pb-tutorial2-dynamic-block-storefront.png){width="600" zoomable="yes"}

### 步骤1：编辑动态块

1. 在&#x200B;_管理员_&#x200B;侧边栏中，转到&#x200B;**[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Dynamic Blocks]**。

1. 在网格中查找您的&#x200B;_[!DNL Tee Shirt Promo]_动态块，并在编辑模式下将其打开。

1. 展开![扩展选择器](../assets/icon-display-expand.png) **[!UICONTROL Content]**&#x200B;部分并单击&#x200B;**[!UICONTROL Edit with Page Builder]**。

1. 更改列宽：

   - 将鼠标悬停在两列之间的边框上。

   - 按住鼠标按钮并将边框向左拖动两个部分。

     ![网格分区](./assets/pb-tutorial2-dynamic-block-edit-column-width.png){width="600" zoomable="yes"}

     第一列是12个网格分区中的4个(4/12)，第二列是12个网格分区中的8个(8/12)。

     ![两个不相等的列](./assets/pb-tutorial2-dynamic-block-edit-column-width-changed.png){width="600" zoomable="yes"}

1. 更改文本颜色：

   - 选择前两行文本。

   - 在编辑器工具栏上，选择&#x200B;**[!UICONTROL Text Color]**&#x200B;并单击&#x200B;**[!UICONTROL White]**&#x200B;色板。

   ![文本颜色](./assets/pb-tutorial2-dynamic-block-edit-text-color.png){width="600" zoomable="yes"}

1. 在舞台的右上角，单击&#x200B;_关闭全屏_ （![关闭全屏图标](./assets/pb-icon-reduce.png)）图标。

   单击此图标会返回动态块的&#x200B;_[!UICONTROL Content]_部分，并显示预览。

1. 单击右上角的&#x200B;**[!UICONTROL Save]**。

### 步骤2：查看动态块

由于此动态块仅对特定客户区段的成员可见，因此您必须以客户区段成员的客户身份登录才能查看促销。 在此示例中，该块仅对女性客户显示。

1. 打开浏览器窗口到您的店面。

1. 要查看示例页面，请修改地址栏中的URL，如下所示：

   mystore.com/sample-page

   如果您的存储配置为包含html后缀，请按照以下方式包含该后缀：

   mystore.com/sample-page.html

1. 以女性客户身份登录：

   - 在主页右上角，单击&#x200B;**[!UICONTROL Sign In]**。

   - 如果您的系统上安装了示例Luma数据，请使用以下凭据：

     **[!UICONTROL Email]** - `roni_cost@example.com`

     **[!UICONTROL Password]** - `roni_cost3@example.com`

   - 单击&#x200B;**[!UICONTROL Sign In]**。

   - 返回到示例页面，以查看您在T恤促销活动中创建的动态块。

   为客户区段显示![动态块](./assets/pb-tutorial2-dynamic-block-storefront.png){width="700" zoomable="yes"}

您已完成“阻止”练习。 请务必保留您的工作以备参考。

准备就绪后，继续执行[第3部分：目录内容](3-catalog-content.md)

[1]: https://developers.google.com/maps/documentation/javascript/get-api-key

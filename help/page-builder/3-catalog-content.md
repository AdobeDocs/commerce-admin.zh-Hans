---
title: ’[!DNL Page Builder] 演练第3部分：目录内容
description: 了解如何将产品列表添加到 [!DNL Page Builder] 页面。
exl-id: f2a0dc29-6d8f-4b97-a947-72659c01d0cb
feature: Page Builder, Page Content
source-git-commit: 2299beb6c11af801076d3aff0b026d41b9dbd212
workflow-type: tm+mt
source-wordcount: '1481'
ht-degree: 0%

---

# [!DNL Page Builder] 演练第3部分：目录内容

本练习将演示向页面中添加产品列表、自定义产品页面以及创建添加以下项的自定义属性是多么的简单 [!DNL Page Builder] 工作区到产品属性集。

![产品列表](./assets/pb-add-content-products-list.png){width="600" zoomable="yes"}

本练习假定您已完成 [第1部分：简单页面](1-simple-page.md) 和 [第2部分：块](2-blocks.md)，包括先决条件和下载的示例文件。 按照顺序执行本练习的三个部分。

## 第1部分：添加产品列表

[!DNL Page Builder] 使得在舞台上添加产品列表更加容易。 在此示例中，产品列表直接添加到页面。

### 第1步：将产品列表添加到暂存环境

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. 查找 _简单页面_ 在第一个练习中创建并在第二个练习中修改的内容，然后选择 **[!UICONTROL Edit]** 在 _[!UICONTROL Action]_列。

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Content]** 部分并单击 **[!UICONTROL Edit with Page Builder]** 或位于内容预览区域内。

1. 在 [!DNL Page Builder] 下的面板 _[!UICONTROL Layout]_，拖动&#x200B;**[!UICONTROL Row]**到舞台的顶端。

1. 在 [!DNL Page Builder] 面板，展开 **[!UICONTROL Add Content]** 并拖动 **[!UICONTROL Products]** 新行的占位符。

   ![将产品占位符拖到行上](./assets/pb-add-content-products-drag.png){width="600" zoomable="yes"}

### 第2步：编写条件

1. 将鼠标悬停在空的产品容器上以显示工具箱，然后选择 _设置_ ( ![“设置”图标](./assets/pb-icon-settings.png){width="20"} )图标。

   ![产品工具箱](./assets/pb-add-content-products-toolbox.png){width="600" zoomable="yes"}

1. 对象 **[!UICONTROL Select Products By]**，选择 `Condition`.

1. 添加条件：

   - 单击 _添加_ (![“添加”图标](../assets/icon-add-green-circle.png))图标。

   - 下 _[!UICONTROL Product Attribute]_，选择&#x200B;**[!UICONTROL Category]**.

     ![选择条件的类别属性](./assets/pb-add-content-products-settings-condition.png){width="600" zoomable="yes"}

   - 完成 _[!UICONTROL Category is]..._ (通过单击更多(...)图标，然后单击 _选择器_ (![“选择器”图标](../assets/icon-list-chooser.png))图标。

     ![定义条件](./assets/pb-add-content-products-settings-condition-category-is.png){width="600" zoomable="yes"}

   - 在类别树中，向下展开至 **女性>上衣** 类别并选择 **T恤** 复选框。

     ![在树中选择类别](./assets/pb-add-content-products-settings-condition-category-tree.png){width="600" zoomable="yes"}

   - 单击复选标记(![复选标记图标](../assets/icon-checkmark-green-circle.png))图标。

     相应的类别ID将显示在字段中，以完成条件。

### 第3步：完成设置

1. 输入 **[!UICONTROL Number of Products to Display]**.

   默认情况下，该列表会显示五个产品。

1. 根据需要完成其余设置。

   如果需要，请使用字段末尾的描述 [添加内容 — 产品](products.md) 页面以供参考。

1. 完成后，单击 **[!UICONTROL Save]** 以保存设置并返回到 [!DNL Page Builder] 工作区。

   ![阶段中的产品列表](./assets/pb-add-content-products-list-stage.png){width="600" zoomable="yes"}

1. 在舞台的右上角，单击 _关闭全屏_ ( ![“关闭全屏”图标](./assets/pb-icon-reduce.png){width="20"} )图标。

   单击此图标会返回到 _[!UICONTROL Content]_显示预览的页面的部分。

1. 在右上角，单击 **[!UICONTROL Save]** 箭头并选择 **[!UICONTROL Save & Close]**.

## 第2部分：自定义产品页面

>[!NOTE]
>
>管理员用户必须具有 [!UICONTROL Content] 的权限 [角色范围](../systems/permissions-user-roles.md) 以查看 [!UICONTROL Edit with Page Builder] 按钮，并能够使用Page Builder。

在本练习的这一可选部分中，您将了解通过在产品页面的一组选项卡下方放置视频来自定义产品页面有多么简单。 更新的进程 [类别页面](../catalog/categories-content-settings.md) 内容基本相同。

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. 查找可用于此示例的简单产品，并在编辑模式下打开它。

1. 向下滚动并展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Content]** 部分。

1. 旁边 _[!UICONTROL Description]_，单击&#x200B;**[!UICONTROL Edit with Page Builder]**.

   ![产品描述内容](./assets/pb-catalog-product-content.png){width="600" zoomable="yes"}

   如果之前输入的产品描述没有 [!DNL Page Builder]，则当前描述将显示为HTML [HTML代码](html-code.md) 容器。 使用Luma主题，产品描述将显示在“详细信息”选项卡上。

1. 在 [!DNL Page Builder] 下的面板 _[!UICONTROL Layout]_，拖动&#x200B;**[!UICONTROL Row]**放到舞台上，将其放在HTML代码容器下方。

   当行处于正确位置时，查找要显示的红色指南。

   ![将行拖到舞台上](./assets/catalog-product-content-stage-row-drag.png){width="600" zoomable="yes"}

1. 在 [!DNL Page Builder] 面板，展开 **[!UICONTROL Media]** 并拖动 **[!UICONTROL Video]** 新行的占位符。

   ![行中的视频占位符](./assets/tutorial3-product-drag-video.png){width="600" zoomable="yes"}

1. 将鼠标悬停在空的视频容器上以显示工具箱，然后选择 _设置_ ( ![“设置”图标](./assets/pb-icon-settings.png){width="20"} )图标。

   ![视频工具箱](./assets/pb-tutorial3-product-video-toolbox.png){width="500" zoomable="yes"}

1. 输入 **[!UICONTROL Video URL]**.

   可以将视频托管在 [YouTube][1] 或 [Vimeo][2]. 此示例中的视频可以在YouTube上的以下URL找到：

   `https://www.youtube.com/watch?v=ZpFrNyD4100`

   ![编辑视频](./assets/pb-tutorial3-product-edit-video.png){width="500" zoomable="yes"}

1. 输入 **[!UICONTROL Maximum Width]** 用于视频显示的像素。

   如果将此选项留空，则视频会填充可用空间。

1. 单击 **[!UICONTROL Save]** 以保存设置并返回到 [!DNL Page Builder] 工作区。

   ![内容阶段的视频](./assets/pb-tutorial3-product-video.png){width="600" zoomable="yes"}

1. 在舞台的右上角，单击 _关闭全屏_ ( ![“关闭全屏”图标](./assets/pb-icon-reduce.png){width="20"} )图标。

   单击此图标会返回到 _[!UICONTROL Content]_显示预览的页面的部分。

1. 在右上角，单击 **[!UICONTROL Save]** 箭头并选择 **[!UICONTROL Save & Close]**.

在店面中，视频显示在选项卡组的下方。 要查看页面在移动设备上的外观，可以调整窗口大小。

![产品页面上显示的视频](./assets/pb-tutorial3-product-video-storefront.png){width="600" zoomable="yes"}

**恭喜！** 您已完成“目录内容”教程的第二部分。 保留您创建的工作，以便您稍后可以参考它。

## 第3部分：添加自定义属性

使用 [!DNL Page Builder] 用于添加完整功能的自定义属性 [!DNL Page Builder] 工作区到产品页面，您可以使用该页面创建吸引人的内容。 在本练习的这一可选部分中，您将了解如何使用 [!DNL Page Builder] 输入类型并将其应用于目录中的产品页面。 有关这些属性的详细信息，请参阅 [产品属性](../catalog/product-attributes.md).

### 步骤1：创建产品

要避免对实时商店进行更改，请使用所述的属性创建产品。

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. 在右上角，单击 **[!UICONTROL Add Product]**.

1. 创建具有以下属性的产品：

   - 
     [！UICONTROL属性集]: Default
   - [!UICONTROL Product Name]：我的产品
   - 
     [!UICONTROL SKU]: Tutorial
   - 
     [!UICONTROL Price]: 75.00
   - 
     [!UICONTROL Quantity]: 100
   - [!UICONTROL Stock Status]：有货
   - 
     [!UICONTROL Weight]: 1
   - [!UICONTROL Categories]：女性>上衣>T恤

1. 在右上角，单击 **[!UICONTROL Save]** 箭头并选择 **[!UICONTROL Save & Close]**.

### 步骤2：创建自定义属性

在此步骤中，您将创建两个新的自定义属性，以显示 [!DNL Page Builder] 和文本编辑器输入类型可以使用。

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. 在右上角，单击 **[!UICONTROL Add New Attribute]**.

1. 输入 **[!UICONTROL Default Label]** 属性的。

   在本例中，使用 `My Page Builder Attribute` 用于标签。

1. 设置 **[!UICONTROL Catalog Input Type for Store Owner]** 到 `Page Builder`.

   创建自定义属性时，您可以将最适合应用程序的编辑器指定为 `Page Builder` 或标准WYSIWYG `Text Editor`.

   ![[!DNL Page Builder] 输入类型](./assets/pb-attribute-page-builder.png){width="600" zoomable="yes"}

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Advanced Attribute Properties]** 部分，并进行以下设置：

   - [!UICONTROL Attribute Code]：使用连字符而不是空格输入小写字符的属性代码。 在本例中，使用 `my_page_builder_attribute`.
   - [!UICONTROL Scope]：接受默认值， `Store View`.
   - [!UICONTROL Default Value]：输入属性的默认值。
   - 
     [!UICONTROL Unique Value]: `No`
   - 
     [!UICONTROL Add to Column Options]: `No`
   - 
     [!UICONTROL Use in Filter Options]: `Yes`

1. 在 _[!UICONTROL Attribute Information]_左侧面板，选择&#x200B;**[!UICONTROL Storefront Properties]**并进行以下设置：

   - 
     [!UICONTROL Use for Promo Rule Conditions]: `Yes`
   - 
     [!UICONTROL Visible on Catalog Pages on Storefront]: `Yes`
   - 
     [!UICONTROL Used in Product Listing]: `Yes`

1. 完成后，单击 **[!UICONTROL Save Attribute]**.

1. 重复上述步骤，创建具有相同基本属性的第二个属性，但文本编辑器输入类型如下所示：

   - [!UICONTROL Default Label]：我的文本编辑器属性
   - [!UICONTROL Catalog Input Type for Store Owner]：文本编辑器
   - 
     [！UICONTROL属性代码]: `my_text_editor_attribute`

### 步骤3：更新产品属性集

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Attribute Set]**.

   在本例中，您临时将新属性添加到 `default` 属性集。 在本练习结束时，从属性集中删除属性，这样就不会影响您的目录。

   >[!NOTE]
   >
   >如果不想更改您的实时商店，您可以遵循操作，而无需更新属性集。

1. 查找 _[!UICONTROL Default]_属性集，并双击该属性以在编辑模式下将其打开。

1. 在 _未分配的属性_ 列表，查找您创建的新属性，并将每个属性拖到 _[!UICONTROL Groups]_列，下&#x200B;**[!UICONTROL Content]**.

   属性在中的位置 [!UICONTROL Groups] 列确定它在页面上的显示位置。

   ![添加到内容组的新属性](./assets/pb-product-attribute-set.png){width="600" zoomable="yes"}

1. 单击 **[!UICONTROL Save]** 以返回到“属性集”列表。

1. 出现提示时，单击 **[!UICONTROL Cache Management]** 链接页面，并刷新任何无效缓存。

### 步骤4：更新产品

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. 在“产品”网格中，查找 _我的产品_ 并在编辑模式下将其打开。

1. 向下滚动并展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Content]** 部分。

   在部分的顶部，有两个产品内容的标准属性：

   - _简要说明_，使用标准WYSIWYG [编辑者](../content-design/editor.md).
   - _描述_，其中显示 [!DNL Page Builder] 预览。

   ![产品内容](./assets/pb-product-content-edit-with-page-builder.png){width="600" zoomable="yes"}

   当您滚动到部分的下半部分时，您创建并分配了以下两个属性：

   - _我的 [!DNL Page Builder] 属性_，其中显示 [!DNL Page Builder] 预览。
   - _我的文本编辑器属性_，它使用标准的WYSIWYG编辑器。

   ![产品内容编辑](./assets/pb-product-content-my-attributes.png){width="600" zoomable="yes"}

1. 在 **我的文本编辑器属性** 编辑者，输入 `Text Editor Attribute placeholder text`.

   - 在右上角，单击 **[!UICONTROL Save]** 箭头并选择 **[!UICONTROL Save & Close]**.

1. 对象 **我的页面生成器属性**，单击 **[!UICONTROL Edit with Page Builder]** 并添加说明文本：

   - 在 [!DNL Page Builder] 面板，展开 **[!UICONTROL Elements]** 并拖动 **[!UICONTROL Text object]** 到舞台上。

   - 输入 `Page Builder attribute placeholder text`.

   - 在舞台的右上角，单击 _关闭全屏_ ( ![“关闭全屏”图标](./assets/pb-icon-reduce.png){width="20"} )图标。

     ![带有占位符文本的自定义属性](./assets/pb-product-content-attributes.png){width="600" zoomable="yes"}

1. 向上滚动到 **[!UICONTROL Description]**，单击 **[!UICONTROL Edit with Page Builder]**，并使用与上一步相同的方法添加您喜欢的任何文本。

1. 在产品页面的右上角，单击 **[!UICONTROL Save]** 箭头并选择 **[!UICONTROL Save & Close]**.

1. 如果出现提示，请单击 **[!UICONTROL Cache Management]** 链接页面顶部的消息，并刷新任何无效缓存。

### 步骤5：查看结果

1. 导航到店面的示例产品页面。

   在本例中，产品位于顶部导航中的“女性”>“上衣”>“T恤”下。

1. 向下滚动到 _我的页面生成器属性_ 信息。

   属性在产品页面上的位置由主题决定。 在Luma主题中，新属性位于产品描述之后。

   ![[!DNL Page Builder] 店面中的和文本编辑器属性](./assets/pb-storefront-product-attribute.png){width="600" zoomable="yes"}

您已完成 [!DNL Page Builder] “目录内容”练习。 保留您创建的工作，以便您稍后可以参考它。

[1]: https://www.youtube.com/
[2]: https://vimeo.com/

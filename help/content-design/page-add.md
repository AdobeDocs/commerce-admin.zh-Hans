---
title: 添加和删除页面
description: 了解如何添加和删除 [!DNL Commerce] 商店中使用的内容页面。
exl-id: a7a503ea-3631-4be2-81e4-aed2ae9419dc
badgePaas: label="仅限PaaS" type="Informative" url="https://experienceleague.adobe.com/zh-hans/docs/commerce/user-guides/product-solutions" tooltip="仅适用于云项目(Adobe管理的PaaS基础架构)和内部部署项目上的Adobe Commerce 。"
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '1122'
ht-degree: 0%

---

# 添加和删除页面

对于您可能要创建的任何类型的页面，将内容页面添加到商店的过程基本上相同。 您可以包含文本、图像、内容块、变量和小部件。 大多数内容页面都是先由搜索引擎设计，再由人设计，以供阅读。 在选择页面标题和URL，以及撰写元数据和内容时，请牢记这两个不同受众中每个受众的需求。 页面完成后，可将其添加到商店导航、链接到其他页面、从商店页脚链接，或用作新的[主页](page-home-new.md)。

![页网格](./assets/pages-grid.png){width="700" zoomable="yes"}

## 添加页面

以下说明将指导您完成每个步骤以创建基本页面。 某些高级功能将被跳过，但将在其他主题中介绍。

### 第1步：创建页面

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**。

1. 单击&#x200B;**[!UICONTROL Add New Page]**。

   ![新页面](./assets/pages-new-page.png){width="600" zoomable="yes"}

1. 如果不希望立即发布页面，请将&#x200B;**[!UICONTROL Enable Page]**&#x200B;设置为`No`。

1. 输入&#x200B;**[!UICONTROL Page Title]**。

   页面标题显示在[痕迹导航](../catalog/navigation-breadcrumb-trail.md)导航中。

### 第2步：完成内容

根据您的[高级内容工具配置](../configuration-reference/general/content-management.md)，添加页面内容。

#### 使用页面生成器内容工具

1. 展开![扩展选择器](../assets/icon-display-expand.png) **[!UICONTROL Content]**。

   使用页面生成器![内容](../page-builder/assets/pb-page-content.png){width="600" zoomable="yes"}

1. 在&#x200B;**[!UICONTROL Content Heading]**&#x200B;框中，输入要显示在页面顶部的标题。

   如果启用，[页面生成器](../page-builder/introduction.md)阶段和面板将显示在内容标题下方。 有关详细信息，请参阅[Workspace](../page-builder/workspace.md)。 如果未启用&#x200B;_页面生成器_，编辑器将在WYSIWYG模式下打开，工具栏位于顶部。

1. 填写内容，并根据需要设置文本格式。

#### 使用编辑器工具栏

1. 展开![扩展选择器](../assets/icon-display-expand.png) **[!UICONTROL Content]**。

   ![内容](./assets/page-content-editor.png){width="600" zoomable="yes"}

1. 在&#x200B;**[!UICONTROL Content Heading]**&#x200B;框中，输入要显示在页面顶部的标题。

1. 填写内容并根据需要设置文本格式。

   您可以根据需要添加[图像](media-storage.md)、[变量](../systems/variables-predefined.md)和[小组件](widgets.md)。 有关详细信息，请参阅[使用编辑器](editor.md)。

### 步骤3：完成SEO信息

1. 展开![扩展选择器](../assets/icon-display-expand.png) **[!UICONTROL Search Engine Optimization]**。

   ![搜索引擎优化](./assets/page-search-engine-optimization.png){width="600" zoomable="yes"}

1. 接受默认值或输入包含所有小写字符的其他&#x200B;**[!UICONTROL URL Key]**，并使用连字符而不是空格。

   默认URL密钥是在保存页面时创建的，且基于内容标题。

1. 为页面输入&#x200B;**[!UICONTROL Meta Title]**。

   元标题应包含少于70个字符，并显示在浏览器标题栏和选项卡中。

1. 输入您选择的高值&#x200B;**[!UICONTROL Meta Keywords]**，搜索引擎可以使用它来索引页面。

   用逗号分隔多个单词。 某些搜索引擎会忽略元关键字，但其他搜索引擎会使用元关键字。

1. 对于&#x200B;**[!UICONTROL Meta Description]**，为搜索结果列表输入页面的简要说明。

   理想情况下，描述长度应为150-160个字符，最大限制为255个字符。

1. 单击&#x200B;**[!UICONTROL Save]**。

### 步骤4：指定页面的范围

1. 展开![扩展选择器](../assets/icon-display-expand.png) **[!UICONTROL Page in Websites]**。

   网站中的![页](./assets/page-in-websites.png){width="600" zoomable="yes"}

1. 在&#x200B;**[!UICONTROL Store View]**&#x200B;列表中，选择页面可用的每个视图。

   如果安装有多个网站，请选择每个网站，然后在该页面可用的位置查看商店。

### 步骤5：标识父页面（如果适用）

{{ee-feature}}

1. 展开![扩展选择器](../assets/icon-display-expand.png) **[!UICONTROL Hierarchy]**。

   ![层次结构](./assets/page-hierarchy.png){width="600" zoomable="yes"}

1. 如果此页面是其他页面的子页面，请选中&#x200B;**[!UICONTROL Parent page]**&#x200B;的复选框。

### 步骤6：输入设计更改（可选）

1. 要更改页面的布局，请展开![扩展选择器](../assets/icon-display-expand.png) **[!UICONTROL Design]**。

   ![设计](./assets/page-design.png){width="600" zoomable="yes"}

1. 要更改页面的列布局，请将&#x200B;**[!UICONTROL Layout]**&#x200B;设置为以下任一项：

   - `Empty`
   - `1 column`
   - `2 columns with left bar`
   - `2 columns with right bar`
   - `3 columns`
   - `Page -- Full Width` （需要[页面生成器](../page-builder/introduction.md)）
   - `Category -- Full Width` （需要页面生成器）
   - `Product -- Full Width` （需要页面生成器）

1. 要应用&#x200B;**[!UICONTROL Custom Layout Update]**，请从列表中选择文件的名称。

   有关详细信息，请参阅[布局更新](layout-updates.md)。

1. 要更改页面主题，请将&#x200B;**[!UICONTROL New Theme]**&#x200B;设置为以下项之一：

   - `Magento Black`
   - `Magento Luma`

1. ![Magento Open Source](../assets/open-source.svg)(仅限Magento Open Source)要计划设计更改，请展开![扩展选择器](../assets/icon-display-expand.png) **[!UICONTROL Custom Design Update]**&#x200B;并执行以下操作：

   ![自定义设计更新](./assets/page-custom-design-update.png){width="600" zoomable="yes"}

   - 使用日历（![日历图标](../assets/icon-calendar.png)）选择更改生效的&#x200B;**[!UICONTROL From]**&#x200B;和&#x200B;**[!UICONTROL To]**&#x200B;日期。

   - 要将其他主题应用到页面，请选择&#x200B;**[!UICONTROL New Theme]**&#x200B;的名称。

   - 要更改页面的列布局，请选择要应用的&#x200B;**[!UICONTROL Layout]**。

### 步骤7：预览页面

1. 单击&#x200B;**[!UICONTROL Save]**&#x200B;箭头并选择&#x200B;**[!UICONTROL Save & Close]**&#x200B;以返回页面网格。

1. 在网格中查找该页面，并在&#x200B;_[!UICONTROL Action]_&#x200B;列中选择&#x200B;**[!UICONTROL View]**。

1. 要返回到网格，请单击浏览器窗口左上角的&#x200B;**[!UICONTROL Back]**。

### 步骤8：发布页面

1. 在网格的&#x200B;_[!UICONTROL Action]_&#x200B;列中选择&#x200B;**[!UICONTROL Edit]**。

1. 将&#x200B;**[!UICONTROL Enable Page]**&#x200B;设置为`Yes`。

1. 单击&#x200B;**[!UICONTROL Save]**&#x200B;箭头并选择&#x200B;**[!UICONTROL Save & Close]**。

## 复制页面

任何内容页面都可以用作模板，并另存为副本。 您可以使用此省时技术为整个网站中的内容页面创建一致的设计。 重复页面会保留原始页面的页面标题，但必须更新URL键和状态字段。

![保存并复制](./assets/page-duplicate-save-menu.png){width="600" zoomable="yes"}

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**。

1. 在网格中，找到要复制的页面，然后单击&#x200B;_[!UICONTROL Action]_&#x200B;列中的&#x200B;**[!UICONTROL Edit]**。

1. 单击&#x200B;**[!UICONTROL Save]**&#x200B;箭头并选择&#x200B;**[!UICONTROL Save & Duplicate]**。

1. 当您看到该页面已保存并复制的消息时，请单击顶部按钮栏中的&#x200B;**[!UICONTROL Back]**&#x200B;以返回到网格。

1. 在网格中找到重复页面，并注意以下事项：

   - 页面标题与原始页面相同。
   - 分配了唯一但临时的URL密钥。
   - 页面的状态为`Disabled`。

1. 以&#x200B;_编辑_&#x200B;模式打开重复页面，并执行以下操作：

   - 如果要立即发布页面，请将&#x200B;**[!UICONTROL Enable Page]**&#x200B;设置为`Yes`。

   - 根据需要更新&#x200B;**[!UICONTROL Page Title]**。

   - 展开![扩展选择器](../assets/icon-display-expand.png) **[!UICONTROL Search Engine Optimization]**&#x200B;部分并输入要用于重复页面的唯一&#x200B;**[!UICONTROL URL Key]**。

     ![临时URL密钥](./assets/page-search-engine-optimization-url-key-duplicate.png){width="600" zoomable="yes"}

   - 根据需要更新其余页面内容。

1. 单击&#x200B;**[!UICONTROL Save]**&#x200B;箭头并选择&#x200B;**[!UICONTROL Save & Close]**。

   网格中的重复页面反映了您所做的更改。

## 保存菜单

| 命令 | 描述 |
|--- |--- |
| [!UICONTROL Save] | 保存当前页面，然后继续工作。 |
| [!UICONTROL Save & New] | 保存并关闭当前页面，然后开始一个新页面。 |
| [!UICONTROL Save & Duplicate] | 保存并关闭当前页面，然后打开新的重复副本。 |
| [!UICONTROL Save & Close] | 保存并关闭当前页面，然后返回到“页面”网格。 |

{style="table-layout:auto"}

## 删除页面

有两种方法可删除已创建的页面。 您可以将其从&#x200B;_[!UICONTROL Pages]_&#x200B;网格或&#x200B;_[!UICONTROL Edit]_&#x200B;页面中删除。

### 方法1：从“页面”网格中删除页面

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**。

1. 使用网格上方的筛选器找到页面，然后选中要删除的一个或多个页面的复选框。

1. 在列表的左上角，将&#x200B;**[!UICONTROL Actions]**&#x200B;设置为`Delete`。

1. 要确认操作，请单击&#x200B;**[!UICONTROL OK]**。

### 方法2：从编辑页面中删除页面

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**。

1. 查找要删除的页面。

1. 在页面实体的&#x200B;_[!UICONTROL Actions]_&#x200B;列中，单击&#x200B;**[!UICONTROL Select]**&#x200B;并选择&#x200B;**[!UICONTROL Edit]**。

1. 在按钮栏中，单击&#x200B;**[!UICONTROL Delete Page]**。

1. 要确认操作，请单击&#x200B;**[!UICONTROL OK]**。

---
title: 布局更新
description: 了解如何使用布局更新来自定义页面布局。
exl-id: e2d8261f-cae1-4bd4-a047-f861dd7ca14e
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '1007'
ht-degree: 0%

---

# 布局更新

在开始使用自定义布局更新之前，请务必了解商店页面的构建方式以及术语之间的差异 *布局* 和 *布局更新*. 布局是指页面的视觉和结构组成。 布局更新是指一组特定的XML指令，这些指令可以覆盖或自定义页面的构建方式。

您的XML布局 [!DNL Commerce] 存储是容器和块的分层结构。 某些元素显示在每个页面上，而其他元素仅显示在特定页面上。 要了解有关布局、容器和块的更多信息，请参阅 [布局概述](https://developer.adobe.com/commerce/frontend-core/guide/layouts/) 在 _前端开发人员指南_.

此 [构件](widgets.md) 工具是添加现有内容的简单方法 [内容块](blocks.md) 到页面的默认布局。 要获得更高级的更新，您必须将XML布局更新代码保存在服务器上，然后作为自定义布局更新从管理员处引用该文件。 有关过程的概述，请参见 [使用布局更新](layout-updates.md#place-a-block-using-layout-updates).

在下图中，引用容器的名称为黑色，块类型（或块类路径）为蓝色。

![标准块布局图](./assets/page-layout-default.png){width="500" zoomable="yes"}

| 块类型 | 描述 |
|--- |--- |
| `page/html` | 此块的名称为 `root` 它是布局中少数几个根块之一。 您还可以创建自己的块并命名它 `root`，此类型的块的标准名称。 每页只能有一个此类型的块。 |
| `page/html_head` | 块名称为 `head` 它是根块的子项。 每个页面只能有一个此类型的块，并且不得将其删除。 |
| `page/html_notices` | 块名称为 `global_notices` 它是根块的子项。 如果从布局中删除此块，则全局通知不会显示在页面上。 每页只能有一个此类型的块。 |
| `page/html_header` | 块名称为 `header` 它是根块的子项。 此块对应于页面顶部的可视标题，并包含多个标准块。 每个页面只能有一个此类型的块，并且不得将其删除。 |
| `page/html_wrapper` | 尽管此块包含在默认布局中，但它已被弃用，并且仅为了确保向后兼容性而包含在默认布局中。 请勿使用此类型的块。 |
| `page/html_breadcrumbs` | 此块的名称为 `breadcrumbs` 它是标头块的子项。 此块显示当前页面的痕迹导航。 每页只能有一个此类型的块。 |
| `page/html_footer` | 块名称为 `footer` 它是根块的子项。 页脚块对应于页面底部的可视页脚，并包含多个标准块。 每个页面只能有一个此类型的块，并且不得将其删除。 |
| `page/template_links` | 标准布局中有两个此类型的块。 此 `top.links` 块是标题块的子项，对应于顶部导航菜单。 此 `footer_links` 块是页脚块的子项，对应于底部导航菜单。 <br/><br/>**_注意：_**可以操作模板链接，如示例中所示。 |
| `page/switch` | 在标准布局中有两个此类型的块。 此 `store_language` 块是标头块的子项，对应于顶部语言切换器。 此 `store_switcher` 块是页脚块的子项，对应于底部存储切换器。 |
| 核心/消息 | 在标准布局中有两个此类型的块。 此 `global_messages` 块显示全局消息。 此 `messages` 块用于显示所有其他消息。 如果删除这些块，客户将看不到任何消息。 |
| `core/text_list` | 这种类型的块在整个 [!DNL Commerce] 作为呈现子块的占位符。 |
| `core/profiler` | 每页只有一个此类块的实例。 它用于内部 [!DNL Commerce] profiler和不应用于任何其他目的。 |

{style="table-layout:auto"}

## 使用布局更新放置块

[布局更新](layout-updates.md) 可以自定义页面布局。 布局更新比 [构件](widgets.md)，但需要访问服务器并具备XML基础知识。

以下步骤显示如何使用版面更新在页面上放置块。 有关特定示例和语法帮助，请参阅 [常见版面自定义任务](https://developer.adobe.com/commerce/frontend-core/guide/layouts/) 在 _前端开发人员指南_.

### 第1步：创建块

1. 创建 [块](block-add.md) 你想摆放的。

1. 请注意 `block_id`，因为它用在布局更新说明中。

### 步骤2：使用XML编写布局更新

1. 以XML格式编写布局说明 [引用CMS块](https://developer.adobe.com/commerce/frontend-core/guide/layouts/xml-manage/).

1. 保存 [布局说明](https://developer.adobe.com/commerce/frontend-core/guide/layouts/xml-instructions/) 位于为主题保存XML文件的布局文件夹中的服务器上。

   例如：

   `<theme_dir>/<Namespace>_<Module>/layout`

   布局句柄是以开头的文件名 `cms_page_view_selectable_`，后跟CMS页面的URL键、布局更新选项和 `xml` 文件后缀。 在以下示例中， `customer-service` 是页面的URL键，并且 `ChatTool` 是您选择用于将布局更新应用到页面的选项。

   `cms_page_view_selectable_`&lt;`customer-service`>`_`&lt;`ChatTool`>`.xml`

   | 元素 | 描述 |
   |--- |--- |
   | CMS页面标识符 | 包含任何正斜杠(`/`)替换为下划线(`_`)。 |
   | 布局更新名称 | 显示的选项 _自定义布局更新_. |

   {style="table-layout:auto"}

### 步骤3：从页面引用布局更新

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. 查找要放置块的页面，并在编辑模式下打开该页面。

1. 向下滚动并展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Design]** 部分。

1. 要显示与页面关联的所有可用布局更新，请单击 **[!UICONTROL Custom Layout Update]** 菜单。

   ![自定义布局更新列表](./assets/page-design-custom-layout-update.png){width="400" zoomable="yes"}

1. 选择要应用于页面的布局更新。

### 步骤4：保存并刷新缓存

1. 完成后，单击 **[!UICONTROL Save & Close]**.

1. 在工作区顶部的消息中，单击 **[!UICONTROL Cache Management]** 并刷新所有无效的缓存项目。

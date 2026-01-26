---
title: 元素 — 按钮
description: 了解Buttons内容类型，用于在 [!DNL Page Builder] 阶段中添加单个按钮或一组按钮。
exl-id: 9f1681c5-04b0-4259-aaf6-5d8081bd8cdb
feature: Page Builder, Page Content
source-git-commit: cace9d1de00955494d8bc607c017778ff7df4806
workflow-type: tm+mt
source-wordcount: '1586'
ht-degree: 0%

---

# 元素 — 按钮

使用&#x200B;_按钮_&#x200B;内容类型在[[!DNL Page Builder] 阶段](workspace.md#stage)中添加单个按钮或一组按钮。 您可以水平或垂直排列按钮，并将它们直接添加到舞台上的行、列、选项卡和横幅中。

店面上有按钮的![横幅](./assets/pb-storefont-banner-with-button.png){width="600" zoomable="yes"}

{{$include /help/_includes/page-builder-save-timeout.md}}

## 工具箱

在使用“按钮”内容类型时，您可以添加和编辑单个按钮以及包含一个或多个按钮的按钮容器。 每个模板都有自己的工具箱，用于设计[!DNL Page Builder]舞台上的按钮。

### 单个按钮工具箱

![按钮工具箱](./assets/pb-elements-button-settings.png){width="500" zoomable="yes"}

| 工具 | 图标 | 描述 |
| --------- | -------- | -------------- |
| 设置 | ![设置图标](./assets/pb-icon-settings.png){width="25"} | 打开“编辑按钮”页面，您可以在该页面中更改按钮的属性。 |
| 复制 | ![图标重复](./assets/pb-icon-duplicate.png){width="25"} | 创建按钮副本。 |
| 移除 | ![删除图标](./assets/pb-icon-remove.png){width="25"} | 从舞台上删除按钮。 |

{style="table-layout:auto"}

### 按钮容器工具箱

![按钮容器工具箱](./assets/pb-elements-buttons-toolbox-settings.png){width="500" zoomable="yes"}

| 工具 | 图标 | 描述 |
| --------- | ----------------- | ----------- |
| 移动 | ![移动图标](./assets/pb-icon-move.png){width="25"} | 将按钮容器移至页面上的另一个有效位置。 |
| 添加 | ![添加图标](./assets/pb-icon-add-button.png){width="25"} | 向容器添加按钮。 |
| （标签） | 按钮 | 将当前容器标识为按钮元素。 |
| 设置 | ![设置图标](./assets/pb-icon-settings.png){width="25"} | 打开“编辑按钮”页面，您可以在此页面更改容器的属性。 |
| 隐藏 | ![隐藏图标](./assets/pb-icon-hide.png){width="25"} | 隐藏按钮容器。 |
| 显示 | ![显示图标](./assets/pb-icon-show.png){width="25"} | 显示隐藏按钮容器。 |
| 复制 | ![图标重复](./assets/pb-icon-duplicate.png){width="25"} | 复制按钮容器。 |
| 移除 | ![删除图标](./assets/pb-icon-remove.png){width="25"} | 从舞台中删除按钮容器及其内容。 |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## 添加单个按钮

1. 在[!DNL Page Builder]面板中，展开&#x200B;**[!UICONTROL Elements]**&#x200B;并将&#x200B;**[!UICONTROL Buttons]**&#x200B;占位符拖到舞台上的行、列或选项卡集中。

   ![将按钮拖到舞台上](./assets/pb-elements-button-drag.png){width="500" zoomable="yes"}

1. 将鼠标悬停在按钮上以显示工具箱，然后选择&#x200B;_设置_ （![设置图标](./assets/pb-icon-settings.png)）图标。

1. 输入要显示在按钮上的&#x200B;**[!UICONTROL Button Text]**。

   ![基本按钮设置](./assets/pb-elements-button-settings-button-text.png){width="600" zoomable="yes"}

1. 将&#x200B;**[!UICONTROL Button Type]**&#x200B;设置为以下项之一：

   | 类型 | 描述 |
   | ------ | ----------- |
   | `Primary` | 从当前样式表中应用主按钮样式。 |
   | `Secondary` | 应用当前样式表中的辅助按钮样式（如果适用）。 |
   | `Link` | 创建超链接而不是按钮。 |

   {style="table-layout:auto"}

   ![主按钮和辅助按钮示例](./assets/pb-elements-button-settings-button-primary-secondary.png){width="500" zoomable="yes"}

1. 使用以下类型之一设置&#x200B;**[!UICONTROL Button Link]**：

   - **[!UICONTROL URL]** — 输入链接的目标URL。

     URL可以是商店中产品或页面的相对链接，也可以是完全限定的URL。

     相对URL示例 — `../luma-analog-watch.html`

     完全限定的URL示例 — `http://mystore.com/luma-analog-watch.html`

     如果链接指向其他网站，则可以在新的浏览器选项卡中打开该链接，以保持当前页面对商店开放。

     要阻止访客离开您的商店，请选中&#x200B;**[!UICONTROL Open in new tab]**&#x200B;复选框。

   - **[!UICONTROL Product]** — 输入产品名称（部分或完整）或SKU，然后在列表中选择产品名称。

     >[!NOTE]
     >
     >产品根据&#x200B;_显示缺货产品_&#x200B;设置显示在列表中。 对于使用[Inventory management](../inventory-management/introduction.md)的多Source商家，产品列表仅受分配给默认网站的源的限制。

     ![为按钮链接选择产品](./assets/pb-elements-button-settings-button-link-product-search.png){width="600" zoomable="yes"}

   - **[!UICONTROL Category]** — 输入类别名称（部分或完整）或单击空白字段以显示类别树。 然后，在树中选择类别名称。

     ![为按钮链接选择类别](./assets/pb-elements-button-settings-button-link-category-search.png){width="600" zoomable="yes"}

   - **[!UICONTROL Page]** — 输入CMS页面的名称（部分或完整），或者单击空白字段以显示完整列表。 然后，在搜索结果列表中选择该页面的名称。

     ![为按钮链接选择CMS页面](./assets/pb-elements-button-settings-button-link-page-search.png){width="600" zoomable="yes"}

1. 根据需要完成[高级设置](#change-advanced-settings)。

1. 完成后，单击右上角的&#x200B;**[!UICONTROL Save]**&#x200B;以应用设置并返回到[!DNL Page Builder]工作区。

## 添加一组按钮

以下各节将介绍一系列步骤，这些步骤将从单个按钮开始，并在按钮容器中创建一组三个按钮。 如果您还没有单独的按钮，请按照之前的说明将单独的按钮添加到舞台。

### 步骤1：创建第二个按钮

1. 将鼠标悬停在按钮容器上以显示工具箱，然后选择&#x200B;_添加_ （![添加图标](./assets/pb-icon-add-button.png){width="20"} ）图标。

   ![正在添加另一个按钮](./assets/pb-elements-buttons-toolbox-add.png){width="500" zoomable="yes"}

1. 输入要显示在第二个按钮上的文本。

1. 单击“新建”按钮以显示其工具箱，然后选择&#x200B;_设置_ （![设置图标](./assets/pb-icon-settings.png){width="20"} ）图标。

   ![正在编辑按钮](./assets/pb-elements-button-set-edit-button2-toolbox.png){width="500" zoomable="yes"}

1. 将&#x200B;**[!UICONTROL Button Type]**&#x200B;设置为`Secondary`。

1. 根据需要设置&#x200B;**[!UICONTROL Button Link]**。

   在以下示例中，链接是转到[联系我们](../getting-started/store-details.md#contact-us-form)页面的相对URL。

   ![联系我们按钮设置](./assets/pb-elements-button-set-edit-button2-toolbox-settings.png){width="600" zoomable="yes"}

1. 根据需要完成[高级设置](#change-advanced-settings)。

1. 完成后，单击&#x200B;**[!UICONTROL Save]**&#x200B;以应用设置并返回到[!DNL Page Builder]工作区。

### 第2步：创建第三个按钮

1. 再次单击舞台上的第二个按钮，然后选择&#x200B;_复制_ （![复制图标](./assets/pb-icon-duplicate.png){width="20"} ）图标。

   ![复制按钮](./assets/pb-elements-button-set-contact-us-toolbox-duplicate.png){width="500" zoomable="yes"}

1. 输入要显示在第三个按钮上的文本。

1. 单击第三个按钮以显示工具箱，然后选择&#x200B;_设置_ （![设置图标](./assets/pb-icon-settings.png){width="20"} ）图标。

   第三个按钮的![工具箱](./assets/pb-elements-button-set-find-us-toolbox-settings.png){width="500" zoomable="yes"}

1. 根据需要更新&#x200B;**[!UICONTROL Button Link]**。

1. 单击右上角的&#x200B;**[!UICONTROL Save]**&#x200B;以应用设置并返回到[!DNL Page Builder]工作区。

### 步骤3：更新按钮容器

1. 将鼠标悬停在按钮容器上以显示工具箱，然后选择&#x200B;_设置_ （ ![设置图标](./assets/pb-icon-settings.png){width="20"} ）图标。

   ![按钮容器工具箱](./assets/pb-elements-buttons-toolbox-settings.png){width="500" zoomable="yes"}

1. 在&#x200B;_[!UICONTROL Appearance]_&#x200B;下，选择&#x200B;**[!UICONTROL Stacked]**。

1. 将&#x200B;**[!UICONTROL All Buttons are same size]**&#x200B;设置为`Yes`。

   ![大小相同的栈叠按钮](./assets/pb-elements-buttons-settings-appearance-stacked.png){width="300"}

1. 使用[更改按钮容器](#change-settings-for-a-button-container)的设置中的说明根据需要更新其余设置。

1. 完成后，单击&#x200B;**[!UICONTROL Save]**&#x200B;以应用设置并返回到[!DNL Page Builder]工作区。

   舞台上将显示完整的栈叠按钮集，其中包含一个主按钮和两个辅助按钮。

   舞台上的![栈叠按钮](./assets/pb-elements-buttons-stacked.png){width="500" zoomable="yes"}

## 移动按钮

1. 单击要移动的按钮。

1. 选择按钮的移动（![移动图标](./assets/pb-icon-move.png){width="20"} ）图标（显示在按钮文本的前面）并将其拖动到按钮容器内按钮的新位置。

   ![移动按钮](./assets/pb-elements-button-set-move-button.png){width="500" zoomable="yes"}

## 更改按钮的设置

1. 单击舞台上的按钮以显示工具箱，然后选择&#x200B;_设置_ （ ![设置图标](./assets/pb-icon-settings.png){width="20"} ）图标。

   ![按钮工具箱](./assets/pb-elements-button-toolboxes.png){width="500" zoomable="yes"}

1. 根据需要更新标准设置。

   - **[!UICONTROL Button Text]** — 输入要显示在按钮上的文本（也可以直接从舞台更新）。

   - **[!UICONTROL Button Type]** — 确定按钮格式。

     | 类型 | 描述 |
     | ------ | ----------- |
     | `Primary` | 从当前样式表中应用主按钮样式。 |
     | `Secondary` | 应用当前样式表中的辅助按钮样式（如果适用）。 |
     | `Link` | 创建超链接而不是按钮。 |

     {style="table-layout:auto"}

   - **[!UICONTROL Button Link]** — 确定单击按钮时提供的目标页面。

     | 选项 | 描述 |
     | ------ | ----------- |
     | `URL` | 使用相对或完全限定的URL来标识目标页面。 |
     | `Product` | 基于产品名称或SKU标识目标页面。 可以根据部分名称或全名搜索产品名称。 然后从搜索结果列表中选择产品。 |
     | `Category` | 将目标页面标识为类别树中的特定类别或子类别。 |
     | `Page` | 将目标页面标识为特定的CMS页面。 |

     {style="table-layout:auto"}

1. 根据需要完成[高级设置](#change-advanced-settings)。

1. 要保存设置并返回[!DNL Page Builder]工作区，请单击右上角的&#x200B;**[!UICONTROL Save]**。

## 更改按钮容器的设置

1. 将鼠标悬停在按钮容器上以显示工具箱，然后选择&#x200B;_设置_ （ ![设置图标](./assets/pb-icon-settings.png){width="20"} ）图标。

1. 根据需要更新&#x200B;**[!UICONTROL Appearance]**&#x200B;设置。

   - 使用排列选项在容器中水平或垂直显示按钮：

     | 选项 | 描述 |
     | ------ | ----------- |
     | `Inline` | 水平排列按钮。 |
     | `Stacked` | 垂直排列按钮。 |

     {style="table-layout:auto"}

   - 根据您的喜好设置&#x200B;**[!UICONTROL All buttons are same size]**&#x200B;选项。

     当设置为`Yes`时，容器中的所有按钮根据最长按钮文本的长度而具有一致的大小。

1. 根据需要完成[高级设置](#change-advanced-settings)。

1. 完成后，单击&#x200B;**[!UICONTROL Save]**&#x200B;以应用设置并返回到[!DNL Page Builder]工作区。

## 更改高级设置

您可以修改单个按钮和按钮容器的&#x200B;_[!UICONTROL Advanced]_&#x200B;设置。

1. 若要控制父容器中的位置，请选择&#x200B;**[!UICONTROL Alignment]**：

   | 选项 | 描述 |
   | ------ | ----------- |
   | `Default` | 应用在当前主题的样式表中指定的对齐默认设置。 |
   | `Left` | 将内容沿父容器的左边框对齐，并允许使用指定的任何边距。 |
   | `Center` | 将内容与父容器的中心对齐，并允许指定的任何边距。 |
   | `Right` | 将内容沿父容器的右边框对齐，并允许使用指定的任何边距。 |

   {style="table-layout:auto"}

1. 设置应用于按钮或按钮容器所有四边的&#x200B;**[!UICONTROL Border]**&#x200B;样式：

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

1. 如果设置了除`None`之外的边框样式，请完成边框显示选项：

   | 选项 | 描述 |
   | ------ |------------ |
   | [!UICONTROL Border Color] | 通过选择色板、单击拾色器或输入有效的颜色名称或等效的十六进制值来指定颜色。 |
   | [!UICONTROL Border Width] | 输入边框线条宽度的像素数。 |
   | [!UICONTROL Border Radius] | 输入像素数，以定义用于使边框每个角倒圆角的半径大小。 |

   {style="table-layout:auto"}

1. （可选）从当前样式表中指定要应用于按钮或按钮容器的&#x200B;**[!UICONTROL CSS classes]**&#x200B;的名称。

   用空格分隔多个类名。

1. 输入&#x200B;**[!UICONTROL Margins and Padding]**&#x200B;的值（以像素为单位），以确定按钮或按钮容器的外边距和内边距。

   在图表中输入相应的值。

   | 容器区域 | 描述 |
   | -------------- | ----------- |
   | [!UICONTROL Margins] | 应用于容器所有边的外边缘的空白空间量。 选项： `Top` / `Right` / `Bottom` / `Left` |
   | [!UICONTROL Padding] | 应用于容器所有边的内边缘的空白空间量。 选项： `Top` / `Right` / `Bottom` / `Left` |

   {style="table-layout:auto"}


<!-- Last updated from includes: 2023-09-11 14:30:19 -->

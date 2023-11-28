---
title: 添加内容 — 产品
description: 了解产品内容类型，用于向添加产品列表 [!DNL Page Builder] 暂存。
exl-id: 8ef38669-a6f6-493b-b963-b0fc4e3bbff4
feature: Page Builder, Page Content, Products
source-git-commit: 167e9d906cebb645f76a5112fa629a73ba823ebc
workflow-type: tm+mt
source-wordcount: '1912'
ht-degree: 0%

---

# 添加内容 — 产品

使用 _产品_ 内容类型，用于将产品列表添加到 [[!DNL Page Builder] 阶段](workspace.md#stage)，使用网格或轮播布局。 使用 [添加内容 — 阻止](block.md) 用于将块放置在 [!DNL Page Builder] 暂存，然后将产品列表放入块中。 或者，您也可以直接在页面的一行中添加产品列表。

## 使用产品轮播的准则

产品轮播提供了一种强大而引人入胜的方式展示您的产品。 为了充分利用，建议遵循以下准则：

- 将产品轮播直接添加到页面宽度容器，如行、选项卡或一列布局。 使用页面宽度布局可确保产品得到最佳的响应式显示。 [!DNL Page Builder] 根据页面宽度而非容器宽度减少显示的产品数。

- 不要将产品轮播添加到窄列。 如前所述， [!DNL Page Builder]默认情况下，会根据页面宽度而不是列宽确定要显示的产品数量。

- 如果您希望产品轮播连续自动滚动，请设置两者 **[!UICONTROL Autoplay]** 和 **[!UICONTROL Infinite Loop]** 到 `Yes`. 如果自动播放设置为 `Yes` 但“无限循环”设置为 `No`，产品列表末尾将自动滚动停止。

- 设置 **[!UICONTROL Carousel Mode]** 到 `Continuous` 在轮盘中一次高亮、居中和滚动一个产品。 其他产品在列表中是可见的，但为突出显示居中的产品，其他产品是透明的。

  ![连续轮播模式下的产品列表](./assets/pb-products-settings-carousel-continuous.png){width="600"}

- 要在轮盘中一次显示和滚动最多五个产品，请保留 **[!UICONTROL Carousel Mode]** 设置为 `Default`.

  ![默认轮播模式下的产品列表](./assets/pb-products-settings-carousel-default.png){width="600"}

以下说明显示如何将Products列表添加到块。 然后，您可以使用 [构件](../content-design/widgets.md) 将块放置在商店中任何页面上的特定位置。

{{$include /help/_includes/page-builder-save-timeout.md}}

## 产品工具箱

| 工具 | 图标 | 描述 |
| --------- | ------------- | ----------------- |
| 移动 | ![“移动”图标](./assets/pb-icon-move.png){width="25"} | 将产品容器及其内容移动到舞台上的另一个位置。 |
| 设置 | ![“设置”图标](./assets/pb-icon-settings.png){width="25"} | 打开 _编辑产品_ 页面，您可以在此页面中选择产品列表并更改容器的属性。 |
| 隐藏 | ![“隐藏”图标](./assets/pb-icon-hide.png){width="25"} | 隐藏当前产品容器及其内容。 |
| 显示 | ![显示图标](./assets/pb-icon-show.png){width="25"} | 显示隐藏的产品容器及其内容。 |
| 复制 | ![“复制”图标](./assets/pb-icon-duplicate.png){width="25"} | 制作产品容器及其内容的副本。 |
| 移除 | ![“删除”图标](./assets/pb-icon-remove.png){width="25"} | 从阶段中删除产品容器及其内容。 |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## 创建产品列表块

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Blocks]**.

1. 单击 **[!UICONTROL Add New Block]**.

1. 输入 **[!UICONTROL Block Title]** 和 **[!UICONTROL Identifier]**.

1. 选择 **[!UICONTROL Store View]** 块可用的位置。

1. 向下滚动并单击 **[!UICONTROL Edit with Page Builder]** 或在内容预览区域内打开 [!DNL Page Builder] 工作区。

1. 在 [!DNL Page Builder] 面板，展开 **[!UICONTROL Add Content]** 并拖动 **[!UICONTROL Products]** 舞台占位符。

   ![添加产品内容类型](./assets/pb-add-content-products-drag.png){width="600" zoomable="yes"}

## 配置产品列表容器

将鼠标悬停在空上 _产品_ 容器以显示工具箱，然后单击 _设置_ (![“设置”图标](./assets/pb-icon-settings.png){width="20"} )图标。

![产品工具箱](./assets/pb-add-content-products-toolbox.png){width="500" zoomable="yes"}

完成 _设置_ 根据以下各节：

### 外观

1. 要确定产品列表在页面上的显示方式，请选择以下外观类型之一：

   | 类型 | 描述 |
   | ---- | ----------- |
   | 产品网格 | 显示网格中的产品，其中每行显示五个产品（默认情况下），每个产品包含显示中输入的数字所需的行数。 **[!UICONTROL Number of Products to Display]** 设置。 |
   | 产品轮播 | 显示轮盘中的产品（也称为滑块）。 每张幻灯片最多可显示五个产品。 <br/><br/>**响应性警报**：选择此外观时，最好直接将Products内容类型添加到其响应式所在的行、选项卡或一列布局中，在较小的屏幕上每侧显示较少的产品。 如果将其添加到宽度小于页面宽度的内容类型（例如窄列），则无论屏幕大小如何，轮盘每张幻灯片显示的产品都会超过容器允许的数量。 |

   {style="table-layout:auto"}

   ![产品外观](./assets/pb-products-appearances.png){width="300"}

   如果您选择产品轮播，则还必须配置 [轮播设置](#carousel-settings).

1. 对象 **[!UICONTROL Select Products By]**，选择产品选择方法：

   您可以按类别、SKU或条件选择产品。 这些选项相互排斥。 例如，您无法依次选择类别选项和类别选择器，然后再切换到条件选项以添加某些条件。 您的产品仅基于您设置的内容进行选择 _一_ 这三种选择。

   - **[!UICONTROL Category]**  — 选择此选项可显示使用选定类别的产品。

     ![按类别的产品选择](./assets/pb-products-settings_category.png){width="500"}

     选中后，此选项将提供 **[!UICONTROL Category]** 选择器。 单击箭头并向下展开以选择要显示的产品类别。 例如，在 [!DNL Commerce] 示例数据，钻取并选择 _女性>上衣>T恤_ 显示该类别的所有产品。

     ![选择目录类别](./assets/pb-select-products-by-category.png){width="500"}

   - **[!UICONTROL SKU]**  — 选择此选项可显示使用一个或多个SKU的产品

     选中后，此选项将提供 **[!UICONTROL Product SKUs]** 文本框，您必须在该框中输入要显示的SKU的逗号分隔列表。

     ![按SKU的产品选择](./assets/pb-products-settings_sku.png){width="500"}

   - **[!UICONTROL Condition]**  — 选择此选项可根据您定义的一个或多个条件显示产品。

     选中后，便可使用一些工具将条件添加到您的产品选择中。 例如，您只能选择将性别设置为Unisex的产品。

     ![按条件划分的产品选择](./assets/pb-products-settings_condition.png){width="500"}

     >[!NOTE]
     >
     >选择类别或SKU选项可提供 **[!UICONTROL Sort By]** 选项 `Position`. 使用此排序选项，产品会以它们在目录中的显示顺序显示。</br>
     >
     >对于“类别”选项，按位置排序会按照产品在目录中的显示顺序来显示产品。 对于SKU选项，按位置排序将按您在以下位置输入的顺序显示产品： **[!UICONTROL Product SKUs]** 文本框。

1. 对象 **[!UICONTROL Sort By]**，选择列表中产品的排序顺序：

   | 选项 | 描述 |
   | ------ | ----------- |
   | `Position` （仅适用于类别和SKU选项） | 选择“类别”选项时，位置会按照产品在目录中的位置显示的顺序显示产品。 选择SKU选项后，职位会按照与产品SKU文本框中的SKU相同的顺序显示产品。 |
   | `Newest products first` | 按产品添加到目录的日期对产品进行排序，首先显示具有最近输入日期的产品。 |
   | `Oldest products first` | 按产品添加到目录的日期对产品进行排序，首先显示具有最早录入日期的产品。 |
   | `Name: A - Z` | 按字母顺序对产品排序。 |
   | `Name: Z - A` | 按反字母顺序对产品排序。 |
   | `SKU: ascending` | 按SKU的字母数字顺序对产品排序。 |
   | `SKU: descending` | 按SKU以反向字母数字顺序对产品排序。 |
   | `Stock: low stock first` | 将产品从最低库存排序到最高库存。 |
   | `Stock: high stock first` | 对产品从最高库存到最低库存进行排序。 |
   | `Price: high to low` | 将产品从最高价排序到最低价。 |
   | `Price: low to high` | 按从最低到最高的价格对产品进行排序。 |

   {style="table-layout:auto"}

   ![产品排序选项](./assets/pb-products-sortby.png){width="300"}

1. 输入 **[!UICONTROL Number of Products to Display]** 在轮播或网格中。

   值可以来自 `1` 到 `999`. 默认为 `5` 对于网格和 `20` 进行轮播。

   >[!NOTE]
   >
   >类别、SKU或条件设置中的某些产品可能不会显示在产品网格或轮播中。 例如，不会显示已禁用的产品、标记为不可见的产品、缺货的产品以及分配给其他网站的产品。

   >[!IMPORTANT]
   >
   >管理员中未定义可配置、分组和捆绑（动态价格）产品的价格。 因此，这些产品不会显示在 **[!UICONTROL Preview]** 产品是否按价格过滤。 无法在中正确订购这些产品 **[!UICONTROL Preview]** 如果按价格订购。

### 轮播设置

1. 要确定产品在轮盘中的显示方式，请选择 **[!UICONTROL Carousel Mode]**：

   | 选项 | 描述 |
   | ------ | ----------- |
   | `Default` | 默认情况下，轮盘每张幻灯片显示五个产品，并且会根据需要相应地减少该数量。 |
   | `Continuous` | 默认情况下，轮盘每张幻灯片显示五个产品（右侧和左侧显示一半产品），但会以无限循环的方式一次居中和滚动一个产品。 居中产品的右侧和左侧的产品将变暗，以便突出显示居中产品。 |

   {style="table-layout:auto"}

   如果在这两种模式之间切换，则会保留其他轮播设置，但 **[!UICONTROL Infinite Loop]** 设置，始终设置为 `Yes` 在连续模式下，该字段被禁用。

   ![轮播设置](./assets/pb-products-carousel-settings.png){width="600" zoomable="yes"}

1. 如果需要，请设置 **[!UICONTROL Autoplay]** 选项至 `Yes`.

   启用自动播放后，轮盘会在页面加载时自动开始滚动。 如果您保留默认设置(`No`)，则客户必须单击幻灯片导航（点或箭头）以按顺序显示每张幻灯片。

   如果启用此功能，请输入 **[!UICONTROL Autoplay Speed]** 指定每张幻灯片之间的延迟时间（以毫秒为单位）。 默认值为 `4000` （4秒）。

1. 如果需要，请设置 **[!UICONTROL Infinite Loop]** 选项至 `Yes`.

   启用无限循环后，在页面打开时，幻灯片放映将无限期地重播。 如果您保留默认设置(`No`)，则幻灯片放映仅播放一次。

   >[!NOTE]
   >
   >如果您设置 **[!UICONTROL Infinite Loop]** 到 `No` 和 **[!UICONTROL Autoplay]** 设置为 `Yes`，则自动播放会在要显示的产品数结束时停止。

1. 如果需要，请设置 **[!UICONTROL Show Arrows]** 选项至 `Yes`.

   启用此选项后，每张幻灯片都包含 _下一个_ 和 _上一个_ 左右两侧的导航箭头。 如果您保留默认设置(`No`)，则幻灯片不会显示导航箭头。

1. 如果需要，请设置 **[!UICONTROL Show Dots]** 选项至 `No`.

   当设置为默认设置时(`Yes`)，导航点显示在轮盘滑块底部。 如果禁用此设置，则轮播滑块不会显示导航点。

### 高级

1. 要控制“产品”列表在父容器中的位置，请选择 **[!UICONTROL Alignment]**：

   | 选项 | 描述 |
   | ------ | ----------- |
   | `Default` | 应用在当前主题的样式表中指定的对齐默认设置。 |
   | `Left` | 将列表沿父容器的左边框对齐，并允许使用指定的任何边距。 |
   | `Center` | 将列表与父容器的中心对齐，并允许使用指定的任何边距。 |
   | `Right` | 将列表沿父容器的右边框对齐，并允许使用指定的任何边距。 |

   {style="table-layout:auto"}

1. 设置 **[!UICONTROL Border]** 应用于产品容器所有四个边的样式：

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

1. 如果设置的边框样式不是 `None`，完成边框显示选项：

   | 选项 | 描述 |
   | ------ |------------ |
   | [!UICONTROL Border Color] | 通过选择色板、单击拾色器或输入有效的颜色名称或等效的十六进制值来指定颜色。 |
   | [!UICONTROL Border Width] | 输入边框线条宽度的像素数。 |
   | [!UICONTROL Border Radius] | 输入像素数，以定义用于使边框每个角倒圆角的半径大小。 |

   {style="table-layout:auto"}

1. （可选）指定以下项目的名称： **[!UICONTROL CSS classes]** 要应用于容器的当前样式表中。

   用空格分隔多个类名。

1. 以像素为单位输入 **[!UICONTROL Margins and Padding]** 确定“产品”容器的外边距和内边距。

   在图表中输入相应的值。

   | 容器区域 | 描述 |
   | -------------- | ----------- |
   | [!UICONTROL Margins] | 应用于容器所有边的外边缘的空白空间量。 选项： `Top` / `Right` / `Bottom` / `Left` |
   | [!UICONTROL Padding] | 应用于容器所有边的内边缘的空白空间量。 选项： `Top` / `Right` / `Bottom` / `Left` |


## 在舞台上保存并预览

在右上角，单击 **[!UICONTROL Save]** 以应用设置并返回到 [!DNL Page Builder] 工作区。

如果您配置了产品轮播，则它应该类似于以下示例：

![舞台上的产品轮播](./assets/pb-products-admin-carousel.png){width="600"}

您现在可以使用 [构件](../content-design/widgets.md) 将此块放在您希望它出现在商店中的任何位置。 或者，您可以使用 [添加内容 — 阻止](block.md) 将块添加到现有页面、选项卡或块。

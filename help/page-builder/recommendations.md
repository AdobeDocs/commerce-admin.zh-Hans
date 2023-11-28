---
title: 添加内容 — 产品Recommendations
description: 了解产品Recommendations内容类型，用于向添加一系列推荐 [!DNL Page Builder] 暂存。
exl-id: ca90c10d-8d7a-42a2-bb13-2602aa9d6eef
feature: Page Builder, Page Content, Recommendations
source-git-commit: 13d00168e1253a7d2698b898caa30d9ca2ad3800
workflow-type: tm+mt
source-wordcount: '950'
ht-degree: 0%

---

# 添加内容 — 产品Recommendations

使用 _产品Recommendations_ 内容类型，用于添加现有的、活动的 [推荐单位](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/admin/create.html) 到 [[!DNL Page Builder] 阶段](workspace.md#stage) CMS页面、块或动态块。

>[!NOTE]
>
>此 [!DNL Page Builder] _产品Recommendations_ Adobe Commerce 2.4.4及更高版本支持内容类型，该内容类型可在 [产品Recommendations中继包版本3.0.x或更高版本](https://marketplace.magento.com/magento-product-recommendations.html). 添加 [!DNL Page Builder] 支持产品Recommendations， [请参阅安装信息](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/getting-started/install-configure.html#pbsupport). **此内容类型不适用于Magento Open Source。**

{{$include /help/_includes/page-builder-save-timeout.md}}

## 产品Recommendations工具箱

| 工具 | 图标 | 描述 |
| --- | --| --- |
| 移动 | ![“移动”图标](./assets/pb-icon-move.png){width="25"} | 将产品推荐容器及其内容移动到舞台上的另一个位置。 |
| 设置 | ![“设置”图标](./assets/pb-icon-settings.png){width="25"} | 打开“编辑产品推荐”页面，您可以在其中选择推荐单元并更改容器的属性。 |
| 隐藏 | ![“隐藏”图标](./assets/pb-icon-hide.png){width="25"} | 隐藏当前产品推荐容器及其内容。 |
| 显示 | ![显示图标](./assets/pb-icon-show.png){width="25"} | 显示隐藏的产品推荐容器及其内容。 |
| 复制 | ![“复制”图标](./assets/pb-icon-duplicate.png){width="25"} | 复制产品推荐容器及其内容。 |
| 移除 | ![“删除”图标](./assets/pb-icon-remove.png){width="25"} | 从阶段中删除产品推荐容器及其内容。 |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## 添加现有的推荐单位

1. 确保您已拥有 [已创建推荐单位](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/admin/create.html) 对于 [!DNL Page Builder] 页面类型。

>[!NOTE]
>
>您可以为创建推荐单位 [!DNL Page Builder] 仅在默认商店视图中键入页面。

1. 在编辑模式下打开页面、块或动态块。

1. 展开 _[!UICONTROL Content]_部分并单击&#x200B;**[!UICONTROL Edit with Page Builder]**或在内容预览区域内打开 [!DNL Page Builder] 工作区。

1. 在 [!DNL Page Builder] 下的面板 _[!UICONTROL Layout]_，拖动&#x200B;**[!UICONTROL Row]**舞台占位符。

1. 在 [!DNL Page Builder] 下的面板 _[!UICONTROL Add Content]_，拖动&#x200B;**[!UICONTROL Product Recommendation]**行的占位符。

   ![添加产品推荐内容类型](./assets/pb-add-prex-drag.png){width="600" zoomable="yes"}

1. 执行以下操作之一：

   - 单击 **[!UICONTROL Edit Product Recommendation]**.
   - 将鼠标悬停在空容器上以显示工具箱，然后单击 _设置_ (![“设置”图标](./assets/pb-icon-settings.png){width="20"} )图标。

   ![编辑产品推荐](./assets/pb-prex-toolbox.png){width="600" zoomable="yes"}

1. 在 _[!UICONTROL Selection]_部分，单击&#x200B;**[!UICONTROL Select]**.

1. 在活动产品推荐列表中，找到包含要添加的推荐单元的行，然后单击 **[!UICONTROL Select]** 在最后一列。

   ![选定的产品推荐](./assets/pb-prex-select.png){width="600" zoomable="yes"}

1. 在右上角，单击 **[!UICONTROL Add Selected]**.

   所选产品推荐的名称将显示在 _[!UICONTROL Selection]_的部分_[!UICONTROL Edit Product Recommendation]_ 页面。

1. 对进行必要的更改 [高级设置](#advanced-settings).

   ![编辑产品推荐](./assets/pb-prex-edit.png){width="600" zoomable="yes"}

1. 完成后，执行以下操作：

   - 如果使用完全最大化的浏览器窗口，请单击 _关闭全屏_ (![“关闭全屏”图标](./assets/pb-icon-reduce.png))图标。

   - 单击 **[!UICONTROL Save]** 以应用设置并返回到 [!DNL Page Builder] 工作区。

   当您返回到舞台时，产品占位符图像会显示在容器中。

## 编辑推荐单元设置

1. 将鼠标悬停在推荐单位容器上以显示工具箱，然后单击 _设置_ (![“设置”图标](./assets/pb-icon-settings.png){width="20"} )图标。

   ![推荐工具箱](./assets/pb-placeholder-toolbox.png){width="600" zoomable="yes"}

1. 对进行必要的更改 [高级设置](#advanced-settings).

1. 完成后，单击 **[!UICONTROL Save]** 以应用设置并返回到 [!DNL Page Builder] 工作区。

## 复制推荐单位

1. 将鼠标悬停在推荐单位容器上以显示工具箱，然后单击 _复制_ ( ![复制ison](./assets/pb-icon-duplicate.png){width="20"} )图标。

   副本会出现在原始文件的正下方。

1. 要将重复的建议单位移动到新位置，请将鼠标悬停在容器上并单击 _移动_ ( ![“移动”图标](./assets/pb-icon-move.png){width="20"} )图标。

1. 选择并拖动推荐单位，直到红色准则出现在新位置。

   移动推荐单元时，每个容器的顶边框和底边框均显示为虚线。

## 从阶段中删除推荐单位

1. 将鼠标悬停在推荐单位容器上，然后单击 _移除_ ( ![“删除”图标](./assets/pb-icon-remove.png){width="20"} )图标。

1. 提示确认时，单击 **[!UICONTROL OK]**.

## 高级设置

1. 要控制Product Recommendations单元在父容器中的位置，请选择 **[!UICONTROL Alignment]**：

   | 选项 | 描述 |
   | ------ | ----------- |
   | `Default` | 应用在当前主题的样式表中指定的对齐默认设置。 |
   | `Left` | 将单位沿父容器的左边框对齐，并允许使用指定的任何边距。 |
   | `Center` | 将单位对齐父容器的中心，并允许指定的任何边距。 |
   | `Right` | 将单位沿父容器的右边框对齐，并允许使用指定的任何边距。 |

   {style="table-layout:auto"}

1. 设置 **[!UICONTROL Border]** 应用于Product Recommendations单元所有四个方面的样式：

   | 选项 | 描述 |
   | ------ | ----------- |
   | `Default` | 应用关联样式表指定的默认边框样式。 |
   | `None` | 不提供任何单位边框的可见指示。 |
   | `Dotted` | 单位边框显示为虚线。 |
   | `Dashed` | 单位边框显示为虚线。 |
   | `Solid` | 单位边框显示为实线。 |
   | `Double` | 单位边框显示为双线。 |
   | `Groove` | 单位边框显示为槽线。 |
   | `Ridge` | 单位边框显示为脊线。 |
   | `Inset` | 单位边框显示为内嵌线。 |
   | `Outset` | 单位边框显示为外线。 |

   {style="table-layout:auto"}

1. 如果设置的边框样式不是 `None`，完成边框显示选项：

   | 选项 | 描述 |
   | ------ |------------ |
   | [!UICONTROL Border Color] | 通过选择色板、单击拾色器或输入有效的颜色名称或等效的十六进制值来指定颜色。 |
   | [!UICONTROL Border Width] | 输入边框线条宽度的像素数。 |
   | [!UICONTROL Border Radius] | 输入像素数，以定义用于使边框每个角倒圆角的半径大小。 |

   {style="table-layout:auto"}

1. （可选）指定以下项目的名称： **[!UICONTROL CSS classes]** 从当前样式表应用到单位。

   用空格分隔多个类名。

1. 以像素为单位输入 **[!UICONTROL Margins and Padding]** 确定单位的外边距和内边距。

   在图表中输入相应的值。

   | 容器区域 | 描述 |
   | ------ | ----------- |
   | [!UICONTROL Margins] | 应用到设备所有侧的外边缘的空白空间量。 选项： `Top` / `Right` / `Bottom` / `Left` |
   | [!UICONTROL Padding] | 应用于设备所有侧的内边缘的空白空间量。 选项： `Top` / `Right` / `Bottom` / `Left` |

   {style="table-layout:auto"}

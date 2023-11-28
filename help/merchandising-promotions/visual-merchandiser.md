---
title: Visual Merchandiser概述
description: 了解可视化促销工具，这些工具允许您定位产品并确定哪些产品显示在类别列表中。
exl-id: 00fe8b7f-0c33-4f06-a3cd-1f0bd18079f1
feature: Categories, Merchandising, Products
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 0%

---

# Visual Merchandiser

{{ee-feature}}

此 _Visual Merchandiser_ 是一组高级工具，可用于定位产品并应用条件来确定哪些产品会显示在类别列表中。 结果可能是根据目录中的变化动态选择产品。 您可以在中工作 _视觉模式_，以在网格上将每个产品显示为拼贴，或者从类别中的产品列表中工作。 每种模式中都提供了相同的工具，您可以使用右上角的按钮在各种显示类型之间切换。

![图块视图中的类别产品](./assets/category-products-visual-with-stock.png){width="600" zoomable="yes"}

## 访问可视化促销活动

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. 深入查看类别树，然后单击要编辑的类别。

1. 向下滚动并展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Products in Category]** 部分。

1. 单击 _以图块查看_ ( ![以图块查看](../assets/icon-view-tiles.png) )按钮以将产品显示为网格。

1. 完成后，单击 **[!UICONTROL Save Category]**.

## 更改产品的位置

1. 使用 [排序顺序](../catalog/navigation-product-listings.md) 查看要移动的产品。

   - **方法1：拖放**

     抓住 _拖动_ (![拖动图标](../assets/icon-move.png))控制product拼贴的右上角，并将产品放置到适当位置。 每个产品的数量会进行相应的调整以反映新位置。

   - **方法2：设置位置值**

     在 _位置_ 控制器(![职位字段](../assets/control-position.png))，输入您希望产品出现的编号。 输入 `0` 将产品放在列表顶部。

1. 完成后，单击 **[!UICONTROL Save Category]**.

>[!NOTE]
>
>在干净安装中，Adobe Commerce会保留类别ID `2` 默认存储的根目录。 可视化促销器只能使用ID号为 `3` 或更高。

## 工作区控件

| 控件 | 描述 |
|--- |--- |
| ![“查看列表”图标](../assets/icon-view-list.png) | 列表查看 |
| ![“以图块形式查看”图标](../assets/icon-view-tiles.png) | 以图块查看 |
| ![按规则匹配切换 — 否](../assets/toggle-no.png) | 按规则匹配 — 否 |
| ![按规则匹配切换 — 是](../assets/toggle-yes.png) | 按规则匹配 — 是 |
| ![“移动”图标](../assets/icon-move.png) | 拖动 |
| ![位置控制器](../assets/control-position.png) | 位置 |
| ![“从类别中移除”图标](../assets/icon-delete-x.png) | 从类别中移除 |
| ![每页控件项目数](../assets/control-items-per-page.png) | 每页查看次数 |
| ![更改页面显示](../assets/control-page-display.png) | 转到下一个/上一个 |

{style="table-layout:auto"}

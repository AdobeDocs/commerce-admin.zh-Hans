---
title: Visual Merchandiser概述
description: 了解可视化促销工具，这些工具允许您定位产品并确定哪些产品显示在类别列表中。
exl-id: 00fe8b7f-0c33-4f06-a3cd-1f0bd18079f1
feature: Categories, Merchandising, Products
badgePaas: label="仅限PaaS" type="Informative" url="https://experienceleague.adobe.com/zh-hans/docs/commerce/user-guides/product-solutions" tooltip="仅适用于云项目(Adobe管理的PaaS基础架构)和内部部署项目上的Adobe Commerce 。"
source-git-commit: 6d782e3aafa7460a0e0d5ca07a2bde2ae371a9ea
workflow-type: tm+mt
source-wordcount: '382'
ht-degree: 0%

---

# Visual Merchandiser

{{ee-feature}}

_可视化促销器_&#x200B;是一组高级工具，可用于定位产品和应用条件，以确定哪些产品出现在类别列表中。 结果可能是根据目录中的变化动态选择产品。 您可以在&#x200B;_可视模式_&#x200B;下工作，该模式在网格上将每个产品显示为拼贴，也可以从类别中的产品列表中工作。 每种模式中都提供了相同的工具，您可以使用右上角的按钮在各种显示类型之间切换。

图块视图中的![类别产品](./assets/category-products-visual-with-stock.png){width="600" zoomable="yes"}

## 访问可视化促销活动

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Catalog]** > **[!UICONTROL Categories]**。

1. 深入查看类别树，然后单击要编辑的类别。

1. 向下滚动并展开&#x200B;**[!UICONTROL Products in Category]**&#x200B;部分的![扩展选择器](../assets/icon-display-expand.png)。

1. 单击“_以图块方式查看_”（![以图块方式查看](../assets/icon-view-tiles.png)）按钮，以网格形式显示产品。

1. 完成后，单击&#x200B;**[!UICONTROL Save Category]**。

## 更改产品的位置

1. 使用[排序顺序](../catalog/navigation-product-listings.md)查看要移动的产品。

   - **方法1：拖放**

     抓住产品拼贴右上角的&#x200B;_拖动_ （![拖动图标](../assets/icon-move.png)）控件，然后将产品放置到适当位置。 每个产品的数量会进行相应的调整以反映新位置。

   - **方法2：设置位置值**

     在产品图块上的&#x200B;_位置_&#x200B;控制器（![位置字段](../assets/control-position.png)）中，输入您希望产品出现的编号。 输入`0`将产品放在列表顶部。

1. 完成后，单击&#x200B;**[!UICONTROL Save Category]**。

>[!NOTE]
>
>在全新安装中，Adobe Commerce为默认存储区的根目录保留类别ID `2`。 可视化促销器只能使用ID号为`3`或更大的类别。

## Workspace控件

| 控件 | 描述 |
|--- |--- |
| ![查看列表图标](../assets/icon-view-list.png) | 列表查看 |
| ![以拼贴图标查看](../assets/icon-view-tiles.png) | 以图块查看 |
| ![按规则匹配切换 — 否](../assets/toggle-no.png) | 按规则匹配 — 否 |
| ![按规则匹配切换 — 是](../assets/toggle-yes.png) | 按规则匹配 — 是 |
| ![移动图标](../assets/icon-move.png) | 拖动 |
| ![位置控制器](../assets/control-position.png) | 位置 |
| ![从类别中移除图标](../assets/icon-delete-x.png) | 从类别中移除 |
| 每个页面控件有![个项目](../assets/control-items-per-page.png) | 每页查看次数 |
| ![更改页面显示](../assets/control-page-display.png) | 转到下一个/上一个 |

{style="table-layout:auto"}

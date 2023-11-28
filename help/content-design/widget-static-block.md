---
title: 使用小组件定位块
description: 了解如何使用静态块构件将现有内容几乎放置在存储中的任意位置。
exl-id: 174deef2-33c4-4f1a-8ca8-4969be209bc7
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '566'
ht-degree: 0%

---

# 使用小组件定位块

此 _CMS静态块_ [构件](widgets.md) 允许您放置现有的 [内容块](blocks.md) 你店里几乎任何一处。

![小组件](./assets/widgets.png){width="700" zoomable="yes"}

## 第1步：选择构件类型

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. 在右上角，单击 **[!UICONTROL Add Widget]**.

1. 在 _设置_ 部分，设置 **[!UICONTROL Type]** 到 `CMS Static Block` 并单击 **[!UICONTROL Continue]**.

1. 验证 **[!UICONTROL Design Theme]** 设置为当前主题，然后单击 **[!UICONTROL Continue]**.

   ![构件设置](./assets/widget-settings.png){width="600" zoomable="yes"}

1. 在 _[!UICONTROL Storefront Properties]_部分，执行以下操作：

   - 对象 **[!UICONTROL Widget Title]**，为构件输入描述性标题。

     此标题仅在 _管理员_.

   - 对象 **[!UICONTROL Assign to Store Views]**，选择显示小部件的商店视图。

     您可以选择特定的商店视图，或者 `All Store Views`. 要选择多个视图，请按住Ctrl键(PC)或Command键(Mac)并单击每个选项。

   - （可选）对于 **[!UICONTROL Sort Order]**，请输入一个数字以确定此项目在页面同一部分中与其他项目一起显示的顺序。 (`0` =第一个， `1` =秒， `3` =第三，依此类推。)

     ![店面属性](./assets/widget-storefront-properties.png){width="600" zoomable="yes"}

## 第2步：完成构件布局更新

1. 在 _[!UICONTROL Layout Updates]_部分，单击&#x200B;**[!UICONTROL Add Layout Update]**.

1. 设置 **[!UICONTROL Display On]** 到您希望块显示的类别、产品或页面。

1. 要将块放置在特定页面上，请执行以下操作：

   - 选择 **[!UICONTROL Page]** 您希望块出现的位置。

   - 选择 **[!UICONTROL Block Reference]** 标识块在页面上显示的位置。

   - 接受默认设置 **[!UICONTROL Template]**，设置为 `CMS Static Block Default Template`.

     ![布局更新](./assets/widget-layout-update-home-page.png){width="600" zoomable="yes"}

### 布局更新选项

| 字段 | 描述 |
|--- |--- |
| **_[!UICONTROL Categories]_** |  |
| [!UICONTROL Anchor Categories] | 在锚点类别页面上显示构件。<br/>**[!UICONTROL Categories]**— 显示锚点的类别。 选项： `All` /`Specific Categories`<br/>**[!UICONTROL Container]**  — 将容器设置为要显示小组件的页面布局部分。<br/>**[!UICONTROL Template]**— 确定布局的主题。 |
| [!UICONTROL Non-Anchor Categories] | 在非锚点类别页面上显示构件。<br/>**[!UICONTROL Categories]**— 显示锚点的类别。 选项： `All` /`Specific Categories`<br/>**[!UICONTROL Container]**  — 将容器设置为要显示小组件的页面布局部分。<br/>**[!UICONTROL Template]**— 确定布局的主题。 |
| **_[!UICONTROL Products]_** |  |
| 所有产品类型 | 在特定类型的产品页面上或所有产品页面上显示构件。 <br/>**[!UICONTROL Products]**— 显示小组件的产品。 选项： `All` /` Specific Products`<br/>**[!UICONTROL Container]**  — 将容器设置为要显示小组件的页面布局部分。<br/>**[!UICONTROL Template]**— 确定布局的主题。 |
| **_[!UICONTROL Generic Pages]_** |  |
| [!UICONTROL All Pages] | 在所有页面上显示构件。 <br/>**[!UICONTROL Container]**— 将容器设置为要显示小组件的页面布局部分。<br/>**[!UICONTROL Template]**  — 确定布局的主题。 |
| [!UICONTROL Specified Page] | 显示特定页面上的构件。 选项：<br/>**[!UICONTROL Page]**— 显示小组件的页面。<br/>**[!UICONTROL Container]**  — 将容器设置为要显示小组件的页面布局部分。<br/>**模板**  — 确定布局的主题。 |
| [!UICONTROL Page Layouts] | 在具有特定布局的页面上显示构件。 <br/>**[!UICONTROL Page]**— 显示小组件的页面。<br/>**[!UICONTROL Container]**  — 将容器设置为要显示小组件的页面布局部分。<br/>**[!UICONTROL Template]**— 确定布局的主题。 |

{style="table-layout:auto"}

## 步骤3：放置块

1. 在左侧面板中，选择 **[!UICONTROL Widget Options]**.

1. 单击 **[!UICONTROL Select Block…]** 并从列表中选择要放置的块。

1. 完成后，单击 **[!UICONTROL Save]**.

   该应用程序现在显示在列表中。

1. 出现提示时，按照页面顶部的说明更新索引和页面缓存。

1. 返回店面，验证块是否出现在正确的位置。

   要移动块，可以重新打开构件或尝试使用其他页面或块引用。

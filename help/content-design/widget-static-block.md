---
title: 使用小组件定位块
description: 了解如何使用静态块构件将现有内容几乎放置在存储中的任意位置。
exl-id: 174deef2-33c4-4f1a-8ca8-4969be209bc7
badgePaas: label="仅限PaaS" type="Informative" url="https://experienceleague.adobe.com/zh-hans/docs/commerce/user-guides/product-solutions" tooltip="仅适用于云项目(Adobe管理的PaaS基础架构)和内部部署项目上的Adobe Commerce 。"
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '586'
ht-degree: 0%

---

# 使用小组件定位块

_CMS静态块_ [小组件](widgets.md)使您能够将现有[内容块](blocks.md)放置到商店中的几乎任何位置。

![小组件](./assets/widgets.png){width="700" zoomable="yes"}

## 第1步：选择构件类型

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**。

1. 单击右上角的&#x200B;**[!UICONTROL Add Widget]**。

1. 在&#x200B;_设置_&#x200B;部分中，将&#x200B;**[!UICONTROL Type]**&#x200B;设置为`CMS Static Block`并单击&#x200B;**[!UICONTROL Continue]**。

1. 验证&#x200B;**[!UICONTROL Design Theme]**&#x200B;是否设置为当前主题，然后单击&#x200B;**[!UICONTROL Continue]**。

   ![小组件设置](./assets/widget-settings.png){width="600" zoomable="yes"}

1. 在&#x200B;_[!UICONTROL Storefront Properties]_&#x200B;部分中，执行以下操作：

   - 对于&#x200B;**[!UICONTROL Widget Title]**，输入小部件的描述性标题。

     此标题仅在&#x200B;_管理员_&#x200B;中可见。

   - 对于&#x200B;**[!UICONTROL Assign to Store Views]**，选择显示小组件的存储视图。

     您可以选择特定的商店视图，或`All Store Views`。 要选择多个视图，请按住Ctrl键(PC)或Command键(Mac)并单击每个选项。

   - （可选）为&#x200B;**[!UICONTROL Sort Order]**&#x200B;输入一个数字，以确定该项在页面的同一部分中与其他项一起出现的顺序。 （`0` =第一，`1` =第二，`3` =第三，依此类推。）

     ![店面属性](./assets/widget-storefront-properties.png){width="600" zoomable="yes"}

## 第2步：完成构件布局更新

1. 在&#x200B;_[!UICONTROL Layout Updates]_&#x200B;部分中，单击&#x200B;**[!UICONTROL Add Layout Update]**。

1. 将&#x200B;**[!UICONTROL Display On]**&#x200B;设置为您希望块显示的类别、产品或页面。

1. 要将块放置在特定页面上，请执行以下操作：

   - 选择要显示块的&#x200B;**[!UICONTROL Page]**。

   - 选择标识块在页面上显示位置的&#x200B;**[!UICONTROL Block Reference]**。

   - 接受设置为`CMS Static Block Default Template`的&#x200B;**[!UICONTROL Template]**&#x200B;的默认设置。

     ![布局更新](./assets/widget-layout-update-home-page.png){width="600" zoomable="yes"}

### 布局更新选项

| 字段 | 描述 |
|--- |--- |
| **_[!UICONTROL Categories]_** |  |
| [!UICONTROL Anchor Categories] | 在锚点类别页面上显示构件。<br/>**[!UICONTROL Categories]**— 显示锚点的类别。 选项： `All` /`Specific Categories`<br/>**[!UICONTROL Container]** — 将容器设置为要显示小组件的页面布局部分。<br/>**[!UICONTROL Template]**— 确定布局的主题。 |
| [!UICONTROL Non-Anchor Categories] | 在非锚点类别页面上显示构件。<br/>**[!UICONTROL Categories]**— 显示锚点的类别。 选项： `All` /`Specific Categories`<br/>**[!UICONTROL Container]** — 将容器设置为要显示小组件的页面布局部分。<br/>**[!UICONTROL Template]**— 确定布局的主题。 |
| **_[!UICONTROL Products]_** |  |
| 所有产品类型 | 在特定类型的产品页面上或所有产品页面上显示构件。 <br/>**[!UICONTROL Products]**— 显示小组件的产品。 选项： `All` /` Specific Products`<br/>**[!UICONTROL Container]** — 将容器设置为要显示小组件的页面布局部分。<br/>**[!UICONTROL Template]**— 确定布局的主题。 |
| **_[!UICONTROL Generic Pages]_** |  |
| [!UICONTROL All Pages] | 在所有页面上显示构件。 <br/>**[!UICONTROL Container]**— 将容器设置为要显示小组件的页面布局部分。<br/>**[!UICONTROL Template]** — 确定布局的主题。 |
| [!UICONTROL Specified Page] | 显示特定页面上的构件。 选项：<br/>**[!UICONTROL Page]**— 显示小组件的页面。<br/>**[!UICONTROL Container]** — 将容器设置为要显示小组件的页面布局部分。<br/>**模板** — 确定布局的主题。 |
| [!UICONTROL Page Layouts] | 在具有特定布局的页面上显示构件。 <br/>**[!UICONTROL Page]**— 显示小组件的页面。<br/>**[!UICONTROL Container]** — 将容器设置为要显示小组件的页面布局部分。<br/>**[!UICONTROL Template]**— 确定布局的主题。 |

{style="table-layout:auto"}

## 步骤3：放置块

1. 在左侧面板中，选择&#x200B;**[!UICONTROL Widget Options]**。

1. 单击&#x200B;**[!UICONTROL Select Block…]**&#x200B;并从列表中选择要放置的块。

1. 完成后，单击&#x200B;**[!UICONTROL Save]**。

   该应用程序现在显示在列表中。

1. 出现提示时，按照页面顶部的说明更新索引和页面缓存。

1. 返回店面，验证块是否出现在正确的位置。

   要移动块，可以重新打开构件或尝试使用其他页面或块引用。

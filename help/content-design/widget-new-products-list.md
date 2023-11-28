---
title: 新产品列表构件
description: 了解如何使用新产品列表构件显示最近添加的产品列表。
exl-id: bdff3655-cd14-4a19-a51f-4cabeb274d2a
feature: Page Content, Products
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '602'
ht-degree: 0%

---

# 新产品列表构件

新产品列表是动态内容的一个示例，由从产品目录中提取的实时数据组成。 默认情况下， _新产品_ 列表包括最近添加的前8个产品。 但是，也可以将其配置为仅包含指定日期范围内的产品。

![店面主页上的新产品列表](./assets/storefront-home-page-new-products.png){width="700" zoomable="yes"}

## 步骤1：将每个产品设置为新产品

![Magento Open Source](../assets/open-source.svg) 此步骤仅适用于Magento Open Source。

![Adobe Commerce](../assets/adobe-logo.svg) 有关Adobe Commerce商店的信息，请参阅 [计划更新](content-staging-scheduled-update.md) 然后继续本页中的步骤2。

_[!UICONTROL Set Product as New]_日期范围设置只能在计划的更新中配置。

将产品设置为新将产品添加到 _新产品_ 列表。 当您不再希望将设置包含在列表中时，可以随时将其更改回。

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. 查找要功能的每个产品，并在编辑模式下打开。

1. 对象 **[!UICONTROL Set Product as New]**，切换是否将产品设置为新产品的选项。

   ![将产品设置为新产品](./assets/product-set-as-new.png){width="400" zoomable="yes"}

1. 完成后，单击 **[!UICONTROL Save]**.

1. 当系统提示您重新索引并刷新页面缓存时，请单击页面顶部的链接并按照说明操作。

## 第2步：创建构件

确定新产品列表内容及其在您商店中的版面的代码由小组件工具生成。

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. 在右上角，单击 **[!UICONTROL Add Widget]**.

1. 在 _[!UICONTROL Settings]_部分，执行以下操作：

   - 设置 **[!UICONTROL Type]** 到 `Catalog New Products List`.

   - 选择 **[!UICONTROL Design Theme]** 店里用的那个。

1. 单击 **[!UICONTROL Continue]**.

   ![新的产品列表构件设置](./assets/widget-settings.png){width="600" zoomable="yes"}

1. 在 _[!UICONTROL Storefront Properties]_部分，执行以下操作：

   - 对象 **[!UICONTROL Widget Title]**，为构件输入描述性标题。 (此标题仅在 _管理员_.)

   - 对象 **[!UICONTROL Assign to Store Views]**，选择显示小部件的商店视图。

     您可以选择特定的商店视图，或者 `All Store Views`. 要选择多个视图，请按住Ctrl键(PC)或Command键(Mac)并单击每个选项。

   - （可选）对于 **[!UICONTROL Sort Order]**，请输入一个数字以确定此项目在页面同一部分中与其他项目一起显示的顺序。 (`0` =第一个， `1` =秒， `3` =第三，依此类推。)

   ![布局更新](./assets/widget-layout-update-home-page.png){width="600" zoomable="yes"}

## 步骤3：选择位置

1. 在 _[!UICONTROL Layout Updates]_部分，单击&#x200B;**[!UICONTROL Add Layout Update]**.

1. 设置 **[!UICONTROL Display On]** 到 `Specified Page.`

1. 设置 **[!UICONTROL Page]** 到 `CMS Home Page`.

1. 设置 **[!UICONTROL Block Reference]** 到 `Main Content Area`.

1. 设置 **[!UICONTROL Template]** 更改为以下任一项：

   - `New Product List Template`
   - `New Products Grid Template`

     ![布局更新](./assets/widget-layout-update-new-products-list.png){width="600" zoomable="yes"}

1. 单击 **[!UICONTROL Save and Continue Edit]**.

   现在，您可以忽略消息以刷新缓存。

## 步骤4：配置列表

1. 在左侧面板中，选择 **[!UICONTROL Widget Options]**.

1. 设置 **[!UICONTROL Display Products]** 更改为以下任一项：

   - `All Products`  — 按顺序列出产品，从最近添加的产品开始。
   - `New Products`  — 仅列出标识为 _新建_. 在中指定的日期范围内，产品会被视为新产品。 _[!UICONTROL Set Product As New From/To]_. 如果日期范围到期，但未定义任何新产品，则列表为空。

1. 要为具有多个页面的列表提供导航控制，请设置 **[!UICONTROL Display Page Control]** 到 `Yes`.

   对象 **[!UICONTROL Number of Products per Page]**，输入要显示在每个页面上的产品数量。

1. 设置 **[!UICONTROL Number of Products to Display]** 选项来确定要包含在列表中的新产品数量。

   默认设置为 `10`.

1. 对象 **[!UICONTROL Cache Lifetime (Seconds)]**，选择刷新新产品列表的频率。

   默认情况下，缓存设置为86,400秒（24小时）。

   ![构件选项](./assets/widget-options-new-product-list.png){width="600" zoomable="yes"}

1. 完成后，单击 **[!UICONTROL Save]**.

1. 提示刷新缓存时，单击页面顶部消息中的链接，然后按照说明操作。

## 步骤5：预览您的工作

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. 在网格中找到页面，其中 _新产品_ 列表并点击 **[!UICONTROL Preview]** 中的链接 _[!UICONTROL Action]_列。

---
title: 商店本地化
description: 了解如何将商店或商店视图本地化。
exl-id: 64e1b431-f599-444c-9d39-207bb95f0400
topic: Commerce, Localization
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '735'
ht-degree: 0%

---

# 商店本地化

通过更改视图的区域设置，可以立即将整个存储中页面上看起来为硬编码的大多数文本更改为其他语言。 更改区域设置实际上不会逐字翻译文本，而只是引用不同的翻译表，该表提供在整个存储区中使用的界面文本。 可以更改的文本包括导航标题、标签、按钮和链接，例如 _我的购物车_ 和 _我的帐户_. 您也可以使用 [内联翻译](../configuration-reference/advanced/developer.md) 工具，用于在界面中修饰文本。

语言包位于 [翻译和本地化][1]Commerce Marketplace时{：target=&quot;_blank&quot;}。 Marketplace会不断添加新扩展，因此请经常回来查看。

## 步骤1：安装语言包

按照标准说明安装语言包扩展。 有关安装扩展的详细信息，请参阅 [常规CLI安装][2] 在 _扩展指南_.

## 步骤2：创建该语言的存储视图

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**.

1. 单击 **[!UICONTROL Create Store View]**.

1. 设置新商店视图的选项：

   - **[!UICONTROL Store]**  — 选择作为视图父级的存储。

   - **[!UICONTROL Name]**  — 输入存储视图的名称。 例如：葡萄牙语。

     在存储的标题中，该名称显示在 _语言选择器_.

   - **[!UICONTROL Code]**  — 输入小写字符代码以标识视图。 例如： `portuguese`.

   - **[!UICONTROL Status]**  — 要激活视图，请将设置为 `Enabled`.

   - **[!UICONTROL Sort Order]**  — （可选）输入一个数字，以确定此视图与其他视图一起列出的顺序。

1. 完成后，单击 **[!UICONTROL Save Store View]**.

## 步骤3：更改存储视图的区域设置

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左上角，设置 **[!UICONTROL Store View]** 到要应用配置的特定视图。

1. 提示确认范围切换时，单击 **[!UICONTROL OK]**.

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Locale Options]** 部分。

1. 清除 **[!UICONTROL Use Website]** 复选框和设置 **[!UICONTROL Locale]** 指定给视图的语言。

   如果存在几种可用的语言变体，请确保为特定区域或方言选择一种变体。

1. 完成后，单击 **[!UICONTROL Save Config]**.

   更改区域设置的语言之后，您创建的其余内容，包括产品名称和说明、类别、 [CMS](../content-design/page-translate.md) 页和块必须为每个存储视图单独翻译。

## 将产品本地化

如果您的商店以不同语言提供了多个视图，则每个商店视图中提供了相同的产品。 您可以使用相同的基本产品信息，例如SKU、价格和库存水平，而无论使用何种语言。 然后，根据需要，仅翻译每种语言的产品名称、描述字段和元数据。

### 步骤1：翻译产品字段

1. 在 _管理员_ 侧栏，转到  **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. 在网格中，找到要翻译的产品，并以编辑模式将其打开。

1. 在左上角，设置 **[!UICONTROL Store View]** 到翻译视图，然后单击 **[!UICONTROL OK]** 提示确认时。

1. 对于要编辑的每个字段，执行以下操作：

   - 取消选择 **[!UICONTROL Use Default Value]** 复选框。

   - 在字段中粘贴或键入已翻译文本。

   确保翻译所有文本字段，包括 [图像](../catalog/catalog-images-video.md) 标签和替换文本， [搜索引擎优化](../catalog/product-search-engine-optimization.md) 字段和任意 [自定义选项](../catalog/settings-advanced-custom-options.md) 信息。

1. 完成后，单击 **[!UICONTROL Save]**.

### 步骤2：翻译字段标签

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. 在列表中，找到要翻译的属性，并在编辑模式下打开。

1. 在左侧面板中，选择 **[!UICONTROL Manage Labels]**.

1. 在 _[!UICONTROL Manage Titles]_部分，为每个商店视图输入已翻译的标签。

   ![输入翻译的标签](./assets/product-attribute-labels-translate.png){width="600" zoomable="yes"}

1. 完成后，单击 **[!UICONTROL Save Attribute]**.

### 步骤3：翻译所有类别

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Catalog]** > **类别**.

1. 在左上角，设置 **[!UICONTROL Store View]** 到翻译视图，然后单击 **[!UICONTROL OK]** 提示确认时。

1. 在树中，找到要翻译的类别，然后在编辑模式下打开该类别。

1. 对象 _基本信息_，转换 **[!UICONTROL Category Name]**.

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 _[!UICONTROL Content]_部分并翻译&#x200B;**[!UICONTROL Description]**.

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Search Engine Optimization Settings]** 部分并翻译以下字段：

   - **[!UICONTROL Meta Title]**
   - **[!UICONTROL Meta Keywords]**
   - **[!UICONTROL Meta Description]**

1. 在 _[!UICONTROL Search Engine Optimization Settings]_部分，请执行以下操作以翻译&#x200B;**[!UICONTROL URL Key]**：

   - 清除 **[!UICONTROL Use Default Value]** 复选框。

   - 输入已翻译文本。

   - 确保 **[!UICONTROL Create Permanent Redirect for old URL]** 复选框处于选中状态。

   ![翻译URL键](./assets/category-translate-url-key.png)

1. 完成后，单击 **[!UICONTROL Save Category]**.

1. 对存储中使用的所有类别重复该过程。

### 步骤4：翻译产品属性和属性选项

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. 选择要翻译的属性。

1. 选择 **[!UICONTROL Manage Labels]** 左侧，并设置 **[!UICONTROL Managed Titles]** 用于定义属性标题翻译的选项。

1. 选择 **[!UICONTROL Properties]** 在左侧输入已翻译的属性选项，该选项位于 **[!UICONTROL Manage Options]** 部分。

   ![管理选项](./assets/manage-option-tab.png){width="600" zoomable="yes"}

1. 完成后，单击 **[!UICONTROL Save Attribute]**.


[1]: https://marketplace.magento.com/extensions/content-customizations/translations-localization.html
[2]: https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html

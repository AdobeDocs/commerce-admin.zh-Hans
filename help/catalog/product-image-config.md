---
title: 产品图像配置
description: 了解如何设置最大像素大小（宽度和高度）并在上传期间自动调整产品图像文件的大小。
exl-id: d8fce5f8-eddf-4335-9a72-24036db077db
feature: Catalog Management, Products, Media
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '699'
ht-degree: 0%

---

# 产品图像配置

如果您计划上传大图像以供在 _[!UICONTROL Product Details]_页面时，您可能需要考虑设置最大像素大小（宽度和高度），并在上传时自动调整文件大小。 为了支持此类产品图像上传，有一个选项可在您上传大型图像文件时自动调整其大小。 对于要添加到目录但尚未显示图像资源的产品，可以配置占位符图像。

## 产品图像大小调整

上传产品图像时，您可以添加不同大小的较大图像，以对图像进行详细的高质量放大 _[!UICONTROL Product Details]_页面。 要确保所有图像具有相似的大小和外观，可以使用图像大小调整选项来确保所有图像均匹配特定的像素大小。 此选项使用配置设置自动调整所有产品图像的大小，这有助于提高缩放性能、加快图像加载速度并保持产品图像的统一外观。

>[!NOTE]
>
>为获得最佳兼容性，建议将所有产品图像与 `sRGB` 颜色配置文件。 所有其他颜色配置文件会自动转换为 `sRGB` 产品图像上传期间的颜色配置文件，这可能导致上传的图像颜色不一致。

设置最大像素宽度和高度可将图像大小按像素调整为物理尺寸。 Commerce会根据较高的宽度或高度调整图像大小，同时保持其比例。 降低JPG图像的质量可减小文件大小。

例如，100%的3000 x 2100像素JPG可以是5 mb或更大的图像文件。 调整此图像的大小会将宽度减少到1920像素，并保持比例和质量为80%，以提供小得多的文件大小和较高的质量。

### 启用图像大小调整

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中，展开 **[!UICONTROL Advanced]** 并选择 **[!UICONTROL System]**.

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 _图像上传配置_ 部分。

   要更改默认设置，请取消选择 **[!UICONTROL Use system value]** 复选框（如果需要）。

   ![图像上传配置](../configuration-reference/advanced/assets/system-image-upload-configuration.png){width="600" zoomable="yes"}

   有关这些配置设置的详细列表，请参阅 [_图像上传配置_](../configuration-reference/advanced/system.md#image-upload-configuration) 在 _配置引用_.

1. 要启用，请确保 **[!UICONTROL Enable Frontend Resize]** 设置为 `Yes`.

1. 输入 **[!UICONTROL Quality]** 设置介于 `1` 和 `100`%。

   为了减小文件大小并提高质量，建议设置80-90%。

1. 设置 **[!UICONTROL Maximum Width]** 图像的像素。

   调整图像大小时，它不会超过此宽度并保留比例。

1. 设置 **[!UICONTROL Maximum Height]** 图像的像素。

   在调整图像大小时，它不会超过此高度，并且会保留比例。

1. 完成后，单击 **[!UICONTROL Save Config]**.

### 字段描述

| 字段 | [范围](../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Quality] | 全局 | 确定调整后图像的JPG质量。 较低的质量会减小文件大小。 建议使用80-90%来帮助以高质量减小文件大小。 默认值：80 |
| [!UICONTROL Enable Frontend Resize] | 全局 | 允许Commerce调整您上传的大型、超大图像的大小， _[!UICONTROL Product Details]_页面。 在上传文件时，Commerce使用JavaScript调整图像文件的大小。 在调整图像大小时，它将保持精确比例，以符合并且不超过“最大宽度”或“最大高度”的最大尺寸。 默认： `Yes` |
| [!UICONTROL Maximum Width] | 全局 | 确定图像的最大像素宽度。 调整图像大小时，它不会超过此宽度。 默认： `1920` |
| [!UICONTROL Maximum Height] | 全局 | 确定图像的最大像素高度。 调整图像大小时，它不会超过此高度。 默认： `1200` |

{style="table-layout:auto"}

## 图像占位符

Adobe Commerce和Magento Open Source使用临时图像作为占位符，直到永久产品图像可用为止。 可以为每个角色上传不同的占位符。 初始占位符图像是一个示例徽标，您可以将其替换为您选择的图像。

![图像占位符](./assets/storefront-image-placeholder.png){width="600" zoomable="yes"}

**_要上传占位符图像，请执行以下操作：_**

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中，展开 **[!UICONTROL Catalog]** 并选择 **[!UICONTROL Catalog]** 下方。

1. 展开 ![“扩展”图标](../assets/icon-display-expand.png) 该 **[!UICONTROL Product Image Placeholders]** 部分。

   ![产品图像占位符](../configuration-reference/catalog/assets/catalog-product-image-placeholders.png){width="600" zoomable="yes"}

   有关这些配置设置的详细列表，请参阅 [_产品图像占位符_](../configuration-reference/catalog/catalog.md#product-image-placeholders) 在 _配置引用_.

1. 对于每个图像角色，单击 **[!UICONTROL Choose File]**，在计算机上找到图像并上传文件。

   您可以为全部三个角色使用相同的图像，也可以为每个角色上传不同的占位符图像。

1. 完成后，单击 **[!UICONTROL Save]**.

有关图像角色和建议大小的信息，请参阅 [上传图像](product-image.md#upload-an-image).

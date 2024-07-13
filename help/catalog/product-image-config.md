---
title: 产品图像配置
description: 了解如何设置最大像素大小（宽度和高度）并在上传期间自动调整产品图像文件的大小。
exl-id: d8fce5f8-eddf-4335-9a72-24036db077db
feature: Catalog Management, Products, Media
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '710'
ht-degree: 0%

---

# 产品图像配置

如果您计划上载大型图像以供在&#x200B;_[!UICONTROL Product Details]_页面上查看，则可能需要考虑设置最大像素大小（宽度和高度），并在上载时自动调整文件大小。 为了支持此类产品图像上传，有一个选项可在您上传大型图像文件时自动调整其大小。 对于要添加到目录但尚未显示图像资源的产品，可以配置占位符图像。

## 产品图像大小调整

上传产品图像时，您可以添加不同大小的大图像，以便在&#x200B;_[!UICONTROL Product Details]_页面上提供详细的高质量缩放。 要确保所有图像具有相似的大小和外观，可以使用图像大小调整选项来确保所有图像均匹配特定的像素大小。 此选项使用配置设置自动调整所有产品图像的大小，这有助于提高缩放性能、加快图像加载速度并保持产品图像的统一外观。

>[!NOTE]
>
>为获得最佳兼容性，建议使用`sRGB`颜色配置文件上载所有产品图像。 所有其他颜色配置文件在产品图像上传期间自动转换为`sRGB`颜色配置文件，这可能导致上传的图像出现颜色不一致。

设置最大像素宽度和高度可将图像大小按像素调整为物理尺寸。 Commerce会根据较高的宽度或高度调整图像大小，同时保持其比例。 降低JPG图像的质量可减小文件大小。

例如，100%的3000 x 2100像素JPG可能是5 mb或更大的图像文件。 调整此图像的大小会将宽度减少到1920像素，并保持比例和质量为80%，以提供小得多的文件大小和较高的质量。

### 启用图像大小调整

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧面板中，展开&#x200B;**[!UICONTROL Advanced]**&#x200B;并选择&#x200B;**[!UICONTROL System]**。

1. 展开![扩展选择器](../assets/icon-display-expand.png) _图像上传配置_&#x200B;部分。

   要更改默认设置，请根据需要取消选中&#x200B;**[!UICONTROL Use system value]**&#x200B;复选框。

   ![图像上传配置](../configuration-reference/advanced/assets/system-image-upload-configuration.png){width="600" zoomable="yes"}

   有关这些配置设置的详细列表，请参阅&#x200B;_配置引用_&#x200B;中的&#x200B;[_图像上传配置_](../configuration-reference/advanced/system.md#image-upload-configuration)。

1. 要启用，请确保&#x200B;**[!UICONTROL Enable Frontend Resize]**&#x200B;设置为`Yes`。

1. 输入介于`1`和`100`%之间的&#x200B;**[!UICONTROL Quality]**&#x200B;设置。

   为了减小文件大小并提高质量，建议设置80-90%。

1. 设置图像的&#x200B;**[!UICONTROL Maximum Width]**&#x200B;像素。

   调整图像大小时，它不会超过此宽度并保留比例。

1. 设置图像的&#x200B;**[!UICONTROL Maximum Height]**&#x200B;像素。

   在调整图像大小时，它不会超过此高度，并且会保留比例。

1. 完成后，单击&#x200B;**[!UICONTROL Save Config]**。

### 字段描述

| 字段 | [作用域](../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Quality] | 全局 | 确定调整后图像的JPG质量。 较低的质量会减小文件大小。 建议使用80-90%来帮助以高质量减小文件大小。 默认值：80 |
| [!UICONTROL Enable Frontend Resize] | 全局 | 允许Commerce调整您为&#x200B;_[!UICONTROL Product Details]_页面上传的大型、超大图像的大小。 上传文件时，Commerce会使用JavaScript调整图像文件的大小。 在调整图像大小时，它将保持精确比例，以符合并且不超过“最大宽度”或“最大高度”的最大尺寸。 默认： `Yes` |
| [!UICONTROL Maximum Width] | 全局 | 确定图像的最大像素宽度。 调整图像大小时，它不会超过此宽度。 默认： `1920` |
| [!UICONTROL Maximum Height] | 全局 | 确定图像的最大像素高度。 调整图像大小时，它不会超过此高度。 默认： `1200` |

{style="table-layout:auto"}

## 图像占位符

Adobe Commerce和Magento Open Source使用临时图像作为占位符，直到永久产品图像可用为止。 可以为每个角色上传不同的占位符。 初始占位符图像是一个示例徽标，您可以将其替换为您选择的图像。

![图像占位符](./assets/storefront-image-placeholder.png){width="600" zoomable="yes"}

**_要上载占位符图像：_**

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧面板中，展开&#x200B;**[!UICONTROL Catalog]**&#x200B;并在下面选择&#x200B;**[!UICONTROL Catalog]**。

1. 展开&#x200B;**[!UICONTROL Product Image Placeholders]**&#x200B;部分的![展开图标](../assets/icon-display-expand.png)。

   ![产品图像占位符](../configuration-reference/catalog/assets/catalog-product-image-placeholders.png){width="600" zoomable="yes"}

   有关这些配置设置的详细列表，请参阅&#x200B;_配置引用_&#x200B;中的&#x200B;[_产品图像占位符_](../configuration-reference/catalog/catalog.md#product-image-placeholders)。

1. 对于每个图像角色，单击&#x200B;**[!UICONTROL Choose File]**，在您的计算机上查找该图像，然后上载该文件。

   您可以为全部三个角色使用相同的图像，也可以为每个角色上传不同的占位符图像。

1. 完成后，单击&#x200B;**[!UICONTROL Save]**。

有关图像角色和建议大小的信息，请参阅[上传图像](product-image.md#upload-an-image)。

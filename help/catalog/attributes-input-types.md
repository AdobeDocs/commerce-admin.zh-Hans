---
title: 属性输入类型
description: 了解产品属性可用的输入类型，这些输入类型决定可输入的数据类型以及字段或输入控件的格式。
exl-id: c35b3b9d-57b0-4c33-abdb-662ac6d0260e
feature: Catalog Management, Products
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '637'
ht-degree: 0%

---

# 属性输入类型

从管理员中查看时，属性是您在创建产品时完成的字段。 分配给属性的输入类型决定了可以输入的数据类型以及字段或输入控件的格式。 从客户的角度看，属性提供了有关产品的信息，是购买产品必须填写的选项和数据输入字段。

## 输入类型

| 属性 | 描述 |
|--- |--- |
| [!UICONTROL Text Field] | 单行输入文本字段。 |
| [!UICONTROL Text Area] | 用于输入文本段落（如产品说明）的多行输入字段。 您可以使用WYSIWYG编辑器设置带有HTML标记的文本格式，或者直接在文本中输入标记。 |
| [!UICONTROL Text Editor] | 属性位置处具有完整功能的文本编辑器。 |
| [!UICONTROL Date] | 以[首选格式](#date-and-time-options)和[时区](../getting-started/store-details.md#locale-options)显示日期值。 可以从列表或日历（ ![日历图标](../assets/icon-calendar.png) ）中选择日期值。 <br/><br/>**_注意：_**&#x200B;根据您的系统配置，_管理员&#x200B;_用户可以在字段中直接输入日期或从日历或列表中选择日期。 有关指定日期和时间值的信息，请参阅[日期和时间选项](#date-and-time-options)。 |
| [!UICONTROL Date and Time] | 以[首选格式](#date-and-time-options)和[时区](../getting-started/store-details.md#locale-options)显示日期和时间值。 日期和时间可以手动输入，也可以从日历中选择。 示例格式： MM/DD/YYYY HH：MM |
| [!UICONTROL Yes/No] | 显示一个预定义选项为`Yes`和`No`的下拉列表。 |
| 下拉列表 | 显示仅接受单个选择的值的下拉列表。 下拉列表输入类型是[可配置产品](../catalog/product-create-configurable.md)的关键组件。 |
| [!UICONTROL Multiple Select] | 显示接受多个选择的值的下拉列表。 |
| [!UICONTROL Price] | 此输入类型用于创建预定义属性之外的价格字段：`Price`、`Special Price`、`Tier Price`和`Cost`。 使用的货币由系统配置决定。 |
| [!UICONTROL Media Image] | 将额外的图像与产品相关联，例如产品徽标、护理说明或食品标签中的成分。 将媒体图像属性添加到产品的属性集时，它将与基本图像、小型图像和缩略图一起成为额外的图像类型。 媒体图像属性可以从[店面媒体浏览器](catalog-images-video.md#storefront-media-browser)中排除。 |
| [!UICONTROL Fixed Product Tax] | 允许您根据区域设置要求定义[FPT费率](../stores-purchase/fixed-product-tax.md)。 |
| [!UICONTROL Visual Swatch] | 显示描述可配置产品的颜色、纹理或图案的色板。 [可视色板](swatches.md)可以用十六进制颜色值填充，或显示代表选项的颜色、材质、纹理或图案的上传图像。 |
| [!UICONTROL Text Swatch] | 经常用于表示大小的可配置产品选项的基于文本的表示形式。 [文本样本](swatches.md)还可以包含十六进制颜色值。 |
| [!UICONTROL Page Builder] | 位于属性位置的[[!DNL Page Builder]](../page-builder/workspace.md)工作区，可轻松将吸引人的内容添加到产品页面。 |

{style="table-layout:auto"}

## 日期和时间选项

您可以自定义日期和时间字段的格式，并选择用于数据输入的输入控件。 可以从下拉列表或弹出日历中选择日期值。

![示例 — 店面弹出日历](./assets/storefront-popup-calendar.png){width="700" zoomable="yes"}

**_格式化日期/时间字段：_**

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧的面板中，展开&#x200B;**[!UICONTROL Catalog]**&#x200B;并单击&#x200B;**[!UICONTROL Catalog]**&#x200B;子项。

1. 展开&#x200B;**[!UICONTROL Date & Time Custom Options]**&#x200B;部分。

   ![目录配置 — 日期和时间选项](../configuration-reference/catalog/assets/catalog-date-time-custom-options.png){width="600" zoomable="yes"}

   有关这些选项的详细列表，请参阅&#x200B;_配置引用_&#x200B;中的&#x200B;[_日期和时间自定义选项_](../configuration-reference/catalog/catalog.md)。

1. 若要使用弹出式日历作为日期字段的输入控件，请将&#x200B;**[!UICONTROL Use JavaScript Calendar]**&#x200B;设置为`Yes`。

1. 要建立&#x200B;**[!UICONTROL Date Fields Order]**，请根据需要设置日期字段各部分的顺序：

   - 月
   - 天
   - 年

1. 若要设置首选时间格式，请将&#x200B;**时间格式**&#x200B;设置为以下设置之一：

   - `12h AM/PM`
   - `24h`

1. 要为下拉值建立&#x200B;**[!UICONTROL Year Range]**，请输入年份(YYYY)以设置&#x200B;**[!UICONTROL from]**&#x200B;和&#x200B;**[!UICONTROL to]**&#x200B;日期。

   如果留空，则字段默认为当前年份。

1. 完成后，单击&#x200B;**[!UICONTROL Save Config]**。

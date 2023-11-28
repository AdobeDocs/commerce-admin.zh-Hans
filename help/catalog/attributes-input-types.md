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
| [!UICONTROL Date] | 在中显示日期值 [首选格式](#date-and-time-options) 和 [时区](../getting-started/store-details.md#locale-options). 可以从列表或日历中选择日期值( ![日历图标](../assets/icon-calendar.png) )。 <br/><br/>**_注意：_**根据您的系统配置，_管理员&#x200B;_用户可以直接在字段中输入日期，或从日历或列表中选择日期。 有关指定日期和时间值的信息，请参见 [日期和时间选项](#date-and-time-options). |
| [!UICONTROL Date and Time] | 在中显示日期和时间值 [首选格式](#date-and-time-options) 和 [时区](../getting-started/store-details.md#locale-options). 日期和时间可以手动输入，也可以从日历中选择。 示例格式： MM/DD/YYYY HH：MM |
| [!UICONTROL Yes/No] | 显示一个预定义选项的下拉列表 `Yes` 和 `No`. |
| 下拉列表 | 显示仅接受单个选择的值的下拉列表。 下拉列表输入类型是的关键组件 [可配置产品](../catalog/product-create-configurable.md). |
| [!UICONTROL Multiple Select] | 显示接受多个选择的值的下拉列表。 |
| [!UICONTROL Price] | 除了预定义属性之外，此输入类型还用于创建价格字段： `Price`， `Special Price`， `Tier Price`、和 `Cost`. 使用的货币由系统配置决定。 |
| [!UICONTROL Media Image] | 将额外的图像与产品相关联，例如产品徽标、护理说明或食品标签中的成分。 将媒体图像属性添加到产品的属性集时，它将与基本图像、小型图像和缩略图一起成为额外的图像类型。 媒体图像属性可从中排除 [店面媒体浏览器](catalog-images-video.md#storefront-media-browser). |
| [!UICONTROL Fixed Product Tax] | 允许您定义 [FPT率](../stores-purchase/fixed-product-tax.md) 根据您区域设置的要求而定。 |
| [!UICONTROL Visual Swatch] | 显示描述可配置产品的颜色、纹理或图案的色板。 A [可视色板](swatches.md) 可以使用十六进制颜色值填充，或者显示一个上传的图像，该图像表示选项的颜色、材质、纹理或图案。 |
| [!UICONTROL Text Swatch] | 经常用于表示大小的可配置产品选项的基于文本的表示形式。 [文本样本](swatches.md) 还可以包括十六进制颜色值。 |
| [!UICONTROL Page Builder] | A [[!DNL Page Builder]](../page-builder/workspace.md) 位于属性位置的工作区，可轻松地将吸引人的内容添加到产品页面。 |

{style="table-layout:auto"}

## 日期和时间选项

您可以自定义日期和时间字段的格式，并选择用于数据输入的输入控件。 可以从下拉列表或弹出日历中选择日期值。

![示例 — 店面弹出日历](./assets/storefront-popup-calendar.png){width="700" zoomable="yes"}

**_要设置日期/时间字段的格式，请执行以下操作：_**

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧的面板中，展开 **[!UICONTROL Catalog]** 然后单击 **[!UICONTROL Catalog]** 子项目。

1. 展开 **[!UICONTROL Date & Time Custom Options]** 部分。

   ![目录配置 — 日期和时间选项](../configuration-reference/catalog/assets/catalog-date-time-custom-options.png){width="600" zoomable="yes"}

   有关这些选项的详细列表，请参阅 [_日期和时间自定义选项_](../configuration-reference/catalog/catalog.md) 在 _配置引用_.

1. 要将弹出日历用作日期字段的输入控件，请设置 **[!UICONTROL Use JavaScript Calendar]** 到 `Yes`.

1. 建立 **[!UICONTROL Date Fields Order]**，根据需要设置日期字段各部分的顺序：

   - 月
   - 天
   - 年

1. 要设置首选时间格式，请设置 **时间格式** 更改为以下任一项：

   - `12h AM/PM`
   - `24h`

1. 建立 **[!UICONTROL Year Range]** 对于下拉值，输入year (YYYY)以设置 **[!UICONTROL from]** 和 **[!UICONTROL to]** 日期。

   如果留空，则字段默认为当前年份。

1. 完成后，单击 **[!UICONTROL Save Config]**.

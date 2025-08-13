---
title: '[!UICONTROL Sales] &amp；gt； [!UICONTROL Google API]'
description: 查看Commerce管理员的[!UICONTROL Sales] &amp；gt； [!UICONTROL Google API]页面上的配置设置。
exl-id: 5031ad3d-1c9a-4bc6-9bfa-683414dca979
feature: Configuration, Marketing Tools
source-git-commit: 5ee52e8d4f2ebb8fc28f13cca53e87c3529f76d3
workflow-type: tm+mt
source-wordcount: '899'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Google API]

{{config}}

## [!UICONTROL Google Analytics]

![Google Analytics](./assets/google-api-analytics-ee.png)<!-- zoom -->

<!-- [Google Analytics](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/google-tools/google-analytics) -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Enable] | 商店视图 | 为您的存储启用[!DNL Google Analytics]。 选项： `Yes` / `No` |
| [!UICONTROL Account Type] | 商店视图 | ![Adobe Commerce](../../assets/adobe-logo.svg)(仅限Adobe Commerce)根据您的Google Analytics帐户类型确定配置选项。 选项：Universal Analytics（默认）/Google标签管理器 |
| [!UICONTROL Account Number] | 商店视图 | 创建[!DNL Google Analytics]帐户时分配的帐号或跟踪代码。 |
| [!UICONTROL Anonymize IP] | 商店视图 | 确定是否从[!DNL Google Analytics]结果中显示的IP地址中删除标识信息。 |

{style="table-layout:auto"}

## [!UICONTROL Google Analytics - Google Tag Manager]

{{ee-feature}}

![Google Analytics - Google Tag Manager帐户类型](./assets/google-api-analytics-tag-manager.png)<!-- zoom -->

当&#x200B;**[!UICONTROL Account Type]**&#x200B;设置为`Google Tag Manager`时，将显示其他字段。

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Container ID] | 商店视图 | [!DNL Google Tag Manager]容器的唯一ID。 此值通常以`GTM-`开头。 此ID在您的[!DNL Google Tag Manager]帐户中。 如果已为商店安装和配置了[!DNL Google Tag Manager]，则容器ID会自动显示在此字段中。 |
| [!UICONTROL List property for the catalog page] | 商店视图 | 标识与目录页面关联的[!DNL Google Tag Manager]属性。 默认值： `Catalog Page` |
| [!UICONTROL List property for the cross-sell block] | 商店视图 | 标识与交叉销售块关联的[!DNL Google Tag Manager]属性。 默认值： `Cross-sell` |
| [!UICONTROL List property for the up-sell block] | 商店视图 | 标识与向上销售块关联的[!DNL Google Tag Manager]属性。 默认值： `Up-sell` |
| [!UICONTROL List property for the related products block] | 商店视图 | 标识与相关产品块关联的[!DNL Google Tag Manager]属性。 默认值： `Related Products` |
| [!UICONTROL List property for the search results page] | 商店视图 | 标识与搜索结果页面关联的[!DNL Google Tag Manager]属性。 默认值： `Search Results` |
| [!UICONTROL 'Internal Promotions' for promotions field "Label"] | 商店视图 | 标识与内部促销标签关联的[!DNL Google Tag Manager]属性。 默认值： `Label` |

{style="table-layout:auto"}

## [!UICONTROL Google AdWords]

![Google AdWords](./assets/google-api-google-adwords.png)<!-- zoom -->

<!-- [Google AdWords](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/google-tools/google-adwords) -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Enable] | 商店视图 | 为存储启用Google AdWords。 选项： `Yes` / `No` |
| [!UICONTROL Conversion ID] | 商店视图 | Google AdWords帐户中的ID。 |
| [!UICONTROL Conversion Language] | 商店视图 | 用于AdWords转换的语言。 选项： `All available languages` |
| [!UICONTROL Conversion Format] | 商店视图 | 确定转换页面上显示的[!DNL Google Site Stats]通知的格式。 通知链接到一个页面，该页面会通知访客有关用于跟踪其访问的Cookie。 此数值已分配给AdWords脚本中的`google_conversion_format`变量。 要了解更多信息，请参阅Google网站上的[关于转化跟踪](https://support.google.com/google-ads/answer/1722022?hl=en)。 选项： <br/>**`1`**— 显示一行通知。<br/>**`2`** — （默认）显示两行通知。 <br/>**`3`**— 不显示客户通知。 |
| [!UICONTROL Conversion Color] | 商店视图 | 确定转换标签的颜色。 使用[拾色器](https://www.w3schools.com/colors/colors_picker.asp)选择十六进制值。 此十六进制值已分配给AdWords脚本中的`google_conversion_color`变量。 例如： ffffff `var google_conversion_color = "ffffff";` |
| [!UICONTROL Conversion Label] | 商店视图 | 随[!DNL Google Site Stats]通知一起显示的文本标签。 此文本字符串已分配给AdWords脚本中的`~`变量。 例如：“感谢您购物！” |
| [!UICONTROL Conversion Value Type] | 商店视图 | 指定用于确定何时进行转换的值类型。 选项： <br/>**`Dynamic`**— 根据动态订单金额确定已发生转换。<br/>**`Constant`** — 根据输入的值确定已发生转换。 |
| [!UICONTROL Conversion Value] | 商店视图 | 指定用于&#x200B;_[!UICONTROL Constant]_&#x200B;转换值类型的值。 |
| [!UICONTROL Send Order Currency] | 商店视图 | 在AdWords中启用特定于交易的货币转换值（适用于使用不同基础货币的网站）。 |

{style="table-layout:auto"}

## [!UICONTROL Google GTag]

{{gtag-api-note}}

### [!UICONTROL Google Analytics4]

![Google Analytics4](./assets/google-api-gtag-google-analytics4.png)<!-- zoom -->

<!-- [Google Analytics4](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/google-tools/google-analytics) -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Enable] | 商店视图 | 为您的商店启用Google Analytics 4。 选项： `Yes` / `No` |
| [!UICONTROL Account Type] | 商店视图 | ![Adobe Commerce](../../assets/adobe-logo.svg)(仅限Adobe Commerce)根据您的Google Analytics帐户类型确定配置选项。 选项： `Google Analytics4` （默认） / `Google Tag Manager` |
| [!UICONTROL Measurement ID] | 商店视图 | 创建Google Analytics帐户时分配的帐号或跟踪代码。 |
| [!UICONTROL Anonymize IP] | 商店视图 | 确定是否从Google Analytics结果中显示的IP地址中删除标识信息。 |

{style="table-layout:auto"}

### [!UICONTROL Google Analytics4 - Google Tag Manager]

{{ee-feature}}

![Google Analytics4 - Google Tag Manager帐户类型](./assets/google-api-gtag-google-analytics4-gtm.png)<!-- zoom -->

当&#x200B;**[!UICONTROL Account Type]**&#x200B;设置为`Google Tag Manager`时，将显示其他字段。

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Container Id] | 商店视图 | [!DNL Google Tag Manager]容器的唯一ID。 此值通常以`GTM-`开头。 此ID位于您的Google选项卡管理器帐户中。 如果已为商店安装和配置了[!DNL Google Tag Manager]，则容器ID会自动显示在此字段中。 |
| [!UICONTROL List property for the catalog page] | 商店视图 | 标识与目录页面关联的[!DNL Google Tag Manager]属性。 默认值： `Catalog Page` |
| [!UICONTROL List property for the cross-sell block] | 商店视图 | 标识与交叉销售块关联的[!DNL Google Tag Manager]属性。 默认值： `Cross-sell` |
| [!UICONTROL List property for the up-sell block] | 商店视图 | 标识与向上销售块关联的[!DNL Google Tag Manager]属性。 默认值： `Up-sell` |
| [!UICONTROL List property for the related products block] | 商店视图 | 标识与相关产品块关联的[!DNL Google Tag Manager]属性。 默认值： `Related Products` |
| [!UICONTROL List property for the search results page] | 商店视图 | 标识与搜索结果页面关联的[!DNL Google Tag Manager]属性。 默认值： `Search Results` |
| [!UICONTROL 'Internal Promotions' for promotions field "Label"] | 商店视图 | 标识与内部促销标签关联的[!DNL Google Tag Manager]属性。 默认值： `Label` |

{style="table-layout:auto"}

### [!UICONTROL Google AdWords]

![Google AdWords](./assets/google-api-gtag-google-adwords.png)<!-- zoom -->

<!-- -- Google AdWords](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/google-tools/google-adwords) -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Enable] | 商店视图 | 为存储启用Google AdWords。 选项： `Yes` / `No` |
| [!UICONTROL Conversion ID] | 商店视图 | Google AdWords帐户中的ID。 |
| [!UICONTROL Conversion Language] | 商店视图 | 用于AdWords转换的语言。 选项：所有可用语言 |
| [!UICONTROL Conversion Format] | 商店视图 | 确定在转化页面上显示的Google站点统计信息通知的格式。 通知链接到一个页面，该页面会通知访客有关用于跟踪其访问的Cookie。 此数值已分配给AdWords脚本中的`google_conversion_format`变量。 要了解更多信息，请参阅Google网站上的[关于转化跟踪](https://support.google.com/google-ads/answer/1722022?hl=en)。 选项： <br/>**`1`**— 显示一行通知。<br/>**`2`** — （默认）显示两行通知。 <br/>**`3`**— 不显示客户通知。 |
| [!UICONTROL Conversion Color] | 商店视图 | 确定转换标签的颜色。 使用[拾色器](https://www.w3schools.com/colors/colors_picker.asp)选择十六进制值。 此十六进制值已分配给AdWords脚本中的`google_conversion_color`变量。 例如： ffffff `var google_conversion_color = "ffffff";` |
| [!UICONTROL Conversion Label] | 商店视图 | 随Google站点统计信息通知一起显示的文本标签。 此文本字符串已分配给AdWords脚本中的`~`变量。 例如：“感谢您购物！” |
| [!UICONTROL Conversion Value Type] | 商店视图 | 指定用于确定何时进行转换的值类型。 选项： <br/>**`Dynamic`**— 根据动态订单金额确定已发生转换。<br/>**`Constant`** — 根据输入的值确定已发生转换。 |
| [!UICONTROL Conversion Value] | 商店视图 | 指定用于&#x200B;_[!UICONTROL Constant]_&#x200B;转换值类型的值。 |
| [!UICONTROL Send Order Currency] | 商店视图 | 在AdWords中启用特定于交易的货币转换值（适用于使用不同基础货币的网站）。 |

{style="table-layout:auto"}

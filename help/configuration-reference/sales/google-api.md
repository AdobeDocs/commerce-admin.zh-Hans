---
title: ’[!UICONTROL Sales] &gt； [!UICONTROL Google API]’
description: 查看 [!UICONTROL Sales] &gt； [!UICONTROL Google API] 商务管理员页面。
exl-id: 5031ad3d-1c9a-4bc6-9bfa-683414dca979
feature: Configuration, Marketing Tools
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '978'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Google API]

{{config}}

## [!UICONTROL Google Analytics]

![Google Analytics](./assets/google-api-analytics-ee.png)<!-- zoom -->

<!-- [Google Analytics](https://docs.magento.com/user-guide/marketing/google-universal-analytics.html) -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Enable] | 商店视图 | 启用 [!DNL Google Analytics] 你商店的。 选项： `Yes` / `No` |
| [!UICONTROL Account Type] | 商店视图 | ![Adobe Commerce](../../assets/adobe-logo.svg) (仅限Adobe Commerce)根据您的Google Analytics帐户类型确定配置选项。 选项：Universal Analytics（默认）/Google标签管理器 |
| [!UICONTROL Account Number] | 商店视图 | 您在创建时分配的帐号或跟踪代码 [!DNL Google Analytics] 帐户。 |
| [!UICONTROL Anonymize IP] | 商店视图 | 确定是否从显示于的IP地址中删除标识信息 [!DNL Google Analytics] 个结果。 |
| [!UICONTROL Enable Content Experiments] | 商店视图 | 激活 [Google内容实验](https://support.google.com/analytics/answer/9366791?hl=en&amp;ref_topic=1745207)，可用于测试同一页面的最多十个不同版本。 选项： `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Google Analytics - Google Tag Manager]

{{ee-feature}}

![Google Analytics- Google标签管理器帐户类型](./assets/google-api-analytics-tag-manager.png)<!-- zoom -->

时间 **[!UICONTROL Account Type]** 设置为 `Google Tag Manager`，则会显示其他字段。

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Container ID] | 商店视图 | 的唯一Id [!DNL Google Tag Manager] 容器。 此值通常以 `GTM-`. 此ID位于您的 [!DNL Google Tag Manager] 帐户。 如果 [!DNL Google Tag Manager] 已经为您的商店安装和配置，容器ID会自动显示在此字段中。 |
| [!UICONTROL List property for the catalog page] | 商店视图 | 标识 [!DNL Google Tag Manager] 与目录页面关联的属性。 默认值： `Catalog Page` |
| [!UICONTROL List property for the cross-sell block] | 商店视图 | 标识 [!DNL Google Tag Manager] 与交叉销售块关联的属性。 默认值： `Cross-sell` |
| [!UICONTROL List property for the up-sell block] | 商店视图 | 标识 [!DNL Google Tag Manager] 与向上销售区块关联的属性。 默认值： `Up-sell` |
| [!UICONTROL List property for the related products block] | 商店视图 | 标识 [!DNL Google Tag Manager] 与相关产品块关联的属性。 默认值： `Related Products` |
| [!UICONTROL List property for the search results page] | 商店视图 | 标识 [!DNL Google Tag Manager] 与搜索结果页面关联的属性。 默认值： `Search Results` |
| [!UICONTROL 'Internal Promotions' for promotions field "Label"] | 商店视图 | 标识 [!DNL Google Tag Manager] 与内部促销的标签关联的属性。 默认值： `Label` |

{style="table-layout:auto"}

## [!UICONTROL Google AdWords]

![Google AdWords](./assets/google-api-google-adwords.png)<!-- zoom -->

<!-- [Google AdWords](https://docs.magento.com/user-guide/marketing/google-adwords.html) -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Enable] | 商店视图 | 为存储启用Google AdWords。 选项： `Yes` / `No` |
| [!UICONTROL Conversion ID] | 商店视图 | Google AdWords帐户中的ID。 |
| [!UICONTROL Conversion Language] | 商店视图 | 用于AdWords转换的语言。 选项： `All available languages` |
| [!UICONTROL Conversion Format] | 商店视图 | 确定 [!DNL Google Site Stats] 显示在转化页面上的通知。 通知链接到一个页面，该页面会通知访客有关用于跟踪其访问的Cookie。 此数值将分配给 `google_conversion_format` 变量标识。 要了解更多信息，请参阅 [关于转化跟踪](https://support.google.com/google-ads/answer/1722022?hl=en) 在Google网站上。 选项： <br/>**`1`**— 显示一行通知。<br/>**`2`**  — （默认）显示两行通知。 <br/>**`3`**— 不显示客户通知。 |
| [!UICONTROL Conversion Color] | 商店视图 | 确定转换标签的颜色。 使用 [拾色器](https://www.w3schools.com/colors/colors_picker.asp) 以选择十六进制值。 此十六进制值被分配给 `google_conversion_color` 变量标识。 例如： ffffff  `var google_conversion_color = "ffffff";` |
| [!UICONTROL Conversion Label] | 商店视图 | 文本标签，显示时带有 [!DNL Google Site Stats] 通知。 此文本字符串将分配给 `~` 变量标识。 例如：“感谢您购物！” |
| [!UICONTROL Conversion Value Type] | 商店视图 | 指定用于确定何时进行转换的值类型。 选项： <br/>**`Dynamic`**— 根据动态订单金额确定已发生转换。<br/>**`Constant`**  — 根据输入的值确定已发生转换。 |
| [!UICONTROL Conversion Value] | 商店视图 | 指定用于 _[!UICONTROL Constant]_转化值类型。 |
| [!UICONTROL Send Order Currency] | 商店视图 | 在AdWords中启用特定于交易的货币转换值（适用于使用不同基础货币的网站）。 |

{style="table-layout:auto"}

## [!UICONTROL Google GTag]

{{gtag-api-note}}

### [!UICONTROL Google Analytics4]

![GOOGLE ANALYTICS4](./assets/google-api-gtag-google-analytics4.png)<!-- zoom -->

<!-- [Google Analytics4](https://docs.magento.com/user-guide/marketing/google-universal-analytics.html) -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Enable] | 商店视图 | 为您的商店启用Google Analytics4。 选项： `Yes` / `No` |
| [!UICONTROL Account Type] | 商店视图 | ![Adobe Commerce](../../assets/adobe-logo.svg) (仅限Adobe Commerce)根据您的Google Analytics帐户类型确定配置选项。 选项： `Google Analytics4` （默认） / `Google Tag Manager` |
| [!UICONTROL Measurement ID] | 商店视图 | 创建Google Analytics帐户时分配的帐号或跟踪代码。 |
| [!UICONTROL Anonymize IP] | 商店视图 | 确定是否从Google Analytics结果中显示的IP地址中删除标识信息。 |
| [!UICONTROL Enable Content Experiments] | 商店视图 | 激活 [Google内容实验](https://support.google.com/analytics/answer/9366791?hl=en&amp;ref_topic=1745207)，可用于测试同一页面的最多十个不同版本。 选项： `Yes` / `No` |

{style="table-layout:auto"}

### [!UICONTROL Google Analytics4 - Google Tag Manager]

{{ee-feature}}

![Google Analytics4 - Google Tag Manager帐户类型](./assets/google-api-gtag-google-analytics4-gtm.png)<!-- zoom -->

时间 **[!UICONTROL Account Type]** 设置为 `Google Tag Manager`，则会显示其他字段。

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Container Id] | 商店视图 | 的唯一Id [!DNL Google Tag Manager] 容器。 此值通常以 `GTM-`. 此ID位于您的Google选项卡管理器帐户中。 如果 [!DNL Google Tag Manager] 已经为您的商店安装和配置，容器ID会自动显示在此字段中。 |
| [!UICONTROL List property for the catalog page] | 商店视图 | 标识 [!DNL Google Tag Manager] 与目录页面关联的属性。 默认值： `Catalog Page` |
| [!UICONTROL List property for the cross-sell block] | 商店视图 | 标识 [!DNL Google Tag Manager] 与交叉销售块关联的属性。 默认值： `Cross-sell` |
| [!UICONTROL List property for the up-sell block] | 商店视图 | 标识 [!DNL Google Tag Manager] 与向上销售区块关联的属性。 默认值： `Up-sell` |
| [!UICONTROL List property for the related products block] | 商店视图 | 标识 [!DNL Google Tag Manager] 与相关产品块关联的属性。 默认值： `Related Products` |
| [!UICONTROL List property for the search results page] | 商店视图 | 标识 [!DNL Google Tag Manager] 与搜索结果页面关联的属性。 默认值： `Search Results` |
| [!UICONTROL 'Internal Promotions' for promotions field "Label"] | 商店视图 | 标识 [!DNL Google Tag Manager] 与内部促销的标签关联的属性。 默认值： `Label` |

{style="table-layout:auto"}

### [!UICONTROL Google AdWords]

![Google AdWords](./assets/google-api-gtag-google-adwords.png)<!-- zoom -->

<!-- -- Google AdWords](https://docs.magento.com/user-guide/marketing/google-adwords.html) -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Enable] | 商店视图 | 为存储启用Google AdWords。 选项： `Yes` / `No` |
| [!UICONTROL Conversion ID] | 商店视图 | Google AdWords帐户中的ID。 |
| [!UICONTROL Conversion Language] | 商店视图 | 用于AdWords转换的语言。 选项：所有可用语言 |
| [!UICONTROL Conversion Format] | 商店视图 | 确定在转化页面上显示的Google站点统计信息通知的格式。 通知链接到一个页面，该页面会通知访客有关用于跟踪其访问的Cookie。 此数值将分配给 `google_conversion_format` 变量标识。 要了解更多信息，请参阅 [关于转化跟踪](https://support.google.com/google-ads/answer/1722022?hl=en) 在Google网站上。 选项： <br/>**`1`**— 显示一行通知。<br/>**`2`**  — （默认）显示两行通知。 <br/>**`3`**— 不显示客户通知。 |
| [!UICONTROL Conversion Color] | 商店视图 | 确定转换标签的颜色。 使用 [拾色器](https://www.w3schools.com/colors/colors_picker.asp) 以选择十六进制值。 此十六进制值被分配给 `google_conversion_color` 变量标识。 例如： ffffff  `var google_conversion_color = "ffffff";` |
| [!UICONTROL Conversion Label] | 商店视图 | 随Google站点统计信息通知一起显示的文本标签。 此文本字符串将分配给 `~` 变量标识。 例如：“感谢您购物！” |
| [!UICONTROL Conversion Value Type] | 商店视图 | 指定用于确定何时进行转换的值类型。 选项： <br/>**`Dynamic`**— 根据动态订单金额确定已发生转换。<br/>**`Constant`**  — 根据输入的值确定已发生转换。 |
| [!UICONTROL Conversion Value] | 商店视图 | 指定用于 _[!UICONTROL Constant]_转化值类型。 |
| [!UICONTROL Send Order Currency] | 商店视图 | 在AdWords中启用特定于交易的货币转换值（适用于使用不同基础货币的网站）。 |

{style="table-layout:auto"}

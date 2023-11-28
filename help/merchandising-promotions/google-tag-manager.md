---
title: '[!DNL Google Tag Manager]'
description: 了解如何使用 [!DNL Google Tag Manager] 用于管理与您的Adobe Commerce网站中的营销活动相关的许多标记（代码片段）。
exl-id: 9c24239b-9efd-42ee-9b99-5a194f3c4347
feature: Marketing Tools, Integration
source-git-commit: 7384481d1a4a2a04882d4c99448cca75abc9be31
workflow-type: tm+mt
source-wordcount: '1161'
ht-degree: 0%

---

# [!DNL Google Tag Manager]

{{ee-feature}}

[!DNL Google Tag Manager] 可帮助您管理与营销活动事件相关的许多标记（代码片段）。 [!DNL Google Tag Manager] 允许您向网站添加跟踪标记以测量受众，或者个性化、重新定位或执行搜索引擎营销计划。

[!DNL Google Tag Manager] 将数据和事件直接传输到 [!DNL Google Analytics]、增强的电子商务和其他第三方分析解决方案，可清楚地了解您的网站、产品和促销的表现如何。

您应该有一个 [!DNL Google Analytics] 和 [!DNL Tag Manager] 帐户，以继续此过程。 以下说明将指导您完成配置Google帐户、配置Commerce商店和创建标记的过程。

>[!NOTE]
>
>如果您的业务受隐私法规的约束，例如 [通用数据保护条例](../getting-started/compliance-gdpr.md) 和/或 [《加州消费者隐私法案》](../getting-started/compliance-ccpa.md)，请参见 [Google隐私设置](google-tools.md#google-privacy-settings).

## 步骤1. 配置您的 [!DNL Google Analytics] 帐户

请参阅 [设置站点搜索](https://support.google.com/analytics/answer/1012264) 如需入门指南所需的基础知识，请参阅Google帮助。 另请参阅Google指南 [Google Analytics](https://support.google.com/analytics/answer/9304153) 和 [Google Tag Manager](https://support.google.com/tagmanager/answer/6102821).

1. 登录到您的 [!DNL Google Analytics] 帐户。

1. 要启用 **[!UICONTROL Internal Site Search Tracking]**，请执行以下操作：

   - 导航到 **[!UICONTROL Select View]** > **[!UICONTROL View Settings]**.

   - 设置 **[!UICONTROL Site Search Tracking]** 到 `On`.

   - 设置 **[!UICONTROL Query]** 参数至 `q`.

   - 完成后， **[!UICONTROL Save]** 设置。

1. 要启用显示功能，请执行以下操作：

   - 选择 **[!UICONTROL Property Settings]**.

   - 下 _[!UICONTROL Advertising Features]_，设置&#x200B;**[!UICONTROL Enable Demographics and Interest Reports]**到 `On`.

   - **[!UICONTROL Save]** 设置。

1. 要启用电子商务跟踪，请执行以下操作：

   - 导航到 **[!UICONTROL Select View]** > **[!UICONTROL Ecommerce Settings]**.

   - 设置 **[!UICONTROL Enable Ecommerce]** 到 `On`.

   - 设置 **[!UICONTROL Enable Enhanced Ecommerce Reporting]** 到 `On`.

   - **[!UICONTROL Save]** 设置。

1. 重新加载页面，并验证所有设置是否仍保留 `On`.

   >[!NOTE]
   >
   >如果不是所有设置 `On`，重复上述步骤，保存并重新加载页面。 重复此过程，直到所有设置均设置为 `On`.

## 步骤2. 配置您的 [!DNL Google Tag Manager] 帐户

以下说明显示如何使用基本设置配置新容器。 示例 [Composer](https://developer.adobe.com/commerce/php/development/composer/) 配置(.json)文件用于简化此过程，导入可在新容器中生成标记。 对于此示例，建议创建容器，而不是修改现有容器。

>[!NOTE]
>
>有关更多信息，请参阅Google的 [集装箱导出和导入](https://support.google.com/tagmanager/answer/6106997). 这些说明提供了一个演练，介绍如何在新容器中导入示例JSON。

1. 下载链接的文件 [GTM_M2_Config_json.txt](./assets/GTM_M2_Config_json.txt)，在编辑器中打开文件，并将其另存为 `GTM_M2_Config.json`.

   json文件直接上传到 [!DNL Google Tag Manager].

1. 导航到 **[!UICONTROL Admin]** > **[!UICONTROL Container]** > **[!UICONTROL Import Container]**.

1. 单击 **[!UICONTROL Choose container file]** 并选择json文件。

1. 下 **[!UICONTROL Choose workspace]**，单击 **[!UICONTROL New]**.

1. 输入标题和说明，然后单击 **[!UICONTROL Save]**.

1. 要导入文件，请选择以下操作之一：

   - 此 **[!UICONTROL Overwrite]** 应该为新容器选择选项。

   - 此 **[!UICONTROL Merge]** 如果您使用的是现有容器，则应选择选项。

1. 单击 **[!UICONTROL Preview]** 查看标记、触发器和变量。

1. 要编辑 **[!UICONTROL Google Analytics ID]** ，请执行以下操作：

   - 导航到 **[!UICONTROL Variables]** > **[!UICONTROL User-Defined Variables]**.

   - 选择 **[!UICONTROL Google Analytics]** 并更新占位符(`UA-xxxxxx-x`)，使用您自己的 **[!UICONTROL GA ID]**.

1. 按照Google的说明将标记、触发器和变量添加到新容器。

   如果您在其他要使用的容器中有设置，则可以将它们移动到新容器。

1. 单击 **[!UICONTROL Confirm]** 完成后。

1. 按照Google的说明发布新容器。

## 步骤3. 配置您的商店

{{gtag-api-note}}

1. 登录到Commerce商店的管理员。

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中，展开 **[!UICONTROL Sales]** 并选择 **[!UICONTROL Google API]**.

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Google Analytics]** 部分并配置以下内容：

   ![Sales配置 — Google Analytics](../configuration-reference/sales/assets/google-api-analytics-tag-manager.png){width="600" zoomable="yes"}

   - 设置 **[!UICONTROL Enable]** 到 `Yes`.

   - 设置 **[!UICONTROL Account type]** 到 `Google Tag Manager`.

   - 在 **[!UICONTROL Container ID]** 字段中，输入您的GTM ID (`GTM-xxxxxx`)。

   - 如果您还使用Google Analytics内容试验，请设置 **启用内容试验** 到 `Yes`.

   - 对其余字段使用默认值。

1. 完成后，单击 **[!UICONTROL Save Config]**.

1. 测试您的 [!DNL Google Tag Manager] 设置并验证所有组件是否正常工作。

>[!NOTE]
>
>每个容器均与一个网站关联，每个帐户只需一个容器。 如果您有一个多站点商务实例，则需要单独的容器。

## 步骤4. 将GTM代码添加到Adobe Commerce应用商店

1. 要复制GTM代码，请转到 **[!UICONTROL Admin]** > **[!UICONTROL Install Google Tag Manager]**.

   有两个GTM代码片段要添加到您的Commerce网站：第一个是 `<head>` 标记和针对的第二个 `<body>` 标记之前。

1. 在Commerce管理员中，转到 **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**并以编辑模式打开商店视图。

1. 下 _[!UICONTROL Other Settings]_，展开&#x200B;**[!UICONTROL HTML Head]**并粘贴您从GTM复制的代码，用于 `<head>` 标记中&#x200B;**[!UICONTROL Scripts and Style Sheets]**字段。

   ![在HTML头中插入代码](./assets/head-tag.png){width="600" zoomable="yes"}

1. 展开 **[!UICONTROL Footer]** 并粘贴的GTM代码 `<body>` 在 **[!UICONTROL Miscellaneous HTML]** 字段。

   ![在页脚中插入代码](./assets/footer-tag-section.png){width="600" zoomable="yes"}

1. 完成后，单击 **[!UICONTROL Save Configuration]**.

## 字段描述

| 字段 | 范围 | 描述 |
|--- |--- |--- |
| [!UICONTROL Enable] | 商店视图 | 确定是否可以使用Google Analytics Enhanced E-commerce分析商店中的活动。 选项： `Yes` / `No` |
| [!UICONTROL Account type] | 商店视图 | 确定用于监视商店活动和流量的Google跟踪代码。 选项： `Google Analytics` / `Google Tag Manager` |
| [!UICONTROL Anonymize IP] | 商店视图 | 确定是否从Google Analytics结果中显示的IP地址中删除标识信息。 |
| [!UICONTROL Enable Content Experiments] | 商店视图 | 激活Google内容实验，该实验可用于测试同一页面的最多十个不同版本。 选项： `Yes` / `No` |
| [!UICONTROL Container Id] | 商店视图 | 如果 [!DNL Google Tag Manager] 已经为您的商店安装和配置，容器ID会自动显示在此字段中。 |
| [!UICONTROL List property for the catalog page] | 商店视图 | 标识与目录页面关联的Tag Manager属性。 默认值： `Catalog Page` |
| [!UICONTROL List property for the cross-sell block] | 商店视图 | 标识与交叉销售块关联的Tag Manager属性。 默认值： `Cross-sell` |
| [!UICONTROL List property for the up-sell block] | 商店视图 | 标识与向上销售块关联的Tag Manager属性。 默认值： `Up-sell` |
| [!UICONTROL List property for the related products block] | 商店视图 | 标识与相关产品块关联的Tag Manager属性。 默认值： `Related Products` |
| [!UICONTROL List property for the search results page] | 商店视图 | 标识与搜索结果页面关联的Tag Manager属性。 默认值： `Search Results` |
| [!UICONTROL "Internal Promotions" for promotions field "Label"] | 商店视图 | 标识与内部促销标签关联的Tag Manager属性。 默认值： `Label` |

{style="table-layout:auto"}

## 创建标记以跟踪转化

如果您拥有Google AdWords帐户，则可以创建跟踪转化的标记。 以下示例说明如何使用这两种方法 [!DNL Google Tag Manager] 和 [!DNL Google Analytics] 创建在商店转化时触发的标记 _成功_ 页面。

### 步骤1. 创建标记

1. 登录 [!DNL Google Tag Manager] 帐户，然后单击为商店创建的容器的链接。

1. 在 **[!UICONTROL New Tag]** 框中，单击 **[!UICONTROL Add a new tag]**.

1. 从您的AdWords帐户获取以下信息：

   - 转换ID
   - 转化标签

   如果您需要帮助，请访问Google的 [支持站点](https://support.google.com/tagmanager/answer/6105160).

1. 从 [!DNL Google Tag Manager] 仪表板，单击 **[!UICONTROL Google AdWords]** 并执行以下操作：

   - 单击标题占位符并输入新标记的名称。

   - 下 **[!UICONTROL Choose Product]**，选择 **[!UICONTROL Google AdWords]**.

   - 下 _[!UICONTROL Choose a Tag Type]_，选择&#x200B;**[!UICONTROL AdWords Conversion Tracking]**并单击&#x200B;**[!UICONTROL Continue]**.

1. 输入 **[!UICONTROL Conversion ID]** 和 **[!UICONTROL Conversion Label]** 从您的AdWords帐户访问，然后单击 **[!UICONTROL Continue]**.

### 步骤2. 创建规则

继续从 [!DNL Google Tag Manager] 仪表板中，下一步是创建一个规则，以在转化页面上触发标记。

1. 下 **[!UICONTROL Fire On]**，单击 **[!UICONTROL Some Pages]**.

1. 在 _[!UICONTROL Choose Pages]_部分，完成以下设置：

   - **[!UICONTROL Name]**  — 输入页面说明的名称。

   - **[!UICONTROL Variable]** `url`

   - **操作** - `matches RegEx`

     要了解更多信息，请参阅 [正则表达式和CSS选择器运算符](https://support.google.com/tagmanager/answer/7679109) Google Tag Manager帮助中的。

   - **[!UICONTROL Value]** - `checkout/success.*`

1. 选中绿色复选框并单击 **[!UICONTROL Save]**.

   您设置的触发器在“点击”部分显示为蓝色按钮。

1. 完成后，单击 **[!UICONTROL Save Tag]**.

### 步骤3. 预览和发布

该过程的下一步是预览标记。 每次预览标记时，都会保存版本的快照。 如果对结果满意，请转到要使用的版本，然后单击 **[!UICONTROL Publish]**.

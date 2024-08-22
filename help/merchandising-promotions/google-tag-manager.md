---
title: '[!DNL Google Tag Manager]'
description: 了解如何使用 [!DNL Google Tag Manager] 管理Adobe Commerce网站中与营销活动活动相关的许多标记（代码片段）。
exl-id: 9c24239b-9efd-42ee-9b99-5a194f3c4347
feature: Marketing Tools, Integration
source-git-commit: be426ca16fb7a72ebeda4a2f92c0f0062a9acc62
workflow-type: tm+mt
source-wordcount: '1050'
ht-degree: 0%

---

# [!DNL Google Tag Manager]

{{ee-feature}}

[!DNL Google Tag Manager]是一个功能强大的工具，可帮助您高效地管理和部署与营销活动事件相关的各种标记（代码片段）。 [!DNL Google Tag Manager]使您能够向网站添加跟踪标记以测量受众，或者个性化、重新定位或执行搜索引擎营销计划。

[!DNL Google Tag Manager]直接将数据和事件传输到[!DNL Google Analytics]、增强型电子商务和其他第三方分析解决方案，以清楚地了解您的网站、产品和促销活动的执行情况。

您应该具有[!DNL Google Analytics]和[!DNL Tag Manager]帐户以继续此过程。 以下说明将指导您完成配置Google帐户、配置Commerce商店和创建标记的过程。

>[!NOTE]
>
>如果您的业务受隐私法规约束，例如[通用数据保护条例](../getting-started/compliance-gdpr.md)和/或[加州消费者隐私法案](../getting-started/compliance-ccpa.md)，请参阅[Google隐私设置](google-tools.md#google-privacy-settings)。

## 步骤1. 配置您的[!DNL Google Analytics]帐户

有关入门所需的基础知识，请参阅Google帮助中的[设置网站搜索](https://support.google.com/analytics/answer/1012264)。 另请参阅[Google Analytics](https://support.google.com/analytics/answer/9304153)和[Google Tag Manager](https://support.google.com/tagmanager/answer/6102821)的Google指南。

1. 登录到您的[!DNL Google Analytics]帐户。

1. 要启用&#x200B;**[!UICONTROL Internal Site Search Tracking]**，请执行以下操作：

   - 导航到&#x200B;**[!UICONTROL Select View]** > **[!UICONTROL View Settings]**。

   - 将&#x200B;**[!UICONTROL Site Search Tracking]**&#x200B;设置为`On`。

   - 将&#x200B;**[!UICONTROL Query]**&#x200B;参数设置为`q`。

   - 完成后，**[!UICONTROL Save]**&#x200B;设置。

1. 要启用显示功能，请执行以下操作：

   - 选择&#x200B;**[!UICONTROL Property Settings]**。

   - 在&#x200B;_[!UICONTROL Advertising Features]_下，将&#x200B;**[!UICONTROL Enable Demographics and Interest Reports]**设置为`On`。

   - **[!UICONTROL Save]**&#x200B;设置。

1. 要启用电子商务跟踪，请执行以下操作：

   - 导航到&#x200B;**[!UICONTROL Select View]** > **[!UICONTROL Ecommerce Settings]**。

   - 将&#x200B;**[!UICONTROL Enable Ecommerce]**&#x200B;设置为`On`。

   - 将&#x200B;**[!UICONTROL Enable Enhanced Ecommerce Reporting]**&#x200B;设置为`On`。

   - **[!UICONTROL Save]**&#x200B;设置。

1. 重新加载页面，并确认所有设置仍为`On`。

   >[!NOTE]
   >
   >如果并非所有设置都是`On`，请重复上述步骤，保存并重新加载页面。 重复此过程，直到所有设置都设置为`On`。

## 步骤2. 配置您的[!DNL Google Tag Manager]帐户

以下说明显示如何使用基本设置配置新容器。 使用示例[Composer](https://developer.adobe.com/commerce/php/development/composer/)配置(.json)文件简化流程，导入文件以在新容器中生成标记。 对于此示例，建议创建容器，而不是修改现有容器。

>[!NOTE]
>
>有关详细信息，请参阅Google的[容器导出和导入](https://support.google.com/tagmanager/answer/6106997)。 这些说明提供了一个演练，介绍如何在新容器中导入示例JSON。

1. 下载链接的文件[GTM_M2_Config_json.txt](./assets/GTM_M2_Config_json.txt)，在编辑器中打开该文件，并将其另存为`GTM_M2_Config.json`。

   json文件已直接上传到[!DNL Google Tag Manager]。

1. 导航到&#x200B;**[!UICONTROL Admin]** > **[!UICONTROL Container]** > **[!UICONTROL Import Container]**。

1. 单击&#x200B;**[!UICONTROL Choose container file]**&#x200B;并选择json文件。

1. 在&#x200B;**[!UICONTROL Choose workspace]**&#x200B;下，单击&#x200B;**[!UICONTROL New]**。

1. 输入标题和说明，然后单击&#x200B;**[!UICONTROL Save]**。

1. 要导入文件，请选择以下操作之一：

   - 应该为新容器选择&#x200B;**[!UICONTROL Overwrite]**&#x200B;选项。

   - 如果您使用现有容器，则应选择&#x200B;**[!UICONTROL Merge]**&#x200B;选项。

1. 单击&#x200B;**[!UICONTROL Preview]**&#x200B;以查看标记、触发器和变量。

1. 要编辑变量中引用的&#x200B;**[!UICONTROL Google Analytics ID]**，请执行以下操作：

   - 导航到&#x200B;**[!UICONTROL Variables]** > **[!UICONTROL User-Defined Variables]**。

   - 选择&#x200B;**[!UICONTROL Google Analytics]**&#x200B;并使用您自己的&#x200B;**[!UICONTROL GA ID]**&#x200B;更新占位符(`UA-xxxxxx-x`)。

1. 按照Google的说明将标记、触发器和变量添加到新容器。

   如果您在其他要使用的容器中有设置，则可以将它们移动到新容器。

1. 完成后，单击&#x200B;**[!UICONTROL Confirm]**。

1. 按照Google的说明发布新容器。

## 步骤3. 配置您的商店

{{gtag-api-note}}

1. 登录到Commerce商店的管理员。

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧面板中，展开&#x200B;**[!UICONTROL Sales]**&#x200B;并选择&#x200B;**[!UICONTROL Google API]**。

1. 展开![扩展选择器](../assets/icon-display-expand.png) **[!UICONTROL Google Analytics]**&#x200B;部分并配置以下内容：

   ![销售配置 — Google Analytics](../configuration-reference/sales/assets/google-api-analytics-tag-manager.png){width="600" zoomable="yes"}

   - 将&#x200B;**[!UICONTROL Enable]**&#x200B;设置为`Yes`。

   - 将&#x200B;**[!UICONTROL Account type]**&#x200B;设置为`Google Tag Manager`。

   - 在&#x200B;**[!UICONTROL Container ID]**&#x200B;字段中，输入您的GTM ID (`GTM-xxxxxx`)。

   - 如果您还使用Google Analytics进行内容实验，请将&#x200B;**启用内容实验**&#x200B;设置为`Yes`。

   - 对其余字段使用默认值。

1. 完成后，单击&#x200B;**[!UICONTROL Save Config]**。

1. 测试您的[!DNL Google Tag Manager]设置并验证所有设置是否均可正常工作。

>[!NOTE]
>
>每个容器均与一个网站关联，每个帐户只需一个容器。 如果您有多站点Commerce实例，则需要单独的容器。

## 字段描述

| 字段 | 范围 | 描述 |
|--- |--- |--- |
| [!UICONTROL Enable] | 商店视图 | 确定是否可以使用Google Analytics Enhanced E-commerce分析商店中的活动。 选项： `Yes` / `No` |
| [!UICONTROL Account type] | 商店视图 | 确定用于监视商店活动和流量的Google跟踪代码。 选项： `Google Analytics` / `Google Tag Manager` |
| [!UICONTROL Anonymize IP] | 商店视图 | 确定是否从Google Analytics结果中显示的IP地址中删除标识信息。 |
| [!UICONTROL Enable Content Experiments] | 商店视图 | 激活Google内容实验，该实验可用于测试同一页面的最多十个不同版本。 选项： `Yes` / `No` |
| [!UICONTROL Container Id] | 商店视图 | 如果已为商店安装和配置了[!DNL Google Tag Manager]，则容器ID会自动显示在此字段中。 |
| [!UICONTROL List property for the catalog page] | 商店视图 | 标识与目录页面关联的Tag Manager属性。 默认值： `Catalog Page` |
| [!UICONTROL List property for the cross-sell block] | 商店视图 | 标识与交叉销售块关联的Tag Manager属性。 默认值： `Cross-sell` |
| [!UICONTROL List property for the up-sell block] | 商店视图 | 标识与向上销售块关联的Tag Manager属性。 默认值： `Up-sell` |
| [!UICONTROL List property for the related products block] | 商店视图 | 标识与相关产品块关联的Tag Manager属性。 默认值： `Related Products` |
| [!UICONTROL List property for the search results page] | 商店视图 | 标识与搜索结果页面关联的Tag Manager属性。 默认值： `Search Results` |
| [!UICONTROL "Internal Promotions" for promotions field "Label"] | 商店视图 | 标识与内部促销标签关联的Tag Manager属性。 默认值： `Label` |

{style="table-layout:auto"}

## 创建标记以跟踪转化

如果您拥有Google AdWords帐户，则可以创建跟踪转化的标记。 以下示例显示如何使用[!DNL Google Tag Manager]和[!DNL Google Analytics]创建在存储区转化&#x200B;_Success_&#x200B;页面上触发的标记。

### 步骤1. 创建标记

1. 登录到您的[!DNL Google Tag Manager]帐户，然后单击您为商店创建的容器的链接。

1. 在&#x200B;**[!UICONTROL New Tag]**&#x200B;框中，单击&#x200B;**[!UICONTROL Add a new tag]**。

1. 从您的AdWords帐户获取以下信息：

   - 转换ID
   - 转化标签

   如果需要帮助，请访问Google的[支持网站](https://support.google.com/tagmanager/answer/6105160)。

1. 在[!DNL Google Tag Manager]仪表板中，单击&#x200B;**[!UICONTROL Google AdWords]**&#x200B;并执行以下操作：

   - 单击标题占位符并输入新标记的名称。

   - 在&#x200B;**[!UICONTROL Choose Product]**&#x200B;下，选择&#x200B;**[!UICONTROL Google AdWords]**。

   - 在&#x200B;_[!UICONTROL Choose a Tag Type]_下，选择&#x200B;**[!UICONTROL AdWords Conversion Tracking]**并单击&#x200B;**[!UICONTROL Continue]**。

1. 输入你的AdWords帐户中的&#x200B;**[!UICONTROL Conversion ID]**&#x200B;和&#x200B;**[!UICONTROL Conversion Label]**，然后单击&#x200B;**[!UICONTROL Continue]**。

### 步骤2. 创建规则

从[!DNL Google Tag Manager]仪表板继续，下一步是创建在转化页面上触发标记的规则。

1. 在&#x200B;**[!UICONTROL Fire On]**&#x200B;下，单击&#x200B;**[!UICONTROL Some Pages]**。

1. 在&#x200B;_[!UICONTROL Choose Pages]_部分中，完成以下设置：

   - **[!UICONTROL Name]** — 输入页面描述的名称。

   - **[!UICONTROL Variable]** `url`

   - **操作** - `matches RegEx`

     若要了解更多信息，请参阅Google Tag Manager帮助中的[正则表达式和CSS选择器运算符](https://support.google.com/tagmanager/answer/7679109)。

   - **[!UICONTROL Value]** - `checkout/success.*`

1. 选中绿色复选框并单击&#x200B;**[!UICONTROL Save]**。

   您设置的触发器在“点击”部分显示为蓝色按钮。

1. 完成后，单击&#x200B;**[!UICONTROL Save Tag]**。

### 步骤3. 预览和发布

该过程的下一步是预览标记。 每次预览标记时，都会保存版本的快照。 如果对结果满意，请转到要使用的版本，然后单击&#x200B;**[!UICONTROL Publish]**。

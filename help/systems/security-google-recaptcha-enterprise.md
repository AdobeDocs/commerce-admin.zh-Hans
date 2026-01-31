---
title: Google reCAPTCHA Enterprise
description: 了解如何配置Google reCAPTCHA Enterprise以保护Adobe Commerce as a Cloud Service店面免受机器人和欺诈活动的侵害。
role: Admin
feature: Configuration, Security
badgeSaas: label="仅限SaaS" type="Positive" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="仅适用于Adobe Commerce as a Cloud Service项目(Adobe管理的SaaS基础架构)。"
source-git-commit: 3bc89a2dcecc91bbb4b3df285b6e1dd7c64bc477
workflow-type: tm+mt
source-wordcount: '570'
ht-degree: 0%

---

# Google reCAPTCHA Enterprise

[Google reCAPTCHA Enterprise](https://cloud.google.com/security/products/recaptcha#protect-against-fraud-and-abuse-with-modern-bot-protection-and-fraud-prevention-platform)通过使用自适应风险分析和机器学习区分人类用户和机器人，为Adobe Commerce as a Cloud Service店面提供高级机器人保护。 这有助于防止网站上的欺诈活动、垃圾邮件和滥用。

>[!NOTE]
>
>此功能不向管理员提供reCAPTCHA支持。

[reCAPTCHA集成](https://experienceleague.adobe.com/developer/commerce/storefront/dropins/user-auth/recaptcha/)介绍了如何在店面中添加对reCAPTCHA Enterprise的支持。

有关配置其他版本的Google reCAPTCHA的信息，请参阅[Google reCAPTCHA V3和V2](security-google-recaptcha.md)。

## 功能

Google reCAPTCHA Enterprise包含以下功能：

- **高级机器人检测**：使用Google Cloud的机器学习模型检测高级机器人
- **风险得分分析**：为每次交互提供详细的风险得分(0.0-1.0)
- **可配置的阈值**：为每个租户设置可接受的最低风险分数
- **多租户支持**：具有独立Google云项目的每个租户配置
- **加密凭据**：服务帐户凭据存储在数据库中
- **表单保护**：保护所有标准Commerce表单，包括登录、结帐、产品审核等。

## 先决条件

在为Google as a Cloud Service店面配置Adobe Commerce reCAPTCHA Enterprise之前，您需要以下资源：

- 启用了reCAPTCHA Enterprise的活动Google Cloud帐户。
- 访问Google Cloud Console以创建和管理reCAPTCHA企业密钥。

在多租户Adobe Commerce as a Cloud Service安装中，每个租户都必须拥有自己的Google Cloud项目和reCAPTCHA Enterprise密钥。

## 步骤1：设置Google reCAPTCHA Enterprise

按照以下常规步骤为您的店面设置Google reCAPTCHA Enterprise 。 有关详细说明，请参阅[Google reCAPTCHA企业版文档](https://docs.cloud.google.com/recaptcha/docs/overview)。

1. [为您的reCAPTCHA Enterprise实施创建一个Google Cloud项目](https://developers.google.com/workspace/guides/create-project)。

1. 启用[reCAPTCHA Enterprise API](https://docs.cloud.google.com/recaptcha/docs/prepare-environment)。

1. 创建基于得分的reCAPTCHA Enterprise [站点密钥](https://docs.cloud.google.com/recaptcha/docs/choose-key-type)。

1. 创建具有`roles/recaptchaenterprise.admin` IAM角色的服务帐户。

1. 下载服务帐户JSON密钥文件，该文件包含使用Google reCAPTCHA Enterprise验证Adobe Commerce as a Cloud Service店面所需的凭据。

## 步骤2：为店面配置Google reCAPTCHA

1. 在Adobe Commerce _管理员_&#x200B;侧边栏中，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 展开&#x200B;_[!UICONTROL Security]_&#x200B;并选择&#x200B;**[!UICONTROL Google reCAPTCHA Storefront]**。

1. 向下滚动到&#x200B;**[!UICONTROL reCAPTCHA Enterprise]**&#x200B;部分，并按照以下方式完成配置。

   - 对于&#x200B;**[!UICONTROL Site Key]**，请从Google Cloud Console复制并粘贴您的reCAPTCHA Enterprise站点密钥。

   - 对于&#x200B;**[!UICONTROL Google Cloud Project ID]**，请从Google Cloud项目中复制并粘贴项目ID。

   - 对于&#x200B;**[!UICONTROL Service Account JSON]**，复制您在[步骤1：设置Google reCAPTCHA Enterprise](#step-1-set-up-google-recaptcha-enterprise)中下载的服务帐户JSON密钥文件的内容。

   - 对于&#x200B;**[!UICONTROL Minimum Score Threshold]**，输入最小得分(0.0-1.0)以标识何时将用户交互标记为潜在风险。 1.0分是典型的用户交互，0.0分可能是机器人。

   - 对于&#x200B;**[!UICONTROL Badge Position]**，选择每个页面上不可见reCAPTCHA徽章的位置。 选项： `Inline` / `Bottom Right` / `Bottom Left`。

   - 对于&#x200B;**[!UICONTROL Theme]**，选择`Light Theme`（默认）或`Dark Theme`以确定Google reCAPTCHA框的样式。

   - 对于&#x200B;**[!UICONTROL Language Code]**，输入指定用于Google reCAPTCHA文本和消息传递的语言的[双字符代码](https://developers.google.com/recaptcha/docs/language)。

   - 对于&#x200B;**[!UICONTROL Validation Failure Message]**，可以选择在验证失败时更改店面中显示的消息。


1. 展开&#x200B;**[!UICONTROL Storefront]**&#x200B;部分并将要保护的每个店面表单设置为&#x200B;**[!UICONTROL reCAPTCHA Enterprise]**。

   {{recaptcha-forms-list}}

   ![店面选项配置](../configuration-reference/security/assets/recaptcha-storefront.png){width="600" zoomable="yes"}

## 步骤3：保存配置

1. 配置设置完成后，单击&#x200B;**[!UICONTROL Save Config]**。

1. 在工作区顶部的消息中，单击&#x200B;**[!UICONTROL Cache Management]**&#x200B;并刷新每个无效缓存。

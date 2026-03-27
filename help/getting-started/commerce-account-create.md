---
title: 创建并访问您的 [!DNL Commerce] 帐户
description: 了解 [!DNL Commerce] 帐户，这些帐户管理您购买的产品和服务。
badgePaas: label="仅限PaaS" type="Informative" url="https://experienceleague.adobe.com/zh-hans/docs/commerce/user-guides/product-solutions" tooltip="仅适用于云项目（Adobe管理的PaaS基础架构）和内部部署项目上的Adobe Commerce 。"
exl-id: 45f938c8-9bd9-4bd3-ac12-cce722a61e03
feature: User Account
source-git-commit: 96acaff3e614a5758fdc51bc5de70ce0507a970a
workflow-type: tm+mt
source-wordcount: '1010'
ht-degree: 0%

---


# 访问您的[!DNL Commerce]帐户

[!DNL Commerce]帐户是您的中心访问点，用于为部署在云基础架构或内部部署的Adobe Commerce项目管理Adobe Commerce服务。 在帐户仪表板中，您可以查看订阅、管理Commerce服务API密钥、查看历史帐单信息并与组织中的其他用户协作。

如果您需要[提交您的第一个票证](https://experienceleague.adobe.com/zh-hans/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide#support-case)或管理您的Adobe Commerce关系（而不是在特定店面中工作），请首先创建或访问您的[!DNL Commerce]帐户。

您可以从[!DNL Commerce]网站访问您的[!DNL Commerce]帐户。 从帐户信息板中，您可以查看与您购买的产品和服务相关的信息，并向其他用户提供[共享访问权限](https://experienceleague.adobe.com/zh-hans/docs/support-resources/adobe-support-tools-guide/adobe-commerce-support/adobe-commerce-help-center-user-guide#provide-shared-access)。 某些信息（如Commerce Services API密钥）仅对许可证所有者可见。

>[!NOTE]
>
>**[!UICONTROL Billing History]**&#x200B;帐户页上的[!DNL Commerce]部分仅显示帐单系统更新之前创建的发票。
>
>如果未列出较新的发票，则表明它们已转换为新系统，无法从此页面访问。

![您的[!DNL Commerce]帐户](./assets/home-acct.png){width="700"}

您的[!DNL Commerce]帐户登录名不同于商店管理员登录名。 您通常会对每个系统使用不同的凭据，并且每个系统的访问权限都受独立管理。

但是，想要简化Adobe Commerce和Adobe商业产品登录流程的用户可以将其Adobe ID配置为登录到应用商店管理员：[Commerce的IMS Integration Guide](https://experienceleague.adobe.com/zh-hans/docs/commerce-admin/start/admin/ims/adobe-ims-config)中的&#x200B;*Configure the Commerce Admin Integration with Adobe ID*。

>[!NOTE]
>
>创建帐户后，建议您使用双重身份验证(TFA)来[保护帐户的安全](commerce-account-secure.md)。

## 登录到您的[!DNL Commerce]帐户

需要Adobe ID才能访问您的[!DNL Commerce]帐户。 如果您已有[!DNL Commerce]帐户，但自2022年8月以来未登录，则必须在登录过程中创建Adobe ID。 您必须先完成此步骤，然后才能登录到您的帐户。

>[!WARNING]
>
>如果在提交Commerce [支持案例](https://experienceleague.adobe.com/zh-hans/docs/support-resources/adobe-support-tools-guide/adobe-commerce-support/adobe-commerce-help-center-user-guide#support-case)时找不到Adobe Commerce组织，则通常意味着出现以下情况之一：帐户所有者未创建Adobe ID，或者Adobe ID存在但未链接到Commerce帐户。

1. 转到[[!DNL Commerce]](https://account.magento.com/customer/account/login/)网站。

1. 单击&#x200B;**[!UICONTROL Sign in with Adobe ID]**。

   ![使用Adobe登录屏幕登录](./assets/sign-in-with-adobe.png){width="700"}

1. 输入您的电子邮件地址并单击&#x200B;**[!UICONTROL Continue]**。

   >[!TIP]
   >
   >如果您使用的电子邮件地址与现有Commerce帐户MAGEID关联，则登录过程会自动将其链接到您的Adobe ID。

## 创建[!DNL Commerce]帐户

任何人都可以创建免费的[!DNL Commerce]帐户。 您使用的电子邮件地址只能与一个Commerce帐户关联。

>[!NOTE]
>
>使用Adobe ID创建和访问Commerce帐户。
>- 如果您没有Commerce帐户，则可以在注册过程中创建一个。
>- 如果您已经拥有Commerce帐户，但是没有Adobe ID，请参阅[登录到Commerce帐户](#log-in-to-your-dnl-commerce-account)。

1. 转到[[!DNL Commerce] 站点](https://account.magento.com/customer/account/login/)。

1. 单击&#x200B;**[!UICONTROL Sign in with Adobe ID]**。

1. 如果您没有Adobe ID，请单击&#x200B;**[!UICONTROL Create an account]**。 否则，请跳至步骤7。

   ![创建帐户链接](./assets/account-create-link.png){width="700"}

1. 完成注册表单。

   ![帐户信息](./assets/account-create.png){width="700"}

1. 单击&#x200B;**[!UICONTROL Create account]**。

1. 输入发送到您电子邮件地址的验证码。

   ![输入验证码](./assets/verification-code.png){width="700"}

1. 创建并验证Adobe ID后，请返回https://account.magento.com/。 这将生成一个图像ID，并将其自动链接到您的Adobe ID。

## 重置密码

1. 转到[[!DNL Commerce] 站点](https://account.magento.com/customer/account/login/)。

1. 单击&#x200B;**[!UICONTROL Sign in with Adobe ID]**。

1. 单击&#x200B;**[!UICONTROL Get help signing in]**。

   ![获取登录帮助](./assets/sign-in-get-help.png){width="700"}

1. 单击&#x200B;**[!UICONTROL Reset your password]**。

   ![更改密码](./assets/change-password.png){width="700"}

1. 输入您的电子邮件地址。

1. 单击&#x200B;**[!UICONTROL Continue]**。

## 提供对您的Commerce帐户的共享访问权限

共享访问允许您授予受信任的用户（例如同事、合作伙伴或管理员）以自己的名义管理Adobe Commerce关系的权限，而无需使用个人登录。 这包括允许其他人打开和跟踪支持案例。

有关设置共享帐户的详细步骤，请参阅Adobe Commerce快速入门指南的[共享Commerce帐户](https://experienceleague.adobe.com/zh-hans/docs/commerce-admin/start/commerce-account/commerce-account-share?lang=en)部分。

有关提交Commerce支持案例的详细说明，请参阅[Adobe Commerce帮助中心用户指南](https://experienceleague.adobe.com/zh-hans/docs/support-resources/adobe-support-tools-guide/adobe-commerce-support/adobe-commerce-help-center-user-guide#support-case)。

## 摘要

| 方案 | 发生了什么 | 用Adobe ID做什么 | 如何处理图像ID/Commerce帐户 | 结果 |
| --- | --- | --- | --- | --- |
| 初次使用Adobe和Commerce | 无Adobe ID，无图像ID | 在登录https://account.magento.com期间出现提示时，创建Adobe ID | 创建Adobe ID后，再次登录到https://account.magento.com | 创建Commerce帐户，并生成图像ID并将其链接到Adobe ID |
| 具有Adobe ID，但尚未提供图像ID | 仅使用其他Adobe产品 | 在https://account.magento.com上使用Adobe ID登录 | 首次成功登录将创建Commerce帐户和图像ID | 会自动创建和链接图像ID |
| 具有旧图像ID的旧版Commerce客户 | 具有历史图像ID，但不具有Adobe ID | 在https://account.adobe.com上使用与现有图像ID相同的电子邮件创建一个Adobe ID | 使用“使用Adobe ID登录”登录到https://account.magento.com | 现有图像ID已链接到新的Adobe ID |
| Adobe ID和图像ID存在，但未关联 | Adobe ID和Commerce的电子邮件有所不同 | 使Adobe ID电子邮件与Commerce帐户电子邮件匹配（反之亦然，具体取决于所有权） | 在电子邮件匹配后，通过“使用Adobe ID登录”进行登录，网址为https://account.magento.com | Adobe ID将变为登录名；图像ID仍然是权利标识符 |
| 具有Adobe ID，但“没有图像ID” | 从未登录https://account.magento.com | 使用现有的Adobe ID | 首次登录https://account.magento.com | 首次登录会生成并链接图像ID |
| 仅使用云项目登录(accounts.magento.cloud) | 可以访问云项目，但无法访问经典Commerce帐户 | 继续使用Adobe ID for cloud项目 | 如果需要市场/许可证，请使用相同的Adobe ID登录https://account.magento.com | 创建并关联了一个经典Commerce帐户（具有图像ID） |

如果用户认为自己应拥有Commerce权限，但未看到图像ID，则默认的下一步是使用其Adobe ID登录https://account.magento.com ，以便能够创建或正确关联Commerce帐户和图像ID。

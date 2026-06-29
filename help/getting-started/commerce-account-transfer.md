---
title: 转移Adobe Commerce帐户
description: 了解如何将Adobe Commerce帐户转移给新所有者或电子邮件地址、选择正确的转移类型、验证电子邮件更改并与支持部门联系。
exl-id: f6528931-dbf1-4702-8989-232c27969c4a
feature: User Account
TQID: https://experienceleague.adobe.com/CIyzus4f8WcBH-jW9R1nCL-gkl065DLTHbjNn0K6e7E
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: e01cba363eb149286479718e660f8cdf6526e826
workflow-type: tm+mt
source-wordcount: 1553
ht-degree: 0%

---

# 转移Adobe Commerce帐户

随着业务职责变化，您可能需要将您的Adobe Commerce帐户转移给新所有者或其他电子邮件地址。 此转移需要更改与该帐户关联的主要用户电子邮件。

以下信息介绍了转移Adobe Commerce帐户(MAGEID)的过程。 它不包括对Adobe Commerce的云基础架构项目所有权或[!DNL New Relic]所有权的更改。 有关云项目访问权限的详细信息，请参阅《云基础架构上的Commerce指南》_中的[管理用户访问权限](https://experienceleague.adobe.com/zh-hans/docs/commerce-cloud-service/user-guide/project/user-access)_。

>[!IMPORTANT]
>
>如果新帐户所有者使用共享访问购买了扩展，则一旦帐户转移开始，对这些扩展的访问权限就会丢失。
>
>在请求帐户转移之前，请确保新所有者从[他们的 [!DNL Commerce Marketplace] 帐户](https://commercemarketplace.adobe.com/sales/order/history/)中检索购买的订单ID并请求[[!DNL Commerce Marketplace] 团队](https://experienceleague.adobe.com/zh-hans/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide#support-case)退款。 扩展购买不能转移到其他帐户。

## 识别您的传输类型

相应的Adobe Commerce帐户转移流程取决于当前所有者和新所有者的帐户状态，以及当前所有者的电子邮件地址是否仍可访问。 例如，如果当前所有者已离开公司，您仍可能需要访问发送到该地址的电子邮件。

以下方案基于这些条件描述了可用的传输选项。

| 传输类型 | 当前所有者 | 新所有者 |
| ------------- | ------------- | --------- |
| [新Adobe ID和电子邮件更改](#new-adobe-id-and-email-change) | 具有尚未连接到Adobe ID的MAGEID | 没有MAGEID，也没有Adobe ID。 |
| [仅电子邮件更改](#email-change) | 具有连接到Adobe ID的MAGEID。 | 具有Adobe ID，但没有与帐户关联的MAGEID。 |
| [Adobe ID帐户开关](#adobe-id-account-switch) | 具有连接到Adobe ID的MAGEID。 | 具有MAGEID并连接到Adobe ID。 |

{style="table-layout:auto"}

>[!NOTE]
>
>由于Adobe Commerce继续与其他Adobe解决方案集成，因此Adobe Commerce帐户(MAGEID)现在需要与Adobe ID关联。 Adobe ID使用连接到您的[Adobe Commerce帐户](https://experienceleague.adobe.com/zh-hans/docs/commerce-admin/start/commerce-account/commerce-account-create?lang=en#create-a-commerce-account)的相同电子邮件地址。

## 验证Adobe ID电子邮件更改

多个传输路径在[account.adobe.com](https://account.adobe.com/)上使用相同的验证工作流。 输入目标电子邮件地址并单击&#x200B;**[!UICONTROL Change]**&#x200B;后，请完成以下步骤：

1. 打开发送到您输入的地址的验证电子邮件，然后找到确认代码。

1. 输入确认代码。

1. 单击&#x200B;**[!UICONTROL Verify]**。

## 新的Adobe ID和电子邮件更改

>[!IMPORTANT]
>
>查看[传输类型](#identify-your-transfer-type)，并确认此路径与您的情况匹配：
>
>- 当前所有者仍在公司中。
>- 当前所有者没有Adobe ID，或者其Adobe ID未连接到其[Adobe Commerce帐户(MAGEID)](https://experienceleague.adobe.com/zh-hans/docs/commerce-admin/start/commerce-account/commerce-account-create?lang=en#create-a-commerce-account)。
>- 新所有者没有Adobe ID，也没有Adobe Commerce帐户。

如果当前所有者的MAGEID尚未链接到Adobe ID，请使用此路径。 当前所有者首先创建并链接Adobe ID，然后将Adobe ID电子邮件地址更改为新所有者的电子邮件地址。

1. 转到[Adobe Commerce帐户登录](https://account.magento.com/customer/account/login/)页面。

1. 单击&#x200B;**[!UICONTROL Sign in with Adobe ID]**。

1. 单击&#x200B;**[!UICONTROL Create an account]**。

1. 输入当前所有者的电子邮件地址和密码。

1. 单击&#x200B;**[!UICONTROL Continue]**。

   此步骤将创建一个Adobe ID并将其链接到当前的Adobe Commerce帐户(MAGEID)。 通过此帐户链接，_[!UICONTROL Email]_&#x200B;字段被阻止进行任何更改。 相关电子邮件地址的配置可通过Adobe ID帐户进行管理。

1. 导航到[account.adobe.com](https://account.adobe.com/)。

1. 单击&#x200B;**[!UICONTROL Change Email]**。

1. 输入新所有者的电子邮件地址。

   如果新的电子邮件地址已链接到系统中的另一个帐户，则无法直接用于传输。 请改为遵循[Adobe ID帐户开关](#adobe-id-account-switch)路径并使用[临时电子邮件地址](#change-to-a-temporary-account)。

1. 完成[电子邮件验证步骤](#verify-an-adobe-id-email-change)。

新所有者验证电子邮件地址后，请继续[最后步骤](#final-steps)，以便Adobe Commerce支持可以更新帐户记录，如[[!DNL Commerce Marketplace]](https://commercemarketplace.adobe.com/)配置文件。

>[!VIDEO](https://video.tv.adobe.com/v/3447669/?captions=chi_hans&learn=on){transcript=true}

## 仅电子邮件更改 {#email-change}

>[!IMPORTANT]
>
>查看[传输类型](#identify-your-transfer-type)，并确认此路径与您的情况匹配：
>
>- 当前所有者仍在公司中。
>- 当前所有者有一个连接到其[Adobe Commerce帐户(MAGEID)](https://experienceleague.adobe.com/zh-hans/docs/commerce-admin/start/commerce-account/commerce-account-create?lang=en#create-a-commerce-account)的Adobe ID。
>- 新所有者拥有的Adobe ID未连接到Adobe Commerce帐户。

在开始之前，请注意，此转移类型会导致当前帐户所有者无法访问与该Adobe ID关联的其他Adobe产品。

1. 导航到[account.adobe.com](https://account.adobe.com/)并完成Adobe登录。

1. 在您的帐户名称和头像下，单击&#x200B;**[!UICONTROL Change Email]**。

1. 在对话框中，输入新所有者的电子邮件地址。

   如果新的电子邮件地址已链接到系统中的另一个帐户，则无法直接用于传输。 请改为遵循[Adobe ID帐户开关](#adobe-id-account-switch)路径并使用[临时电子邮件地址](#change-to-a-temporary-account)。

1. 完成[电子邮件验证步骤](#verify-an-adobe-id-email-change)。

新所有者验证电子邮件地址后，请继续[最后步骤](#final-steps)，以便Adobe Commerce支持可以更新帐户记录，如[[!DNL Commerce Marketplace]](https://commercemarketplace.adobe.com/)配置文件。

## Adobe ID帐户切换

>[!IMPORTANT]
>
>查看[传输类型](#identify-your-transfer-type)，并确认此路径与您的情况匹配：
>
>- 当前所有者已离开公司，但发送到当前所有者的公司电子邮件地址的电子邮件仍可访问，或者您的IT团队可以将这些电子邮件转发给授权联系人。
>- 当前所有者有一个连接到其[Adobe Commerce帐户(MAGEID)](https://experienceleague.adobe.com/zh-hans/docs/commerce-admin/start/commerce-account/commerce-account-create?lang=en#create-a-commerce-account)的Adobe ID。
>- 新所有者有一个连接到其Adobe Commerce帐户的Adobe ID。

如果当前所有者和新所有者均拥有现有的Adobe ID，并且您想要保留这两个Adobe ID，则此转移类型会使用临时电子邮件地址来切换帐户所有权。 要完成所有权转让，必须使用与Adobe ID无关联的临时电子邮件地址。

### 更改为临时帐户

完成这些步骤可将当前所有者的Adobe ID与临时电子邮件地址相关联。 您必须有权访问该电子邮件地址，以便检索确认代码。

>[!NOTE]
>
>如果您无法访问当前所有者的电子邮件，请让您的IT团队为您公司电子邮件系统中的帐户电子邮件地址设置电子邮件转发。 如果无法配置电子邮件转发，请确保新帐户所有者具有Adobe ID，然后[提交支持请求](https://experienceleague.adobe.com/zh-hans/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide#support-case)以及启动帐户转移所需的所有详细信息。

1. 导航到[account.adobe.com](https://account.adobe.com/)并完成Adobe登录。

1. 在您的帐户名称和头像下，单击&#x200B;**[!UICONTROL Change Email]**。

1. 在对话框中，输入Adobe ID未使用的有效临时电子邮件地址。

1. 完成[电子邮件验证步骤](#verify-an-adobe-id-email-change)。

1. 注销Adobe帐户。

### 新所有者步骤

在当前所有者完成向临时电子邮件地址的转移后，新所有者必须完成这些步骤，将其Adobe ID电子邮件地址更改为当前所有者的原始电子邮件地址。

1. 导航到[account.adobe.com](https://account.adobe.com/)并完成Adobe登录。

1. 在您的帐户名称和头像下，单击&#x200B;**[!UICONTROL Change Email]**。

1. 在对话框中，输入当前所有者的原始电子邮件地址。

1. 完成[电子邮件验证步骤](#verify-an-adobe-id-email-change)。

1. 注销Adobe帐户。

### 后续步骤

新所有者使用当前所有者的原始电子邮件地址成功配置其Adobe ID后，请完成这些步骤以将该电子邮件地址分配给新所有者。

1. 导航到[account.adobe.com](https://account.adobe.com/)，并使用[临时帐户](#change-to-a-temporary-account)的电子邮件地址完成Adobe登录。

1. 在帐户名称和头像下，单击&#x200B;**[!UICONTROL Change Email]**。

1. 在对话框中，输入新所有者的电子邮件地址。

1. 完成[电子邮件验证步骤](#verify-an-adobe-id-email-change)。

新所有者验证电子邮件地址后，请继续[最后步骤](#final-steps)，以便Adobe Commerce支持可以更新帐户记录，如[[!DNL Commerce Marketplace]](https://commercemarketplace.adobe.com/)配置文件。

## 最后步骤

在完成[新Adobe ID和电子邮件更改](#new-adobe-id-and-email-change)、[仅电子邮件更改](#email-change)或[Adobe ID帐户切换](#adobe-id-account-switch)流程后，完成这些步骤。

1. 作为新所有者，[提交支持请求](https://experienceleague.adobe.com/zh-hans/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide?lang=en#support-case)。

   包括以下详细信息：

   - 上一个帐户所有者的电子邮件地址
   - 新所有者的电子邮件地址
   - 请注意，您已完成Adobe Commerce帐户转移并更新了Adobe ID电子邮件地址

1. 等待Adobe Commerce支持以确认更新。

   支持人员还会更新相关记录，如您[[!DNL Commerce Marketplace]](https://commercemarketplace.adobe.com/)个人资料上的电子邮件地址。

支持人员完成请求后，新所有者可以使用其Adobe ID登录到Adobe Commerce帐户。 MAGEID仍然是帐户的权利标识符。

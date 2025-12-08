---
title: 转移Commerce帐户
description: 了解如何将您的Commerce帐户转移给其他所有者或电子邮件地址。
exl-id: f6528931-dbf1-4702-8989-232c27969c4a
feature: User Account
source-git-commit: a7b23834b00b2ae0f5fd98de47fdc6f4aa00c010
workflow-type: tm+mt
source-wordcount: '1196'
ht-degree: 0%

---

# 转移Commerce帐户

随着业务职责变化，您可能需要将您的Commerce帐户转移给新所有者或其他电子邮件地址。 此转移需要更改与该帐户关联的主要用户电子邮件。

以下信息介绍了转移Commerce (MAGEID)帐户的流程。 它不包括对Cloud帐户(Cloud项目或New Relic)所有权的更改。 有关云项目访问权限的详细信息，请参阅《云基础架构上的Commerce指南》[中的](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/user-access.html?lang=zh-Hans)管理用户访问权限&#x200B;__。

>[!IMPORTANT]
>
>如果新帐户所有者使用共享访问购买了扩展，则一旦启动帐户转移流程，对这些扩展的访问权限就会丢失。 在请求帐户转移之前，请确保新所有者从[其Marketplace帐户](https://commercemarketplace.adobe.com/sales/order/history/)中检索购买的订单ID，并向[Marketplace团队](https://experienceleague.adobe.com/zh-hans/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide#support-case)申请这些扩展的退款。 无法将延期购买转移到其他帐户。

## 识别您的传输类型

Commerce帐户转移的类型取决于当前所有者和新所有者可用的Commerce帐户凭据。 以下方案基于这些凭据描述了不同的传输类型。

| 传输类型 | 当前所有者 | 新所有者 |
| ------------- | ------------- | --------- |
| [新Adobe ID和电子邮件更改](#new-adobe-id-and-email-change) | 具有&#x200B;**_尚未连接到Adobe登录帐户的MAGEID_** | 没有MAGEID，并且未连接到Adobe登录帐户。 |
| [电子邮件更改](#email-change) | 具有&#x200B;**_已连接_**&#x200B;且具有Adobe登录帐户的MAGEID。 | 具有Adobe登录帐户，但&#x200B;**_没有连接到Adobe登录帐户的MAGEID_**。 |
| [Adobe ID帐户开关](#adobe-id-account-switch) | MAGEID是&#x200B;**_连接到_** Adobe登录帐户的。 | 具有MAGEID并已连接到Adobe登录帐户。 |

{style="table-layout:auto"}

>[!NOTE]
>
>由于Adobe Commerce继续与其他Adobe解决方案集成，因此Commerce帐户(MAGEID)现在需要与Adobe登录关联。 此Adobe ID使用连接到您的Commerce帐户的相同电子邮件地址。

## 新的Adobe ID和电子邮件更改

>[!IMPORTANT]
>
>查看[传输类型](#identify-your-transfer-type)，并确保您满足此步骤序列的前提条件。

此转移类型要求具有与现有Commerce帐户关联的Adobe ID，然后将该帐户更改为新所有者的电子邮件地址。

1. 转到[Commerce帐户登录](https://account.magento.com/customer/account/login/)页面。

1. 单击&#x200B;**[!UICONTROL Sign in with Adobe ID]**。

1. 单击&#x200B;**[!UICONTROL Create an account]**。

1. 输入当前所有者的电子邮件地址和密码。

1. 单击&#x200B;**[!UICONTROL Continue]**。

   此步骤将创建一个Adobe ID并将其链接到当前的Commerce帐户(MAGEID)。 通过此帐户链接，_[!UICONTROL Email]_&#x200B;字段被阻止进行任何更改。 相关电子邮件地址的配置可通过Adobe ID帐户进行管理。

1. 导航到[account.adobe.com](https://account.adobe.com/)。

1. 单击&#x200B;**[!UICONTROL Change Email]**。

1. 输入新所有者的电子邮件地址。

   如果新的电子邮件地址已链接到系统中的另一个帐户，则无法直接用于传输。 相反，该进程需要使用[临时电子邮件地址](#change-to-a-temporary-account)来促进更改。

1. 单击&#x200B;**[!UICONTROL Change]**。

   此步骤会生成一封验证电子邮件，该电子邮件会发送到新的电子邮件地址。 该电子邮件包含完成电子邮件地址更改所需的确认代码。

1. 输入发送到新电子邮件地址的确认代码。

1. 单击&#x200B;**[!UICONTROL Verify]**。

>[!VIDEO](https://video.tv.adobe.com/v/3447669/?captions=chi_hans&learn=on)

## 电子邮件更改

>[!IMPORTANT]
>
>查看[传输类型](#identify-your-transfer-type)，并确保您满足此步骤序列的前提条件。

此转移类型会导致当前帐户所有者失去对其他Adobe产品的访问权限。

1. 导航到[account.adobe.com](https://account.adobe.com/)并完成Adobe登录。

1. 在您的帐户名称和头像下，单击&#x200B;**[!UICONTROL Change Email]**。

1. 在对话框中，输入新所有者的电子邮件地址。

   如果新的电子邮件地址已链接到系统中的另一个帐户，则无法直接用于传输。 相反，该进程需要使用[临时电子邮件地址](#change-to-a-temporary-account)来促进更改。

1. 单击&#x200B;**[!UICONTROL Change]**。

   此步骤会生成一封验证电子邮件，该电子邮件会发送到新的电子邮件地址。 该电子邮件包含完成电子邮件地址更改所需的确认代码。

1. 输入发送到新电子邮件地址的确认代码。

1. 单击&#x200B;**[!UICONTROL Verify]**。

## Adobe ID帐户切换

>[!IMPORTANT]
>
>查看[传输类型](#identify-your-transfer-type)，并确保您满足此步骤序列的前提条件。

如果当前所有者和新所有者均具有现有Adobe ID，并且您想要保留这两个帐户，则此转移类型使用临时电子邮件地址来切换帐户所有权。 要完成所有权转让，必须使用与Adobe ID无关联的临时电子邮件地址。

### 更改为临时帐户

当前所有者完成这些步骤，将其Adobe ID与另一个临时电子邮件地址相关联。

1. 导航到[account.adobe.com](https://account.adobe.com/)并完成Adobe登录。

1. 在您的帐户名称和头像下，单击&#x200B;**[!UICONTROL Change Email]**。

1. 在对话框中，输入Adobe ID未使用的有效临时电子邮件地址。

>[!NOTE]
>
>您必须具有电子邮件地址的访问权限，才能检索包含确认代码的电子邮件。
>
>如果您无法访问帐户电子邮件，请要求IT团队在您的公司电子邮件系统中为帐户电子邮件地址设置电子邮件转发。 如果无法配置电子邮件转发，请确保新帐户所有者具有Adobe ID，然后[提交支持请求](https://experienceleague.adobe.com/zh-hans/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide#support-case)以及启动帐户转移所需的所有详细信息。

1. 单击&#x200B;**[!UICONTROL Change]**。

   此步骤会生成验证电子邮件，该电子邮件会发送到临时电子邮件地址。 该电子邮件包含完成电子邮件地址更改所需的确认代码。

1. 输入发送到临时电子邮件地址的确认代码。

1. 单击&#x200B;**[!UICONTROL Verify]**。

1. 注销Adobe帐户。

### 新所有者步骤

在当前所有者完成向临时电子邮件地址的转移后，新所有者必须完成这些步骤以将其帐户配置更改为指向当前所有者的原始电子邮件地址。

1. 导航到[account.adobe.com](https://account.adobe.com/)并完成Adobe登录。

1. 在您的帐户名称和头像下，单击&#x200B;**[!UICONTROL Change Email]**。

1. 在对话框中，输入当前所有者的原始电子邮件地址。

1. 单击&#x200B;**[!UICONTROL Change]**。

   此步骤会生成一封验证电子邮件，发送到当前所有者的原始电子邮件地址。 该电子邮件包含完成电子邮件地址更改所需的确认代码。

1. 输入发送到当前所有者原始电子邮件地址的确认代码。

1. 单击&#x200B;**[!UICONTROL Verify]**。

1. 注销Adobe帐户。

### 后续步骤

新所有者使用当前所有者的原始电子邮件地址成功配置其Adobe帐户后，请完成这些步骤以转移所有权。

1. 导航到[account.adobe.com](https://account.adobe.com/)，并使用[临时帐户](#change-to-a-temporary-account)的电子邮件地址完成Adobe登录。

1. 在帐户名称和头像下，单击&#x200B;**[!UICONTROL Change Email]**。

1. 在对话框中，输入新所有者的电子邮件地址。

1. 单击&#x200B;**[!UICONTROL Change]**。

   此步骤会生成一封验证电子邮件，发送到新所有者的电子邮件地址。 该电子邮件包含完成电子邮件地址更改所需的确认代码。

1. 输入发送到新所有者电子邮件地址的确认代码。

1. 单击&#x200B;**[!UICONTROL Verify]**。

## 最后步骤

新所有者完成第一个或第三个用例中的步骤后，新所有者必须[提交支持请求](https://experienceleague.adobe.com/zh-hans/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide?lang=en#support-case)以通知支持团队电子邮件地址更新。 然后，支持团队完成其他任务，例如更新[Commerce Marketplace](https://commercemarketplace.adobe.com/)配置文件中的电子邮件地址。 在请求中包含前一个帐户所有者的电子邮件地址。
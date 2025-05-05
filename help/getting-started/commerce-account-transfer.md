---
title: 转移Commerce帐户
description: 了解如何将您的Commerce帐户转移给其他所有者或电子邮件地址。
exl-id: f6528931-dbf1-4702-8989-232c27969c4a
feature: User Account
source-git-commit: 9daf227e52c8f225e957ee5009d0d0a02815d835
workflow-type: tm+mt
source-wordcount: '1020'
ht-degree: 0%

---

# 转移Commerce帐户

随着业务职责的变更，您可能需要将现有Commerce帐户的所有权转移给新所有者或其他电子邮件地址。 此转移需要更改与该帐户关联的主要用户电子邮件。

以下信息介绍了转移Commerce (MAGEID)帐户的流程。 它不包括对Cloud帐户(Cloud项目或New Relic)所有权的更改。 有关云项目访问权限的详细信息，请参阅《云基础架构上的Commerce指南》_中的[管理用户访问权限](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/user-access.html)_。

>[!IMPORTANT]
>
>如果新的帐户所有者最初使用共享访问购买了扩展，则一旦启动帐户转移流程，对这些扩展的访问权限就会丢失。 在请求帐户转移之前，请确保新所有者从[其Marketplace帐户](https://commercemarketplace.adobe.com/sales/order/history/)中检索购买的订单ID，并向[Marketplace团队](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide#support-case)申请这些扩展的退款。 无法将延期购买转移到其他帐户。

## 识别您的传输类型

完成此转移的方式取决于以下哪些情况描述了您作为帐户的当前所有者和要向其转移帐户的新所有者（电子邮件地址）的情况：

| 传输类型 | 当前所有者 | 新所有者 |
| ------------- | ------------- | --------- |
| [新Adobe ID和电子邮件更改](#new-adobe-id-and-email-change) | MAGEID为&#x200B;**_未与Adobe登录帐户连接_**。 | 没有MAGEID，并且未连接到Adobe登录帐户。 |
| [电子邮件更改](#email-change) | 具有&#x200B;**_已连接_**&#x200B;且具有Adobe登录帐户的MAGEID。 | 没有MAGEID，并且未连接到Adobe登录帐户。 |
| [Adobe ID开关](#adobe-id-account-switch) | 具有&#x200B;**_已连接_**&#x200B;且具有Adobe登录帐户的MAGEID。 | 具有MAGEID，并且已连接到Adobe登录帐户，而没有关联的其他Adobe产品/服务。 |

{style="table-layout:auto"}

>[!NOTE]
>
>由于Adobe Commerce继续与其他Adobe解决方案集成，因此Commerce帐户(MAGEID)现在需要与Adobe登录关联。 此Adobe ID使用连接到您的Commerce帐户的相同电子邮件地址。

## 新的Adobe ID和电子邮件更改

>[!IMPORTANT]
>
>查看[传输类型](#identify-your-transfer-type)，并确保您满足此步骤序列的前提条件。

此转接类型要求您首先创建一个关联的Adobe ID，然后将该帐户更改为新所有者的电子邮件地址。

1. 转到您的[Commerce帐户](https://account.magento.com/customer/account/login/)。

1. 单击&#x200B;**[!UICONTROL Sign in with Adobe ID]**。

1. 单击&#x200B;**[!UICONTROL Create an account]**。

1. 输入当前所有者的电子邮件地址和密码。

1. 单击&#x200B;**[!UICONTROL Continue]**。

   这会创建一个Adobe ID并将其链接到当前的Commerce帐户(MAGEID)。 通过此帐户链接，_[!UICONTROL Email]_&#x200B;字段被阻止进行任何更改。 关联的电子邮件地址由Adobe ID帐户管理。

1. 导航到[account.adobe.com](https://account.adobe.com/)。

1. 单击&#x200B;**[!UICONTROL Change Email]**。

1. 输入新所有者的电子邮件地址。

1. 单击&#x200B;**[!UICONTROL Change]**。

   这将生成验证电子邮件，该电子邮件将发送到新的电子邮件地址。 该电子邮件包含完成电子邮件地址更改所需的确认代码。

1. 输入发送到新电子邮件地址的确认代码。

1. 单击&#x200B;**[!UICONTROL Verify]**。

>[!VIDEO](https://video.tv.adobe.com/v/3435325/?learn=on)

## 电子邮件更改

>[!IMPORTANT]
>
>查看[传输类型](#identify-your-transfer-type)，并确保您满足此步骤序列的前提条件。

1. 导航到[account.adobe.com](https://account.adobe.com/)并完成Adobe登录。

1. 在您的帐户名称和头像下，单击&#x200B;**[!UICONTROL Change Email]**。

1. 在对话框中，输入新所有者的电子邮件地址。

1. 单击&#x200B;**[!UICONTROL Change]**。

   这将生成验证电子邮件，该电子邮件将发送到新的电子邮件地址。 该电子邮件包含完成电子邮件地址更改所需的确认代码。

1. 输入发送到新电子邮件地址的确认代码。

1. 单击&#x200B;**[!UICONTROL Verify]**。

## Adobe ID帐户切换

>[!IMPORTANT]
>
>查看[传输类型](#identify-your-transfer-type)，并确保您满足此步骤序列的前提条件。

如果当前所有者和新所有者拥有现有的Adobe ID，则两个帐户都应保留，但电子邮件地址需要在它们之间切换。 这需要使用有效的&#x200B;_临时_&#x200B;电子邮件地址，该地址与和Adobe ID无关联。

### 更改为临时帐户

当前所有者完成这些步骤，将其Adobe ID与另一个临时电子邮件地址相关联。

1. 导航到[account.adobe.com](https://account.adobe.com/)并完成Adobe登录。

1. 在您的帐户名称和头像下，单击&#x200B;**[!UICONTROL Change Email]**。

1. 在对话框中，输入Adobe ID未使用的有效临时电子邮件地址。

   您必须具有电子邮件地址的访问权限，才能检索包含确认代码的电子邮件。

1. 单击&#x200B;**[!UICONTROL Change]**。

   这将生成验证电子邮件，该电子邮件将发送到临时电子邮件地址。 该电子邮件包含完成电子邮件地址更改所需的确认代码。

1. 输入发送到临时电子邮件地址的确认代码。

1. 单击&#x200B;**[!UICONTROL Verify]**。

1. 注销Adobe帐户。

### 新所有者步骤

在当前所有者完成向临时电子邮件地址的转移后，请完成这些步骤以将您的帐户更改为当前所有者。

1. 导航到[account.adobe.com](https://account.adobe.com/)并完成Adobe登录。

1. 在您的帐户名称和头像下，单击&#x200B;**[!UICONTROL Change Email]**。

1. 在对话框中，输入当前所有者的原始电子邮件地址。

1. 单击&#x200B;**[!UICONTROL Change]**。

   这将生成一封发送到该电子邮件地址的验证电子邮件。 该电子邮件包含完成电子邮件地址更改所需的确认代码。

1. 输入发送给当前所有者的确认代码。

1. 单击&#x200B;**[!UICONTROL Verify]**。

1. 注销Adobe帐户。

### 后续步骤

新所有者成功将其Adobe帐户转移给当前（现在是以前的）所有者后，请完成这些步骤以转移所有权。

1. 导航到[account.adobe.com](https://account.adobe.com/) （一系列步骤中使用的第一个帐户）并完成Adobe登录。

   此登录需要使用临时电子邮件地址。

1. 在帐户名称和头像下，单击&#x200B;**[!UICONTROL Change Email]**。

1. 在对话框中，输入新所有者的电子邮件地址。

1. 单击&#x200B;**[!UICONTROL Change]**。

   这将生成一封发送到该电子邮件地址的验证电子邮件。 该电子邮件包含完成电子邮件地址更改所需的确认代码。

1. 输入发送给新所有者的确认代码。

1. 单击&#x200B;**[!UICONTROL Verify]**。

>[!IMPORTANT]
>
>提交支持请求，通知支持团队您已更新帐户所有者的电子邮件地址。 团队必须执行其他步骤以完成更新，例如更新[Commerce Marketplace](https://commercemarketplace.adobe.com/)配置文件上的电子邮件地址。 在您的请求中包含以前帐户所有者的电子邮件地址。

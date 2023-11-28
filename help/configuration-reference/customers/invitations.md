---
title: ’[!UICONTROL Customers] &gt； [!UICONTROL Invitations]’
description: 查看 [!UICONTROL Customers] &gt； [!UICONTROL Invitations] 商务管理员页面。
exl-id: edafeaed-9c4f-4d9f-b35c-381ae5f43b67
feature: Configuration, Promotions/Events
source-git-commit: 76bd1b1af9b55d69bd98209d70fb5518f190a3e1
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 1%

---

# [!UICONTROL Customers] > [!UICONTROL Invitations]

{{ee-feature}}

{{config}}

## [!UICONTROL General]

![常规](./assets/invitations-general.png)<!-- zoom -->

<!-- [General](https://docs.magento.com/user-guide/marketing/invitations-configure.html) -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Enable Invitations Functionality] | 全局 | 确定是否启用邀请模块。 选项： `Yes` / `No` |
| [!UICONTROL Enable Invitations on Frontend] | 网站 | 确定能否从店面管理邀请。 选项： `Yes` / `No` |
| [!UICONTROL Referred Customer Group] | 商店视图 | 确定被邀请人的客户组。 选项： <br/>**`Same as Inviter`**— 被邀请者将自动分配到邀请他们的客户的同一客户组。<br/>**`Default Customer Group from Configuration`**  — 被邀请者自动拥有默认值 [客户组](../../customers/customer-groups.md). |
| [!UICONTROL New Accounts Registration] | 商店视图 | 确定受邀者如何创建帐户。 选项： <br/>**`By Invitation Only`**— 受邀者必须按照邀请电子邮件中的链接创建帐户。<br/>**`Available to All`**  — 受邀者可以使用商店中提供的帐户注册表。 |
| [!UICONTROL Allow Customers to Add Custom Message to Invitation Email] | 商店视图 | 确定邀请表单中是否存在字段，邀请者可以在其中添加通过电子邮件发送给被邀请者的自定义消息。 这不会影响管理员向邀请添加消息的能力。 选项： `Yes` / `No`. |
| [!UICONTROL Max Invitations Allowed to be Sent at One Time] | 商店视图 | 确定邀请者一次可发送的最大邀请数。 向邀请者在表单中包含的每个电子邮件地址发送不同的邀请。 这样可以防止同时发送大量邀请，从而保护服务器资源，并降低将邀请作为垃圾邮件发送的可能性。 |

{：style=&quot;table-layout：auto&quot;}

## [!UICONTROL Email]

![电子邮件](./assets/invitations-email.png)<!-- zoom -->

<!-- [Email](https://docs.magento.com/user-guide/marketing/invitations-configure.html) -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Customer Invitation Email Sender] | 商店视图 | 确定在发送邀请电子邮件时受邀者所收到电子邮件的发件人。 默认值： `General Contact` |
| [!UICONTROL Customer Invitation Email Template] | 商店视图 | 确定在发送邀请电子邮件时受邀者所收到电子邮件的模板。 默认模板： `Customer Invitation` |

{：style=&quot;table-layout：auto&quot;}

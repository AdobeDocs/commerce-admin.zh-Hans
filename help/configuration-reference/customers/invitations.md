---
title: '[!UICONTROL Customers] > [!UICONTROL Invitations]'
description: 查看Commerce管理员的[!UICONTROL Customers] &gt； [!UICONTROL Invitations]页面上的配置设置。
exl-id: edafeaed-9c4f-4d9f-b35c-381ae5f43b67
feature: Configuration, Promotions/Events
TQID: https://experienceleague.adobe.com/UOJF8r7CsXWK6qG7FjkJoJTIqnH2fPQhnRyZrJ7u4nE
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 250
ht-degree: 1%

---

# [!UICONTROL Customers] > [!UICONTROL Invitations]

{{ee-feature}}

{{config}}

## [!UICONTROL General]

![常规](./assets/invitations-general.png)<!-- zoom -->

<!-- [General](https://experienceleague.adobe.com/zh-hans/docs/commerce-admin/marketing/promotions/events/invitations#enable-invitations-for-your-store) -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Enable Invitations Functionality] | 全局 | 确定是否启用邀请模块。 选项： `Yes` / `No` |
| [!UICONTROL Enable Invitations on Frontend] | 网站 | 确定能否从店面管理邀请。 选项： `Yes` / `No` |
| [!UICONTROL Referred Customer Group] | 商店视图 | 确定被邀请人的客户组。 选项： <br/>**`Same as Inviter`**— 受邀者自动分配到邀请他们的客户所在的客户组。<br/>**`Default Customer Group from Configuration`** — 受邀者自动拥有默认的[客户组](../../customers/customer-groups.md)。 |
| [!UICONTROL New Accounts Registration] | 商店视图 | 确定受邀者如何创建帐户。 选项： <br/>**`By Invitation Only`**— 受邀者必须按照邀请电子邮件中的链接创建帐户。<br/>**`Available to All`** — 受邀者可以使用商店中提供的帐户注册表。 |
| [!UICONTROL Allow Customers to Add Custom Message to Invitation Email] | 商店视图 | 确定邀请表单中是否存在字段，邀请者可以在其中添加通过电子邮件发送给被邀请者的自定义消息。 这不会影响管理员向邀请添加消息的能力。 选项： `Yes` / `No`。 |
| [!UICONTROL Max Invitations Allowed to be Sent at One Time] | 商店视图 | 确定邀请者一次可发送的最大邀请数。 向邀请者在表单中包含的每个电子邮件地址发送不同的邀请。 这样可以防止同时发送大量邀请，从而保护服务器资源，并降低将邀请作为垃圾邮件发送的可能性。 |

{style="table-layout:auto"}

## [!UICONTROL Email]

![电子邮件](./assets/invitations-email.png)<!-- zoom -->

<!-- [Email](https://experienceleague.adobe.com/zh-hans/docs/commerce-admin/marketing/promotions/events/invitations#enable-invitations-for-your-store) -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Customer Invitation Email Sender] | 商店视图 | 确定在发送邀请电子邮件时受邀者所收到电子邮件的发件人。 默认值： `General Contact` |
| [!UICONTROL Customer Invitation Email Template] | 商店视图 | 确定在发送邀请电子邮件时受邀者所收到电子邮件的模板。 默认模板： `Customer Invitation` |

{style="table-layout:auto"}

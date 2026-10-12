---
title: 批准公司帐户
description: 了解如何在管理员中批准公司帐户请求。
exl-id: c7123383-0e94-4d6c-be3c-b6ca84145a59
feature: B2B, Companies, Configuration
role: Admin, User
TQID: 'https://experienceleague.adobe.com/ZpDdYMYaSnG1lOwV22mmrkYjBvf90pUJVZxP2r526pw'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
    internal-label: Storefront
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: e9004f3c-09ae-5d24-acd2-fa0987fdb66e
    internal-label: Companies
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
    internal-label: Accounts
subfeature_v2:
  - id: f56d26ed-050b-4fb7-b29b-8e6e994e80a2
    internal-label: B2B
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: acc7571574eb9c7e96911266897350a77913488e
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 0%
---
# 批准公司帐户

从店面收到的创建公司的请求的状态为`Pending Approval`，直到该请求被店面管理员审核并批准或拒绝。 公司帐户的状态可以设置为以下任意状态：

- [!UICONTROL Active]
- [!UICONTROL Pending Approval]
- [!UICONTROL Rejected]
- [!UICONTROL Blocked]

您还可以使用[Actions控件](account-company-manage.md)来批准多个公司请求。

![未决批准](./assets/companies-pending-approval.png){width="700" zoomable="yes"}

## 批准待处理公司帐户

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Customers]** > **[!UICONTROL Companies]**。

   您可以使用网格上方的&#x200B;_[!UICONTROL Columns]_&#x200B;选择器来显示&#x200B;**[!UICONTROL Status]**&#x200B;列。

1. 在&#x200B;_[!UICONTROL Action]_&#x200B;列中，单击&#x200B;**[!UICONTROL Edit]**。

1. 将&#x200B;**[!UICONTROL Company Status]**&#x200B;设置为`Active`。

   ![设置公司状态](./assets/company-status-active.png){width="700" zoomable="yes"}

1. 提示确认时，单击&#x200B;**[!UICONTROL Change status]**。

   公司管理员会收到公司当前处于活动状态的电子邮件通知。

1. 如果适用，请将&#x200B;**[!UICONTROL Sales Representative]**&#x200B;设置为特定的管理员用户帐户。

1. 展开&#x200B;**[!UICONTROL Account Information]**&#x200B;部分的![扩展选择器](../assets/icon-display-expand.png)，并使用&#x200B;**[!UICONTROL Comment]**&#x200B;字段输入有关帐户的注释。

   评论在店面不可见。

1. 完成后，单击&#x200B;**[!UICONTROL Save]**。

   向公司和公司管理员发送确认电子邮件，确认公司帐户已获得批准。

## 公司状态

| 状态 | 描述 |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Active] | 公司已获批准，公司管理员可从店面对其进行管理。 |
| [!UICONTROL Pending Approval] | 创建公司帐户的请求已从店面提交，但尚未审核。 |
| [!UICONTROL Rejected] | 创建公司帐户的请求被商店管理员拒绝。 |
| [!UICONTROL Blocked] | 公司账户不再健全。 客户可以从店面访问帐户，但不能进行购买。 |

{style="table-layout:auto"}

---
title: 管理公司用户帐户
description: 了解公司用户帐户以及它们在关联的公司帐户中的运行方式。
exl-id: 36b55f61-e579-4eb8-8f67-0156221d378e
feature: B2B, Companies, User Account, Storefront
role: Admin, User
source-git-commit: 03d1892799ca5021aad5c19fc9f2bb4f5da87c76
workflow-type: tm+mt
source-wordcount: '390'
ht-degree: 0%

---

# 管理公司用户帐户

公司用户由公司管理员分配，并且在&#x200B;_[!UICONTROL Customers]_网格中的管理员中按客户类型_[!UICONTROL Company User]_&#x200B;可见。 这些个人通常是具有不同级别权限来访问商店服务和资源的购买者。

公司管理员首先设置[公司结构](account-company-structure.md)，然后根据需要完成以下任务：

- 创建公司用户并将用户分配给团队

- 定义角色和权限，并将用户分配给角色

>[!IMPORTANT]
>
>公司用户只能由公司管理员添加、编辑或删除。 移除操作无法撤消，因为用户已从公司结构中移除。

## 添加公司用户

1. 公司管理员从店面登录他们的帐户。

1. 在左侧面板中，选择&#x200B;**[!UICONTROL Company Users]**。

   ![公司用户](./assets/company-users-list-storefront.png){width="700" zoomable="yes"}

1. 单击&#x200B;**[!UICONTROL Add New User]**&#x200B;并执行以下操作：

   - 输入新用户的&#x200B;**[!UICONTROL Job Title]**。

   - 如果定义了角色和权限，则选择适当的&#x200B;**[!UICONTROL User Role]**。 否则，他们可以稍后返回以分配角色。

     ![添加新用户](./assets/company-structure-users-add.png){width="700" zoomable="yes"}

   - 根据用户的需要填写其余字段：

      - **[!UICONTROL First Name]**&#x200B;和&#x200B;**[!UICONTROL Last Name]**
      - **[!UICONTROL Email]**
      - **[!UICONTROL Phone Number]**

   默认情况下，帐户的&#x200B;**[!UICONTROL Status]**&#x200B;为`Active`。

1. 完成后，单击&#x200B;**[!UICONTROL Save]**。

1. 重复该过程以根据需要创建尽可能多的公司用户。

   新用户与“公司管理员”一起显示在“公司用户”列表中。

为了节省首次订购的时间，公司管理员可以提醒每个公司用户将默认的公司帐单和送货地址添加到其[通讯簿](../customers/account-dashboard-address-book.md)。

## 编辑公司用户

1. 公司管理员从店面登录他们的帐户。

1. 在左侧面板中，选择&#x200B;**[!UICONTROL Company Users]**。

1. 查找要更新的用户记录，然后单击&#x200B;**[!UICONTROL Edit]**。

1. 进行所需的更改。

1. 完成后，单击&#x200B;**[!UICONTROL Save]**。

## 删除公司用户

1. 公司管理员从店面登录他们的帐户。

1. 在左侧面板中，选择&#x200B;**[!UICONTROL Company Structure]**。

1. 选择公司结构中的公司用户。

1. 单击&#x200B;**[!UICONTROL Delete Selected]**。

   ![删除用户](./assets/company-structure-delete-user.png){width="600" zoomable="yes"}

1. 提示确认时，单击&#x200B;**[!UICONTROL Delete]**。

在管理员中，公司用户仍列在[客户](../customers/customers-all.md)网格中，但处于`Inactive`状态。

## 字段描述

| 字段 | 描述 |
|--------------|---------------|
| [!UICONTROL Job Title] | 公司用户的工作标题。 |
| [!UICONTROL User Role] | 分配给公司用户的[角色](account-company-roles-permissions.md)。 选项： `Default User` / （其他角色） |
| [!UICONTROL First Name] | 公司用户的名字。 |
| [!UICONTROL Last Name] | 公司用户的姓氏。 |
| [!UICONTROL Email] | 公司用户的电子邮件地址。 |
| [!UICONTROL Phone Number] | 公司用户的电话号码。 |
| [!UICONTROL Status] | 公司用户帐户的状态。 选项： `Active` / `Inactive` |

{style="table-layout:auto"}

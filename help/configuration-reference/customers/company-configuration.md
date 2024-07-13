---
title: '[!UICONTROL Customers] &amp；gt； [!UICONTROL Company Configuration]'
description: 查看Commerce管理员的[!UICONTROL Customers] &amp；gt； [!UICONTROL Company Configuration]页面上的配置设置。
exl-id: 330eabeb-edab-4a9f-968e-37d0b95cdedb
feature: Configuration, Companies
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '837'
ht-degree: 0%

---

# [!UICONTROL Customers] > [!UICONTROL Company Configuration]

{{b2b-feature}}

{{config}}

>[!TIP]
>
>通过安装和启用Adobe Commerce B2B，您可以利用公司的特定功能个性化购买体验。 Adobe Commerce B2B是一个集成式解决方案，同时支持B2B和B2C模型。 有关B2B功能的详细信息，请参阅[Adobe Commerce B2B用户指南](https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html)。

>[!NOTE]
>
>对B2B功能的这些配置选项的访问权限由[角色资源](../../systems/permissions-user-roles.md#role-resources)控制。 必须为分配给管理员用户的用户角色设置这些角色资源。

有关配置这些设置的详细信息，请参阅&#x200B;_Adobe Commerce B2B用户指南_&#x200B;中的[启用基本B2B功能](../../b2b/enable-basic-features.md)。

## [!UICONTROL General]

![常规](./assets/company-general.png)<!-- zoom -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Allow Company Registration from the Storefront] | 网站 | 确定您商店的访客是可以选择为公司帐户还是个人帐户[注册](../../customers/customer-sign-in.md)。 选项： `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Email Options - Company Registration]

![电子邮件选项 — 公司注册](./assets/company-email-options-company-registration.png)<!-- zoom -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Company Registration Email Recipient] | 商店视图 | 从店面提交公司注册请求时通知的店面联系人。 选项： `General Contact` / `Sales Representative` / `Customer Support` / `Custom Email 1` / `Custom Email 2` |
| [!UICONTROL Send Company Registration Email Copy To] | 商店视图 | 接收注册通知副本的每个人的电子邮件地址。 用逗号分隔多个电子邮件地址。 |
| [!UICONTROL Send Email Copy Method] | 商店视图 | 用于发送注册电子邮件副本的电子邮件方法。 选项： `Bcc` / `Separate Email` |
| [!UICONTROL Default Company Registration Email] | 商店视图 | 默认用于公司注册通知的电子邮件模板。 默认模板： `Company Registration Request` |

{style="table-layout:auto"}

## [!UICONTROL Customer-Related Emails]

![与客户相关的电子邮件](./assets/company-email-options-customer-related-emails.png)<!-- zoom -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Default 'Sales Rep Assigned' Email] | 商店视图 | 将销售代表分配给公司帐户时默认使用的电子邮件模板。 此电子邮件将发送给销售代表和公司管理员。 默认模板： `Sales Representative Assigned to Company` |
| [!UICONTROL Default 'Assign Company to Customer' Email] | 商店视图 | 将单个客户帐户分配给公司帐户时默认使用的电子邮件模板。 此电子邮件仅发送给客户。 默认模板： `Assign Company to Customer` |
| [!UICONTROL Default 'Assign Company Admin' Email] | 商店视图 | 将公司管理员分配给公司时使用的电子邮件模板。 此电子邮件将发送给销售代表和公司管理员。 默认模板： `Assign Company Admin` |
| [!UICONTROL Default 'Company Admin Inactive' Email] | 商店视图 | 作为公司管理员的人员的状态更改为“不活动”时，默认使用的电子邮件模板。 系统向新的和以前的公司管理员发送更改电子邮件通知。 默认模板： `Company Admin Set Inactive` |
| [!UICONTROL Default 'Company Admin Changed to Member' Email] | 商店视图 | 当前公司管理员成为公司成员时，默认使用的电子邮件模板。 电子邮件仅发送给公司成员。 默认模板： `Company Admin Changed to Member` |
| [!UICONTROL Default 'Customer Status Active' Email] | 商店视图 | 客户状态变为活动时默认使用的电子邮件模板。 此电子邮件仅发送给客户。 默认模板： `Customer Status Active` |
| [!UICONTROL Default 'Customer Status Inactive' Email] | 商店视图 | 客户状态变为不活动时默认使用的电子邮件模板。 此电子邮件仅发送给客户。 默认模板： `Customer Status Inactive` |

{style="table-layout:auto"}

## [!UICONTROL Company Status Change]

![公司状态更改](./assets/company-email-options-company-status-change.png)<!-- zoom -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Company Status Change Email Recipient] | 商店视图 | 每当公司状态发生变化时通知的商店联系人。 选项： `General Contact` / `Sales Representative` / `Customer Support` / `Custom Email 1` / `Custom Email 2` |
| [!UICONTROL Send Company Status Change Email Copy To] | 商店视图 | 每个接收公司状态更改通知副本的人员的电子邮件地址。 用逗号分隔多个电子邮件地址。 |
| [!UICONTROL Send Email Copy Method] | 商店视图 | 用于发送状态更改通知副本的电子邮件方法。 选项： `Bcc` / `Separate Email` |
| [!UICONTROL Default "Company Status Change to Active 1' Email] | 商店视图 | 当公司的状态从&#x200B;_未决批准_&#x200B;更改为&#x200B;_活动_&#x200B;时使用的电子邮件模板。 默认模板： `Company Status Active 1` |
| [!UICONTROL Default 'Company Status Change to Active 2' Email] | 商店视图 | 公司状态从&#x200B;_已拒绝_&#x200B;或&#x200B;_已阻止_&#x200B;更改为&#x200B;_活动_&#x200B;时默认使用的电子邮件模板。 默认模板： `Company Status Active 2` |
| [!UICONTROL Default 'Company Status Change to Rejected' Email] | 商店视图 | 公司状态更改为&#x200B;_已拒绝_&#x200B;时默认使用的电子邮件模板。 默认模板： `Company Status Rejected` |
| [!UICONTROL Default 'Company Status Change to Blocked' Email] | 商店视图 | 公司状态更改为&#x200B;_已阻止_&#x200B;时默认使用的电子邮件模板。 默认模板： `Company Status Blocked` |
| [!UICONTROL Default 'Company Status Change to Pending Approval' Email] | 商店视图 | 公司状态更改为&#x200B;_未决批准_&#x200B;时默认使用的电子邮件模板。 默认模板： `Company Status Pending Approval` |

{style="table-layout:auto"}

## [!UICONTROL Company Credit]

![公司信用](./assets/company-email-options-company-credit.png)<!-- zoom -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Company Credit Change Email Sender] | 商店视图 | 公司信用发生更改时通知的商店联系人。 选项： `General Contact` / `Sales Representative` / `Customer Support` / `Custom Email 1` / `Custom Email 2` |
| [!UICONTROL Send Company Credit Change Email Copy To] | 商店视图 | 每个将接收公司信用更改通知副本的人员的电子邮件地址。 用逗号分隔多个电子邮件地址。 |
| [!UICONTROL Send Email Copy Method] | 商店视图 | 用于发送信用更改通知副本的电子邮件方法。 选项： `Bcc` / `Separate Email` |
| [!UICONTROL Allocated Email Template] | 商店视图 | 分配公司业绩时默认使用的电子邮件模板。 此电子邮件将发送给公司管理员。 默认模板： `Credit Limit Allocated` |
| [!UICONTROL Updated Email Template] | 商店视图 | 更新公司的信用额度时默认使用的电子邮件模板。 此电子邮件将发送给公司管理员。 默认模板： `Credit Limit Updated` |
| [!UICONTROL Reimbursed Email Template] | 商店视图 | 对公司信用进行[报销](../../b2b/credit-company.md#apply-a-payment-to-a-company-account)时默认使用的电子邮件模板。 此电子邮件将发送给公司管理员。 默认模板： `Credit Reimbursed` |
| [!UICONTROL Refunded Email Template] | 商店视图 | 将订单中的金额退回到公司贷项时默认使用的电子邮件模板。 此电子邮件将发送给公司管理员。 默认模板： `Order Refunded to Company Credit` |
| [!UICONTROL Reverted Email Template] | 商店视图 | 将订单还原为公司信用时默认使用的电子邮件模板。 此电子邮件将发送给公司管理员。 默认模板： `Order Reverted to Company Credit` |

{style="table-layout:auto"}

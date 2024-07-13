---
title: 配置公司电子邮件
description: 了解用于为公司帐户发送通信的电子邮件选项和模板。
exl-id: fd61c0c6-0887-4ff2-8002-906ff615bad9
feature: B2B, Companies, Configuration
role: Admin
source-git-commit: 03d1892799ca5021aad5c19fc9f2bb4f5da87c76
workflow-type: tm+mt
source-wordcount: '676'
ht-degree: 0%

---

# 配置公司电子邮件选项

默认情况下，将指定为公司主要联系人的[销售代表](account-company-manage.md)配置为许多自动发送给公司的电子邮件的发件人。

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧面板中，展开&#x200B;**[!UICONTROL Customers]**&#x200B;并选择&#x200B;**[!UICONTROL Company Configuration]**。

1. 如有必要，请将&#x200B;**[!UICONTROL Store View]**&#x200B;设置为存储视图以定义配置的[作用域](../getting-started/websites-stores-views.md#scope-settings)。

1. 完成&#x200B;**[!UICONTROL Company Registration]**&#x200B;部分：

   >[!NOTE]
   >
   >清除&#x200B;**[!UICONTROL Use system value]**&#x200B;复选框以使字段可编辑。

   - 将&#x200B;**[!UICONTROL Company Registration Email Recipient]**&#x200B;设置为[商店联系人](../getting-started/store-details.md#store-email-addresses)，在收到新的公司注册请求时会通知该联系人。

   - 在&#x200B;**[!UICONTROL Send Company Registration Email Copy To]**&#x200B;字段中，输入要接收注册通知副本的每个人的电子邮件地址。 用逗号分隔多个电子邮件地址。

   - 要确定通知副本的发送方式，请将&#x200B;**[!UICONTROL Send Email Copy Method]**&#x200B;设置为以下项之一：

      - `Bcc` — 通过在发送给客户的同一电子邮件的标头中包含收件人，发送&#x200B;_免费副本_。 客户看不到密件抄送收件人。
      - `Separate Email` — 将副本作为单独的电子邮件发送。

   - 如果您已准备要使用的电子邮件模板而不是默认模板，请将&#x200B;**[!UICONTROL Default Company Registration Email]**&#x200B;设置为模板的名称。 默认情况下，使用`Company Registration Request`模板。

     ![客户配置 — 公司注册](./assets/company-email-options-company-registration.png){width="600" zoomable="yes"}

1. 完成&#x200B;**[!UICONTROL Customer-Related Emails]**&#x200B;部分：

   如果您已准备要使用的备用电子邮件模板而不是默认模板，请选择要用于以下各项的模板：

   - **[!UICONTROL Default 'Sales Rep Assigned' Email]**
   - **[!UICONTROL Default 'Assign Company to Customer' Email]**
   - **[!UICONTROL Default 'Assign Company Admin' Email]**
   - **[!UICONTROL Default 'Company Admin Inactive' Email]**
   - **[!UICONTROL Default 'Company Admin Changed to Member' Email]**
   - **[!UICONTROL Default 'Customer Status Active' Email]**
   - **[!UICONTROL Default 'Customer Status Inactive' Email]**

   ![客户配置 — 客户相关电子邮件](./assets/company-email-options-customer-related-emails.png){width="600" zoomable="yes"}

1. 完成&#x200B;**[!UICONTROL Company Status Change]**&#x200B;部分：

   - 将&#x200B;**[!UICONTROL Company Status Change for Email Recipient]**&#x200B;设置为[商店联系人](../getting-started/store-details.md#store-email-addresses)，当公司状态发生变化时，将通知该联系人。

   - 在&#x200B;**[!UICONTROL Send Company Status Change Email Copy To]**&#x200B;字段中，输入要接收状态更改通知副本的每个人的电子邮件地址。 用逗号分隔多个电子邮件地址。

   - 要确定通知副本的发送方式，请将&#x200B;**[!UICONTROL Send Email Copy Method]**&#x200B;设置为以下项之一：

      - `Bcc` — 通过在发送给客户的同一电子邮件的标头中包含收件人，发送&#x200B;_免费副本_。 客户看不到密件抄送收件人。
      - `Separate Email` — 将副本作为单独的电子邮件发送。

   - 如果您的准备好的电子邮件模板将在公司状态从`Pending Approval`更改为`Active`时使用，而不是默认模板，请将&#x200B;**[!UICONTROL Default 'Company Status Change to Active 1' Email]**&#x200B;设置为该模板。 默认情况下，使用`Company Status Active 1`模板。

   - 如果您有一个准备好的电子邮件模板，当公司状态从`Rejected`或`Blocked`更改为`Active`时，将使用该模板，而不是默认模板，请将&#x200B;**[!UICONTROL Default 'Company Status Change to Active 2' Email]**&#x200B;设置为该模板。 默认情况下，使用`Company Status Active 2`模板。

   - 如果您的准备好的电子邮件模板将在公司状态更改为`Rejected`时使用，而不是默认模板，请将&#x200B;**[!UICONTROL Default 'Company Status Change to Rejected' Email]**&#x200B;设置为该模板。 默认情况下，使用`Company Status Rejected`模板。

   - 如果您的准备好的电子邮件模板将在公司状态更改为`Blocked`时使用，而不是默认模板，请将&#x200B;**[!UICONTROL Default 'Company Status Change to Blocked' Email]**&#x200B;设置为该模板。 默认情况下，使用`Company Status Blocked`模板。

   - 如果您的准备好的电子邮件模板将在公司状态更改为`Pending Approval`时使用，而不是默认模板，请将&#x200B;**[!UICONTROL Default 'Company Status Change to Pending Approval' Email]**&#x200B;设置为该模板。 默认情况下，使用`Company Status Pending Approval`模板。

     ![客户配置 — 公司状态更改](./assets/company-email-options-company-status-change.png){width="600" zoomable="yes"}

1. 完成&#x200B;**[!UICONTROL Company Credit Emails]**&#x200B;部分：

   - 将&#x200B;**[!UICONTROL Company Credit Change Email Sender]**&#x200B;设置为[商店联系人](../getting-started/store-details.md#store-email-addresses)，当分配给公司的信用额度发生更改时，将通知该联系人。 默认情况下，该通知将发送给&#x200B;_销售代表_。

   - 在&#x200B;**[!UICONTROL Send Company Credit Change Email Copy To]**&#x200B;字段中，输入要接收信用更改通知副本的每个人员的电子邮件地址。 用逗号分隔多个电子邮件地址。

   - 要确定通知副本的发送方式，请将&#x200B;**[!UICONTROL Send Email Copy Method]**&#x200B;设置为以下项之一：

      - `Bcc` — 通过在发送给客户的同一电子邮件的标头中包含收件人，发送&#x200B;_免费副本_。 客户看不到密件抄送收件人。
      - `Separate Email` — 将副本作为单独的电子邮件发送。

   - 如果您已准备要使用的电子邮件模板而不是默认模板，请为发送给公司管理员的以下每个通知选择模板。

      - **[!UICONTROL Allocated Email Template]**
      - **[!UICONTROL Updated Email Template]**
      - **[!UICONTROL Reimbursed Email Template]**
      - **[!UICONTROL Refunded Email Template]**
      - **[!UICONTROL Reverted Email Template]**

   ![客户配置 — 公司信用电子邮件](./assets/company-email-options-company-credit.png){width="600" zoomable="yes"}

1. 完成后，单击&#x200B;**[!UICONTROL Save Config]**。

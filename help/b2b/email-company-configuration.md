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

此 [销售代表](account-company-manage.md) 默认情况下，会将指定为公司的主要联系人的电子邮件配置为许多发送给公司的自动电子邮件的发件人。

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中，展开 **[!UICONTROL Customers]** 并选择 **[!UICONTROL Company Configuration]**.

1. 如有必要，请设置 **[!UICONTROL Store View]** 到商店视图以定义 [范围](../getting-started/websites-stores-views.md#scope-settings) 配置中。

1. 完成 **[!UICONTROL Company Registration]** 部分：

   >[!NOTE]
   >
   >清除 **[!UICONTROL Use system value]** 复选框，使字段可编辑。

   - 设置 **[!UICONTROL Company Registration Email Recipient]** 到 [商店联系人](../getting-started/store-details.md#store-email-addresses) 在收到新的公司注册请求时，将通知谁。

   - 在 **[!UICONTROL Send Company Registration Email Copy To]** 字段中，输入要接收注册通知副本的每个人员的电子邮件地址。 用逗号分隔多个电子邮件地址。

   - 要确定通知副本的发送方式，请设置 **[!UICONTROL Send Email Copy Method]** 更改为以下任一项：

      - `Bcc`  — 发送 _盲文提供_ 在发送给客户的同一电子邮件的标题中包含收件人。 客户看不到密件抄送收件人。
      - `Separate Email`  — 将副本作为单独的电子邮件发送。

   - 如果您已准备要使用的电子邮件模板而不是默认模板，请设置 **[!UICONTROL Default Company Registration Email]** 到模板的名称。 默认情况下， `Company Registration Request` 使用模板。

     ![客户配置 — 公司注册](./assets/company-email-options-company-registration.png){width="600" zoomable="yes"}

1. 完成 **[!UICONTROL Customer-Related Emails]** 部分：

   如果您已准备要使用的备用电子邮件模板而不是默认模板，请选择要用于以下各项的模板：

   - **[!UICONTROL Default 'Sales Rep Assigned' Email]**
   - **[!UICONTROL Default 'Assign Company to Customer' Email]**
   - **[!UICONTROL Default 'Assign Company Admin' Email]**
   - **[!UICONTROL Default 'Company Admin Inactive' Email]**
   - **[!UICONTROL Default 'Company Admin Changed to Member' Email]**
   - **[!UICONTROL Default 'Customer Status Active' Email]**
   - **[!UICONTROL Default 'Customer Status Inactive' Email]**

   ![客户配置 — 客户相关电子邮件](./assets/company-email-options-customer-related-emails.png){width="600" zoomable="yes"}

1. 完成 **[!UICONTROL Company Status Change]** 部分：

   - 设置 **[!UICONTROL Company Status Change for Email Recipient]** 到 [商店联系人](../getting-started/store-details.md#store-email-addresses) 当公司的状态发生变化时，将通知谁。

   - 在 **[!UICONTROL Send Company Status Change Email Copy To]** 字段中，输入要接收状态更改通知副本的每个人员的电子邮件地址。 用逗号分隔多个电子邮件地址。

   - 要确定通知副本的发送方式，请设置 **[!UICONTROL Send Email Copy Method]** 更改为以下任一项：

      - `Bcc`  — 发送 _盲文提供_ 在发送给客户的同一电子邮件的标题中包含收件人。 客户看不到密件抄送收件人。
      - `Separate Email`  — 将副本作为单独的电子邮件发送。

   - 如果您有准备好的电子邮件模板，则在公司状态从更改时使用该模板，而不是默认模板 `Pending Approval` 到 `Active`，设置 **[!UICONTROL Default 'Company Status Change to Active 1' Email]** 到那个模板上。 默认情况下， `Company Status Active 1` 使用模板。

   - 如果您有准备好的电子邮件模板，则在公司状态从更改时使用该模板，而不是默认模板 `Rejected` 或 `Blocked` 到 `Active`，设置 **[!UICONTROL Default 'Company Status Change to Active 2' Email]** 到那个模板上。 默认情况下， `Company Status Active 2` 使用模板。

   - 如果您有准备好的电子邮件模板，当公司状态更改为时，将使用该模板，而不是默认模板 `Rejected`，设置 **[!UICONTROL Default 'Company Status Change to Rejected' Email]** 到那个模板上。 默认情况下， `Company Status Rejected` 使用模板。

   - 如果您有准备好的电子邮件模板，当公司状态更改为时，将使用该模板，而不是默认模板 `Blocked`，设置 **[!UICONTROL Default 'Company Status Change to Blocked' Email]** 到那个模板上。 默认情况下， `Company Status Blocked` 使用模板。

   - 如果您有准备好的电子邮件模板，当公司状态更改为时，将使用该模板，而不是默认模板 `Pending Approval`，设置 **[!UICONTROL Default 'Company Status Change to Pending Approval' Email]** 到那个模板上。 默认情况下， `Company Status Pending Approval` 使用模板。

     ![客户配置 — 公司状态更改](./assets/company-email-options-company-status-change.png){width="600" zoomable="yes"}

1. 完成 **[!UICONTROL Company Credit Emails]** 部分：

   - 设置 **[!UICONTROL Company Credit Change Email Sender]** 到 [商店联系人](../getting-started/store-details.md#store-email-addresses) 指定给公司的信用额度发生更改时，将通知哪些人。 默认情况下，通知将发送至 _销售代表_.

   - 在 **[!UICONTROL Send Company Credit Change Email Copy To]** 字段中，输入接收信用更改通知副本的每个人员的电子邮件地址。 用逗号分隔多个电子邮件地址。

   - 要确定通知副本的发送方式，请设置 **[!UICONTROL Send Email Copy Method]** 更改为以下任一项：

      - `Bcc`  — 发送 _盲文提供_ 在发送给客户的同一电子邮件的标题中包含收件人。 客户看不到密件抄送收件人。
      - `Separate Email`  — 将副本作为单独的电子邮件发送。

   - 如果您已准备要使用的电子邮件模板而不是默认模板，请为发送给公司管理员的以下每个通知选择模板。

      - **[!UICONTROL Allocated Email Template]**
      - **[!UICONTROL Updated Email Template]**
      - **[!UICONTROL Reimbursed Email Template]**
      - **[!UICONTROL Refunded Email Template]**
      - **[!UICONTROL Reverted Email Template]**

   ![客户配置 — 公司信用电子邮件](./assets/company-email-options-company-credit.png){width="600" zoomable="yes"}

1. 完成后，单击 **[!UICONTROL Save Config]**.

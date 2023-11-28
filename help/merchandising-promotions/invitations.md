---
title: 活动邀请
description: 了解客户如何从其客户帐户的仪表板发送和查看活动和私人销售邀请。
exl-id: 6a9123a0-bdb4-4cd6-99cd-658f728aa90c
feature: Promotions/Events, Communications
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '633'
ht-degree: 0%

---

# 活动邀请

{{ee-feature}}

启用邀请后，客户可以从其客户帐户的仪表板发送和查看邀请。 邀请电子邮件包括一个指向您商店的客户登录页面的链接。

## 我的邀请

此 _[!UICONTROL My Invitations]_客户帐户的部分列出了客户发送的所有邀请。 客户可以向朋友和家人发送邀请，让他们参加商店活动、礼品注册和愿望清单等。

![我的邀请](./assets/account-dashboard-my-invitations.png){width="700" zoomable="yes"}

### 邀请工作流程

1. **客户准备邀请**：客户通过帐户仪表板准备收件人列表并完成邀请。 可包含自定义消息，具体取决于配置。
1. **客户发送邀请**：准备就绪后，客户单击 _[!UICONTROL Send Invitations]_按钮。
1. **系统管理传输**：系统根据配置中设置的数量批量发送邀请。
1. **客户监控响应**：客户从帐户仪表板监控每个邀请的状态，如 `Sent`， `Accepted`，或 `Canceled`.

### 发送邀请

1. 在店面账户侧边栏中，客户选择 **[!UICONTROL My Invitations]**.

1. 在 _我的邀请_ 页面，点击量 **[!UICONTROL Send Invitation]**.

1. 定义新的邀请项目：

   - 完成电子邮件信息。

   - （可选）通过单击创建多地址邀请 **+** 并添加另一个电子邮件地址。

     单个邀请的电子邮件地址限制为5个。

   - （可选）输入随附消息。

1. 完成后，单击 **[!UICONTROL Send Invitation]**.

将向受邀用户的电子邮件地址发送邀请通知，其中包含用于设置帐户的说明链接。

>[!NOTE]
>
>用户只能向特定电子邮件地址发送一个邀请。 尝试将邀请重新发送到同一电子邮件地址会导致显示错误消息，并且不会发送邀请。

## 为您的商店启用邀请

邀请配置启用商店邀请并决定发送方式。

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中，展开 **[!UICONTROL Customers]** 并选择 **[!UICONTROL Invitations]**.

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL General]** 部分。

   ![客户配置 — 邀请常规选项](../configuration-reference/customers/assets/invitations-general.png){width="600" zoomable="yes"}

1. 设置 **[!UICONTROL Enable Invitations Functionality]** 到 `Yes`.

1. 要允许客户管理店面的邀请，请设置 **在店面启用邀请** 到 `Yes`.

1. 设置 **[!UICONTROL Referred Customer Group]** 更改为以下任一项：

   - `Same as Inviter`
   - `Default Customer Group from Configuration`

1. 设置 **[!UICONTROL New Accounts Registration]** 更改为以下任一项：

   - `By Invitation Only`
   - `Available to All`

1. 至 **[!UICONTROL Allow Customers to Add Custom Message to Invitation Email]**，选择 `Yes`.

1. 要限制一次可发送的邀请数，请在 **[!UICONTROL Max Invitations Allowed to be Sent at One Time]** 字段。

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Email]** 部分并执行以下操作：

   ![客户配置 — 邀请电子邮件选项](../configuration-reference/customers/assets/invitations-email.png){width="600" zoomable="yes"}

   - 选择要用作的存储标识 **[!UICONTROL Customer Invitation Email Sender]**.

   - 选择 **[!UICONTROL Customer Invitation Email Template]** 用于发送的邀请。

1. 完成后，单击 **[!UICONTROL Save Config]**.

## 在管理员中发送和管理邀请

在 [专用销售报表](../getting-started/private-sales-reports.md) 部分中，您可以查看在指定时间段发送的邀请数，或您已向其发送邀请的客户。

### 在管理员中创建邀请

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Marketing]** > _[!UICONTROL Private Sales]_>**[!UICONTROL Invitations]**.

1. 在右上角，单击 **[!UICONTROL Add Invitations]**.

1. 在下一个屏幕中，输入电子邮件地址以邀请新客户，添加自定义消息，选择发件人，然后选择受邀者组。

   如果您有多个商店视图，请使用 **[!UICONTROL Send From]** 用于指定从中发送邀请的存储区视图的选项。

   ![邀请信息](./assets/create-invitation-page.png){width="700" zoomable="yes"}

1. 完成后，单击 **[!UICONTROL Save]**.

### 放弃单个实体的邀请

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Marketing]** > _[!UICONTROL Private Sales]_>**[!UICONTROL Invitations]**.

1. 使用筛选器查找所需的邀请，并在编辑模式下将其打开。

1. 在右上角，单击 **[!UICONTROL Discard Invitation]**.

1. 要确认操作，请单击 **[!UICONTROL OK]**.

### 放弃多个实体的邀请

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Marketing]** > _[!UICONTROL Private Sales]_>**[!UICONTROL Invitations]**.

1. 查找并选择要放弃的邀请。

1. 在左上角，使用 **[!UICONTROL Actions]** 要选择的菜单 **[!UICONTROL Discard Selected]** 并单击 **[!UICONTROL Submit]**.

1. 要确认操作，请单击 **[!UICONTROL OK]**.

### 字段描述

| 字段 | 描述 |
|--- |--- |
| [!UICONTROL Select] | 选中此复选框可选择要执行某项操作的邀请，或者使用列标题中的选择控件。 选项： `Select All` /` Deselect All` / `Select Visible` / `Unselect Visible` |
| [!UICONTROL ID] | 邀请的内部标识号 |
| [!UICONTROL Email] | 相应的客户电子邮件地址 |
| [!UICONTROL Invitee] | 受邀用户电子邮件 |
| [!UICONTROL Sent] | 发送邀请的时间和日期 |
| [!UICONTROL Registered] | 客户注册的时间和数据 |
| [!UICONTROL Status] | 邀请状态。 选项： `Sent` / `Not Sent` / `Accepted` / `Discarded` |
| [!UICONTROL Valid Website] | 相应的网站 |
| [!UICONTROL Invitee Group] | 被邀请人的客户组 |

{style="table-layout:auto"}

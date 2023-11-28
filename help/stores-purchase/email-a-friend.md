---
title: 向朋友发送电子邮件
description: 了解如何提供电子邮件链接，以便客户能够轻松地与朋友共享产品链接。
exl-id: 46cf9994-6490-4cb4-85b7-9a7cab7783e0
feature: Storefront, Configuration
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 0%

---

# 向朋友发送电子邮件

电子邮件链接可让您的客户轻松地与朋友共享指向产品的链接。 在演示Luma商店中，电子邮件链接显示为信封图标。 可以根据您的语音和品牌定制消息模板。 要防止发送垃圾邮件，您可以限制每封电子邮件的收件人数量，以及在一小时内可以共享的产品数量。

![示例店面 — 向朋友发送电子邮件](./assets/storefront-email-a-friend.png){width="700" zoomable="yes"}

## 配置朋友电子邮件

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中，展开 **[!UICONTROL Catalog]** 并选择 **[!UICONTROL Email to a Friend]**.

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Email Templates]** 并设置以下选项：

   ![目录配置 — 电子邮件模板](../configuration-reference/catalog/assets/email-to-a-friend-email-templates.png){width="600" zoomable="yes"}

   有关每个配置设置的详细说明，请参阅 [电子邮件模板](../configuration-reference/catalog/email-to-a-friend.md) 在 _配置参考指南_.

   要更改任何字段的默认设置，请清除 **[!UICONTROL Use system value]** 复选框，使字段可编辑。

   - 设置 **[!UICONTROL Enabled]** 到 `Yes`.

   - 设置 **[!UICONTROL Select Email Template]** 要用作消息基础的模板。

   - 如果要要求仅注册客户可以向朋友发送电子邮件，请设置 **[!UICONTROL Allow for Guests]** 到 `No`.

   - 对象 **[!UICONTROL Max Recipients]**，输入单个消息可以加入通讯组列表的最多朋友数量。

   - 对象 **[!UICONTROL Max Products Sent in 1 Hour]**，输入单个用户在一小时内的好友可以共享的产品的最大数量。

   - 设置 **[!UICONTROL Limit Sending By]** 使用以下方法之一来识别电子邮件的发件人：

     `IP Address`   — （推荐）根据用于发送电子邮件的计算机的IP地址标识发件人。

     `Cookie (unsafe)`  — 通过浏览器Cookie标识发件人。 此方法不太有效，因为发送者可以删除Cookie以绕过限制。

1. 完成后，单击 **[!UICONTROL Save Config]**.

## 向店面的朋友发送电子邮件

配置此功能后，商店客户将按照以下步骤与好友共享产品信息。

1. 在目录页面上，客户单击 **[!UICONTROL Email]** 链接。

1. 如果仅为注册用户配置该功能，则执行以下操作之一：

   - 登录到您的客户帐户。
   - 注册一个新帐户。

1. 完成 **[!UICONTROL Message]** 并输入收件人 **[!UICONTROL Name]** 和 **[!UICONTROL Email Address]**.

   如果需要，客户可以添加更多收件人：

   - 点击次数 **[!UICONTROL Add Invitee]**.

   - 进入 **[!UICONTROL Name]** 和 **[!UICONTROL Email Address]** 其他人员的。

     他们可以向配置允许数量的其他人员发送消息。 他们可以通过单击 **[!DNL Remove]** 链接。

1. 准备发送消息时，单击 **[!UICONTROL Send Email]**.

   ![示例店面 — 通过电子邮件发送给朋友](./assets/storefront-email-a-friend-form.png){width="700" zoomable="yes"}

---
title: 销售电子邮件
description: 了解如何配置销售电子邮件，以支持向客户提供有关其订单的通信。
exl-id: b205dc61-08cc-4783-810c-686ccf2ba300
feature: Communications, Orders
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '424'
ht-degree: 0%

---

# 销售电子邮件

与订单相关的事件会触发多个电子邮件，并且配置类似。 确保您识别显示为邮件发件人的商店联系人、要使用的电子邮件模板以及要接收邮件副本的任何其他人。 销售电子邮件可以在由事件触发时发送，也可以按预定间隔发送。

![销售配置 — 销售电子邮件](./assets/config-sales-sales-email-full.png){width="600" zoomable="yes"}

## 步骤1. 更新电子邮件模板

确保更新[电子邮件标头](../systems/email-template-custom.md#header-template)模板，以便它反映您的品牌，并根据需要反映其他电子邮件模板。 有关模板的完整列表，请参阅[电子邮件模板](../systems/email-templates.md)。

## 步骤2. 选择传输类型

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧面板中，展开&#x200B;**[!UICONTROL Sales]**&#x200B;并选择&#x200B;**[!UICONTROL Sales Emails]**。

1. 如有必要，请展开![扩展选择器](../assets/icon-display-expand.png) **[!UICONTROL General Settings]**&#x200B;部分。

   ![销售配置 — 销售电子邮件常规设置](../configuration-reference/sales/assets/sales-emails-general-settings.png){width="600" zoomable="yes"}

   默认情况下，异步发送设置为`Disable`。 要更改系统设置，请清除&#x200B;**[!UICONTROL Use system value]**&#x200B;复选框，并将&#x200B;**[!UICONTROL Asynchronous sending]**&#x200B;设置为以下项之一：

   - `Disable` — 在事件触发时发送销售电子邮件。
   - `Enable` — 定期发送销售电子邮件。

   Adobe Commerce支持部门建议启用异步发送以提高下单性能。 请参阅Adobe Commerce支持知识库中的[订单处理的配置最佳实践](https://experienceleague.adobe.com/docs/commerce-operations/implementation-playbook/best-practices/maintenance/order-processing-configuration.html)。

## 步骤3. 填写每封销售电子邮件的详细信息

1. 如有必要，请展开![扩展选择器](../assets/icon-display-expand.png) **[!UICONTROL Order]**&#x200B;部分。

   ![销售配置 — 销售电子邮件订单](../configuration-reference/sales/assets/sales-emails-order.png){width="600" zoomable="yes"}

1. 验证&#x200B;**[!UICONTROL Enabled]**&#x200B;是否设置为`Yes`（默认）。

1. 将&#x200B;**[!UICONTROL New Order Confirmation Email]**&#x200B;设置为显示为邮件发件人的商店联系人。

1. 将&#x200B;**[!UICONTROL New Order Confirmation Template]**&#x200B;设置为用于发送给注册客户的电子邮件的模板。

1. 将&#x200B;**[!UICONTROL New Order Confirmation Template for Guest]**&#x200B;设置为用于发送电子邮件的模板，该电子邮件将发送给没有您商店帐户的来宾。

1. 对于&#x200B;**[!UICONTROL Send Order Email Copy To]**，输入任何要接收新订单电子邮件副本的人员的电子邮件地址。

   如果向多个收件人发送副本，请使用逗号分隔每个地址。

1. 将&#x200B;**[!UICONTROL Send Order Email Copy Method]**&#x200B;设置为以下项之一：

   - `Bcc` — 通过在发送给客户的同一电子邮件的标头中包含收件人，发送&#x200B;_免费副本_。 客户看不到密件抄送收件人。
   - `Separate Email` — 将副本作为单独的电子邮件发送。

1. 展开![扩展选择器](../assets/icon-display-expand.png) **[!UICONTROL Order Comments]**&#x200B;部分并重复这些步骤。

   ![销售配置 — 销售电子邮件订单评论](../configuration-reference/sales/assets/sales-emails-order-comments.png){width="600" zoomable="yes"}

1. 完成其余销售电子邮件类型的配置：

   - **[!UICONTROL Invoice]** / **[!UICONTROL Invoice Comments]**
   - **[!UICONTROL Shipment]** / **[!UICONTROL Shipment Comments]**
   - **[!UICONTROL Credit Memo]** / **[!UICONTROL Credit Memo Comments]**

1. 完成后，单击&#x200B;**[!UICONTROL Save Config]**。

   出现提示时，单击工作区顶部消息中的[缓存管理](../systems/cache-management.md)链接，并清除所有无效缓存。

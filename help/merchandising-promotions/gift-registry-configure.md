---
title: 配置礼品登记簿
description: 了解如何启用礼品注册并配置相关电子邮件通知。
exl-id: 48193621-731d-4640-8ea8-5b201915cdf1
feature: Gift, Storefront, Configuration
TQID: https://experienceleague.adobe.com/a7DRiAPSkWhBIPdXPXnH3HB1uw9d4WY4vXOtfgg9kRY
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: bd989d82-1e15-4534-88db-f1f51dd77ffaid: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: b5520579-b31f-4df7-9281-f0d9f91e2edcid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 358
ht-degree: 0%

---

# 配置礼品登记簿

{{ee-feature}}

在向客户提供礼品注册之前，您必须启用礼品注册并配置相关电子邮件通知。 Adobe Commerce会发送以下电子邮件通知，以响应礼品注册工作流中的事件。

- 创建新的礼品注册时，会向所有者发送一封电子邮件，其中包含可共享的注册链接。
- 或者，商店可以向礼品注册所有者的朋友和家人发送包含礼品注册链接的通知。
- 从礼品注册处购买物品时，系统会通知所有者，但不会指明购买者。

Adobe Commerce为每条电子邮件提供了预定义的模板，您可以根据自己的品牌对这些模板进行自定义。

## 步骤1. 启用礼品登记簿

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧面板中，展开&#x200B;**[!UICONTROL Customers]**&#x200B;并选择&#x200B;**[!UICONTROL Gift Registry]**

1. 展开&#x200B;**[!UICONTROL General Options]**&#x200B;部分中的![扩展选择器](../assets/icon-display-expand.png)并执行以下操作：

   ![客户配置 — 礼品注册常规](../configuration-reference/customers/assets/gift-registry-general-options.png){width="600" zoomable="yes"}

   - 默认情况下，会启用礼品注册表。 如有必要，请将&#x200B;**[!UICONTROL Enable Gift Registry]**&#x200B;设置为`Yes`。

   - 对于&#x200B;**[!UICONTROL Maximum Registrants]**，请输入可以邀请其参加礼品注册活动的最大人数。

## 步骤2. 配置电子邮件通知

1. 展开&#x200B;**[!UICONTROL Owner Notification]**&#x200B;部分中的![扩展选择器](../assets/icon-display-expand.png)并执行以下操作：

   ![客户配置 — 礼品注册所有者通知](../configuration-reference/customers/assets/gift-registry-owner-notification.png){width="600" zoomable="yes"}

   - 选择在创建礼品注册表时通知其所有者的&#x200B;**[!UICONTROL Email Template]**。

   - 选择显示为消息&#x200B;**[!UICONTROL Email Sender]**&#x200B;的[存储联系人](../getting-started/store-details.md#store-email-addresses)。

1. 展开&#x200B;**[!UICONTROL Gift Registry Sharing]**&#x200B;部分中的![扩展选择器](../assets/icon-display-expand.png)并执行以下操作：

   ![客户配置 — 礼品注册共享](../configuration-reference/customers/assets/gift-registry-gift-registry-sharing.png){width="600" zoomable="yes"}

   - 选择在与礼品注册表收件人共享注册表时通知这些收件人的&#x200B;**[!UICONTROL Email Template]**。

   - 选择显示为消息&#x200B;**[!UICONTROL Email Sender]**&#x200B;的存储区标识。

   - 对于&#x200B;**[!UICONTROL Maximum Sent Emails Threshold]**，输入一次可以发送的最大电子邮件数。

1. 展开&#x200B;**[!UICONTROL Gift Registry Update]**&#x200B;部分中的![扩展选择器](../assets/icon-display-expand.png)并执行以下操作：

   ![客户配置 — 礼品注册更新](../configuration-reference/customers/assets/gift-registry-gift-registry-update.png){width="600" zoomable="yes"}

   - 选择将更改通知到注册表的&#x200B;**[!UICONTROL Email Template]**。

   - 选择显示为消息&#x200B;**[!UICONTROL Email Sender]**&#x200B;的存储区标识。

1. 完成后，单击&#x200B;**[!UICONTROL Save Config]**。

1. 出现提示时，更新缓存。

   在刷新缓存后，礼品注册显示在商店菜单的其他设置下，并可在客户帐户中使用。

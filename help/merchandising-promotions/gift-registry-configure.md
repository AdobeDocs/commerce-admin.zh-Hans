---
title: 配置礼品登记簿
description: 了解如何启用礼品注册并配置相关电子邮件通知。
exl-id: 48193621-731d-4640-8ea8-5b201915cdf1
feature: Gift, Storefront, Configuration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '356'
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

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中，展开 **[!UICONTROL Customers]** 并选择 **[!UICONTROL Gift Registry]**

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL General Options]** 部分并执行以下操作：

   ![客户配置 — 礼品注册常规](../configuration-reference/customers/assets/gift-registry-general-options.png){width="600" zoomable="yes"}

   - 默认情况下，会启用礼品注册表。 如有必要，请设置 **[!UICONTROL Enable Gift Registry]** 到 `Yes`.

   - 对象 **[!UICONTROL Maximum Registrants]**，输入可以受邀参加礼品注册活动的最大人数。

## 步骤2. 配置电子邮件通知

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Owner Notification]** 部分并执行以下操作：

   ![客户配置 — 礼品注册所有者通知](../configuration-reference/customers/assets/gift-registry-owner-notification.png){width="600" zoomable="yes"}

   - 选择 **[!UICONTROL Email Template]** 在创建礼品注册时通知其所有者。

   - 选择 [商店联系人](../getting-started/store-details.md#store-email-addresses) 显示为 **[!UICONTROL Email Sender]** 消息的。

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Gift Registry Sharing]** 部分并执行以下操作：

   ![客户配置 — 礼品注册共享](../configuration-reference/customers/assets/gift-registry-gift-registry-sharing.png){width="600" zoomable="yes"}

   - 选择 **[!UICONTROL Email Template]** 当与礼品注册接收者共享注册表时，通知他们。

   - 选择显示为 **[!UICONTROL Email Sender]** 消息的。

   - 对象 **[!UICONTROL Maximum Sent Emails Threshold]**，输入一次可以发送的最大电子邮件数。

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Gift Registry Update]** 部分并执行以下操作：

   ![客户配置 — 礼品注册更新](../configuration-reference/customers/assets/gift-registry-gift-registry-update.png){width="600" zoomable="yes"}

   - 选择 **[!UICONTROL Email Template]** 通知赠品注册所有者注册表的更改。

   - 选择显示为 **[!UICONTROL Email Sender]** 消息的。

1. 完成后，单击 **[!UICONTROL Save Config]**.

1. 出现提示时，更新缓存。

   在刷新缓存后，礼品注册显示在商店菜单的其他设置下，并可在客户帐户中使用。

---
title: 管理员消息收件箱
description: 了解管理员消息收件箱，该收件箱提供来自Adobe和 [!DNL Commerce] 系统的重要且有用的消息。
exl-id: c53bb0e4-9f18-4d40-8cc4-8c3b485f8d68
source-git-commit: 7b6d70e2f3052af69075790cec1f396e2505bf8b
workflow-type: tm+mt
source-wordcount: '395'
ht-degree: 0%

---

# 管理员消息收件箱

您的商店会定期接收来自Adobe的消息。 这些消息按重要性评级，可能涉及系统更新、修补程序、新版本、定期维护或即将发生的事件。 标题中的铃铛图标表示收件箱中未读邮件的数量。

![管理员 — 传入邮件](./assets/admin-inbox-summary.png){width="700" zoomable="yes"}

_[!UICONTROL Notifications]_页列出了按日期排序的所有邮件。_[!UICONTROL Action]_&#x200B;命令可用于将单个邮件标记为已读、查看更多详细信息或从收件箱中删除邮件。

该配置决定收件箱更新的频率以及邮件的投放方式。 如果您的商店管理员具有安全URL，则必须通过HTTPS传送通知。

## 查看新传入消息

1. 单击标题中的&#x200B;**[!UICONTROL Notification]**&#x200B;图标并读取摘要。

1. 执行以下操作之一：

   - 如有必要，单击消息以显示全文。
   - 要删除消息，请单击消息右侧的删除图标。
   - 要显示完整的通知列表，请单击&#x200B;**[!UICONTROL See All]**。

## 处理关键消息

对于关键重要消息，请执行下列操作之一：

- 单击&#x200B;**[!UICONTROL Read Details]**。
- 若要关闭警报框但使邮件保持活动状态，请单击&#x200B;**[!UICONTROL Close]**。

## 管理您的通知

1. 执行以下操作之一以打开“通知”页面：

   - 单击标题中的&#x200B;**[!UICONTROL Notification]**&#x200B;图标。 如果显示一个或多个新消息，请单击&#x200B;**[!UICONTROL See All]**。

   - 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL System]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Notifications]**。

1. 在&#x200B;**[!UICONTROL Action]**&#x200B;列中，执行以下任一操作：

   - 有关详细信息，请单击&#x200B;**[!UICONTROL Read Details]**&#x200B;以在新窗口中打开链接的页面。

   - 若要将邮件保留在收件箱中，请单击&#x200B;**[!UICONTROL Mark As Read]**。

     ![管理员 — 将所选通知标记为已读](./assets/admin-notifications-mark-as-read.png){width="700" zoomable="yes"}

   - 若要删除邮件，请单击&#x200B;**[!UICONTROL Remove]**。

1. 要将操作应用于多条消息，请执行以下操作之一：

   - 选中要管理的每个消息第一列中的复选框。
   - 要选择多个消息，请根据需要设置&#x200B;**[!UICONTROL Mass Actions]**&#x200B;控件。

1. 将&#x200B;**[!UICONTROL Actions]**&#x200B;控件设置为以下项之一：

   - `Mark as Read`
   - `Remove`

1. 单击&#x200B;**[!UICONTROL Submit]**&#x200B;以完成该过程。

## 配置通知

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧导航面板中，展开&#x200B;**[!UICONTROL Advanced]**&#x200B;并选择&#x200B;**[!UICONTROL System]**。

1. 展开![扩展选择器](../assets/icon-display-expand.png)的&#x200B;**[!UICONTROL Notifications]**&#x200B;部分。

   ![通知配置](./assets/system-notifications.png){width="600"}

1. 如果您的商店管理员在[安全URL](../stores-purchase/store-urls.md)上运行，请将&#x200B;**[!UICONTROL Use HTTPS to Get Feed]**&#x200B;设置为`Yes`。

1. 设置&#x200B;**[!UICONTROL Update Frequency]**&#x200B;以确定收件箱更新的频率。

   间隔可以是1到24小时。

1. 完成后，单击&#x200B;**[!UICONTROL Save Config]**。

有关[!UICONTROL System]配置选项的详细信息，请参阅&#x200B;[_配置参考指南_](../configuration-reference/advanced/system.md)。

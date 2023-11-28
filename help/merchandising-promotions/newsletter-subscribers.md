---
title: 管理新闻稿订阅者
description: 了解如何使用活动订阅的简单列表管理您的新闻稿订阅者。
exl-id: c7e8e642-e3fd-4979-9ea3-2d96839730b2
feature: Customers, Communications
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '499'
ht-degree: 0%

---

# 管理新闻稿订阅者

作为最佳实践，您应定期管理订阅列表，并确保处理任何取消订阅的请求。 在一些法域，法律规定取消订阅的请求在特定时间段内处理。

您可以使用活动订阅的简单列表轻松管理订阅者。 当客户提交取消订阅请求时，您只需应用 _取消订阅_ 一个或多个选定订阅的操作。

在具有多个商店视图的单站点设置中，客户帐户订阅可以与特定商店视图相关联。

在多商店和多站点设置中，使用全局 [客户帐户范围](../customers/customer-account-scope.md)，客户帐户可以订阅多个站点/商店的新闻稿。 在这种情况下，您可能需要编辑客户帐户以管理订阅组，或取消特定站点/商店的订阅以响应请求。

如果要使用第三方服务发送新闻稿，可以将订阅列表导出为CSV或XML文件。

## 管理客户的订阅

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. 在网格中查找客户并单击 **[!UICONTROL Edit]** 在 _[!UICONTROL Action]_列。

1. 单击 **[!UICONTROL Newsletter]** 在左侧面板中。

1. 根据您的网站/商店设置修改客户的订阅。

   对于单站点/单商店设置，您只需选择或清除 **[!UICONTROL Subscribed to Newsletter]** 复选框。

   ![“单商店客户新闻稿订阅”复选框](./assets/newsletter-customer-single-store.png){width="500" zoomable="yes"}

   对于单站点/多存储设置，您可以选择或清除 **[!UICONTROL Subscribed to Newsletter]** 复选框和设置 **[!UICONTROL Subscribed on Store View]** 到订阅的正确商店视图。

   ![多商店客户新闻稿订阅复选框和商店视图选择器](./assets/newsletter-customer-multi-store.png){width="500" zoomable="yes"}

   对于具有全局客户帐户范围的多站点/多商店设置，页面会显示所有站点的订阅状态。 您可以选择或清除 **[!UICONTROL Subscribed]** 复选框和/或更改 **[!UICONTROL Store View]** 用于订阅。

   ![多站点客户新闻稿订阅复选框和商店视图选择器](./assets/newsletter-customer-multi-site.png){width="500" zoomable="yes"}

1. 单击 **[!UICONTROL Save Customer]**.

## 从订阅者列表中取消订阅

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Newsletter Subscribers]**.

   对于多站点设置，如果某些客户具有多个站点的订阅，则每个订阅将作为行项目显示在网格中。

1. 在网格中查找订户，然后选中第一列中的复选框。

   >[!NOTE]
   >
   >要批量取消订阅，请选中要取消的每个订阅者的复选框。

1. 设置 _[!UICONTROL Action]_控制对象&#x200B;**[!UICONTROL Unsubscribe]**并单击&#x200B;**[!UICONTROL Submit]**.

   ![取消订阅新闻稿](./assets/newsletter-unsubscribe.png){width="600" zoomable="yes"}

   记录的状态更改为 `Unsubscribed`.

## 导出订阅者列表

1. 从 _[!UICONTROL Newsletter Subscribers]_列表时，使用过滤器控件以仅包含具有以下特征的记录：_&#x200B;状态&#x200B;_之 `Subscribed` 和以获取相应的网站、商店或商店视图。

1. 设置 **[!UICONTROL Export to]** 控制以下任一项：

   - `CSV`
   - `XML`

1. 单击 **[!UICONTROL Export]** 并查找屏幕底部的提示并保存文件。

   ![导出新闻稿订阅者](./assets/newsletter-subscribers-export.png){width="600" zoomable="yes"}

## 从订户列表中删除订户

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Newsletter Subscribers]**.

1. 在网格中查找订户，然后选中第一列中的复选框。

1. 设置 _[!UICONTROL Action]_控制对象&#x200B;**[!UICONTROL Delete]**并单击&#x200B;**[!UICONTROL Submit]**.

1. 提示确认时，单击 **[!UICONTROL OK]**.

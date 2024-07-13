---
title: 新闻稿队列
description: 了解如何管理新闻稿队列以发送多个新闻稿批次。
exl-id: bf85b3ff-3093-49a1-8a9a-d3ea71fe3f09
feature: Customers, Communications
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '342'
ht-degree: 0%

---

# 新闻稿队列

为了管理服务器上的负载，在多个批次的队列中发送具有多个订阅者的新闻稿。 您可以定期检查新闻稿队列以检查状态，并查看已处理的新闻稿数量。 传输期间发生的任何问题都会显示在&#x200B;_新闻稿问题_&#x200B;报告中。

## 发送新闻稿

1. 在&#x200B;_管理员_&#x200B;菜单上，转到&#x200B;**[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Newsletter Template]**。

1. 在网格中，查找要发送的[新闻稿模板](newsletter-template.md)，并将&#x200B;**[!UICONTROL Action]**&#x200B;列设置为`Queue Newsletter`。

1. 对于&#x200B;**[!UICONTROL Queue Date Start]**，从日历中选择传输开始日期（![日历图标](../assets/icon-calendar.png)）。

1. 对于&#x200B;**[!UICONTROL Subscribers From]**，请选择要包含在电子邮件爆炸中的每个商店视图。

1. 填写电子邮件标头信息：

   - 为电子邮件标头的&#x200B;**[!UICONTROL Subject]**&#x200B;行输入新闻稿的简短说明。

   - 输入&#x200B;**[!UICONTROL Sender Name]**。

   - 对于&#x200B;**[!UICONTROL Sender Email]**，输入发件人的电子邮件地址。

     发件人的默认名称和电子邮件地址在配置中指定。

     ![新闻稿队列信息](./assets/newsletter-queue-information1.png){width="600" zoomable="yes"}

1. 如果适用，请在说明上方的&#x200B;**[!UICONTROL Message]**&#x200B;框中输入注释以取消订阅。

   >[!NOTE]
   >
   >请勿删除这些指令，因为许多司法管辖区的法律都要求这样做。

1. 要将自定义样式应用于新闻稿，请将其添加到&#x200B;**[!UICONTROL Newsletter Styles]**&#x200B;字段。

1. 完成后，单击&#x200B;**[!UICONTROL Save and Resume]**。

   新闻稿会显示在等待处理的队列中。

## 检查问题

在&#x200B;_管理员_&#x200B;菜单上，转到&#x200B;**[!UICONTROL Reports]** > _[!UICONTROL Marketing]_>**[!UICONTROL Newsletter Problem Reports]**。

## 按钮栏

| 按钮 | 描述 |
|--- |--- |
| **[!UICONTROL Back]** | 返回到“新闻稿模板”页面而不保存更改。 |
| **[!UICONTROL Reset]** | 将队列信息表单中未保存的任何更改重置为其以前的值。 |
| **[!UICONTROL Preview Template]** | 在单独的选项卡中打开预览页面。 |
| **[!UICONTROL Save and Resume]** | 保存所有所做的更改。 将新闻稿放入队列。 |
| **[!UICONTROL Save Newsletter]** | 保存所有所做的更改。 将新闻稿放入队列。 |

{style="table-layout:auto"}

## 列

| 列 | 描述 |
|--- |--- |
| [!UICONTROL ID] | 分配给每个新闻稿模板的唯一数字标识符。 |
| [!UICONTROL Queue Start] | 发送新闻稿的日期。 |
| [!UICONTROL Queue End] | 新闻稿完成发送的日期。 |
| [!UICONTROL Subject] | 新闻稿模板的主题。 |
| [!UICONTROL Status] | 指示新闻稿邮件的状态。 可能的值： `Sent`、`Canceled`、`Not Sent`、`Sending`或`Paused`。 |
| [!UICONTROL Processed] | 指示发送了多少新闻稿。 |
| [!UICONTROL Recipients] | 指示订阅者已接收的新闻稿数量。 |
| [!UICONTROL Actions] | **[!UICONTROL Preview]**：打开一个单独的窗口来预览模板。 |

{style="table-layout:auto"}

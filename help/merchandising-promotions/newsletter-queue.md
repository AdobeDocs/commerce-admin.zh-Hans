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

为了管理服务器上的负载，在多个批次的队列中发送具有多个订阅者的新闻稿。 您可以定期检查新闻稿队列以检查状态，并查看已处理的新闻稿数量。 传输过程中出现的任何问题都将显示在 _新闻稿问题_ 报告。

## 发送新闻稿

1. 在 _管理员_ 菜单，转到 **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Newsletter Template]**.

1. 在网格中，查找 [新闻稿模板](newsletter-template.md) ，并设置 **[!UICONTROL Action]** 列至 `Queue Newsletter`.

1. 对象 **[!UICONTROL Queue Date Start]**，选择传输从日历开始的日期(![日历图标](../assets/icon-calendar.png))。

1. 对象 **[!UICONTROL Subscribers From]**，选择要包含在电子邮件爆炸中的每个商店视图。

1. 填写电子邮件标头信息：

   - 输入以下对象的新闻稿的简短说明： **[!UICONTROL Subject]** 电子邮件标头的行。

   - 输入 **[!UICONTROL Sender Name]**.

   - 对象 **[!UICONTROL Sender Email]**，输入发件人的电子邮件地址。

     发件人的默认名称和电子邮件地址在配置中指定。

     ![新闻稿队列信息](./assets/newsletter-queue-information1.png){width="600" zoomable="yes"}

1. 如果适用，请在 **[!UICONTROL Message]** 框中，取消订阅。

   >[!NOTE]
   >
   >请勿删除这些指令，因为许多司法管辖区的法律都要求这样做。

1. 要将自定义样式应用于新闻稿，请将其添加到 **[!UICONTROL Newsletter Styles]** 字段。

1. 完成后，单击 **[!UICONTROL Save and Resume]**.

   新闻稿会显示在等待处理的队列中。

## 检查问题

在 _管理员_ 菜单，转到 **[!UICONTROL Reports]** > _[!UICONTROL Marketing]_>**[!UICONTROL Newsletter Problem Reports]**.

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
| [!UICONTROL Status] | 指示新闻稿邮件的状态。 可能的值： `Sent`， `Canceled`， `Not Sent`， `Sending`，或 `Paused`. |
| [!UICONTROL Processed] | 指示发送了多少新闻稿。 |
| [!UICONTROL Recipients] | 指示订阅者已接收的新闻稿数量。 |
| [!UICONTROL Actions] | **[!UICONTROL Preview]**：打开单独的窗口以预览模板。 |

{style="table-layout:auto"}

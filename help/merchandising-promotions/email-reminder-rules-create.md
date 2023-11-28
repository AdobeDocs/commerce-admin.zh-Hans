---
title: 创建电子邮件提醒
description: 了解如何设置使用现有购物车价格规则的电子邮件提醒规则。
exl-id: b04dc8a3-5daa-43f2-bf52-d85bfd2554b7
feature: Merchandising, Communications
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '679'
ht-degree: 0%

---

# 创建电子邮件提醒

在设置电子邮件提醒规则之前，必须首先设置购物车价格规则以定义提供的促销。 触发电子邮件提醒的规则条件可以基于购物车属性、愿望清单属性或同时基于两者。

>[!NOTE]
>
>电子邮件提醒可能会促销包含或不包含优惠券的购物车价格规则。 定义自动生成优惠券的购物车价格规则为每个客户生成随机优惠券代码。

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Email Reminder Rules]**.

1. 在右上角，单击 **[!UICONTROL Add New Rule]**.

1. 完成 _[!UICONTROL Rule Information]_，如下所示：

   ![电子邮件提醒规则](./assets/email-reminder-new.png){width="700" zoomable="yes"}

   - 输入 **[!UICONTROL Rule Name]** 以在内部标识规则。

   - 输入摘要 **[!UICONTROL Description]** 规则的。

   - 选择 **[!UICONTROL Cart Price Rule]** 要提醒的促销活动，请单击 **[!UICONTROL Select Rule…]**，然后选择规则。

     ![购物车规则 — 选择](./assets/email-reminder-select-rule.png){width="600" zoomable="yes"}

   - 如果希望规则立即生效，请设置 **[!UICONTROL Status]** 到 `Active`.

   - 要设置规则生效的日期范围，请输入 **[!UICONTROL From]** 和 **[!UICONTROL To]** 日期。

     您还可以从日历( ![日历图标](../assets/icon-calendar.png) )。

   - 要多次发送提醒，请在 **[!UICONTROL Repeat Schedule]** 字段。

1. 在左侧的面板中，选择 **[!UICONTROL Conditions]**.

   必须为规则定义至少一个条件。 该过程类似于构建 [目录价格规则。](price-rules-catalog.md)

   ![电子邮件提醒条件](./assets/email-reminder-conditions.png){width="600" zoomable="yes"}

   单击 _添加_ ( ![“添加”图标](../assets/icon-add-green-circle.png))以显示选项列表，然后选择以下条件之一：

   - 愿望清单
   - 购物车

   >[!NOTE]
   >
   >如果客户有多个匹配的放弃购物车、愿望清单或两者的组合，则仅为该客户触发一次电子邮件提醒。 要再次触发相同的电子邮件提醒，请使用 _[!UICONTROL Repeat Schedule]_用于设置电子邮件间隔天数的字段。

   完成条件以描述触发电子邮件提醒的情况。

   ![电子邮件提醒条件示例](./assets/email-reminder-condition-example.png){width="600" zoomable="yes"}

1. 在左侧的面板中，选择 **[!UICONTROL Emails and Labels]**.

   ![电子邮件提醒规则 — 电子邮件和标签模板 ](./assets/email-reminder-rule-emails-labels-email-templates.png){width="600" zoomable="yes"}

1. 在 **[!UICONTROL Email Templates]** 部分，选择要用于您网站和商店视图的电子邮件模板 [存储层级](../getting-started/websites-stores-views.md).

   如果您不想向商店视图的客户发送提醒电子邮件，请保留值 `Not Selected`.

1. 在 _默认标题和描述_ 部分，执行以下操作：

   - 输入 **[!UICONTROL Rule Title for All Store Views]**.

     >[!NOTE]
     >
     >通过使用，可将此值并入电子邮件模板 `promotion_name` 变量。

   - 输入 **[!UICONTROL Rule Description for All Store Views]**.

     ![电子邮件提醒 — 标题和描述](./assets/email-reminders-emails-and-labels-default-titles-description.png){width="500" zoomable="yes"}

   - 在 _[!UICONTROL Titles and Descriptions Per Store View]_部分，输入&#x200B;**[!UICONTROL Rule Title]**和&#x200B;**[!UICONTROL Description]**对于_&#x200B;默认存储视图&#x200B;_. 对于多个商店视图，请为每个商店视图输入相应的标题和描述。

     >[!NOTE]
     >
     >通过使用promotion_description变量，可以将描述并入电子邮件模板中。

     ![标题和描述 — 商店视图](./assets/email-reminder-rules-title-descriptions-per-store-view.png){width="500" zoomable="yes"}

1. 完成后，单击 **[!UICONTROL Save]**.

## 触发条件

| 来源 | 触发器 |
|--- |--- |
| [!UICONTROL Wish List] | [!UICONTROL Conditions Combination]<br/>[!UICONTROL Sharing]<br/>[!UICONTROL Number of Items]<br/>[!UICONTROL Items Sub selection] |
| [!UICONTROL Shopping Cart] | [!UICONTROL Conditions Combination]<br/>[!UICONTROL Coupon Code]<br/>[!UICONTROL Cart Line Items]<br/>[!UICONTROL Items Quantity]<br/>[!UICONTROL Virtual Only]<br/>[!UICONTROL Total Amount]<br/>[!UICONTROL Items Subselection] |

{style="table-layout:auto"}

## 字段描述

| 字段 | 描述 |
|--- |--- |
| [!UICONTROL Rule Name] | 自动提醒规则的名称在内部标识该规则。 |
| [!UICONTROL Description] | 供内部参考的规则的描述。 |
| [!UICONTROL Shopping Cart Price Rule] | 与此电子邮件提醒关联的购物车规则。 提醒电子邮件可以促销带有或不带有优惠券的购物车价格规则。 如果购物车价格规则包括自动生成的优惠券，则提醒规则为每个客户生成随机、唯一的优惠券代码。 |
| [!UICONTROL Assigned to Website] | 基于此规则接收自动提醒电子邮件的网站。 |
| [!UICONTROL Status] | 激活规则。 如果状态为非活动，则忽略所有其他设置，并且不触发规则。 选项： `Active` / `Inactive` |
| [!UICONTROL From Date] | 此自动提醒规则的开始日期。 如果未指定日期，则规则将立即处于活动状态。 |
| [!UICONTROL To Date] | 此自动提醒规则的结束日期。 如果未指定日期，则规则将无限期地处于活动状态。 |
| [!UICONTROL Repeat Schedule] | 触发规则前的天数，以及在满足条件的情况下再次发送提醒电子邮件。 要多次触发规则，请输入下次发送电子邮件前的天数（以逗号分隔）。 例如，输入 `7` 7天后再次触发规则；输入 `7,14` 7天后触发规则，14天后再次触发。 |
| [!UICONTROL Email Templates] | 确定用于每个商店视图的电子邮件模板。 |
| [!UICONTROL Rule Title for All Store Views] | 确定每个商店视图的规则标题。 |
| [!UICONTROL Rule Description for All Store Views] | 确定每个存储视图的规则描述。 |

{style="table-layout:auto"}

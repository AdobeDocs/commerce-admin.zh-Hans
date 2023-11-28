---
title: ’[!UICONTROL Customers] &gt； [!UICONTROL Promotions]’
description: 查看 [!UICONTROL Customers] &gt； [!UICONTROL Promotions] 商务管理员页面。
exl-id: 93035d46-2e9e-466d-a5e3-d69ce6b662b8
feature: Configuration, Promotions/Events
source-git-commit: 76bd1b1af9b55d69bd98209d70fb5518f190a3e1
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 0%

---

# [!UICONTROL Customers] > [!UICONTROL Promotions]

{{config}}

## [!UICONTROL Automated Email Reminder Rules]

{{ee-feature}}

![自动电子邮件提醒规则](./assets/promotions-automated-email-reminder-rules.png)<!-- zoom -->

<!-- [Automated Email Reminder Rules](https://docs.magento.com/user-guide/marketing/email-reminder-rules-configure.html) -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Enable Reminder Emails] | 全局 | 启用自动电子邮件提醒。 如果将此选项设置为“否”，则会忽略其余设置。 选项： `Yes` / `No` |
| [!UICONTROL Frequency] | 全局 | 指示Commerce应检查符合自动电子邮件提醒条件的新客户的频率。 选项： <br/>**`Minute Intervals`**— 根据所选时间间隔发送电子邮件。 （5分钟、10分钟、15分钟、20分钟或30分钟）<br/>**`Hourly`**  — 每小时发送一次电子邮件，在指定的小时后的某一分钟发送。 输入一个介于0-59之间的值。 <br/>**`Daily`**— 从开始时间起，每天发送电子邮件。 |
| [!UICONTROL Interval] | 全局 | 间隔应等于或大于cron.php启动周期。 选项： `5 minutes` / `10 minutes` / `15 minutes` / `20 minutes` / `30 minutes` |
| [!UICONTROL Start Time] | 全局 | 设置发送电子邮件的日期、分钟和秒数。 根据服务器上的系统时间，以24小时制指定。 |
| [!UICONTROL Maximum Emails per One Run] | 全局 | 限制在计划块中发送的电子邮件数。 |
| [!UICONTROL Email Send Failure Threshold] | 全局 | 提醒尝试将通知发送到特定电子邮件地址并失败的次数。 将该值设置为0时，没有阈值，即使发生任何故障，仍将继续发送通知。 |
| [!UICONTROL Reminder Email Sender] | 商店视图 | 显示为电子邮件发件人的商店标识。 |

{：style=&quot;table-layout：auto&quot;}

## [!UICONTROL Auto Generated Specific Coupon Codes]

![自动生成的特定优惠券代码](./assets/promotions-auto-generated-specific-coupon-codes.png)<!-- zoom -->

<!-- [Auto Generated Specific Coupon Codes](https://docs.magento.com/user-guide/marketing/price-rules-cart-coupon-code-configure.md  -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Code Length] | 全局 | 定义优惠券代码的长度，不包括前缀、后缀和分隔符。 |
| [!UICONTROL Code Format] | 全局 | 定义优惠券代码格式。 选项包括： <br/>**`Alphanumeric`**— 字母和数字的任意组合。<br/>**`Alphabetical`**  — 仅限字母。 <br/>**`Numeric`**— 仅限数字。 |
| [!UICONTROL Code Prefix] | 全局 | 附加到所有优惠券代码开头的值。 如果您不想使用前缀，请将该字段留空。 |
| [!UICONTROL Code Suffix] | 全局 | 附加到所有代码末尾的值。 如果不想使用后缀，请将该字段留空。 |
| [!UICONTROL Dash Every X Characters] | 全局 | 在所有优惠券代码中插入破折号(-)的间隔。 如果不想使用破折号，请将该字段留空。 <br/>_**注意：**_ 只有短划线不同的优惠券代码被视为不同的代码。 |

{：style=&quot;table-layout：auto&quot;}

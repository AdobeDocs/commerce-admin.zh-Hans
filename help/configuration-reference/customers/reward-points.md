---
title: '[!UICONTROL Customers] &amp；gt； [!UICONTROL Reward Points]'
description: 查看Commerce管理员的[!UICONTROL Customers] &amp；gt； [!UICONTROL Reward Points]页面上的配置设置。
exl-id: 0b7f8806-74c5-4467-87da-0faae50f164b
feature: Configuration, Rewards
source-git-commit: 5a4417373f6dc720e8e14f883c27348a475ec255
workflow-type: tm+mt
source-wordcount: '781'
ht-degree: 0%

---

# [!UICONTROL Customers] > [!UICONTROL Reward Points]

{{ee-feature}}

{{config}}

>[!NOTE]
>
>在结帐期间客户和管理员兑换奖励积分需要[奖励汇率](../../merchandising-promotions/reward-exchange-rates.md)配置。

## [!UICONTROL Reward Points]

![奖励积分](./assets/reward-points-reward-points.png)<!-- zoom -->

<!-- [Reward Points](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/merchandising/reward-points/rewards-loyalty#enable-reward-point-operations-for-your-store) -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable Reward Points Functionality] | 全局 | 激活或停用奖励积分。 选项： `Yes` / `No`。 |
| [!UICONTROL Enable Reward Points Functionality on Storefront] | 网站 | 启用后，客户可以通过其活动获得点数，并在结账时兑换点数。 如果禁用，则只有管理员用户可以代表客户分配和兑换点数。 选项： `Yes` / `No`。 |
| [!UICONTROL Customers May See Reward Points History] | 网站 | 启用后，客户可以在帐户控制面板中查看每个应计、赎回和奖励积分到期的详细历史记录。 选项： `Yes` / `No` |
| [!UICONTROL Reward Points Balance Redemption Threshold] | 网站 | 要求客户达到最低点余额，然后才能将其兑换为订单。 保留为空则没有最小值。 |
| [!UICONTROL Cap Reward Points Balance At] | 网站 | 防止客户应计超过此最大点数余额。 留空表示没有最大值。 |
| [!UICONTROL Reward Points Expire in (days)] | 网站 | 指示奖励分数的生命周期（以天为单位）。 在单独的活动中获得的每批积分都具有单独的生命周期。 奖励积分历史记录中的每一批均指示积分到期前的剩余天数。 可以从客户的帐户仪表板（如果已启用）和管理员查看历史记录。 留空表示无过期时间。 |
| [!UICONTROL Reward Points Expiry Calculation] | 网站 | 确定用于确定奖励积分何时过期的方法。 选项： <br/>**`Static`**— 根据配置中设置的天数确定奖励积分的剩余生命周期。 如果配置中的到期限制更改，则现有点的到期日期不会更改。<br/>**`Dynamic`** — 计算奖励点余额增加时剩余的天数。 如果配置中的到期限制发生更改，则将相应地更新所有现有点的到期计算。 |
| [!UICONTROL Refund Reward Points Automatically] | 全局 | 确定是否自动退款可用的奖励积分。 选项： `Yes` / `No` |
| [!UICONTROL Deduct Reward Points from Refund Amount Automatically] | 全局 | 此功能可确定在启用此功能后，通过采购获得的奖励积分在订单退款时是否全部或部分失效。 只有获得奖励的订单中的奖励积分在该订单退款时才会受到影响。 选项： `Yes` / `No`。 |
| [!UICONTROL Landing Page] | 商店视图 | 指定用于说明您的奖励积分计划的CMS页面。 指向默认“奖励”页面的链接将显示在商店中可获得点数的位置。 |

{style="table-layout:auto"}

## [!UICONTROL Actions for Acquiring Reward Points by Customers]

![客户获取奖励积分的操作](./assets/reward-points-actions-for-acquiring.png)<!-- zoom -->

<!-- [Actions for Acquiring Reward Points by Customers](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/merchandising/reward-points/rewards-loyalty#enable-reward-point-operations-for-your-store) -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Purchase] | 网站 | 确定是否根据配置的[奖励汇率](../../merchandising-promotions/reward-exchange-rates.md)为购买获得奖励积分。 选项： `Yes` / `No` |
| [!UICONTROL Registration] | 网站 | 指定开立客户帐户获得的点数。 |
| [!UICONTROL Newsletter Signup] | 网站 | 指定订阅新闻稿的注册客户获得的点数。 （访客的订阅没有积分。） 如果客户取消订阅，然后再次订阅，则不会为第二个订阅获得积分。 |
| [!UICONTROL Converting Invitation to Customer] | 网站 | 指定发送邀请的客户在收件人随后打开客户帐户时获得的点数。 |
| [!UICONTROL Invitation to Customer Conversions Quantity Limit] | 网站 | 限制可用于为发送邀请的客户获取点数的邀请转换次数。 保留为空表示无限制。 |
| [!UICONTROL Converting Invitation to Order] | 网站 | 指定在收件人下达初始订单时发送邀请的客户获得的点数。 |
| [!UICONTROL Invitation to Order Conversions Quantity Limit] | 网站 | 限制可为发送邀请的人员获取点数的订单转换次数。 如果为空，则没有最大限制。 |
| [!UICONTROL Invitation Conversion to Order Reward] | 网站 | 指示受邀者进行购买时客户获得奖励积分的频率。 选项： <br/>**`Each`**— 客户会收到被邀请者下每个开票订单的奖励积分。 奖励积分乃根据网站及客户群所需组合之汇率厘定。<br/>**`First`** — 客户仅会收到被邀请者下达的第一个开票订单的奖励积分。 如果有多位被邀请者注册并下订单，则只有第一笔订单的金额会转换为奖励积分并授予客户。 |
| [!UICONTROL Review Submission] | 网站 | 确定提交审核且已批准发布的客户获得的点数。 |
| [!UICONTROL Rewarded Reviews Submission Quantity Limit] | 网站 | 限制可用于为每个客户获取点数的评论数量。 保留为空表示无限制。 |

{style="table-layout:auto"}

## [!UICONTROL Email Notification Settings]

![电子邮件通知设置](./assets/reward-points-email-notification-settings.png)<!-- zoom -->

<!-- [Email Notification Settings](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/merchandising/reward-points/rewards-loyalty#enable-reward-point-operations-for-your-store) -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Email Sender] | 商店视图 | 确定显示为余额更新和到期通知电子邮件发件人的商店联系人。 |
| [!UICONTROL Subscribe Customers by Default] | 全局 | 确定客户在余额更新和过期通知电子邮件中的默认订阅状态。 |
| [!UICONTROL Balance Update Email] | 商店视图 | 确定在客户点数余额更新时发送给客户的通知所使用的模板。 默认模板： `Reward Points Balance Update` |
| [!UICONTROL Reward Points Expiry Warning Email] | 商店视图 | 确定当达到一批点的到期警告限制时客户收到的电子邮件模板。 默认模板： `Reward Points Expiry Warning` |
| [!UICONTROL Expiry Warning before (days)] | 全局 | 指定在点到期之前发送通知的天数。 留空将不发送过期通知。 如果输入的天数大于点的剩余生命周期，则不会发送通知。 |

{style="table-layout:auto"}

---
title: 奖励和忠诚计划
description: 了解可用于提高客户参与度和客户忠诚度的奖励积分系统。
exl-id: 2bccdcce-7936-4449-9634-d463ad29e5cc
feature: Rewards, Promotions/Events, Customers, Configuration
source-git-commit: f8254db7d69e58c8e9a78948ee6e40f5ea88cea0
workflow-type: tm+mt
source-wordcount: '1389'
ht-degree: 0%

---

# 奖励和忠诚计划

{{ee-feature}}

Adobe Commerce中的&#x200B;_奖励积分_&#x200B;系统允许您实施独特的计划，以提高客户参与度并提高客户忠诚度。 可以为广泛的交易和客户活动授予积分，并且可以设置配置来控制积分分配、平衡和到期。 客户可以根据您在奖励点数和货币之间建立的兑换率将点数兑换为购买商品。

## 购物车价格规则

积分可根据[购物车规则](price-rules-cart.md)奖励客户。 它们可以按价格规则的唯一动作获得奖励，也可以附带折扣。

## 客户余额

管理员用户可为每位客户管理奖励点余额。 如果在店面中启用，客户还可以查看其积分余额的详细信息。

## 兑换点

>[!NOTE]
>
>在结帐期间客户和管理员用户兑换奖励积分需要[奖励汇率](reward-exchange-rates.md)配置。

在结账过程中，管理员用户和客户（如果已启用）可以兑换积分。 在“付款方法”部分，已启用的付款方法上方将显示一个使用我的奖励积分复选框。 包括可用点数和货币汇率。 如果可用余额大于订单的总计，则无需其他付款方式。 应用于订单的奖励积分数与订单总额一起显示（从总计中扣除），类似于商店信用卡或礼品卡。 如果奖励积分与商店信用卡或礼品卡一起使用，则首先扣除奖励积分。 如果订单总额大于可兑换的奖励点数，则扣减商店信用卡或礼品卡。

>[!NOTE]
>
>不建议将奖励积分用于COD采购，因为只有在订单开票后才能确认付款收据。

## 退回奖励积分

带有奖励积分的订单可以退回到奖励积分余额，直至订单中赎回的金额。 在&#x200B;[_新贷项通知单_&#x200B;页](../stores-purchase/credit-memo-create.md)上，可以输入应用于客户余额的点数。 默认情况下，字段包含按顺序使用的完整点数。

## 启用商店的奖励点操作

奖励点配置确定奖励点在商店中的呈现方式并定义基本操作参数。

![客户配置 — 奖励积分](../configuration-reference/customers/assets/reward-points-reward-points.png){width="600" zoomable="yes"}

### 步骤1. 配置奖励积分

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧面板中，展开&#x200B;**[!UICONTROL Customers]**&#x200B;并选择&#x200B;**[!UICONTROL Reward Points]**。

1. 展开&#x200B;**[!UICONTROL Reward Points]**&#x200B;部分中的![扩展选择器](../assets/icon-display-expand.png)并执行以下操作：

   - 要激活奖励积分，请将&#x200B;**[!UICONTROL Enable Reward Points Functionality]**&#x200B;设置为`Yes`。

   - 若要允许客户获得自己的奖励积分，请将&#x200B;**[!UICONTROL Enable Reward Points Functionality on Storefront]**&#x200B;设置为`Yes`。

   - 若要允许客户查看其奖励的详细历史记录，请将&#x200B;**[!UICONTROL Customers May See Reward Point History]**&#x200B;设置为`Yes`。

1. 对于&#x200B;**[!UICONTROL Reward Points Balance Redemption Threshold]**，输入兑换前必须累积的点数（无最小值为空白）。

1. 对于&#x200B;**[!UICONTROL Cap Reward Points Balance At]**，输入客户可以累积的最大点数（空白表示无限制）。

1. 对于&#x200B;**[!UICONTROL Reward Points Expire in (days)]**，输入奖励积分过期前的天数（无过期则为空）。

1. 将&#x200B;**[!UICONTROL Reward Points Expiry Calculation]**&#x200B;设置为以下项之一：

   - `Static` — 根据配置中设置的天数确定奖励分数的剩余生命周期。 如果配置中的到期限制更改，则现有点的到期日期不会更改。

   - `Dynamic` — 计算奖励点余额增加时的剩余天数。 如果配置中的到期限制发生更改，则所有现有点的到期都将相应地更新。

1. 如果要自动退款可用的奖励积分，请将&#x200B;**[!UICONTROL Refund Reward Points Automatically]**&#x200B;设置为`Yes`。

1. 要在获得积分的订单已全部或部分退款时撤消通过购买获得的奖励积分，请将&#x200B;**[!UICONTROL Deduct Reward Points from Refund Amount Automatically]**&#x200B;设置为`Yes`。

   >[!NOTE]
   >
   >只有通过正在退款的订单获得的点数会受到影响。

1. 将&#x200B;**[!UICONTROL Landing Page]**&#x200B;设置为说明您的奖励积分计划的内容页面。

   确保使用您自己的信息更新默认的“奖励积分”页面。

1. 完成后，单击&#x200B;**[!UICONTROL Save Config]**。

### 步骤2. 配置客户活动获得的点数

在此步骤中，指定可为各种客户活动获得的奖励积分数。 当客户完成分配了点的活动时，将会向客户显示一条消息，指明他们已获得多少点。

1. 展开&#x200B;**[!UICONTROL Actions for Acquiring Reward Points by Customer]**&#x200B;部分的![扩展选择器](../assets/icon-display-expand.png)。

   ![客户配置 — 客户获取奖励积分的操作](../configuration-reference/customers/assets/reward-points-actions-for-acquiring.png){width="600" zoomable="yes"}

1. 若要允许根据配置的[奖励汇率](reward-exchange-rates.md)为购买获得奖励积分，请将&#x200B;**[!UICONTROL Purchase]**&#x200B;设置为`Yes`。

   >[!NOTE]
   >
   >若要获得其&#x200B;_前_&#x200B;订单的奖励积分，客户必须在&#x200B;_前_&#x200B;通过付款方式获取交易之前注册。 大多数付款方式都可以配置为在下订单时&#x200B;_自动_&#x200B;捕获交易记录，但&#x200B;_在_&#x200B;之前，客户帐户注册已完成。

1. 对于&#x200B;**[!UICONTROL Registration]**，输入开立客户帐户获得的点数。

1. 对于&#x200B;**[!UICONTROL Newsletter Signup]**，输入订阅新闻稿的注册客户获得的点数。

1. 对于&#x200B;**[!UICONTROL Converting Invitation to Customer]**，输入发送邀请的客户获得的点数，然后收件人打开客户帐户。

   您可以限制为发送邀请的客户获取点数的邀请转换次数（无限制为空白）。 为此，请在&#x200B;**[!UICONTROL Invitation to Customer Conversions Quantity Limit]**&#x200B;字段中输入一个数字。

1. 对于&#x200B;**[!UICONTROL Converting Invitation to Order]**，输入客户获得的点数，该客户向收件人发送邀请函，收件人随后下达订单，然后执行以下操作：

   - 对于&#x200B;**订单转化邀请数量限制**，输入收件人下达初始订单时发送邀请的客户获得的点数（空白表示无限制）。

   - 对于&#x200B;**[!UICONTROL Invitation Conversion to Order Reward]**，选择`Each`选项以获得收件人订单每次下单的点数，或选择`First`选项以仅获得收件人首次下单的订单点数。

1. 对于&#x200B;**[!UICONTROL Review Submission]**，输入提交审核且已批准发布的客户获得的点数。

1. 然后，要限制可用于获得每位客户点数的评论数量，请在&#x200B;**[!UICONTROL Rewarded Reviews Submission Quantity Limit]**&#x200B;字段中输入数字（空白表示无限制）。

1. 完成后，单击&#x200B;**[!UICONTROL Save Config]**。

### 步骤3. 完成电子邮件通知设置

1. 展开&#x200B;**[!UICONTROL Email Notification Settings]**&#x200B;部分的![扩展选择器](../assets/icon-display-expand.png)。

   ![客户配置 — 奖励点数电子邮件通知](../configuration-reference/customers/assets/reward-points-email-notification-settings.png){width="600" zoomable="yes"}

1. 将&#x200B;**[!UICONTROL Email Sender]**&#x200B;设置为显示为余额更新和到期通知发送者的商店联系人。

1. 如果您要订阅客户，以接收余额更新和即将到期日期的通知，请将&#x200B;**[!UICONTROL Subscribe Customers by Default]**&#x200B;设置为`Yes`。

1. 将&#x200B;**[!UICONTROL Balance Update Email]**&#x200B;设置为每次更新积分余额时发送给客户的通知所使用的模板。

1. 将&#x200B;**[!UICONTROL Reward Points Expiry Warning Email]**&#x200B;设置为在达到点批次的到期限制时发送给客户的通知所使用的模板。

1. 对于&#x200B;**[!UICONTROL Expiry Warning Before (days)]**，输入发送该通知的点数过期前的天数。

1. 完成后，单击&#x200B;**[!UICONTROL Save Config]**。

## 更新奖励积分余额

奖励积分余额可以从管理员更新。

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Customers]** > **[!UICONTROL All Customers]**。

1. 在网格中查找客户，然后单击&#x200B;_[!UICONTROL Action]_&#x200B;列中的&#x200B;**[!UICONTROL Edit]**。

1. 在&#x200B;_客户信息_&#x200B;下，选择&#x200B;**[!UICONTROL Reward Points]**&#x200B;部分。

1. 输入&#x200B;**[!UICONTROL Update Points]**&#x200B;的数字：

   - 要更新奖励积分金额，请输入数字以增加总积分余额。
   - 要减去奖励积分金额，请输入要减少总积分余额的负数。

1. 如果需要，请输入与奖励积分调整相关的&#x200B;**[!UICONTROL Comments]**。

   ![奖励积分余额](./assets/reward-points-balance.png){width="700" zoomable="yes"}

1. （可选）为客户订阅&#x200B;_奖励积分通知_：

   - **[!UICONTROL Subscribe for Balance Updates]**
   - **[!UICONTROL Subscribe for Points Expiration Notifications]**

1. 单击&#x200B;**[!UICONTROL Save Customer]**。

与奖励积分相关的所有操作都会显示在店面客户帐户中的&#x200B;_[!UICONTROL Reward Points History]_&#x200B;块中。

## 字段描述

| 字段 | 描述 |
|--- |--- |
| [!UICONTROL Balance] | 客户奖励积分的当前余额 |
| [!UICONTROL Amount Balance] | 当前现金余额的金额 |
| [!UICONTROL Points] | 添加或减去的点数 |
| [!UICONTROL Amount] | 加减货币金额 |
| [!UICONTROL Rate] | [奖励汇率](reward-exchange-rates.md) |
| [!UICONTROL Website] | 将奖励点历史记录分配到的网站 |
| [!UICONTROL Reason] | 积分原因：<br>**[!UICONTROL Making purchases]**— 客户每次购买时都可以获得积分。<br>**[!UICONTROL Registering on the site]** — 注册时累计（一次）。<br>**[!UICONTROL Subscribing to a newsletter]**— 首次订阅应计（一次）。<br>**[!UICONTROL Sending Invitations]** — 通过邀请朋友加入网站来获得点数。<br>**[!UICONTROL Converting Invitations to Customer]**— 每次发出邀请时都能获得点数，在网站上注册的主要朋友。<br>**[!UICONTROL Converting Invitations to Order]** — 每次销售获得发送邀请的积分。<br>**[!UICONTROL Review Submission]**— 获得提交产品评论的积分。 |
| [!UICONTROL Created] | 奖励积分更新的日期和时间 |
| [!UICONTROL Expired] | 已过期的奖励积分数 |
| [!UICONTROL Comment] | 添加或减去点时的注释 |

{style="table-layout:auto"}

## 资源疑难解答

有关排查奖励点问题的帮助，请参阅以下Commerce支持知识库文章：

- [404错误 — 正在删除多送货结帐的奖励点](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/storefront/magento-2.4.0-404-error-removing-rewards-points-on-multi-shipping-checkout.html?lang=zh-Hans)

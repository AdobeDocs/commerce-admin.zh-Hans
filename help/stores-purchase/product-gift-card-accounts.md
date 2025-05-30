---
title: 礼品卡帐户
description: 了解礼品卡帐户以及如何配置代码池管理的默认设置。
exl-id: f8caff04-38fd-4195-ab11-77dae900976d
feature: Products, Gift, Configuration
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '934'
ht-degree: 0%

---

# 礼品卡帐户

系统会自动为每个购买的礼品卡创建礼品卡帐户。 然后，礼品卡的价值可用于购买您商店中的产品。 您还可以从管理员创建礼品卡帐户，作为客户的促销或服务。 礼品卡帐号对应于礼品卡代码。

![礼品卡帐户](./assets/marketing-gift-card-accounts-grid.png){width="700" zoomable="yes"}

## 配置礼品卡帐户

礼品卡配置将为商店视图的所有礼品卡建立默认设置，并管理代码池。 代码池是特定格式的一组唯一礼品卡代码。 每次创建礼品卡帐户时，都会使用池中的代码。 商店管理员有责任确保有足够的代码可供礼品卡销售。 在提供礼品卡销售之前，请确保生成代码池。 默认情况下，Adobe Commerce会生成1,000个代码。 在当前池中没有更多可用代码之前，不会生成新的代码池。

### 步骤1：配置电子邮件通知

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧面板中，展开&#x200B;**[!UICONTROL Sales]**&#x200B;并选择&#x200B;**[!UICONTROL Gift Cards]**。

1. 展开&#x200B;_[!UICONTROL Gift Card Email Settings]_&#x200B;部分中的![扩展选择器](../assets/icon-display-expand.png)并执行以下操作：

   - 将&#x200B;**[!UICONTROL Gift Card Notification Email Sender]**&#x200B;设置为显示为礼品卡通知发送者的商店标识。

   - 将&#x200B;**[!UICONTROL Gift Card Notification Email Template]**&#x200B;设置为用于通知的模板。

   ![礼品卡电子邮件设置](../configuration-reference/sales/assets/gift-cards-gift-card-email-settings.png){width="600" zoomable="yes"}

1. 展开&#x200B;_[!UICONTROL Email Sent from Gift Card Account Management]_&#x200B;部分中的![扩展选择器](../assets/icon-display-expand.png)并执行以下操作：

   - 将&#x200B;**[!UICONTROL Gift Card Email Sender]**&#x200B;设置为要显示为礼品卡发送者的商店标识。

   - 将&#x200B;**[!UICONTROL Gift Card Template]**&#x200B;设置为要用于礼品卡的模板。

有关特定配置字段和选项，请参阅[存储电子邮件地址](../configuration-reference/general/store-email-addresses.md)。

### 第2步：完成常规设置

1. 展开&#x200B;_[!UICONTROL Gift Card General Settings]_&#x200B;部分的![扩展选择器](../assets/icon-display-expand.png)。

1. 若要允许客户兑换卡上的值以换取现金，请将&#x200B;**[!UICONTROL Redeemable]**&#x200B;设置为`Yes`。

1. 对于&#x200B;**[!UICONTROL Lifetime (days)]**，输入卡片过期前的天数。

   如果没有到期日期，请将该字段留空。

   >[!NOTE]
   >
   >根据您所在的位置，礼品卡过期可能是非法的。 在为礼品卡设置生命周期之前，请查看您当地的法律。

1. 若要让客户可以选择输入邮件以随礼品卡一起发送，请将&#x200B;**[!UICONTROL Allow Gift Message]**&#x200B;设置为`Yes`，并输入&#x200B;**[!UICONTROL Gift Message Maximum Length]**&#x200B;的邮件可用字符数。

1. 将&#x200B;**[!UICONTROL Generate Gift Card Account when Orders Item is]**&#x200B;设置为以下项之一：

   - `Ordered` — 在下订单时创建礼品卡帐户。
   - `Invoiced` — 在捕获付款并对订单开票后创建礼品卡帐户。

   ![礼品卡常规设置](../configuration-reference/sales/assets/gift-cards-gift-card-general-settings.png){width="600" zoomable="yes"}

### 步骤3：建立礼品卡代码池

1. 展开&#x200B;_[!UICONTROL Gift Card Account General Settings]_&#x200B;部分中的![扩展选择器](../assets/icon-display-expand.png)并执行以下操作：

   ![礼品卡帐户常规设置](../configuration-reference/sales/assets/gift-cards-gift-card-account-general-settings.png){width="600" zoomable="yes"}

   - 要自定义代码，请根据您的喜好完成以下操作：

      - 代码长度
      - 代码格式
      - 代码前缀
      - 代码后缀
      - 将每X个字符破折号

   - 要确定要生成的代码数，请输入&#x200B;**[!UICONTROL New Pool Size]**。

   - 要指定您何时收到通知以重新补充代码池，请输入&#x200B;**[!UICONTROL Low Code Pool Threshold]**。

1. 在生成代码池之前，单击&#x200B;**[!UICONTROL Save Config]**。

1. 单击&#x200B;**[!UICONTROL Generate]**。

1. 完成后，单击&#x200B;**[!UICONTROL Save Config]**。

## 检查现有的礼品卡帐户

1. 要查找当前订单的礼品卡帐户编号，请执行以下操作：

   - 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**。

   - 在列表中查找该顺序，然后单击&#x200B;_[!UICONTROL Action]_&#x200B;列中的&#x200B;**[!UICONTROL View]**。

   - 向下滚动到&#x200B;_[!UICONTROL Items Ordered]_&#x200B;部分。

   该数字位于&#x200B;**[!UICONTROL Gift Card Accounts]**&#x200B;下的&#x200B;_[!UICONTROL Product]_&#x200B;列中。

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Gift Card Accounts]**。

1. 在网格中找到礼品卡帐户，并在编辑模式下将其打开。

   礼品卡代码显示在&#x200B;_信息_&#x200B;部分的顶部。

   ![礼品卡帐户信息](./assets/gift-card-account-information.png){width="600" zoomable="yes"}

## 创建礼品卡帐户

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Gift Card Accounts]**。

1. 单击右上角的&#x200B;**[!UICONTROL Add Gift Card Account]**。

1. 在&#x200B;_[!UICONTROL Information]_&#x200B;部分中，将&#x200B;**[!UICONTROL Active]**&#x200B;设置为`Yes`并执行以下操作：

   - 若要使卡余额可在结账时兑换或转移到客户的商店贷方，请将&#x200B;**[!UICONTROL Redeemable]**&#x200B;设置为`Yes`。

   - 选择可以使用礼品卡帐户的&#x200B;**[!UICONTROL Website]**。

   - 输入礼品卡上的初始&#x200B;**[!UICONTROL Balance]**。

   - _（可选）_&#x200B;要为礼品卡设置&#x200B;**[!UICONTROL Expiration Date]**，请从日历![日历图标](../assets/icon-calendar.png)中选择日期。

     如果留空，礼品卡帐户将不会过期。

     ![新帐户](./assets/gift-card-account-add-new.png){width="600" zoomable="yes"}

1. 在左侧面板中，选择&#x200B;**[!UICONTROL Send Gift Card]**&#x200B;并执行以下操作：

   - 输入&#x200B;**[!UICONTROL Recipient Email]**&#x200B;地址。

   - 输入&#x200B;**[!UICONTROL Recipient Name]**。

   - 将&#x200B;**[!UICONTROL Send Email from the Following Store View]**&#x200B;设置为显示为礼品卡通知发送者的商店视图。

   ![发送礼品卡设置](./assets/marketing-gift-card-accounts-new-send.png){width="600" zoomable="yes"}

1. 执行以下操作之一以保存新帐户：

   - 如果您尚未准备好发送礼品卡，请单击&#x200B;**[!UICONTROL Save]**。

   - 若要保存更改并通过电子邮件将礼品卡发送给收件人，请单击&#x200B;**保存并发送电子邮件**。

## 查看礼品卡帐户历史记录

1. 转到&#x200B;**[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Gift Card Accounts]**。

1. 在编辑模式下打开礼品卡。

1. 将显示礼品卡的&#x200B;**[!UICONTROL History]**。

   ![礼品卡历史记录](./assets/gift-card-history.png){width="600" zoomable="yes"}

| 列 | 描述 |
|--- |--- |
| [!UICONTROL ID] | 礼品卡操作的唯一数值。 |
| [!UICONTROL Date] | 操作日期。 |
| [!UICONTROL Action] | 确定礼品卡的所有可能操作。 选项： `Created` / `Updated` / `Sent` / `Used` / `Redeemed` / `Expired` |
| [!UICONTROL Balance Change] | 显示礼品卡余额的更改金额。 |
| [!UICONTROL Balance] | 指示可用余额。 |
| [!UICONTROL More Information] | 显示有关谁更改了礼品卡余额的信息。 |

{style="table-layout:auto"}

## 删除礼品卡帐户

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Gift Card Accounts]**。

1. 选择要删除的礼品卡帐户，并在编辑模式下将其打开。

1. 在菜单栏中，单击&#x200B;**[!UICONTROL Delete]**。

1. 要确认操作，请单击&#x200B;**[!UICONTROL OK]**。

## 列描述

| 列 | 描述 |
|--- |--- |
| [!UICONTROL ID] | 分配给礼品卡帐户的唯一数字标识符。 |
| [!UICONTROL Code] | 要应用礼品卡必须输入的代码。 |
| [!UICONTROL Website] | 指示礼品卡帐户可用的网站。 |
| [!UICONTROL Created] | 创建日期。 |
| [!UICONTROL End] | 礼品卡到期日期（如果已计划）。 |
| [!UICONTROL Active] | 确定礼品卡是否有效。 |
| [!UICONTROL Status] | 确定礼品卡是在客户帐户中兑现还是可用。 选项： `Used` / `Redeemed` / `Expired` |
| [!UICONTROL Balance] | 指示可用余额。 |

{style="table-layout:auto"}

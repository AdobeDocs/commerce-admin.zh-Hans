---
title: 应用商店积分
description: 商店管理员可将商店点数申请至购买。
exl-id: 97b6b206-71db-435c-8736-a781437bb0b4
feature: Customers, Storefront
TQID: 'https://experienceleague.adobe.com/O2EJMZscownPnhjPeFROdwikhYmHuDYdCx4N7NpXlho'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
    internal-label: Accounts
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
    internal-label: Order Management System
  - id: 22bad240-8308-569b-a9d5-578f1ff890ca
    internal-label: Customers
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
    internal-label: Storefront
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: b2b09a49ecd0c585d6ea456f0c00e05d813e324d
workflow-type: tm+mt
source-wordcount: '521'
ht-degree: 0%
---
# 应用商店积分

{{ee-feature}}

商店管理员可以查看客户帐户的信用余额和历史记录，还可以将商店信用应用于购买。

![客户信用余额和历史记录](assets/store-credit-balance-history.png){width="600" zoomable="yes"}

## 存储信用角色资源

仅[!BADGE SaaS]{type=Positive url="https://experienceleague.adobe.com/zh-hans/docs/commerce/user-guides/product-solutions" tooltip="仅适用于Adobe Commerce as a Cloud Service项目（Adobe管理的SaaS基础架构）。"}

以下资源确定哪些管理员用户可以更改客户的商店信用余额，以及哪些用户可以将商店信用应用于订单。 有关将资源分配给用户角色的信息，请参阅[角色资源](../systems/permissions-user-roles.md#role-resources)。

- **[!UICONTROL Customers]** > **[!UICONTROL All Customers]** > **[!UICONTROL Manage Store Credit Balances]**&#x200B;允许用户查看和更新商店信用余额。 如果没有它，**[!UICONTROL Store Credit]**&#x200B;选项卡和&#x200B;**[!UICONTROL Customer View]**&#x200B;选项卡上的&#x200B;**[!UICONTROL Store Credit Balance]**&#x200B;将不可见。 用户仍然可以对客户帐户进行其他编辑。

- **[!UICONTROL Sales]** > **[!UICONTROL Operations]** > **[!UICONTROL Orders]** > **[!UICONTROL Actions]** > **[!UICONTROL Create]** > **[!UICONTROL Can Spend Store Credit]**&#x200B;允许用户在[创建订单](../stores-purchase/customer-account-create-order.md)时申请商店积分。 如果没有该复选框，**[!UICONTROL Use Store Credit]**&#x200B;复选框将不可见。

使用REST API的管理员用户和集成需要&#x200B;**[!UICONTROL Can Spend Store Credit]**&#x200B;资源才能将商店积分应用到购物车，或为已应用商店积分的购物车下订单。 有关详细信息，请参阅[存储点数](https://developer.adobe.com/commerce/webapi/rest/saas-integrations/store-credit/)。

## 查看贷方余额

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Customers]** > **[!UICONTROL All Customers]**。

1. 在网格中查找客户。

1. 在&#x200B;_操作_&#x200B;列中，单击&#x200B;**[!UICONTROL Edit]**。

1. 滚动&#x200B;_[!UICONTROL Customer View]_&#x200B;页面并在底部查看&#x200B;**[!UICONTROL Store Credit Balance]**。

![存储信用余额](assets/store-credit-balance.png){width="600" zoomable="yes"}

## 更新商店贷方余额

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Customers]** > **[!UICONTROL All Customers]**。

1. 在网格中查找客户。

1. 在&#x200B;_操作_&#x200B;列中，单击&#x200B;**[!UICONTROL Edit]**。

1. 在左侧面板中，选择&#x200B;**[!UICONTROL Store Credit]**。

1. 选择要与余额关联的网站（店面）。

1. 对于&#x200B;**[!UICONTROL Update Balance]**，输入新值。

1. 要通知客户余额更新，请选中&#x200B;**[!UICONTROL Notify Customer by Email]**&#x200B;复选框，然后从&#x200B;**[!UICONTROL Send Email Notification From the Following Store View]**&#x200B;中选择商店视图。

1. 输入有关更改的&#x200B;**[!UICONTROL Comment]**。

1. 更新完成后，单击&#x200B;**[!UICONTROL Save and Continue Edit]**&#x200B;或&#x200B;**[!UICONTROL Save Customer]**。

更新的余额应显示在&#x200B;**[!UICONTROL Balance History]**&#x200B;中。

## 以商店管理员身份将贷方余额应用于订单

作为商店管理员，您可以代表客户执行各种操作，包括提交订单。 当您[创建订单](../stores-purchase/customer-account-create-order.md)时，您可以应用应付给客户的商店贷方余额。 可用余额显示在&#x200B;_付款和送货信息_&#x200B;部分。 选中&#x200B;**[!UICONTROL Use Store Credit]**&#x200B;复选框以应用余额，如果订单合计少于此值，则选择余额的一部分。

![将商店贷方余额应用于订单](assets/store-credit-apply.png){width="500" zoomable="yes"}

[!BADGE 仅限SaaS]{type=Positive url="https://experienceleague.adobe.com/zh-hans/docs/commerce/user-guides/product-solutions" tooltip="仅适用于Adobe Commerce as a Cloud Service项目（Adobe管理的SaaS基础架构）。"}仅当您的用户角色包含&#x200B;**[!UICONTROL Can Spend Store Credit]**&#x200B;资源时，**[!UICONTROL Use Store Credit]**&#x200B;复选框才会显示。 查看[存储信用角色资源](#store-credit-role-resources)。

## 在结账期间应用商店积分

如果地点有贷方余额，客户可以在将订单放在店面之前将商店贷方应用于订单余额。

1. 客户查看可用商店贷项的金额。

   在&#x200B;_审核和付款_&#x200B;步骤中，可用金额显示在&#x200B;_[!UICONTROL Store Credit]_&#x200B;下。

1. 要将金额应用于订单，请单击&#x200B;**[!UICONTROL Use Store Credit]**。

   >[!INFO]
   >
   >重新计算订单总计，应用的商店积分金额显示在&#x200B;_[!UICONTROL Order Summary]_&#x200B;中。

   ![存储应用于订单的贷方余额](assets/store-credit-checkout.png){width="700" zoomable="yes"}

1. 准备就绪后，单击&#x200B;**[!UICONTROL Place Order]**。

---
title: 来宾结帐
description: 了解如何在您的商店中启用访客签出功能。
exl-id: ce25eba3-7503-46aa-a5cd-9b7d5662164b
feature: Checkout
source-git-commit: 347321ec5b0722f06240780136cb29816aab559f
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 0%

---

# 来宾结帐

您的商店可以配置为要求购物者在购买之前开立帐户。 默认设置允许来宾进行购买，并允许在来宾完成结账过程后注册帐户。

![Luma存储区显示“签出”为来宾](./assets/storefront-checkout-as-guest.png){width="600" zoomable="yes"}

**_禁用来宾签出:_**

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧面板上，展开&#x200B;**[!UICONTROL Sales]**&#x200B;并选择&#x200B;**[!UICONTROL Checkout]**。

1. 展开![部分的](../assets/icon-display-expand.png)扩展选择器&#x200B;**[!UICONTROL Checkout Options]**。

   ![在配置页面上扩展的签出选项](./assets/checkout-checkout-options.png){width="700" zoomable="yes"}

有关每个配置设置的详细说明，请参阅[配置参考指南](../configuration-reference/sales/checkout.md#checkout-options)中的&#x200B;_签出选项_。

1. 如果该设置针对特定的存储视图，[请选择应用该配置的存储视图](../configuration-reference/scope-change.md#set-the-scope)。

   出现提示时，单击&#x200B;**[!UICONTROL OK]**&#x200B;继续。

1. 将&#x200B;**[!UICONTROL Allow Guest Checkout]**&#x200B;设置为`No`。

   如有必要，请清除&#x200B;**[!UICONTROL Use system value]**&#x200B;复选框以启用对此设置的更改。

1. 单击&#x200B;**[!UICONTROL Save Config]**。

## 允许已注册电子邮件访问访客订单

仅[!BADGE SaaS]{type=Positive url="https://experienceleague.adobe.com/zh-hans/docs/commerce/user-guides/product-solutions" tooltip="仅适用于Adobe Commerce as a Cloud Service项目(Adobe管理的SaaS基础架构)。"}

通过默认禁用的可选商店级别配置，访客购物者可以跟踪他们使用与注册客户帐户匹配的电子邮件地址下达的订单。

启用后，随已注册电子邮件一起下达的访客结帐订单将保持可访问状态，但同时也会显示在客户的订单历史记录中。

要启用此功能，请导航到&#x200B;**商店** >设置> **配置** >销售> **销售** > **来宾签出**，并将&#x200B;**允许已注册电子邮件访问来宾订单**&#x200B;设置设置为`Yes`。

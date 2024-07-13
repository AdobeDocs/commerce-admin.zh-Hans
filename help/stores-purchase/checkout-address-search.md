---
title: 结账时的地址搜索
description: 了解如何在商店结帐时包含地址搜索。
exl-id: 8153c456-0848-4bb4-8deb-8219323344ed
feature: Checkout
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '434'
ht-degree: 0%

---

# 结账时的地址搜索

{{ee-feature}}

您的客户在其通讯簿中可以有许多已保存的地址和信息，尤其是定期回头客户或输入多个订单和发运地点的公司。 显示多个地址可能会减慢结帐加载速度并显着影响流程，并导致负面购物体验。 为帮助提高签出的响应速度，建议激活并配置站点的地址搜索。

>[!NOTE]
>
>默认情况下不启用地址搜索。 您可以将此功能配置为在站点上包含该功能。

启用此功能且客户的保存地址数达到或超过配置限制时，_送货_&#x200B;和&#x200B;_审核和付款_&#x200B;步骤仅显示一个地址（默认值）。 客户可以通过单击&#x200B;**更改地址**，然后按城市、州/省、街道或邮政编码搜索正确的地址来更改所选地址。 此功能还支持为礼品注册结帐选择地址。

![显示已保存配送地址的结帐](./assets/storefront-checkout-address-search.png){width="700" zoomable="yes"}

如果客户没有默认送货地址，则&#x200B;_送货_&#x200B;页显示&#x200B;_未选择地址_。 在这种情况下，客户必须单击&#x200B;**更改地址**&#x200B;以选择保存的地址，或单击&#x200B;**新建地址**&#x200B;以添加并选择地址，然后才能继续结帐。 如果客户没有默认帐单地址，则&#x200B;_审核和付款_&#x200B;页面将显示选定要发送的地址以及&#x200B;_更改地址_&#x200B;选项。

![签出，未选择地址](./assets/storefront-checkout-address-search-no-default.png){width="600" zoomable="yes"}

## 锁定的询价地址搜索

![Adobe Commerce B2B](../assets/b2b.svg)(仅适用于Adobe Commerce B2B)

启用地址搜索还会影响对从报价创建的订单的结帐，其中客户保存的地址数达到或超过配置的限制。 当报价完成并且客户进行结帐时，只显示选定的送货地址。 此页面还会显示一条消息，说明送货地址已锁定，只能在报价中进行更改。

![为报价锁定送货地址](./assets/quote-checkout-shipping-address-locked.png){width="600" zoomable="yes"}

## 启用地址搜索

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧面板中，展开&#x200B;**[!UICONTROL Sales]**&#x200B;并选择&#x200B;**[!UICONTROL Checkout]**。

1. 展开&#x200B;**[!UICONTROL Checkout Options]**&#x200B;部分的![扩展选择器](../assets/icon-display-expand.png)。

   ![配置 — 签出选项](./assets/checkout-checkout-options.png){width="700" zoomable="yes"}

   有关每个配置设置的详细说明，请参阅&#x200B;_配置参考指南_&#x200B;中的[签出选项](../configuration-reference/sales/checkout.md#checkout-options)。

1. 将&#x200B;**[!UICONTROL Enable Address Search]**&#x200B;设置为`Yes`。

1. 要指定包含地址搜索功能的阈值，请设置&#x200B;**[!UICONTROL Number of Customer Addresses Limit]**&#x200B;选项。

   如有必要，请清除&#x200B;**[!UICONTROL Use system value]**&#x200B;复选框以进行此更改。

   当客户的已保存地址数达到或超过此限制时，页面将显示默认地址（如果客户有默认地址）或使用&#x200B;_更改地址_&#x200B;选项的&#x200B;_未选择地址_。 默认限制为`10`。

1. 单击&#x200B;**[!UICONTROL Save Config]**。

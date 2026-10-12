---
title: 产品设置 — [!UICONTROL Gift Options]
description: 对于产品，[!UICONTROL Gift Options]设置可确定是否可以包含礼品消息，或者是否在结帐期间提供礼品包装选项。
exl-id: 21597e38-60f5-45e5-8d99-955d088c5c48
feature: Catalog Management, Products, Gift
TQID: 'https://experienceleague.adobe.com/MIzb2vY-DiVqODkNFmgX3tFLejQFZMtOETUDPoHrt-Y'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
    internal-label: Order Management System
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
    internal-label: Catalog management
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
    internal-label: Storefront
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: 4067ab89-2e97-5de1-8d98-de8318461a8d
    internal-label: Products
  - id: 4fc0a729-4349-5307-bd06-1b4bfbaf5d0c
    internal-label: Gift
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: acc7571574eb9c7e96911266897350a77913488e
workflow-type: tm+mt
source-wordcount: '230'
ht-degree: 0%
---
# 产品设置 — [!UICONTROL Gift Options]

在&#x200B;_[!UICONTROL Gift Options]_部分中，您可以在产品层级结帐时设置礼品消息和礼品包装选项。 要覆盖默认配置设置，请取消选中&#x200B;**[!UICONTROL Use Config Settings]**复选框。

![礼品选项](./assets/product-gift-options-ee.png){width="600" zoomable="yes"}

## 为单个产品设置赠品选项

1. 在编辑模式下打开产品。

1. 向下滚动并展开![扩展选择器](../assets/icon-display-expand.png) _[!UICONTROL Gift Options]_部分，然后执行以下操作：

   - 要覆盖默认设置，请取消选中&#x200B;**[!UICONTROL Use Config Settings]**&#x200B;复选框。

   - 根据需要为产品设置&#x200B;**[!UICONTROL Allow Gift Message]**。

   - ![Adobe Commerce](../assets/adobe-logo.svg) （仅限[Adobe Commerce](../landing/home.md#product-editions)）根据需要为产品设置&#x200B;**[!UICONTROL Allow Gift Wrapping]**。

   - ![Adobe Commerce](../assets/adobe-logo.svg) （仅限[Adobe Commerce](../landing/home.md#product-editions)）如果适用，请输入&#x200B;**[!UICONTROL Price for Gift Wrapping]**。

1. 完成后，单击&#x200B;**[!UICONTROL Save]**。

## 为商店启用礼品消息

默认情况下，Commerce允许客户在结账过程中向其订单和产品添加个性化礼品消息。

您可以为商店启用&#x200B;_礼品邮件_，从而向客户提供此功能：

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧面板中，展开&#x200B;**[!UICONTROL Sales]**&#x200B;并在下面选择&#x200B;**[!UICONTROL Sales]**。

1. 展开页面上的![扩展选择器](../assets/icon-display-expand.png) **[!UICONTROL Gift Options]**。

1. 对于&#x200B;**[!UICONTROL Allow Gift Messages on Order Level]**，选择`Yes`以启用整个订单的单个礼品消息。

1. 对于&#x200B;**[!UICONTROL Allow Gift Messages for Order Items]**，选择`Yes`以启用将礼品邮件单独添加到客户购物车中的各个项目。

1. 单击&#x200B;**[!UICONTROL Save Config]**。

使用此配置，客户可以从店面将礼品消息添加到购物车页面，如以下示例所示：

![礼品邮件](./assets/gift-message.png){width="600" zoomable="yes"}

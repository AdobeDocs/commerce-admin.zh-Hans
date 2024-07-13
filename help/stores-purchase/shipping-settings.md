---
title: 配送设置
description: 了解如何配置配送设置，以定义商店的原点和配送政策。
exl-id: 767b3039-39c7-4692-a0a8-a8fde27622cc
feature: Shipping/Delivery
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '352'
ht-degree: 0%

---

# 配送设置

发运配置为所有发运、您的发运策略以及将发运处理到多个地址建立起点位置。

## 原点

原产地用于计算从您的商店或仓库发运的费用，也可以确定所销售产品的税率。 在计算[EU税](international-tax-guidelines.md#eu-tax-configuration)时，请确保每个商店视图的[默认纳税目标计算](../configuration-reference/sales/tax.md)与装运设置原始点相对应。

![来源](../configuration-reference/sales/assets/shipping-settings-origin.png){width="600" zoomable="yes"}

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧面板中，展开&#x200B;**[!UICONTROL Sales]**&#x200B;并选择&#x200B;**[!UICONTROL Shipping Settings]**。

1. 展开![扩展选择器](../assets/icon-display-expand.png) **[!UICONTROL Origin]**&#x200B;部分并完成以下操作：

   - [!UICONTROL Country]
   - [!UICONTROL Region / State]
   - [!UICONTROL ZIP / Postal Code]
   - [!UICONTROL City]
   - [!UICONTROL Street Address]（如果需要，在第2行）

1. 单击&#x200B;**[!UICONTROL Save Config]**。

## 配送政策

发货政策应说明贵公司的发货业务规则和指南。 例如，如果您有触发免运费的价格规则，则可以解释配送政策中的条款。

签出期间![送货策略](./assets/storefront-checkout-shipping-policy.png){width="700" zoomable="yes"}

要在结帐期间显示送货策略，请完成配置中的送货策略参数。 当客户在结帐期间单击&#x200B;_查看我们的送货策略_&#x200B;时，将显示此文本。

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧面板中，展开&#x200B;**[!UICONTROL Sales]**&#x200B;并选择&#x200B;**[!UICONTROL Shipping Settings]**。

1. 展开&#x200B;**[!UICONTROL Shipping Policy Parameters]**&#x200B;部分的![扩展选择器](../assets/icon-display-expand.png)。

1. 将&#x200B;**[!UICONTROL Apply Custom Shipping Policy]**&#x200B;设置为`Yes`。

1. 将您的&#x200B;**[!UICONTROL Shipping Policy]**&#x200B;粘贴或输入文本框中。

   >[!NOTE]
   >
   >如果使用文字处理器撰写文本，请确保将文档另存为.txt文件，以便从文本中删除任何控制字符。 然后，将文本复制并粘贴到“送货策略”文本框中。

   ![配送策略参数](../configuration-reference/sales/assets/shipping-settings-shipping-policy-parameters.png){width="600" zoomable="yes"}

1. 单击&#x200B;**[!UICONTROL Save Config]**。

## 多个地址

多个地址发运选项使客户能够在结帐时将订单发运到多个地址，并确定订单可以发运的最大地址数。

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧面板中，展开&#x200B;**[!UICONTROL Sales]**&#x200B;并选择&#x200B;**[!UICONTROL Multishipping Settings]**。

1. 展开&#x200B;**[!UICONTROL Options]**&#x200B;部分的![扩展选择器](../assets/icon-display-expand.png)。

   ![多地址送货选项](../configuration-reference/sales/assets/multishipping-settings-options.png){width="600" zoomable="yes"}

1. 将&#x200B;**[!UICONTROL Allow Shipping to Multiple Addresses]**&#x200B;设置为`Yes`。

1. 输入&#x200B;**[!UICONTROL Maximum Qty Allowed for Shipping to Multiple Addresses]**。

1. 单击&#x200B;**[!UICONTROL Save Config]**。

>[!NOTE]
>
>![Adobe Commerce B2B](../assets/b2b.svg) (Adobe Commerce B2B)对于具有多个配送地址的订单，在结帐期间无法使用[帐户付款](../b2b/enable-basic-features.md#configure-payment-on-account)付款方式（即使已启用）。

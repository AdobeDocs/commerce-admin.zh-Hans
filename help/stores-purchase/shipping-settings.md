---
title: 配送设置
description: 了解如何配置配送设置，以定义商店的原点和配送政策。
exl-id: 767b3039-39c7-4692-a0a8-a8fde27622cc
feature: Shipping/Delivery
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '355'
ht-degree: 0%

---

# 配送设置

发运配置为所有发运、您的发运策略以及将发运处理到多个地址建立起点位置。

## 原点

原产地用于计算从您的商店或仓库发运的费用，也可以确定所销售产品的税率。 计算时 [欧盟税收](international-tax-guidelines.md#eu-tax-configuration)，确保 [默认纳税目标计算](../configuration-reference/sales/tax.md) 每个商店视图对应于“送货设置”原点。

![Origin](../configuration-reference/sales/assets/shipping-settings-origin.png){width="600" zoomable="yes"}

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中，展开 **[!UICONTROL Sales]** 并选择 **[!UICONTROL Shipping Settings]**.

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Origin]** 部分并完成以下操作：

   - [!UICONTROL Country]
   - [!UICONTROL Region / State]
   - [!UICONTROL ZIP / Postal Code]
   - [!UICONTROL City]
   - [!UICONTROL Street Address] （如果需要，可以添加第2行）

1. 单击 **[!UICONTROL Save Config]**.

## 配送政策

发货政策应说明贵公司的发货业务规则和指南。 例如，如果您有触发免运费的价格规则，则可以解释配送政策中的条款。

![结帐时的配送政策](./assets/storefront-checkout-shipping-policy.png){width="700" zoomable="yes"}

要在结帐期间显示送货策略，请完成配置中的送货策略参数。 客户单击时将显示文本 _查看我们的配送政策_ 结账期间。

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中，展开 **[!UICONTROL Sales]** 并选择 **[!UICONTROL Shipping Settings]**.

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Shipping Policy Parameters]** 部分。

1. 设置 **[!UICONTROL Apply Custom Shipping Policy]** 到 `Yes`.

1. 粘贴或输入您的 **[!UICONTROL Shipping Policy]** 放到文本框中。

   >[!NOTE]
   >
   >如果使用文字处理器撰写文本，请确保将文档另存为.txt文件，以便从文本中删除任何控制字符。 然后，将文本复制并粘贴到“送货策略”文本框中。

   ![配送政策参数](../configuration-reference/sales/assets/shipping-settings-shipping-policy-parameters.png){width="600" zoomable="yes"}

1. 单击 **[!UICONTROL Save Config]**.

## 多个地址

多个地址发运选项使客户能够在结帐时将订单发运到多个地址，并确定订单可以发运的最大地址数。

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中，展开 **[!UICONTROL Sales]** 并选择 **[!UICONTROL Multishipping Settings]**.

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Options]** 部分。

   ![多地址送货选项](../configuration-reference/sales/assets/multishipping-settings-options.png){width="600" zoomable="yes"}

1. 设置 **[!UICONTROL Allow Shipping to Multiple Addresses]** 到 `Yes`.

1. 输入 **[!UICONTROL Maximum Qty Allowed for Shipping to Multiple Addresses]**.

1. 单击 **[!UICONTROL Save Config]**.

>[!NOTE]
>
>![适用于Adobe Commerce的B2B](../assets/b2b.svg) (适用于Adobe Commerce的B2B)对于具有多个发运地址的订单，应 [分期付款](../b2b/enable-basic-features.md#configure-payment-on-account) 付款方式即使已启用，在结帐期间也不可用。

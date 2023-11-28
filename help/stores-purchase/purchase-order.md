---
title: 采购订单
description: 了解如何将采购订单设置为商店的离线付款方式。
exl-id: 493c1b59-2155-449f-a08a-eb1aa2af9b3e
feature: Purchase Orders
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 0%

---

# 采购订单

A _采购订单_ (PO)允许商业客户通过参考PO编号来支付授权采购。 采购单由进行采购的公司预先授权和签发。 在结账过程中，客户选择“采购订单”作为付款方式。 收到您的发票后，公司即在其应付帐款系统中处理付款，并支付购买费用。

接受采购订单付款前，应始终建立商业客户的资信。

**_要按采购订单配置付款，请执行以下操作：_**

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中，展开 **[!UICONTROL Sales]** 并选择 **[!UICONTROL Payment Methods]**.

1. 下 _[!UICONTROL Other Payment Methods]_，展开 ![扩展选择器](../assets/icon-display-expand.png) 该&#x200B;**[!UICONTROL Purchase Order]**部分。

   ![采购订单](../configuration-reference/sales/assets/payment-methods-purchase-order.png){width="600" zoomable="yes"}

   有关每个配置设置的详细说明，请参阅 [采购订单](../configuration-reference/sales/payment-methods.md#purchase-order) 在 _配置参考指南_.

   >[!NOTE]
   >
   >如有必要，请先清除 **[!UICONTROL Use system value]** 复选框以更改这些设置。

1. 要激活此付款方法，请设置 **[!UICONTROL Enabled]** 到 `Yes`.

1. 对象 **[!UICONTROL Title]**，输入在结账时标识此付款方式的标题。

1. 设置 **[!UICONTROL New Order Status]** 到 `Pending` 直到付款获得批准。

1. 设置 **[!UICONTROL Payment from Applicable Countries]** 更改为以下任一项：

   - `All Allowed Countries`  — 来自所有客户的客户 [国家/地区](../getting-started/store-details.md#country-options) 在商店配置中指定的可使用此付款方式。
   - `Specific Countries`  — 选择此选项后， _[!UICONTROL Payment from Specific Countries]_列表出现。 要选择多个国家/地区，请按住Ctrl键(PC)或Command键(Mac)并单击每个选项。

1. 设置 **[!UICONTROL Minimum Order Total]** 和 **[!UICONTROL Maximum Order Total]** 与符合此付款方法所需的金额之间的差额。

   >[!NOTE]
   >
   >如果合计在最小或最大合计值之间，或者与最小或最大合计值完全匹配，则订单合格。

1. 对象 **[!UICONTROL Sort Order]**，请输入一个数字，该数字用于确定此项目在结账时显示的付款方式列表中的位置。

   此数字相对于其他支付方式。 (`0` =第一个， `1` =秒， `2` =第三，依此类推。)

1. 完成后，单击 **[!UICONTROL Save Config]**.

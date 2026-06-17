---
title: 采购订单
description: 了解如何将采购订单设置为商店的离线付款方式。
exl-id: 493c1b59-2155-449f-a08a-eb1aa2af9b3e
feature: Purchase Orders
TQID: https://experienceleague.adobe.com/Oc2vdP-OTXwo-6cjKWFj5zPf-QJVvU8aK6OUMPko4eY
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: bd989d82-1e15-4534-88db-f1f51dd77ffaid: c1256247-af4b-46d8-9dca-0c654ecfa157id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 296
ht-degree: 0%

---

# 采购订单

_采购订单_ (PO)允许商业客户通过引用PO编号来支付授权采购。 采购单由进行采购的公司预先授权和签发。 在结账过程中，客户选择“采购订单”作为付款方式。 收到您的发票后，公司即在其应付帐款系统中处理付款，并支付购买费用。

接受采购订单付款前，应始终建立商业客户的资信。

**_要按采购订单配置付款，请执行以下操作:_**

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧面板中，展开&#x200B;**[!UICONTROL Sales]**&#x200B;并选择&#x200B;**[!UICONTROL Payment Methods]**。

1. 在&#x200B;_[!UICONTROL Other Payment Methods]_下，展开&#x200B;**[!UICONTROL Purchase Order]**部分的![扩展选择器](../assets/icon-display-expand.png)。

   ![采购订单](../configuration-reference/sales/assets/payment-methods-purchase-order.png){width="600" zoomable="yes"}

   有关每个配置设置的详细说明，请参阅&#x200B;_配置参考指南_&#x200B;中的[采购订单](../configuration-reference/sales/payment-methods.md#purchase-order)。

   >[!NOTE]
   >
   >如有必要，请先清除&#x200B;**[!UICONTROL Use system value]**&#x200B;复选框以更改这些设置。

1. 若要激活此付款方法，请将&#x200B;**[!UICONTROL Enabled]**&#x200B;设置为`Yes`。

1. 对于&#x200B;**[!UICONTROL Title]**，输入在结帐时标识此付款方式的标题。

1. 将&#x200B;**[!UICONTROL New Order Status]**&#x200B;设置为`Pending`，直到获得付款授权。

1. 将&#x200B;**[!UICONTROL Payment from Applicable Countries]**&#x200B;设置为以下项之一：

   - `All Allowed Countries` — 来自您商店配置中指定的所有[国家/地区](../getting-started/store-details.md#country-options)的客户都可以使用此付款方式。
   - `Specific Countries` — 选择此选项后，将显示&#x200B;_[!UICONTROL Payment from Specific Countries]_列表。 要选择多个国家/地区，请按住Ctrl键(PC)或Command键(Mac)并单击每个选项。

1. 将&#x200B;**[!UICONTROL Minimum Order Total]**&#x200B;和&#x200B;**[!UICONTROL Maximum Order Total]**&#x200B;设置为符合此付款方式所需的金额。

   >[!NOTE]
   >
   >如果合计在最小或最大合计值之间，或者与最小或最大合计值完全匹配，则订单合格。

1. 对于&#x200B;**[!UICONTROL Sort Order]**，输入一个数字，该数字确定此项目在结帐期间显示的付款方式列表中的位置。

   此数字相对于其他支付方式。 （`0` =第一，`1` =第二，`2` =第三，依此类推。）

1. 完成后，单击&#x200B;**[!UICONTROL Save Config]**。

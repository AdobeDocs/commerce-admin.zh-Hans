---
title: 银行转帐
description: 了解如何将银行转帐设置为商店的离线付款方式。
exl-id: 34b2163c-2edd-4741-b002-3d8fb561fc78
feature: Payments
TQID: https://experienceleague.adobe.com/uIYk-S9M8nsKxo3O71N1z25Y-K5WaYOOAM26k9HLVoQ
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 275
ht-degree: 0%

---

# 银行转帐

Adobe Commerce和Magento Open Source允许您接受从客户银行帐户转账并存入您的商家银行帐户的付款。

**_要配置银行转帐付款:_**

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧面板中，展开&#x200B;**[!UICONTROL Sales]**&#x200B;并选择&#x200B;**[!UICONTROL Payment Methods]**。

1. 在&#x200B;_其他付款方式_&#x200B;下，展开![扩展选择器](../assets/icon-display-expand.png) **[!UICONTROL Bank Transfer Payment]**&#x200B;部分。

   ![银行转帐付款](../configuration-reference/sales/assets/payment-methods-bank-transfer-payment.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >如有必要，请先清除&#x200B;**[!UICONTROL Use system value]**&#x200B;复选框以更改这些设置。

1. 要激活银行转帐，请将&#x200B;**[!UICONTROL Enabled]**&#x200B;设置为`Yes`。

1. 对于&#x200B;**[!UICONTROL Title]**，输入在结帐期间标识银行转帐付款方式的标题。

1. 将&#x200B;**[!UICONTROL New Order Status]**&#x200B;设置为`Pending`，直到获得付款授权。

1. 将&#x200B;**[!UICONTROL Payment from Applicable Countries]**&#x200B;设置为以下项之一：

   - `All Allowed Countries` — 来自您商店配置中指定的所有[国家/地区](../getting-started/store-details.md#country-options)的客户都可以使用此付款方式。

   - `Specific Countries` — 选择此选项后，将显示&#x200B;_[!UICONTROL Payment from Specific Countries]_&#x200B;列表。 要选择多个国家/地区，请按住Ctrl键(PC)或Command键(Mac)并单击每个选项。

1. 输入客户设置银行转帐时必须遵循的&#x200B;**[!UICONTROL Instructions]**。

   根据银行所在的国家/地区和银行要求，您可以包括以下信息：

   - 银行帐户名称
   - 银行帐号
   - 银行代号
   - 银行名称
   - 银行地址

1. 将&#x200B;**[!UICONTROL Minimum Order Total]**&#x200B;和&#x200B;**[!UICONTROL Maximum Order Total]**&#x200B;设置为有资格使用此付款方法所需的金额。

   >[!NOTE]
   >
   >如果合计在最小或最大合计值之间，或者与最小或最大合计值完全匹配，则订单合格。

1. 对于&#x200B;**[!UICONTROL Sort Order]**，输入一个数字，该数字确定此项目在结帐期间显示的付款方法列表中的位置。

   此数字相对于其他支付方式。 （`0` =第一，`1` =第二，`2` =第三，依此类推。）

1. 完成后，单击&#x200B;**[!UICONTROL Save Config]**。

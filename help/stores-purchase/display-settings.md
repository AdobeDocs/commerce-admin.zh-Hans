---
title: 价格显示设置
description: 了解目录、购物车、订单、发票和支持客户购买体验的贷项通知单中税项的显示。
exl-id: 6f97c474-ef6e-4ca6-899d-812c58b993ca
feature: Checkout, Invoices, Taxes
TQID: https://experienceleague.adobe.com/XIcN-vl8owiToGhM3Et2euyNWgnJdsgSl6urwJcRdLE
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 519
ht-degree: 0%

---

# 价格显示设置

价格显示设置可确定产品和运输价格是含税还是不含税，或者显示两个版本的价格；一个含税，另一个不含税。

如果产品价格含税，则仅当存在与税源匹配的税则或客户地址与税则匹配时，系统才会显示税。 可能触发匹配的事件包括：客户创建帐户、登录，或从购物车中生成税费和运费估计值时。

>[!IMPORTANT]
>
>显示含税和不含税的价格会让客户感到困惑。 为避免触发警告消息，请参阅您所在国家/地区的[指南](international-tax-guidelines.md)和[避免警告消息的建议](taxes.md#warning-messages)。

![价格显示设置](../configuration-reference/sales/assets/tax-price-display-settings.png){width="600" zoomable="yes"}

有关这些配置设置的详细说明，请参阅&#x200B;_配置参考指南_&#x200B;中的[价格显示设置](../configuration-reference/sales/tax.md#price-display-settings)。

## 配置价格显示设置

完成税费、税率和类别的计算配置后，将按照这些设置计算税费。 但是，也应配置目录、购物车、订单、发票和贷项通知单中的税种显示，以支持店面的客户体验。

最好是将价格与相关的税费（包括税费，或同时包括税费和不包括税费）一起显示，这样客户就可以在下订单之前了解如何应用这些计算。

### 步骤1：配置目录价格显示设置

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧面板中，展开&#x200B;**[!UICONTROL Sales]**&#x200B;并选择&#x200B;**[!UICONTROL Tax]**。

1. 展开&#x200B;**[!UICONTROL Price Display Settings]**&#x200B;部分的![扩展选择器](../assets/icon-display-expand.png)。

1. 对于&#x200B;**[!UICONTROL Display Product Prices in Catalog]**，请选择下列选项之一：

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

   >[!NOTE]
   >
   >如果将此选项设置为`Including Tax`，则仅当存在与税源匹配的税则或存在与税则匹配的客户地址时，才会显示税。 可触发匹配的事件包括客户帐户创建、登录，或购物车中使用税务和运输估计工具。

1. 对于&#x200B;**[!UICONTROL Display Shipping Prices]**，请选择下列选项之一：

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

如果您选择同时显示这两个价格（含税和不含税），店面将类似于以下内容：

![店面含税价格显示示例](./assets/catalog-prices-tax.png){width="700" zoomable="yes"}

### 步骤2：配置购物车显示设置

1. 展开&#x200B;**[!UICONTROL Shopping Cart Display Settings]**&#x200B;部分的![扩展选择器](../assets/icon-display-expand.png)。

   ![购物车显示设置](../configuration-reference/sales/assets/tax-shopping-cart-display-settings.png){width="600" zoomable="yes"}

1. 对于&#x200B;**[!UICONTROL Display Prices]**，请选择下列选项之一：

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. 对于&#x200B;**[!UICONTROL Display Subtotal]**，请选择下列选项之一：

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. 对于&#x200B;**[!UICONTROL Display Shipping Amount]**，请选择下列选项之一：

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. ![Adobe Commerce](../assets/adobe-logo.svg)（仅限Adobe Commerce）对于&#x200B;**[!UICONTROL Display Gift Wrapping Prices]**，请选择以下选项之一：

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. ![Adobe Commerce](../assets/adobe-logo.svg)（仅限Adobe Commerce）对于&#x200B;**[!UICONTROL Display Printed Card Prices]**，请选择以下选项之一：

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. 对于其余各个选项，根据您的喜好切换到`Yes`或`No`：

   - **[!UICONTROL Include Tax in Order Total]**
   - **[!UICONTROL Display Full Tax Summary]**
   - **[!UICONTROL Display Zero Tax Subtotal]**

### 步骤3：配置订单、发票和贷项通知单显示设置

1. 展开&#x200B;**[!UICONTROL Orders, Invoices, Credit Memos Display Settings]**&#x200B;部分的![扩展选择器](../assets/icon-display-expand.png)。

   ![订单、发票、贷项通知单显示设置](../configuration-reference/sales/assets/tax-orders-invoices-credit-memos-display-settings.png){width="600" zoomable="yes"}

1. 对于&#x200B;**[!UICONTROL Display Prices]**，请选择下列选项之一：

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. 对于&#x200B;**[!UICONTROL Display Subtotal]**，请选择下列选项之一：

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. 对于&#x200B;**[!UICONTROL Display Shipping Amount]**，请选择下列选项之一：

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. ![Adobe Commerce](../assets/adobe-logo.svg)（仅限Adobe Commerce）对于&#x200B;**[!UICONTROL Display Gift Wrapping Prices]**，请选择以下选项之一：

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. ![Adobe Commerce](../assets/adobe-logo.svg)（仅限Adobe Commerce）对于&#x200B;**[!UICONTROL Display Printed Card Prices]**，请选择以下选项之一：

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. 对于其余各个选项，根据您的喜好切换到`Yes`或`No`：

   - **[!UICONTROL Include Tax in Order Total]**
   - **[!UICONTROL Display Full Tax Summary]**
   - **[!UICONTROL Display Zero Tax Subtotal]**

1. 完成后，单击&#x200B;**[!UICONTROL Save Config]**。

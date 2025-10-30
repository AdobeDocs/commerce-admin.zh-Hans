---
title: 配置配送标签
description: 了解如何配置商店以生成装运标签。
exl-id: 0693d74b-8b36-4a36-8739-c9fe5a934ff0
feature: Shipping/Delivery, Orders
source-git-commit: d5beff4d450dab21f74e5baec6b718b844963858
workflow-type: tm+mt
source-wordcount: '593'
ht-degree: 0%

---

# 配置配送标签

必须在产品级别以及在每个用于打印标签的托架的配置中进行以下设置。 要打印标签，所有运营商均要求您开立帐户。 然后，在商店中为您计划使用的每个运营商完成配置。

## 承运人要求

| [!UICONTROL Carrier] | 要求 |
|-------|--------|
| [USPS](usps.md) | 需要用于装运标签邮资的USPS帐户。 |
| [UPS](ups.md) | 需要UPS帐户。 发运标签仅适用于源于美国的发运。美国以外的商店需要特定凭据才能运输。 |
| [联邦快递](fedex.md) | 需要FedEx帐户。 对于美国以外的商店，仅支持对国际运输使用运输标签。 联邦快递不允许来自美国境外的国内货物运送 |
| [DHL](dhl.md) | 需要DHL帐户。 仅对源自美国的装运支持装运标签。 |

{style="table-layout:auto"}

## 第1步：核实制造国

USPS和FedEx向国际发运的所有产品均要求生产国。 如果您有许多应更新的产品，您可以[导入](../systems/data-import.md)更新，或者使用清单网格更新多个记录。

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Catalog]** > **[!UICONTROL Products]**。

1. 使用以下方法之一更新装运标签记录。

### 方法1：更新单个记录

1. 在网格中，找到要更新的产品，并以编辑模式打开。

1. 根据需要更新&#x200B;**制造国家/地区**。

   ![制造国家/地区](./assets/product-country-of-manufacture.png){width="700" zoomable="yes"}

1. 单击&#x200B;**[!UICONTROL Save]**。

### 方法2：更新多个记录

1. 在网格中，选中要更新的每个产品的复选框。

   例如，所有在中国生产的产品。

1. 将&#x200B;**[!UICONTROL Actions]**&#x200B;控件设置为`Update Attributes`并单击&#x200B;**[!UICONTROL Submit]**。

1. 在&#x200B;_更新属性_&#x200B;表单中，找到&#x200B;**制造国家/地区**&#x200B;字段并选择&#x200B;**更改**&#x200B;复选框。

1. 选择国家。

1. 单击&#x200B;**[!UICONTROL Save]**。

## 步骤2验证存储信息

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧面板中，展开&#x200B;**[!UICONTROL Sales]**&#x200B;并选择&#x200B;**[!UICONTROL Shipping Settings]**。

1. 展开![部分的](../assets/icon-display-expand.png)扩展选择器&#x200B;**[!UICONTROL Origin]**，并验证以下字段是否完整：

   - **[!UICONTROL Street Address]** — 发货地点的街道地址。 例如，公司或仓库的位置。 装运标签需要此字段。
   - **[!UICONTROL Street Address Line 2]** — 任何其他地址信息，如楼层或入口。 建议使用此字段。

   ![来源](../configuration-reference/sales/assets/shipping-settings-origin.png){width="600" zoomable="yes"}

1. 在左侧面板的&#x200B;_Sales_&#x200B;部分中，选择&#x200B;**[!UICONTROL Delivery Methods]**。

1. 展开![部分的](../assets/icon-display-expand.png)扩展选择器&#x200B;**[!UICONTROL USPS]**，并验证以下字段是否完整：

   - **[!UICONTROL Secure Gateway URL]** — 系统自动进入网关URL。
   - **[!UICONTROL Password]** — 密码由USPS提供，允许您通过Web服务访问其系统。
   - **长度、宽度、高度、周长** — 包的默认尺寸。 若要显示这些字段，请将&#x200B;**[!UICONTROL Size]**&#x200B;设置为`Large`。

1. 展开![FedEx](../assets/icon-display-expand.png)部分的&#x200B;**扩展选择器**，并验证以下字段是否完整：

   - 计量器编号
   - 键
   - 密码

   此信息由运营商提供，通过Web服务访问其系统时需要此信息。

1. 在左侧面板中，展开&#x200B;**[!UICONTROL General]**&#x200B;并在下面选择&#x200B;**[!UICONTROL General]**。

1. 展开![扩展选择器](../assets/icon-display-expand.png) **[!UICONTROL Store Information]**&#x200B;部分，并验证以下字段是否已完成：

   - **[!UICONTROL Store Name]** — 商店或商店视图的名称。
   - **[!UICONTROL Store Contact Telephone]** — 商店或商店视图的主要联系人的电话号码。
   - **[!UICONTROL Country]** — 您的商店所在的国家/地区。
   - **[!UICONTROL VAT Number]** — 如果适用，为商店的增值税号。 （位于美国的商店不需要）
   - **[!UICONTROL Store Contact Address]** — 商店或商店视图的主要联系人的街道地址。

1. 如果您有多个商店，并且联系人信息与默认信息不同，请为每个商店设置&#x200B;**[!UICONTROL Store View]**&#x200B;并验证信息是否完整。

   如果缺少信息，则在尝试打印标签时出现错误。

   ![存储信息](../configuration-reference/general/assets/general-store-information.png){width="600" zoomable="yes"}

1. 单击&#x200B;**[!UICONTROL Save Config]**。

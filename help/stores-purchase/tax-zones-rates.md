---
title: 税区和税率
description: 了解如何为您收税和汇款的每个地理区域定义税率。
exl-id: d8eb0743-d277-438d-91ed-fc711a6ba3ae
feature: Taxes
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '377'
ht-degree: 0%

---

# 税区和税率

税率通常适用于在特定地理区域内进行的交易。 使用 _税区和税率_ 工具，为收税和汇税的每个地理区域指定税率。 由于每个税区和税率具有唯一标识符，因此您可以对指定地理区域使用多个税率（例如，不对食物或药品征税，但对其他项目征税的位置）。

根据商店地址计算商店税。 在客户完成订单信息后计算订单的实际客户税。 然后，Commerce根据商店的税务配置计算税额。

![税区和税率](./assets/tax-zones-rates.png){width="600" zoomable="yes"}

## 定义新税率

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Zones and Rates]**.

1. 在右上角，单击 **[!UICONTROL Add New Tax Rate]**.

   ![新税率](./assets/tax-rate-new.png){width="600" zoomable="yes"}

1. 输入 **[!UICONTROL Tax Identifier]**.

1. 要将税率应用于单个邮政编码，请输入 **[!UICONTROL Zip/Post Code]**.

   星号(`*`)可用于匹配代码中最多十个字符。 例如， `90*` 表示从90000到90999的所有邮政编码。

1. 要将税率应用于某个邮政编码范围，请执行以下操作：

   - 选择 **[!UICONTROL Zip/Post is Range]** 复选框，并通过输入第一个和最后一个邮政编码来定义范围 **[!UICONTROL Range From]** 和 **[!UICONTROL Range To]**.

     ![ZIP/Post为范围](./assets/tax-rate-new-zip-post-range.png){width="600" zoomable="yes"}

   - 选择 **[!UICONTROL State]** 适用税率的地方。

   - 选择 **[!UICONTROL Country]** 适用税率的地方。

   - 输入 **[!UICONTROL Rate Percent]** 用于计算税率。

1. 如果您有多个商店，则可以设置 **[!UICONTROL Tax Titles]** 每个商店视图。

   >[!NOTE]
   >
   >如果要使用税务标识符，请将此字段留空。

1. 完成后，单击 **[!UICONTROL Save Rate]**.

## 编辑现有税率

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Zones and Rates]**.

1. 在 _[!UICONTROL Tax Zones and Rates]_网格，并以编辑模式打开记录。

   如果列表中包含多个费率，请使用 [筛选器控件](../getting-started/admin-grid-controls.md) 找到所需的费率。

1. 对 **[!UICONTROL Tax Rate Information]**.

1. 更新 **[!UICONTROL Tax Titles]** 根据需要。

1. 完成后，单击 **[!UICONTROL Save Rate]**.

## 删除税率

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Zones and Rates]**.

1. 查找要删除的税率并在编辑模式下将其打开。

1. 在菜单栏中，单击 **[!UICONTROL Delete Rate]**.

1. 要确认操作，请单击 **[!UICONTROL OK]**.

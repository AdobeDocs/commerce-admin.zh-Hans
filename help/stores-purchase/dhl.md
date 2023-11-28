---
title: DHL
description: 了解如何将DHL设置为您商店的运输运营商。
exl-id: 765e5f90-3e93-43cf-a5bc-6132e00b506c
feature: Shipping/Delivery
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '580'
ht-degree: 0%

---

# DHL

DHL提供集成的国际服务和量身定制、以客户为中心的解决方案，用于管理和传输信件、货物和信息。

## 步骤1：启用DHL

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中，展开 **[!UICONTROL Sales]** 并选择 **[!UICONTROL Delivery Methods]**.

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL DHL]** 部分。

   >[!NOTE]
   >
   >如有必要，请先清除 **[!UICONTROL Use system value]** 复选框，以按所述更改以下设置。

1. 设置 **[!UICONTROL Enabled for Checkout]** 到 `Yes`.

1. 通常，您可以接受默认值 **[!UICONTROL Gateway URL]**.

   如果DHL为您提供了替代URL，请在此字段中输入该值。

1. 使用DHL提供的凭据完成以下字段：

   - **[!UICONTROL Access ID]**
   - **[!UICONTROL Password]**
   - **[!UICONTROL Account Number]**

![DHL帐户设置](../configuration-reference/sales/assets/delivery-methods-dhl-account-settings.png){width="600" zoomable="yes"}

## 步骤2；输入包描述和处理费

1. 在 **[!UICONTROL Content Type]** 列表中，选择最能描述所发运的包类型的选项：

   - `Documents`
   - `Non documents`

1. 根据您的要求配置手续费选项。

   手续费是可选的，显示为额外费用，将添加到DHL运输成本中。 如果要包括手续费，请执行以下操作：

   - 对象 **[!UICONTROL Calculate Handling Fee]**，选择要用于计算手续费的方法：

      - `Fixed`
      - `Percentage`

   - 对象 **[!UICONTROL Handling Applied]**，选择收取手续费的方式：

      - `Per Order`
      - `Per Package`

   - 对象 **[!UICONTROL Handling Fee]**，根据您选择用于计算金额的方法，输入要收取的金额。

     例如，如果费用基于固定费用，则以小数形式输入金额，如 `4.90`. 但是，如果手续费基于订单的百分比，则按百分比输入金额。 例如，如果您对订单的6%计费，则输入值为 `.06`.

   - 要允许分解订单总重量以确保准确计算发运费用，请设置 **[!UICONTROL Divide Order Weight]** 到 `Yes`.

   - 设置 **[!UICONTROL Weight Unit]** 包更改为以下任一项：

      - `Pounds`
      - `Kilograms`

   - 设置 **[!UICONTROL Size]** 将典型软件包更改为下列选项之一：

      - `Regular`
      - `Specific`

     如果您选择 `Specific`，输入 **[!UICONTROL Height]**， **[!UICONTROL Depth]**、和 **[!UICONTROL Width]** 以厘米为单位的包装材料。

   ![DHL包设置](../configuration-reference/sales/assets/delivery-methods-dhl-package-settings.png){width="600" zoomable="yes"}

## 步骤3：指定允许的投放方法

1. 对象 **[!UICONTROL Allowed Methods]**，选择您希望可供客户使用的每种方法。

   要选择多种方法，请按住Ctrl键(PC)或Command键(Mac)并单击每个选项。

   要显示正确的投放方法列表，您必须首先指定 [原产国/地区](../configuration-reference/sales/shipping-settings.md).

1. 对象 **[!UICONTROL Ready Time]**，输入在提交订单后，程序包准备发运的小时数。

1. 编辑 **[!UICONTROL Displayed Error Message]** 根据需要。

   如果所选的方法不可用，则会显示此消息。

1. 如果您要提供 [免费送货](shipping-free.md) 选项通过DHL，设置免费送货选项。

   - 对象 **[!UICONTROL Free Method]**，选择您喜欢用于免费配送的方法。

   - 设置 **[!UICONTROL Free Shipping Amount Threshold]**：

     `Enable`  — 如果提供最低订单的免运费，请输入 **[!UICONTROL Minimum Order Amount for Free Shipping]**.

     `Disable`  — 不对任何订单应用免费DHL装运。

     此设置类似于标准设置 _免费送货_ 方法，但出现在DHL部分，以便客户知道用于其订单的方法。

   - 对象 **[!UICONTROL Free Shipping Amount Threshold]**，输入订单达到免运费资格的最小金额。

     ![DHL允许的方法](../configuration-reference/sales/assets/delivery-methods-dhl-allowed-methods.png){width="600" zoomable="yes"}

## 第4步：指定适用的国家

1. 设置 **[!UICONTROL Ship to Applicable Countries]** 更改为以下任一项：

   - `All Allowed Countries`
   - `Specific Countries`

   如果发运到特定国家/地区，请从 **[!UICONTROL Ship to Specific Countries]** 列表。

1. 设置 **[!UICONTROL Show Method if Not Applicable]**：

   `Yes`  — 在结帐期间将DHL显示为送货方法，即使不适用于该订单也是如此。

   `No`  — 仅在适用的情况下，在签出期间将DHL显示为送货方法。

1. 要创建包含从您的商店发出的DHL发货详细信息的日志文件，请设置 **[!UICONTROL Debug]** 到 `Yes`.

1. 对象 **[!UICONTROL Sort Order]**，请输入数字以确定在结账期间与其他交付方法一起列出DHL时显示的顺序。

   `0` =第一个， `1` =秒， `2` =第三，依此类推。

1. 单击 **[!UICONTROL Save Config]**.

   ![DHL适用的国家/地区](../configuration-reference/sales/assets/delivery-methods-dhl-applicable-countries.png){width="600" zoomable="yes"}

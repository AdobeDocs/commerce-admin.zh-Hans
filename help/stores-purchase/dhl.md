---
title: DHL
description: 了解如何将DHL设置为您商店的运输运营商。
exl-id: 765e5f90-3e93-43cf-a5bc-6132e00b506c
feature: Shipping/Delivery
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '584'
ht-degree: 0%

---

# DHL

DHL提供集成的国际服务和量身定制、以客户为中心的解决方案，用于管理和传输信件、货物和信息。

## 步骤1：启用DHL

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧面板中，展开&#x200B;**[!UICONTROL Sales]**&#x200B;并选择&#x200B;**[!UICONTROL Delivery Methods]**。

1. 展开&#x200B;**[!UICONTROL DHL]**&#x200B;部分的![扩展选择器](../assets/icon-display-expand.png)。

   >[!NOTE]
   >
   >如有必要，请首先清除&#x200B;**[!UICONTROL Use system value]**&#x200B;复选框以更改以下设置，如所述。

1. 将&#x200B;**[!UICONTROL Enabled for Checkout]**&#x200B;设置为`Yes`。

1. 通常，您可以接受默认&#x200B;**[!UICONTROL Gateway URL]**。

   如果DHL为您提供了替代URL，请在此字段中输入该值。

1. 使用DHL提供的凭据完成以下字段：

   - **[!UICONTROL Access ID]**
   - **[!UICONTROL Password]**
   - **[!UICONTROL Account Number]**

![DHL帐户设置](../configuration-reference/sales/assets/delivery-methods-dhl-account-settings.png){width="600" zoomable="yes"}

## 步骤2；输入包描述和处理费

1. 在&#x200B;**[!UICONTROL Content Type]**&#x200B;列表中，选择最能描述您发运的程序包类型的选项：

   - `Documents`
   - `Non documents`

1. 根据您的要求配置手续费选项。

   手续费是可选的，显示为额外费用，将添加到DHL运输成本中。 如果要包括手续费，请执行以下操作：

   - 对于&#x200B;**[!UICONTROL Calculate Handling Fee]**，选择要用于计算手续费的方法：

      - `Fixed`
      - `Percentage`

   - 对于&#x200B;**[!UICONTROL Handling Applied]**，请选择您希望如何收取手续费：

      - `Per Order`
      - `Per Package`

   - 对于&#x200B;**[!UICONTROL Handling Fee]**，根据您选择用于计算金额的方法，输入要收取的金额。

     例如，如果费用基于固定费用，则以小数形式输入金额，如`4.90`。 但是，如果手续费基于订单的百分比，则按百分比输入金额。 例如，如果您对订单的6%收费，则输入值为`.06`。

   - 若要允许分解订单总重量以确保准确计算运费，请将&#x200B;**[!UICONTROL Divide Order Weight]**&#x200B;设置为`Yes`。

   - 将包的&#x200B;**[!UICONTROL Weight Unit]**&#x200B;设置为以下项之一：

      - `Pounds`
      - `Kilograms`

   - 将典型包的&#x200B;**[!UICONTROL Size]**&#x200B;设置为以下任一项：

      - `Regular`
      - `Specific`

     如果选择`Specific`，请输入包的&#x200B;**[!UICONTROL Height]**、**[!UICONTROL Depth]**&#x200B;和&#x200B;**[!UICONTROL Width]**（以厘米为单位）。

   ![DHL包设置](../configuration-reference/sales/assets/delivery-methods-dhl-package-settings.png){width="600" zoomable="yes"}

## 步骤3：指定允许的投放方法

1. 对于&#x200B;**[!UICONTROL Allowed Methods]**，请选择您希望可供客户使用的每个方法。

   要选择多种方法，请按住Ctrl键(PC)或Command键(Mac)并单击每个选项。

   要显示正确的传递方法列表，您必须首先指定[原产国](../configuration-reference/sales/shipping-settings.md)。

1. 对于&#x200B;**[!UICONTROL Ready Time]**，输入在提交订单后程序包准备发运的小时数。

1. 根据需要编辑&#x200B;**[!UICONTROL Displayed Error Message]**。

   如果所选的方法不可用，则会显示此消息。

1. 如果要通过DHL提供[免运费](shipping-free.md)选项，请设置免运费选项。

   - 对于&#x200B;**[!UICONTROL Free Method]**，请选择您喜欢用于免费送货的方法。

   - 设置&#x200B;**[!UICONTROL Free Shipping Amount Threshold]**：

     `Enable` — 如果提供最低订单的免运费，请输入&#x200B;**[!UICONTROL Minimum Order Amount for Free Shipping]**。

     `Disable` — 不向任何订单应用免费DHL装运。

     此设置类似于标准&#x200B;_Free Shipping_&#x200B;方法的设置，但显示在DHL部分中，这样客户就可以知道他们的订单使用了哪种方法。

   - 对于&#x200B;**[!UICONTROL Free Shipping Amount Threshold]**，输入订单可免费送货的最小金额。

     ![DHL允许的方法](../configuration-reference/sales/assets/delivery-methods-dhl-allowed-methods.png){width="600" zoomable="yes"}

## 第4步：指定适用的国家

1. 将&#x200B;**[!UICONTROL Ship to Applicable Countries]**&#x200B;设置为以下项之一：

   - `All Allowed Countries`
   - `Specific Countries`

   如果发运到特定国家/地区，请从&#x200B;**[!UICONTROL Ship to Specific Countries]**&#x200B;列表中选择每个国家/地区。

1. 设置&#x200B;**[!UICONTROL Show Method if Not Applicable]**：

   `Yes` — 在结帐期间将DHL显示为送货方法，即使不适用于该订单也是如此。

   `No` — 仅在适用的情况下，在签出期间将DHL显示为送货方法。

1. 若要创建包含从您的商店发出的DHL装运详细信息的日志文件，请将&#x200B;**[!UICONTROL Debug]**&#x200B;设置为`Yes`。

1. 对于&#x200B;**[!UICONTROL Sort Order]**，输入一个数字来确定在签出期间与其他传递方法一起列出DHL时显示的顺序。

   `0` =第一，`1` =第二，`2` =第三，依此类推。

1. 单击&#x200B;**[!UICONTROL Save Config]**。

   ![DHL适用的国家/地区](../configuration-reference/sales/assets/delivery-methods-dhl-applicable-countries.png){width="600" zoomable="yes"}

---
title: 美国邮政局(USPS)
description: 了解如何将USPS设置为商店的装运承运商。
exl-id: c9601fb8-f0f9-484a-a2e1-d50ee0f2dbf0
feature: Shipping/Delivery
source-git-commit: cace9d1de00955494d8bc607c017778ff7df4806
workflow-type: tm+mt
source-wordcount: '763'
ht-degree: 0%

---

# 美国邮政局(USPS)

美国邮政服务局是美国政府的一个独立邮政服务，通过陆空提供国内和国际航运服务。

## 步骤1：打开USPS装运帐户

打开[USPS Web工具](https://secure.shippingapis.com/registration/)帐户。 完成注册过程后，您将收到用户ID和USPS测试服务器的URL。

您还可以打开[USPS Web Tools](https://secure.shippingapis.com/registration/)帐户。 完成注册过程后，您将收到用户ID和USPS测试服务器的URL。 要了解有关USPS Web工具的更多信息，请参阅其[技术文档](https://www.usps.com/business/web-tools-apis/welcome.htm)。

## 步骤2：为存储启用USPS

{{$include /help/_includes/usps-api-type-configuration-note.md}}

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧面板中，展开&#x200B;**[!UICONTROL Sales]**&#x200B;并选择&#x200B;**[!UICONTROL Delivery Methods]**。

1. 展开![部分的](../assets/icon-display-expand.png)扩展选择器&#x200B;**[!UICONTROL USPS]**。

   >[!NOTE]
   >
   >如有必要，请首先取消选中&#x200B;**[!UICONTROL Use system value]**&#x200B;复选框以更改以下设置，如所述。

1. 将&#x200B;**[!UICONTROL Enabled for Checkout]**&#x200B;设置为`Yes`。

1. 如果您使用USPS REST API，请将&#x200B;**[!UICONTROL USPS Type]**&#x200B;设置为`USPS Rest APIs`。

   如果您使用的是USPS Web Tools API，请将&#x200B;**[!UICONTROL USPS Type]**&#x200B;设置为`USPS Web Tools API`。

1. 如果需要，输入&#x200B;**[!UICONTROL Gateway URL]**&#x200B;以访问USPS运费。

   该字段默认为预设，通常不需要更改。

1. 为签出期间显示的此配送方式输入&#x200B;**[!UICONTROL Title]**。

1. 使用USPS提供的凭据完成以下字段：

   如果您使用的是USPS Rest API，则必须提供以下凭据：

   - **[!UICONTROL Consumer Key]**
   - **[!UICONTROL Consumer Secret]**
   - **[!UICONTROL Pricing Options]**

   如果您使用的是USPS Web Tools API，则必须提供以下凭据：

   - **[!UICONTROL User ID]**
   - **[!UICONTROL Password]**

1. 将&#x200B;**[!UICONTROL Mode]**&#x200B;设置为以下项之一：

   - `Development` — 在测试环境中运行USPS。 在开发环境中运行USPS后，请确保稍后返回并将模式设置为`Live`。
   - `Live` — 在实时生产环境中运行USPS。

## 第3步：完成打包说明

1. 要确定在作为多个包发送时如何管理订单，请将&#x200B;**[!UICONTROL Packages Request Type]**&#x200B;设置为以下项之一：

   - `Divide to Equal Weight` - （一个请求）如果多个包的装运除以相等的权重，则可以作为一个请求提交这些包。
   - `Use Origin Weight` — （多个请求）如果使用原始重量作为计算运费的基础，则必须作为单独的请求提交多个包。

1. 将&#x200B;**[!UICONTROL Container]**&#x200B;设置为通常用于装运为商店订购的产品的包装类型。

1. 设置从商店发货的典型包的&#x200B;**[!UICONTROL Size]**。

1. 将&#x200B;**[!UICONTROL Machinable]**&#x200B;设置为以下项之一：

   - `Yes` — 如果您的典型包可以由计算机处理。
   - `No` — 如果必须手动处理您的典型包。

1. 根据运营商要求输入&#x200B;**[!UICONTROL Maximum Package Weight]**。

   ![USPS打包设置](../configuration-reference/sales/assets/delivery-methods-usps-packaging.png){width="600" zoomable="yes"}

## 第4步：设置手续费

手续费是可选的，显示为额外费用，将添加到DHL运输成本中。 如果要包括手续费，请执行以下操作：

1. 将&#x200B;**[!UICONTROL Calculate Handling Fee]**&#x200B;设置为以下方法之一：

   - `Fixed`
   - `Percent`

1. 要确定如何收取手续费，请将&#x200B;**[!UICONTROL Handling Applied]**&#x200B;设置为以下项之一：

   - `Per Order`
   - `Per Package`

1. 输入要收费的&#x200B;**[!UICONTROL Handling Fee]**&#x200B;的金额。

   要输入百分比，请使用小数格式。 例如，输入`0.25`表示25%。

   ![USPS处理费](../configuration-reference/sales/assets/delivery-methods-usps-handling-fee.png){width="600" zoomable="yes"}

## 步骤5：指定允许的方法和适用的国家/地区

1. 对于&#x200B;**[!UICONTROL Allowed Methods]**，选择客户可用的每个USPS送货方法。

   在签出过程中，方法显示在USPS下。 要选择多种方法，请按住Ctrl键(PC)或Command键(Mac)并单击每个选项。

1. 如果要通过USPS提供[免运费](shipping-free.md)选项，请设置免运费选项：

   - 将&#x200B;**[!UICONTROL Free Method]**&#x200B;设置为要用于免费配送的方法。 如果您不想通过USPS提供免运费，请选择`None`。

   - 若要要求符合USPS免费配送订单资格的最低订单金额，请将&#x200B;**[!UICONTROL Enable Free Shipping Threshold]**&#x200B;设置为`Enable`。 然后，输入&#x200B;**[!UICONTROL Free Shipping Amount Threshold]**&#x200B;中的最小值。

1. 如果需要，请更改&#x200B;**[!UICONTROL Displayed Error Message]**。

   此文本框预设了默认消息，但您可以输入在USPS不可用时要显示的其它消息。

   ![USPS允许的方法](../configuration-reference/sales/assets/delivery-methods-usps-allowed-methods.png){width="600" zoomable="yes"}

1. 将&#x200B;**[!UICONTROL Ship to Applicable Countries]**&#x200B;设置为以下项之一：

   - `All Allowed Countries` — 来自您商店配置中指定的所有[国家/地区](../getting-started/store-details.md#country-options)的客户都可以使用此交付方法。
   - `Specific Countries` — 选择此选项时，将显示&#x200B;_发送到特定国家/地区_&#x200B;列表。 选择列表中可使用此投放方法的每个国家/地区。

   ![USPS适用的国家/地区](../configuration-reference/sales/assets/delivery-methods-usps-countries.png){width="600" zoomable="yes"}

1. 将&#x200B;**[!UICONTROL Show Method if Not Applicable]**&#x200B;设置为以下项之一：

   - `Yes` — 列出结账期间所有可用的USPS装运方法，包括不适用于装运的方法。
   - `No` — 仅列出适用于装运的USPS装运方法。

1. 要创建包含从您的商店发出的USPS装运详细信息的日志文件，请将&#x200B;**[!UICONTROL Debug]**&#x200B;设置为`Yes`。

1. 对于&#x200B;**[!UICONTROL Sort Order]**，输入一个数字以确定在结账期间与其他交付方法一起列出USPS时的显示顺序。

   `0` =第一，`1` =第二，`2` =第三，依此类推。

1. 单击&#x200B;**[!UICONTROL Save Config]**。


<!-- Last updated from includes: 2025-11-26 10:55:00 -->

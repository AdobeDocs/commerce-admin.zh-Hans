---
title: 联合包裹服务(UPS)
description: 了解如何将UPS设置为您商店的配送运营商。
exl-id: a7965b2f-2473-4b63-a247-3b2230cde5d8
feature: Shipping/Delivery
source-git-commit: a925827f2d939eeb9e6b3e57c023792ae358cbfc
workflow-type: tm+mt
source-wordcount: '1013'
ht-degree: 0%

---

# 联合包裹服务(UPS)

联合包裹服务(UPS)向220多个国家提供国内和国际陆运和空运服务。

{{ups-api}}

>[!NOTE]
>
>UPS可以使用[维重量](carriers.md#dimensional-weight)来确定某些运费。 但是，Adobe Commerce仅支持基于重量的运输成本计算。

## 步骤1：打开UPS发运帐户

要为客户提供此配送方式，您必须首先打开UPS帐户，并完成申请以获取发货人帐号。 请参阅[打开一个免费的UPS帐户](https://www.ups.com/us/en/business-solutions/open-an-account)。

## 步骤2：获取UPS OAUTH凭据

按照[UPS API快速入门指南](https://developer.ups.com/get-started)中的步骤获取API凭据（客户端ID和客户端密钥）以启用UPS集成。 必须创建UPS应用程序才能获取凭据。

当您在Admin中配置UPS设置时，请使用`username`和`password`的凭据值。

## 步骤3：为您的存储启用UPS

1. 在&#x200B;_管理员侧栏_&#x200B;上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧面板的&#x200B;**[!UICONTROL Sales]**&#x200B;下，选择&#x200B;**[!UICONTROL Delivery Methods]**。

1. 展开![部分的](../assets/icon-display-expand.png)扩展选择器&#x200B;**[!UICONTROL UPS]**。

1. 将&#x200B;**[!UICONTROL Enabled for Checkout]**&#x200B;设置为`Yes`。

1. 对于UPS REST帐户（默认），请执行以下操作：

   - 输入您的UPS凭据： UPS客户端ID为&#x200B;**[!UICONTROL User ID]**，UPS客户端密钥为&#x200B;**[!UICONTROL Password]**。

   - 将&#x200B;**[!UICONTROL Mode]**&#x200B;设置为`Live`以通过安全连接将数据发送到UPS配送系统。 （开发模式不会通过安全连接发送数据。）

   - 验证发送请求所需的&#x200B;**[!UICONTROL Gateway URL]**。 将沙盒URL (`https://wwwcie.ups.com/api/rating/`)用于测试模式，将生产URL用于实时请求(`https://onlinetools.ups.com/api/rating/`)。 请确保对给定主机中的每个请求都使用各自的端点。

   - 验证获取跟踪信息所需的&#x200B;**[!UICONTROL Tracking URL]**。 将沙盒URL (`https://wwwcie.ups.com/api/track/`)用于测试模式，将生产URL用于实时请求(`https://onlinetools.ups.com/api/track/`)。 请确保对给定主机中的每个请求都使用各自的端点。

   - 将&#x200B;**[!UICONTROL Origin of the Shipment]**&#x200B;设置为装运来源区域。

   - 如果您对UPS有特殊费率，请将&#x200B;**[!UICONTROL Enable Negotiated Rates]**&#x200B;设置为`Yes`并输入UPS分配给您的六位数&#x200B;**[!UICONTROL Shipper Number]**。

   - 将&#x200B;**[!UICONTROL Live Account]**&#x200B;设置为以下项之一：

      - `Yes` — 在生产模式下运行UPS，并将UPS作为配送方式提供给您的客户。 请确保在网关URL和跟踪URL下使用正确的端点。
      - `No` — 在测试模式下运行UPS。 请确保在网关URL和跟踪URL下使用正确的端点。

   >[!NOTE]
   >
   >标准联合包裹服务类型已计划弃用。 对于新配置，使用默认`United Parcel Service REST`类型。 还需要REST类型才能生成[装运标签](shipping-labels.md)。<br/>
   >对于2.4.7版本，**[!UICONTROL UPS Type]**&#x200B;被删除，因为`UPS`和`UPS XML`类型已计划弃用，并且默认为`UPS REST`。 本机Adobe Commerce集成使用的United Parcel Service (UPS) API暂时被弃用，因为它当前不支持OAuth 2.0安全模型。

   >[!IMPORTANT]
   >
   >UPS将停止支持HTTP，它用于当前默认值（系统值）。 清除&#x200B;**[!UICONTROL Use system value]**&#x200B;复选框并修改URL以使用HTTPS。 示例： `https://www.ups.com/using/services/rave/qcostcgi.cgi`

1. 对于&#x200B;**[!UICONTROL Title]**，输入此送货选项在结帐时显示的名称。

   默认情况下，此字段设置为`United Parcel Service`。

   ![启用UPS](../configuration-reference/sales/assets/delivery-methods-ups1.png){width="600" zoomable="yes"}

## 步骤3：完成容器说明

1. 将&#x200B;**[!UICONTROL Packages Request Type]**&#x200B;设置为以下项之一：

   - `Use origin weight (few requests)`
   - `Divide to equal weight (one request)`

1. 对于&#x200B;**[!UICONTROL Container]**，请指定用于装运的典型包装类型：

   - `Customer Packaging`
   - `UPS Letter Envelope`
   - `Customer Supplied Package`
   - `UPS Tube`
   - `PAK`
   - `UPS Express Box`
   - `UPS Worldwide 25 kilo`
   - `UPS Worldwide 10 kilo`
   - `Pallet`
   - `Small Express Box`
   - `Medium Express Box`
   - `Large Express Box`

1. 将&#x200B;**[!UICONTROL Weight Unit]**&#x200B;设置为用于测量产品重量的系统。

   UPS支持的重量系统因国家/地区而异。 如有疑问，请询问UPS您应该使用哪个配重系统。 选项包括：

   - `LBS`
   - `KGS`

1. 将&#x200B;**[!UICONTROL Destination Type]**&#x200B;设置为以下项之一：

   - `Residential` — 您的装运大部分是企业对消费者(B2C)。
   - `Commercial` — 您的大多数装运都是企业对企业(B2B)。

1. 输入运营商允许的&#x200B;**[!UICONTROL Maximum Package Weight]**。

1. 将&#x200B;**[!UICONTROL Pickup Method]**&#x200B;设置为以下项之一：

   - `Regular Daily Pickup`
   - `On Call Air`
   - `One Time Pickup`
   - `Letter Center`
   - `Customer Counter`

1. 输入运营商允许的&#x200B;**[!UICONTROL Minimum Package Weight]**。

   ![容器说明](./assets/ups2.png){width="600" zoomable="yes"}

## 步骤5：设置手续费

处理费是可选的，显示为额外费用，将添加到UPS运输成本中。 如果要包括手续费，请执行以下操作：

1. 将&#x200B;**[!UICONTROL Calculate Handling Fee]**&#x200B;设置为以下方法之一：

   - `Fixed`
   - `Percent`

1. 要确定如何收取手续费，请将&#x200B;**[!UICONTROL Handling Applied]**&#x200B;设置为以下项之一：

   - `Per Order`
   - `Per Package`

1. 输入要收费的&#x200B;**[!UICONTROL Handling Fee]**&#x200B;的金额。

   要输入百分比，请使用小数格式。 例如，输入`0.25`表示25%。

   ![手续费](./assets/ups3.png){width="600" zoomable="yes"}

## 步骤6：指定允许的方法和适用的国家/地区

1. 对于&#x200B;**[!UICONTROL Allowed Methods]**，请选择客户可用的每种UPS配送方式。

   签出期间，这些方法显示在UPS下。 要选择多种方法，请按住Ctrl键(PC)或Command键(Mac)并单击每个选项。

1. 如果要通过UPS提供[免运费](shipping-free.md)选项，请设置免运费选项：

   - 将&#x200B;**[!UICONTROL Free Method]**&#x200B;设置为要用于免费配送的方法。 如果不希望通过UPS提供免费送货，请选择`None`。

   - 若要要求满足订单免费送货条件的最低订单金额，请将&#x200B;**[!UICONTROL Enable Free Shipping Threshold]**&#x200B;设置为`Enable`。 然后，输入&#x200B;**[!UICONTROL Free Shipping Amount Threshold]**&#x200B;中的最小值。

1. 如果需要，请更改&#x200B;**[!UICONTROL Displayed Error Message]**。

   此文本框预设了默认消息，但您可以输入在UPS不可用时要显示的其它消息。

   ![允许的方法](./assets/ups4.png){width="600" zoomable="yes"}

1. 将&#x200B;**[!UICONTROL Ship to Applicable Countries]**&#x200B;设置为以下项之一：

   - `All Allowed Countries` — 来自您商店配置中指定的所有[国家/地区](../getting-started/store-details.md#country-options)的客户都可以使用此交付方法。
   - `Specific Countries` — 选择此选项时，将显示&#x200B;_发送到特定国家/地区_&#x200B;列表。 选择列表中可使用此投放方法的每个国家/地区。

1. 将&#x200B;**[!UICONTROL Show Method if Not Applicable]**&#x200B;设置为以下项之一：

   - `Yes` — 列出结帐期间所有可用的UPS配送方式，包括不适用于配送的方法。
   - `No` — 仅列出适用于装运的UPS装运方法。

   ![适用的国家/地区](./assets/ups5.png){width="600" zoomable="yes"}

1. 要创建包含从您的商店发出的UPS装运详细信息的日志文件，请将&#x200B;**[!UICONTROL Debug]**&#x200B;设置为`Yes`。

1. 对于&#x200B;**[!UICONTROL Sort Order]**，请输入一个数字以确定在签出期间与其他传递方法一起列出UPS时的显示顺序。

   `0` =第一，`1` =第二，`2` =第三，依此类推。

1. 单击&#x200B;**[!UICONTROL Save Config]**。

## 步骤7：设置发运来源地址

1. 确保您的[存储信息](../getting-started/store-details.md#store-information)已完成。

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧面板中，展开&#x200B;**[!UICONTROL Sales]**&#x200B;并选择&#x200B;**[!UICONTROL Shipping Settings]**。

1. 展开页面上的![扩展选择器](../assets/icon-display-expand.png) **[!UICONTROL Origin]**&#x200B;并配置送货来源地址。

   ![销售配置 — 发货地址选项](./assets/shipping-origin.png){width="600" zoomable="yes"}

1. 单击&#x200B;**[!UICONTROL Save Config]**。

>[!NOTE]
>
>计算运费时，Commerce不向UPS申报完整订单价格。 此行为无法更改。

---
title: 美国邮政局(USPS)
description: 了解如何将USPS设置为商店的装运承运商。
exl-id: c9601fb8-f0f9-484a-a2e1-d50ee0f2dbf0
feature: Shipping/Delivery
source-git-commit: 06673ccb7eb471d3ddea97218ad525dd2cdcf380
workflow-type: tm+mt
source-wordcount: '746'
ht-degree: 0%

---

# 美国邮政局(USPS)

美国邮政服务局是美国政府的一个独立邮政服务，通过陆空提供国内和国际航运服务。

## 步骤1：打开USPS装运帐户

打开 [USPS Web Tools][1] 帐户。 完成注册过程后，您将收到用户ID和USPS测试服务器的URL。

您也可以打开 [USPS Web Tools][1] 帐户。 完成注册过程后，您将收到用户ID和USPS测试服务器的URL。 要了解有关USPS Web工具的更多信息，请参阅他们的 [技术文档][2].

## 步骤2：为存储启用USPS

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中，展开 **[!UICONTROL Sales]** 并选择 **[!UICONTROL Delivery Methods]**.

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL USPS]** 部分。

   >[!NOTE]
   >
   >如有必要，请首先取消选择 **[!UICONTROL Use system value]** 复选框，以按所述更改以下设置。

1. 设置 **[!UICONTROL Enabled for Checkout]** 到 `Yes`.

1. 如果需要，请输入 **[!UICONTROL Gateway URL]** 访问USPS运费。

   >[!IMPORTANT]
   >
   >自2021年6月24日起，USPS Web Tools将取消对所有不安全HTTP端点的支持。 进行此更改后，所有对不安全HTTP端点的Web工具API请求都将失败。 确保您的 **[!UICONTROL Gateway URL]** 使用安全HTTPS端点。

   该字段默认为预设，通常不需要更改。

1. 输入 **[!UICONTROL Title]** 对于结帐期间显示的这种配送方式。

1. 输入 **[!UICONTROL User ID]** 和 **[!UICONTROL Password]** 你的USPS帐户。

1. 设置 **[!UICONTROL Mode]** 更改为以下任一项：

   - `Development`  — 在测试环境中运行USPS。 在开发环境中运行USPS后，请确保稍后返回，并将模式设置为 `Live`.
   - `Live`  — 在实时生产环境中运行USPS。

## 第3步：完成打包说明

1. 要确定在作为多个包发送时如何管理订单，请设置 **[!UICONTROL Packages Request Type]** 更改为以下任一项：

   - `Divide to Equal Weight`  — （一个请求）如果多个包裹的发运量除以相等的权重，则可以作为一个请求提交。
   - `Use Origin Weight`  — （多个请求）如果使用原始重量作为计算运费的基础，则必须作为单独的请求提交多个包。

1. 设置 **[!UICONTROL Container]** 与通常用于装运商店所订购产品的包装类型相对应。

1. 设置 **[!UICONTROL Size]** 从商店发货的典型产品包中。

1. 设置 **[!UICONTROL Machinable]** 更改为以下任一项：

   - `Yes`  — 如果您的典型软件包可以由计算机处理。
   - `No`  — 如果必须手动处理您的典型程序包。

1. 输入 **[!UICONTROL Maximum Package Weight]** 根据运营商的要求。

   ![USPS打包设置](../configuration-reference/sales/assets/delivery-methods-usps-packaging.png){width="600" zoomable="yes"}

## 第4步：设置手续费

手续费是可选的，显示为额外费用，将添加到DHL运输成本中。 如果要包括手续费，请执行以下操作：

1. 设置 **[!UICONTROL Calculate Handling Fee]** 更改为以下方法之一：

   - `Fixed`
   - `Percent`

1. 要确定如何应用手续费，请设置 **[!UICONTROL Handling Applied]** 更改为以下任一项：

   - `Per Order`
   - `Per Package`

1. 输入 **[!UICONTROL Handling Fee]** 将被收费。

   要输入百分比，请使用小数格式。 例如，输入 `0.25` 25%。

   ![USPS手续费](../configuration-reference/sales/assets/delivery-methods-usps-handling-fee.png){width="600" zoomable="yes"}

## 步骤5：指定允许的方法和适用的国家/地区

1. 对象 **[!UICONTROL Allowed Methods]**，选择客户可用的每个USPS配送方式。

   在签出过程中，方法显示在USPS下。 要选择多种方法，请按住Ctrl键(PC)或Command键(Mac)并单击每个选项。

1. 如果您要提供 [免费送货](shipping-free.md) 选项通过USPS，设置免运费选项：

   - 设置 **[!UICONTROL Free Method]** 到您要用于免费配送的方法。 如果您不想通过USPS提供免运费，请选择 `None`.

   - 要要求满足订单与USPS免费发运条件的最低订单金额，请设置 **[!UICONTROL Enable Free Shipping Threshold]** 到 `Enable`. 然后，输入最小值 **[!UICONTROL Free Shipping Amount Threshold]**.

1. 如果需要，请更改 **[!UICONTROL Displayed Error Message]**.

   此文本框预设了默认消息，但您可以输入在USPS不可用时要显示的其它消息。

   ![USPS允许的方法](../configuration-reference/sales/assets/delivery-methods-usps-allowed-methods.png){width="600" zoomable="yes"}

1. 设置 **[!UICONTROL Ship to Applicable Countries]** 更改为以下任一项：

   - `All Allowed Countries`  — 来自所有客户的客户 [国家/地区](../getting-started/store-details.md#country-options) 在商店配置中指定的可使用此投放方法。
   - `Specific Countries`  — 选择此选项时， _发运至特定国家/地区_ 列表出现。 选择列表中可使用此投放方法的每个国家/地区。

   ![USPS适用的国家/地区](../configuration-reference/sales/assets/delivery-methods-usps-countries.png){width="600" zoomable="yes"}

1. 设置 **[!UICONTROL Show Method if Not Applicable]** 更改为以下任一项：

   - `Yes`  — 列出结账期间所有可用的USPS装运方法，包括不适用于装运的方法。
   - `No`  — 仅列出适用于装运的USPS装运方法。

1. 要创建包含从您的商店发出的USPS装运详细信息的日志文件，请设置 **[!UICONTROL Debug]** 到 `Yes`.

1. 对象 **[!UICONTROL Sort Order]**，请输入数字以确定在结账期间与其他交付方法一起列出USPS时的显示顺序。

   `0` =第一个， `1` =秒， `2` =第三，依此类推。

1. 单击 **[!UICONTROL Save Config]**.


[1]: https://secure.shippingapis.com/registration/
[2]: https://www.usps.com/business/web-tools-apis/welcome.htm

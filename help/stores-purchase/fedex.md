---
title: 联邦快递
description: 了解如何将FedEx设置为您商店的运输运营商。
exl-id: 75bb3ed1-3ae9-418a-be90-888046b28a7b
feature: Shipping/Delivery
source-git-commit: 50b44190a9568a8d6ad38ab29177904596569d75
workflow-type: tm+mt
source-wordcount: '849'
ht-degree: 0%

---

# 联邦快递

联邦快递是世界上最大的航运服务公司之一，提供航空、货运和陆运服务，有几个优先级别。

![结账时的FedEx送货选项](./assets/storefront-checkout-shipping-fedex.png){width="700" zoomable="yes"}

>[!NOTE]
>
>联邦快递可以使用 [维度权重](carriers.md#dimensional-weight) 以确定一些运费。 但是，Adobe Commerce和Magento Open Source仅支持基于重量的运输成本计算。

## 步骤1：注册FedEx Web服务生产

A [联邦快递商家账户][1] 需要注册FedEx Web服务生产访问。 创建FedEx帐户后，通读生产帐户信息页面，然后单击 _获取生产密钥_ 页面底部的链接，用于注册和获取密钥。

>[!NOTE]
>
>请确保复制或写下身份验证密钥。 必须在Commerce配送设置中设置联邦快递。

## 步骤2：为您的存储启用FedEx

{{beta2-updates}}

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中，展开 **[!UICONTROL Sales]** 并选择 **[!UICONTROL Delivery Methods]**.

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL FedEx]** 部分。

1. 设置 **[!UICONTROL Enabled for Checkout]** 到 `Yes`.

1. 对象 **[!UICONTROL Title]**，输入在结账期间标识FedEx配送方法的标题。

1. 从联邦快递帐户输入以下信息：

   - **[!UICONTROL Account ID]**
   - **[!UICONTROL Meter Number]**
   - **[!UICONTROL Key]**
   - **[!UICONTROL Password]**

1. 如果您已设置FedEx沙盒并希望在测试环境中工作，请设置 **[!UICONTROL Sandbox Mode]** 到 `Yes`.

   >[!NOTE]
   >
   >请记得将沙盒模式设置为 `No` 准备将FedEx作为配送方式提供给客户时。

   ![联邦快递帐户设置](../configuration-reference/sales/assets/delivery-methods-fedex-account-settings.png){width="600" zoomable="yes"}

## 步骤3：包描述和处理费

1. 选择 **[!UICONTROL Packages Request Type]** 要将订单拆分为多个发运时，最能说明您的首选项的选项：

   - `Divide to equal weight (one request)`
   - `Use origin weight (few requests)`

1. 选择类型 **[!UICONTROL Packaging]** 通常用于从您的商店发运产品。

1. 设置 **[!UICONTROL Dropoff]** 用于交货的提货方式。

   - `Regular Pickup`  — 如果发货量很大，与联邦快递安排定期取货可能具有成本效益。

   - `Request Courier`  — 您必须致电并请求联邦快递快递取货。

   - `Drop Box`  — 您必须在附近的联邦快递托运箱卸货。

   - `Business Service Center`  — 您必须在当地联邦快递商务服务中心卸货。

   - `Station`  — 您必须在当地联邦快递站卸货。

1. 设置 **[!UICONTROL Weight Unit]** 到在区域设置中使用的度量单位。

   - `Pounds`
   - `Kilograms`

1. 输入 **[!UICONTROL Maximum Package Weight]** 允许联邦快递发货。

   默认的FedEx最大重量为150磅。 有关更多信息，请咨询您的承运商。 除非您与FedEx进行了特殊安排，否则建议使用默认值。 请参阅 [维度权重](carriers.md#dimensional-weight) 以了解更多信息。

   ![FedEx包设置](../configuration-reference/sales/assets/delivery-methods-fedex-packaging.png){width="600" zoomable="yes"}

1. 根据您的要求配置手续费选项。

   处理费是可选的，在结账期间不可见。 如果要包括手续费，请执行以下操作：

   - 设置 **[!UICONTROL Calculate Handling Fee]**：

      - `Fixed Fee`
      - `Percentage`

   - 对象 **[!UICONTROL Handling Applied]**，请选择以下方法之一来管理手续费：

      - `Per Order`
      - `Per Package`

   - 输入 **[!UICONTROL Handling Fee]** 作为 `fixed` 金额或 `percentage`，具体取决于计算方法。

1. 设置 **[!UICONTROL Residential Delivery]** 更改为以下任一项，具体取决于您销售的是企业对消费者(B2C)还是企业对企业(B2B)。

   - `Yes`  — 用于B2C住宅投放。
   - `No`  — 用于B2B住宅投放。

   ![FedEx处理费设置](../configuration-reference/sales/assets/delivery-methods-fedex-handling-fee.png){width="600" zoomable="yes"}

## 步骤4：允许的方法和适用的国家

1. 设置 **[!UICONTROL Allowed Methods]** 您想要提供的每种配送方式。

   在选择方法时，请考虑联邦快递帐户、发货频率和大小，以及是否允许国际发货。 您可以提供所需数量的方法，例如：

   - 欧洲第一要务
   - 交货日期选项：1天运费、2天运费、2天上午、2天运费、3天运费
   - 国内期权 — Express Saver、Ground、First、Onight、Home Delivery、Standard Onight
   - 国际选择 — 国际经济、国际经济货运、国际优先、国际地面、国际、优先国际
   - 优先级选项 — 运费，优先级隔夜
   - 智能开机自检提供Smart Post方法(输入 **中心编号**)
   - 运费选项 — 运费，国家运费

1. 如果您要提供 [免费送货](shipping-free.md) 选项通过FedEx，设置免运费选项。

   - 设置 **[!UICONTROL Free Method]** 到您要用于免费配送的方法。 如果您不想通过FedEx提供免运费，请选择 `None`.

   - 要要求满足订单与FedEx免费配送资格的最低订单金额，请设置 **[!UICONTROL Enable Free Shipping Threshold]** 到 `Enable`. 然后，输入最小值 **[!UICONTROL Free Shipping Amount Threshold]**.

   此设置类似于标准“免运费”方法中的设置，但会在结账时显示在FedEx部分中，这样客户就可以知道用于其订单的方法。

1. 如果需要，请更改 **[!UICONTROL Displayed Error Message]**.

   此文本框预设了默认消息，但您可以输入在FedEx不可用时要显示的其它消息。

   ![FedEx允许的投放方法](../configuration-reference/sales/assets/delivery-methods-fedex-delivery-methods.png){width="600" zoomable="yes"}

1. 设置 **[!UICONTROL Ship to Applicable Countries]**：

   - `All Allowed Countries`  — 来自所有客户的客户 [国家/地区](../getting-started/store-details.md#country-options) 在商店配置中指定的可使用此投放方法。

   - `Specific Countries`  — 选择此选项时， _发运至特定国家/地区_ 列表出现。 选择列表中可使用此投放方法的每个国家/地区。

1. 如果要保留商店与FedEx系统之间所有通信的日志，请设置 **[!UICONTROL Debug]** 到 `Yes`.

1. 设置 **[!UICONTROL Show Method if Not Applicable]**：

   - `Yes`  — 向客户显示所有FedEx配送方式，无论其是否可用。
   - `No`  — 仅显示适用于订单的FedEx配送方式。

1. 对象 **[!UICONTROL Sort Order]**，请输入数字以确定在结账期间与其他投放方法一起列出FedEx时的显示顺序。

   `0` =第一个， `1` =秒， `2` =第三，依此类推。

1. 单击 **[!UICONTROL Save Config]**.

   ![FedEx适用国家/地区](../configuration-reference/sales/assets/delivery-methods-fedex-applicable-countries.png){width="600" zoomable="yes"}

>[!NOTE]
>
>计算运费时，Commerce始终向FedEx声明完整的订单价格。 此行为无法更改。

[1]: https://www.fedex.com/login/web/jsp/contactInfo1.jsp

---
title: 创建装运标签和包装
description: 了解如何按订单打包项目并创建配送标签。
exl-id: ed9be72a-0dcd-4dbf-82ba-b1d75a1e76fd
feature: Shipping/Delivery, Orders
source-git-commit: c9acf475eeadcd249467e4cc89fe61d37230bd7d
workflow-type: tm+mt
source-wordcount: '1944'
ht-degree: 0%

---

# 创建配送标签

要创建装运标签，您必须首先设置装运承运人帐户以支持标签。 然后，按照提示输入软件包及其内容的说明。

在您配置装运标签信息并提交订单后，Commerce将连接到装运承运人系统，提交订单，并接收装运标签和跟踪编号。 如果系统中存在此装运的装运标签，则用新标签替换。 但是，不会替换现有跟踪编号。 任何新跟踪编号将添加到现有跟踪编号。

## 步骤1：联系您的承运商

在开始之前，请确保将您的配送帐户设置为处理标签。 某些运营商可能会收取额外的费用，以便向您的帐户添加运输标签。

联系您用于启用商店装运标签的每个承运商。

按照每个运营商提供的说明为您的帐户添加运货标签支持。

- **FedEx** — 联系[FedEx Web Integration Services][1]，了解您帐户的标签打印要求。
- **USPS** — 请参阅托运人支持中心下的[Web工具API门户][4]，了解如何设置标签打印凭据。
- **UPS** — 联系[UPS][2]，确认您的帐户支持运送标签。 要生成发运标签，您必须使用UPS XML选项。
- **DHL** — 联系[DHL电子商务解决方案][3]，了解您帐户的标签打印要求。

## 步骤2：更新每个运营商的配置

1. 确保您的[存储信息](../getting-started/store-details.md#store-information)已完成。

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧面板中，展开&#x200B;**[!UICONTROL Sales]**&#x200B;并选择&#x200B;**[!UICONTROL Shipping Settings]**。

1. 展开![扩展选择器](../assets/icon-display-expand.png) **[!UICONTROL Origin]**&#x200B;部分并配置&#x200B;**[!UICONTROL Shipping Origin Address]**。

1. 对于已激活进行标签打印的每个承运人帐户，请按照下面的说明操作。

### UPS配置

美国联合包裹服务公司在国内和国际上都有船只。 但是，只能为源自美国的货物生成装运标签。

1. 在左侧面板的&#x200B;_[!UICONTROL Sales]_部分中，选择&#x200B;**[!UICONTROL Delivery Methods]**。

1. 展开![部分的](../assets/icon-display-expand.png)扩展选择器&#x200B;**[!UICONTROL UPS]**。

1. 验证您的UPS **[!UICONTROL Shipper Number]**&#x200B;是否正确。

   仅当启用[!DNL United Parcel Service XML]时，才会显示您的发货人编号。

1. 单击&#x200B;**[!UICONTROL Save Config]**。

### USPS配置

[!DNL United States Postal Service]在国内和国际上都发货。

{{$include /help/_includes/usps-api-type-configuration-note.md}}

1. 在&#x200B;**[!UICONTROL Delivery Methods]**&#x200B;配置中继续，展开![部分的](../assets/icon-display-expand.png)扩展选择器&#x200B;**[!UICONTROL USPS]**。

1. 选择&#x200B;**[!UICONTROL USPS Type]**&#x200B;作为`USPS Rest APIs`或`USPS Web Tools API`。

1. 验证&#x200B;**[!UICONTROL Secure Gateway URL]**&#x200B;是否正确。

1. 输入USPS提供给您的&#x200B;**[!UICONTROL Password]**。

1. 验证基于所选&#x200B;**[!UICONTROL USPS Type]**&#x200B;的以下配置是否完成：

   如果您使用的是USPS Web Tools API：
   - 用户ID
   - 密码

   如果您使用的是USPS REST API：
   - 使用者密钥
   - 使用者密码
   - 定价选项
   - 帐户类型
   - 帐号
   - 客户注册ID (CRID)
   - 邮件程序标识符(MID)
   - 清单MID
   - AES/ITN

1. 将&#x200B;**[!UICONTROL Size]**&#x200B;设置为`Large`并输入以下维度的值：

   - 长度
   - 宽度
   - 高度
   - 环状

1. 单击&#x200B;**[!UICONTROL Save Config]**。

### FedEx配置

联邦快递在国内和国际上发货。 位于美国境外的商店只能为国际货运创建联邦快递标签。

1. 在&#x200B;**[!UICONTROL Delivery Methods]**&#x200B;配置中继续，展开![部分的](../assets/icon-display-expand.png)扩展选择器&#x200B;**[!UICONTROL FedEx]**。

1. 验证以下FedEx凭据是否正确：

   - 计量器编号
   - 键
   - 密码

1. 单击&#x200B;**[!UICONTROL Save Config]**。

### DHL配置

DHL提供国际航运服务。

1. 在&#x200B;**[!UICONTROL Delivery Methods]**&#x200B;配置中继续，展开![部分的](../assets/icon-display-expand.png)扩展选择器&#x200B;**[!UICONTROL DHL]**。

1. 验证&#x200B;**[!UICONTROL Gateway URL]**&#x200B;是否正确。

1. 验证以下凭证是否已完成：

   - 访问ID
   - 密码
   - 帐号

1. 单击&#x200B;**[!UICONTROL Save Config]**。

## 步骤3：创建配送标签

### 方法1：为新发运创建标签

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Sales]** > **[!UICONTROL Orders]**。

1. 在网格中查找订单，然后打开记录。

   订单的状态必须为`Pending`或`Processing`。

1. 单击右上角的&#x200B;**[!UICONTROL Ship]**。

1. 根据承运人要求确认装运信息。

1. 在右下角，选中&#x200B;**[!UICONTROL Create Shipping Label]**&#x200B;复选框。

1. 单击&#x200B;**[!UICONTROL Submit Shipment]**。

1. 在包中添加或更新产品：

   - 要将订单中的产品添加到包，请单击&#x200B;**[!UICONTROL Add Products]**。 _[!UICONTROL Quantity]_列显示可用于包的最大产品数。

   - 选中要添加到包中的每个产品的复选框，然后输入每个产品的&#x200B;**[!UICONTROL Quantity]**。 然后，单击&#x200B;**[!UICONTROL Add Selected Product(s) to Package]**。

   - 要添加包，请单击&#x200B;**[!UICONTROL Add Package]**。

   - 要删除包，请单击&#x200B;**[!UICONTROL Delete Package]**。

   - 要取消订单，请单击&#x200B;**[!UICONTROL Cancel]**。 未创建送货标签，并且清除了&#x200B;_[!UICONTROL Create Shipping Label]_复选框。

   >[!NOTE]
   >
   >如果您使用默认包装类型以外的包装类型或需要签名，则运输成本可能会不同于您向客户收取的费用。 任何运费差异都不会反映在您的商店中。

1. 单击&#x200B;**[!UICONTROL OK]**。

   Commerce连接到装运承运人系统，提交订单，并接收每个包的装运标签和跟踪编号。

### 方法2：为现有发运创建标签

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**。

1. 在网格中查找订单并打开装运表单。

1. 在&#x200B;_[!UICONTROL Shipping and Tracking Information]_部分中，单击&#x200B;**[!UICONTROL Create Shipping Label]**。

1. 将订购的产品分发到相应的包中，然后单击&#x200B;**[!UICONTROL OK]**。

1. 要查看包信息，请单击&#x200B;**[!UICONTROL Show Packages]**。

## 步骤4：打印标签

配送标签以PDF格式生成，并可从管理员处打印。 每个标签包括订单编号和包装编号。

>[!NOTE]
>
>由于为每个包创建了单独的装运订单，因此可能会为单个装运接收多个装运标签。

### 方法1：打印装运表单中的标签

1. 在&#x200B;_管理员侧栏_&#x200B;上，转到以下页面之一，然后找到装运记录：

   - **[!UICONTROL Sales]** > **[!UICONTROL Orders]** — 在网格中查找订单并打开记录。 在左侧面板中，选择&#x200B;**[!UICONTROL Shipments]**。 然后，打开装运记录。

   - **[!UICONTROL Sales]** > **[!UICONTROL Shipments]** — 在网格中查找装运并打开记录。

1. 要下载PDF文件，请转到表单的&#x200B;_[!UICONTROL Shipping and Tracking]_部分，然后单击&#x200B;**[!UICONTROL Print Shipping Label]**。

   根据您的浏览器设置，可以直接从PDF文件查看和打印送货标签。

   _[!UICONTROL Print Shipping Label]_按钮仅在承运人为装运生成标签后显示。 如果缺少按钮，请单击&#x200B;**[!UICONTROL Create Shipping Label]**。 在Commerce收到来自运营商的标签后，将会显示按钮。

### 方法2：打印多个订单的标签

1. 在&#x200B;_管理员侧栏_&#x200B;上，转到以下页面之一，然后选择订单或装运以进行打印：

   - **[!UICONTROL Sales]** > **[!UICONTROL Orders]** — 在网格中，选中要打印装运标签的每个订单的复选框。

   - **[!UICONTROL Sales]** > **[!UICONTROL Shipments]** — 在网格中，选中每个包含要打印标签的装运的复选框。

1. 将&#x200B;**[!UICONTROL Actions]**&#x200B;控件设置为`Print Shipping Labels`。

1. 单击&#x200B;**[!UICONTROL Submit]**。

系统会为与选定订单相关的每次发运打印一整套发运标签。

## 必需运营商设置

| 字段 | 描述 |
|--- |--- |
| [!UICONTROL Type] | 包装类型因载体和方法而异。 最初会选择每个承运人的默认包装类型。 USPS不需要国内装运的包装类型。 |
| [!UICONTROL Customs Value] | （仅限国际装运）国际装运货物内容的申报价值或销售价格。 |
| [!UICONTROL Total Weight] | 系统会自动计算添加到包的所有产品的总重量。 该值也可以手动更改，并输入为磅或千克。 |
| [!UICONTROL Length, Width, Height] | （可选）包维度仅用于自定义包。 可将度量单位指定为英寸或厘米。<br/><br/>**[!UICONTROL Not Required]**：装运承运人未向商店发送任何交货确认。<br/><br/>**[!UICONTROL No Signature]**：运输运营商将没有收件人签名的交货确认发送到商店。<br/><br/>**[!UICONTROL Signature Required]**：装运承运人获取收件人的签名并向商店提供打印副本。<br/><br/>**[!UICONTROL Direct]**： （仅限FedEx） FedEx从投放地址中的某人获取签名。 如果没有人签名该程序包，承运人将在另一时间尝试交付该程序包。<br/><br/>**[!UICONTROL Indirect]**： （仅限FedEx住宅投放） FedEx在投放地址获取某人（可能是邻居或建筑经理）的签名。 收件人可以留下已签名的FedEx门标签，以授权在没有任何人在场的情况下留下包裹。<br/><br/>**[!UICONTROL Contents]**： （仅限USPS）选择以下包描述之一： <br/>- Gift<br/>- Documents<br/>- Commercial Sample<br/>- Returned Goods<br/>- Commercial<br/>- Other <br/><br/>**[!UICONTROL Explanation]**： （仅限USPS）包内容的详细说明。<br/><br/>**[!UICONTROL Adult Required]**：装运承运人获得成人收件人的签名并向商店提供打印副本。 |

{style="table-layout:auto"}

## 创建包

当您选择创建送货标签时，将显示&#x200B;_[!UICONTROL Create Packages]_窗口。 您可以立即开始配置第一个包。

### 配置包

>[!NOTE]
>
>如果您为[!UICONTROL Type]选择了非默认值或选择要求签名确认，则装运的价格可能与您向客户收取的价格不同。

1. 要查看已发运产品的列表并将它们添加到包中，请单击&#x200B;**[!UICONTROL Add Products]**。

   - 指定产品和数量。

     _[!UICONTROL Qty]_列显示可添加的最大数量。 对于第一个包，编号是产品要发运的总数量。

   - 要将产品添加到包，请单击&#x200B;**[!UICONTROL Add Selected Product(s) to Package]**。

1. 要添加包，请单击&#x200B;**[!UICONTROL Add Package]**。

   您可以添加多个包并同时编辑它们。

1. 要删除包，请单击&#x200B;**[!UICONTROL Delete Package]**。

将产品添加到包后，无法直接编辑数量。

### 增加数量

1. 单击&#x200B;**[!UICONTROL Add Selection]**。

1. 输入附加数量。

   编号将添加到包中产品的上一个数量。

### 减少数量

1. 从包中删除产品。

1. 单击&#x200B;**[!UICONTROL Add Selection]**。

1. 输入新的较小值。

### 生成装运标签

分发所有产品后，要使用的资源包总数等于列表中最后一个资源包的数目。 在所有装运的项目都分发到包并完成所有必要的信息之前，_确定_&#x200B;按钮处于禁用状态。

要生成标签，请单击&#x200B;**[!UICONTROL OK]**。

如果需要，您可以单击&#x200B;**[!UICONTROL Cancel]**&#x200B;停止该进程。 包未保存，并且送货标签过程被取消。

### 字段描述

| 字段 | 描述 |
|--- |--- |
| [!UICONTROL Type] | 指定包的类型。 选择一个预定义值。 每个装运承运人的可用包装类型不同。 当“创建货包”弹出窗口打开时，发运承运人的默认货包将显示在“类型”字段中。 如果您选择的包装不是由装运承运人设计的，则必须输入包装的尺寸。 对于为DHL、FedEx和UPS装运创建的装运标签，“货物类型”字段设置为`Merchandise`。 对于USPS，该字段反映了&#x200B;_窗口中_ Contents _[!UICONTROL Create Packages]_字段的值。 |
| [!UICONTROL Total Weight] | 程序包的总重。 该字段已预先填充了包中产品的总重量。 度量单位可以设置为磅或千克。 |
| [!UICONTROL Length] | 程序包长度、整数和浮点数。 如果使用自定义包类型，则会启用该字段。 测量单位可设置为英寸或厘米。 |
| [!UICONTROL Width] | 包的宽度、整数和浮点数。 如果使用自定义包类型，则会启用该字段。 可以使用“高度”字段旁边的下拉菜单指定度量单位；在英寸和厘米之间选择。 |
| [!UICONTROL Height] | 程序包的高度、整数和浮点数。 如果使用自定义包类型，则会启用该字段。 可以使用“高度”字段旁边的下拉菜单指定度量单位；在英寸和厘米之间选择。 |
| [!UICONTROL Signature] | 定义投放确认。 选项：<br/><br/>**[!UICONTROL Not Required]**：未向您发送任何投放确认函。<br/><br/>**[!UICONTROL No Signature]**：已向您发送不带收件人签名的投放确认函。<br/><br/>**[!UICONTROL Signature Required]**：装运承运人获取收件人的签名并向您提供其打印副本。<br/><br/>**[!UICONTROL Adult Required]**：装运承运人获取成人收件人的签名并向您提供其打印副本。<br/><br/>**[!UICONTROL Direct (FedEx only)]**： FedEx从投放地址处的某人获取签名，如果没有人签名该包，则重新尝试投放。<br/><br/>**[!UICONTROL Indirect (FedEx only)]**： FedEx通过以下三种方式之一获得签名：<br/>(1)来自投放地址的人；<br/>(2)来自邻居、建筑经理或地址的其他人；或者<br/>(3)收件人可以留下已签名的FedEx门标记，授权在没有任何人出席的情况下释放包。 仅适用于住宅投放。 选项可能因不同的配送方式而略有不同。 有关最新信息，请参阅承运人的资源。 |
| [!UICONTROL Contents] | （仅适用于USPS装运）包装内容的描述。 选项： `Gift` / `Documents` / `Commercial Sample` / `Returned Goods` / `Merchandise` / `Other` |
| [!UICONTROL Explanation] | （仅限USPS装运）包内容的详细说明。 |

{style="table-layout:auto"}

[1]: https://www.fedex.com/en-us/api/get-support.html
[2]: https://www.ups.com/us/en/support/contact-us.page
[3]: https://www.dhl.com/us-en/home/our-divisions/ecommerce-solutions.html
[4]: https://www.usps.com/business/web-tools-apis/#ssc

<!-- Last updated from includes: 2025-11-26 10:55:00 -->

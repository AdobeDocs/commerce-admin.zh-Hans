---
title: ’[!UICONTROL Sales] &gt； [!UICONTROL Delivery Methods]’
description: 查看 [!UICONTROL Sales] &gt； [!UICONTROL Delivery Methods] 商务管理员页面。
exl-id: 159b76a8-3676-4692-9cd6-18947bda4666
feature: Configuration, Shipping/Delivery
source-git-commit: 1f84bf9ab20aeccacf56eab396b2778140964d17
workflow-type: tm+mt
source-wordcount: '3878'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Delivery Methods]

{{config}}

## [!UICONTROL Basic Delivery Methods]

### [!UICONTROL Flat Rate]

![统一费率](./assets/delivery-methods-flat-rate.png)<!-- zoom -->

<!-- [Flat Rate](https://docs.magento.com/user-guide/shipping/shipping-flat-rate.html) -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Enabled] | 网站 | 启用后，“统一速率”将作为选项显示在 _估计运费和税金_ 部分，以及 _配送_ 部分。 选项： `Yes` / `No` |
| [!UICONTROL Title] | 商店视图 | 结帐期间用于此配送方法的名称。 |
| [!UICONTROL Method Name] | 商店视图 | 描述用于生成装运估计的计算方法的名称。 方法名称显示在购物车中计算的预计费率旁边。 默认值为 `Fixed`. |
| [!UICONTROL Type] | 网站 | 描述用于确定统一费率的计算类型。 选项： <br/>**`None`**— 不使用计算。 将“统一费率”设置为零，这等同于免运费。<br/>**`Per Order`**  — 对整个订单收取单一统一费率。 <br/>**`Per Item`**— 对购物车中的每个项目收取单独的统一费率。 比率乘以购物车中的项目数，即使总数量包含不同项目的组合也是如此。 |
| [!UICONTROL Price] | 网站 | 您向客户收取的统一费率运费价格。 |
| [!UICONTROL Calculate Handling Fee] | 网站 | 确定如何计算手续费（如果包括）。 选项： `Fixed` / `Percent` |
| [!UICONTROL Handling Fee] | 网站 | 根据您选择用于计算金额的方法，输入手续费的收费金额。 例如，如果费用基于固定费用，则以小数形式输入金额，如4.90。但是，如果手续费基于订单的百分比，则按百分比输入金额。 例如，如果您对订单的6%计费，则输入值为 `.06`. |
| [!UICONTROL Displayed Error Message] | 商店视图 | 如果客户选择“统一费率”，但由于某种原因此方法不可用，则会显示消息。 |
| [!UICONTROL Ship to Applicable Countries] | 网站 | 标识提供统一费率配送的国家/地区。 选项： <br/>**`All Allowed Countries`**— 来自商店配置中指定的任何国家/地区的客户可以使用统一费率配送。<br/>**`Specific Countries`**  — 仅特定国家/地区的客户可以使用统一费率运输。 |
| [!UICONTROL Ship to Specific Countries] | 网站 | 标识客户可以使用统一费率配送的每个国家/地区。 |
| [!UICONTROL Show Method if Not Applicable] | 网站 | 如果统一费率不适用于购买，则确定在结帐期间是否显示为一个选项。 选项： `Yes` / `No` |
| [!UICONTROL Sort Order] | 网站 | 确定结帐期间与其他交货方法一起列出统一费率时显示的顺序的数字。 |

{：style=&quot;table-layout：auto&quot;}

### [!UICONTROL Free Shipping]

![免费送货](./assets/delivery-methods-free-shipping.png)<!-- zoom -->

<!-- [Free Shipping](https://docs.magento.com/user-guide/shipping/shipping-free.html) -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Enabled] | 网站 | 启用后，在结账过程中，免费送货将显示为送货分区中的一个选项。 选项： `Yes` / `No` |
| [!UICONTROL Title] | 商店视图 | 结帐期间用于此配送方法的名称。 |
| 方法名称 | 商店视图 | 描述用于生成装运估计的计算方法的名称。 方法名称显示在购物车中计算的预计费率旁边。 默认值为 `Free`. |
| 最小订单金额 | 网站 | 将免运费应用于订单所需的最低采购额。 |
| 含税目标金额 | 网站 | 确定最小订单金额计算中是否包含税。 选项： <br/>**是**  — 计算最小订单金额时包括税金（小计+税 — 折扣）。<br/>**否**  — 计算最小订单金额（小计 — 折扣）时不包括税。 |
| 显示的错误消息 | 商店视图 | 如果客户选择“免运费”，但由于某种原因无法使用此方法，则会显示一条消息。 |
| 发运至适用的国家/地区 | 网站 | 标识您提供免运费的国家/地区。 选项： <br/>**所有允许的国家/地区**  — 商店配置中指定的任何国家/地区的客户都可以使用免运费。 <br/>**特定国家/地区**  — 仅特定国家/地区的客户可使用免运费。 |
| 发运至特定国家/地区 | 网站 | 标识客户可在其中使用免运费的每个国家/地区。 |
| 显示方法（如果不适用） | 网站 | 如果免费送货方法不适用于购买，则确定在结账期间是否显示免费送货选项。 选项： `Yes` / `No` |
| [!UICONTROL Sort Order] | 网站 | 一个数字，用于确定在结帐期间与其他交付方法一起列出免费送货时显示的顺序。 |

{：style=&quot;table-layout：auto&quot;}

### [!UICONTROL Table Rates]

![表费率](./assets/delivery-methods-table-rates.png)<!-- zoom -->

<!-- [Table Rates](https://docs.magento.com/user-guide/shipping/shipping-table-rate.html) -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Enabled] | 网站 | 启用后，表费率在购物车的“估计运费和税”部分以及在结帐期间显示在“运费”部分中的一个选项。 选项： `Yes` / `No` |
| [!UICONTROL Title] | 商店视图 | 结帐期间用于此配送方法的名称。 |
| 方法名称 | 商店视图 | 描述用于生成装运估计的计算方法的名称。 方法名称显示在购物车中计算的预计费率旁边。 默认值为 `Table Rate`. |
| [!UICONTROL Condition] | 网站 | 确定计算所依据的条件。 上传的CSV文件的格式特定于每个条件。 选项： `Weight vs. Destination` / `Price vs. Destination` / `# of Items vs. Destination` |
| [!UICONTROL Include Virtual Products in Price Calculation] | 网站 | 确定表费率价格计算中是否包括不需要发运的虚拟产品。 |
| [!UICONTROL Calculate Handling Fee] | 网站 | 确定如何计算手续费（如果包括）。 选项： `Fixed` / `Percent` |
| [!UICONTROL Handling Fee] | 网站 | 添加到装运费用中用于支付装运费用的任何费用金额。 输入小数值。 例如，如果费用基于百分比，请输入0.06而不是6 %。 对于固定金额，输入 `6.00`. |
| [!UICONTROL Displayed Error Message] | 商店视图 | 如果客户选择“表费率”，但由于某种原因导致此方法不可用，则会显示消息。 |
| [!UICONTROL Ship to Applicable Countries] | 网站 | 标识您提供表费率配送的国家/地区。 选项： <br/>**`All Allowed Countries`**— 来自商店配置中指定的任何国家/地区的客户可以使用表费率配送。<br/>**`Specific Countries`**  — 仅来自特定国家/地区的客户可以使用表费率运输。 |
| [!UICONTROL Ship to Specific Countries] | 网站 | 标识客户可使用表费率配送的每个国家/地区。 |
| [!UICONTROL Show Method if Not Applicable] | 网站 | 确定签出期间“表费率”是否显示为选项（如果该方法不适用于购买）。 选项： `Yes` / `No` |
| [!UICONTROL Sort Order] | 网站 | 一个数字，可确定在结账期间与其他交付方法一起列出表格费率时显示的顺序。 |

{：style=&quot;table-layout：auto&quot;}

### [!UICONTROL In-Store Delivery]

![店内投放](./assets/delivery-methods-in-store-delivery.png)<!-- zoom -->

<!-- [In-Store Delivery](https://docs.magento.com/user-guide/shipping/shipping-in-store-delivery.html) -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Enabled] | 网站 | 启用后，店内交付可作为选项显示在 _估计运费和税金_ 部分，以及 _配送_ 部分。 选项： `Yes` / `No` |
| [!UICONTROL Method Name] | 商店视图 | 将店内取货功能标识为配送方法的名称。 此值显示为“Shipping checkout”（发运结帐）页面顶部的选项卡标签，以及同一页面底部的可用发运方法表中的标签。 默认值为 `In-store Delivery`. |
| [!UICONTROL Title] | 商店视图 | 结帐期间用于此配送方法的名称。 |
| [!UICONTROL Price] | 网站 | 您向客户收取店内取货的价格。 |
| [!UICONTROL Search Radius] | 网站 | 搜索取车位置时使用的半径（以公里为单位）。 |
| [!UICONTROL Displayed Error Message] | 商店视图 | 当客户选择店内提货时显示的消息，但交货方式不可用。 |

{：style=&quot;table-layout：auto&quot;}

## [!UICONTROL Carriers]

### [!UICONTROL UPS]

{{ups-api}}

{{beta2-updates}}

![UPS XML帐户设置](./assets/delivery-methods-ups1.png)<!-- zoom -->

<!-- [UPS XML Account Settings](https://docs.magento.com/user-guide/shipping/ups.html) -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Enabled for Checkout] | 网站 | 确定客户在结帐期间是否可以将UPS作为配送方式使用。 选项： `Yes` / `No` |
| [!UICONTROL Enabled for RMA] | 网站 | 确定UPS是否作为RMA的配送方式提供给客户。 选项： `Yes` / `No` |
| [!UICONTROL UPS Type] | 商店视图 | 指定用于连接到UPS运输系统的方法。 选项： <br/>**`United Parcel Service XML`**— （默认）您的存储将包含数据的XML文件作为请求发送给UPS。<br/>**`United Parcel Service`**  — 您的存储将键值对作为请求发送到UPS。 <br/><br/>**_注意：_**标准联合包裹服务类型计划在Commerce中被弃用。 对于新配置，您应该使用 [!UICONTROL United Parcel Service XML] 类型。 |
| _[!UICONTROL UPS Account Settings]_ |  |  |
| [!UICONTROL Live Account] | 商店视图 | 指定United Parcel Service帐户处于活动状态。 选项： `Yes` / `No` |
| [!UICONTROL Gateway URL] | 网站 | 连接到UPS系统以检索动态配送费率的URL。 UPS将停止支持HTTP。 默认值： `https://www.ups.com/using/services/rave/qcostcgi.cgi` |
| [!UICONTROL Title] | 商店视图 | 结帐期间用于此配送方法的名称。 |
| _[!UICONTROL UPS XML Account Settings]_ |  |  |
| [!UICONTROL Access License Number] | 网站 | 您的UPS托运人帐户访问许可证编号。 |
| [!UICONTROL Gateway XML URL] | 网站 | 对于UPS XML服务，显示传输XML数据所需的以下URL：网关XML URL、跟踪XML URL、发运确认XML URL、发运接受XML URL |
| [!UICONTROL Mode] | 网站 | 确定用于发送到UPS系统的数据的传输模式。 选项： <br/>**`Development`**- UPS不会验证从Commerce服务器接收的数据是否通过SSL发送。<br/>**`Live`** - UPS验证从Commerce服务器接收的数据是否通过安全套接字层(SSL)发送。 |
| 用户标识 | 网站 | 您的UPS托运人帐户用户ID。 |
| [!UICONTROL Origin of the Shipment] | 网站 | （仅限UPS XML）产品发运来源的国家/地区。 |
| [!UICONTROL Password] | 商店视图 | 您的UPS发货人帐户密码。 |

{：style=&quot;table-layout：auto&quot;}

![UPS包信息](./assets/delivery-methods-ups-packaging-settings.png)<!-- zoom -->

<!-- [UPS Package Information](https://docs.magento.com/user-guide/shipping/ups.html) -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| _[!UICONTROL UPS Negotiated Rate Settings]_ |  |  |
| [!UICONTROL Enable Negotiated Rates] | 网站 | （仅限UPS XML ）根据您与UPS的协议启用/禁用特殊费率。 选项： `Yes` / `No` |
| [!UICONTROL Packages Request Type] | 网站 | 确定如何计算具有多个包装的发运的重量。 选项： `Divide to equal weight (one request)` / `Use origin weight (multiple requests)` |
| [!UICONTROL Shipper Number] | 网站 | （仅限UPS XML）要参考使用议定费率，需要六个字符的UPS发货人编号。 |
| [!UICONTROL Container] | 网站 | 设置用于包装订单发运的集装箱类型。 选项： `Customer Packaging` / `UPS Letter Envelope` / `Customer Packaging` / `UPS Letter Envelope` / `UPS Tube` / `UPS Express Box` / `UPS Worldwide 25 kilo` / `UPS Worldwide 10 kilo` |
| [!UICONTROL Weight Unit] | 网站 | 设置商店中产品重量的默认度量单位。 请参阅 [维度权重](../../stores-purchase/carriers.md#dimensional-weight) 以了解其他信息。 |
| [!UICONTROL Tracking XML URL] | 网站 | （仅限UPS XML）用于跟踪包的UPS URL。 |
| [!UICONTROL Destination Type] | 网站 | 设置默认发运目的地类型。 选项： `Business` / `Residential` |
| [!UICONTROL Maximum Package Weight] | 网站 | 设置包可以由UPS指定的最大重量。 如果订购的产品超出最大包装重量，则此选项不可用。 根据 [UPS.com](https://www.ups.com/us/en/global.page)，包装不得超过150磅（70千克）请与您的承运商核实，以确认最大重量。 |
| [!UICONTROL Pickup Method] | 网站 | 设置UPS拾取方法。 选项： `Regular Daily Pickup` / `On Call Air` / `One Time Pickup` / `Letter Center` / `Customer Counter` |
| [!UICONTROL Minimum Package Weight] | 网站 | 设置包可以由UPS指定的最小重量。 如果订购的产品重量小于最小包装重量，则此发运选项不可用。 要验证最小重量，请与您的运输公司核实。 |
| [!UICONTROL Calculate Handling Fee] | 网站 | 设置表费率发运的处理费计算方法。 选项： <br>**`Fixed`**— 手续费为固定费率。<br>**`Percent`**  — 手续费按订单金额的百分比收取。 |
| [!UICONTROL Handling Applied] | 网站 | 指定处理费是应用于每个订单还是应用于订单中的每个包。 |
| [!UICONTROL Handling Fee] | 网站 | 设置包含在运费价格中的处理。 处理费可以设置为固定金额或百分比。 <br/><br/>**_注意：_**如果键入百分比金额，请使用小数格式 `0.25` 25%。 |

{：style=&quot;table-layout：auto&quot;}

![UPS允许的方法](./assets/delivery-methods-ups-allowed-methods.png)<!-- zoom -->

<!-- [UPS Allowed Methods](https://docs.magento.com/user-guide/shipping/ups.html) -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| _[!UICONTROL UPS allowed methods]_ |  |  |
| [!UICONTROL Allowed Methods] | 网站 | 指定提供给客户的UPS配送允许的方法。 根据所选配送方式计算配送费率。 |
| [!UICONTROL Free Method] | 网站 | 标识用于通过UPS免费配送的方法。 要禁用免费送货，请选择“无”。 <br/><br/>**_注意：_**此方法与基本方法类似 [免费送货](../../stores-purchase/shipping-free.md)，但在结帐期间会显示为UPS送货选项。 |
| [!UICONTROL Free Shipping Amount Threshold] | 网站 | 确定当订单金额满足免运费阈值时是否应用免运费。 选项： `Enable` / `Disable` |
| [!UICONTROL Free Shipping Amount Threshold] | 网站 | 设置订单达到免费配送资格所需达到的最低总金额。 |
| [!UICONTROL Displayed Error Message] | 商店视图 | 由于任何原因无法使用此配送方式时显示的错误消息。 |

{：style=&quot;table-layout：auto&quot;}

![UPS适用的国家/地区和其他设置](./assets/delivery-methods-ups-ship-to.png)<!-- zoom -->

<!-- [UPS Applicable Countries and Other Settings](https://docs.magento.com/user-guide/shipping/ups.html) -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| _[!UICONTROL UPS Applicable countries and other Settings]_ |  |  |
| [!UICONTROL Ship to Applicable Countries] | 网站 | 指定允许哪些国家/地区客户使用此配送方式。 选项： <br/>**`All Allowed Countries`**— 来自所有客户的客户 [国家/地区](../../getting-started/store-details.md#country-options) 在商店配置中指定的可使用此配送方式。<br/>**`Specific Countries`**  — 选择此选项后， [!UICONTROL Ship to Specific Countries] 列表出现。 选择列表中可使用此配送方法的每个国家/地区。 |
| [!UICONTROL Show Method if Not Applicable] | 网站 | 确定UPS在签出期间是否始终显示为送货选项。 选项： <br/>**`Yes`**— 在结账过程中，UPS始终显示为送货选项，即使不适用于该订单。<br/>**`No`**  — 只有在订单适用时，UPS才会在结帐期间显示为送货选项。 （例如，如果订单重量超过最大重量。） |
| [!UICONTROL Debug] | 网站 | 指定系统是否记录存储和UPS之间的数据传输以进行调试。 除非存在必须跟踪和记录的问题，否则此选项应设置为 `No`. |
| [!UICONTROL Sort Order] | 网站 | 一个数字，用于在结账期间与其他交付方法一起列出UPS时确定其显示顺序。 输入 `0` ，在列表顶部。 |

{：style=&quot;table-layout：auto&quot;}

### [!UICONTROL USPS]

{{beta2-updates}}

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| 已启用签出 | 网站 | 确定客户在结帐期间是否可以将USPS作为配送方式使用。 选项： `Yes` / `No` |
| _[!UICONTROL USPS Account Settings]_ |  |  |
| [!UICONTROL Gateway URL] | 网站 | 用于连接到USPS系统以动态检索运费的URL。 |
| [!UICONTROL Secure Gateway URL] | 网站 | 用于通过安全套接字层(SSL)连接到USPS系统的安全URL，以动态检索运费。 |
| [!UICONTROL Title] | 商店视图 | 此配送选项的标题，显示在购物车结帐中。 |
| [!UICONTROL User ID] | 网站 | 您的USPS托运人帐户用户ID。 |
| [!UICONTROL Password] | 网站 | 您的USPS发货人帐户密码。 |
| [!UICONTROL Mode] | 网站 | 确定用于发送到USPS系统的数据的传输模式。 选项包括： <br/>**`Development`**- USPS不会验证从Commerce服务器接收的数据是否通过SSL发送。<br/>**`Live`** - USPS验证从Commerce服务器接收的数据是否通过安全套接字层(SSL)发送。 |

{：style=&quot;table-layout：auto&quot;}

![USPS打包设置](./assets/delivery-methods-usps-packaging.png)<!-- zoom -->

<!-- [USPS Packaging Settings](https://docs.magento.com/user-guide/shipping/usps.html) -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| _[!UICONTROL USPS packaging Settings]_ |  |  |
| [!UICONTROL Packages Request Type] | 网站 | 确定如何计算具有多个包装的发运的重量。 选项： `Divide to equal weight (one request)` / `Use origin weight (multiple requests)` |
| [!UICONTROL Container] | 网站 | 设置用于包装订单发运的集装箱类型。 选项： `Variable` / `Flat Rate Box` / `Flat Rate Envelope` / `Rectangular` /非矩形 |
| [!UICONTROL Size] | 网站 | 将Size选项设置为典型装运包大小。 此选项会影响装运率的计算。 选项： `Regular` / `Large` / `Oversize` |
| [!UICONTROL Machinable] | 网站 | 指定计算机是否可以处理包。 此选项会影响装运率的计算。 |
| [!UICONTROL Maximum Package Weight] | 网站 | 设置包可以由USPS指定的最大重量。 如果订购的产品超出最大包装重量，则此选项不可用。 |

{：style=&quot;table-layout：auto&quot;}

![USPS处理费设置](./assets/delivery-methods-usps-handling-fee.png)<!-- zoom -->

<!-- [USPS Handling Fee Settings](https://docs.magento.com/user-guide/shipping/usps.html) -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| _[!UICONTROL USPS Handling Fee settings]_ |  |  |
| [!UICONTROL Calculate Handling Fee] | 网站 | 设置表费率发运的处理费计算方法。 选项： <br/>**`Fixed`**— 手续费为固定费率。<br/>**`Percent`**  — 手续费按订单金额的百分比收取。 |
| [!UICONTROL Handling Applied] | 网站 | 指定处理费是应用于每个订单还是应用于订单中的每个包。 |
| [!UICONTROL Handling Fee] | 网站 | 设置包含在运费价格中的处理。 处理费可以设置为固定金额或百分比。 <br/><br/>**_注意：_**输入百分比金额时，请使用小数格式 `0.25` 25%。 |

{：style=&quot;table-layout：auto&quot;}

![USPS允许的方法](./assets/delivery-methods-usps-allowed-methods.png)<!-- zoom -->

<!-- [USPS Allowed Methods](https://docs.magento.com/user-guide/shipping/usps.html) -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| _[!UICONTROL USPS Allowed Methods]_ |  |  |
| [!UICONTROL Allowed Methods] | 网站 | 指定提供给客户的USPS装运的允许方法。 根据所选配送方式计算配送费率。 |
| [!UICONTROL Free Method] | 网站 | 通过USPS设置免费配送方式，也可以通过选择禁用 `None`. <br/><br/>**_注意：_**此配送方式与商店的免运费方法类似，但它列为USPS配送选项，并标识为USPS配送。 |
| [!UICONTROL Minimum Order Amount for Free Shipping] | 网站 | 设置符合免费配送资格所需的最低订单金额。 |
| [!UICONTROL Displayed Error Message] | 商店视图 | USPS由于任何原因不可用时显示的错误消息。 |

{：style=&quot;table-layout：auto&quot;}

![USPS适用的国家/地区](./assets/delivery-methods-usps-countries.png)<!-- zoom -->

<!-- [USPS Applicable Countries](https://docs.magento.com/user-guide/shipping/usps.html) -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| _[!UICONTROL USPS Applicable Countries]_ |  |  |
| [!UICONTROL Ship to Applicable Countries] | 网站 | 指定可以发运订单的国家/地区。 选项： <br/>**`All Allowed Countries`**— 来自所有客户的客户 [国家/地区](../../getting-started/store-details.md#country-options) 在商店配置中指定的可使用此配送方式。<br/>**`Specific Countries`**  — 选择此选项后， [!UICONTROL Ship to Specific Countries] 列表出现。 选择列表中可使用此配送方法的每个国家/地区。 |
| [!UICONTROL Show Method if Not Applicable] | 网站 | 控制结账过程中USPS送货的显示。 选项： <br/>**`Yes`**- USPS在结账期间始终显示为送货选项，即使不适用于该订单。<br/>**`No`**  — 只有在订单适用（即订单重量超过最大重量）时，USPS才会在结帐期间显示为发运选项。 |
| [!UICONTROL Debug] | 网站 | 确定系统是否维护您的商店和USPS之间的数据传输日志以进行调试。 除非存在必须跟踪和记录的问题，否则此选项应设置为 `No`. |
| [!UICONTROL Sort Order] | 网站 | 确定在结账期间与其他交付方法一起列出USPS时显示的顺序的数字。 输入 `0` ，在列表顶部。 |

{：style=&quot;table-layout：auto&quot;}

### [!UICONTROL FedEx]

{{beta2-updates}}

![联邦快递帐户设置](./assets/delivery-methods-fedex-account-settings.png)<!-- zoom -->

<!-- [FedEx Account Settings](https://docs.magento.com/user-guide/shipping/fedex.html) -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| _[!UICONTROL FedEx Account Settings]_ |  |  |
| [!UICONTROL Enabled for Checkout] | 网站 | 确定客户在结账期间是否可以将FedEx作为配送方式使用。 选项： `Yes` / `No` |
| [!UICONTROL Title] | 商店视图 | 此配送选项的标题，显示在购物车结帐中。 |
| [!UICONTROL Account ID] | 网站 | 您的联邦快递帐户ID。 |
| [!UICONTROL Meter Number] | 网站 | 你的FedEx表号。 |
| [!UICONTROL Key] | 网站 | 您的联邦快递帐户密钥。 |
| [!UICONTROL Password] | 网站 | 您的FedEx帐户密码。 |
| [!UICONTROL Sandbox Mode] | 网站 | 要在测试环境中运行FedEx事务，请将沙盒模式设置为 `Yes`. 选项： `Yes` / `No`. |
| [!UICONTROL Web-Services URL] | 网站 | 所需的URL取决于沙盒模式设置。 选项： <br/>**`Production`**— 存储上线时用于访问FedEx Web服务的URL。<br/>**`Sandbox`**  — 用于访问FedEx Web服务的测试环境的URL。 |

{：style=&quot;table-layout：auto&quot;}

![FedEx封装](./assets/delivery-methods-fedex-packaging.png)<!-- zoom -->

<!-- [FedEx Packaging](https://docs.magento.com/user-guide/shipping/fedex.html) -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| _[!UICONTROL FedEx Packaging Settings]_ |  |  |
| [!UICONTROL Packages Request Type] | 网站 | 确定如何计算具有多个包装的发运的重量。 选项： `Divide to equal weight (one request)` / `Use origin weight (multiple requests)` |
| [!UICONTROL Packaging] | 网站 | 从列表中选择通常用于包装从商店中订购的产品的容器类型。 |
| [!UICONTROL Dropoff] | 网站 | 从列表中选择选取方法： <br/>**`Regular Pickup`**— （默认）如果发运量很大，则安排定期提货可能具有成本效益。<br/>**`Request Courier`**  — 您必须致电并请求联邦快递快递取货。 <br/>**`Drop Box`**— 您必须在当地联邦快递托运箱中卸货。<br/>**`Business Service Center`**  — 您必须在当地联邦快递商务服务中心卸货。 <br/>**`Station`**— 您必须在当地联邦快递站卸货。 |
| [!UICONTROL Maximum Package Weight] | 网站 | 联邦快递的默认价格为150磅。 有关支持的最大重量，请咨询您的承运商。 除非您与FedEx有特殊安排，否则建议使用默认值。 |

{：style=&quot;table-layout：auto&quot;}

![联邦快递手续费](./assets/delivery-methods-fedex-handling-fee.png)<!-- zoom -->

<!-- [FedEx Handling Fee](https://docs.magento.com/user-guide/shipping/fedex.html) -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| _[!UICONTROL FedEx Handling Fee Settings]_ |  |  |
| [!UICONTROL Calculate Handling Fee] | 网站 | 确定用于计算手续费的方法。 选项： `Fixed Fee` / `Percentage` <br/><br/>**_注意：_**手续费是可选的，显示为联邦快递运费中增加的额外费用。 |
| [!UICONTROL Handling Applied] | 网站 | 确定如何处理手续费。 选项： `Per Order` / `Per Package` |
| [!UICONTROL Handling Fee] | 网站 | 根据用于计算金额的方法，指定作为手续费收取的金额。 如果费用基于固定费用，请以小数形式输入金额，例如 `4.90`. 如果手续费基于订单的百分比，则按百分比输入金额。 例如，要收取订单的6%的费用，请输入以下值 `.06`. |

{：style=&quot;table-layout：auto&quot;}

![FedEx投放方法](./assets/delivery-methods-fedex-delivery-methods.png)<!-- zoom -->

<!-- [FedEx Delivery Methods](https://docs.magento.com/user-guide/shipping/fedex.html) -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| _[!UICONTROL FedEx delivery methods]_ |  |  |
| [!UICONTROL Residential Delivery] | 网站 | 根据您销售的是企业对消费者(B2C)还是企业对企业(B2B)，设置为以下选项之一： <br/>**`Yes`**— 对于B2C投放<br/>**`No`**  — 对于B2B投放 |
| [!UICONTROL Allowed Methods] | 网站 | 从列表中，选择您支持的装运方法。 具体方法取决于您的联邦快递账户、发货频率和规模，以及您是否允许国际发货。 作为商人，您可能决定只提供陆运。 |
| [!UICONTROL Hub ID] | 网站 | 由FedEx提供的ID，用于 [!DNL Smart Post] 方法。 |
| [!UICONTROL Free Method] | 网站 | 从列表中，选择您喜欢用于免费送货的送货方式。 <br/><br/>**_注意：_**此配送方式类似于常规免运费方式，但它列在FedEx配送选项中，并被标识为FedEx配送。 |
| [!UICONTROL Free Shipping Amount Threshold] | 网站 | 确定免运费是否需要最小订单金额。 选项： <br/>**`Enable`**— 为达到最小数量的订单启用免费FedEx装运。<br/>**`Disable`**  — 禁用带有最低订单的免费FedEx运输。 |
| [!UICONTROL Free Shipping Amount Threshold] | 网站 | 指定免费送货所需的最小订单金额。 |
| [!UICONTROL Displayed Error Message] | 商店视图 | FedEx由于任何原因不可用时显示的消息。 您可以使用默认消息或输入其他消息。 |

{：style=&quot;table-layout：auto&quot;}

![FedEx适用国家/地区](./assets/delivery-methods-fedex-applicable-countries.png)<!-- zoom -->

<!-- [FedEx Applicable Countries](https://docs.magento.com/user-guide/shipping/fedex.html) -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| _[!UICONTROL FedEx Applicable Countries]_ |  |  |
| [!UICONTROL Ship to Applicable Countries] | 网站 | 指示客户可通过FedEx发货的国家/地区。 选项： <br/>**`All Allowed Countries`**— 来自所有客户的客户 [国家/地区](../../getting-started/store-details.md#country-options) 在商店配置中指定的可使用此配送方式。<br/>**`Specific Countries`**  — 选择此选项后， [!UICONTROL Ship to Specific Countries] 列表出现。 选择列表中可使用此配送方法的每个国家/地区。 |
| [!UICONTROL Ship to Specific Countries] | 网站 | 指示客户可通过FedEx发货的特定国家/地区。 |
| [!UICONTROL Debug] | 网站 | 确定系统是否维护您的商店和FedEx之间的数据传输日志以进行调试。 除非存在必须跟踪和记录的问题，否则此选项应设置为 `No`. |
| [!UICONTROL Show Method if Not Applicable] | 网站 | 确定在结账期间何时将FedEx显示为配送方式。 选项： <br/>**`Yes`**— 无论订单是否符合使用条件，FedEx发运选项都会显示在交货方式列表中。<br/>**`No`**  — 如果交货方法列表不适用于FedEx发运选项（例如，如果订单重量超过最大重量金额），则不会在该订单中显示该选项。 |
| [!UICONTROL Sort Order] | 网站 | 确定在结账期间与其他投放方法一起列出时FedEx显示的顺序的数字。 输入 `0` ，在列表顶部。 |

{：style=&quot;table-layout：auto&quot;}

### [!UICONTROL DHL]

![DHL帐户设置](./assets/delivery-methods-dhl-account-settings.png)<!-- zoom -->

<!-- [DHL Account Settings](https://docs.magento.com/user-guide/shipping/dhl.html) -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| _[!UICONTROL DHL Account Settings]_ |  |  |
| [!UICONTROL Enabled for Checkout] | 网站 | 确定客户在结帐期间是否可以将DHL作为送货方法使用。 选项： `Yes` / `No` |
| [!UICONTROL Title] | 商店视图 | 此配送方式在结账时显示的标题。 |
| [!UICONTROL Gateway URL] | 网站 | 通常，您可以接受默认网关URL。 但是，如果DHL为您提供了替代URL，请在此字段中输入值。 |
| [!UICONTROL Access ID] | 网站 | 您的DHL托运人帐户访问ID。 |
| [!UICONTROL Password] | 网站 | 您的DHL托运人帐户密码。 |
| [!UICONTROL Account Number] | 网站 | 您的DHL托运人帐号。 |

{：style=&quot;table-layout：auto&quot;}

![DHL包设置](./assets/delivery-methods-dhl-package-settings.png)<!-- zoom -->

<!-- [DHL Package Settings](https://docs.magento.com/user-guide/shipping/dhl.html) -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| _[!UICONTROL DHL Package Settings]_ |  |  |
| [!UICONTROL Calculate Handling Fee] | 网站 | 处理费是可选的，显示为在DHL运输成本中增加的额外费用。 从列表中选择要用于计算手续费的方法。 选项：固定费用/百分比。 |
| [!UICONTROL Handling Applied] | 网站 | 从列表中，选择要如何应用手续费。 选项： `Per Order` / `Per Package` |
| 手续费 | 网站 | 根据您选择用于计算金额的方法，输入手续费的收费金额。 例如，如果费用基于固定费用，则以小数形式输入金额，如 `4.90`. 但是，如果手续费基于订单的百分比，则按百分比输入金额。 例如，如果您对订单的6%计费，则输入值为 `.06`. |
| [!UICONTROL Divide Order Weight] | 商店视图 | 确定超过70千克的订单是否可分解为较小的单位，以确保装运费用的准确性。 选项： `Yes` / `No` |
| [!UICONTROL Weight Unit] | 商店视图 | 确定在装运计算中使用的重量的度量单位。 选项： `Pounds` / `Kilograms` |
| [!UICONTROL Size] | 商店视图 | 确定包的大小。 选项： <br/>**`Regular`**— 发运的软件包符合DHL标准包装方法。 在 [!UICONTROL Allowed Methods] 列表，选择用于从商店发运产品的每种包装方法。<br/>**`Specific`**  — 如果发运的软件包具有自定义维度，请完成以下操作： [!UICONTROL Height (cm)] / [!UICONTROL Depth (cm)] / [!UICONTROL Width (cm)] |

{：style=&quot;table-layout：auto&quot;}

![DHL允许的方法](./assets/delivery-methods-dhl-allowed-methods.png)<!-- zoom -->

<!-- DHL Allowed Methods](https://docs.magento.com/user-guide/shipping/dhl.html) -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| _[!UICONTROL DHL allowed methods]_ |  |  |
| [!UICONTROL Allowed Methods] | 网站 | 在列表中，选择您支持的每种发运方法。 |
| [!UICONTROL Ready Time] | 网站 | 指定在提交订单后，程序包何时准备好取货（以小时为单位）。 |
| [!UICONTROL Displayed Error Message] | 商店视图 | 当DHL由于任何原因变得不可用时，将出现此消息。 您可以使用默认消息或输入自己的消息。 |
| [!UICONTROL Free Method] |  | 此配送方式与常规免运费配送方式类似，但它列在DHL配送选项中，并被标识为DHL配送。 在列表中，选择您喜欢用于免费送货的送货方式。 |
| [!UICONTROL Free Shipping with Minimum Order Amount] | 网站 | 设置为以下任一项： <br/>**`Enable`**— 允许对达到最小数量的订单免费DHL装运。<br/>**`Disable`**  — 不提供最低订货量的免费DHL运输。 |
| [!UICONTROL Minimum Order Amount for Free Shipping] | 网站 | 如果您启用 [!UICONTROL Free Shipping with Minimum Order]，在字段中输入最小订单金额值。 |

{：style=&quot;table-layout：auto&quot;}

![DHL适用的国家/地区](./assets/delivery-methods-dhl-applicable-countries.png)<!-- zoom -->

<!-- [DHL Applicable Countries](https://docs.magento.com/user-guide/shipping/dhl.html) -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| _[!UICONTROL DHL applicable countries]_ |  |  |
| [!UICONTROL Ship to Applicable Countries] | 网站 | 指定允许哪些国家/地区客户使用此配送方式。 选项： <br/>**所有允许的国家/地区**  — 所有允许的国家/地区均适用免运费方法。 允许的国家/地区在 [!UICONTROL General] 配置页面。 <br/>**特定国家/地区**  — 将此送货选项限制为“送货至特定国家/地区”列表中指定的国家/地区。 |
| [!UICONTROL Ship to Specific Countries] | 网站 | 指定可以发送DHL装运的国家/地区。 此选定国家/地区列表用于 `Specific Countries` 在 [!UICONTROL Ship to Applicable Countries] 选项。 |
| [!UICONTROL Show Method if Not Applicable] | 网站 | 确定在结帐期间DHL何时显示为送货方法。 选项： <br/>**`Yes`**- DHL在结帐期间始终显示为送货选项，即使不适用于该订单。<br/>**`No`** - DHL仅在适用于订单（即订单重量超过最大重量）时，在结帐期间显示为发运选项。 |
| [!UICONTROL Debug] | 网站 | 创建包含错误信息的日志文件。 |
| [!UICONTROL Sort Order] | 网站 | 一个数字，它确定在结账期间与其他交付方法一起列出DHL时的显示顺序。 要将其放在列表顶部，请输入 `0`. |

{：style=&quot;table-layout：auto&quot;}

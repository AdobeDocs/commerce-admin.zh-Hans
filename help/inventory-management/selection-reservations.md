---
title: Source算法和预留
description: 了解后台运行的Source选择算法和预留系统，以保持可销售数量的更新。
exl-id: dcd63322-fb4c-4448-b6e7-0c54350905d7
feature: Inventory, Shipping/Delivery
source-git-commit: fdc14758788fa5cd0391371ebfafb478dadec8a4
workflow-type: tm+mt
source-wordcount: '2196'
ht-degree: 0%

---

# Source算法和预留

[!DNL Inventory Management]的核心跟踪您的仓库和商店中虚拟和现有的所有可用产品。 Source选择算法和预留系统在后台运行，可销售量会随时更新，结帐时不会出现冲突，并且会推荐发运选项。

>[!NOTE]
>
>有关以编程方式使用[!DNL Inventory Management]系统的信息，请参阅[开发人员文档](https://developer.adobe.com/commerce/php/development/framework/inventory-management/)。

## Source选择算法

Source选择算法(SSA)使用库存中配置的源的优先级顺序来分析和确定源和运输的最佳匹配。 在订单发运期间，算法会提供建议的来源列表、可用数量以及根据所选算法扣除的金额。 [!DNL Inventory Management]提供优先级算法，并支持新选项的扩展。

由于拥有多个来源地点、全球客户以及拥有各种运送选项和费用的承运商，了解您的实际可用库存并找到最佳运送选项会很困难。 SSA为您完成从跟踪所有来源的库存可销售数量到计算发运并提出建议的工作。

**跟踪库存** — 使用库存和来源，SSA检查传入产品请求的销售渠道并确定可用库存：

- 计算每个库存中所有已分配来源的总虚拟可销售数量：汇总数量 — 每个来源的缺货阈值
- 从可销售量中减去缺货阈值金额以防止过度销售
- 在提交订单时预留库存数量，在订单处理和发运时从库存库存中扣除
- 通过负阈值的增强选项支持延期交货

**管理发运** — 当您处理和发运订单时，算法会有所帮助。 您可以运行算法以获取有关运送产品的最佳来源的建议，也可以将所做的选择覆盖到：

- 发运部分装运，仅从特定地点发送少量产品，稍后完成全部订单
- 从一个来源发运整个订单
- 按不同金额分解多个来源中的发运，并在所有仓库和商店中保持库存平衡

SSA可扩展，用于推荐经济高效的发货的第三方支持和自定义算法。

>[!NOTE]
>
>SSA对虚拟产品和可下载产品的功能有所不同，这可能不会产生运输成本。 在这些情况下，系统在创建发票时隐式运行算法，并始终使用建议的结果。 您无法调整虚拟和可下载产品的这些结果。

### Source优先级算法

自定义库存包括指定的来源列表，这些来源通过您的店面销售和发运可用的产品库存。 在开票和发运订单时，Source优先级算法使用库存中分配的来源顺序来建议每个来源的产品扣除额。

运行时，算法将：

- 从顶部开始按照库存级别的已配置来源顺序工作
- 根据列表中的订单、可用数量和订购数量，建议每个产品的发运数量和来源
- 在订单装运完成之前继续沿列表向下移动
- 如果在列表中找到已禁用的源，则跳过该源

要配置、分配和订购自定义库存的来源，请执行以下操作： 请参阅[优先处理股票的来源](stocks-prioritize-sources.md)。

以下实例详细说明了按订单映射的来源、可用数量以及要扣除和发运的建议来源和金额。 最大来源是英国的卸货托运人，可用数量为240。

![山地自行车的示例SSA推荐](assets/ssa-sources-example.png){width="600" zoomable="yes"}

### 距离优先级算法

距离优先级算法将发运目标地址的位置与来源位置进行比较，以确定完成发运的最近来源。 该距离可以通过物理距离或使用导入的数据库位置或Google方向（驾驶、步行或骑自行车）从一个位置到另一个位置所花费的时间来确定。

您可以使用两个选项来计算距离和时间，以查找发运履行的最近来源：

- **Google MAP** — 使用[Google Map Platform][1]服务计算送货目标地址与源位置（地址和GPS坐标）之间的距离和时间。 此选项使用源的纬度和经度。 已启用[地理编码API][2]和[距离矩阵API][3]的Google API密钥是必需的。 此选项需要Google计费计划，并且可能会通过Google产生费用。

- **离线计算** — 使用下载和导入的地理代码数据计算距离，以确定距离送货目标地址最近的源。 此选项使用装运地址和来源的国家/地区代码。 要配置此选项，您可能需要开发人员帮助才能使用命令行最初下载和导入地理代码。

要配置，请选择配置并完成其他步骤，例如Google API密钥或下载配送数据。 请参阅[配置距离优先级算法](distance-priority-algorithm.md)。

### 自定义算法

[!DNL Commerce]支持自定义开发和扩展，以添加替代算法来优先处理源。 例如，您可以有一个基于地理位置的优先级算法，另一个基于库存或客户属性的优先级算法。 当库存成本发生变化时，您的实施可以轻松更改算法以确保最低成本。

## 预订

预留不会立即扣减或添加产品库存数量，而是保留库存量，直到订单发运或取消为止。 预留完全在后端工作，以便在库存层自动更新可销售数量。

>[!NOTE]
>
>[!BADGE 仅限PaaS]{type=Informative url="https://experienceleague.adobe.com/zh-hans/docs/commerce/user-guides/product-solutions" tooltip="仅适用于云项目(Adobe管理的PaaS基础架构)和内部部署项目上的Adobe Commerce 。"}保留功能要求`inventory.reservations.updateSalabilityStatus`消息队列使用者连续运行。 要检查它是否正在运行，请使用`bin/magento queue:consumers:list`命令。 如果未列出消息队列使用者，请启动该使用者： `bin/magento queue:consumers:start inventory.reservations.updateSalabilityStatus`。

### 订单预订

在提交订单时，保留会保留从可销售数量中扣除的库存数量。 保留在库存层，在开票、发运、取消订单等之前根据数量进行计数。 在发运订单时，您可以使用SSA建议或人工输入每个来源的数量扣减额。 发运时，系统会自动清除保留并扣除数量。 系统会重新计算具有更新数量的库存以及系统中剩余的任何保留金额的可销售数量。

下图有助于定义订单期间和直至发运的保留流程。

![从订单到交货的预订](assets/diagram-quantity.png){width="600" zoomable="yes"}

客户提交订单。 [!DNL Commerce]检查当前库存的可销售数量。 如果库存级别有足够的库存，则保留将临时暂挂产品SKU（对于该库存），并重新计算可销售数量。

对订单开票后，您可以确定要从来源扣除和发运的产品金额。 系统会处理装运，并将货物从一个或多个选定来源发送至客户。 数量会自动从来源库存数量中扣除，并且保留清除。 有关完整的详细信息和示例，请参阅[关于订单状态和预留](order-status.md)。

## 预订计算

发生以下事件时，系统会为每个产品创建预订：

- 客户或商家下订单。
- 客户或商家完全或部分取消订单。
- 商家为实物产品创建装运。
- 商家为虚拟或可下载的产品创建发票。
- 商家签发贷项通知单。

保留是仅附加的操作，类似于事件日志。 初始预留分配了负数量值。 处理订单时创建的所有后续保留均为正值。 订单完成时，产品的所有保留的总和为0。

在系统可以发布预订来响应新订单之前，系统会确定是否有足够的可销售商品来履行订单。 计算时考虑以下数量因素：

- **库存项目数量**。 StockItem数量是当前销售渠道的所有实际来源库存的合计金额。 举个例子，巴尔的摩的来源有20件产品，奥斯汀的来源有25件相同产品，雷诺的来源有10件。 当所有这些来源都链接到库存A时，此产品的StockItem计数为55 (20 + 25 + 10)。 （在发运项目时，库存索引器会更新每个来源的可用数量。）

- **未完成的预留**。 系统将计算所有未补偿的初始预留的总和。 此数字始终为负。 如果客户A预订了10个项目，而客户B预订了5个项目，则未完成的产品预订总数为–15。

因此，只要客户订购少于40(55+-15)个单元，商家就可以完成传入的订单。

当您完成处理订单（完成、已取消、已关闭）时，该订单范围内的所有保留应解析为`0`。 这将清除所有可销售数量暂挂。

>[!NOTE]
>
>延交订单（“缺货阈值”）和“通知低于阈值的数量”设置也会影响可销售数量的计算，但它们超出了本主题的范围。 有关这些设置的详细信息，请参阅[配置 [!DNL Inventory Management]](./configuration.md)。

## 预订对象

预订包含以下信息：

| 参数 | 数据类型 | 描述 |
| --- | --- | --- |
| `reservation_id` | 整数 | 系统生成的ID |
| `stock_id` | 整数 | 产品分配到的库存的ID |
| `sku` | 字符串 | 产品的SKU |
| `quantity` | 浮动 | 此预订中的项目数 |
| `metadata` | 字符串 | 此预订的事件类型、对象类型和对象ID。 例如，`{"event_type":"order_placed","object_type":"order",| "object_id":"8"}` |

{style="table-layout:auto"}

元数据`event_type`可以具有以下值：

- `order_placed`
- `order_canceled`
- `shipment_created`
- `creditmemo_created`
- `invoice_created`

当前，元数据对象类型必须是`order`，而对象ID是订单ID。

在将来的版本中，当客户将商品添加到购物车时，可能会创建预订。 每个项目可以预留固定时间（如15分钟），以便客户在继续购物时预留项目。 启用此类型的预订后，元数据可能包含其他类型的信息。

## 预订生命周期

以下示例显示了为简单订单生成的保留序列。

1. 客户针对25件产品`SKU-1`发出采购订单。 预订包含以下信息：

   ```text
   reservation_id = 1
   stock_id = 1
   sku = SKU-1
   quantity = -25
   event_type = order_placed
   ```

1. 客户发送了20个项目的发票，基本上取消了5个订购单位。

   ```text
   reservation_id = 2
   stock_id = 1
   sku = SKU-1
   quantity = 5
   event_type = order_canceled
   ```

1. 商户出货购买了20件。

   ```text
   reservation_id = 3
   stock_id = 1
   sku = `SKU-1`
   quantity = 20
   event_type = shipment_created
   ```

三个`quantity`值的总和为0 (-25 + 5 + 20)。 系统不会修改任何现有的预留。

## 正在删除已处理的预留

`inventory_cleanup_reservations` cron作业执行SQL查询以清除保留数据库表。 默认情况下，它每天在午夜运行，但您可以配置时间和频率。 cron作业运行一个脚本，该脚本查询数据库以查找数量值总和为0的完整保留序列。 当对同一天（或其他配置时间）发生的给定产品的所有预订进行补偿时，cron作业会一次删除所有预订。

`inventory_reservations_cleanup` cron作业与`inventory.reservations.cleanup`消息队列使用者不同。 在删除产品后，消费者按产品SKU异步删除预订，而cron作业将清除整个预订表。 在商店配置中启用&#x200B;[**与目录**](../configuration-reference/catalog/inventory.md)&#x200B;库存同步选项时需要消费者。 请参阅&#x200B;_配置指南_&#x200B;中的[管理消息队列](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html?lang=zh-Hans)。

通常，一天内产生的所有初始预留无法在同一天得到补偿。 当客户在cron作业开始之前下订单或使用离线付款方法（如银行转帐）进行购买时，可能会发生此情况。 补偿的预留序列保留在数据库中，直到它们全部得到补偿。 这种做法不会影响预订的计算，因为每个预订的总数为0。

>[!NOTE]
>
>有些CLI命令可用于检测和管理保留不一致（请参阅[[!DNL Inventory Management] CLI引用](cli.md)）。

### 预订更新

当订单和产品金额的更改完成时，[!DNL Commerce]将自动输入预订补偿。 您无需通过管理员或代码输入补偿，即可更新或清除这些保留。 保留只受输入的保留影响，以便保留数量或清除保留量（补偿保留）。

以下是它们的工作方式：

- **已提交订单** — 为多个产品提交订单时，将输入该金额的预订。 例如，从美国网站订购5个背包会为该SKU和库存输入`-5`的预订。 可销售量减少5。

- **已取消订单** — 取消订单（全部或部分）时，将输入报酬保留以清除该金额。 例如，取消三个背包会为该SKU和股票输入+3预留，从而清除保留。 可销售量增加3。

- **已发运订单** — 当订单全部或部分发运时，将输入报酬保留以结算该金额。 例如，发运两个背包会为该SKU和库存输入+2预留，从而清除保留。 对于装运，产品数量直接减少2。 计算出的可销售量也会根据减少的库存量进行更新，但不再受预订的影响。

![预订更新](assets/diagram-reservation.png){width="600" zoomable="yes"}

当订单完成履行、产品取消、发放贷项通知单等时，必须通过补偿来结算所有预留。 如果补偿没有清除预订，则数量可能会处于停滞状态（不可销售，且永远不可运输）。

>[!NOTE]
>
>如果要复查预留，则可以使用一系列命令行选项。 您只能通过命令行界面复查预留。 使用CLI命令可能需要开发人员协助。 请参阅[[!DNL Inventory Management] CLI引用](cli.md)。

如果从产品中删除具有待定订单的库存的所有来源，则预留可能会卡住。

{{$include /help/_includes/unassign-source.md}}

[1]: https://cloud.google.com/maps-platform/
[2]: https://developers.google.com/maps/documentation/geocoding/start
[3]: https://developers.google.com/maps/documentation/distance-matrix/start

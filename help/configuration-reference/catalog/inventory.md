---
title: '[!UICONTROL Catalog] &amp；gt； [!UICONTROL Inventory]'
description: 查看Commerce管理员的[!UICONTROL Catalog] &amp；gt； [!UICONTROL Inventory]页面上的配置设置。
exl-id: 80113a31-3585-4ee1-95af-31efc09389eb
feature: Configuration, Inventory
source-git-commit: 5a4417373f6dc720e8e14f883c27348a475ec255
workflow-type: tm+mt
source-wordcount: '1195'
ht-degree: 0%

---

# [!UICONTROL Catalog] > [!UICONTROL Inventory]

{{config}}

>[!NOTE]
>
>适用于Adobe Commerce和Magento Open Source的[!DNL Inventory Management]为您提供了用于管理产品库存的工具。 只有一家商店到多个仓库、商店、提货地点、卸货托运人等的商家可以使用这些功能来维护销售数量，并处理发运以完成订单。 有关这些功能以及如何使用这些功能管理多个位置的库存的详细信息，请参阅[_[!DNL Inventory Management]用户指南&#x200B;_](https://experienceleague.adobe.com/docs/commerce-admin/inventory/introduction.html)。

## [!UICONTROL Stock Options]

![股票期权](./assets/catalog-inventory-stock-options.png)<!-- zoom -->

<!-- [Stock Options](https://experienceleague.adobe.com/en/docs/commerce-admin/inventory/configuration/global-options) -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Decrease Stock When Order is Placed] | 全局 | 如果设置为`Yes`，则会在下订单时减少库存数量。 启用&#x200B;_管理库存_&#x200B;后，为订购的产品和数量输入预留。 选项： `Yes` / `No` |
| [!UICONTROL Set Items' Status to be in Stock When Order is Cancelled] | 商店视图 | 如果设置为`Yes`，则在取消订单时将物料返回至库存。 启用&#x200B;_管理库存_&#x200B;后，将为取消的产品和数量清除预留。 选项： `Yes` / `No` |
| [!UICONTROL Display Out of Stock Products] | 全局 | 如果设置为`Yes`，则显示缺货的产品。 如果还启用了产品警报，则客户可以注册以便在产品可用时收到通知。 选项： `Yes` / `No` |
| [!UICONTROL Only X left Threshold] | 网站 | 建立`Only x left`消息的阈值。 例如，如果设置为3，则当库存中有三个或更少项目时，将显示消息。 如果该值设置为`0`，则不会显示该消息。 |
| [!UICONTROL Display products availability in Stock on Storefront] | 商店视图 | 如果设置为`Yes`，则在产品页面上显示`In Stock`或`Out of Stock`消息。 选项： `Yes` / `No` |
| [!UICONTROL Enable Inventory Check On Cart Load] | 全局 | 确定在购物车中加载产品时是否执行库存检查。 禁用此库存检查可以提高结账步骤的性能，尤其是购物车中有许多项目时。 但是，如果您跳过预验证，客户稍后在结账过程中可能会看到&#x200B;_缺货_&#x200B;错误。 选项： `Yes` / `No` |
| [!UICONTROL Synchronize with Catalog] | 全局 | 当设置为`Yes`时，将根据目录更改（如产品移除、产品SKU更改和产品类型更改）调整库存数据，并保持库存和目录之间的一致性。 选项： `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Product Stock Options]

![产品股票期权](./assets/catalog-inventory-product-stock-options.png)<!-- zoom -->

<!-- [Product Stock Options](https://experienceleague.adobe.com/en/docs/commerce-admin/inventory/configuration/global-options) -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Manage Stock] | 全局 | 确定您是否使用完全库存控制来管理目录中的物料。 选项： <br/>**是** — 激活完整库存控制以跟踪当前库存中的项目数。 <br/>**否** — 不跟踪当前库存中的项目数。 |
| [!UICONTROL Backorders] | 全局 | 确定商店管理延期交货的方式。 延交订单不会更改订单的处理状态。 无论产品是否有库存，在下单后仍会立即授权或获取资金。 产品可用后，即会发货。 选项： <br/>**无延交订单** — 产品缺货时不接受延交订单。 <br/>**允许数量低于0** — 在数量低于零时接受延交订单。 <br/>**允许数量低于0并通知客户** — 在数量低于零时接受延交订单，但通知客户仍然可以下订单。 |
| [!UICONTROL Use deferred Stock update] | 全局 | ![Adobe Commerce](../../assets/adobe-logo.svg)(仅限Adobe Commerce)如果允许延期交货，则确定是否延迟库存更新（_延期交货_&#x200B;选项设置为`No backorders`默认值以外的任何值）。 它适用于单个产品或整个网站，并使用&#x200B;_作业队列_&#x200B;机制允许库存数量指标在下订单后异步更新。 此选项也适用于[异步下单](https://experienceleague.adobe.com/docs/commerce-operations/performance-best-practices/high-throughput-order-processing.html#asynchronous-order-placement)和[Inventory management](../../inventory-management/introduction.md)。 |
| 购物车中允许的最大数量 | 全局 | 确定单笔订单可购买产品的最大数量。 默认情况下，最大数量设置为10,000。 |
| [!UICONTROL Out-of-Stock Threshold] | 全局 | 确定将产品视为缺货的库存水平。 选项： <br/>**正金额** — 禁用&#x200B;_延期交货_&#x200B;后，请输入正金额。 启用延交订单后，此金额将被忽略。 <br/>**零** — 启用&#x200B;_延交订单_&#x200B;后，输入`0`将允许无限延交订单。 <br/>**负金额** — 启用&#x200B;_延期交货_&#x200B;后，我们建议输入负金额。 该金额将添加到可销售数量。 例如，输入–50可允许订单数量达到此金额。 |
| [!UICONTROL Minimum Qty Allowed in Shopping Cart] | 全局 | 根据客户组确定可供采购物料的最小金额。 默认情况下，最小数量设置为1。 单击&#x200B;**[!UICONTROL Add Minimum Qty]**&#x200B;为特定客户组输入其他值。 |
| [!UICONTROL Notify for Quantity Below] | 全局 | 确定在库存已低于阈值的情况下发送通知的库存水平。 |
| [!UICONTROL Enable Qty Increments] | 全局 | 确定物料是否可以按数量递增销售。 选项： `Yes` / `No` |
| [!UICONTROL Qty Increments] | 全局 | 确定构成数量增量的产品数量。 |
| [!UICONTROL Automatically Return Credit Memo Item to Stock] | 全局 | 确定是否自动将贷项通知单中包含的物料退回库存。 选项： `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Admin Bulk Operations]

![管理员批量操作](./assets/catalog-inventory-admin-bulk-operations.png)<!-- zoom -->

<!-- [Admin Bulk Operations](https://experienceleague.adobe.com/en/docs/commerce-admin/inventory/configuration/global-options) -->

>[!NOTE]
>
>要配置和支持&#x200B;**异步队列管理器**，必须使用命令行。 这可能需要开发人员的帮助。 请参阅&#x200B;_配置指南_&#x200B;中的[启动消息队列使用者](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/start-message-queues.html)。

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Run asynchronously] | 全局 | 确定您是否为批量产品操作异步运行批量操作，包括[批量](../../inventory-management/bulk-assignment.md)分配源、取消分配源以及[将库存转移到源](../../inventory-management/inventory-transfer.md)。 它将收集到&#x200B;_[!UICONTROL Asynchronous batch size]_&#x200B;的批量操作，然后运行这些操作。 默认情况下，此功能处于禁用状态。 我们建议在启用之前使用批量操作检查您的性能。 选项：<br/>**`Yes`**— 异步运行[!DNL Inventory Management]的所有批量操作。 要启用，必须配置异步队列管理器。<br/>**`No`**— 默认。 不会异步运行批量操作。 |
| [!UICONTROL Asynchronous batch size] | 全局 | 将&#x200B;**[!UICONTROL Run asynchronously]**&#x200B;设置为`Yes`以输入&#x200B;_[!UICONTROL Asynchronous batch size]_&#x200B;字段的值。 <br/>默认批次大小为100。 当批量进程达到此数量时，即会执行。 |

{style="table-layout:auto"}

## [!UICONTROL Inventory Indexer Settings]

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Stock/Source reindex strategy] | 全局 | 确定用于重新编制库存/来源索引的策略。 选项： `Synchronous` / `Asynchronous` （必须为异步模式配置异步队列管理器） |

{style="table-layout:auto"}

>[!NOTE]
>
> 由于依赖与订单相关的活动的库存更新，因此无论`Synchronous`或`Asynchronous`设置如何，在产品保存时也会触发库存索引器。


## [!UICONTROL Distance Provider for Distance Based SSA]

基于距离的SSA的![距离提供程序](./assets/catalog-inventory-distance-provider.png)<!-- zoom -->

<!-- [Distance Providers for Distance Based SSA](https://experienceleague.adobe.com/en/docs/commerce-admin/inventory/configuration/distance-priority-algorithm) -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Provider] | 全局 | 确定要用于Source距离优先级选择算法的提供程序。 此功能默认处于启用状态。 选项： <br/>**`Google MAP`**— 使用Google服务计算送货目标地址与源位置（地址和GPS坐标）之间的距离和时间。 此选项需要Google API密钥，并且可能会通过Google产生费用。<br/>**`Offline Calculation`** — 使用嵌入的数据库计算距离，以确定源地址与送货目标地址之间的最近距离。 要使用此选项，您可能需要开发人员帮助才能使用命令行首先下载您发送到的所有国家/地区的数据库位置内容。 |

{style="table-layout:auto"}

## [!UICONTROL Google Distance Provider]

![Google距离提供程序](./assets/catalog-inventory-distance-provider-settings.png)<!-- zoom -->

<!-- [Google Distance Provider](https://experienceleague.adobe.com/en/docs/commerce-admin/inventory/configuration/distance-priority-algorithm) -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Google API key] | 全局 | 输入Google MAP提供商的Google API密钥。 密钥来自[!DNL Google Maps Platform]，应该启用[!DNL Geocoding API]和[!DNL Distance Matrix API]。 有关详细信息，请参阅&#x200B;_Inventory management指南_&#x200B;中的[配置距离优先级算法](../../inventory-management/distance-priority-algorithm.md#configure-the-distance-priority-algorithm)。 |
| [!UICONTROL Computation mode] | 全局 | 确定方向和路径，以计算距装运地址和分配给库存的所有源的距离。 默认情况下，计算使用驱动模式。 选项： <br/>**`Driving`**— 默认设置，使用路网请求标准行车方向。<br/>**`Walking`** — 使用行人路径和人行道（如果可用）请求步行方向。 <br/>**`Bicycling`**— 使用自行车道和首选街道申请自行车骑行路线（目前仅美国和一些加拿大城市提供）。 |
| [!UICONTROL Value] | 全局 | 指示要计算的来源地点与发运目的地地址的距离和返回的时间。 距离优先级算法建议源与发运目的地地址之间的距离或时间最短，这样可以更快地完成发运，并且可能更便宜。 选项： <br/>**`Distance`**— 返回以公制（公里和米）或英制（英里和英尺）表示的点之间的距离。<br/>**`Time to Destination`** — 返回从源位置到送货地址所需的时间（以小时和分钟为单位）。 |

{style="table-layout:auto"}

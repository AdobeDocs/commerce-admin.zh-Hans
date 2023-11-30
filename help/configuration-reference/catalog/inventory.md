---
title: ’[!UICONTROL Catalog] &gt； [!UICONTROL Inventory]’
description: 查看 [!UICONTROL Catalog] &gt； [!UICONTROL Inventory] 商务管理员页面。
exl-id: 80113a31-3585-4ee1-95af-31efc09389eb
feature: Configuration, Inventory
source-git-commit: 768c9fdc37127b408230983e39e98b11149713a7
workflow-type: tm+mt
source-wordcount: '1205'
ht-degree: 0%

---

# [!UICONTROL Catalog] > [!UICONTROL Inventory]

{{config}}

>[!NOTE]
>
>[!DNL Inventory Management] 适用于Adobe Commerce和Magento Open Source的工具，可让您管理产品库存。 只有一家商店到多个仓库、商店、提货地点、卸货托运人等的商家可以使用这些功能来维护销售数量，并处理发运以完成订单。 有关这些功能以及如何使用这些功能管理多个位置的毛坯的更多信息，请参阅 [_[!DNL Inventory Management] 用户指南&#x200B;_](https://experienceleague.adobe.com/docs/commerce-admin/inventory/introduction.html).

## [!UICONTROL Stock Options]

![股票期权](./assets/catalog-inventory-stock-options.png)<!-- zoom -->

<!-- [Stock Options](https://docs.magento.com/user-guide/catalog/inventory-options-global.html) -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Decrease Stock When Order is Placed] | 全局 | 如果设置为 `Yes`，会减少下订单后的库存量。 替换为 _管理库存_ 启用，则为订购的产品和数量输入预留。 选项： `Yes` / `No` |
| [!UICONTROL Set Items' Status to be in Stock When Order is Cancelled] | 商店视图 | 如果设置为 `Yes`，在取消订单时将物料返回至库存。 替换为 _管理库存_ 启用后，将为已取消的产品和数量清除预留。 选项： `Yes` / `No` |
| [!UICONTROL Display Out of Stock Products] | 全局 | 如果设置为 `Yes`，则显示缺货的产品。 如果还启用了产品警报，则客户可以注册以便在产品可用时收到通知。 选项： `Yes` / `No` |
| [!UICONTROL Only X left Threshold] | 网站 | 建立阈值 `Only x left` 消息。 例如，如果设置为3，则当库存中有三个或更少项目时，将显示消息。 如果将该值设置为，则不会显示该消息 `0`. |
| [!UICONTROL Display products availability in Stock on Storefront] | 商店视图 | 如果设置为 `Yes`，显示 `In Stock` 或 `Out of Stock` 产品页面上的消息。 选项： `Yes` / `No` |
| [!UICONTROL Enable Inventory Check On Cart Load] | 全局 | 确定在购物车中加载产品时是否执行库存检查。 禁用此库存检查可以提高结账步骤的性能，尤其是购物车中有许多项目时。 但是，如果您跳过预验证，客户将看到 _缺货_ 稍后在结账过程中出现错误。 选项： `Yes` / `No` |
| [!UICONTROL Synchronize with Catalog] | 全局 | 当设置为 `Yes`，库存数据根据目录变化（如产品移除、产品SKU变化以及产品类型变化）进行调整，并保持库存和目录之间的一致性。 选项： `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Product Stock Options]

![产品股票期权](./assets/catalog-inventory-product-stock-options.png)<!-- zoom -->

<!-- [Product Stock Options](https://docs.magento.com/user-guide/catalog/inventory-options-global.html) -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Manage Stock] | 全局 | 确定您是否使用完全库存控制来管理目录中的物料。 选项： <br/>**是**  — 激活完全库存控制以跟踪当前库存中的物料数量。 <br/>**否**  — 不跟踪当前库存中的项目数。 |
| [!UICONTROL Backorders] | 全局 | 确定商店管理延期交货的方式。 延交订单不会更改订单的处理状态。 无论产品是否有库存，在下单后仍会立即授权或获取资金。 产品可用后，即会发货。 选项： <br/>**无延交**  — 当产品缺货时，不接受延交订单。 <br/>**允许数量低于0**  — 在数量低于零时接受延交订单。 <br/>**允许数量低于0并通知客户**  — 在数量低于零时接受延交订单，但通知客户仍然可以下订单。 |
| [!UICONTROL Use deferred Stock update] | 全局 | ![Adobe Commerce](../../assets/adobe-logo.svg) (仅限Adobe Commerce)确定在允许延交订单时是否延迟库存更新( _延期交货_ 选项设置为 `No backorders` 默认值)。 它适用于单个产品或整个网站，并使用 _作业队列_ 允许在下订单后异步更新库存数量指示器的机制。 此选项也适用于 [异步下单](https://experienceleague.adobe.com/docs/commerce-operations/performance-best-practices/high-throughput-order-processing.html#asynchronous-order-placement) 与 [Inventory management](../../inventory-management/introduction.md). |
| 购物车中允许的最大数量 | 全局 | 确定单笔订单可购买产品的最大数量。 默认情况下，最大数量设置为10,000。 |
| [!UICONTROL Out-of-Stock Threshold] | 全局 | 确定将产品视为缺货的库存水平。 选项： <br/>**正数**  — 带 _延期交货_ 禁用，请输入正数。 启用延交订单后，此金额将被忽略。 <br/>**零**  — 带 _延期交货_ 已启用，正在输入 `0` 允许无限延交。 <br/>**负金额**  — 带 _延期交货_ 已启用，我们建议输入负数。 该金额将添加到可销售数量。 例如，输入–50可允许订单数量达到此金额。 |
| [!UICONTROL Minimum Qty Allowed in Shopping Cart] | 全局 | 根据客户组确定可供采购物料的最小金额。 默认情况下，最小数量设置为1。 单击 **[!UICONTROL Add Minimum Qty]** 为特定客户组输入不同的值。 |
| [!UICONTROL Notify for Quantity Below] | 全局 | 确定在库存已低于阈值的情况下发送通知的库存水平。 |
| [!UICONTROL Enable Qty Increments] | 全局 | 确定物料是否可以按数量递增销售。 选项： `Yes` / `No` |
| [!UICONTROL Qty Increments] | 全局 | 确定构成数量增量的产品数量。 |
| [!UICONTROL Automatically Return Credit Memo Item to Stock] | 全局 | 确定是否自动将贷项通知单中包含的物料退回库存。 选项： `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Admin Bulk Operations]

![管理员批量操作](./assets/catalog-inventory-admin-bulk-operations.png)<!-- zoom -->

<!-- [Admin Bulk Operations](https://docs.magento.com/user-guide/catalog/inventory-options-global.html) -->

>[!NOTE]
>
>配置和支持 **异步队列管理器**，则必须使用命令行。 这可能需要开发人员的帮助。 请参阅 [启动消息队列使用者](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/start-message-queues.html) 在 _配置指南_.

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Run asynchronously] | 全局 | 确定您是否为批量产品操作异步运行批量操作，包括 [批量](../../inventory-management/bulk-assignment.md) 分配源、取消分配源以及 [将库存转移到来源](../../inventory-management/inventory-transfer.md). 它会收集到 _[!UICONTROL Asynchronous batch size]_，然后运行这些操作。 默认情况下，此功能处于禁用状态。 我们建议在启用之前使用批量操作检查您的性能。 选项：<br/>**`Yes`**— 运行所有批量操作 [!DNL Inventory Management] 非同步。 要启用，必须配置异步队列管理器。<br/>**`No`**— 默认。 不会异步运行批量操作。 |
| [!UICONTROL Asynchronous batch size] | 全局 | 设置 **[!UICONTROL Run asynchronously]** 到 `Yes` 输入值 _[!UICONTROL Asynchronous batch size]_字段。 <br/>默认批次大小为100。 当批量进程达到此数量时，即会执行。 |

{style="table-layout:auto"}

## [!UICONTROL Inventory Indexer Settings]

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Stock/Source reindex strategy] | 全局 | 确定用于重新编制库存/来源索引的策略。 选项： `Synchronous` / `Asynchronous` （必须为异步模式配置异步队列管理器） |

{style="table-layout:auto"}

>[!NOTE]
>
> 由于订单相关活动的库存更新依赖关系，因此库存索引器也会在产品保存时触发，而不考虑 `Synchronous` 或 `Asynchronous` 设置。


## [!UICONTROL Distance Provider for Distance Based SSA]

![基于距离的SSA的距离提供程序](./assets/catalog-inventory-distance-provider.png)<!-- zoom -->

<!-- [Distance Providers for Distance Based SSA](https://docs.magento.com/user-guide/catalog/inventory-configure-distance-priority.html) -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Provider] | 全局 | 确定用于距离优先级源选择算法的提供程序。 此功能默认处于启用状态。 选项： <br/>**`Google MAP`**— 使用Google服务计算送货目标地址与来源位置（地址和GPS坐标）之间的距离和时间。 此选项需要Google API密钥，并且可能会通过Google产生费用。<br/>**`Offline Calculation`**  — 使用嵌入的数据库计算距离，以确定源地址与传送目标地址之间的最近距离。 要使用此选项，您可能需要开发人员帮助才能使用命令行首先下载您发送到的所有国家/地区的数据库位置内容。 |

{style="table-layout:auto"}

## [!UICONTROL Google Distance Provider]

![Google距离提供程序](./assets/catalog-inventory-distance-provider-settings.png)<!-- zoom -->

<!-- [Google Distance Provider](https://docs.magento.com/user-guide/catalog/inventory-configure-distance-priority.html) -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Google API key] | 全局 | 输入Google MAP提供商的Google API密钥。 密钥来自 [!DNL Google Maps Platform] 而且应该有 [!DNL Geocoding API] 和 [!DNL Distance Matrix API] 已启用。 有关详细信息，请参阅 [配置距离优先级算法](../../inventory-management/distance-priority-algorithm.md#configure-the-distance-priority-algorithm) 在 _Inventory management指南_. |
| [!UICONTROL Computation mode] | 全局 | 确定方向和路径，以计算距装运地址和分配给库存的所有源的距离。 默认情况下，计算使用驱动模式。 选项： <br/>**`Driving`**— 默认设置，使用道路网络请求标准行车方向。<br/>**`Walking`**  — 使用人行道和人行道（如果可用）请求步行路线。 <br/>**`Bicycling`**— 使用自行车道和首选街道要求自行车（目前仅在美国和加拿大一些城市提供）。 |
| [!UICONTROL Value] | 全局 | 指示要计算的来源地点与发运目的地地址的距离和返回的时间。 距离优先级算法建议源与发运目的地地址之间的距离或时间最短，这样可以更快地完成发运，并且可能更便宜。 选项： <br/>**`Distance`**— 返回以公制（公里和米）或英制（英里和英尺）为单位的点之间的距离。<br/>**`Time to Destination`**  — 返回从源位置到送货地址所需的时间（以小时和分钟为单位）。 |

{style="table-layout:auto"}

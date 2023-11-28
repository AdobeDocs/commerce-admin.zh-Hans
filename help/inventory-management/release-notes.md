---
title: ’[!DNL Inventory Management] 发行说明
description: 查看发行说明，了解所有 [!DNL Inventory Management] 版本发布。
exl-id: 856b9503-7621-4beb-ac2f-3eb1a240cebc
feature: Inventory, Release Notes
source-git-commit: 7384481d1a4a2a04882d4c99448cca75abc9be31
workflow-type: tm+mt
source-wordcount: '3361'
ht-degree: 0%

---

# [!DNL Inventory Management] 发行说明

以下发行说明介绍了 [!DNL Inventory Management] 并包括：

![新建](../assets/new.svg) 新增功能
![修复的问题](../assets/fix.svg) 修复和改进功能
![已知问题](../assets/bug.svg) 已知问题

[!DNL Inventory Management] 是一个对参与者开放的Magento Open Source社区工程特殊项目。 要参与并做出贡献，请参阅 [GitHub项目](https://github.com/magento/inventory) 存储库和 [维客](https://github.com/magento/inventory/wiki) 以开始使用。 要讨论该项目，请加入 [Slack](https://magentocommeng.slack.com/?redir=%2Farchives%2FC5FU5E2HY) 渠道([自我注册](https://opensource.magento.com/slack))。

[发布计划](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/schedule.html){target="_blank"} 支持版本和兼容版本。

## v1.2.6

[!DNL Inventory Management] 1.2.6(模块版本： `magento/inventory-metapackage = 1.2.6`)在版本2.4.6中受支持，并且与Adobe Commerce版本2.4.0、Adobe Commerce on cloud infrastructure和Magento Open Source代码库兼容。

![修复的问题](../assets/fix.svg) 现在，当已售出的子产品返回到库存中时，店面将复合产品（可配置、捆绑和分组）显示为库存中产品。 之前，店面显示复合产品在这些条件下缺货。 <!-- ACP2E-1106-->

![修复的问题](../assets/fix.svg) 现在，如果可配置产品选项是在数量设置为0且 **[!UICONTROL Display out-of-stock products]** 已启用。 <!-- ACP2E-1148-->

![修复的问题](../assets/fix.svg) 当库存数量发生变化并且产品仍有库存时，类别页面缓存不再失效。 现在，Adobe Commerce从缓存中加载页面，而不是在店面类别页面上的产品数量（没有任何其他变化）发生更改时重新生成页面。 <!-- ACP2E-118-->

![修复的问题](../assets/fix.svg) 现在，在单一来源模式下将库存与类别列表产品计数一起使用时，该类别列表产品计数是正确的 **[!UICONTROL Display Out-Of-Stock Products]** 设置已启用。 Adobe Commerce现在会检查产品在计数时是否可销售。 <!-- ACP2E-1033-->

![修复的问题](../assets/fix.svg) 启用库存后，店内交付的购物车价格规则现在可按预期运行。 以前，在这些情况下不会应用购物车价格规则生成的折扣。 <!-- ACP2E-1015-->

![修复的问题](../assets/fix.svg) 在计划模式下更新产品库存不再清除所有缓存。 以前，清单索引器清除所有配置缓存。 <!-- ACP2E-1003-->

![修复的问题](../assets/fix.svg) 的值 **[!UICONTROL Allow Multiple Boxes for Shipping]** 现在，高级清单中产品的属性按预期保存。 <!-- ACP2E-992-->

![修复的问题](../assets/fix.svg) 现在，Adobe Commerce会在为随店内取货一起下达的订单生成部分退款贷项通知单后，发出准确的保留补偿。 以前，不正确的预订会保存到 `inventory_reservation` 表当管理员用户创建贷项通知单而未选择 **[!UICONTROL Return to Stock]** 复选框。 <!-- ACP2E-979-->

![修复的问题](../assets/fix.svg) 当其某个变体已在实施多来源库存的部署中手动退库时，Adobe Commerce不再将可配置产品显示为缺货。 <!-- ACP2E-952-->

![修复的问题](../assets/fix.svg) 产品网格上的列位置(**[!UICONTROL Catalog]** > **[!UICONTROL Products]**)在配置多个库存源的部署中重新加载页面后，不再恢复到其之前的位置。 <!-- ACP2E-925-->

![修复的问题](../assets/fix.svg) 现在，为虚拟产品签发贷项通知单后，库存数量是正确的，并且 **[!UICONTROL Back to stock]** 未选中复选框。 <!-- ACP2E-908-->

![修复的问题](../assets/fix.svg) 您现在可以使用自动产品排序和分配给非默认库存的范围来保存类别。 以前，Adobe Commerce不保存类别并显示以下错误： `Something went wrong while saving the category`. <!-- ACP2E-859-->

![修复的问题](../assets/fix.svg) 现在，当使用所有缺货的可配置变体创建产品时，可配置产品库存状态会按预期更新。 <!-- ACP2E-813-->

![修复的问题](../assets/fix.svg) 现在，保留不一致分析器工具可以正确处理部分发运的订单，这些订单包含可配置的产品、捆绑产品和分组产品。 现对复合产品类型进行分析。 以前，仅为父产品保存取消和退款，而不为可配置和捆绑捆绑产品中的子产品订单项目保存取消和退款。 <!-- ACP2E-924-->

![修复的问题](../assets/fix.svg) 当管理员用户尝试将200个或更多库存来源分配给库存或产品时，Adobe Commerce不再显示错误。 <!-- ACP2E-1180-->

![修复的问题](../assets/fix.svg) Adobe Commerce现在支持为已删除产品的订单创建贷项通知单。 以前，在创建发票后从订单中删除产品时，商家无法创建贷项通知单。 应用程序显示此错误： `Following products with requested skus were not found: s00001`. t. <!-- ACP2E-1138-->

![修复的问题](../assets/fix.svg) 现在，商店会根据单个或多个商店ID进行过滤。 此 `event` 产品属性代码已添加到保留的属性代码列表中。 以前，当安装了Inventory模块时， Low Stock报表会引发异常。 <!-- ACP2E-1017-->

![修复的问题](../assets/fix.svg) 分层导航筛选器现在可按预期工作，缺货产品现在可附加到店面类别产品列表。 新 `is_out_of_stock` 排序属性使用店面产品集合的Elasticsearch动态字段映射器。 <!-- ACP2E-748-->

![修复的问题](../assets/fix.svg) 当子产品库存状态由REST更改时，复合产品（捆绑、已分组和可配置）库存状态会按预期更新 `POST /rest/V1/inventory/source-items` 呼叫。 <!-- ACP2E-1209-->

## v1.2.5

[!DNL Inventory Management] 1.2.5(模块版本： `magento/inventory-metapackage = 1.2.5`)在版本2.4.5中受支持，并且与Adobe Commerce版本2.4.0、Adobe Commerce on cloud infrastructure和Magento Open Source代码库兼容。

![修复的问题](../assets/fix.svg) 当商家从管理员创建发运时，捆绑产品和分组产品的默认库存库存状态现在会按预期更新。 以前，这些产品的状态在创建装运后保持不变。 <!--- ACP2E-418-->

![修复的问题](../assets/fix.svg) 现在，当满足以下条件之一时，可配置产品会返回到库存： 1. 父产品中至少有一个已保存的子库存。 2.对可配置产品本身进行了更新并设置为 **有货** 并且至少有一个孩子有库存。 <!--- ACP2E-443-->

![修复的问题](../assets/fix.svg) 通过REST API实施的库存更改现在按预期反映在产品详细信息页面上。 现在，在比较上次和当前库存状态之后，会清理目录产品的缓存。 以前，省略回调函数会导致不正确评估库存状态更改，从而不会触发必要的缓存清理。 因此，店面没有反映库存变化。 <!--- ACP2E-161-->

![修复的问题](../assets/fix.svg) 现在，在使用更新源项目后，分配给默认库存且之前缺货的产品将显示在店面上 `/V1/inventory/source-items`. 以前，此REST API端点设置错误 `stock_status`. <!--- ACP2E-562-->

![修复的问题](../assets/fix.svg) 通过批量操作取消分配库存来源(**[!UICONTROL Catalog]** > **[!UICONTROL Products]** > **[!UICONTROL Select Products]** > **[!UICONTROL Actions - Unassign Inventory Source]**)现在，当源包含重复的SKU(前导零除外，例如， `01234` 和 `1234`)。 以前，应用程序不会取消分配库存源，并会引发错误。 <!--- ACP2E-2641-->

![修复的问题](../assets/fix.svg) 产品库存状态现在始终为 **有货** 在店面上，启用无限延期交货订单并将产品分配给自定义库存，而不考虑延期交货的数量。 以前，即使启用了延期交货，产品也会缺货。 <!--- ACP2E-664-->

![修复的问题](../assets/fix.svg) 使用更新源项目后，现在可以正确更新可配置产品的父产品和子产品库存 `POST /V1/inventory/source-items`. 在通过API更新子产品后，新的库存插件会检查默认库存，并更新可配置产品的数量和状态。 <!--- ACP2E-442-->

![修复的问题](../assets/fix.svg) 缺货的分组产品不再列在店面类别页面上。 <!--- ACP2E-2082-->

![修复的问题](../assets/fix.svg) 更正了中的包名称 `CatalogInventory` `composer.json`. <!--- ACP2E-2914-->

![修复的问题](../assets/fix.svg) 现在，在多源/库存部署中下达零数量产品的订单后，可在管理员中正确显示延期交货订单状态。 [GitHub-33756](https://github.com/magento/magento2/issues/33756) <!--- ACP2E-713-->

![修复的问题](../assets/fix.svg) 从库存部分更新捆绑销售产品时，缺货捆绑销售产品不再显示在店面类别页面上。 <!--- ACP2E-2012-->

![修复的问题](../assets/fix.svg) 解决了与PHP 7.4的兼容性问题。 <!--- AC-3192-->

![修复的问题](../assets/fix.svg) 提高了包含包含包含多个选项（多个100）的捆绑产品的保存操作的性能。 以前，保存这些大型捆绑产品需要几分钟时间，并且在启用库存服务的部署中有时会导致超时。 [GitHub-34732](https://github.com/magento/magento2/issues/34732) <!--- AC-1901-->

![修复的问题](../assets/fix.svg) 产品批量操作工具(**[!UICONTROL Select Products]** > **[!UICONTROL Actions]** > **[!UICONTROL Assign Inventory Source]**)现在，在复制SKU（行距除外）时，当将库存来源分配给多个产品时，可以按预期工作 `0` (例如， `01234` 和 `1234`)。 以前，只分配了一个库存来源的产品。 [GitHub-35171](https://github.com/magento/magento2/issues/35171) <!--- AC-2584-->

![修复的问题](../assets/fix.svg) 此 `ProductInterface.only_x_left_in_stock` 如果库存为0，则字段现在返回0。 以前，它返回null。 [GitHub-29932](https://github.com/magento/magento2/issues/29932) <!--- AC-1806-->

![修复的问题](../assets/fix.svg) 您现在可以从管理员编辑默认库存 **[!UICONTROL Stores]** > **[!UICONTROL Inventory]** > **[!UICONTROL Stocks]**. 以前，当您尝试从默认库存添加或删除来源时，控制台中会显示JavaScript错误，不过您可以将网站分配给默认库存。 <!--- ACP2E-545-->

![修复的问题](../assets/fix.svg) <!--- ACP2E-274--> 现在，在库存单一来源模式下使用时，类别列表产品计数是正确的 **[!UICONTROL Display Out-Of-Stock Products]** 设置已启用。 现在，新插件使用 `AreProductsSalableInterface` 和 `StockConfigurationInterface` 以确定产品的总数。 以前，类别产品列表返回错误的产品数量。

![修复的问题](../assets/fix.svg) <!--- ACP2E-322--> 现在，当库存更新后，可配置产品会移至产品列表中的最后一个位置， **[!UICONTROL Move out of stock to the bottom]** 设置已启用。 实施新的自定义数据库查询以使Elasticsearch索引排序顺序无效，这忽视了启用管理员的排序顺序。 以前，启用此设置时，可配置产品及其子产品不会移到列表的底部。

## v1.2.4

Inventory management 1.2.4(模块版本： `magento/inventory-metapackage = 1.2.4`)在版本2.4.4中受支持，并且与Adobe Commerce版本2.4.0、Adobe Commerce on cloud infrastructure和Magento Open Source代码库兼容。

![修复的问题](../assets/fix.svg) Commerce现在在管理员产品列表视图中为所有产品显示准确的可销售数量值。 以前，对于库存产品的可销售数量（包含特殊字符的SKU），它显示空白值。 <!--- MC-41936-->

![修复的问题](../assets/fix.svg) 提高了购物车和结账操作的性能，例如，在具有许多（大约10,000个）库存源的部署中将产品添加到购物车。 <!--- MC-42570-->

![修复的问题](../assets/fix.svg) 此 `bin/magento inventory:reservation:list-inconsistencies` 现在，即使从数据库中丢失了保留并且缓存已被清除，命令仍可正确处理具有部分装运的订单。 以前，如果使用预清除的缓存执行此命令时，Commerce显示以下错误： `Area code is not set`. <!--- MC-42142-->

![修复的问题](../assets/fix.svg) 在共享子项时，对分组产品子产品的增量索引不再导致其他分组产品索引不正确。 <!--- MC-41963-->

![修复的问题](../assets/fix.svg) 现在，通过API从类别中删除产品后，店面类别页面可显示正确的产品计数。 以前，在重新索引之前，类别页面产品计数不正确。 <!--- MC-42287-->

![修复的问题](../assets/fix.svg) 现在，在创建贷项通知单时，如果配置产品满足以下条件，则可以将其返回至库存： **[!UICONTROL Manage Stock]** 选项已禁用。 以前，Commerce不显示 **返回股票** 复选框（在禁用此选项时）。 <!--- MC-42002-->

![修复的问题](../assets/fix.svg) 超过10,000件物品的库存管理已得到改进。 以前，性能问题有时会阻止商家在启动其网站之前编辑管理员中的库存。 <!--- MC-42643-->

![修复的问题](../assets/fix.svg) 此 **[!UICONTROL User Roles]** 管理员中的页面已更新，为管理员提供了对投放方法配置的有限权限访问权限。 此 _配送方式_ 部分已重命名为 _[!UICONTROL Delivery methods]_、和_[!UICONTROL In-Store Pickup]_ 被移到 _[!UICONTROL Delivery methods]_部分。 [GitHub-30053](https://github.com/magento/magento2/issues/30053)  <!--- MC-41545-->

![修复的问题](../assets/fix.svg) 通过API更新贷项通知单后，Adobe Commerce不再创建重复的产品预订。 <!--- MC-41757-->

![修复的问题](../assets/fix.svg) 从切换 _[!UICONTROL Pick up in Store]_按tab键转到_[!UICONTROL Shipping]_ 当只有店内收取交付可用时，结账工作流中的选项卡不再触发JavaScript错误。 <!--- MC-42808-->

![修复的问题](../assets/fix.svg) 可销售产品数量和库存产品数量现在可以正确同步。 以前，不会为已取消的订单重新创建库存预留补偿。 <!--- MC-42485-->

![修复的问题](../assets/fix.svg) 该验证器的性能已得到优化，以防止向捆绑产品的子产品中添加带有装运类型的新源 `Ship Together`. <!--- MC-43039-->

## 1.2.3

[!DNL Inventory Management] 1.2.3(模块版本： `magento/inventory-metapackage = 1.2.3`)在版本2.4.3中受支持，并且与Adobe Commerce版本2.4.0、Adobe Commerce on cloud infrastructure和Magento Open Source代码库兼容。

![修复的问题](../assets/fix.svg) 修复了与前端复合产品可见性相关的几个问题。

![修复的问题](../assets/fix.svg) 以最低所需数量改进了购物车页面管理性能。

![修复的问题](../assets/fix.svg) 修复了多个问题，以解决来源创建、缺货物料、库存采购、已分配来源排序、店内交付和库存命令等问题。

![修复的问题](../assets/fix.svg) [!DNL Commerce] 现在支持使用三位数的加拿大邮政编码进行店内投放。 由于设置的限制，不支持六位数代码 `geonames.org`.

![修复的问题](../assets/fix.svg) 现在，管理员在屏幕上为禁用的产品显示正确的默认库存数量 **产品** 网格和 **编辑产品** 多存储部署页面。

![修复的问题](../assets/fix.svg) [!DNL Commerce] 现在，当捆绑产品重新上架时，将刷新类别产品缓存。

## 1.2.2

[!DNL Inventory Management] 1.2.2(模块版本： `magento/inventory-metapackage = 1.2.2`)在版本2.4.2中受支持，并且与Adobe Commerce版本2.4.0、Adobe Commerce on cloud infrastructure和Magento Open Source代码库兼容。

![修复的问题](../assets/fix.svg) 修复了与前端复合产品可见性相关的几个问题。

![修复的问题](../assets/fix.svg) 改进了B2B数量更新期间的购物车页面性能。

![修复的问题](../assets/fix.svg) 修复了一些问题，旨在解决店内收取情况、批量更新和库存阈值等问题。

![新建](../assets/new.svg) **功能测试。** 引入了新的功能测试，并为现有测试提供了修复，使它们更加稳定。

## 1.2.1

[!DNL Inventory Management] 1.2.1(模块版本： `magento/inventory-metapackage = 1.2.1`)在版本2.4.1中受支持，并且与Adobe Commerce版本2.4.0、Adobe Commerce on cloud infrastructure和Magento Open Source代码库兼容。

![修复的问题](../assets/fix.svg) 修复了与相关的已知问题 `inventory_cleanup_reservations` cron作业并解决了与捆绑产品的店内代答功能相关的问题。 此更新还包括对库存计算、捆绑产品支持和延交功能的常规改进。

![新建](../assets/new.svg) **功能测试。** 引入了新的功能测试，为店内取货功能提供额外的覆盖范围。

## 1.2.0

[!DNL Inventory Management] 1.2.0(模块版本： `magento/inventory-metapackage = 1.2.0`)在Adobe Commerce版本2.4.0、Adobe Commerce on cloud基础架构和Magento Open Source代码库中受支持。

![修复的问题](../assets/fix.svg) 进行了大量修复，以解决源分配问题、支持可扩展环境功能以及与PHP 7.4、MySQL 8和PHPUNIT 9的兼容性。

![新建](../assets/new.svg) **店内投放方法。** 添加了一个选项，让用户在结账时选择用作取车位置的来源。 请参阅 [店内投放](../stores-purchase/shipping-in-store-delivery.md) 在 _销售和购买体验指南_.

![新建](../assets/new.svg) **针对多源模式捆绑产品支持。** 清单支持具有多个来源的所有产品类型。

![新建](../assets/new.svg) **异步重新编制股票索引。** 添加了异步重新索引股票的功能，并提高了几种关键场景的性能。

![新建](../assets/new.svg) **批量接口。** 为可销售性检查引入了新的批量接口： `\Magento\InventorySalesApi\Api\AreProductsSalableInterface`， `\Magento\InventorySalesApi\Api\AreProductsSalableForRequestedQtyInterface`.

![新建](../assets/new.svg) **扩大测试覆盖范围。** 自动测试涵盖了新功能，包括已发现问题和已修复问题的扩展覆盖范围。

![已知问题](../assets/bug.svg) **已知问题。** 缺席 `object_id` 保留元数据中的字段正在阻止 `inventory_cleanup_reservations` cron作业无法正常工作。 此问题已在中引入 [magento/inventory#3046](https://github.com/magento/inventory/pull/3046).

**解决方法：** 执行以下MySQL查询以手动清除保留：

```sql
SELECT GROUP_CONCAT(reservation_id) FROM inventory_reservation GROUP BY stock_id, sku HAVING SUM(quantity) = 0;
DELETE FROM inventory_reservation where reservation_id IN (result_of_the_first_query);
```

## 1.1.6

[!DNL Inventory Management] 1.1.6(模块版本： `inventory-composer-metapackage = 1.1.6`)在版本2.3.6中受支持，并且与版本2.3.5、2.3.4、2.3.3、2.3.2、2.3.1和2.3.0的Adobe Commerce、云基础架构上的Adobe Commerce以及Magento Open Source代码库兼容。

![修复的问题](../assets/fix.svg) 修复了与延交、贷项通知单、低库存报表网格相关的问题，修复了与“解决不一致”CLI工具相关的修复以及进行了常规改进。

![新建](../assets/new.svg) **异步重新编制股票索引。** 添加了异步重新索引股票的功能，并提高了几种关键场景的性能。

## 1.1.5

[!DNL Inventory Management] 1.1.5(模块版本： `inventory-composer-metapackage = 1.1.5`)在版本2.3.5中受支持，并且与Adobe Commerce的版本2.3.4、2.3.3、2.3.2、2.3.1和2.3.0、Adobe Commerce on cloud infrastructure以及Magento Open Source代码库兼容。

![新建](../assets/new.svg) **在产品SKU更改后更新库存。** 引入了新的配置设置以切换到新行为：“与目录同步”。

![新建](../assets/new.svg) **功能测试。** 引入了新的功能测试以消除测试覆盖率差距。 修复了若干问题，使测试更稳定、更可靠)。

![已知问题](../assets/bug.svg) 修复了产品以防止过度销售、在店面中显示产品“缺货”、针对可扩展环境支持和用户界面改进的许多修复。

## 1.1.4

[!DNL Inventory Management] 1.1.4(模块版本： `inventory-composer-metapackage = 1.1.4`)在版本2.3.4中受支持，并且与Adobe Commerce的版本2.3.3、2.3.2、2.3.1和2.3.0、Adobe Commerce on cloud infrastructure和Magento Open Source代码库兼容。

![修复的问题&#x200B;](../assets/fix.svg)**提高了性能。** 为清单保留CLI命令引入了聚集逻辑，以减少内存使用量，避免进程在没有任何响应的情况下卡住的情况。

![新建&#x200B;](../assets/new.svg)**扩大测试覆盖范围。** 引入了许多新的功能测试。 几乎所有手动清单情形都包含自动测试。

![已知问题](../assets/bug.svg) 修复了多个问题，旨在解决贷项通知单、分组产品以及来源和库存成批活动的问题。

## 1.1.3

[!DNL Inventory Management] 1.1.3(模块版本： `inventory-composer-metapackage = 1.1.3`)在版本2.3.3中受支持，并且与Adobe Commerce的版本2.3.2、2.3.1和2.3.0、云基础架构上的Adobe Commerce以及Magento Open Source代码库兼容。

![修复的问题&#x200B;](../assets/fix.svg)**更好地与Adobe Commerce和B2B功能集成。** [!DNL Inventory Management] 现在，对于使用非默认库存源和库存的网站，可以使用以下功能来正常工作：

- 由SKU订购(Adobe Commerce)
- 快速订购(B2B)
- 申购单列表(B2B)

![新建&#x200B;](../assets/new.svg)**提高了性能。** 对于运行默认库存库存和来源的网站，店面目录浏览性能得到了改进。

![新建&#x200B;](../assets/new.svg)**扩大测试覆盖范围。** 自动化功能和集成测试的覆盖范围已显着提高。

## 1.1.2

[!DNL Inventory Management] 1.1.2(模块版本： `inventory-composer-metapackage = 1.1.2`)在版本2.3.2中受支持，并且与Adobe Commerce版本2.3.1、2.3.0、 Adobe Commerce on cloud infrastructure和Magento Open Source代码库兼容。

![修复的问题](../assets/fix.svg) 已添加 `source_code` 对GET的响应 `/V1/shipments` REST端点。 <!-- https://github.com/magento/inventory/pull/2142 -->

![修复的问题](../assets/fix.svg) 解决了在签发未发运订单的贷项通知单后，正确清除保留和更新产品数量的问题。 当您选择选项 <!-- https://github.com/magento/inventory/pull/2179 -->

![修复的问题](../assets/fix.svg) 解决了在创建产品期间输入数量时，正确保存可配置产品子项数量的问题。 <!-- https://github.com/magento/inventory/pull/2158 -->

的新模块 [!DNL Inventory Management] 1.1.2测试版包括：

```php
        'Magento_InventoryGraphQl' => 1,
        'Magento_InventoryReservations' => 1,
        'Magento_InventoryReservationsApi' => 1,
        'Magento_InventoryReservationCli' => 1,
        'Magento_InventoryExportStock' => 0,
        'Magento_InventoryExportStockApi' => 0,
```

![新建](../assets/new.svg) **添加了批量部分库存转移端点**  — 当前批量转移端点将所有分配的数量从来源移动到目标来源。 新 `/rest/V1/inventory/bulk-partial-source-transfer` 端点允许商家作为批量操作将部分库存从源传输到源。 要转移特定数量的数量，请使用以下内容向端点输入请求： `sku`， `qty`， `origin_source_code`、和 `destination_source_code`. 传输验证源是否已分配给 `sku`，则有足够的数量可供转移，等等。 请参阅 [库存成批活动](https://developer.adobe.com/commerce/webapi/rest/inventory/bulk-inventory/){target="_blank"} 在REST API文档中。 <!-- https://github.com/magento/inventory/pull/2117 -->

![新建](../assets/new.svg) **添加了保留CLI**  — 新命令为您提供了检测和解决保留不一致问题的选项。 订单提交和更改状态时， [!DNL Inventory Management] 通过报酬预留生成初始预留和更新。 这些命令会按订单ID、SKU和库存ID返回检测到的不一致列表，并创建要解决的保留。 请参阅 [CLI参考](cli.md) 以了解更多信息。 <!-- https://github.com/magento/inventory/pull/2199 https://github.com/magento/inventory/pull/2184 https://github.com/magento/inventory/pull/2171 https://github.com/magento/inventory/pull/2148  -->

![新建](../assets/new.svg) **针对源和SSA选项的性能改进**  — 在装运期间对来源进行排序和选择，导致来源数量多的库存性能下降。 在复查和选择发运中的SSA选项时，此版本在列出和排序可用来源方面提供了显着的性能改进。 <!-- https://github.com/magento/inventory/pull/2056 https://github.com/magento/inventory/pull/2090 -->

![新建](../assets/new.svg) **添加了对Inventory management的GraphQL支持**  — 此版本将安装新的 `magento/module-inventory-graph-ql` 模块。 GraphQL [ProductInterface属性](https://developer.adobe.com/commerce/webapi/graphql/schema/products/interfaces/attributes/){target="_blank"} 现在包括 `only_x_left_in_stock` 和 `stock_status` 属性 [!DNL Inventory Management] 支持。 <!-- https://github.com/magento/inventory/pull/2124 -->

![新建](../assets/new.svg) **简化的已分配源UI**  — 产品页面中的“分配的源”表格简化了内容，便于进行更新，在显示多个源时提高了性能。 按源名称列出所有源(将鼠标悬停在 `source_code`)。

![新建](../assets/new.svg) **导出汇总的库存服务**  — 此版本提供了新的导出聚合库存服务（保留系统中的预留），以支持外部Sales Channel，如Amazon、eBay和Google购物广告。  <!-- https://github.com/magento/inventory/pull/2067 -->

## 1.1.0

[!DNL Inventory Management] 1.1.0(模块版本： `inventory-composer-metapackage = 1.1.0`)受支持，并且与Adobe Commerce版本2.3.0、云基础架构上的Adobe Commerce和Magento Open Source代码库兼容。 [!DNL Inventory Management] 1.1.1仅作为包名称更新发布，对版本2.3.1提供支持，并与Adobe Commerce版本2.3.0、云基础架构上的Adobe Commerce和Magento Open Source代码库兼容。

![修复的问题](../assets/fix.svg) **增加了对单源模式和多源模式Elasticsearch的支持**  — 您现在可以将Elasticsearch配置和用于自定义库存。 请参阅 [设置Elasticsearch服务](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/service/elasticsearch.html){target="_blank"} 了解安装信息。 <!-- PR https://github.com/magento/inventory/pull/1943 -->

![修复的问题](../assets/fix.svg) 解决了Default Stock的性能问题，大幅提高了多项操作的性能。 改进提高了单一来源模式、“将库存转移至来源”、“店面类别”页和“可销售数量”计算的性能。

<!-- All Performance Track issues resolved https://github.com/magento/inventory/issues?q=is%3Aopen+is%3Aissue+label%3APerformance -->

![修复的问题](../assets/fix.svg) 解决了可配置和分组产品的缺货状态和批量库存转入库存问题。 选择父产品并执行批量操作不会影响产品状态。 如果父产品有库存，则它仍然有库存。

<!-- PR https://github.com/magento/inventory/pull/1972 -->

![新建](../assets/new.svg) **距离优先级算法**  — 距离优先级算法是一种全新的现成源选择算法，用于基于距离的送货推荐。 此算法将发运目的地地址的位置与来源位置进行比较，以确定距离完成发运最近的来源。 该距离可由物理距离或使用导入的地理码位置数据或Google方向（驾驶、步行或骑自行车）从一个位置到另一个位置所花费的时间确定。

![新建](../assets/new.svg) **扩展的源数量列表**  — 具有大量来源的商家可以通过Product Grid轻松移动和查看每个产品的所有来源。 每个产品至少会显示五个来源和匹配数量。 将鼠标悬停在源上时，可以滚动浏览源与当前量的整个列表。

![已知问题](../assets/bug.svg) Magento Open Source和Adobe Commerce v2.3.1的已知问题 — 由于异步API中的主题名称反映了PHP类和方法名称，因此在源之间异步迁移数据时遇到问题。 使用同步操作，设置 **[!UICONTROL Run asynchronously]** 到 `No`，推荐。

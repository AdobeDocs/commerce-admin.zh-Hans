---
title: '[!DNL Inventory Management]发行说明'
description: 查看发行说明，了解所有 [!DNL Inventory Management] 发行版本的信息。
exl-id: 856b9503-7621-4beb-ac2f-3eb1a240cebc
feature: Inventory, Release Notes
source-git-commit: 01d8a1d50f574330f3ce7e8bf03a018f0079f5db
workflow-type: tm+mt
source-wordcount: '3445'
ht-degree: 0%

---

# [!DNL Inventory Management]发行说明

这些发行说明描述了[!DNL Inventory Management]的发行版本，其中包括：

![新](../assets/new.svg)新功能
![已修复问题](../assets/fix.svg)修复和改进
![已知问题](../assets/bug.svg)已知问题

[!DNL Inventory Management]是一个对参与者开放的Magento Open Source社区工程特殊项目。 要参与并做出贡献，请参阅[GitHub项目](https://github.com/magento/inventory)存储库和[wiki](https://github.com/magento/inventory/wiki)以开始操作。 若要讨论此项目，请加入[Slack](https://magentocommeng.slack.com/?redir=%2Farchives%2FC5FU5E2HY)渠道（[自注册](https://opensource.magento.com/slack)）。

[发行计划](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/schedule.html?lang=zh-Hans){target="_blank"}，适用于受支持和兼容的发行版。

## v1.2.7

[!DNL Inventory Management] 1.2.7发行说明包含在[core 2.4.7发行说明](https://experienceleague.adobe.com/zh-hans/docs/commerce-operations/release/notes/adobe-commerce/2-4-7#inventory-management-1)中。

## v1.2.6

版本2.4.6支持[!DNL Inventory Management] 1.2.6（模块版本：`magento/inventory-metapackage = 1.2.6`），并且与Adobe Commerce版本2.4.0、云基础架构上的Adobe Commerce和Magento Open Source代码库兼容。

![已修复问题](../assets/fix.svg)当已售出的子产品返回到库存中时，店面现在将组合产品（可配置、捆绑和分组）显示为库存。 之前，店面显示复合产品在这些条件下缺货。<!-- ACP2E-1106-->

![已修复问题](../assets/fix.svg)如果可配置产品选项是在数量设置为0且启用了&#x200B;**[!UICONTROL Display out-of-stock products]**&#x200B;的情况下创建的，则现在，可配置产品选项在店面上按预期显示为无库存。<!-- ACP2E-1148-->

![已修复问题](../assets/fix.svg)当库存数量发生变化并且产品仍然有库存时，类别页面缓存不再失效。 现在，Adobe Commerce从缓存中加载页面，而不是在店面类别页面上的产品数量（没有任何其他变化）发生更改时重新生成页面。<!-- ACP2E-118-->

![已修复问题](../assets/fix.svg)在启用&#x200B;**[!UICONTROL Display Out-Of-Stock Products]**&#x200B;设置的单源模式下使用库存时，类别列表产品计数现在是正确的。 Adobe Commerce现在会检查产品在计数时是否可销售。<!-- ACP2E-1033-->

在启用库存后，![修复了问题](../assets/fix.svg)店内交货的购物车价格规则现在可按预期工作。 以前，在这些情况下不会应用购物车价格规则生成的折扣。<!-- ACP2E-1015-->

![修复了问题](../assets/fix.svg)在计划模式下更新产品库存不再清除所有缓存。 以前，清单索引器清除所有配置缓存。<!-- ACP2E-1003-->

![修复了问题](../assets/fix.svg)高级库存中产品的&#x200B;**[!UICONTROL Allow Multiple Boxes for Shipping]**&#x200B;属性的值现在按预期保存。<!-- ACP2E-992-->

![已修复问题](../assets/fix.svg) Adobe Commerce现在为随店内提货一起下订单的部分退款贷项通知单发出准确的预订补偿。 以前，当管理员用户创建贷项通知单而未选中&#x200B;**[!UICONTROL Return to Stock]**&#x200B;复选框时，保存到`inventory_reservation`表中的保留不正确。<!-- ACP2E-979-->

![修复了问题](../assets/fix.svg)在执行多源库存的部署中，当其某个变体已手动退回到库存中时，Adobe Commerce不再在店面上将可配置产品显示为缺货。<!-- ACP2E-952-->

![修复了问题](../assets/fix.svg)在配置了多个库存源的部署中重新加载页面后，产品网格上的列位置(**[!UICONTROL Catalog]** > **[!UICONTROL Products]**)不再恢复到其之前的位置。<!-- ACP2E-925-->

![已修复问题](../assets/fix.svg)在未选中&#x200B;**[!UICONTROL Back to stock]**&#x200B;复选框的情况下为虚拟产品签发贷项通知单后，库存数量现在是正确的。<!-- ACP2E-908-->

![已修复问题](../assets/fix.svg)您现在可以使用自动产品排序和范围保存已分配给非默认库存的类别。 以前，Adobe Commerce未保存类别并显示此错误： `Something went wrong while saving the category`。<!-- ACP2E-859-->

![修复了问题](../assets/fix.svg)当使用所有缺货的可配置变体创建产品时，可配置产品库存状态现在会按预期更新。<!-- ACP2E-813-->

![修复了问题](../assets/fix.svg)预订不一致性分析器工具现在可以正确处理包含可配置、捆绑和分组产品的部分装运的订单。 现对复合产品类型进行分析。 以前，仅为父产品保存取消和退款，而不为可配置和捆绑捆绑产品中的子产品订单项目保存取消和退款。<!-- ACP2E-924-->

![修复了问题](../assets/fix.svg)当管理员用户尝试将200个或更多库存源分配给库存或产品时，Adobe Commerce不再显示错误。<!-- ACP2E-1180-->

![已修复问题](../assets/fix.svg) Adobe Commerce现在支持为已删除产品的订单创建贷项通知单。 以前，在创建发票后从订单中删除产品时，商家无法创建贷项通知单。 应用程序显示此错误： `Following products with requested skus were not found: s00001`。 t. <!-- ACP2E-1138-->

![已修复问题](../assets/fix.svg)存储现在已根据单个或多个存储ID进行过滤。 `event`产品属性代码已添加到保留的属性代码列表中。 以前，当安装了Inventory模块时， Low Stock报表会引发异常。<!-- ACP2E-1017-->

![已修复问题](../assets/fix.svg)分层导航筛选器现在按预期工作，缺货产品现在已附加到店面类别产品列表。 新的`is_out_of_stock`排序属性使用Elasticsearch的动态字段映射器作为店面产品集合。<!-- ACP2E-748-->

![修复了问题](../assets/fix.svg)当子产品库存状态通过REST `POST /rest/V1/inventory/source-items`调用更改时，复合产品（捆绑包、已分组和可配置）库存状态将按预期更新。<!-- ACP2E-1209-->

## v1.2.5

版本2.4.5支持[!DNL Inventory Management] 1.2.5（模块版本：`magento/inventory-metapackage = 1.2.5`），并且与Adobe Commerce版本2.4.0、云基础架构上的Adobe Commerce和Magento Open Source代码库兼容。

![已修复问题](../assets/fix.svg)当商家从管理员创建装运时，捆绑包和分组产品的默认库存库存状态现在会按预期更新。 以前，这些产品的状态在创建装运后保持不变。<!--- ACP2E-418-->

![已修复问题](../assets/fix.svg)现在，当满足以下条件之一时，可配置产品将返回到库存： 1. 父产品中至少有一个已保存的子库存。 2.可配置产品本身已更新并在库存&#x200B;**中设置为**，并且库存中至少有一个子项。<!--- ACP2E-443-->

![已修复问题](../assets/fix.svg)通过REST API实施的库存更改现在按预期反映在产品详细信息页面上。 现在，在比较上次和当前库存状态之后，会清理目录产品的缓存。 以前，省略回调函数会导致不正确评估库存状态更改，从而不会触发必要的缓存清理。 因此，店面没有反映库存变化。<!--- ACP2E-161-->

![修复问题](../assets/fix.svg)使用`/V1/inventory/source-items`更新源项目后，现在店面中会显示分配给默认库存且之前缺货的产品。 以前，此REST API端点设置错误的`stock_status`。<!--- ACP2E-562-->

![修复了问题](../assets/fix.svg)当源包含重复的SKU（前导零除外，例如，`01234`和`1234`）时，通过批量操作(**[!UICONTROL Catalog]** > **[!UICONTROL Products]** > **[!UICONTROL Select Products]** > **[!UICONTROL Actions - Unassign Inventory Source]**)取消分配库存源现在可以按预期工作。 以前，应用程序不会取消分配库存源，并会引发错误。<!--- ACP2E-2641-->

![已修复问题](../assets/fix.svg)现在，在启用无限延期交货订单并将产品分配给自定义库存的情况下，无论延期交货的数量是多少，店面的产品库存状态始终为&#x200B;**库存**。 以前，即使启用了延期交货，产品也会缺货。<!--- ACP2E-664-->

![已修复问题](../assets/fix.svg)使用`POST /V1/inventory/source-items`更新源项后，现在可正确更新可配置的产品父产品和子产品库存。 在通过API更新子产品后，新的库存插件会检查默认库存，并更新可配置产品的数量和状态。<!--- ACP2E-442-->

![已修复问题](../assets/fix.svg)店面类别页面上不再列出缺货的分组产品。<!--- ACP2E-2082-->

![修复了问题](../assets/fix.svg)更正了`CatalogInventory` `composer.json`中的包名称。<!--- ACP2E-2914-->

![已修复问题](../assets/fix.svg)在多源/库存部署中下达了零数量产品的订单后，管理员现在可正确显示延期交货订单状态。 [GitHub-33756](https://github.com/magento/magento2/issues/33756) <!--- ACP2E-713-->

![已修复问题](../assets/fix.svg)当捆绑产品从库存部分更新时，缺货的捆绑产品不再显示在店面类别页面上。<!--- ACP2E-2012-->

![已修复问题](../assets/fix.svg)已解决与PHP 7.4的兼容性问题。<!--- AC-3192-->

![修复了问题](../assets/fix.svg)提高了包含包含包含多个选项（多个100）的捆绑产品的保存操作的性能。 以前，保存这些大型捆绑产品需要几分钟时间，并且在启用库存服务的部署中有时会导致超时。 [GitHub-34732](https://github.com/magento/magento2/issues/34732) <!--- AC-1901-->

![修复了问题](../assets/fix.svg)当复制SKU时，将库存来源分配给多个产品时，产品批量操作工具(**[!UICONTROL Select Products]** > **[!UICONTROL Actions]** > **[!UICONTROL Assign Inventory Source]**)现在可按预期工作，但前导的`0`除外（例如`01234`和`1234`）。 以前，只分配了一个库存来源的产品。 [GitHub-35171](https://github.com/magento/magento2/issues/35171) <!--- AC-2584-->

![已修复问题](../assets/fix.svg)如果库存为0，则`ProductInterface.only_x_left_in_stock`字段现在返回0。 以前，它返回null。 [GitHub-29932](https://github.com/magento/magento2/issues/29932) <!--- AC-1806-->

![已修复问题](../assets/fix.svg)您现在可以从管理员&#x200B;**[!UICONTROL Stores]** > **[!UICONTROL Inventory]** > **[!UICONTROL Stocks]**&#x200B;编辑默认库存。 以前，当您尝试从默认库存添加或删除来源时，控制台中会显示JavaScript错误，不过您可以将网站分配给默认库存。<!--- ACP2E-545-->

![修复了问题](../assets/fix.svg) <!--- ACP2E-274-->在启用&#x200B;**[!UICONTROL Display Out-Of-Stock Products]**&#x200B;设置的情况下使用库存单源模式时，类别列表产品计数现在是正确的。 新插件现在使用`AreProductsSalableInterface`和`StockConfigurationInterface`来确定产品总数。 以前，类别产品列表返回错误的产品数量。

![修复的问题](../assets/fix.svg) <!--- ACP2E-322-->启用&#x200B;**[!UICONTROL Move out of stock to the bottom]**&#x200B;设置后，库存更新后，可配置产品现在移至产品列表中的最后一个位置。 实施新的自定义数据库查询以使Elasticsearch索引排序顺序无效，这忽视了启用管理员的排序顺序。 以前，启用此设置时，可配置产品及其子产品不会移到列表的底部。

## v1.2.4

Inventory management 1.2.4（模块版本： `magento/inventory-metapackage = 1.2.4`）受版本2.4.4支持，并且与Adobe Commerce版本2.4.0、云基础架构上的Adobe Commerce和Magento Open Source代码库兼容。

![已修复问题](../assets/fix.svg) Commerce现在在管理员产品列表视图中显示所有产品的准确可销售数量值。 以前，对于库存产品的可销售数量（包含特殊字符的SKU），它显示空白值。<!--- MC-41936-->

![修复了问题](../assets/fix.svg)购物车和结账操作的性能已得到改进，例如，在具有许多（大约10,000个）库存源的部署中将产品添加到购物车。<!--- MC-42570-->

![修复了问题](../assets/fix.svg) `bin/magento inventory:reservation:list-inconsistencies`命令现在可以正确处理具有部分装运的订单，即使从数据库中缺少保留并且缓存已清除也是如此。 以前，当使用预清除的缓存执行此命令时，Commerce显示以下错误： `Area code is not set`。<!--- MC-42142-->

![修复了问题](../assets/fix.svg)在共享子项时，对分组产品子产品的增量索引不再导致其他分组产品索引不正确。<!--- MC-41963-->

![已修复问题](../assets/fix.svg)通过API从类别中删除产品后，店面类别页面现在显示正确的产品计数。 以前，在重新索引之前，类别页面产品计数不正确。<!--- MC-42287-->

![已修复问题](../assets/fix.svg)禁用&#x200B;**[!UICONTROL Manage Stock]**&#x200B;选项后，创建贷项通知单时，现在可配置产品可返回库存。 以前，在禁用此选项的情况下，Commerce不会在贷项通知单创建页面上显示&#x200B;**返回库存**&#x200B;复选框。<!--- MC-42002-->

![修复了问题](../assets/fix.svg)已改进对超过10,000个项目的库存库存库存的管理。 以前，性能问题有时会阻止商家在启动其网站之前编辑管理员中的库存。<!--- MC-42643-->

![已修复问题](../assets/fix.svg)管理员中的&#x200B;**[!UICONTROL User Roles]**&#x200B;页面已更新，以便为管理员提供对投放方法配置的受限权限访问权限。 _配送方式_&#x200B;部分已重命名为&#x200B;_[!UICONTROL Delivery methods]_，且&#x200B;_[!UICONTROL In-Store Pickup]_&#x200B;被移动到&#x200B;_[!UICONTROL Delivery methods]_&#x200B;部分下。 [GitHub-30053](https://github.com/magento/magento2/issues/30053) <!--- MC-41545-->

![已修复问题](../assets/fix.svg) Adobe Commerce在贷项通知单由API更新后不再创建重复的产品预订。<!--- MC-41757-->

![修复了问题](../assets/fix.svg)在结账工作流中从&#x200B;_[!UICONTROL Pick up in Store]_&#x200B;选项卡切换到&#x200B;_[!UICONTROL Shipping]_&#x200B;选项卡时，如果只有店内收取投放可用，则不再触发JavaScript错误。<!--- MC-42808-->

![已修复问题](../assets/fix.svg)可销售产品数量和库存产品数量现已正确同步。 以前，不会为已取消的订单重新创建库存预留补偿。<!--- MC-42485-->

![已修复问题](../assets/fix.svg)已优化验证器的性能，以防止向装运类型为`Ship Together`的捆绑产品的子产品添加新源。<!--- MC-43039-->

## 1.2.3

版本2.4.3支持[!DNL Inventory Management] 1.2.3（模块版本：`magento/inventory-metapackage = 1.2.3`），并且与Adobe Commerce版本2.4.0、云基础架构上的Adobe Commerce和Magento Open Source代码库兼容。

![修复了问题](../assets/fix.svg)修复了多个与前端上的复合产品可见性相关的问题。

![已修复问题](../assets/fix.svg)使用所需的最小数量提高了购物车页面管理性能。

![修复了问题](../assets/fix.svg)针对解决源创建、缺货物料、库存采购、已分配源排序、店内交付和库存命令等问题的多个修复。

![已修复问题](../assets/fix.svg) [!DNL Commerce]现在支持使用三位数的加拿大邮政编码进行店内投放。 由于`geonames.org`设置的限制，不支持六位数代码。

![已修复问题](../assets/fix.svg)对于多商店部署，管理员现在在&#x200B;**产品**&#x200B;网格和&#x200B;**编辑产品**&#x200B;页面上显示已禁用产品的正确默认库存数量。

![修复了问题](../assets/fix.svg) [!DNL Commerce]现在在捆绑产品重新上架时刷新类别产品缓存。

## 1.2.2

版本2.4.2支持[!DNL Inventory Management] 1.2.2（模块版本：`magento/inventory-metapackage = 1.2.2`），并且与Adobe Commerce版本2.4.0、云基础架构上的Adobe Commerce和Magento Open Source代码库兼容。

![修复了问题](../assets/fix.svg)修复了多个与前端上的复合产品可见性相关的问题。

![修复了问题](../assets/fix.svg)在B2B的数量更新期间改善了购物车页面性能。

![已修复问题](../assets/fix.svg)针对解决店内提货、批量更新和库存阈值问题的多个修复。

![新](../assets/new.svg) **功能测试。**&#x200B;引入了新的功能测试，并为现有测试提供了修复，以使测试更加稳定。

## 1.2.1

版本2.4.1支持[!DNL Inventory Management] 1.2.1（模块版本：`magento/inventory-metapackage = 1.2.1`），并且与Adobe Commerce版本2.4.0、云基础架构上的Adobe Commerce和Magento Open Source代码库兼容。

![修复了问题](../assets/fix.svg)修复了与`inventory_cleanup_reservations` cron作业相关的已知问题，并解决了与捆绑产品的店内代答功能相关的问题。 此更新还包括对库存计算、捆绑产品支持和延交功能的常规改进。

![新](../assets/new.svg) **功能测试。**&#x200B;引入了新功能测试，为店内取货功能提供了额外的覆盖范围。

## 1.2.0

Adobe Commerce版本2.4.0、云基础架构上的Adobe Commerce和Magento Open Source代码库支持[!DNL Inventory Management] 1.2.0（模块版本：`magento/inventory-metapackage = 1.2.0`）。

![修复了问题](../assets/fix.svg)修复了许多问题，以解决源分配问题、可扩展环境功能支持问题以及与PHP 7.4、MySQL 8和PHPUNIT 9的兼容性问题。

![新](../assets/new.svg) **店内传递方法。**&#x200B;添加了一个选项，用户可选择在结账期间用作取车位置的来源。 请参阅&#x200B;_销售和购买体验指南_&#x200B;中的[店内递送](../stores-purchase/shipping-in-store-delivery.md)。

![新](../assets/new.svg) **包产品支持多源模式。**&#x200B;库存支持具有多个来源的所有产品类型。

![新](../assets/new.svg) **异步股票重新索引。**&#x200B;添加了异步为股票重新索引的功能，并提高了几个关键方案的性能。

![新](../assets/new.svg) **批量接口。**&#x200B;为可访问性检查引入了新的批量接口： `\Magento\InventorySalesApi\Api\AreProductsSalableInterface`，`\Magento\InventorySalesApi\Api\AreProductsSalableForRequestedQtyInterface`。

![新](../assets/new.svg) **已增加测试覆盖率。**&#x200B;自动测试涵盖了新功能，包括已发现问题和已修复问题的扩展覆盖范围。

![已知问题](../assets/bug.svg) **已知问题。**&#x200B;保留元数据中缺少`object_id`字段导致`inventory_cleanup_reservations` cron作业无法正常工作。 此问题已在[magento/inventory#3046](https://github.com/magento/inventory/pull/3046)中引入。

**解决方法：**&#x200B;执行以下MySQL查询以手动清除保留：

```sql
SELECT GROUP_CONCAT(reservation_id) FROM inventory_reservation GROUP BY stock_id, sku HAVING SUM(quantity) = 0;
DELETE FROM inventory_reservation where reservation_id IN (result_of_the_first_query);
```

## 1.1.6

版本2.3.6支持[!DNL Inventory Management] 1.1.6（模块版本： `inventory-composer-metapackage = 1.1.6`），并且与Adobe Commerce的版本2.3.5、2.3.4、2.3.3、2.3.2、2.3.1和2.3.0、云基础架构上的Adobe Commerce以及Magento Open Source代码库兼容。

![修复了问题](../assets/fix.svg)修复了以下问题：延期交货、贷项通知单、低库存报表网格、连接到“解决不一致”CLI工具的修复以及一般改进。

![新](../assets/new.svg) **异步股票重新索引。**&#x200B;添加了异步为股票重新索引的功能，并提高了几个关键方案的性能。

## 1.1.5

版本2.3.5支持[!DNL Inventory Management] 1.1.5（模块版本： `inventory-composer-metapackage = 1.1.5`），并且与Adobe Commerce的版本2.3.4、2.3.3、2.3.2、2.3.1和2.3.0、云基础架构上的Adobe Commerce以及Magento Open Source代码库兼容。

![新建](../assets/new.svg) **在产品SKU更改后更新库存。**&#x200B;引入了一个新的配置设置以切换到新行为：“与目录同步”。

![新](../assets/new.svg) **功能测试。**&#x200B;引入了新功能测试以消除测试覆盖率差距。 修复了若干问题，使测试更稳定、更可靠)。

![已知问题](../assets/bug.svg)修复以防止产品过度销售、店面上“缺货”产品可见性、针对可扩展环境支持和用户界面改进的众多修复。

## 1.1.4

版本2.3.4支持[!DNL Inventory Management] 1.1.4（模块版本： `inventory-composer-metapackage = 1.1.4`），并且与Adobe Commerce的版本2.3.3、2.3.2、2.3.1和2.3.0、云基础架构上的Adobe Commerce以及Magento Open Source代码库兼容。

![修复了问题&#x200B;](../assets/fix.svg)**提高了性能。**&#x200B;为清单保留CLI命令引入了聚集逻辑，以减少内存使用量，避免进程在没有任何响应的情况下卡住的情况。

![新&#x200B;](../assets/new.svg)**测试覆盖率提高。**&#x200B;引入了许多新的功能测试。 几乎所有手动清单情形都包含自动测试。

![已知问题](../assets/bug.svg)针对解决贷项通知单、分组产品以及来源和库存批量操作问题的大量修复。

## 1.1.3

版本2.3.3支持[!DNL Inventory Management] 1.1.3（模块版本： `inventory-composer-metapackage = 1.1.3`），并且与Adobe Commerce的版本2.3.2、2.3.1和2.3.0、云基础架构上的Adobe Commerce以及Magento Open Source代码库兼容。

![已修复问题&#x200B;](../assets/fix.svg)**更好地与Adobe Commerce和B2B功能集成。对于使用非默认库存源和库存的网站，** [!DNL Inventory Management]现在可以使用以下功能正常工作：

- 由SKU订购(Adobe Commerce)
- 快速订购(B2B)
- 申购单列表(B2B)

![新&#x200B;](../assets/new.svg)**性能提高。针对运行默认库存库存和来源的网站，**&#x200B;店面目录浏览性能得到了改进。

![新&#x200B;](../assets/new.svg)**测试覆盖率提高。**&#x200B;自动化功能和集成测试覆盖率已显着提高。

## 1.1.2

版本2.3.2支持[!DNL Inventory Management] 1.1.2（模块版本： `inventory-composer-metapackage = 1.1.2`），并且与Adobe Commerce版本2.3.1、2.3.0、云基础架构上的Adobe Commerce以及Magento Open Source代码库兼容。

![修复了问题](../assets/fix.svg)已将`source_code`添加到GET`/V1/shipments` REST终结点的响应中。<!-- https://github.com/magento/inventory/pull/2142 -->

![已修复问题](../assets/fix.svg)已解决在签发未发运订单的贷项通知单后正确清除保留和更新产品数量的问题。 当您选择<!-- https://github.com/magento/inventory/pull/2179 -->的选项时

![修复了问题](../assets/fix.svg)解决了在创建产品期间输入数量时，为可配置产品子项正确保存数量的问题。<!-- https://github.com/magento/inventory/pull/2158 -->

[!DNL Inventory Management] 1.1.2 Beta的新模块包括：

```php
        'Magento_InventoryGraphQl' => 1,
        'Magento_InventoryReservations' => 1,
        'Magento_InventoryReservationsApi' => 1,
        'Magento_InventoryReservationCli' => 1,
        'Magento_InventoryExportStock' => 0,
        'Magento_InventoryExportStockApi' => 0,
```

![新](../assets/new.svg) **添加了一个批量部分库存转移终结点** — 当前批量转移终结点将所有分配的数量从来源移动到目标来源。 新`/rest/V1/inventory/bulk-partial-source-transfer`终结点允许商家作为批量操作将部分库存从源转移到源。 要转移特定数量的数量，请输入具有`sku`、`qty`、`origin_source_code`和`destination_source_code`的终结点请求。 转移验证源是否分配给`sku`，是否存在足够的数量可转移，等等。 请参阅REST API文档中的[清单批量操作](https://developer.adobe.com/commerce/webapi/rest/inventory/bulk-inventory/){target="_blank"}。<!-- https://github.com/magento/inventory/pull/2117 -->

![新](../assets/new.svg) **已添加保留CLI** — 新命令为您提供了检测和解决保留不一致问题的选项。 在订单提交并更改状态时，[!DNL Inventory Management]通过报酬预留生成初始预留和更新。 这些命令会按订单ID、SKU和库存ID返回检测到的不一致列表，并创建要解决的保留。 有关详细信息，请参阅[CLI引用](cli.md)。<!-- https://github.com/magento/inventory/pull/2199 https://github.com/magento/inventory/pull/2184 https://github.com/magento/inventory/pull/2171 https://github.com/magento/inventory/pull/2148  -->

![新](../assets/new.svg) **源和SSA选项的性能改进** — 在装运期间排序和选择源导致源数量多的库存性能下降。 在复查和选择发运中的SSA选项时，此版本在列出和排序可用来源方面提供了显着的性能改进。<!-- https://github.com/magento/inventory/pull/2056 https://github.com/magento/inventory/pull/2090 -->

![新](../assets/new.svg) **已添加对Inventory management的GraphQL支持** — 此版本安装了一个新的`magento/module-inventory-graph-ql`模块。 GraphQL [ProductInterface属性](https://developer.adobe.com/commerce/webapi/graphql/schema/products/interfaces/attributes/){target="_blank"}现在包含用于[!DNL Inventory Management]支持的`only_x_left_in_stock`和`stock_status`属性。<!-- https://github.com/magento/inventory/pull/2124 -->

![新](../assets/new.svg) **简化的已分配源UI** — 产品页面中的“已分配源”表简化了内容，以便更轻松地更新，并且在显示多个源时提高了性能。 按源名称列出所有源（将鼠标悬停在`source_code`上）。

![新](../assets/new.svg) **导出汇总库存服务** — 此版本提供了新的导出汇总库存服务（保留系统中的预留）以支持外部Sales Channel，如Amazon、eBay和Google购物广告。 <!-- https://github.com/magento/inventory/pull/2067 -->

## 1.1.0

[!DNL Inventory Management] 1.1.0（模块版本： `inventory-composer-metapackage = 1.1.0`）受支持，并且与Adobe Commerce版本2.3.0、云基础架构上的Adobe Commerce和Magento Open Source代码库兼容。 [!DNL Inventory Management] 1.1.1仅作为包名称更新发布，对版本2.3.1提供支持，并与Adobe Commerce版本2.3.0、云基础架构上的Adobe Commerce和Magento Open Source代码库兼容。

![已修复问题](../assets/fix.svg) **已添加对单源模式和多源模式Elasticsearch的支持** — 您现在可以将Elasticsearch配置用于自定义股票。 有关安装信息，请参阅[设置Elasticsearch服务](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/service/elasticsearch.html?lang=zh-Hans){target="_blank"}。<!-- PR https://github.com/magento/inventory/pull/1943 -->

![已修复问题](../assets/fix.svg)解决了默认库存的性能问题，从而通过大量操作显着提高性能。 改进提高了单一来源模式、“将库存转移到Source”、“店面类别”页面和“可销售数量”计算的性能。

<!-- All Performance Track issues resolved https://github.com/magento/inventory/issues?q=is%3Aopen+is%3Aissue+label%3APerformance -->

![已修复问题](../assets/fix.svg)已解决可配置和分组产品的缺货状态和批量库存转储问题。 选择父产品并执行批量操作不会影响产品状态。 如果父产品有库存，则它仍然有库存。

<!-- PR https://github.com/magento/inventory/pull/1972 -->

![新](../assets/new.svg) **距离优先级算法** — 距离优先级算法是一种用于基于距离的送货推荐的现成新的Source选择算法。 此算法将发运目的地地址的位置与来源位置进行比较，以确定距离完成发运最近的来源。 该距离可由物理距离或使用导入的地理码位置数据或Google方向（驾驶、步行或骑自行车）从一个位置到另一个位置所花费的时间确定。

![新](../assets/new.svg) **扩展源数量列表** — 具有大量源的商家可以通过产品网格轻松移动和查看每个产品的所有源。 每个产品至少会显示五个来源和匹配数量。 将鼠标悬停在源上时，可以滚动浏览源与当前量的整个列表。

![已知问题](../assets/bug.svg)Magento Open Source和Adobe Commerce v2.3.1的已知问题 — 由于异步API中的主题名称反映了PHP类和方法名称，因此在源之间的异步数据迁移遇到问题。 建议使用同步操作，将&#x200B;**[!UICONTROL Run asynchronously]**&#x200B;设置为`No`。

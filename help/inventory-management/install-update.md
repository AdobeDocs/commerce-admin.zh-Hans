---
title: 安装、更新和删除 [!DNL Inventory Management]
description: 了解如何管理 [!DNL Inventory Management] 中继。
exl-id: d088ff35-c0e1-41c8-89fb-78180eaefbf7
level: Experienced
feature: Inventory, Install
badgePaas: label="仅限PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="仅适用于云项目(Adobe管理的PaaS基础架构)和内部部署项目上的Adobe Commerce 。"
source-git-commit: b4623ada788d44f4628930dcf5dfcb51dd88ee3a
workflow-type: tm+mt
source-wordcount: '620'
ht-degree: 0%

---

# 安装、更新和删除[!DNL Inventory Management]

[!DNL Inventory Management]模块为单一来源和多来源商家提供所有库存功能和选项，以管理销售渠道的产品数量和库存。 Adobe Commerce和Magento Open Source的2.4.x版本中提供了这些功能。

这些功能和扩展是通过Magento Open Source社区工程计划作为[清单项目](https://github.com/magento/inventory)的一部分开发的。

[!DNL Inventory Management]安装在Adobe Commerce和Magento Open Source的2.3.x和2.4.x版本中，默认启用所有功能。 启用这些清单功能无需执行其他步骤。 从v2.1.x或2.2.x升级可能需要额外的步骤。 请参阅[升级Inventory management](#upgrade-inventory-management)。

建议根据[快速入门本地安装](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/composer.html){target="_blank"}进行安装。 使用中继包安装以接收所有[!DNL Inventory Management]模块。

`composer.json`中继包中的以下行安装[!DNL Inventory Management]：

```json
        magento/inventory-composer-metapackage = 1.1.3
```

有关[!DNL Inventory Management]中继包版本的列表，请参阅[发行说明](release-notes.md)。

[!DNL Inventory Management]安装过程将所有模块添加到`<Magento_installation_directory>/app/etc/config.php`文件中。 `1`值表示相应的模块已启用。 添加了以下模块列表：

```php
        'Magento_Inventory' => 1,
        'Magento_InventoryAdminUi' => 1,
        'Magento_InventoryAdvancedCheckout' => 1,
        'Magento_InventoryApi' => 1,
        'Magento_InventoryBundleProduct' => 1,
        'Magento_InventoryBundleProductAdminUi' => 1,
        'Magento_InventoryCatalog' => 1,
        'Magento_InventorySales' => 1,
        'Magento_InventoryCatalogAdminUi' => 1,
        'Magento_InventoryCatalogApi' => 1,
        'Magento_InventoryCatalogSearch' => 1,
        'Magento_InventoryConfigurableProduct' => 1,
        'Magento_InventoryConfigurableProductAdminUi' => 1,
        'Magento_InventoryConfigurableProductIndexer' => 1,
        'Magento_InventoryConfiguration' => 1,
        'Magento_InventoryConfigurationApi' => 1,
        'Magento_InventoryDistanceBasedSourceSelection' => 1,
        'Magento_InventoryDistanceBasedSourceSelectionAdminUi' => 1,
        'Magento_InventoryDistanceBasedSourceSelectionApi' => 1,
        'Magento_InventoryElasticsearch' => 1,
        'Magento_InventoryExportStockApi' => 1,
        'Magento_InventoryIndexer' => 1,
        'Magento_InventorySalesApi' => 1,
        'Magento_InventoryGroupedProduct' => 1,
        'Magento_InventoryGroupedProductAdminUi' => 1,
        'Magento_InventoryGroupedProductIndexer' => 1,
        'Magento_InventoryImportExport' => 1,
        'Magento_InventoryCache' => 1,
        'Magento_InventoryLowQuantityNotification' => 1,
        'Magento_InventoryLowQuantityNotificationApi' => 1,
        'Magento_InventoryMultiDimensionalIndexerApi' => 1,
        'Magento_InventoryProductAlert' => 1,
        'Magento_InventoryRequisitionList' => 1,
        'Magento_InventoryReservations' => 1,
        'Magento_InventoryReservationCli' => 1,
        'Magento_InventoryReservationsApi' => 1,
        'Magento_InventoryExportStock' => 1,
        'Magento_InventorySalesAdminUi' => 1,
        'Magento_InventorySalesFrontendUi' => 1,
        'Magento_InventorySetupFixtureGenerator' => 1,
        'Magento_InventoryShipping' => 1,
        'Magento_InventorySourceDeductionApi' => 1,
        'Magento_InventorySourceSelection' => 1,
        'Magento_InventorySourceSelectionApi' => 1,
        'Magento_InventoryLowQuantityNotificationAdminUi' => 1,
        'Magento_InventoryShippingAdminUi' => 1,
        'Magento_InventoryGraphQl' => 1,
```

## 启用[!DNL Inventory Management]功能

安装、升级或更新后，Admin中的&#x200B;_[!UICONTROL Manage Stock]_选项默认启用。 此选项启用库存跟踪和管理，但不影响模块状态。 要禁用模块，请参阅下一部分。

有关配置的详细信息，请参阅[配置Inventory management](configuration.md)。

## 禁用Inventory management

>[!IMPORTANT]
>
>强烈建议使用默认[!DNL Inventory Management]模块。 用于已禁用[!DNL Inventory Management]模块的系统的替代[!DNL CatalogInventory]模块现已弃用。 禁用[!DNL Inventory Management]模块可能会导致系统不稳定并导致各种问题。

您可能要禁用[!DNL Inventory Management]模块以：

* 加速从2.0.x、2.1.x、2.2.x或2.3.x迁移到2.4.x的商户升级过程。
* 使用自定义或第三方库存和订单管理系统模块。

有关如何禁用适用模块的信息，请参阅&#x200B;_安装指南_&#x200B;中的[启用或禁用模块](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/manage-modules.html)页面。

完成后，系统将在`<Magento_installation_directory>/app/etc/config.php`中提供模块和值的列表，开头为：

```php
   'Magento_Inventory' => 0,
   'Magento_InventoryAdminUi' => 0,
   'Magento_InventoryAdvancedCheckout' => 0,
   ...
```

>[!IMPORTANT]
>
>如果安装了OMS连接器模块，请确保不禁用`Magento_InventoryMessageBus`模块，该模块是连接器模块。 需要将连接器与OMS一起使用。

## 删除Inventory management

>[!IMPORTANT]
>
>强烈建议使用默认[!DNL Inventory Management]模块。 替代模块[!DNL CatalogInventory]用于已移除[!DNL Inventory Management]模块的系统，现已弃用。 删除[!DNL Inventory Management]模块可能会导致系统不稳定并导致各种问题。

如果您选择不使用[!DNL Inventory Management]功能，则可以删除（卸载）这些模块。 要通过编辑器文件删除所有模块，请将以下内容添加到`composer.json`：

```
"replace": {
        "magento/module-inventory": "*",
        "magento/module-inventory-admin-ui": "*",
        "magento/module-inventory-advanced-checkout": "*",
        "magento/module-inventory-api": "*",
        "magento/module-inventory-bundle-product": "*",
        "magento/module-inventory-bundle-product-admin-ui": "*",
        "magento/module-inventory-cache": "*",
        "magento/module-inventory-catalog": "*",
        "magento/module-inventory-catalog-admin-ui": "*",
        "magento/module-inventory-catalog-api": "*",
        "magento/module-inventory-catalog-search": "*",
        "magento/module-inventory-configurable-product": "*",
        "magento/module-inventory-configurable-product-admin-ui": "*",
        "magento/module-inventory-configurable-product-indexer": "*",
        "magento/module-inventory-configuration": "*",
        "magento/module-inventory-configuration-api": "*",
        "magento/module-inventory-distance-based-source-selection": "*",
        "magento/module-inventory-distance-based-source-selection-admin-ui": "*",
        "magento/module-inventory-distance-based-source-selection-api": "*",
        "magento/module-inventory-export-stock": "*",
        "magento/module-inventory-export-stock-api": "*",
        "magento/module-inventory-elasticsearch": "*",
        "magento/module-inventory-graph-ql": "*",
        "magento/module-inventory-grouped-product": "*",
        "magento/module-inventory-grouped-product-admin-ui": "*",
        "magento/module-inventory-grouped-product-indexer": "*",
        "magento/module-inventory-import-export": "*",
        "magento/module-inventory-indexer": "*",
        "magento/module-inventory-low-quantity-notification": "*",
        "magento/module-inventory-low-quantity-notification-admin-ui": "*",
        "magento/module-inventory-low-quantity-notification-api": "*",
        "magento/module-inventory-multi-dimensional-indexer-api": "*",
        "magento/module-inventory-product-alert": "*",
        "magento/module-inventory-requisition-list": "*",
        "magento/module-inventory-reservations": "*",
        "magento/module-inventory-reservations-api": "*",
        "magento/module-inventory-reservation-cli": "*",
        "magento/module-inventory-sales": "*",
        "magento/module-inventory-sales-admin-ui": "*",
        "magento/module-inventory-sales-api": "*",
        "magento/module-inventory-sales-frontend-ui": "*",
        "magento/module-inventory-setup-fixture-generator": "*",
        "magento/module-inventory-shipping": "*",
        "magento/module-inventory-shipping-admin-ui": "*",
        "magento/module-inventory-source-deduction-api": "*",
        "magento/module-inventory-source-selection": "*",
        "magento/module-inventory-source-selection-api": "*",
        "magento/module-inventory-visual-merchandiser": "*",
        "magento/module-inventory-swatches-frontend-ui": "*",
        "magento/module-inventory-quote-graph-ql": "*",
        "magento/module-inventory-in-store-pickup": "*",
        "magento/module-inventory-in-store-pickup-sales": "*",
        "magento/module-inventory-in-store-pickup-admin-ui": "*",
        "magento/module-inventory-in-store-pickup-sales-admin-ui": "*",
        "magento/module-inventory-in-store-pickup-api": "*",
        "magento/module-inventory-in-store-pickup-sales-api": "*",
        "magento/module-inventory-in-store-pickup-frontend": "*",
        "magento/module-inventory-in-store-pickup-shipping": "*",
        "magento/module-inventory-in-store-pickup-graph-ql": "*",
        "magento/module-inventory-in-store-pickup-shipping-admin-ui": "*",
        "magento/module-inventory-in-store-pickup-multishipping": "*",
        "magento/module-inventory-in-store-pickup-shipping-api": "*",
        "magento/module-inventory-in-store-pickup-quote": "*",
        "magento/module-inventory-in-store-pickup-webapi-extension": "*",
        "magento/module-inventory-in-store-pickup-quote-graph-ql": "*",
        "magento/module-inventory-configurable-product-frontend-ui": "*",
        "magento/module-inventory-catalog-search-configurable-product": "*",
        "magento/module-inventory-catalog-search-bundle-product": "*",
        "magento/module-inventory-catalog-frontend-ui": "*",
        "magento/module-inventory-bundle-import-export": "*",
        "magento/module-inventory-bundle-product-indexer": "*"
    }
```

完成此更改后，运行composer install，此时将自动删除这些Inventory management模块。

## 升级Inventory management

### 早期[!DNL Commerce]版本

将现有2.1.x、2.2.x或2.3.x安装升级或更新到Adobe Commerce或Magento Open Source 2.4.x时，[!DNL Inventory Management]模块默认处于禁用状态。 为了防止向后不兼容的升级并更好地支持Order Management (OMS)，使用此默认设置是一种预防措施。

>[!NOTE]
>
>Order Management不支持[!DNL Inventory Management]。 升级时，[!DNL Inventory Management]模块被禁用，以允许OMS和[!DNL Commerce] 2.3.x无缝工作。


要启用[!DNL Inventory Management]模块：

1. 编辑`<Commerce_installation_directory>/app/etc/config.php`文件。
1. 将所有清单模块从`0`修改为`1`以启用。
1. 更新数据库：

   ```bash
   bin/magento setup:upgrade
   ```

1. 清理缓存：

   ```bash
   bin/magento cache:clean
   ```

建议您在升级后使用[保留不一致命令](cli.md)。 升级时，您的所有产品都会添加到默认库存。 如果您有待定订单，则这些命令会正确更新您的可销售数量和预留，以便进行销售和订单履行。

### 早期[!DNL Inventory Management]版本

从以前版本的[!DNL Inventory Management]升级到最新版本时，请按照正常的扩展升级步骤操作。

对于最新版本，请更新您的中继包版本：

```json
        magento/inventory-composer-metapackage = 1.1.3
```

有关Commerce升级的更多信息，请参阅以下指南：

* [Commerce更新指南](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/overview.html){target="_blank"}
* [启用或禁用模块](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/manage-modules.html){target="_blank"}

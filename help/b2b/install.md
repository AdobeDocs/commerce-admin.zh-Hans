---
title: 安装 [!DNL Adobe Commerce B2B] 扩展
description: 了解如何安装 [!DNL Adobe Commerce B2B] 暗喻。
feature: B2B, Install
role: Admin, Developer
exl-id: a6947212-1708-40ae-9e81-874467eba5e1
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '873'
ht-degree: 0%

---


# 安装 [!DNL Adobe Commerce B2B] 扩展

Adobe Commerce B2B扩展仅适用于Adobe Commerce v2.2.0或更高版本。 它会在安装Adobe Commerce之后安装。

安装已部署的Adobe Commerce版本支持的最新版本的B2B扩展。

>[!NOTE]
>
>这些安装说明适用于内部部署的Adobe Commerce。 要为部署在云基础架构上的Commerce项目安装B2B扩展，请参阅 [《Commerce Cloud基础结构指南》](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure-store/b2b-module.html).

## 要求

- Adobe Commerce版本2.3.x或更高版本
- [支持的B2B扩展版本](https://experienceleague.adobe.com/docs/commerce-operations/release/product-availability.html#compatibility)
- 有效 [身份验证密钥](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html) 下载Adobe Commerce扩展。

  保存身份验证密钥以供安装，方法是在中全局定义它们 [COMPOSER_HOME](https://getcomposer.org/doc/03-cli.md#composer-home) 目录。 或者，将它们保存到 [auth.json](https://developer.adobe.com/commerce/contributor/guides/install/clone-repository/#authentication-file) 文件，该文件位于Adobe Commerce应用程序根目录中。

在安装或升级B2B扩展之前，请查看发行说明，以了解有关版本兼容性、更新或可能影响安装或升级要求的更改的最新信息。

- [B2B发行说明](release-notes.md)
- [Adobe Commerce发行说明](https://experienceleague.adobe.com/docs/commerce-operations/release/versions.html?lang=en)

## 安装步骤

1. 从Adobe Commerce应用程序根目录中，更新 `composer.json` 添加B2B扩展的依赖项：

   ```bash
   composer require magento/extension-b2b:<version>
   ```

   如果出现错误，例如：

   ```terminal
   [InvalidArgumentException] Could not find a matching version of package magento/extension-b2b.
   ```

   检查包的拼写、版本限制，以及包是否可用并符合最低稳定性（稳定）要求。

1. 如果出现提示，请输入 [身份验证密钥](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html).

   您的 _公钥_ 是您的用户名；您的 _私钥_ 是您的密码。 如果您已将公钥和私钥存储在 `auth.json`，则不会提示您进行身份验证。

1. 在Composer完成更新模块后运行以下命令：

   ```bash
   bin/magento setup:upgrade
   ```

   ```bash
   bin/magento setup:di:compile
   ```

   ```bash
   bin/magento setup:static-content:deploy -f
   ```

   ```bash
   bin/magento cache:clean
   ```

   >[!NOTE]
   >
   >在生产模式下，您可能会收到 `Please rerun Magento compile command`. 输入命令以完成安装。 Adobe Commerce不会提示您以开发人员模式运行编译命令。

完成安装后，配置并启动消息使用者，包括 [指定消息使用者的参数](#configure-message-consumers).

## 消息使用者

Adobe Commerce B2B扩展使用MySQL进行消息队列管理。 下表列出了支持B2B功能的消息使用者。 安装该扩展后，启动消息消费者，了解Commerce店面所需的B2B功能。

| 消费者 | 描述 |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sharedCatalogUpdatePrice` | 更新共享目录中每个产品的价格。 在以下情况下需要： [**[!UICONTROL Shared Catalogs]**](catalog-shared.md) 选项在管理员系统配置设置中启用。 |
| `sharedCatalogUpdateCategoryPermissions` | 更新分配给共享目录类别的类别。 在以下情况下需要： [**[!UICONTROL Shared Catalogs]**](catalog-shared.md) 选项在管理员系统配置设置中启用。 |
| `negotiableQuotePriceUpdate` | 更新可协商报价的价格。 在以下情况下需要： [**[!UICONTROL Quotes]**](quotes.md) 选项在管理员系统配置设置中启用。 |
| `purchaseorder.toorder` | 将采购订单转换为订单。 在以下情况下需要： [**[!UICONTROL Purchase Orders]**](purchase-order-flow.md) 选项在管理员系统配置设置中启用。 |
| `purchaseorder.transactional.email` | 发送采购订单电子邮件。 在以下情况下需要： [**[!UICONTROL Purchase Orders]**](purchase-order-flow.md) 选项在管理员系统配置设置中启用。 |
| `purchaseorder.validation` | 根据相关验证采购订单 [审批规则](account-dashboard-approval-rules.md). 在以下情况下需要： [**[!UICONTROL Purchase Orders]**](purchase-order-flow.md) 选项在管理员系统配置设置中启用。 |
| `quoteItemCleaner` | 从目录中删除或从购物车中删除产品时，删除无效或不活动的报价。 在以下情况下需要： [**[!UICONTROL Quotes]**](quotes.md) 选项在管理员系统配置设置中启用。 |
| `inventoryQtyCounter` | 在下达订单或移除产品后，异步更正股票指数。 在以下情况下需要： [**[!UICONTROL Use deferred stock update]**](../configuration-reference/catalog/inventory.md#product-stock-options) 选项会在管理员配置设置中启用Inventory management。 请参阅 [性能最佳实践](https://experienceleague.adobe.com/docs/commerce-operations/performance-best-practices/configuration.html#deferred-stock-update). |
| `async.operations.all` | 为的每项任务创建消息 [批量操作](https://developer.adobe.com/commerce/php/development/components/message-queues/bulk-operations/)，例如导入或导出物料、批量更改价格以及将产品分配给仓库。 在以下情况下需要： [**管理员批量操作**](../configuration-reference/catalog/inventory.md#admin-bulk-operations) 选项 [!DNL Inventory Management] 设置为 **异步运行** 在管理员系统配置设置中。 |

{style="table-layout:auto"}

>[!NOTE]
>
>有关所有Adobe Commerce消息使用者的列表，请参阅 [消息队列使用者](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/consumers.html) 在 _配置指南_.

### 配置消息使用者

在执行以下操作时，通过添加以下参数防止可能出现的处理问题或延迟 [启动消息使用者](#start-message-consumers) 用于B2B功能。

- `--max-messages <value>` — 指定终止前每个使用者必须处理的最大消息数(默认值= 10000)。 虽然我们不建议这样做，但可以使用0来阻止消费者终止。 PHP应用程序的最佳做法是重新启动长时间运行的进程，以防止可能的内存泄漏。

- `--batch-size <value>` — 允许您限制使用者使用的系统资源（CPU、内存）。 使用较小的批会减少资源用量，因此会导致处理速度变慢。  如果指定，队列中的消息将分批使用 `<value>` 每个。 此选项仅适用于批处理消费者。 如果 `--batch-size` 未定义，批处理使用者会接收队列中所有可用的消息。

有关其他配置选项的信息，请参见 [特定配置](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html#specific-configuration).

### 启动消息使用者

要为B2B功能启用异步操作，您必须启动多个消息使用者。

1. 列出可用的消息使用者：

   ```bash
   bin/magento queue:consumers:list
   ```

   该命令返回可用的消息使用者，包括 [B2B消息使用者](#message-consumers).

1. 分别启动每个消费者：

   ```bash
   bin/magento queue:consumers:start [--max-messages=<value>] [--batch-size=<value>] <consumer_name>
   ```

   例如：

   ```bash
   bin/magento queue:consumers:start quoteItemCleaner
   ```

>[!TIP]
>
>要在后台运行它，请附加 `&` 返回到命令提示符后，继续运行命令。 例如： `bin/magento queue:consumers:start sharedCatalogUpdatePrice &`.

有关更多信息，请参阅 [管理消息队列](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html) 在 _配置指南_.

### 将消息使用者添加到cron

您可以选择为以下项自动运行计划 `SharedCatalogUpdateCategoryPermissions` 和 `SharedCatalogUpdatePrice` 通过将计划添加到cron配置文件来使用消息 [/app/code/Magento/MessageQueue/etc/crontab.xml](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html#process-management).

```terminal
* * * * * ps ax | grep [s]haredCatalogUpdateCategoryPermissions >>/dev/null 2>&1 || nohup php /var/www/html/magento2/bin/magento queue:consumers:start sharedCatalogUpdateCategoryPermissions &
* * * * * ps ax | grep [s]haredCatalogUpdatePrice >>/dev/null 2>&1 || nohup php /var/www/html/magento2/bin/magento queue:consumers:start sharedCatalogUpdatePrice &
```

您还可以从以下位置为消息使用者配置计划 [存储配置设置](../systems/cron.md) 在“管理员”中。

## 在管理员中启用B2B功能

安装Adobe Commerce B2B扩展并启动消息使用者后，您还必须 [在管理员中启用B2B功能](enable-basic-features.md).

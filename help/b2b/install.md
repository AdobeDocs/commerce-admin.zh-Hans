---
title: 安装 [!DNL Adobe Commerce B2B] 扩展
description: 了解如何安装 [!DNL Adobe Commerce B2B] 中继包。
feature: B2B, Install
role: Admin, Developer
exl-id: a6947212-1708-40ae-9e81-874467eba5e1
source-git-commit: df3f01bb8e6dab61523d5cb7e0e430b61f87145b
workflow-type: tm+mt
source-wordcount: '1132'
ht-degree: 0%

---


# 安装[!DNL Adobe Commerce B2B]扩展

Adobe Commerce B2B扩展`magento/extension-b2b`适用于所有受支持的Adobe Commerce版本。 它会在安装Adobe Commerce之后安装。


## 要求

- [Adobe Commerce](https://business.adobe.com/products/magento/magento-commerce.html)，所有支持的版本
- PHP 8.1、8.2和8.3（需要B2B 1.5.0）
- [!DNL Composer]

>[!IMPORTANT]
>
>Adobe Commerce B2B版本1.4.2+与PHP 8.3不兼容。如果将Commerce实例升级到Commerce版本2.4.7+，请确保该实例上安装的PHP版本是PHP 8.2，以保持与B2B 1.4.2+的兼容性。

## 支持的平台

- 云基础架构上的Adobe Commerce (ECE)
- Adobe Commerce内部部署(EE)

## 安装步骤

>[!BEGINSHADEBOX]

**先决条件**

- 访问[repo.magento.com](https://repo.magento.com/)以下载扩展。 有关密钥生成和获取必要的权限，请参阅[获取您的身份验证密钥](https://experienceleague.adobe.com/en/docs/commerce-operations/installation-guide/prerequisites/authentication-keys)。

  通过在[COMPOSER_HOME](https://getcomposer.org/doc/03-cli.md#composer-home)目录中全局定义身份验证密钥来保存身份验证密钥以供安装。 或者，将它们保存到Adobe Commerce应用程序根目录中的[auth.json](https://developer.adobe.com/commerce/contributor/guides/install/clone-repository/#authentication-file)文件。

- [支持的B2B扩展版本](https://experienceleague.adobe.com/en/docs/commerce-operations/release/product-availability) — 确定部署的Adobe Commerce版本支持的B2B扩展的最新版本。

- 查看发行说明，了解有关版本兼容性、更新或可能影响安装或升级要求的更改的最新信息。

   - [B2B发行说明](release-notes.md)
   - [Adobe Commerce发行说明](https://experienceleague.adobe.com/en/docs/commerce-operations/release/versions)

>[!ENDSHADEBOX]

使用编辑器安装B2B扩展(`magento/b2b-extension`)。 该扩展是一个编辑器中继包，其中包含可为Adobe Commerce实例启用B2B功能的模块集合。 有关包含的模块的列表，请参阅[B2B包](packages.md)。

>[!BEGINTABS]

>[!TAB 云基础架构]

>[!TIP]
>
>在云基础架构上安装Adobe Commerce B2B时，Adobe建议您在开始之前将Adobe Commerce应用程序部署到集成或暂存环境。

将B2B扩展添加到项目时，Adobe建议在开发分支中工作。 如果没有分支，请参阅[创建用于开发的分支](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/cli-branches)。 安装B2B扩展时，`Magento_B2b`扩展名会自动插入`app/etc/config.php`文件中。 无需直接编辑文件。

**安装B2B扩展**：

1. 在本地工作站上，转到您的项目目录。

1. 创建或签出开发分支。

1. 将B2B扩展添加到`composer.json`文件的`require`部分。

   ```bash
   composer require magento/extension-b2b --no-update
   ```

1. 更新项目依赖关系。

   ```bash
   composer update
   ```

1. 添加、提交和推送代码更改。

   ```bash
   git add -A
   ```

   ```bash
   git commit -m "Install the B2B extension."
   ```

   ```bash
   git push origin <branch-name>
   ```

   >[!NOTE]
   >
   >将更新推送到云环境会启动Commerce云部署过程以应用更改。 从[部署日志](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/deploy/process)中检查部署状态。 如果遇到部署错误，请参阅[从组件故障中恢复](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/deploy/recover-failed-deployment)。

1. 构建和部署完成后，使用SSH登录到远程环境，并验证是否已安装和启用B2B扩展。

   ```bash
   bin/magento module:status Magento_B2b
   ```

   扩展名使用格式： `<VendorName>_<ComponentName>`。

   示例响应：

   ```
   Magento_B2b : Module is enabled
   ```

>[!TAB 内部部署]

1. 从Adobe Commerce应用程序根目录中，更新`composer.json`以添加B2B扩展的依赖项：

   ```bash
   composer require magento/extension-b2b:<version>
   ```

   如果出现错误，例如：

   ```
   [InvalidArgumentException] Could not find a matching version of package magento/extension-b2b.
   ```

   检查包的拼写、版本限制，以及包是否可用并符合最低稳定性（稳定）要求。

1. 如果出现提示，请输入您的[身份验证密钥](https://experienceleague.adobe.com/en/docs/commerce-operations/installation-guide/prerequisites/authentication-keys)。

   您的&#x200B;_公钥_&#x200B;是您的用户名；_私钥_&#x200B;是您的密码。 如果您已将公钥和私钥存储在`auth.json`中，则不会提示您进行身份验证。

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
   >在生产模式下，您可能会收到发送给`Please rerun Magento compile command`的消息。 输入命令以完成安装。 Adobe Commerce不会提示您以开发人员模式运行编译命令。

>[!ENDTABS]

完成安装后，配置并启动消息使用者。

## 消息使用者

Adobe Commerce B2B扩展使用MySQL进行消息队列管理。 下表列出了支持B2B功能的消息使用者。 安装该扩展后，启动消息消费者，了解Commerce店面所需的B2B功能。

| 消费者 | 描述 |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sharedCatalogUpdatePrice` | 更新共享目录中每个产品的价格。 在管理系统配置设置中启用[**[!UICONTROL Shared Catalogs]**](catalog-shared.md)选项时必需。 |
| `sharedCatalogUpdateCategoryPermissions` | 更新分配给共享目录类别的类别。 在管理系统配置设置中启用[**[!UICONTROL Shared Catalogs]**](catalog-shared.md)选项时必需。 |
| `negotiableQuotePriceUpdate` | 更新可协商报价的价格。 在管理系统配置设置中启用[**[!UICONTROL Quotes]**](quotes.md)选项时必需。 |
| `purchaseorder.toorder` | 将采购订单转换为订单。 在管理系统配置设置中启用[**[!UICONTROL Purchase Orders]**](purchase-order-flow.md)选项时必需。 |
| `purchaseorder.transactional.email` | 发送采购订单电子邮件。 在管理系统配置设置中启用[**[!UICONTROL Purchase Orders]**](purchase-order-flow.md)选项时必需。 |
| `purchaseorder.validation` | 根据相关[审批规则](account-dashboard-approval-rules.md)验证采购订单。 在管理系统配置设置中启用[**[!UICONTROL Purchase Orders]**](purchase-order-flow.md)选项时必需。 |
| `quoteItemCleaner` | 从目录中删除或从购物车中删除产品时，删除无效或不活动的报价。 在管理系统配置设置中启用[**[!UICONTROL Quotes]**](quotes.md)选项时必需。 |
| `inventoryQtyCounter` | 在下达订单或移除产品后，异步更正股票指数。 在管理员配置设置中为Inventory management启用[**[!UICONTROL Use deferred stock update]**](../configuration-reference/catalog/inventory.md#product-stock-options)选项时必需。 请参阅[性能最佳实践](https://experienceleague.adobe.com/en/docs/commerce-operations/performance-best-practices/configuration#deferred-stock-update)。 |
| `async.operations.all` | 为[批量操作](https://developer.adobe.com/commerce/php/development/components/message-queues/bulk-operations/)的每个单独任务创建消息，例如导入或导出物料、批量更改价格以及将产品分配给仓库。 当[!DNL Inventory Management]的&#x200B;[**管理员批量操作**](../configuration-reference/catalog/inventory.md#admin-bulk-operations)&#x200B;选项在管理员系统配置设置中设置为&#x200B;**异步运行**&#x200B;时需要。 |

{style="table-layout:auto"}

>[!NOTE]
>
>有关所有Adobe Commerce消息使用者的列表，请参阅&#x200B;_配置指南_&#x200B;中的[消息队列使用者](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/message-queues/consumers)。

### 配置消息使用者

在针对B2B功能[启动消息使用者](#start-message-consumers)时，通过添加以下参数防止可能的处理问题或延迟。

- `--max-messages <value>` — 指定每个使用者在终止前必须处理的最大消息数(默认值= 10000)。 虽然Adobe不建议这样做，但您可以使用0来阻止使用者终止。 PHP应用程序的最佳做法是重新启动长时间运行的进程，以防止可能的内存泄漏。

- `--batch-size <value>` — 允许您限制使用者使用的系统资源(CPU、内存)。 使用较小的批会减少资源用量，因此会导致处理速度变慢。  如果指定，则队列中的消息将以`<value>`批次（每批）使用。 此选项仅适用于批处理消费者。 如果未定义`--batch-size`，则批处理使用者将接收队列中的所有可用消息。

有关其他配置选项的信息，请参阅[特定配置](https://experienceleague.adobe.com//en/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues#specific-configuration)。

### 启动消息使用者

要为B2B功能启用异步操作，您必须启动多个消息使用者。

1. 列出可用的消息使用者：

   ```bash
   bin/magento queue:consumers:list
   ```

   该命令返回可用的消息使用者，包括所有[B2B消息使用者](#message-consumers)。

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
>若要在后台运行它，请将`&`附加到命令，返回到提示符，然后继续运行命令。 例如： `bin/magento queue:consumers:start sharedCatalogUpdatePrice &`。

有关详细信息，请参阅&#x200B;_配置指南_&#x200B;中的[管理消息队列](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues)。

### 将消息使用者添加到cron

通过将计划添加到cron配置文件[/app/code/Magento/MessageQueue/etc/crontab.xml](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues#process-management)，可以自动执行`SharedCatalogUpdateCategoryPermissions`和`SharedCatalogUpdatePrice`消息使用者的运行计划。

```
* * * * * ps ax | grep [s]haredCatalogUpdateCategoryPermissions >>/dev/null 2>&1 || nohup php /var/www/html/magento2/bin/magento queue:consumers:start sharedCatalogUpdateCategoryPermissions &
* * * * * ps ax | grep [s]haredCatalogUpdatePrice >>/dev/null 2>&1 || nohup php /var/www/html/magento2/bin/magento queue:consumers:start sharedCatalogUpdatePrice &
```

您还可以从“管理员”中的[存储配置设置](../systems/cron.md)为消息使用者配置计划。

## 在管理员中启用B2B功能

安装Adobe Commerce B2B扩展并启动邮件使用者后，您还必须[在管理员中启用B2B功能](enable-basic-features.md)。


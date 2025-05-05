---
title: '[!DNL Inventory Management] CLI引用'
description: 了解 [!DNL Inventory Management] 模块提供的用于管理清单数据和配置设置的命令。
exl-id: d92dffce-94a1-443c-8c72-98fecbbd5320
level: Experienced
feature: Inventory, Configuration
badgePaas: label="仅限PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="仅适用于云项目(Adobe管理的PaaS基础架构)和内部部署项目上的Adobe Commerce 。"
source-git-commit: b4623ada788d44f4628930dcf5dfcb51dd88ee3a
workflow-type: tm+mt
source-wordcount: '843'
ht-degree: 0%

---

# [!DNL Inventory Management] CLI引用

[!DNL Inventory Management]提供管理清单数据和配置设置的命令。

这些命令包括：

- 检查和解决影响可销售数量的预订不一致问题
- 为距离优先级算法添加地理代码

## 解决预留不一致

预留对每种库存的产品SKU设置了可销售数量暂挂。 在您发运、添加产品、取消或退款订单时，报酬保留将输入以放置或清除这些暂挂。

[!DNL Inventory Management]提供了两个命令来检查和解决保留不一致：

- [&#39;库存:reservation:列表不一致&#39;](#list-inconsistencies-command)
- [&#39;库存:reservation:创建补偿&#39;](#create-compensations-command)

### 保留不一致的原因

[!DNL Inventory Management]为关键事件生成预留：

- 订单安排（初始预订）
- 订单装运（补偿预留）
- 退款单或发放贷项通知单（报酬预留）
- 订单取消（补偿预留）

在以下情况下，可能会出现保留不一致：

- [!DNL Inventory Management]丢失初始预订并输入过多预订补偿（补偿过重并导致数量不一致）
- [!DNL Inventory Management]正确放置了初始预订，但丢失了补偿预订。

您可以在`inventory_reservation`表中手动查看和检查预留。

以下配置和事件可能会导致预订不一致：

- **升级至2.3.x，订单未处于最终状态（“完成”、“已取消”或“已关闭”）。** [!DNL Inventory Management]为这些订单创建补偿预留，但它没有输入或从可销售数量中扣除的初始预留。 建议在从2.1.x或2.2.x升级到Adobe Commerce或Magento Open Source v2.3.x后使用这些命令。 如果您有待定订单，则这些命令会正确更新您的可销售数量和预留，以便进行销售和订单履行。
- **您不管理Stock，稍后再更改此配置。**&#x200B;您可以在配置中将&#x200B;**[!UICONTROL Manage Stock]**&#x200B;设置为`No`的情况下开始使用2.3.x。 [!DNL Commerce]未在订单下单和装运事件中预订。 如果您稍后启用&#x200B;**[!UICONTROL Manage Stock]**&#x200B;配置并创建了某些订单，则当您处理并履行该订单时，可销售数量将会因补偿预留而损坏。
- **在订单提交到某个网站时，您重新分配该网站的Stock**。 初始预留将输入初始库存，所有报酬预留将输入新库存。
- **所有保留的总数不能解析为`0`。**&#x200B;处于最终状态（完成、已取消、已关闭）的订单范围内的所有保留应解析为`0`，正在清除所有可销售数量暂挂。

### 列出不一致命令

`list-inconsistencies`命令检测并列出所有保留不一致。 使用命令选项仅检查已完成或不完整的订单，或检查所有订单。

```bash
bin/magento inventory:reservation:list-inconsistencies
```

命令选项：

- `-c`，`--complete-orders` — 返回已完成订单的不一致情况。 已完成的订单可能仍保留不正确的预留。
- `-i`，`--incomplete-orders` — 未完成订单（部分发运，未发运）的退货不一致。 不正确的保留可能会保留过多或不足的订单可销售数量。
- `-b`，`--bunch-size` — 定义一次加载的订单数。
- `-r`，`--raw` — 原始输出。

使用`-r`的响应以`<ORDER_INCREMENT_ID>:<SKU>:<QUANTITY>:<STOCK-ID>`格式返回：

- 订单ID指示不一致的范围。
- SKU指示具有不一致的产品。
- 数量设置要为预留补偿输入的金额。
- 库存ID定义为库存的范围，它使用预留来计算可销售数量。

示例：

```bash
bin/magento inventory:reservation:list-inconsistencies

Inconsistencies found on following entries:
Order 172:
- Product bike-123 should be compensated by +2.000000 for stock 1
```

```bash
bin/magento inventory:reservation:list-inconsistencies -r

172:bike-123:+2.000000:1
```

如果未发现任何问题，则会返回以下消息：未找到任何订单不一致。

### 创建补偿命令

`create-compensations`命令创建薪酬预留。 根据问题而定，系统将创建新保留以放置或释放对可销售数量的暂挂。

要创建保留，请使用格式`<ORDER_INCREMENT_ID>:<SKU>:<QUANTITY>:<STOCK-ID>`提供补偿，如`172:bike-123:+2.000000:1`。

```bash
bin/magento inventory:reservation:create-compensations
```

命令选项：

- `-r`，`--raw` — 返回原始输出。

如果请求的格式不正确，则会显示以下消息：

```
Error while parsing argument "your_incorrect_format_argument". Given argument does not match pattern "/(?P<increment_id>.*):(?P<sku>.*):(?P<quantity>.*):(?P<stock_id>.*)/".
```

当该命令创建预留时，它会显示指示SKU、订单和库存更新的消息。

```bash
bin/magento inventory:reservation:create-compensations 172:bike-123:+2.000000:1

Following reservations were created:
- Product bike-123 was compensated by +2.000000 for stock 1
```

如果报酬条目的SKU包含空格，请用引号将SKU括起来。

```bash
bin/magento inventory:reservation:create-compensations 172:"bike 123":+2.000000:1
```

### 检测不一致并创建补偿

您可以使用管道同时运行`list-inconsistencies`和`create-compensations`来检测不一致并立即创建补偿。 使用`-r`命令选项生成原始数据并将其提交到`create-compensations`。

```bash
bin/magento inventory:reservation:list-inconsistencies -r | bin/magento inventory:reservation:create-compensations
```

示例响应：

```bash
bin/magento inventory:reservation:list-inconsistencies -r | bin/magento inventory:reservation:create-compensations
```

```
Following reservations were created:
- Product bike-123 was compensated by +2.000000 for stock 1
- Product bikehat-456 was compensated by +1.000000 for stock 1
```

更新完成后，运行list命令以验证：

```bash
bin/magento inventory:reservation:list-inconsistencies -r
```

```
No order inconsistencies were found.
```

您还可以发送命令以检测不一致情况，并为不完整(`-i`)或完整(`-c`)订单创建补偿。

```bash
bin/magento inventory:reservation:list-inconsistencies -r -i | bin/magento inventory:reservation:create-compensations
```

```bash
bin/magento inventory:reservation:list-inconsistencies -r -c | bin/magento inventory:reservation:create-compensations
```

## 导入地理代码

[!DNL Inventory Management]提供了[距离优先级算法](distance-priority-algorithm.md)，这有助于确定发送完整订单或部分订单的最佳选项。 该算法使用GPS信息或地理代码计算订单中每个物料的来源（仓库或其他物理位置）与发运地址之间的距离。 根据这些结果，算法建议使用哪个来源按顺序发运每个项目。

商家会选择计算距离所需的GPS或地理代码数据提供商：

- **Google MAP**&#x200B;使用[Google Map Platform](https://mapsplatform.google.com/)服务计算送货目标地址与源位置之间的距离和时间。 此选项需要Google计费计划，并且可能会通过Google产生费用。

- **离线计算**&#x200B;使用从[geonames.org](https://www.geonames.org/)下载并通过命令导入到Commerce中的数据计算距离。 此选项是免费的。

要导入用于离线计算的地理代码，请执行以下操作：

输入以下命令，该命令带有以空格分隔的[ISO-3166 alpha2国家/地区代码](https://www.geonames.org/countries/)列表：

```bash
bin/magento inventory-geonames:import <country code> <country code> ...
```

例如：

```bash
bin/magento inventory-geonames:import us ca gb de
```

系统下载地理编码数据并将其导入数据库，然后显示消息`Importing <country code>: OK`。

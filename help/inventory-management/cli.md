---
title: ’[!DNL Inventory Management] CLI参考
description: 了解提供的命令 [!DNL Inventory Management] 用于管理清单数据和配置设置的模块。
exl-id: d92dffce-94a1-443c-8c72-98fecbbd5320
level: Experienced
feature: Inventory, Configuration
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '830'
ht-degree: 0%

---

# [!DNL Inventory Management] CLI参考

[!DNL Inventory Management] 提供了管理清单数据和配置设置的命令。

这些命令包括：

- 检查和解决影响可销售数量的预订不一致问题
- 为距离优先级算法添加地理代码

## 解决预留不一致

预留对每种库存的产品SKU设置了可销售数量暂挂。 在您发运、添加产品、取消或退款订单时，报酬保留将输入以放置或清除这些暂挂。

[!DNL Inventory Management] 提供了两个命令来检查和解决保留不一致问题：

- [&#39;库存:reservation:列表不一致](#list-inconsistencies-command)
- [&#39;库存:reservation:create-compensations&#39;](#create-compensations-command)

### 保留不一致的原因

[!DNL Inventory Management] 生成关键事件的预留：

- 订单安排（初始预订）
- 订单装运（补偿预留）
- 退款单或发放贷项通知单（报酬预留）
- 订单取消（补偿预留）

在以下情况下，可能会出现保留不一致：

- [!DNL Inventory Management] 会丢失初始预订，并输入过多的预订补偿（补偿过度，从而导致数量不一致）
- [!DNL Inventory Management] 正确放置初始预订，但丢失补偿预订。

您可以在中人工复查和检查预留 `inventory_reservation` 表格。

以下配置和事件可能会导致预订不一致：

- **升级到2.3.x，其中订单未处于最终状态（“完成”、“已取消”或“已关闭”）。** [!DNL Inventory Management] 创建这些订单的补偿保留，但是它不会输入或从可销售数量中扣除的初始保留。 建议在从2.1.x或2.2.x升级到Adobe Commerce或Magento Open Source v2.3.x后使用这些命令。 如果您有待定订单，则这些命令会正确更新您的可销售数量和预留，以便进行销售和订单履行。
- **您不管理Stock，稍后再更改此配置。** 您可以开始将2.3.x与 **[!UICONTROL Manage Stock]** 设置为 `No` 在配置中。 [!DNL Commerce] 不会在订单下达和发运事件中预订。 如果您稍后启用 **[!UICONTROL Manage Stock]** 创建配置和某些订单后，当您处理并履行该订单时，可销售数量将会受到补偿预留的损坏。
- **您可以在订单提交至某个网站时重新分配该网站的Stock**. 初始预留将输入初始库存，所有报酬预留将输入新库存。
- **所有保留的总数不能解析为 `0`.** 处于最终状态（“完成”、“已取消”、“已关闭”）的订单范围内的所有保留应解析为 `0`，清除所有可销售数量暂挂。

### 列出不一致命令

此 `list-inconsistencies` 命令检测并列出所有保留不一致。 使用命令选项仅检查已完成或不完整的订单，或检查所有订单。

```bash
bin/magento inventory:reservation:list-inconsistencies
```

命令选项：

- `-c`， `--complete-orders`  — 返回已完成订单的不一致情况。 已完成的订单可能仍保留不正确的预留。
- `-i`， `--incomplete-orders`  — 返回未完成订单（部分发运、未发运）的不一致情况。 不正确的保留可能会保留过多或不足的订单可销售数量。
- `-b`， `--bunch-size`  — 定义一次加载的订单数。
- `-r`， `--raw`  — 原始输出。

响应使用 `-r` 返回位置 `<ORDER_INCREMENT_ID>:<SKU>:<QUANTITY>:<STOCK-ID>` 格式：

- 订单ID指示不一致的范围。
- SKU指示具有不一致的产品。
- 数量设置要为预留补偿输入的金额。
- 库存ID定义为库存的范围，它使用预留来计算可销售数量。

示例:

```terminal
bin/magento inventory:reservation:list-inconsistencies

Inconsistencies found on following entries:
Order 172:
- Product bike-123 should be compensated by +2.000000 for stock 1
```

```terminal
bin/magento inventory:reservation:list-inconsistencies -r

172:bike-123:+2.000000:1
```

如果未发现任何问题，则会返回以下消息：未找到任何订单不一致。

### 创建补偿命令

此 `create-compensations` 命令创建薪酬预留。 根据问题而定，系统将创建新保留以放置或释放对可销售数量的暂挂。

要创建保留，请使用格式提供补偿 `<ORDER_INCREMENT_ID>:<SKU>:<QUANTITY>:<STOCK-ID>` 例如 `172:bike-123:+2.000000:1`.

```bash
bin/magento inventory:reservation:create-compensations
```

命令选项：

- `-r`， `--raw`  — 返回原始输出。

如果请求的格式不正确，则会显示以下消息：

```terminal
Error while parsing argument "your_incorrect_format_argument". Given argument does not match pattern "/(?P<increment_id>.*):(?P<sku>.*):(?P<quantity>.*):(?P<stock_id>.*)/".
```

当该命令创建预留时，它会显示指示SKU、订单和库存更新的消息。

```terminal
bin/magento inventory:reservation:create-compensations 172:bike-123:+2.000000:1

Following reservations were created:
- Product bike-123 was compensated by +2.000000 for stock 1
```

如果报酬条目的SKU包含空格，请用引号将SKU括起来。

```bash
bin/magento inventory:reservation:create-compensations 172:"bike 123":+2.000000:1
```

### 检测不一致并创建补偿

您可以使用管道同时运行和，以检测不一致并立即创建补偿。 `list-inconsistencies` 和 `create-compensations`. 使用 `-r` 命令选项，用于生成原始数据并将其提交到 `create-compensations`.

```bash
bin/magento inventory:reservation:list-inconsistencies -r | bin/magento inventory:reservation:create-compensations
```

示例响应：

```bash
bin/magento inventory:reservation:list-inconsistencies -r | bin/magento inventory:reservation:create-compensations
```

```terminal
Following reservations were created:
- Product bike-123 was compensated by +2.000000 for stock 1
- Product bikehat-456 was compensated by +1.000000 for stock 1
```

更新完成后，运行list命令以验证：

```bash
bin/magento inventory:reservation:list-inconsistencies -r
```

```terminal
No order inconsistencies were found.
```

也可以通过传送命令来检测不一致情况，并只为不完整情况创建补偿(`-i`)或完成(`-c`)个订单。

```bash
bin/magento inventory:reservation:list-inconsistencies -r -i | bin/magento inventory:reservation:create-compensations
```

```bash
bin/magento inventory:reservation:list-inconsistencies -r -c | bin/magento inventory:reservation:create-compensations
```

## 导入地理代码

[!DNL Inventory Management] 提供 [距离优先级算法](distance-priority-algorithm.md)，这有助于确定完整或部分订单交付的最佳选项。 该算法使用GPS信息或地理代码计算订单中每个物料的来源（仓库或其他物理位置）与发运地址之间的距离。 根据这些结果，算法建议使用哪个来源按顺序发运每个项目。

商家会选择计算距离所需的GPS或地理代码数据提供商：

- **GOOGLE MAP** 用途 [Google Maps平台](https://mapsplatform.google.com/) 服务，用于计算送货目标地址与来源位置之间的距离和时间。 此选项需要Google计费计划，并且可能会通过Google产生费用。

- **离线计算** 使用从以下位置下载的数据计算距离 [geonames.org](https://www.geonames.org/) 并使用命令导入到Commerce中。 此选项是免费的。

要导入用于离线计算的地理代码，请执行以下操作：

输入以下命令，其中以空格分隔的列表为 [ISO-3166 alpha2国家/地区代码](https://www.geonames.org/countries/)：

```bash
bin/magento inventory-geonames:import <country code> <country code> ...
```

例如：

```bash
bin/magento inventory-geonames:import us ca gb de
```

系统会下载地理编码数据并将其导入数据库，然后显示消息  `Importing <country code>: OK`.

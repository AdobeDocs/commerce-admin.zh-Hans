---
title: 管理库存源
description: 了解来源以及它们如何定义管理和发运产品库存以进行订单履行或提供服务的物理位置。
exl-id: 1315a8c9-7791-4c4b-9463-3126b79793c2
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '688'
ht-degree: 0%

---

# 管理源

来源是管理和发运产品库存以进行订单履行或提供服务的实际地点。 这些地点可包括仓库、实体店、配送中心、取货地点和卸货托运人。 将库存数量分配给这些来源，并且 [!DNL Commerce] 自动汇总库存的可销售产品总数。 对于大型公司，请为所有位置添加多个来源：在按国家/地区和大陆划分的不同地理位置，根据库存类型（甚至根据服务）划分的城市中的位置。

建议您在创建源时提供特定的物理地理位置。 这允许 _距离优先级算法_ 比较发运目的地地址的地点与可用的来源地点，以确定完成发运的最接近的来源。 您可以使用Google地图或使用地理代码的离线计算。 有关此内容的更多信息 _距离优先级算法_，请参见 [配置距离优先级算法](distance-priority-algorithm.md).

开始于 _默认源_ 您可以更新但不能禁用。 此源由单一源商家用于产品迁移。 您始终需要默认源。

- **位置信息**  — 每个来源均包括名称、国家/地区、地点的实际地址和联系点。
- **启用资源**  — 您可以根据需要启用和禁用源。 仅当来源接受并履行订单和延交订单时才启用它。
- **可用库存**  — 通过产品页分配和更新每个来源的库存数量。 库存数量通过来源和库存映射进行计算、提供和预留。

下图可帮助说明销售山地自行车的自行车商店商人的来源，山地自行车可供库存使用，并且可供销售局发货使用。

![示例源图表](assets/diagram-sources.png){width="600" zoomable="yes"}

所有存储都以必须保持启用状态的默认源开始：

- 所有新产品导入到 [!DNL Commerce] 需要源和库存，自动分配以便立即访问 [!DNL Inventory Management].
- 单一来源商家使用默认来源作为其库存地点和发运的单一地点。

## 编辑源

您可以更新姓名、地址、GPS位置和联系点信息。 源代码是一个受保护的值，充当将源代码与您的产品数量和库存关联的唯一ID。

如果编辑“默认源”，则可以编辑所有配置，但名称和代码除外。 建议单个来源商家添加与其位置匹配的信息。

此 _[!UICONTROL Manage Sources]_页面列出了所有可用的库存库位和履行设施。 您可以添加新的清单来源并编辑现有位置。

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Inventory]_>**[!UICONTROL Sources]**.

1. 要添加库存库位，请参阅 [添加新源](sources-add.md).

1. 查找库存来源并在中将其打开 _编辑_ 模式。

1. 更新信息并保存更改。

   ![管理源](assets/inventory-sources.png){width="600" zoomable="yes"}

## 按钮栏

| 按钮 | 描述 |
|--|--|
| [!UICONTROL Add New Source] | 打开“新建来源”表单，该表单用于输入新的库存来源、履行地点或地点。 |

## 管理源列说明

| 列 | 描述 |
|--|--|
| [!UICONTROL Code] | 系统用于标识库存来源的唯一字母数字代码。 |
| [!UICONTROL Name] | 标识管理员用户的清单来源的唯一名称。 |
| [!UICONTROL Is Enabled] | 指示库存来源是否有效并可使用。 |
| [!UICONTROL Pickup Location] | 指示来源是否作为的取车地点处于活动状态 [店内投放](../stores-purchase/shipping-in-store-delivery.md). |
| [!UICONTROL Action] | 点击 **[!UICONTROL Edit]** 在编辑模式下打开库存来源记录。 |

## 其他列

| 列 | 描述 |
|--- |--- |
| [!UICONTROL Latitude] | 指定GPS库存源的纬度坐标。 输入数字形式的值，并根据需要加号或减号加号。 不允许使用度符号和字母。 例如： `32.7555` |
| [!UICONTROL State/Province] | 源所在的省/市/自治区。 |
| [!UICONTROL Postcode] | 源的邮政编码。 |
| [!UICONTROL Email] | 主要联系人的电子邮件。 |
| [!UICONTROL Longitude] | 指定GPS库存源的经度坐标。 输入数字形式的值，并根据需要加号或减号加号。 不允许使用度符号和字母。 例如：经度–97.3308 |
| [!UICONTROL City] | 源所在的城市。 |
| [!UICONTROL Phone] | 主要联系人的电话号码。 |
| [!UICONTROL Country] | 源所在的国家/地区。 |
| [!UICONTROL Street] | 源的街道地址。 |
| [!UICONTROL Fax] | 主要联系人的区号和传真号。 |

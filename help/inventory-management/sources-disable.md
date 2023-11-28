---
title: 禁用库存来源
description: 了解如何禁用来源并修改信息，包括位置和联系点。
exl-id: 3fcbfa3c-8bb7-4e08-a395-9760bbd69f04
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '402'
ht-degree: 0%

---

# 禁用源

要确保所有订单数据都保留在 [!DNL Commerce]，无法删除源。 来源、订单和发运彼此直接相连。 您可以禁用源并修改信息，包括位置和联系点。

根据位置的状态，您可能需要禁用源。 禁用的来源会保留每个库存和产品的所有分配，但库存和订单不会访问它们。

禁用源时：

- [!DNL Inventory Management] 忽略并且不列出发运或订单处理的来源。
- 库存不会从来源访问汇总库存总计的库存数量。
- 不能将订单发运分配给禁用的地点。

不能禁用“默认源”。 [!DNL Commerce] 将此源用于所有新导入的产品、捆绑产品以及第三方系统支持。 您可以随时启用或禁用自定义源。

将源设置为 `disabled` 对于以下情况很有帮助：

- 添加商店或仓库 — 打开新商店或使新仓库和装运地点联机时，添加来源条目以使用导入设置产品库存，并连接到潜在库存。
- 季节性发货 — 假日是一年中的繁忙时段。 您可能希望限制仅从特定装运地点（如仓库）发运，以保持实体地点充足并专注于当地购物者。 或者，您可以在有限的时间内添加新的发货地点，以处理较高的销售和传入订单率。
- 关闭地点 — 在关闭地点以便移至新设施或永久关闭地点时，请禁用以停止该地点的新发运。

## 禁用一个或多个自定义源

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Inventory]_>**[!UICONTROL Sources]**.

1. 选中要禁用的每个已启用的自定义源的复选框。

1. 单击 _操作_ 菜单，然后选择 **[!UICONTROL Disable]**.

   ![[!DNL Inventory Management] 源 — “操作”菜单](assets/inventory-source-disable.png){width="600" zoomable="yes"}

1. 在确认对话框中，单击 **[!UICONTROL OK]**.

## 启用或禁用单个自定义源

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Inventory]_>**[!UICONTROL Sources]**.

1. 找到自定义源，然后单击 **[!UICONTROL Edit]**.

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 _常规_ 部分和更改 **[!UICONTROL Is Enabled]**：

   | 选项 | 描述 |
   | ----- | ----- |
   | `Yes` | 已启用源。 数量将添加到可销售数量。 发运订单时，来源将列出当前数量。 源选择算法会检查其送货源。 |
   | `No` | 源已禁用。 数量不会添加至可销售数量。 装运订单时源不列出。 配送选项跳过此来源。 |

1. 单击 **[!UICONTROL Save and Close]**.

---
title: 将库存转移到来源
description: 了解多来源商家如何将产品库存从一个来源地点转移到另一个来源地点。
exl-id: 30438412-bc93-4e65-8b6a-5ddb50afa7ff
feature: Inventory, Configuration
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 0%

---

# 将库存转移到来源

根据业务需求和地点的状态，多来源商家经常将产品库存从一个来源地点转移到另一个来源地点。 例如，您可能要关闭某个仓库库位，或不再从某个库位发运特定产品，并将这些产品的所有工序移至新库位。

此选项允许您选择一个或多个产品、要转移库存的原始来源以及要接收数量的目标来源：

- 按产品移动库存数量、来源物料状态（有库存/无库存）以及选定来源的“通知数量”。

- 如果产品没有该来源，则会跳过该来源。

- 将移动源的所有产品库存。 不能转移部分数量。

>[!NOTE]
>
>如果来源和目标来源具有不同的库存，则它会影响累计的可销售数量和进行中订单的保留。

在转移库存数量时，您也可以取消分配来源。

{{$include /help/_includes/unassign-source.md}}

![将库存转移到另一个来源](assets/inventory-bulk-transfer-source.gif)

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. 选择要修改其源的产品。

   浏览或搜索以查找产品，并选中要转移的复选框。

1. 单击 **[!UICONTROL Actions]** 菜单，然后选择 **[!UICONTROL Transfer Inventory to Source]**.

1. 单击 **[!UICONTROL OK]** 在确认对话框中。

1. 要将产品转移到新目标，请选择来源(_[!UICONTROL from]_)源。

1. 要将产品传输到新目标，请选择目标(_[!UICONTROL to]_)源。

1. 要从产品中删除源，请选中可选复选框 **[!UICONTROL Unassign from origin source after transfer]**.

   ![选择要转移的来源和目标](assets/inventory-bulk-transfer-summary.png){width="600" zoomable="yes"}

1. 单击 **[!UICONTROL Transfer Inventory]**.

   所有产品数量均从来源来源来源中扣除，并添加到目标来源中。 数量和可销售数量会自动更新。

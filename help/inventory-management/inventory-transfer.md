---
title: 将库存转移到来源
description: 了解多来源商家如何将产品库存从一个来源地点转移到另一个来源地点。
exl-id: 30438412-bc93-4e65-8b6a-5ddb50afa7ff
feature: Inventory, Configuration
TQID: https://experienceleague.adobe.com/HV6GQjHa88xgcSAi-LXhyqe7k2QW95VzQ8eG2mGlJ8I
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 282
ht-degree: 0%

---

# 将库存转移到来源

根据业务需求和地点的状态，多来源商家经常将产品库存从一个来源地点转移到另一个来源地点。 例如，您可能要关闭某个仓库库位，或不再从某个库位发运特定产品，并将这些产品的所有工序移至新库位。

此选项允许您选择一个或多个产品、要转移库存的原始来源以及要接收数量的目标来源：

- 按产品移动库存数量、Source物料状态（有库存/无库存）以及选定来源的“通知数量”。

- 如果产品没有该来源，则会跳过该来源。

- 将移动源的所有产品库存。 不能转移部分数量。

>[!NOTE]
>
>如果来源和目标来源具有不同的库存，则它会影响累计的可销售数量和进行中订单的保留。

在转移库存数量时，您也可以取消分配来源。

{{$include /help/_includes/unassign-source.md}}

![将库存转移到其他源](assets/inventory-bulk-transfer-source.gif)

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Catalog]** > **[!UICONTROL Products]**。

1. 选择要修改其源的产品。

   浏览或搜索以查找产品，并选中要转移的复选框。

1. 单击顶部的&#x200B;**[!UICONTROL Actions]**&#x200B;菜单，然后选择&#x200B;**[!UICONTROL Transfer Inventory to Source]**。

1. 在确认对话框中，单击&#x200B;**[!UICONTROL OK]**。

1. 要将产品转移到新目标，请选择来源(_[!UICONTROL from]_)源。

1. 要将产品传输到新目标，请选择目标(_[!UICONTROL to]_)源。

1. 要从产品中删除源，请选中可选复选框&#x200B;**[!UICONTROL Unassign from origin source after transfer]**。

   ![选择要转移的来源和目标](assets/inventory-bulk-transfer-summary.png){width="600" zoomable="yes"}

1. 单击&#x200B;**[!UICONTROL Transfer Inventory]**。

   所有产品数量均从来源来源来源中扣除，并添加到目标来源中。 数量和可销售数量会自动更新。

<!-- Last updated from includes: 2022-08-30 15:36:09 -->

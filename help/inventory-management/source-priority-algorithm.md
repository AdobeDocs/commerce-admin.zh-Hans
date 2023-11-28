---
title: 配置源优先级算法
description: 了解如何配置用于库存中分配来源顺序的源优先级以提出建议。
exl-id: 7b25212d-0cd0-4280-be23-c67f06db900a
feature: Inventory, Shipping/Delivery
source-git-commit: 023716935a6657b0dc2317876debe608e65bf010
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 0%

---

# 配置源优先级算法

自定义库存包括指定的来源列表，这些来源通过您的店面销售和发运可用的产品库存。 此算法使用库存中的已分配源顺序进行推荐。

运行时，算法将：

- 从顶部开始按照库存级别的已配置来源顺序工作

- 根据列表中的订单、可用数量和订购数量，建议每个产品的发运数量和来源

- 在订单装运完成之前继续沿列表向下移动

- 如果在列表中找到已禁用的源，则跳过该源

要配置，请按照从上到下的优先级排列这些来源以完成订单。 来源选择算法(SSA)在确定发运和库存扣减额时使用此订单提供算法“优先级”。 请参阅 [设置库存来源的优先级](stocks-prioritize-sources.md).

## 配置源的优先级

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > **[!UICONTROL Inventory]** > **[!UICONTROL Stocks]**.

1. 在编辑模式下打开股票并导航到 _[!UICONTROL Sources]_区域。

1. 单击 **[!UICONTROL Assign Sources]**.

1. 在 _[!UICONTROL Assign Sources]_视图，选中所需源的复选框，然后单击&#x200B;**[!UICONTROL Done]**为库存分配来源。

>[!NOTE]
>
>使用时 [距离优先级](distance-priority-algorithm.md) 如果路由和数据没有针对所选路由返回，则使用配送算法 [计算模式](distance-priority-algorithm.md) （驾驶、骑车或行走）对于发运，SSA默认使用“来源优先级”。

![优先级排序后的源顺序](assets/inventory-stock-priority-after.png)

| 图标 | 描述 |
|----------------------------------------------|----------------------------------------------------------------|
| ![拖放图标以设置优先级](assets/icon-drag-and-drop-action.png) | 用于根据优先级拖放源。 |
| ![单击图标以取消分配源](assets/icon-delete-action.png) | 为库存取消分配源。 |

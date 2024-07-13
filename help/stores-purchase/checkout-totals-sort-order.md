---
title: 签出总计排序顺序
description: 了解显示的结帐总计以及如何根据订单摘要配置结帐总计排序顺序。
exl-id: 2b1345e3-6ad3-472a-af3e-3f7b24577b13
feature: Checkout, Configuration
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 0%

---

# 签出总计排序顺序

在订单复查期间，合计显示在订单底部，其中包括折扣、运费、商店贷项和税的任何调整。 每个项目的顺序决定了计算的顺序，并在配置中按分配给每个项目的编号进行设置。 例如，小计是部分中的第一个项目，其值被指定为10。 “总计”将显示在最后，并且被指定为100值。 合计部分中的所有其他项将分配一个介于这些值之间的值。

![订单摘要显示签出总计](./assets/storefront-checkout-totals.png){width="700" zoomable="yes"}

**_要配置签出总计排序顺序：_**

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧面板中，展开&#x200B;**[!UICONTROL Sales]**&#x200B;部分并在下面选择&#x200B;**[!UICONTROL Sales]**。

1. 展开&#x200B;**[!UICONTROL Checkout Totals Sort Order]**&#x200B;部分的![扩展选择器](../assets/icon-display-expand.png)。

   ![编号为以确定排序顺序的签出总计选项](../configuration-reference/sales/assets/sales-checkout-totals-sort-order.png){width="600" zoomable="yes"}

   有关每个配置设置的详细说明，请参阅&#x200B;_配置参考指南_&#x200B;中的[签出总计排序顺序](../configuration-reference/sales/sales.md#checkout-totals-sort-order)。

1. 如果该设置针对特定的存储视图，[请选择应用该配置的存储视图](../configuration-reference/scope-change.md#set-the-scope)。

   出现提示时，单击&#x200B;**[!UICONTROL OK]**&#x200B;继续。

1. 要确定&#x200B;_总计_&#x200B;部分中的顺序，请更改分配给每个项目的编号。

   值越低，其在列表中的放置位置越早。 在默认配置中，小计(`10`)是第一个，总计(`100`)是最后一个。

   如有必要，请清除&#x200B;**[!UICONTROL Use system value]**&#x200B;复选框以完成这些更改。

1. 单击&#x200B;**[!UICONTROL Save Config]**。

---
title: 数据管理功能板
description: 了解如何访问有关目录服务、实时搜索和产品Recommendations的数据流的见解。
feature: Products, Customers, Data Import/Export
source-git-commit: eed80afd8755d416d979c362f8c21fe97ce2d2ba
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 0%

---


# 数据管理功能板

“数据管理功能板”可让您深入了解Adobe Commerce SaaS产品的数据流。 用户 [!DNL Live Search]， [!DNL Product Recommendations]、和 [!DNL Catalog Service] 可以从单个功能板查看产品同步状态和重新同步数据。

数据管理功能板位于 *系统* >数据传输> *数据管理功能板*.

![数据管理功能板](assets/data-management-dashboard.png)

## 设置

此 **[!UICONTROL Settings]** 页面右侧的按钮将打开对话框，您可以在其中重新同步目录数据。

重新同步目录数据强制服务从Commerce数据库中重新获取数据。 当目录同步数小时未运行时，通常在首次载入期间使用此操作。

## 同步状态

此 _[!UICONTROL Sync]_状态面板报告过去三小时内已同步的产品数量。 如果您不经常更新目录，此值通常为零。 单击&#x200B;**[!UICONTROL Refresh]**以刷新计数。

## 产品计数

产品计数面板反映可供该服务使用的目录产品的总数。

此 [!DNL Product Recommendations] 和 [!DNL Live Search] 仪表板显示总数 _可显示_ 产品。 [!DNL Catalog Service] 不按可显示内容过滤产品，因此，如果您同时具有 [!DNL Catalog Service] 和 [!DNL Live Search] 或 [!DNL Product Recommendations] 安装后，两个功能板可能会显示两个不同的产品计数值。

## 已同步的产品

“同步的产品”表提供有关索引中产品的详细信息。 默认情况下，此表按“上次更新时间”排序。

要查找特定产品，请使用 **[!UICONTROL Search by SKU]** 字段。
要控制显示的列，请单击 **[!UICONTROL Customize Table]** 在桌子的右边。

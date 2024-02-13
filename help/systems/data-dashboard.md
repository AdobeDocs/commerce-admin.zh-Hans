---
title: 数据管理功能板
description: 了解数据管理功能板
feature: Products, Customers, Data Import/Export
source-git-commit: 925af4d3841f2972dfffcd52125a41c4a4b28815
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 0%

---

# 数据管理功能板

“数据管理功能板”可让您深入了解Adobe Commerce SaaS产品的数据流。 用户 [!DNL Live Search]， [!DNL Product Recommendations]、和 [!DNL Catalog Service] 可以从单个功能板查看产品同步状态和重新同步数据。

数据管理功能板位于 *系统* >数据传输> *数据管理功能板*.

![数据管理功能板](assets/data-management-dashboard.png)

## 设置

页面右侧的“设置”按钮打开 [[!DNL Catalog Sync]](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/data-services/catalog-sync.html) “设置”对话框。

通常， [!DNL Catalog Sync] 进程每小时自动运行一次。

重新同步目录数据强制服务从Commerce数据库重新获取数据，确保最新的更改反映在服务和您的网站上。 如果您进行了一些产品更改，并且需要在正常自动同步过程之前更新这些更改，请使用此按钮。

## 同步状态

此 _[!UICONTROL Sync]_状态面板报告过去三小时内已同步的产品数量。 如果您不经常更新目录，此值通常为零。 单击&#x200B;**[!UICONTROL Refresh]**以刷新计数。

## 产品计数

产品计数面板反映可供该服务使用的目录产品的总数。

此 [!DNL Catalog Service] 仪表板反映目录中可供服务使用的产品总数。 这通常是Commerce数据库中的所有产品。

产品Recommendations和Live Search功能板显示总数 [_可搜索_](https://experienceleague.adobe.com/docs/commerce-admin/catalog/catalog/search/search.html) 产品。 如果某些产品未设置为可搜索，则会导致两者之间的产品总数差异 [!DNL Product Recommendations] 和 [!DNL Live Search]、和 [!DNL Catalog Service].

## 已同步的产品

“同步的目录产品”表提供有关索引中产品的详细信息。 默认情况下，此表按“上次更新时间”排序。

要查找特定产品，请使用**[!UICONTROL Search by SKU]**字段。
要控制显示的列，请单击 **[!UICONTROL Customize Table]** 在桌子的右边。

---
title: 配置申请列表最大值
description: 了解申请列表配置，该配置控制每个客户帐户可维护的最大数量。
exl-id: a36dda0e-c00f-4182-9046-717b9d811f71
feature: B2B, Companies, Configuration
role: Admin
source-git-commit: 03d1892799ca5021aad5c19fc9f2bb4f5da87c76
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 0%

---

# 配置申请列表最大值

启用申请列表功能后，客户可以创建多个经常采购的物料列表，并使用这些列表进行订单下单。 它同时适用于已登录的用户和来宾。 您可以在以下情况下启用申请列表： [配置B2B功能](enable-basic-features.md).

客户可以有多个列表，重点关注来自不同供应商、购买者、团队、营销活动的产品，或简化常见工作流程的任何其他产品。 [申购单列表功能](requisition-lists.md) 与愿望清单类似，但存在以下差异：

- 将物料发送到购物车后未清除申请列表。 它可多次使用。
- 申请列表的用户界面使用紧凑视图来显示许多物料。

默认情况下，客户可以为其帐户维护多达999个申请列表。 但您可以修改配置并指定较低的数字以减轻存储上的负载。

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中，展开 **[!UICONTROL Customers]** 并选择 **[!UICONTROL Requisition Lists]**.

   ![申购单列表 — 常规设置](./assets/requisition-lists-general.png){width="600" zoomable="yes"}

1. 对象 **[!UICONTROL Number of Requisition Lists]**，输入可为每个客户帐户维护的申请列表的最大数量。

   最小值为 `2`，最大值为 `999`.

1. 完成后，单击 **[!UICONTROL Save Config]**.

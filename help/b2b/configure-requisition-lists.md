---
title: 配置申请列表最大值
description: 了解申请列表配置，该配置控制每个客户帐户可维护的最大数量。
exl-id: a36dda0e-c00f-4182-9046-717b9d811f71
feature: B2B, Companies, Configuration
role: Admin
TQID: 'https://experienceleague.adobe.com/we9sPvRg20kEV4EpfemuA7WW-rjv7G6evjr5MwzRGyM'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: e9004f3c-09ae-5d24-acd2-fa0987fdb66e
    internal-label: Companies
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
    internal-label: Accounts
subfeature_v2:
  - id: f56d26ed-050b-4fb7-b29b-8e6e994e80a2
    internal-label: B2B
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: acc7571574eb9c7e96911266897350a77913488e
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 0%
---
# 配置申请列表最大值

启用申请列表功能后，客户可以创建多个经常采购的物料列表，并使用这些列表进行订单下单。 它同时适用于已登录的用户和来宾。 您可以在[配置B2B功能](enable-basic-features.md)时启用申请列表。

客户可以有多个列表，重点关注来自不同供应商、购买者、团队、营销活动的产品，或简化常见工作流程的任何其他产品。 [申购单列表功能](requisition-lists.md)与愿望列表类似，但有以下区别：

- 将物料发送到购物车后未清除申请列表。 它可多次使用。
- 申请列表的用户界面使用紧凑视图来显示许多物料。

默认情况下，客户可以为其帐户维护多达999个申请列表。 但您可以修改配置并指定较低的数字以减轻存储上的负载。

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧面板中，展开&#x200B;**[!UICONTROL Customers]**&#x200B;并选择&#x200B;**[!UICONTROL Requisition Lists]**。

   ![申请列表 — 常规设置](./assets/requisition-lists-general.png){width="600" zoomable="yes"}

1. 对于&#x200B;**[!UICONTROL Number of Requisition Lists]**，输入每个客户帐户可维护的申请列表的最大数量。

   最小值为`2`，最大值为`999`。

1. 完成后，单击&#x200B;**[!UICONTROL Save Config]**。

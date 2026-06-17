---
title: 产品设置 — [!UICONTROL Sources]
description: 对于产品，[!UICONTROL Sources]设置提供对可从其中分发产品的 [!DNL Inventory Management] 源的访问权限。
exl-id: 986f6031-0edc-4105-aa02-1c22364b3e7c
feature: Catalog Management, Products, Inventory
TQID: https://experienceleague.adobe.com/7LFF4ufXyKtJwUp4DiNDdnRMhFRsM1tX8Z2TlPt1Kso
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
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
source-wordcount: 259
ht-degree: 0%

---

# 产品设置 — [!UICONTROL Sources]

产品设置的&#x200B;_[!UICONTROL Sources]_&#x200B;部分列出了分发产品的来源。 它用于分配和取消分配来源，以及管理产品的数量和可用性。 仅当为您的存储定义了多个源时，才会显示此部分。 有关源的详细信息，请参阅[管理源](../inventory-management/sources-manage.md)。

## 为产品分配源

1. 单击&#x200B;**[!UICONTROL Assign Source]**。

1. 选中所需源的复选框。

1. 单击&#x200B;**[!UICONTROL Done]**。

1. 选择&#x200B;**[!UICONTROL Source Item Status]**&#x200B;并根据需要输入&#x200B;**[!UICONTROL Qty]**&#x200B;和&#x200B;**[!UICONTROL Notify Qty]**&#x200B;值。

1. 单击&#x200B;**[!UICONTROL Save]**&#x200B;保存更改。

![源视图](./assets/catalog-sources-list.png){width="600" zoomable="yes"}

## 字段引用

| 字段 | 描述 |
|--- |--- |
| [!UICONTROL Name] | 源的唯一名称。 |
| [!UICONTROL Source Status] | 确定在目录中是启用还是禁用该产品。 |
| [!UICONTROL Source Item Status] | 确定产品的当前可用性。 选项：<br />**[!UICONTROL In Stock]**— 使产品可供购买。<br />**[!UICONTROL Out of Stock]**  — 除非激活延交订单，否则将阻止产品可供购买，并从目录中删除列表。 |
| [!UICONTROL Qty] | 每个来源的现有库存量。 |
| [!UICONTROL Notify Qty] | 如果未选择`Notify Quantity Use Default`，则此特定源的&#x200B;_通知数量_&#x200B;的金额。 |
| [!UICONTROL Notify Qty Use Default] | 指示使用产品“高级库存”中的&#x200B;_通知数量_&#x200B;的默认设置或商店配置中的全局设置。 有关产品的高级清单设置的详细信息，请参阅[配置高级产品选项](../inventory-management/product-options.md)。 |
| [!UICONTROL Actions] | 对于已分配的源，单击&#x200B;**[!UICONTROL Unassign]**&#x200B;使该源不可用于该产品。 对于未分配的源，单击&#x200B;**[!UICONTROL Assign Sources]**&#x200B;使该源可用于该产品。 有关[!UICONTROL Assign Sources]选项的详细信息，请参阅[为每个产品分配源](../inventory-management/sources-assign-per-product.md)。 |

{style="table-layout:auto"}

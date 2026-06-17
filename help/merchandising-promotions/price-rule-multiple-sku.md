---
title: 具有多个SKU的目录价格规则
description: 了解如何将单个目录价格规则应用于多个SKU。
exl-id: 99023460-0501-45cd-8990-5f2b9ed7b4a2
feature: Merchandising, Price Rules, Catalog Management
TQID: https://experienceleague.adobe.com/nChe-8VA4V0nrC46PbeKyh7DB4Ta-0lpcezMV3uHEw0
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 367
ht-degree: 0%

---

# 具有多个SKU的目录价格规则

单个目录价格规则可应用于多个SKU，这使得根据产品、品牌或类别创建各种促销活动成为可能。 创建此规则时，您需要设置与所选SKU匹配的条件。 在构建规则时，您可以轻松地浏览并从网格中选择SKU。

## 步骤1. 验证产品属性的店面属性

在开始之前，请确保`sku`属性的[Storefront属性](../catalog/attribute-product-create.md#step-4-describe-the-storefront-properties)设置为`Use in Promo Rules`。

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**。

1. 在&#x200B;_[!UICONTROL Attribute Code]_&#x200B;列顶部的搜索筛选器中，输入`sku`并单击&#x200B;**[!UICONTROL Search]**。

1. 单击以在编辑模式下打开`sku`属性。

1. 在左侧面板中，单击&#x200B;**[!UICONTROL Storefront Properties]**&#x200B;并确保将&#x200B;**[!UICONTROL Use for Promo Rule Conditions]**&#x200B;设置为`Yes`。

1. 如果更改了属性的值，请单击&#x200B;**[!UICONTROL Save Attribute]**。

## 步骤2. 将价格规则应用于多个SKU

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Catalog Price Rules]**。

1. 执行以下操作之一：

   - 按照说明创建[目录价格规则](price-rules-catalog.md)。
   - 打开现有的目录价格规则。

1. 展开&#x200B;**[!UICONTROL Conditions]**&#x200B;部分中的![扩展选择器](../assets/icon-display-expand.png)，然后执行以下操作：

   - 在第一行中，将第一个参数设置为`ANY`。

     ![目录价格规则条件 — ANY](./assets/multiple-skus-condition1.png){width="600" zoomable="yes"}

   - 在下一行的开头单击&#x200B;_添加_ （![添加图标](../assets/icon-add-green-circle.png)），然后在&#x200B;**[!UICONTROL Product Attribute]**&#x200B;下的列表中单击`SKU`。

     ![目录价格规则条件 — SKU是](./assets/multiple-skus-condition1a.png){width="600" zoomable="yes"}之一

   - 要进行比较，您可以选择以下选项。 如果要从SKU列表中至少查找一个，`select is one of`。 如果要查找必须找到所有要应用的SKU组，请选择`is`。 我们建议选择`is one of`。

     ![目录价格规则条件 — SKU是](./assets/multiple-skus-condition1b.png){width="600" zoomable="yes"}之一

   - 要完成条件，请单击更多(**...**)链接，然后单击可用产品列表的&#x200B;_选择器_ （![列表图标](../assets/icon-list-chooser.png)）图标。

     ![目录价格规则条件 — 多个SKU](./assets/multiple-skus-condition2b.png){width="600" zoomable="yes"}

   - 浏览、过滤或搜索以查找要添加的SKU。 在列表中，选中要包含的每个产品的复选框。

   - 单击&#x200B;**[!UICONTROL Save and Apply]**&#x200B;以将SKU添加到条件。

     ![目录价格规则条件 — 多个SKU](./assets/multiple-skus-condition2.png){width="600" zoomable="yes"}

1. 完成规则，包括满足条件时要执行的任何[操作](price-rules-catalog.md)。

1. 规则完成后，单击&#x200B;**[!UICONTROL Save]**。

{{new-price-rule}}

---
title: 具有多个SKU的目录价格规则
description: 了解如何将单个目录价格规则应用于多个SKU。
exl-id: 99023460-0501-45cd-8990-5f2b9ed7b4a2
feature: Merchandising, Price Rules, Catalog Management
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '367'
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

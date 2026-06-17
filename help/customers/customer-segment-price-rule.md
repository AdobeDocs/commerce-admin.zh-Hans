---
title: 价格规则中的客户区段
description: 了解如何将客户区段与购物车价格规则关联，以便您能够为商店定义定向促销活动。
exl-id: eaa04e7a-c0f9-4f09-8e65-75965ccbdc69
feature: Customers, Configuration, Price Rules
TQID: https://experienceleague.adobe.com/MSMNikJwG2lQuLlQxnK82zjCOeF-u8JEjmabKFJgpZU
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 232
ht-degree: 0%

---

# 价格规则中的客户区段

{{ee-feature}}

通过将客户区段与[购物车价格规则](../merchandising-promotions/price-rules-cart.md)相关联，可将其用于目标促销。

![购物车价格规则 — 目标客户区段](assets/price-rule-cart-condition-segments.png){width="700" zoomable="yes"}

_&#x200B;**要将区段与购物车价格规则关联，请执行以下操作：**&#x200B;_

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Marketing]** > _促销活动_ > **[!UICONTROL Cart Price Rules]**。

1. 打开新规则或现有规则：

   * 要使用新规则，请单击右上角的&#x200B;**[!UICONTROL Add New Rule]**。
   * 要使用现有规则，请单击列表中的规则以在编辑模式下将其打开。

1. 向下滚动并展开&#x200B;**[!UICONTROL Conditions]**&#x200B;部分。

1. 添加条件。

   * 单击&#x200B;_添加_ （![列表图标](../assets/icon-add-green-circle.png)）图标，该图标显示条件列表。 然后选择&#x200B;**[!UICONTROL Customer Segment]**。

   ![购物车价格规则 — 添加客户区段条件](assets/condition-customer-segment.png){width="600" zoomable="yes"}

   默认情况下，该条件设置为查找匹配条件。 如果需要，请单击&#x200B;**[!UICONTROL matches]**&#x200B;链接，并将运算符更改为以下操作之一：

   * `does not match`
   * `is one of`
   * `is not one of`

   ![条件运算符](assets/price-rule-condition-customer-segment-operator.png){width="600" zoomable="yes"}

1. 要定位特定区段，请单击“更多&#x200B;**...**”链接以显示其他选项。 然后，单击&#x200B;_选择器_ （![列表图标](../assets/icon-list-chooser.png)）图标以显示客户区段列表。

1. 在列表中，选中要以条件定位的每个区段的复选框。

   ![购物车价格规则 — 条件选择器列表](assets/condition-segment-chooser-list.png){width="600" zoomable="yes"}

1. 单击&#x200B;**[!UICONTROL Select]**&#x200B;将所选客户区段置于条件中。

1. 根据需要完成价格规则的其余部分。

1. 完成后，单击&#x200B;**[!UICONTROL Save]**。

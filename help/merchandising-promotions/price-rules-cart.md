---
title: 购物车价格规则
description: 了解根据一组条件对购物车中的商品应用折扣的购物车价格规则。
exl-id: f3038f2a-9d34-4696-a39e-f87fbb1294a2
feature: Merchandising, Price Rules, Shopping Cart
TQID: https://experienceleague.adobe.com/i3G3iGuomU0cjy3aX9eynyzAtpCgQxeEFAyRUdUUu44
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: b5520579-b31f-4df7-9281-f0d9f91e2edcid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 451
ht-degree: 0%

---

# 购物车价格规则

购物车价格规则根据一组条件对购物车中的商品应用折扣。 当满足条件或客户输入有效优惠券代码时，可自动应用折扣。 应用时，折扣会显示在小计下的购物车中。 购物车价格规则可以根据需要通过更改其状态和日期范围用于季节或促销。

>[!NOTE]
>
>如果优惠券购物车规则具有指定结账选项的条件，例如某些送货或付款方法，则只有在选择特定送货/付款方法后才能在结账时满足这些条件。 在这种情况下，可在最后一步结账时应用优惠券。

![店面示例 — 购物车应用优惠券](./assets/storefront-cart-apply-coupon.png){width="600" zoomable="yes"}

## 访问购物车价格规则

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Cart Price Rules]**。

   ![购物车价格规则](./assets/price-rule-cart.png){width="700" zoomable="yes"}

1. 如果您有许多规则，请使用每列顶部的筛选器选项来简化列表，然后单击&#x200B;**[!UICONTROL Search]**&#x200B;以应用筛选器。

1. 要清除所有筛选器选项并显示完整列表，请单击&#x200B;**[!UICONTROL Reset Filter]**。

1. 更新规则的属性：

   - ![Adobe Commerce](../assets/adobe-logo.svg)（仅限Adobe Commerce）单击&#x200B;**[!UICONTROL Edit]**&#x200B;以显示“规则信息”页面。

   - ![Magento Open Source](../assets/open-source.svg)（仅限Magento Open Source）单击列表中的规则以显示“规则信息”页面。

   您可以在此处更改规则的设置（与创建规则类似）。

## 按列筛选选项

| 列 | 描述 |
|--- |--- |
| [!UICONTROL ID] | 输入文本以筛选特定规则ID号的列表。 |
| [!UICONTROL Rule] | 输入文本，以根据创建规则时定义的规则名称筛选列表。 |
| [!UICONTROL Coupon Code] | 输入文本，以根据创建规则时定义的代码名称筛选列表。 |
| [!UICONTROL Priority] | 自由文本字段，用于根据为规则定义的优先级筛选列表。 |
| [!UICONTROL Status] | 使用此选项可根据规则状态（`Active`或`Inactive`）筛选列表。 |
| [!UICONTROL Web Site] | 使用此选项可根据为规则定义的网站筛选列表。 |
| [!UICONTROL Action] | ![Adobe Commerce](../assets/adobe-logo.svg)（仅限Adobe Commerce）单击&#x200B;**[!UICONTROL Edit]**&#x200B;以显示&#x200B;_[!UICONTROL Rule Information]_页面并更新规则设置（与创建规则类似）。 |
| [!UICONTROL Start] | ![Magento Open Source](../assets/open-source.svg)（仅限Magento Open Source）使用动态日历字段（_[!UICONTROL To:]_和_[!UICONTROL From:]_）根据创建规则时定义的规则的开始日期筛选列表。 |
| [!UICONTROL End] | ![Magento Open Source](../assets/open-source.svg)（仅限Magento Open Source）使用动态日历字段（_[!UICONTROL To:]_和_[!UICONTROL From:]_）根据创建规则时定义的规则的结束日期筛选列表。 |

{style="table-layout:auto"}

## 使用Real-Time CDP受众来告知购物车价格规则

了解如何在您的Adobe Commerce实例中[激活](../customers/audience-activation.md)Real-Time CDP受众以告知购物车价格规则。

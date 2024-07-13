---
title: 目录价格规则
description: 了解目录价格规则，这些规则可用于根据一组定义的条件以折扣价格向买方提供产品。
exl-id: 8da95076-d724-41f6-b3ca-e61ff1906b72
feature: Merchandising, Price Rules, Catalog Management
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '522'
ht-degree: 0%

---

# 目录价格规则

目录价格规则可用于根据一组已定义的条件以折扣价格向买方提供产品。 目录价格规则不使用[优惠券代码](price-rules-cart-coupon.md)，因为它们是在将产品放入购物车之前触发的。

例如，您可以定义并设置价格规则的条件，当满足该条件时，将自动显示具有特殊或促销价格的产品。 定义的规则属性可能包括客户组、产品类别、折扣金额或百分比、产品颜色、产品大小，或者商店中设置的几乎任何产品属性。 您可以为价格规则设置起始日期和终止日期，以在该规则中定义的日期自动开始和停止促销。 可以根据需要更新或修改已保存规则的属性。

- ![Adobe Commerce](../assets/adobe-logo.svg)(仅限Adobe Commerce)您还可以将定义的规则链接到[动态块](../content-design/dynamic-blocks.md)，以帮助促销商店中的事件或产品。

- ![Magento Open Source](../assets/open-source.svg)(仅限Magento Open Source)对于定期促销，每次要运行促销时，您都可以手动将保存的规则设置为&#x200B;_活动_&#x200B;或&#x200B;_不活动_&#x200B;状态。

## 访问目录价格规则

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Catalog Price Rules]**。

   ![目录价格规则](./assets/price-rule-catalog.png){width="700" zoomable="yes"}

1. 更新规则的属性：

   - ![Adobe Commerce](../assets/adobe-logo.svg)(仅限Adobe Commerce)单击&#x200B;**[!UICONTROL Edit]**&#x200B;以显示&#x200B;_规则信息_&#x200B;页面。

   - ![Magento Open Source](../assets/open-source.svg) (仅限Magento Open Source)单击列表中的规则以显示“规则信息”页。

   您可以在此处更改规则的设置（类似于[创建规则](price-rules-catalog-create.md)）。

## 筛选器选项

| 字段 | 描述 |
|--- |--- |
| [!UICONTROL ID] | 输入文本以筛选特定规则ID号的列表。 |
| [!UICONTROL Rule] | 输入文本，以根据创建规则时定义的规则名称筛选列表。 |
| [!UICONTROL Priority] | ![Adobe Commerce](../assets/adobe-logo.svg)(仅限Adobe Commerce)在此字段中输入文本，以根据为规则定义的优先级筛选列表。 |
| [!UICONTROL Web Site] | ![Adobe Commerce](../assets/adobe-logo.svg)(仅限Adobe Commerce)使用此选项可根据为规则定义的网站筛选列表。 |
| [!UICONTROL Action] | ![Adobe Commerce](../assets/adobe-logo.svg)(仅限Adobe Commerce)单击&#x200B;**[!UICONTROL Edit]**&#x200B;以显示规则信息并更新规则设置（与创建规则类似）。 |
| [!UICONTROL Start] | ![Magento Open Source](../assets/open-source.svg)(仅限Magento Open Source)使用动态日历字段(“收件人”(To：)和“发件人”(From：))根据创建规则时定义的规则的开始日期筛选列表。 |
| [!UICONTROL End] | ![Magento Open Source](../assets/open-source.svg)(仅限Magento Open Source)使用动态日历字段(“收件人”(To：)和“发件人”(From：))根据创建规则时定义的规则的结束日期筛选列表。 |
| [!UICONTROL Status] | ![Magento Open Source](../assets/open-source.svg) (仅限Magento Open Source)使用此选项根据规则状态（`Active`或`Inactive`）筛选列表。 |

{style="table-layout:auto"}

## 资源疑难解答

有关目录价格规则问题疑难解答的帮助，请参阅以下Commerce支持知识库文章：

- 执行目录价格规则计划更新后，[404商店前端出错](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/known-issues-patches-attached/404-error-on-store-front-once-catalog-price-rule-schedules-update-is-performed.html)
- [通过相关产品和目标规则改进了产品页面的性能](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-9/mdva-31791-magento-patch-improvement-for-product-page-with-related-products-and-target-rules.html)
- [目录价格规则不起作用](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-14/mdva-24201-magento-patch-catalog-price-rules-don-t-work.html)
- [GraphQL价格计算](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-14/mdva-33975-magento-patch-graphql-price-calculations.html)

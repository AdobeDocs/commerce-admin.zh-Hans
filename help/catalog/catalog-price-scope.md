---
title: 价格范围
description: 了解用于产品价格的范围，可以将其配置为在全球或网站级别应用。
exl-id: 3726b16b-4ed5-4286-a7fd-69ed6677f87a
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '326'
ht-degree: 0%

---

# 价格范围

范围 [基础货币](../stores-purchase/currency-configuration.md) 可用于产品价格的区段，可以配置为在全球或网站级别应用。 如果应用到全局级别，则在整个商店层次结构中使用相同的价格。 如果应用到网站级别，则可以使用与不同网站关联的商店中的相同产品，但价格不同。 默认情况下，产品定价的范围是全球性的。

不同的因素可能会影响同一产品在一个地点的价格，而不会影响另一个地点的价格。 例如，产品可能会产生额外的分销成本，以及影响特定商店中销售产品价格的其他注意事项。 下图显示了将基础货币设置为网站级别的多站点安装。 与每个网站关联的商店和商店视图反映在网站级别设置的产品定价。

![适用于Adobe Commerce的B2B](../assets/b2b.svg) 如果您使用共享目录，另请参阅 [设置共享目录定价和结构](../b2b/catalog-shared-pricing-structure.md) 在 _Adobe Commerce的B2B指南_.

![价格范围图](./assets/catalog-price-scope.svg){width="550"}

## 配置价格范围

1. 在 _管理员_ 菜单，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中，展开 **[!UICONTROL Catalog]** 并选择 **[!UICONTROL Catalog]** 下方。

1. 向下滚动到 **[!UICONTROL Price]** 分区和设置 **[!UICONTROL Catalog Price Scope]** 更改为以下任一项：

   - `Global`
   - `Website`

   您选择的范围设置显示在目录的价格字段下方。

   ![目录价格范围](./assets/catalog-price.png){width="600" zoomable="yes"}

1. 完成后，单击 **[!UICONTROL Save Config]**.

## 使用范围设置产品价格

Commerce不允许为每个商店设置产品价格。 但您可以更改每个网站的价格：

1. 在 _管理员_ 菜单，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中，展开 **[!UICONTROL Catalog]** 并选择 **[!UICONTROL Catalog]** 下方。

1. 在 **[!UICONTROL Price]** 选项卡，将价格范围设置为 `Website` 而不是全球性的。

1. 通过打开产品编辑页面，选择左上角的范围，然后为每个网站输入新价格来设置价格。

---
title: 价格范围
description: 了解用于产品价格的范围，可以将其配置为在全球或网站级别应用。
exl-id: 3726b16b-4ed5-4286-a7fd-69ed6677f87a
feature: Catalog Management, Products
source-git-commit: bc3977f29c8048a1b8578aa21fa55fa1a4d903f2
workflow-type: tm+mt
source-wordcount: '376'
ht-degree: 0%

---

# 价格范围

可将用于产品价格的[基本货币](../stores-purchase/currency-configuration.md)的范围配置为在全局或网站级别应用。 如果应用到全局级别，则在整个商店层次结构中使用相同的价格。 如果应用到网站级别，则可以使用与不同网站关联的商店中的相同产品，但价格不同。 默认情况下，产品定价的范围是全球性的。

不同的因素可能会影响同一产品在一个地点的价格，而不会影响另一个地点的价格。 例如，产品可能会产生额外的分销成本，以及影响特定商店中销售产品价格的其他注意事项。 下图显示了将基础货币设置为网站级别的多站点安装。 与每个网站关联的商店和商店视图反映在网站级别设置的产品定价。

![Adobe Commerce B2B](../assets/b2b.svg)如果您使用共享目录，另请参阅[Adobe Commerce B2B指南](../b2b/catalog-shared-pricing-structure.md)中的&#x200B;_设置共享目录定价和结构_。

![价格范围图](./assets/catalog-price-scope.svg){width="550"}

## 配置价格范围

1. 在&#x200B;_管理员_&#x200B;菜单上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧面板中，展开&#x200B;**[!UICONTROL Catalog]**&#x200B;并在下面选择&#x200B;**[!UICONTROL Catalog]**。

1. 向下滚动到&#x200B;**[!UICONTROL Price]**&#x200B;部分，并将&#x200B;**[!UICONTROL Catalog Price Scope]**&#x200B;设置为以下项之一：

   - `Global`
   - `Website`

   您选择的范围设置显示在目录的价格字段下方。

   ![目录价格范围](./assets/catalog-price.png){width="600" zoomable="yes"}

1. 完成后，单击&#x200B;**[!UICONTROL Save Config]**。

## 使用范围设置产品价格

Commerce不允许为每个商店设置产品价格。 但您可以更改每个网站的价格：

1. 在&#x200B;_管理员_&#x200B;菜单上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧面板中，展开&#x200B;**[!UICONTROL Catalog]**&#x200B;并在下面选择&#x200B;**[!UICONTROL Catalog]**。

1. 在&#x200B;**[!UICONTROL Price]**&#x200B;选项卡中，将价格范围设置为`Website`而不是`Global`。

1. 通过打开产品编辑页面，选择左上角的范围，然后为每个网站输入新价格来设置价格。

在极少数情况下，当价格范围设置为`Global`时，Commerce数据库在网站级别上仍可以有不同的价格。 这可能是由于Commerce外部的同步问题而发生的。 在这些情况下，商家必须在商店级别执行价格清理，并运行与Commerce Services的目录同步。
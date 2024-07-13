---
title: 税种
description: 了解如何配置用于税则的税分类。
exl-id: dd867eba-3f1e-45a8-9332-9e668a2092e1
feature: Taxes
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '501'
ht-degree: 0%

---

# 税种

税分类可分配给客户、产品和发运。 Commerce分析每位客户的购物车，并根据客户类别、购物车中产品的类别以及区域计算相应的税额。 区域由客户的送货地址、帐单地址或送货来源来确定。 定义[税则](tax-rules.md)后，可以创建新的税类。

- **客户** — 您可以根据需要创建任意数量的客户税类，并将其分配给[客户组](../customers/customer-groups.md)。 例如，在某些管辖区，批发交易不征税，但零售交易征税。 您可以将“批发客户”组的成员与“批发”税类相关联。

- **产品** — 在计算中使用产品类，以确定购物车中应用的正确税率。 在创建产品时，该产品将分配给特定的税分类。 例如，食物可能不征税，或按不同的税率征税。

- **运费** — 如果您的商店对运费收取额外税费，您应该为运费指定特定的产品税类。 然后在配置中，将其指定为用于发运的税分类。

## 配置税分类

在&#x200B;_[!UICONTROL Sales]_配置中设置[产品和客户](#add-a-product-tax-class)的纳税类别以及默认纳税类别。

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧面板中，展开&#x200B;**[!UICONTROL Sales]**&#x200B;并选择&#x200B;**[!UICONTROL Tax]**。

1. 展开&#x200B;**[!UICONTROL Tax Classes]**&#x200B;部分的![扩展选择器](../assets/icon-display-expand.png)。

   ![配置 — 税类](../configuration-reference/sales/assets/tax-tax-classes.png){width="600" zoomable="yes"}

1. 为以下各项选择税分类：

   - **[!UICONTROL Set Tax Class for Shipping]**
   - **[!UICONTROL Tax Class for Gift Options]**
   - **[!UICONTROL Default Tax Class for Product]**
   - **[!UICONTROL Default Tax Class for Customer]**

1. 完成后，单击&#x200B;**[!UICONTROL Save Config]**。

## 添加税分类

可以方便地为客户和产品添加税类，然后将其分配给个别客户和产品，并用于税则中。

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Rules]**。

1. 单击&#x200B;**[!UICONTROL Add New Tax Rule]**。

1. 展开&#x200B;**[!UICONTROL Additional Settings]**&#x200B;部分的![扩展选择器](../assets/icon-display-expand.png)。

   ![添加新税类](./assets/tax-class-additional-settings.png){width="600" zoomable="yes"}

1. 在&#x200B;_客户税类_&#x200B;下，单击&#x200B;**[!UICONTROL Add New Tax Class]**。

1. 在文本框中输入新税种的&#x200B;**[!UICONTROL Name]**。

   ![添加新税类](./assets/tax-class-customer-add-new.png){width="600" zoomable="yes"}

1. 要将新分类添加至可用客户税分类的列表，请单击复选标记。

   ![新税类](./assets/tax-classes-updated.png){width="600" zoomable="yes"}

## 添加产品税分类

1. 在&#x200B;_产品税类_&#x200B;下，单击&#x200B;**[!UICONTROL Add New Tax Class]**。

1. 在文本框中输入新税种的&#x200B;**[!UICONTROL Name]**。

1. 要将新分类添加到可用产品税分类的列表，请单击复选标记。

1. 完成后，单击按钮栏中的&#x200B;**[!UICONTROL Back]**&#x200B;以返回到&#x200B;_税则_&#x200B;网格。

## 默认纳税目标

默认纳税目标设置确定用作纳税计算基础的国家/地区、省/自治区/直辖市以及邮政编码。

**_要为计算配置默认税务目标：_**

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧面板中，展开&#x200B;**[!UICONTROL Sales]**&#x200B;并选择&#x200B;**[!UICONTROL Tax]**。

1. 展开&#x200B;**[!UICONTROL Default Tax Destination Calculation]**&#x200B;部分的![扩展选择器](../assets/icon-display-expand.png)。

   ![默认纳税目标计算](../configuration-reference/sales/assets/tax-default-tax-destination-calculation.png){width="600" zoomable="yes"}

1. 将&#x200B;**[!UICONTROL Default Country]**&#x200B;设置为税收计算所基于的国家/地区。

1. 将&#x200B;**[!UICONTROL Default State]**&#x200B;设置为用作计税基础的州或省。

1. 将&#x200B;**[!UICONTROL Default Post Code]**&#x200B;设置为用作本地税计算基础的邮政编码。

1. 完成后，单击&#x200B;**[!UICONTROL Save Config]**。

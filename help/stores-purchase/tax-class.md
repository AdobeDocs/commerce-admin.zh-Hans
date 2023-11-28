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

税分类可分配给客户、产品和发运。 商业分析每个客户的购物车，并根据客户类别、购物车中产品的类别以及区域计算相应的税额。 区域由客户的送货地址、帐单地址或送货来源来确定。 在以下情况下可以创建新的税分类： [税则](tax-rules.md) 已定义。

- **客户**  — 您可以根据需要创建任意数量的客户税分类，并将其分配给 [客户组](../customers/customer-groups.md). 例如，在某些管辖区，批发交易不征税，但零售交易征税。 您可以将“批发客户”组的成员与“批发”税类相关联。

- **产品**  — 在计算中使用产品类，以确定在购物车中应用的正确税率。 在创建产品时，该产品将分配给特定的税分类。 例如，食物可能不征税，或按不同的税率征税。

- **配送**  — 如果您的商店对配送额外收费，则您应当为配送指定特定的产品税分类。 然后在配置中，将其指定为用于发运的税分类。

## 配置税分类

用于发运的税分类，以及的默认税分类 [产品和客户](#add-a-product-tax-class) 在中设置 _[!UICONTROL Sales]_配置。

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中，展开 **[!UICONTROL Sales]** 并选择 **[!UICONTROL Tax]**.

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Tax Classes]** 部分。

   ![配置 — 税分类](../configuration-reference/sales/assets/tax-tax-classes.png){width="600" zoomable="yes"}

1. 为以下各项选择税分类：

   - **[!UICONTROL Set Tax Class for Shipping]**
   - **[!UICONTROL Tax Class for Gift Options]**
   - **[!UICONTROL Default Tax Class for Product]**
   - **[!UICONTROL Default Tax Class for Customer]**

1. 完成后，单击 **[!UICONTROL Save Config]**.

## 添加税分类

可以方便地为客户和产品添加税类，然后将其分配给个别客户和产品，并用于税则中。

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Rules]**.

1. 单击 **[!UICONTROL Add New Tax Rule]**.

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Additional Settings]** 部分。

   ![添加新税分类](./assets/tax-class-additional-settings.png){width="600" zoomable="yes"}

1. 下 _客户税分类_，单击 **[!UICONTROL Add New Tax Class]**.

1. 输入 **[!UICONTROL Name]** 在文本框中输入新的税分类。

   ![添加新税分类](./assets/tax-class-customer-add-new.png){width="600" zoomable="yes"}

1. 要将新分类添加至可用客户税分类的列表，请单击复选标记。

   ![新税分类](./assets/tax-classes-updated.png){width="600" zoomable="yes"}

## 添加产品税分类

1. 下 _产品税分类_，单击 **[!UICONTROL Add New Tax Class]**.

1. 输入 **[!UICONTROL Name]** 在文本框中输入新的税分类。

1. 要将新分类添加到可用产品税分类的列表，请单击复选标记。

1. 完成后，单击 **[!UICONTROL Back]** ，以返回到 _税则_ 网格。

## 默认纳税目标

默认纳税目标设置确定用作纳税计算基础的国家/地区、省/自治区/直辖市以及邮政编码。

**_要为计算配置默认纳税目标，请执行以下操作：_**

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中，展开 **[!UICONTROL Sales]** 并选择 **[!UICONTROL Tax]**.

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Default Tax Destination Calculation]** 部分。

   ![默认纳税目标计算](../configuration-reference/sales/assets/tax-default-tax-destination-calculation.png){width="600" zoomable="yes"}

1. 设置 **[!UICONTROL Default Country]** 税收计算所依据的国家/地区。

1. 设置 **[!UICONTROL Default State]** 用作计税基础的省/自治区/直辖市。

1. 设置 **[!UICONTROL Default Post Code]** 用作本地税计算基础的邮政编码。

1. 完成后，单击 **[!UICONTROL Save Config]**.

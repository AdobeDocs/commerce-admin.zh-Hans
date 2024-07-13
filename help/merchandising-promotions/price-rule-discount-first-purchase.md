---
title: 购物车价格规则示例 — 首次购买的折扣
description: 查看使用购物车价格规则为首次客户提供折扣的示例。
exl-id: 46add769-6fa9-40e0-9f4f-af2215f36283
feature: Merchandising, Price Rules, Shopping Cart
source-git-commit: dbe31fa6e7b83ac852e6e4988ac61627e30d9089
workflow-type: tm+mt
source-wordcount: '737'
ht-degree: 0%

---

# 购物车价格规则示例 — 首次购买的折扣

{{ee-feature}}

购物车价格规则可用于在客户首次购买时自动为他们提供折扣，而无需赠券。

要提供面向首次客户的折扣，您可以：

- 创建定义为&#x200B;_没有订单的采购员_&#x200B;的客户区段，然后
- 创建定位新客户区段的购物车价格规则。

>[!NOTE]
>
>确保已启用客户区段功能。 请参阅[创建客户区段](../customers/customer-segment-create.md)。

## 步骤1. 创建客户区段

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Customers]** > **[!UICONTROL Segments]**。

1. 单击右上角的&#x200B;**[!UICONTROL Add Segment]**。

1. 定义&#x200B;**[!UICONTROL General Properties]**。

   - 输入&#x200B;**[!UICONTROL Segment Name]**&#x200B;以标识客户区段（例如： _首次客户_）。

   - 对于&#x200B;**[!UICONTROL Assigned to Website]**，请选择可在其中使用客户区段的网站。

   - 对于&#x200B;**[!UICONTROL Status]**，选择`Active`。

   - 对于&#x200B;**[!UICONTROL Apply to]**，选择`Visitors and Registered Customers`。

   - 完成后，单击&#x200B;**[!UICONTROL Save and Continue Edit]**。

     左侧面板中提供了其他选项。

   ![客户区段属性](./assets/customer-segment-first-time.png){width="600" zoomable="yes"}

1. 定义&#x200B;**[!UICONTROL Conditions]**。

   对于此示例，条件目标客户的&#x200B;_订单总数小于1_&#x200B;为True。

   - 在左侧的面板中，选择&#x200B;**[!UICONTROL Conditions]**。

     默认条件开始于“如果所有这些条件均为TRUE：”

   - 单击&#x200B;_添加_ （![添加图标](../assets/icon-add-green-circle.png)）并选择`Number of Orders`。

   - 单击&#x200B;**[!UICONTROL is]**&#x200B;并选择`less than`。

   - 单击&#x200B;**...**&#x200B;并在字段中输入`1`。

   - 单击绿色复选标记（ ![绿色复选标记](../assets/icon-checkmark-green-circle.png) ）以保存条件设置。

   ![客户区段条件](./assets/customer-segment-first-time-condition.png){width="600" zoomable="yes"}

1. 单击&#x200B;**[!UICONTROL Save]**。

在&#x200B;_[!UICONTROL Customer Segments]_网格中创建并显示客户区段。

>[!TIP]
>
>记下区段ID。 您可以使用此ID号创建购物车价格规则。

## 步骤2. 创建购物车价格规则

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Cart Price Rule]**。

1. 单击右上角的&#x200B;**[!UICONTROL Add New Rule]**。

   默认显示&#x200B;**[!UICONTROL Rule Information]**&#x200B;部分，其中包含&#x200B;**[!UICONTROL Conditions]**&#x200B;和&#x200B;**[!UICONTROL Conditions]**&#x200B;的可扩展部分。

1. 定义&#x200B;**[!UICONTROL Rule Information]**。

   - 完成&#x200B;**[!UICONTROL Rule Name]**&#x200B;和&#x200B;**[!UICONTROL Description]**&#x200B;字段。 这些字段仅供内部参考。

   - 对于&#x200B;**[!UICONTROL Websites]**，选择规则可用的网站。

   - 对于&#x200B;**[!UICONTROL Customer Groups]**，选择此规则应用于的客户组。

     要选择多个组，请按住Ctrl键(PC)或Command键(Mac)并单击每个选项。

     >[!NOTE]
     >
     >此列表中的选项取决于在&#x200B;**[!UICONTROL Customers]** > **[!UICONTROL Customer Groups]**&#x200B;中创建和管理的客户组。

   - 对于&#x200B;**[!UICONTROL Coupon]**，选择`No Coupon`。

   - 对于&#x200B;**[!UICONTROL Uses per Customer]**，输入`1`。

   - 对于&#x200B;**[!UICONTROL Priority]**，输入一个数字以建立此规则相对于其他规则的优先级。

     >[!NOTE]
     >
     >当同一目录产品满足为多个价格规则设置的条件时，优先级设置非常重要。 具有最高优先级设置的规则将针对客户激活。 最高优先级为1。 对于此示例，输入`1`表示此规则先于任何其他价格规则应用。 此值由&#x200B;**[!UICONTROL Action]**&#x200B;部分中的&#x200B;**[!UICONTROL Discard Subsequent Rules]**&#x200B;设置使用。

   - 完成后，单击&#x200B;**[!UICONTROL Save and Continue Edit]**。

     左侧面板中提供了其他选项。

   ![购物车价格规则信息](./assets/rule-information-first-time.png){width="600" zoomable="yes"}

1. 定义&#x200B;**[!UICONTROL Conditions]**。

   - 向下滚动并展开&#x200B;**[!UICONTROL Conditions]**&#x200B;部分的![扩展选择器](../assets/icon-display-expand.png)。

     默认规则开始于“如果所有这些条件都为TRUE：”。

   - 单击&#x200B;_添加_ （![添加图标](../assets/icon-add-green-circle.png)）并选择`Customer Segment`。

     限定符字段默认为`matches`。

   - 单击&#x200B;**...**，然后输入要定位的客户区段的区段ID。

     对于此示例，在步骤1中创建的新区段的区段ID为`2`。

     >[!NOTE]
     >
     >如果您不知道区段ID，请单击选择器图标（ ![列表图标](../assets/icon-list-chooser.png)）以显示客户区段列表。 您可以在字段中手动输入ID，或选中所需区段的复选框以自动填充该字段。

   - 单击绿色复选标记（ ![绿色复选标记](../assets/icon-checkmark-green-circle.png) ）以保存条件设置。

   - 完成后，单击&#x200B;**[!UICONTROL Save and Continue Edit]**。

     此规则行适用于匹配客户区段ID 2的所有客户。

   ![客户区段条件](./assets/customer-segment-matches.png){width="400"}

1. 向下滚动并展开![扩展选择器](../assets/icon-display-expand.png)的&#x200B;**[!UICONTROL Conditions]**&#x200B;部分，并定义规则的操作。

   在此部分中，您可以定义要用于首次客户的折扣类型和折扣值/金额。 此示例为所有满足定义的条件的客户定义了10%的折扣。 有关其他可用选项的信息，请参阅[创建购物车价格规则](price-rules-cart-create.md)。

   - 对于&#x200B;**[!UICONTROL Apply]**，选择产品价格折扣的百分比。

   - 对于&#x200B;**[!UICONTROL Discount Amount]**，输入`10`。

   - 若要将此价格规则仅应用于产品金额，请将&#x200B;**[!UICONTROL Apply to Shipping Amount]**&#x200B;设置为`No`。

   - 要阻止系统将多个价格规则应用于同一产品，请将&#x200B;**[!UICONTROL Discard Subsequent Rules]**&#x200B;设置为`Yes`。

   - 完成后，单击&#x200B;**[!UICONTROL Save]**。

   ![购物车价格规则操作](./assets/actions-first-time.png){width="600" zoomable="yes"}

新规则通常在一小时内可用。 测试规则以确保它按您定义的规则工作。

## 步骤3：保存并测试规则

{{new-price-rule}}

1. 规则完成后，单击&#x200B;**[!UICONTROL Save Rule]**。

1. 测试规则以确保其正常工作。

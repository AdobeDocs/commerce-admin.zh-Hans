---
title: 返回属性
description: 了解退货属性以及如何创建处理商店中的退货所需的属性。
exl-id: 639c1e94-1211-4a4e-8599-e54ed99b2355
feature: Attributes, Returns
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 0%

---

# 返回属性

{{ee-feature}}

退货属性用于存储产品退货过程中所需的信息。 默认属性包括返回产品的条件、返回原因以及指示如何解决返回的字段。 创建退货属性的过程与创建退货属性的过程类似 [客户属性](../customers/attribute-properties.md).

![管理员 — 返回属性](./assets/attribute-returns.png){width="700" zoomable="yes"}

## 创建退货属性

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Returns]**.

1. 在右上角，单击 **[!UICONTROL Add New Attribute]**.

   ![新返回 — 属性属性](./assets/attribute-returns-new-properties.png){width="600" zoomable="yes"}

### 定义属性

1. 要在输入数据时标识属性，请设置 **[!UICONTROL Default Label]**.

1. 对象 **[!UICONTROL Attribute Code]**，输入在系统中标识属性的代码。

1. 要确定用于数据输入的输入控件的类型，请设置 **[!UICONTROL Input Type]** 更改为以下任一项：

   - `Text Field`
   - `Text Area`
   - `Dropdown`
   - `Yes/No`
   - `File`
   - `Image File`

1. 要使字段成为必需项，请设置 **[!UICONTROL Values Required]** 到 `Yes`.

1. 要为字段分配初始值，请输入 **[!UICONTROL Default Value]**.

1. 要在保存记录之前验证输入到字段中的数据是否准确，请设置 **[!UICONTROL Input Validation]** 更改为以下任一项：

   - `None`
   - `Alphanumeric`
   - `Alphanumeric with Space`
   - `Numeric Only`
   - `Alpha Only`
   - `URL`
   - `Email`

1. 对于 `Text Field` 和 `Text Area` 输入类型，输入 **[!UICONTROL Minimum Text Length]** 和 **[!UICONTROL Maximum Text Length]**.

1. 要应用预处理过滤器，请设置 **[!UICONTROL Input/Output Filter]** 更改为以下任一项：

   - `None`
   - `Strip HTML Tags`
   - `Escape  HTML Entities`

1. 要使客户能够看到属性，请设置 **[!UICONTROL Show on Storefront]** 到 `Yes` 在 _[!UICONTROL Storefront Properties]_部分。

1. （可选）对于 **[!UICONTROL Sort Order]**，输入一个数字以确定该属性在页面的同一部分中相对于其他属性的显示位置。 (`0` =第一个， `1` =秒， `2` =第三，依此类推。)

### 管理标签/选项

1. 在左侧面板中，选择 **[!UICONTROL Manage Labels/Options]**.

1. 在 **[!UICONTROL Manage Titles (Size, Color, etc.)]** 部分，输入每个商店视图的标签。

   ![管理标签](./assets/return-attributes.png){width="600" zoomable="yes"}

1. 如果 **[!UICONTROL Input Type]** 属性为 `Dropdown`，管理中的选项 **[!UICONTROL Manage Options (Values of Your Attribute)]** 部分。

   - 要添加选项，请单击 **[!UICONTROL Add Option]** 并输入管理员和每个商店视图的标签。
   - 要将某个选项设为缺省选项，请选择 **[!UICONTROL Is Default]**.
   - 要删除选项，请单击 **[!UICONTROL Delete]**.

1. 要保存更改，请单击 **[!UICONTROL Save Attribute]**.

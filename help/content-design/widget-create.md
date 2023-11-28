---
title: 创建和管理构件
description: 了解如何创建和管理用于在您的商店中自动更新内容的构件。
exl-id: 680f2f41-ec51-4ac6-9e92-2817591af3e6
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '550'
ht-degree: 1%

---

# 创建和管理构件

构件是可重用的组件。 您可以轻松地创建并修改现有构件，以自动更新整个存储区的内容。 您还可以删除不再使用的构件。

![小组件](./assets/widgets.png){width="700" zoomable="yes"}

## 创建构件

每个小组件的创建过程几乎相同 [构件类型](widgets.md#widget-types). 您可以按照说明的第一部分操作，然后为所需的特定类型构件完成最后一部分。

### 第1步：选择类型

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. 单击 **[!UICONTROL Add Widget]**.

1. 在 _[!UICONTROL Settings]_部分：

   - 设置 **[!UICONTROL Type]** 到要创建的构件类型。

   - 验证 **[!UICONTROL Design Theme]** 设置为当前主题。

     ![构件设置](./assets/widget-settings.png){width="600" zoomable="yes"}

1. 单击 **[!UICONTROL Continue]**.

### 第2步：指定店面属性和布局

1. 在 _[!UICONTROL Storefront Properties]_部分：

   - 对象 **[!UICONTROL Widget Title]**，为构件输入描述性标题。

     此标题仅从管理员中可见。

   - 对象 **[!UICONTROL Assign to Store Views]**，选择您希望构件可见的存储区视图。

     您可以选择特定的商店视图，或者 `All Store Views`. 要选择多个视图，请按住Ctrl键(PC)或Command键(Mac)并单击每个选项。

   - （可选）对于 **[!UICONTROL Sort Order]**，请输入一个数字以确定此项目在页面同一部分中与其他项目一起显示的顺序。 (`0` =第一个， `1` =秒， `3` =第三，依此类推。)

     ![店面属性](./assets/widget-storefront-properties.png){width="600" zoomable="yes"}

1. 在 _[!UICONTROL Layout Updates]_部分，单击&#x200B;**[!UICONTROL Add Layout Update]**.

1. 设置 **[!UICONTROL Display On]** 到要在其中显示的页面类型。

1. 在 **[!UICONTROL Container]** 列表，选择要放置它的页面布局区域。

   ![布局更新](./assets/widget-layout-update-home-page.png){width="600" zoomable="yes"}

1. 如果小组件是链接，则设置 **[!UICONTROL Template]** 更改为以下任一项：

   - `Block Template`  — 设置内容格式，以便将其作为页面上的独立单元放置。
   - `Inline Template`  — 设置内容格式，以使其可置于其他内容中。 例如，进入文本段落的链接。

### 第3步：完成构件选项

每种构件类型的选项略有不同，但过程基本相同。 以下示例显示具有分页控件的特定类别的产品列表。

1. 在左侧面板中，选择 **[!UICONTROL Widget Options]**.

1. 单击 **[!UICONTROL Select Block]**.

1. 输入 **[!UICONTROL Title]** 显示在列表上方，例如 `Featured Products`.

1. 对于分页控件，请设置 **[!UICONTROL Display Page Control]** 到 `Yes`  并执行以下操作：

   - 输入 **[!UICONTROL Number of Products per Page]**.

   - 输入总计 **[!UICONTROL Number of Products to Display]**.

   - 设置 **[!UICONTROL Condition]** 到要推荐的产品类别。

     该过程与设置条件的过程相同 [价格规则](../merchandising-promotions/price-rules-catalog.md).

### 第4步：保存并检查结果

1. 完成后，单击 **[!UICONTROL Save]**.

1. 出现提示时，按照工作区顶部的说明根据需要更新缓存。

1. 返回到店面以验证构件是否正常工作。

   要将其移动到其他位置，可以重新打开构件并尝试使用其他页面或块引用。

## 构件创建演示

要了解如何创建构件，请观看此视频：

>[!VIDEO](https://video.tv.adobe.com/v/343786?quality=12)

## 编辑构件

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. 使用网格上方的筛选器找到构件，然后单击构件名称。

1. 进行所需的更改。

   有关构件选项的信息，请查看创建构件的步骤。

1. 单击 **[!UICONTROL Save]**.

## 删除构件

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. 使用网格上方的筛选器找到构件，然后选中要删除的构件的复选框。

1. 在列表的左上角，设置 **[!UICONTROL Actions]** 到 `Delete`.

1. 完成后，单击 **[!UICONTROL Submit]**.

1. 要确认操作，请单击 **[!UICONTROL OK]**.

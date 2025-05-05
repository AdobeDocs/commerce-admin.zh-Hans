---
title: 创建和管理构件
description: 了解如何创建和管理用于在您的商店中自动更新内容的构件。
exl-id: 680f2f41-ec51-4ac6-9e92-2817591af3e6
source-git-commit: 7288a4f47940e07c4d083826532308228d271c5e
workflow-type: tm+mt
source-wordcount: '554'
ht-degree: 0%

---

# 创建和管理构件

构件是可重用的组件。 您可以轻松地创建并修改现有构件，以自动更新整个存储区的内容。 您还可以删除不再使用的构件。

![小组件](./assets/widgets.png){width="700" zoomable="yes"}

## 创建构件

对于每个[构件类型](widgets.md#widget-types)，创建构件的过程几乎相同。 您可以按照说明的第一部分操作，然后为所需的特定类型构件完成最后一部分。

### 第1步：选择类型

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**。

1. 单击&#x200B;**[!UICONTROL Add Widget]**。

1. 在&#x200B;_[!UICONTROL Settings]_&#x200B;部分中：

   - 将&#x200B;**[!UICONTROL Type]**&#x200B;设置为要创建的构件类型。

   - 验证&#x200B;**[!UICONTROL Design Theme]**&#x200B;是否设置为当前主题。

     ![小组件设置](./assets/widget-settings.png){width="600" zoomable="yes"}

1. 单击&#x200B;**[!UICONTROL Continue]**。

### 第2步：指定店面属性和布局

1. 在&#x200B;_[!UICONTROL Storefront Properties]_&#x200B;部分中：

   - 对于&#x200B;**[!UICONTROL Widget Title]**，输入小部件的描述性标题。

     此标题仅从管理员中可见。

   - 对于&#x200B;**[!UICONTROL Assign to Store Views]**，选择您希望小组件可见的存储区视图。

     您可以选择特定的商店视图，或`All Store Views`。 要选择多个视图，请按住Ctrl键(PC)或Command键(Mac)并单击每个选项。

   - （可选）为&#x200B;**[!UICONTROL Sort Order]**&#x200B;输入一个数字，以确定该项在页面的同一部分中与其他项一起出现的顺序。 （`0` =第一，`1` =第二，`3` =第三，依此类推。）

     ![店面属性](./assets/widget-storefront-properties.png){width="600" zoomable="yes"}

1. 在&#x200B;_[!UICONTROL Layout Updates]_&#x200B;部分中，单击&#x200B;**[!UICONTROL Add Layout Update]**。

1. 将&#x200B;**[!UICONTROL Display On]**&#x200B;设置为要显示的页面类型。

1. 在&#x200B;**[!UICONTROL Container]**&#x200B;列表中，选择要放置它的页面布局区域。

   ![布局更新](./assets/widget-layout-update-home-page.png){width="600" zoomable="yes"}

1. 如果小组件是链接，请将&#x200B;**[!UICONTROL Template]**&#x200B;设置为以下项之一：

   - `Block Template` — 设置内容格式，以便将其作为页面上的独立单元放置。
   - `Inline Template` — 格式化内容，以便将其置于其他内容中。 例如，进入文本段落的链接。

### 第3步：完成构件选项

每种构件类型的选项略有不同，但过程基本相同。 以下示例显示具有分页控件的特定类别的产品列表。

1. 在左侧面板中，选择&#x200B;**[!UICONTROL Widget Options]**。

1. 单击&#x200B;**[!UICONTROL Select Block]**。

1. 输入要在列表上方显示的&#x200B;**[!UICONTROL Title]**，如`Featured Products`。

1. 对于分页控件，请将&#x200B;**[!UICONTROL Display Page Control]**&#x200B;设置为`Yes`并执行以下操作：

   - 输入&#x200B;**[!UICONTROL Number of Products per Page]**。

   - 输入总计&#x200B;**[!UICONTROL Number of Products to Display]**。

   - 将&#x200B;**[!UICONTROL Condition]**&#x200B;设置为要支持的产品类别。

     此过程与为[价格规则](../merchandising-promotions/price-rules-catalog.md)设置条件相同。

### 第4步：保存并检查结果

1. 完成后，单击&#x200B;**[!UICONTROL Save]**。

1. 出现提示时，按照工作区顶部的说明根据需要更新缓存。

1. 返回到店面以验证构件是否正常工作。

   要将其移动到其他位置，可以重新打开构件并尝试使用其他页面或块引用。

## 构件创建演示

要了解如何创建构件，请观看此视频：

>[!VIDEO](https://video.tv.adobe.com/v/343786?quality=12&learn=on)

## 编辑构件

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**。

1. 使用网格上方的筛选器找到构件，然后单击构件名称。

1. 进行所需的更改。

   有关构件选项的信息，请查看创建构件的步骤。

1. 单击&#x200B;**[!UICONTROL Save]**。

## 删除构件

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**。

1. 使用网格上方的筛选器找到构件，然后选中要删除的构件的复选框。

1. 在列表的左上角，将&#x200B;**[!UICONTROL Actions]**&#x200B;设置为`Delete`。

1. 完成后，单击&#x200B;**[!UICONTROL Submit]**。

1. 要确认操作，请单击&#x200B;**[!UICONTROL OK]**。

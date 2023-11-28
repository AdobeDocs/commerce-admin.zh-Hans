---
title: 操作控制
description: 了解如何使用Actions控件将操作应用于Admin中的一个或多个记录。
exl-id: 03f313a9-bc17-4151-a2c8-8906342f025d
source-git-commit: a3fb702d0b6e08c3aaaa0d6b5e07aa825026ef76
workflow-type: tm+mt
source-wordcount: '428'
ht-degree: 0%

---

# 操作控制

在网格中处理记录集合时，可以使用“操作”控件将操作应用到一个或多个记录。 Actions控件列出了可用于特定类型数据的每个操作。 例如，您可以使用“操作”控件更新所选产品的属性，以更改以下项的状态： `Disabled` 到 `Enabled`，或从数据库中删除记录。

您可以进行所需数量的更改，然后在单一步骤中更新记录。 它比单独更改每个产品的设置要高效得多。 将编辑应用到记录批次是一项异步操作，它将在后台执行，这样您就可以继续在Admin中工作，而无需等待操作完成。 任务完成后，系统将显示一条消息。

可用操作的选择因列表而异，并且可能会显示其他选项，具体取决于所选的操作。 例如，在更改一组记录的状态时， _[!UICONTROL Status]_框出现在“操作”控件旁边，其中包含其他选项。

## 第1步：选择记录

列表第一列中的复选框标识作为操作目标的每个记录。 此 [筛选器控件](admin-grid-controls.md) 可用于将列表缩小到要为该操作定位的记录。

1. 如果需要，请在每列的顶部设置过滤器，以仅显示要包含的记录。

1. 选中作为操作目标的每个记录的复选框，或使用列选择器来选择批量选择。

![选择或取消选择页面上的所有或所有内容](./assets/action-change-selection.png){width="500"}

## 第2步：将操作应用于选定记录

1. 设置 **[!UICONTROL Actions]** 控制要应用的操作。

   **_示例：_** 更新属性

   - 在列表中，选中要更新的每个记录的复选框。

   - 设置 **[!UICONTROL Actions]** 控制对象 `Update Attributes`.

     ![选择“更新属性”操作](./assets/action-select.png){width="450"}

   - 单击 **[!UICONTROL Submit]**.

     “更新属性”页面列出了所有可用的属性，按左侧面板中的组进行整理。

     ![“更新属性”页](./assets/action-update-attributes.png){width="700" zoomable="yes"}

   - 选择 **[!UICONTROL Change]** 复选框，并进行必要的更改。

   - 单击 **[!UICONTROL Save]** 更新选定记录组的属性。

1. 完成后，单击 **[!UICONTROL Submit]**.

## 复选框操作

| 操作 | 描述 |
|--- |--- |
| [!UICONTROL Select All] | 选中列表中所有记录的复选框。 |
| [!UICONTROL Unselect All] | 清除列表中所有记录的复选框。 |
| [!UICONTROL Select All on This Page] | 选中当前页面上显示的记录复选框。 |
| [!UICONTROL Deselect All on This Page] | 清除当前页面上显示的记录复选框。 |

{style="table-layout:auto"}

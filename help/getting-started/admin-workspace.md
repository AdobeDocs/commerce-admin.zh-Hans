---
title: 管理工具和工作区
description: 了解管理员工作区，该工作区提供对用于运行商店的所有工具、数据和内容的访问权限。
exl-id: 61cc53ab-e1c5-4349-b306-a15eb7c5ab57
source-git-commit: 7b6d70e2f3052af69075790cec1f396e2505bf8b
workflow-type: tm+mt
source-wordcount: '528'
ht-degree: 0%

---

# 管理工具和工作区

管理工作区允许访问用于运行存储的所有工具、数据和内容。 可以在配置中设置默认启动页面。 许多“管理员”页面都有一个网格，其中列出了该部分的数据，并包含一组用于搜索、排序、筛选、选择和应用操作的工具。 默认情况下，[仪表板](admin-dashboard.md)是管理员的启动页面。 但是，您可以选择在登录时作为启动页面显示的任何其他页面。 您可以单击管理员侧边栏中的徽标以返回管理员启动页面。

![管理员 — 工作区](./assets/admin-workspace.png){zoomable="yes"}

## Workspace控件

| 控件 | 描述 |
|--- |--- |
| [!UICONTROL Global Search] | 可使用右上角的搜索图标来查找数据库中的任何值，包括产品、客户和订单记录。 |
| [!UICONTROL Grid Search] | 网格上方的搜索框可用于根据在记录中找到的关键字快速筛选网格显示。 |
| [!UICONTROL Sort] | 每列的标题可用于按升序或降序对列表进行排序。 |
| [!UICONTROL Filters] | 定义一组搜索参数，这些参数可确定网格中显示的记录。 此外，某些列标题中的过滤器可用于将列表限制为特定值。 某些过滤器具有可从列表框中选择的其他选项。 |
| [!UICONTROL Default View] | 确定网格的默认列布局。 |
| [!UICONTROL Columns] | 确定网格中[列](admin-grid-controls.md)的选择及其顺序。 列布局可更改并另存为&#x200B;_视图_。 默认情况下，网格中只包含某些列。 |
| [!UICONTROL Paginate] | 分页控件用于查看结果的其他页面。 |
| [!UICONTROL Actions] | “操作”控件将操作应用于所有选定的记录。 |
| [!UICONTROL Select] | Select控件用于选择要作为操作目标的多个记录。 选项： `Select All` / `Deselect All` |

{style="table-layout:auto"}

## Workspace搜索

要在数据库中查找任何记录，请使用&#x200B;_Admin_&#x200B;标题中的放大镜图标。 结果可以包括客户、产品、订单或任何相关属性。 例如，如果输入客户名称，结果可能包括客户记录以及与名称关联的任何订单。

![管理员搜索工具](./assets/admin-search.png){width="700" zoomable="yes"}

1. 在标题中，单击&#x200B;_搜索_ （![放大镜](../assets/icon-magnify-search.png)）图标以打开搜索框。

1. 执行以下操作之一：

   - 要查找最接近的匹配项，请输入要查找内容的前几个字母。
   - 要查找完全匹配的单词，请输入要查找的一个或多个单词。

1. 在显示的搜索结果中，单击任意项目以打开记录。

## 更改管理员启动页面

[仪表板](admin-workspace.md#the-dashboard)是管理员的默认启动页面，但您可以配置其他启动页面。

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧导航面板中的&#x200B;**[!UICONTROL Advanced]**&#x200B;下，选择&#x200B;**[!UICONTROL Admin]**。

1. 展开&#x200B;**[!UICONTROL Startup Page]**&#x200B;部分的![扩展选择器](../assets/icon-display-expand.png)。

   ![高级配置 — 管理员启动页面设置](./assets/admin-startup-page.png){width="600"}

1. 将&#x200B;**[!UICONTROL Startup Page]**&#x200B;设置为您登录管理员后希望首先显示的页面。

   有关所有管理员选项的详细列表，请参阅&#x200B;_配置引用_&#x200B;中的[管理员](../configuration-reference/advanced/admin.md)。

1. 完成后，单击&#x200B;**[!UICONTROL Save Config]**。

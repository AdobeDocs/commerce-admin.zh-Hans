---
title: 操作日志报告
description: 了解如何查看、筛选和导出操作日志报告，该报告提供了所有启用日志的管理员操作的详细记录。
exl-id: f2be5852-9185-4f14-b0bb-44d779b40819
feature: Logs, Data Import/Export
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '438'
ht-degree: 0%

---

# 操作日志报告

{{ee-feature}}

此 _操作日志_ 报告显示启用日志记录的所有管理员操作的详细记录。 每个记录都带有时间戳，并记录IP地址和用户名称。 日志详细信息包括管理员用户数据以及在操作期间所做的相关更改。

您要在报告中显示的操作必须在以下位置启用： [管理员操作日志记录](action-log.md) 商店设置中的屏幕。 如果勾选（启用）了操作类型，则这些类型的管理员操作将显示在操作日志报表中。

可以使用每列中的选项过滤报告。 您可以设置单个筛选器选项或为多个列设置筛选器选项，以缩小报告范围并列出特定操作。 您还可以以CSV或Excel XML格式导出报表数据。

操作日志报表包含以下信息：

- **[!UICONTROL Time]**  — 操作发生的日期和时间
- **[!UICONTROL Action Group]**  — 显示操作类型，与上启用的操作相关联 _管理员操作日志记录_ 商店设置中的屏幕
- **[!UICONTROL Action]**  — 显示已记录的操作
- **[!UICONTROL IP Address]**  — 显示执行操作的计算机的IP地址
- **[!UICONTROL Username]**  — 显示执行操作的用户的登录ID
- **[!UICONTROL Result]**  — 显示用户操作的成功或失败
- **[!UICONTROL Full Action Name]**  — 显示后端操作名称
- **[!UICONTROL Details]**  — 显示后端操作类别
- **[!UICONTROL Full Details]**  — 显示管理员操作的所有已记录详细信息

## 查看操作日志报告

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL System]** > _[!UICONTROL Actions Logs]_>**[!UICONTROL Report]**.

   ![操作日志](./assets/action-log-report.png){width="600" zoomable="yes"}

1. 要查看列出的管理员操作的完整详细信息，请单击 **[!UICONTROL View]**.

   ![操作日志条目详细信息](./assets/action-log-report-view.png){width="600" zoomable="yes"}

## 筛选操作日志报告

您可以定义过滤器选项字段，然后单击 **[!UICONTROL Search]** 以缩小显示的操作范围。

要清除筛选器选项并返回完整报表，请单击 **[!UICONTROL Reset Filter]**.

![操作日志报告过滤器](./assets/action-log-report-filters.png){width="600" zoomable="yes"}

| 字段 | 描述 |
|--- |--- |
| [!UICONTROL Time] | 在 **[!UICONTROL From]**，单击以从动态日历中选择一个日期来定义过滤器的开始日期。 在 **[!UICONTROL To]**，单击以选择日期来定义过滤器的结束日期。 |
| [!UICONTROL Action Group] | 选择操作组。 |
| [!UICONTROL Action] | 选择操作。 |
| [!UICONTROL IP Address] | 输入用于操作的计算机的IP地址。 |
| [!UICONTROL Username] | 选择用户名。 默认为 `All Users`. |
| [!UICONTROL Result] | 选择“成功”或“失败”。 |
| [!UICONTROL Full Action Name] | 在字段中输入要匹配的搜索文本。 |
| [!UICONTROL Details] | 在字段中输入要匹配的搜索文本。 |

{style="table-layout:auto"}

## 导出操作日志报告

1. 对象 **[!UICONTROL Export to]**，选择导出格式：

   - `CSV`  — 包含纯文本数据的逗号分隔值文件
   - `Excel XML`  — 基于XML的电子表格数据格式

1. 单击 **[!UICONTROL Export]**.

   生成的文件会自动保存到指定的文件夹以供下载。

   ![操作日志报告导出](./assets/action-log-report-export.png){width="200"}

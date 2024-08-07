---
title: 操作日志
description: 了解操作日志以及如何配置记录的操作以帮助您跟踪对存储所做的所有更改。
exl-id: a482adfe-a63f-428b-b078-7542a1e2ecee
feature: Logs, Configuration
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 0%

---

# 操作日志

{{ee-feature}}

操作日志功能会记录（记录）在您的商店中工作的管理员用户所做的每项更改。 这样，您就可以跟踪对存储所做的所有更改。 跟踪这些更改，并为用户设置[管理员权限](permissions.md)，有助于保护您的存储免受不需要的更改。

对于大多数管理员操作，记录的信息包括操作、用户名、操作成功或失败以及受操作影响的对象的ID。 还会记录IP地址和日期。

默认情况下，将启用并记录所有管理员操作。 要配置管理员操作日志记录，请查看各个选项，然后选中或清除每个操作类型的复选框。 Adobe Commerce仅记录勾选类型。

查看[操作日志报告](action-log-report.md)以查看已记录的管理员操作和详细信息。

![高级配置 — 管理员操作日志记录](../configuration-reference/advanced/assets/admin-actions-logging.png){width="600" zoomable="yes"}

有关配置设置的详细列表，请参阅&#x200B;_配置引用_&#x200B;中的[管理操作日志存档](../configuration-reference/advanced/system.md)。

## 配置用于日志记录的管理操作

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧面板中，展开&#x200B;**[!UICONTROL Advanced]**&#x200B;并选择&#x200B;**[!UICONTROL Admin]**。

1. 展开&#x200B;**[!UICONTROL Admin Actions Logging]**&#x200B;部分中的![扩展选择器](../assets/icon-display-expand.png)并对每个操作执行以下操作：

   - 要为操作启用管理员日志记录，请选中复选框。
   - 要禁用操作的管理员日志记录，请清除复选框。

1. 完成后，单击&#x200B;**[!UICONTROL Save Config]**。

## 存档管理操作日志

管理员操作日志可以存档任意天数。 存档也可以在指定的持续时间后删除。

1. 在左侧面板中，展开&#x200B;**[!UICONTROL Advanced]**&#x200B;并选择&#x200B;**[!UICONTROL System]**。

1. 展开&#x200B;**[!UICONTROL Admin Action Log Archiving]**&#x200B;并设置选项：

   - **[!UICONTROL Logs Entry Lifetime, Days]** — 设置保留存档日志的天数。
   - **[!UICONTROL Log Archiving Frequency]** — 设置创建存档的频率。

1. 完成后，单击&#x200B;**[!UICONTROL Save Config]**。

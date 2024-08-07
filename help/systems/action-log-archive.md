---
title: 操作日志存档
description: 了解如何配置和查看管理员操作日志存档。
exl-id: a839f1c6-b5e2-4881-bfaa-267e47585441
feature: Logs, Configuration
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 0%

---

# 操作日志存档

{{ee-feature}}

管理员[操作](action-log.md)存档列出了服务器上存储的CSV日志文件。 在配置中，您可以指定日志条目的存储时间以及归档频率。 缺省情况下，文件名包括ISO格式的当前日期：  `yyyyMMddHH`

>[!NOTE]
>
>日志存档需要设置[cron作业](cron.md)。

## 配置日志存档

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧面板中，展开&#x200B;**[!UICONTROL Advanced]**&#x200B;并选择&#x200B;**[!UICONTROL System]**。

1. 展开![扩展选择器](../assets/icon-display-expand.png) **[!UICONTROL Admin Actions Log Archiving]**&#x200B;部分并设置以下选项：

   - **[!UICONTROL Log Entry Lifetime, Days]** — 输入删除日志条目之前要在数据库中保留的天数。
   - **[!UICONTROL Log Archiving Frequency]** — 设置为`Daily`、`Weekly`或`Monthly`。

   ![高级配置 — 管理员操作日志存档](../configuration-reference/advanced/assets/system-admin-actions-log-archiving.png){width="600" zoomable="yes"}

   有关配置设置的详细列表，请参阅&#x200B;_配置引用_&#x200B;中的[管理操作日志存档](../configuration-reference/advanced/system.md)。

1. 完成后，单击&#x200B;**[!UICONTROL Save Config]**。

## 查看存档

在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL System]** > _[!UICONTROL Actions Logs]_>**[!UICONTROL Archive]**。

![操作日志存档](./assets/action-log-archive.png){width="600" zoomable="yes"}

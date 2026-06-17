---
title: 操作日志存档
description: 了解如何配置和查看管理员操作日志存档。
exl-id: a839f1c6-b5e2-4881-bfaa-267e47585441
feature: Logs, Configuration
TQID: https://experienceleague.adobe.com/xgyeoO5XJFZPopM9bsIn2oOtrxl4fyuEY2du5ryXeTY
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 160
ht-degree: 0%

---

# 操作日志存档

{{ee-feature}}

管理员[操作](action-log.md)存档列出了服务器上存储的CSV日志文件。 在配置中，您可以指定日志条目的存储时间以及归档频率。 默认情况下，文件名包含ISO格式的当前日期： `yyyyMMddHH`

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

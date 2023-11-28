---
title: 系统备份
description: 了解如何创建和计划系统备份，包括文件系统、数据库和媒体文件。
exl-id: 3a9655c1-c124-42be-a487-b31404dada90
feature: System, Configuration
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 0%

---

# 系统备份

Adobe Commerce和Magento Open Source让您能够备份系统的各个部分（如文件系统、数据库和介质文件），并自动回滚。 每个备份的记录都显示在上的网格中。 _备份_ 页面。 从列表中删除记录也会删除存档的文件。 数据库备份文件使用GZ格式进行压缩。 对于系统备份、数据库和介质备份，使用TGZ格式。 作为最佳实践，您应限制对备份工具的访问，并在安装扩展和更新之前进行备份。

- **限制对备份工具的访问。** 可以通过配置来限制对备份和回滚管理工具的访问 [用户角色](permissions-user-roles.md) 用于备份和回滚资源。 要限制访问，请取消选中相应的复选框。 要授予回滚资源的访问权限，您还必须授予对备份资源的访问权限。

- **在安装扩展和更新之前进行备份。** 安装扩展或更新之前，请始终执行备份。

{{$include /help/_includes/backups-note.md}}

## 启用和计划备份

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中，展开 **[!UICONTROL Advanced]** 并选择 **[!UICONTROL System]**.

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Backup Settings]**.

1. 设置 **[!UICONTROL Enabled Schedule Backup]** 到 `Yes`.

1. 要计划自动生成，请设置计划选项：

   - 设置 **[!UICONTROL Enabled Schedule Backup]** 到 `Yes`.
   - 设置 **[!UICONTROL Scheduled Backup Type]** 按计划间隔运行的备份类型。
   - 设置 **[!UICONTROL Start Time]** 到运行备份操作的时间。
   - 设置 **[!UICONTROL Frequency]** 到 `Daily`， `Weekly`，或 `Monthly`.
   - 设置 **[!UICONTROL Maintenance Mode]** 到 `Yes`.

   ![高级配置 — 备份](../configuration-reference/advanced/assets/system-scheduled-backup-settings.png){width="600" zoomable="yes"}

1. 完成后，单击 **[!UICONTROL Save Config]**.

## 创建备份

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Backups]**.

1. 单击右上角的要创建的备份类型：

   - **[!UICONTROL System Backup]**  — 创建数据库和文件系统的完整备份。 在此过程中，您可以选择在备份中包含介质文件夹。

   - **[!UICONTROL Database and Media Backup]**  — 创建数据库和介质文件夹的备份。

   - **[!UICONTROL Database Backup]**  — 创建数据库的备份。

   ![系统工具 — 备份](./assets/tools-backups.png){width="600" zoomable="yes"}

1. 要在备份期间将存储置于维护模式，请选中复选框。

   备份完成后，维护模式会自动关闭。

1. 对于系统备份，选择 **[!UICONTROL Include Media folder to System Backup]** 用于包含媒体文件夹的复选框。

1. 出现提示时，确认操作。



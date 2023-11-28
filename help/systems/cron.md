---
title: Cron（计划任务）
description: 了解如何从管理员那里控制Commerce cron作业的执行和计划。
exl-id: e0da08ab-212f-4977-9387-0b4b40560cfb
feature: System, Configuration
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '417'
ht-degree: 0%

---

# Cron（计划任务）

Adobe Commerce和Magento Open Source通过定期运行脚本来按计划执行某些操作。 您可以从管理员控制Commerce cron作业的执行和计划。 根据CRON计划运行的存储操作包括但不限于：

- [电子邮件](email-communications.md)
- [目录价格规则](../merchandising-promotions/price-rules-catalog.md)
- [快讯](../merchandising-promotions/newsletters.md)
- [XML站点地图生成](../merchandising-promotions/sitemap-xml.md)
- [汇率更新](../stores-purchase/currency-update.md)
- [Inventory management](../inventory-management/introduction.md)

>[!IMPORTANT]
>
>Commerce服务必须安装在crontab中，以确保核心组件以及一些第三方扩展按预期工作。 请参阅 [中的说明 _安装指南_](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/next-steps/configuration.html) 有关将服务安装到crontab的详细信息。

此外，您还可以将以下内容配置为根据cron计划运行：

- 订购系统网格更新并重新编制索引
- 待定付款期限

确保 [基本URL](../stores-purchase/store-urls.md) 正确设置了存储的，以便在cron操作期间生成的URL正确无误。 有关云基础架构上的Adobe Commerce，请参阅 [设置cron作业](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/app/properties/crons-property.html) 在 _云基础架构上的Commerce指南_. 有关内部部署，请参阅 [配置和运行图标](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html) 在 _配置指南_.

## 配置cron

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中，展开 **[!UICONTROL Advanced]** 并选择 **[!UICONTROL System]**.

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Cron]** 部分。

   ![高级配置 — cron任务](../configuration-reference/advanced/assets/system-cron.png){width="600" zoomable="yes"}

1. 完成以下设置 **[!UICONTROL Index]** 和 **[!UICONTROL Default]** 组。

   每个部分中的设置相同。

   - **[!UICONTROL Generate Schedules Every]**  — 定义计划的生成频率（以分钟为单位）。 调度存储在数据库中。
   - **[!UICONTROL Schedule Ahead for]**  — 定义cron作业计划的提前时间（分钟）。 例如，如果将此设置设为 `10` cron运行， cron作业计划在接下来的10分钟内运行。
   - **[!UICONTROL Missed if not Run Within]**  — 定义用于确定错过的作业的时间（以分钟为单位）。 如果cron作业未在其计划时间运行，并且指定的时间已过，则无法运行该作业，其状态将设置为 `Missed`.
   - **[!UICONTROL History Cleanup Every]**  — 定义从数据库中清除已结束任务历史的时间（以分钟为单位）。
   - **[!UICONTROL Success History Lifetime]**  — 定义具有的cron作业的历史记录的时间长度（以分钟为单位） `Successful` 状态仍保留在数据库中。
   - **[!UICONTROL Failure History Lifetime]**  — 定义具有的cron作业的历史记录的时间长度（以分钟为单位） `Error` 状态仍保留在数据库中。
   - **[!UICONTROL Use Separate Process]**  — 定义是否所有来自组的cron作业都在单独的系统进程中运行。 选项： `Yes` / `No`

   ![高级配置 — cron组索引](../configuration-reference/advanced/assets/system-cron-group-index.png){width="600" zoomable="yes"}

1. 完成后，单击 **[!UICONTROL Save Config]**.

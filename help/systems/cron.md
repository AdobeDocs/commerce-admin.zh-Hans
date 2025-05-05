---
title: Cron（计划任务）
description: 了解如何从管理员那里控制Commerce cron作业的执行和计划。
exl-id: e0da08ab-212f-4977-9387-0b4b40560cfb
feature: System, Configuration
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '398'
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
>Commerce服务必须安装在crontab中，以确保核心组件和某些第三方扩展按预期工作。 有关将服务安装到crontab的详细信息，请参阅&#x200B;_安装指南_[&#128279;](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/next-steps/configuration.html?lang=zh-Hans)中的说明。

此外，您还可以将以下内容配置为根据cron计划运行：

- 订购系统网格更新并重新编制索引
- 待定付款期限

请确保存储的[基本URL](../stores-purchase/store-urls.md)设置正确，以便cron操作期间生成的URL正确无误。 有关云基础架构上的Adobe Commerce，请参阅《云基础架构上的Commerce指南》_中的[设置cron作业](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/app/properties/crons-property.html?lang=zh-Hans)_。 有关内部部署，请参阅&#x200B;_配置指南_&#x200B;中的[配置并运行con](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html?lang=zh-Hans)。

## 配置cron

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧面板中，展开&#x200B;**[!UICONTROL Advanced]**&#x200B;并选择&#x200B;**[!UICONTROL System]**。

1. 展开&#x200B;**[!UICONTROL Cron]**&#x200B;部分的![扩展选择器](../assets/icon-display-expand.png)。

   ![高级配置 — cron任务](../configuration-reference/advanced/assets/system-cron.png){width="600" zoomable="yes"}

1. 完成&#x200B;**[!UICONTROL Index]**&#x200B;和&#x200B;**[!UICONTROL Default]**&#x200B;组的以下设置。

   每个部分中的设置相同。

   - **[!UICONTROL Generate Schedules Every]** — 定义生成计划的频率（分钟）。 调度存储在数据库中。
   - **[!UICONTROL Schedule Ahead for]** — 定义预定cron作业的计划时间（以分钟为单位）。 例如，如果将此设置设为`10`且cron运行，则将cron作业安排在接下来的10分钟内。
   - **[!UICONTROL Missed if not Run Within]** — 定义用于确定错过的作业的时间（以分钟为单位）。 如果cron作业未在其计划时间运行且指定的时间已过，则无法运行该作业并将其状态设置为`Missed`。
   - **[!UICONTROL History Cleanup Every]** — 定义从数据库中清除已结束任务历史记录的时间（以分钟为单位）。
   - **[!UICONTROL Success History Lifetime]** — 定义状态为`Successful`的cron作业历史记录保留在数据库中的时间长度（以分钟为单位）。
   - **[!UICONTROL Failure History Lifetime]** — 定义状态为`Error`的cron作业历史记录保留在数据库中的时间长度（以分钟为单位）。
   - **[!UICONTROL Use Separate Process]** — 定义是否所有来自组的cron作业都在单独的系统进程中运行。 选项： `Yes` / `No`

   ![高级配置 — cron组索引](../configuration-reference/advanced/assets/system-cron-group-index.png){width="600" zoomable="yes"}

1. 完成后，单击&#x200B;**[!UICONTROL Save Config]**。

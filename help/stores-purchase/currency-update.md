---
title: 更新汇率
description: 了解如何手动设置汇率或将其导入您的商店。
exl-id: 316a7bc8-1118-46e7-82ff-891ada04cd13
feature: Currency, Configuration, Data Import/Export
TQID: https://experienceleague.adobe.com/tEt15Mzt7MeDtf6MZfu9n6EsvJKUCNBdGhUo0-RK3zk
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 275
ht-degree: 0%

---

# 更新汇率

可以手动设置汇率，也可以将汇率导入存储中。 为确保您的商店具有最新的汇率，您可以配置要自动计划的汇率。

在导入货币汇率之前，请完成[货币汇率设置](currency-configuration.md)以指定您接受的货币，并建立导入连接和计划。

![汇率](./assets/stores-currency-rate-update.png){width="600" zoomable="yes"}

## 手动更新汇率

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Currency]_>**[!UICONTROL Currency Rates]**。

1. 单击要更改的汇率，并为支持的每种货币输入新值。

1. 完成后，单击&#x200B;**[!UICONTROL Save Currency Rates]**。

## 导入汇率

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Currency]_>**[!UICONTROL Currency Rates]**。

1. 将&#x200B;**[!UICONTROL Import Service]**&#x200B;设置为货币汇率提供程序。

   默认提供程序为`fixer.io (legacy)`。

   >[!IMPORTANT]
   >
   >从2.4.6版本开始，[[!DNL Fixer.io]](https://fixer.io/)服务已弃用，并替换为[[!DNL Fixer API] (APILayer)](https://apilayer.com/marketplace/fixer-api)服务。 强烈建议您使用APILayer帐户，而不是已弃用的[!DNL Fixer.io]帐户。

1. 单击&#x200B;**[!UICONTROL Import]**。

   更新的费率显示在&#x200B;_[!UICONTROL Currency Rates]_&#x200B;列表中。 如果自上次更新以来费率已发生更改，则旧费率将显示在下方以供参考。

1. 完成后，单击&#x200B;**[!UICONTROL Save Currency Rates]**。

1. 提示更新缓存时，单击&#x200B;**[!UICONTROL Cache Management]**&#x200B;链接并刷新无效缓存。

   ![系统消息 — 刷新无效的缓存](./assets/currency-cache-update.png){width="600" zoomable="yes"}

## 按计划导入汇率

1. 确保为你的存储启用了[Cron](../systems/cron.md)。

1. 要指定您接受的货币并建立导入连接和计划，请完成[货币汇率设置](currency-configuration.md)。

1. 要验证费率是否按计划导入，请检查&#x200B;_[!UICONTROL Currency Rates]_&#x200B;列表。

1. 等待为计划建立的频率设置的时间段，然后再次检查速率。

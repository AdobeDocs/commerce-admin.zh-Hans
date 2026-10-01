---
title: '[!UICONTROL Services] &gt； ACO目录视图同步'
description: 查看Commerce管理员的[!UICONTROL Services] &gt； [!UICONTROL ACO Catalog View Sync]页面上的配置设置。
feature: Configuration, Security
badgePaas: label="仅限PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="仅适用于云项目（Adobe管理的PaaS基础架构）和内部部署项目上的Adobe Commerce 。"
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
    internal-label: Security
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 9ec73be87dd329dc04e7b133885fcc156f4ffcb6
workflow-type: tm+mt
source-wordcount: '304'
ht-degree: 3%
---
# [!UICONTROL Services] > [!UICONTROL ACO Catalog View Sync]

使用这些设置可控制[!DNL Adobe Commerce Optimizer Connector for B2B]如何将B2B共享目录配置（目录视图、策略、价格手册和密钥）同步到[!DNL Adobe Commerce Optimizer]，以及如何解决两个系统之间的配置差异。 请参阅[目录视图同步状态监视](../../systems/catalog-view-sync-status.md)以监视这些设置的结果。

{{config}}

## [!UICONTROL Deletion]

![删除](./assets/aco-catalog-view-sync-configuration.png)<!-- zoom -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
| --- | --- | --- |
| [!UICONTROL Deletion Grace Period (days)] | 全局 | 共享目录数据的保留期。 指定在硬删除之前保留已删除共享目录的目录视图、策略和元数据的天数。 该值默认为7天。 设置为`0`可立即硬删除。 |

{style="table-layout:auto"}

## [!UICONTROL Creation]

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
| --- | --- | --- |
| [!UICONTROL Creation Grace Period (days)] | 全局 | 新注册的目录视图可等待[!DNL Adobe Commerce Optimizer Connector for B2B]完成其目录视图、策略、价格手册和关键配置的首次同步的天数，而其状态报告为[!UICONTROL Pending]。 如果宽限期没有成功同步就失效，则状态将更改为[!UICONTROL Failed]。 默认值： `1` |

{style="table-layout:auto"}

## [!UICONTROL Drift Reconciler]

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
| --- | --- | --- |
| [!UICONTROL Enabled] | 全局 | 运行计划的漂移协调器以检测和报告从[!DNL Adobe Commerce]投影的目录视图与[!DNL Adobe Commerce Optimizer]中的目录视图配置之间的差异。 如果启用了`automatically repair drift`，它还将尝试修复任何可修复的差异。 |
| [!UICONTROL Automatically Repair Drift] | 全局 | 当设置为`Yes`时，计划的漂移协调器更新[!DNL Adobe Commerce Optimizer]配置以匹配[!DNL Adobe Commerce]并重新同步配置。 当设置为`No`时，该运行仅检测和报告漂移。 孤立的[!DNL Adobe Commerce Optimizer]实体始终报告，从不自动删除。 |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
> - [ACO目录视图](./aco-catalog-view.md) — 为目录视图的店面读取配置访问令牌
> - [目录视图同步状态监视](../../systems/catalog-view-sync-status.md) — 使用这些设置监视同步运行状况并协调偏移
> - [受限访问密钥管理](../../systems/restricted-access-keys.md) — 管理分配给同步目录视图的访问密钥

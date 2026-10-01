---
title: '[!UICONTROL Services] > [!UICONTROL ACO Restricted Access Keys]'
description: 查看Commerce管理员的[!UICONTROL Services] &gt； [!UICONTROL ACO Restricted Access Keys]页面上的配置设置。
feature: Configuration, Security
badgePaas: label="仅限PaaS" type="Informative" url="https://experienceleague.adobe.com/zh-hans/docs/commerce/user-guides/product-solutions" tooltip="仅适用于云项目（Adobe管理的PaaS基础架构）和内部部署项目上的Adobe Commerce 。"
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
source-wordcount: '182'
ht-degree: 4%
---
# [!UICONTROL Services] > [!UICONTROL ACO Restricted Access Keys]

使用此设置可控制[!DNL Adobe Commerce Optimizer Connector for B2B]应用于B2B共享目录视图设置的受限访问密钥的默认过期时间。 要创建、分配和删除这些密钥，请参阅[受限访问密钥管理](../../systems/restricted-access-keys.md)。

{{config}}

## [!UICONTROL Provisioning]

![正在设置](./assets/optimizer-restricted-access-key-config.png)<!-- zoom -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
| --- | --- | --- |
| [!UICONTROL Default key expiry (days)] | 全局 | 新配置的受限访问密钥的有效期。 [!DNL Adobe Commerce Optimizer]要求每个密钥在以后至少有一分钟的到期日期，并从网关读取中排除过期的密钥，因此始终应用至少一天的值。 默认值： `36500` |

{style="table-layout:auto"}

>[!NOTE]
>
>由于自动密钥轮换尚不可用，因此默认到期设置为较长的到期期。 请参阅[键选择和轮换](../../systems/restricted-access-keys.md#key-selection-and-rotation)。

>[!MORELIKETHIS]
>
> - [ACO目录视图](./aco-catalog-view.md) — 为目录视图配置店面访问令牌
> - [受限访问密钥管理](../../systems/restricted-access-keys.md) — 创建、分配和删除受限访问密钥
> - [目录视图同步状态监视](../../systems/catalog-view-sync-status.md) — 监视密钥即将过期

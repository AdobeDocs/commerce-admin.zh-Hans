---
title: '[!UICONTROL Services] &gt； ACO目录视图'
description: 在Adobe Commerce Optimizer管理员的[!UICONTROL Services] &gt； [!UICONTROL ACO Catalog View]页面上查看和更新Commerce配置设置。
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
source-git-commit: b32c28afffe75b3f684f0fef81bd61e9cdcb485a
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 3%
---
# [!UICONTROL Services] > [!UICONTROL ACO Catalog View]

使用这些设置控制[!DNL Adobe Commerce Optimizer Connector for B2B]颁发的访问令牌。 Storefront使用这些令牌对使用从管理员中配置的自定义共享目录同步的数据填充的Commerce Optimizer专用目录视图进行身份验证。

{{config}}

![Adobe Commerce管理员显示ACO目录视图访问令牌设置，已启用3,600秒TTL和令牌颁发。](./assets/aco-catalog-view-access-token-config.png)<!-- zoom -->

## [!UICONTROL Access Token Configuration]

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
| --- | --- | --- |
| [!UICONTROL Token TTL (seconds)] | 全局 | 访问令牌在生成后保持有效的秒数。 在默认范围内，此设置是只读的。 忽略在网站或商店视图范围中配置的值。 默认为：3600秒。 |
| [!UICONTROL Issue Access Tokens] | 商店视图 | 控制店面是否可以获取目录视图的访问令牌。 当设置为`No`时，`Company.catalogViewContext`返回目录视图ID，但没有访问令牌，因此店面无法进行身份验证以从从Adobe Commerce同步的[!DNL Adobe Commerce Optimizer]私有目录视图读取。 |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
> - [ACO目录视图同步](./aco-catalog-view-sync.md) — 配置如何将目录视图同步到[!DNL Adobe Commerce Optimizer]
> - [目录视图同步状态监视](../../systems/catalog-view-sync-status.md) — 监视同步运行状况并协调偏移

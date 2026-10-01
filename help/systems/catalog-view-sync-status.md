---
title: 目录视图同步状态监控
description: 监视B2B共享目录投影运行状况并协调Adobe Commerce Optimizer Connector的目录视图、策略、价格手册和访问密钥。
feature: Products, Customers, Data Import/Export
role: Admin
level: Intermediate
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
  - id: b974b164-8a4e-43b8-a9e2-8e67ec131677
    internal-label: Commerce on Prem
  - id: cdf0c6dd-1717-4e20-9530-a24eee57088b
    internal-label: Commerce on Cloud
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
    internal-label: Security
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: f42e0a1a-0d79-488d-a83f-f2c30672b137
    internal-label: Reporting
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
    internal-label: Data management
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 9ec73be87dd329dc04e7b133885fcc156f4ffcb6
workflow-type: tm+mt
source-wordcount: '1332'
ht-degree: 0%
---

# 目录视图同步状态监控

使用“目录视图：同步状态”页可以监视同步，并对已投影到Adobe Commerce Optimizer的目录视图进行故障排除。 对于每个自定义共享目录，[!DNL Adobe Commerce Optimizer Connector for B2B]会为共享目录网站范围内的每个商店视图创建一个目录视图。 每个目录视图配置有分类策略、其链接的价格手册以及用于验证受限访问令牌的公共密钥。 Adobe Commerce保留相应的目录视图元数据，包括私钥和默认价格手册ID。

>[!NOTE]
>
>若要跟踪目录数据馈送的同步状态，请使用[[!UICONTROL Data Feed Sync Status]](data-feed-sync-status.md)页面。

## 受众和可用性 {#audience}

仅[!BADGE PaaS]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="仅适用于云基础架构和内部部署项目上的Adobe Commerce 。"}

使用B2B共享目录与[!DNL Adobe Commerce Optimizer Connector for B2B]集成的Adobe Commerce on Cloud Infrastructure和本地商户可以使用[!UICONTROL Catalog View Sync Status]页面。 安装连接器扩展时，会自动安装和启用页面。

## 访问“目录视图：同步状态”页 {#access-catalog-view-sync-status-page}

从管理区域，导航到&#x200B;**[!UICONTROL System]** > **[!UICONTROL Data Transfer]** > **[!UICONTROL Catalog View Sync Status]**。

![目录视图同步状态页面列出具有同步运行状况的目录视图](assets/catalog-view-sync-status.png){width="600" zoomable="yes"}

该页面有三个选项卡：

- **[!UICONTROL Catalog Views]** — 连接器创建的目录视图，每个视图具有同步运行状况。 查看[目录视图同步状态摘要](#catalog-view-sync-status-summary)。
- **[!UICONTROL Orphaned in ACO]** — 存在于[!DNL Adobe Commerce Optimizer]中的实体，没有相应的[!DNL Adobe Commerce]源。 查看ACO选项卡[&#128279;](#orphaned-in-aco-tab)中的孤立。
- **[!UICONTROL Deleted]** — 目录视图投影的记录已删除，因为其共享目录已被删除。 查看[已删除选项卡](#deleted-tab)。

## 目录视图同步状态摘要 {#catalog-view-sync-status-summary}

页面顶部的摘要信息卡显示每个运行状况中的目录查看次数，以及在30天内过期的限制访问密钥计数：

| 卡片 | 描述 |
| --- | --- |
| **状况良好** | 未检测到漂移的目录视图。 |
| **已降级** | 具有可修复漂移的目录视图。 |
| **失败** | 从未在[!DNL Adobe Commerce Optimizer]中创建或直接删除的目录视图。 |
| **密钥≤30D** | 受限访问密钥将在30天内过期。 |

网格为每个目录视图列出一行：

| 字段 | 描述 |
| --- | --- |
| **目录视图** | 投影到[!DNL Adobe Commerce Optimizer]中的目录视图的标识符。 |
| **Source** | 投影目录视图的共享目录。 选择链接以在管理员中打开共享目录。 |
| **存储视图** | 目录视图代表的商店视图。 |
| **公司** | 当前链接到此目录视图的公司数。 |
| **状态** | 目录视图的整体同步运行状况。 查看[同步状态值](#sync-status-values)。 |
| **策略** | 分配给此目录视图的分类策略是否与您的[!DNL Adobe Commerce]配置匹配。 |
| **价格手册** | 分配给此目录视图的价格手册是否与您的[!DNL Adobe Commerce]配置匹配。 |
| **访问密钥** | 是否将受限访问密钥链接到此目录视图。 |
| **密钥过期** | 目录视图的受限访问密钥的到期日期，以及剩余天数。 |
| **漂移** | 检测到的漂移类型（如果有）。 |
| **上次协调时间** | 协调进程上次选中此目录视图的时间。 |
| **操作** | **[!UICONTROL View details]**&#x200B;打开“目录查看同步状态”详细信息页面以查看当前状态、漂移、访问密钥和最近事件。 **[!UICONTROL Open in ACO admin]**&#x200B;在[!DNL Adobe Commerce Optimizer] Studio中打开目录视图详细信息页面。 **[!UICONTROL Copy ID]**&#x200B;复制目录视图ID以供参考。 请参阅[调解和修复漂移](#reconcile-and-repair-drift)。 |

## 同步状态值 {#sync-status-values}

| 状态 | 含义 |
| --- | --- |
| **状况良好** | 未检测到漂移。 目录视图、政策、价格手册和密钥与您的[!DNL Adobe Commerce]配置匹配。 |
| **已降级** | 检测到漂移，该漂移是可修复的 — 例如，在[!DNL Adobe Commerce Optimizer]中直接更改了政策或价格手册。 |
| **失败** | 从未创建目录视图，或直接在[!DNL Adobe Commerce Optimizer]中删除该视图。 |
| **挂起** | 目录视图尚未协调，或正在等待其第一个投影。 |
| **正在弃用** | 共享目录已在[!DNL Adobe Commerce]中删除，并且目录视图位于其删除宽限期内。 |
| **已删除** | 目录视图投影在其宽限期之后被删除。 它将作为记录保留在[!UICONTROL Deleted]选项卡上90天。 |
| **孤立** | 目录视图或键存在于[!DNL Adobe Commerce Optimizer]中，但没有相应的[!DNL Adobe Commerce]源。 查看ACO选项卡[&#128279;](#orphaned-in-aco-tab)中的孤立。 |

### 配置删除宽限期 {#configure-the-deletion-grace-period}

删除宽限期指定删除关联的共享目录后目录视图和相关数据的数据保留窗口。 该值默认为7天。
窗口过期后，将删除所有数据。

#### 更改数据保留设置

1. 打开[!DNL Adobe Commerce]管理员。

1. 从&#x200B;**[!UICONTROL Stores]**&#x200B;菜单中选择&#x200B;**[!UICONTROL Configuration]** > **[!UICONTROL Services]** > **[!UICONTROL ACO Catalog View Sync]** > **[!UICONTROL Deletion]** > **[!UICONTROL Deletion Grace Period (days)]**。

1. 根据需要更新&#x200B;**[!UICONTROL Deletion Grace Period (days)]**&#x200B;值。

   要在删除共享目录后立即删除目录视图ACO投影，请将此值设置为`0`。

1. 选择&#x200B;**[!UICONTROL Save Config]**。

有关详细信息，请参阅[服务> ACO目录视图同步](../configuration-reference/services/aco-catalog-view-sync.md)，以获取所有可用的同步和漂移协调器设置。

## 协调并修复配置差异 {#reconcile-and-repair-drift}

[!DNL Adobe Commerce]是B2B共享目录投影的权威源。 协调会将您的[!DNL Adobe Commerce]配置与[!DNL Adobe Commerce Optimizer]进行比较，并报告或修复任何差异。

>[!IMPORTANT]
>
>直接在[!DNL Adobe Commerce Optimizer]中对连接器管理的目录视图、策略、价格手册或键所做的更改不是真实的主要来源。 协调会将这些差异报告为配置差异，当您修复时，会将其还原以与[!DNL Adobe Commerce]匹配。 在[!DNL Adobe Commerce]中进行配置更改，而不是在[!DNL Adobe Commerce Optimizer]中进行更改。 修复不会删除您在连接器管理的策略旁边手动添加的策略。

使用页面级别按钮进行协调：

- **[!UICONTROL Reconcile]** — 检查配置差异并更新同步状态，而不在[!DNL Adobe Commerce Optimizer]中进行任何更改。

- **[!UICONTROL Reconcile & Repair]** — 检查配置差异，并自动恢复任何可修复差异的预期配置。

  选择&#x200B;**[!UICONTROL Reconcile & Repair]**&#x200B;会发送异步协调请求，并在修复运行之前返回。 确认消息显示状态会很快刷新，但页面不会自动重新加载。 等待处理完成，然后刷新网格以检查结果。

使用行上的&#x200B;**[!UICONTROL Action]**&#x200B;菜单可以：

- **[!UICONTROL View details]** — 打开“目录查看同步状态”详细信息页面以查看当前状态、漂移、访问密钥和最近事件。
- **[!UICONTROL Open in ACO admin]** — 在[!DNL Adobe Commerce Optimizer] Studio中打开目录视图详细信息页面。
- **[!UICONTROL Copy ID]** — 复制目录视图ID以供参考。

## 在ACO选项卡中孤立 {#orphaned-in-aco-tab}

**[!UICONTROL Orphaned in ACO]**&#x200B;选项卡列出存在于[!DNL Adobe Commerce Optimizer]中但没有相应[!DNL Adobe Commerce]源的目录视图和受限访问键，例如，在[!DNL Adobe Commerce Optimizer] Studio中手动创建的实体，而不是由连接器创建的实体。 这些实体无法显示在主网格中，因为没有可与其匹配的[!DNL Adobe Commerce]记录。

![在ACO选项卡中被孤立，列出没有Adobe Commerce源的实体](assets/catalog-view-sync-orphan.png){width="600" zoomable="yes"}

| 字段 | 描述 |
| --- | --- |
| **类型** | 孤立实体的类别： [!UICONTROL Catalog View]或[!UICONTROL Access Key]。 |
| **ACO ID** | [!DNL Adobe Commerce Optimizer]中实体的标识符。 |
| **详细信息** | 有关实体的其他上下文，例如其策略。 |
| **第一次看到** | 协调首次检测到此实体时。 |
| **操作** | 选择&#x200B;**[!UICONTROL Copy ID]**&#x200B;以复制实体标识符。 使用复制的ID查找并从[!DNL Adobe Commerce Optimizer] Studio目录视图中删除该实体。 |

>[!NOTE]
>
>此选项卡仅用于报告。 协调永远不会删除孤立的实体。 如果不再需要它们，则直接在[!DNL Adobe Commerce Optimizer] Studio中将其删除。

## 已删除选项卡 {#deleted-tab}

**[!UICONTROL Deleted]**&#x200B;选项卡列出了因共享目录已在[!DNL Adobe Commerce]中删除而被删除的目录视图投影。 由于共享目录及其目录视图不再存在，因此这些行不会在任何位置链接。 它们仅作为被删除内容的记录保留。

![已删除选项卡，列出删除共享目录后删除的目录视图投影](assets/catalog-view-sync-deleted.png){width="600" zoomable="yes"}

| 字段 | 描述 |
| --- | --- |
| **目录视图** | 已删除目录视图的标识符。 |
| **Source** | 已删除的共享目录。 |
| **存储视图** | 所代表的目录视图的存储区视图。 |
| **删除于** | 删除投影时。 |

此选项卡中的行将在90天后自动清除。

## 已知限制

- [!DNL Adobe Commerce Optimizer] Studio中没有可视指示器来区分连接器管理的目录视图和手动创建的目录视图。 使用此页面而不是[!DNL Adobe Commerce Optimizer] Studio UI来确定连接器管理的内容。
- **[!UICONTROL Orphaned in ACO]**&#x200B;选项卡的&#x200B;**[!UICONTROL ACO ID]**&#x200B;列标识目录视图、策略或访问键，而不是唯一标识符。 列命名可能会发生更改。

>[!MORELIKETHIS]
>
> - [管理目录视图配置](/help/b2b/catalog-views-manage.md) — 从共享目录或公司帐户中查看目录视图
> - [数据馈送同步状态](data-feed-sync-status.md)
> - [服务> ACO目录视图同步](../configuration-reference/services/aco-catalog-view-sync.md) — 配置删除和创建宽限期以及漂移协调器
> - [受限访问密钥管理](restricted-access-keys.md) — 管理此页面显示的过期密钥
> - *Adobe Commerce Optimizer Connector Guide*&#x200B;中的[监视B2B共享目录的目录视图同步](https://experienceleague.adobe.com/en/docs/commerce/aco-optimizer-connector/manage-sync/catalog-view-sync/catalog-view-sync-status)
> - [专用目录视图](https://experienceleague.adobe.com/en/docs/commerce/optimizer/setup/private-catalog-view)
> - [受限访问密钥](https://experienceleague.adobe.com/en/docs/commerce/optimizer/setup/restricted-access-keys)

---
title: 产品详细信息页面扩充
description: 使用[!DNL Adobe Commerce]产品详细信息页面扩充功能查看AI建议的产品副本、创建扩充作业并为LLM和AI发现部署批准的更新。
role: Admin, User, Leader
recommendations: noCatalog
touch: true
badgePaas or on-premises: label="Cloud or on-premises only" type="Informative" url="https://experienceleague.adobe.com/zh-hans/docs/commerce/user-guides/product-solutions" tooltip="Applies to Adobe Commerce on Cloud projects (Adobe-managed Cloud or on-premises infrastructure) and on-premises projects only."
autotag-review: '2026-06-23T17:36:07.142Z'
TQID: 'https://experienceleague.adobe.com/cjHuva7PP7UzP-yVhe0rkDzHgAYjfSdYEx3g5gorxwk'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
    internal-label: Accounts
  - id: c32adafa-ed01-4b31-997e-2413013911b0
    internal-label: Integrations
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
    internal-label: Storefront
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 9e234eb68fe34171d9e5cf95e8cdab5c31825492
workflow-type: tm+mt
source-wordcount: '1102'
ht-degree: 0%
---

# 产品详细信息页面扩充

产品详细信息页面(PDP)扩充使用结构化产品数据最大限度地提高LLM在每个PDP上的可抓取性，而无需对您的人类可见体验进行任何更改。 此功能会读取您的产品目录，以便为每个PDP创建结构化的数据有效负载，LLM可以轻松读取和解析这些有效负载。

## 工作原理 {#how-it-works}

您的Adobe Commerce目录包含产品信息，如属性、系列品种、类别、价格和可用性。 在PDP扩充作业中，您可以选择产品页面和目录事实组以供AI代理使用。 信息是为座席整理的，不会更改店面体验。

通过PDP扩充，您可以：

- 选择具有实时产品页面的特定已启用产品。
- 在保存或运行作业之前，请查看所选页面和事实的摘要。
- 预览扩充中包含的产品信息。

| 方向 | 用途 |
| --- | --- |
| Commerce目录 — >扩充作业 | Select Live产品页面以及要包含的目录事实。 |
| 扩充作业 — > AI代理 | 使所选现有产品信息以结构化形式提供。 人类看得见的店面不会改变。 |

## 访问PDP扩充

在开始之前，请查看特定于部署的[AI产品发现先决条件](prerequisites.md)。 完成Commerce平台的设置后，在管理员中打开&#x200B;**[!UICONTROL AI Product Discovery]**&#x200B;并选择&#x200B;**[!UICONTROL Product Details Page Enrichment]**。

## PDP增强的两条途径

接收PDP增强的路径有两种：

- **代理流量** — 此类型的扩充会在您配置Commerce实例后24-48小时自动开始，并在&#x200B;**优化**&#x200B;选项卡上显示结果。
- **扩充管理器** — 这些扩充由商家在单击&#x200B;**[!UICONTROL Create enrichment]**&#x200B;按钮并手动选择要扩充的SKU时配置。 了解有关[扩充管理器](#create-an-enrichment-job)的更多信息。

## 审查PDP扩充活动

此时将打开PDP扩充页面以显示&#x200B;**[!UICONTROL Optimizations]**&#x200B;选项卡。 使用控制面板可复查扩充覆盖范围、任务活动和需要注意的任务。 使用&#x200B;**[!UICONTROL Settings]**&#x200B;选项卡将[链接](settings.md)您的Commerce实例到AI产品发现。

### 查找需要注意的作业

**[!UICONTROL Needs your attention]**&#x200B;部分突出显示需要操作的作业。 信息卡可显示作业名称、产品选择方式、产品页数、作业状态和进度。 使用信息卡上的可用操作继续作业。

### 搜索所有作业

使用表格可搜索和跟踪作业。 按作业详细信息搜索或按状态筛选，包括&#x200B;**[!UICONTROL Generating]**、**[!UICONTROL Ready to review]**、**[!UICONTROL Deployed]**、**[!UICONTROL Queued]**&#x200B;或&#x200B;**[!UICONTROL Failed]**。 该表列出了每个作业的ID、名称、来源、产品页数、开始日期、状态和可用操作。

## 创建扩充作业

在此部分中，您将了解如何创建产品详细信息页面扩充。

![创建PDP扩充](./assets/create-cat-enrich.png)

1. 在&#x200B;**[!UICONTROL Optimizations]**&#x200B;中，单击&#x200B;**[!UICONTROL Create enrichment]**。
1. 输入&#x200B;**扩充名称**，如“Black Friday 2026”。
1. Select **类别**，如“咖啡”。
1. Select **属性集**，如“附件”。
1. Select **产品类型**，如“简单产品”。
1. 在&#x200B;**价格范围**&#x200B;内Select。
1. 单击&#x200B;**[!UICONTROL Apply filters]**。

   您可以预览符合扩充条件的产品，然后单击&#x200B;**自定义**&#x200B;以进一步限定要扩充的产品。

1. 单击&#x200B;**[!DNL Next]**&#x200B;以确认要扩充的特定产品。
1. 单击&#x200B;**[!DNL Run enrichment]**。

   扩充作业运行并显示在&#x200B;**优化**&#x200B;表中。 当它完成运行时，您可以[查看和部署](#review-and-deploy-an-enrichment-job)优化。

### 查看扩充作业 {#review-and-deploy-an-enrichment-job}

打开扩充作业。

![PDP扩充URL列表](./assets/pdp-enrich-urls.png)

带有建议&#x200B;**表的** URL列出了具有扩充机会的所有产品。 对于每个产品，您可以：

- **展开行**&#x200B;以查看AI分析和建议的扩充。
- **在申请之前编辑**&#x200B;建议的产品名称或描述，以符合您的品牌声音和促销准则。
- 针对要扩充的产品&#x200B;**部署优化**，并将其直接发布到Adobe Commerce店面。
- 在审核和应用扩充后&#x200B;**标记为已固定**。
- **忽略**&#x200B;与您的目录策略无关的建议。

建议分为三个视图：**当前建议**、**固定建议**&#x200B;和&#x200B;**忽略的建议**。 应用扩充后，它会移至&#x200B;**固定建议**，状态为&#x200B;**已应用**。 可以随时回滚应用的增强功能。

### 部署优化

查看建议并选择要优化的产品页后，单击&#x200B;**部署优化**&#x200B;以使用Edge中的优化发布扩充。 **部署到Edge**&#x200B;确认对话框将显示所选产品URL、优化类型和正在应用的扩充。 部署后，确认屏幕会确认哪些产品页面已成功优化。

优化通过[在Edge中优化](https://experienceleague.adobe.com/zh-hans/docs/brand-visibility/using/resources/optimize-at-edge/fastly-byocdn)专门交付给AI用户代理。 人类访客会继续像之前一样看到您现有的店面体验，而不会更改您的PDP设计、页面性能或品牌体验。

## 限制和注意事项 {#limits}

- 只能选择已启用且包含实时产品页面的产品。
- 扩充整理目录中已经存在的事实；不添加新的产品信息。
- PDP扩充工作流不会更改店面。
- PDP扩充作业和目录扩充作业具有不同的目的和工作流。
- PDP优化使用[在Edge中优化](https://experienceleague.adobe.com/zh-hans/docs/brand-visibility/using/resources/optimize-at-edge/fastly-byocdn) 。

## 最佳实践 {#best-practices}

- 使用用于标识产品组或营销活动的清晰作业名称。
- 预览作业中包含的事实，并确认它们对于AI代理是准确且合适的。
- 在决定跳过或覆盖产品之前，检查产品是否已扩充。
- 与负责这些记录的团队协调目录同步和产品事实的所有权。

## 示例：使用变体和规范扩充产品

产品页面包含的目录信息通常比AI代理可读到的多。 例如，商家卖防水登山靴。 大小、宽度和颜色选项位于随JavaScript一起加载的变量选择器中。 材料、防水功能和护理说明位于折叠的“详细信息”选项卡中，适合的指导在弹出窗口中打开。 购物者可以打开所有这些页面，但在首次加载时读取页面的AI爬虫可能只能看到产品名称、价格和简短描述。

当扩充作业在此产品上运行时，它会获取产品的所有目录数据（包括其属性和每个变体），并将其打包为人工智能代理可以读取的结构化格式。 然后，AI助手可以回答诸如“此靴子是否适合大小为11？”之类的问题。 或“它是否完全防水？” 商家自己的目录数据。

扩充作业仅使用目录中已存在的信息。 它不会创造新的产品事实，也不会改变购物者看到的产品页面。

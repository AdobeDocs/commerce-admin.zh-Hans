---
title: 促销服务限制和边界
description: 了解Adobe Commerce Optimizer许可证限制和系统边界。 规划容量、跟踪使用情况，并在超出限制时避免延迟和限制。
role: Admin, Developer
hide: true
badgeSaas: label="仅限SaaS" type="Positive" url="https://experienceleague.adobe.com/zh-hans/docs/commerce/user-guides/product-solutions" tooltip="仅适用于使用CCDM设置的Adobe Commerce as a Cloud Service实例（Adobe管理的SaaS基础架构）。"
autotag-review: '2026-11-02T18:48:38.168Z'
TQID: 'https://experienceleague.adobe.com/KoRp--G2sMvv-Hr7KiHriZrFmtEm0BhGoGWVQQK-ofE'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
  - id: de2e2e68-c5d7-4efe-be7b-27528698f06b
    internal-label: Commerce as a Cloud Service
feature_v2:
  - id: 5a951749-fac9-5bc7-9a98-ebe4ff066437
    internal-label: Cloud
  - id: 8d0b446f-5b16-5a10-b272-01143504a11c
    internal-label: System
  - id: d3b92bef-63fa-5031-a925-d04d9362d616
    internal-label: Saas
source-git-commit: 71df9ad673f2e7dff802e4b26d8e169c42d9c063
workflow-type: tm+mt
source-wordcount: '1006'
ht-degree: 1%
---

# 使用可组合目录数据模型(CCDM)的促销服务限制和边界

带有CCDM的Adobe Commerce促销服务应用许可证限制和系统边界，这些限制定义了您的项目可以使用的容量：

- **许可证限制** — 基于您购买容量；可通过购买其他包来扩展。
- **系统边界** — 固定限制以保护系统资源并确保所有用户的可靠性能。

您的使用情况必须保持在这些限制之内。 超过这些超时可能会导致延迟增加并请求限制。

## 请求额外容量

通过购买[许可证限制和系统边界](#license-limits-and-system-boundaries)部分中描述的许可证包，或通过就独特用例协商自定义许可证，可以增加许可证限制。 请联系您的Adobe客户代表以讨论您的要求。

有关系统边界的问题，请联系[Adobe支持](https://experienceleague.adobe.com/home?lang=zh-Hans#support)。

## 防止出现性能问题

遵循这些最佳实践以保持在限制范围内并避免操作问题：

- **查看您的限制** — 在启动新店面或营销活动之前了解您的[容量限制](#license-limits-and-system-boundaries)。
- **跟踪您的使用情况** — 使用内置量度仪表板或CDN日志。

## 许可证限制和系统边界

下表按功能区域汇总了许可证限制和系统边界，并包含有关添加其他许可证以扩展适用容量的信息。


### 目录

| **功能** | **描述** | **基础分配** | **可扩展？** |
| --- | --- | --- | --- |
| 产品摄取率 | 创建或更新的产品数 | 每分钟1千次更新<p>每天最多可更新10万次</p> | 是<p>添加一个许可证包：</p><ul><li>每分钟5K更新<br>每天最多500K更新</li> <li>每分钟10K更新<br>每天最多更新1M</li></ul><p>每天的最大数据摄取容量为100万次更新。</p> |
| 产品有效负载大小 | 使用API创建、更新或摄取产品信息时允许的最大数据量 | 200 KB | 否 |
| 目录变体 | 店面用户可用的目录查看次数。<p>被计为（*目录查看次数×价格手册数量*）</p> | 100个变量 | 是<p>添加100个目录变体许可证包</p> |
| 单个目录源中的产品 | 目录中支持的SKU | 25万SKU | 是<p>添加100K SKU许可证包</p> |
| 每个产品的变体 | 每个产品允许的产品变体数量（大小、颜色组合） | 1万 | 否 |
| 目录源 | 目录数据上下文的数量（例如，区域设置或PIM和ERP等数据源） | 50 | 否 |

{style="table-layout:auto"}

### 价格手册

| **功能** | **描述** | **基础分配** | **可扩展？** |
| --- | --- | --- | --- |
| 价格手册 | 每个实例允许的价格簿数量 | 基于[目录变体](#catalog)的数量 | 是<br>增加目录变体 |
| 每个价格记录的折扣 | 单个价格手册中可应用于产品价格的折扣数 | 10 | 否 |

{style="table-layout:auto"}

### 目录视图和策略

| **功能** | **描述** | **基础分配** | **可扩展？** |
| --- | --- | --- | --- |
| 目录视图 | 主目录的可配置子集的数量 | 基于[目录变体](#catalog)的数量 | 是<br>增加目录变体 |
| 每个目录视图的策略 | 允许的数据过滤器数量 | 10 | 否 |
| 策略中的属性值 | 可配置为进行筛选的产品特征数 | 100 | 否 |
| [受限访问密钥分配](setup/private-catalog-view.md) | 可分配给单个目录视图的受限制访问键数 | 3 | 否 |
| RSA密钥大小（受限访问密钥） | 受限制访问密钥可接受的最小和最大密钥强度 | 最小2048位，最大8192位 | 否 |
| 受限访问密钥 | 密钥吊销传播延迟 | 由于缓存，最长为5分钟。 延迟过后，由已删除的密钥签名的令牌会被拒绝。 | 不适用 |

{style="table-layout:auto"}

### 目录店面

目录店面功能的基本分配基于GMV（毛商品价值）层确定。 该表指示每个功能的最小分配。

| **功能** | **描述** | **基础分配** | **可扩展？** |
| --- | --- | --- | --- |
| 目录检索率 | 系统（店面、交易系统、ERP或其他）每月调用目录API以从目录中检索数据的次数 | 基于GMV层<p>最小分配：1000万/月</p> | 是<p>每月添加100万个许可证包请求</p> |
| 内容请求 | 请求店面进行HTML页面查看或JSON API调用。 计为1次页面查看或5次API调用。 | 基于GMV层<p>最小分配：200万/月</p> | 是<p>每月添加100万份许可证包</p> |
| 店面GenAI变体 | 允许基于文本的内容生成 | 基于GMV层<p>最小分配：1K变量/月</p> | 是<p>单独购买Generative AI积分</p> |

{style="table-layout:auto"}

>[!NOTE]
>
>图像生成需要将[!DNL Adobe Firefly]许可证配置为与[!DNL Adobe Commerce Optimizer]相同的IMS组织。


### 产品发现

以下限制适用于storefront产品搜索、列表和促销配置。

| **功能** | **描述** | **基础分配** | **可扩展？** |
| --- | --- | --- | --- |
| 产品检索 | 获取具有`products`、`productSearch`、`refineProduct`和`variants`的产品数据时，每个[!DNL Catalog Service] GraphQL请求的最大SKU数。 将较大的请求拆分为多个调用。 | 100 | 否 |
| 可过滤属性 | 可为分层导航和Facet启用的产品特征（如颜色、大小、品牌或材料）的数量 | 200 | 否 |
| 可搜索属性 | 可以为目录搜索编制索引的产品特征数 | 200 | 否 |
| 可排序的属性 | 在搜索和类别页面上可用作排序选项的产品特征数。 | 50 | 否 |
| 搜索分页深度 | 通过搜索分页可访问的最大产品数（例如，第100页×100个产品/页面） | 1万 | 否 |
| Facet | 可过滤的产品属性（如品牌、颜色、大小和价格）的数量，可配置这些属性以帮助购物者优化搜索结果和浏览类别 | 100<p>必须是可筛选的属性</p> | 否 |
| 每个方面的选项 | 购物者可在Facet中选择的可过滤产品属性值的数量（例如，“红色”、“蓝色”表示颜色，“小”、“Medium”表示大小） | 100 | 是<p>可以通过支持请求增加</p> |

{style="table-layout:auto"}

### Recommendations

以下功能适用于产品推荐。 [!DNL Adobe Commerce Optimizer]不支持其他Adobe Commerce产品中提供的某些功能。

| **功能** | **描述** | **基础分配** | **可扩展？** |
| --- | --- | --- | --- |
| 有效的推荐单位 | 店面上实时推荐组件的数量（如“客户也查看了”或“您可能也喜欢”） | 50 | 否 |
| 类别或属性包含/排除项 | 将产品筛选到符合推荐条件的特定集 | 不支持 | — |

{style="table-layout:auto"}

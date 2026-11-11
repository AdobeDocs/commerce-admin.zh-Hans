---
title: 目录视图
description: 了解目录视图是什么以及如何创建它们以按业务结构、策略和定价整理产品目录。
role: Admin, Developer
recommendations: noCatalog
badgeSaas: label="仅限SaaS" type="Positive" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="仅适用于使用CCDM设置的Adobe Commerce as a Cloud Service实例（Adobe管理的SaaS基础架构）。"
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
  - id: de2e2e68-c5d7-4efe-be7b-27528698f06b
    internal-label: Commerce as a Cloud Service
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
    internal-label: Metadata
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
source-git-commit: 8fbcfcdeb13c452a45e872d939e129703ac5abab
workflow-type: tm+mt
source-wordcount: '997'
ht-degree: 0%
---

# 目录视图

目录视图定义店面可以检索的产品和定价。 在配置有可组合目录数据模型(CCDM)的Adobe Commerce as a Cloud Service实例中，目录视图使用支持Adobe Commerce Optimizer的相同目录基础。

目录视图将目录来源、策略和价格手册组合在一起，以定义店面的目录上下文。 策略确定可用的产品分类。 促销规则控制该分类中产品的促销和排名方式，并且可以跨所有目录视图应用或针对特定视图进行定制。 请参阅[创建促销规则](../merchandising/rules/add.md)。

Commerce基金会仍然是产品和价格的真实来源。 产品和价格数据通过本机Adobe Commerce as a Cloud Service集成以单向方式同步到CCDM，无需单独的连接器安装或App Builder应用程序。 网站、商店和商店视图配置保留在Commerce Foundation中，该基金会还管理购物车、结账、促销、客户、订单和付款。

>[!NOTE]
>
>对于使用CCDM配置的实例，请使用Adobe Unified Experience中的[Commerce管理员](../../getting-started/admin-unified-experience.md)配置目录视图和策略，并将同步的价格手册与目录视图关联。 将目录服务用于“实时搜索”和“产品推荐”的实例无权访问这些目录管理屏幕。

## 目录视图的工作方式

目录视图将店面上下文的目录数据和配置汇集在一起。 它可用于表示业务部门、品牌、区域或其他店面体验。

- **[目录源](catalog-sources.md)**&#x200B;为目录体验提供产品数据。
- **[策略](policies.md)**&#x200B;为目录视图筛选产品数据。
- **[价格手册](pricebooks.md)**&#x200B;提供了与目录视图关联的定价数据。

目录视图不会替换Adobe Commerce as a Cloud Service中的网站、商店和商店视图结构。 Commerce Foundation将继续管理该结构和事务操作。

目录数据以单向方式从Commerce Foundation同步到CCDM中。 CCDM支持店面目录体验和产品发现。 Commerce Foundation将继续处理购物车、结账、促销活动、客户和订单。

## 开始之前

配置目录视图之前：

- [确认Adobe Commerce as a Cloud Service实例使用CCDM](../overview.md)。
- 确认已填充店面所需的目录数据并[已同步](data-sync.md)。
- 识别店面上下文所需的[目录源](catalog-sources.md)、[策略](policies.md)和[价格手册](pricebooks.md)。
- 确定是需要手动创建B2C目录视图，还是需要查看本机同步生成的B2B目录视图。

>[!NOTE]
>
>对于B2B实施，本机同步将从Commerce Foundation中的B2B配置生成目录视图、策略和价格手册。 请勿手动创建这些自动生成结构的重复项。

## 为B2C实施创建目录视图

当B2C实施需要手动配置目录视图时，使用此工作流。

1. 登录到Unified Experience中的[Commerce管理员](../../getting-started/admin-unified-experience.md)，然后选择配置了CCDM的Adobe Commerce as a Cloud Service实例。
1. 在左侧导航中，转到&#x200B;**[!UICONTROL Catalog]** > **[!UICONTROL Catalog Views]**。
1. 选择&#x200B;**[!UICONTROL Create catalog view]**。
1. 输入目录视图的名称。
1. 为店面上下文选择[目录源](catalog-sources.md)。
1. 将相关的[策略](policies.md)与目录视图关联。
1. 通过[配置价格手册可用性](pricebooks.md)，将相关价格手册与目录视图关联。
1. 创建目录视图。

## B2B目录视图

对于B2B实施，本机同步将从Commerce Foundation中的B2B配置生成目录视图、策略和价格手册。 在Commerce Foundation中管理底层B2B目录和公司关系，而不是在CCDM中手动创建重复结构。

有关设置说明，请参阅[创建共享目录](../../b2b/catalog-shared-create.md)和[将公司分配给共享目录](../../b2b/catalog-shared-assign-companies.md)。

配置B2B关系后：

1. 确认[同步](data-sync.md)已完成。
2. 在Unified Experience的[Commerce管理员中，查看生成的目录视图、[策略](policies.md)和[价格手册](pricebooks.md)。](../../getting-started/admin-unified-experience.md)
3. 验证店面是否显示公司的预期产品分类和定价。
4. 测试添加到购物车、购物车和结账功能，确认产品可用性和交易定价符合预期的B2B配置。

## 价格手册和结账

价格手册通过目录视图提供可用的定价数据。 在Adobe Commerce as a Cloud Service中，Commerce Foundation仍然是价格的真实来源，定价数据通过本机集成同步到CCDM。 在配置目录视图时，请使用适用的同步价格手册，而不是在CCDM中单独创作价格。

购物车和结帐使用Commerce Foundation定价。 验证显示的店面价格是否与适用的购物车和结账价格相匹配。

## 查看和验证目录视图

配置目录视图后，验证完整的店面体验：

- 确认目标目录数据是[已同步](data-sync.md)。
- 确认目录视图与预期的[策略](policies.md)和[价格手册](pricebooks.md)相关联。
- 检查店面是否返回了预期的产品分类。
- 根据相应的Commerce Foundation定价验证显示的定价。
- 测试添加到购物车、购物车和结账。

对于B2B实施，还要确认通过同步生成的目录结构与预期的公司和目录配置相匹配。

## 故障排除

### 店面中缺少产品

- [确认实例使用CCDM](../overview.md)。
- 确认目录数据已[同步](data-sync.md)。
- 检查店面是否正在使用预期的目录上下文。
- 查看与目录视图关联的[策略](policies.md)。

### 显示的价格是意外的

- 确认预期的[价格手册](pricebooks.md)与目录视图相关联。
- 检查价格数据是否为[已同步](data-sync.md)并且与Commerce Foundation一致。

  有关网站和客户组定价映射，请参阅[价格手册](pricebooks.md)。

- 在购物车和结帐中再次验证价格。

### CCDM目录屏幕在Commerce管理中不可见

[确认所选实例使用CCDM](../overview.md)，并且您正在访问Unified Experience中的[Commerce管理员](../../getting-started/admin-unified-experience.md)。 运行目录服务v1的实例没有CCDM管理屏幕。

## 相关内容

- [Adobe Commerce as a Cloud Service快速入门](https://experienceleague.adobe.com/en/docs/commerce/cloud-service/getting-started)
- [Adobe Commerce B2B共享目录概述](../../b2b/catalog-shared.md)
- [Adobe Commerce as a Cloud Service发行说明](https://experienceleague.adobe.com/en/docs/commerce/cloud-service/release-notes)
- [目录同步](data-sync.md)

---
title: 管理公司层次结构
description: 构建和管理公司层次结构，以支持具有复杂运营模型的B2B组织。
feature: B2B, Companies
role: Admin
hide: false
hidefromtoc: false
exl-id: a277ed95-7935-4d27-adb2-35116972732b
source-git-commit: 1fc1e07f20e2c22ac430f384e9e2b278edae405c
workflow-type: tm+mt
source-wordcount: '827'
ht-degree: 0%

---

# 管理公司层次结构

[!UICONTROL Company Hierarchy]功能允许您在单个父公司结构下组织多个相关公司。 这非常适合具有子公司、特许经营机构、多个位置或复杂组织结构的企业，这些公司在保持单个公司身份的同时需要集中管理。

## 用例

* **集中管理** — 跨单个母公司的多个公司应用设置和配置
* **维护结构** — 将公司组织到反映业务组织的逻辑层次结构中
* **简化操作** — 管理整个组织的报价、采购订单、付款方式和送货设置
* **保留Autonomy** — 各个公司保留其身份，同时受益于共享配置

## 先决条件

在创建公司层次结构之前，请确保：

* B2B功能已在Commerce安装中启用
* 您具有管理公司的管理员访问权限
* 母公司和子公司已创建为单独公司
* 您了解应用父设置将覆盖现有的子公司配置

## 工作原理

管理员可以通过将相关公司分配给指定的母公司（位于组织层次结构顶部的公司）来构建公司层次结构。

从管理员中，通过编辑单个公司(`[!UICONTROL Company Type] = Company`)并在[!UICONTROL Company Hierarchy]配置中分配相关公司来创建父公司。

![公司层次结构网格](./assets/company-hierarchy-grid.png){width="700"}

>[!NOTE]
>
>有关[!UICONTROL Company Hierarchy]网格的详细信息，请参阅[公司层次结构](account-company-create.md#company-hierarchy)字段描述。

通过编辑父公司并使用&#x200B;*[!UICONTROL Company Hierarchy]*&#x200B;网格添加或删除公司来管理公司分配。 使用&#x200B;*[!UICONTROL Actions]*&#x200B;控件管理组织中公司的[高级设置配置](#change-company-settings)。

## 将公司分配给母公司

1. 在&#x200B;_管理员_&#x200B;侧边栏中，导航到&#x200B;**[!UICONTROL Customers]** > **[!UICONTROL Companies]**。

   ![公司网格](./assets/companies-grid-view.png){width="700" zoomable="yes"}

1. 从[!UICONTROL Companies]网格中，打开公司详细信息页面以创建分配。

   * 要将其他公司分配给现有的母公司，请选择母公司的&#x200B;**[!UICONTROL Edit]**&#x200B;操作。
   * 要创建母公司，请为指定为母公司的公司选择&#x200B;**[!UICONTROL Edit]**&#x200B;操作。

     您无法从现有的父公司或子公司创建新父公司。

1. 在公司详细信息页面上，展开&#x200B;**[!UICONTROL Company Hierarchy]**，然后选择&#x200B;**[!UICONTROL Assign Companies]**。

   ![创建母公司](./assets/company-hierarchy-grid.png){width="675" zoomable="yes"}

1. 从可用公司列表中，选择要分配的公司，然后选择&#x200B;**[!UICONTROL Assign Selected Companies]**。

   ![选择要分配的公司](./assets/company-hierarchy-select-companies-assign.png){width="675" zoomable="yes"}

1. 出现提示时，选择&#x200B;**[!UICONTROL Assign]**&#x200B;完成公司分配。

## 从母公司取消分配公司

1. 在公司页面上，通过选择&#x200B;**[!UICONTROL Edit]**&#x200B;操作打开母公司的公司详细信息页面。

   ![父公司详细信息页面](./assets/company-update.png){width="700" zoomable="yes"}

1. 通过展开&#x200B;**[!UICONTROL Company Hierarchy]**&#x200B;查看已分配公司的列表。

1. 从组织中删除公司。

   * 在要删除的公司的[!UICONTROL Action]列中，**[!UICONTROL Select]** > **[!UICONTROL Unassign from parent]**。

     ![从组织中删除公司](./assets/company-hierarchy-grid-unassign.png){width="640" zoomable="yes"}

   * 出现提示时，通过选择&#x200B;**[!UICONTROL Unassign]**&#x200B;从层次结构中删除分配的公司。

## 管理组织的公司设置

更新组织的[高级设置](account-company-create.md#advanced-settings)配置。 您可以：

* 将父配置设置应用于所有子公司
* 将相同的设置应用于组织中选定的公司

您可以应用以下任何设置：

* **报价管理** — 启用或禁用公司请求和管理报价的功能
* **采购订单** — 控制公司是否可以创建和管理采购订单
* **付款方式配置** — 定义公司可用的付款方式
* **付款方式设置** — 配置特定付款方式参数和限制
* **配送方式可用性** — 设置公司可以使用哪些配送方式
* **配送方式配置** — 定义配送方式设置和限制

在更新过程中，初始配置值默认为为父公司配置的当前值。 必须至少选中一个设置的更改复选框才能将设置应用于所选公司。 您还可以在应用更改之前更新每个设置的默认值。

>[!WARNING]
>
>应用父公司设置将替换现有的子公司配置，包括信用限制、付款方法、送货设置和自定义限制。 应用设置后，您仍然可以通过编辑公司行项目来管理和自定义各个父公司和子公司的高级设置。

### 最佳实践

将父公司设置应用于子公司时，请考虑以下最佳实践：

* 在应用父配置之前查看现有的子公司设置
* 先更改单个子公司的测试设置
* 向可能受影响的公司管理员传达更改

### 将父配置设置应用于子公司

1. 在&#x200B;_管理员_&#x200B;侧边栏中，导航到&#x200B;**[!UICONTROL Customers]** > **[!UICONTROL Companies]**。

1. 从[!UICONTROL Companies]网格中，通过从&#x200B;**[!UICONTROL Edit]**&#x200B;列中选择&#x200B;**[!UICONTROL Action]**&#x200B;来编辑父公司。

1. 在父公司详细信息页面上，展开&#x200B;**[!UICONTROL Company Hierarchy]**&#x200B;部分以查看组织中包含的公司。

1. 选择要配置的公司。

   ![从公司层次结构中选择公司](assets/company-hierarchy-select-companies.png){width="675" zoomable="yes"}

1. 从网格上方的&#x200B;**[!UICONTROL Actions]**&#x200B;控件中选择&#x200B;**[!UICONTROL Change company settings]**。

   ![更改公司层次结构的公司设置](assets/company-hierarchy-change-company-settings-action.png){width="675" zoomable="yes"}

1. 更改设置配置。

   * 在[!UICONTROL Change company settings]页面上，找到要修改的配置设置。

   * 选中&#x200B;**[!UICONTROL Change]**&#x200B;复选框以启用设置。

   * 如有需要，请更新值。

     ![更改多个公司的公司设置](assets/company-hierarchy-change-settings-config.png){width="575" zoomable="yes"}

1. 更新配置后，选择&#x200B;**[!UICONTROL Apply Changes]**。

1. 出现提示时，选择&#x200B;**[!UICONTROL Change settings]**&#x200B;以更新所选公司的配置。

>[!MORELIKETHIS]
>
>* [创建公司帐户](account-company-create.md) — 了解如何在生成层次结构之前创建各个公司
>* [公司角色和权限](account-company-roles-permissions.md) — 了解公司结构内的用户访问权限
>* [公司信用管理](credit-company.md) — 为公司配置信用限额和付款条件
>* [管理公司](manage-companies.md) — 公司管理功能概述
>* [启用B2B功能](enable-basic-features.md) — 启用和配置B2B功能

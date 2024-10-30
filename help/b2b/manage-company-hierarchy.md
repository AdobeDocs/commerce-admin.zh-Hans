---
title: 管理公司层次结构
description: 构建和管理公司层次结构，以支持具有复杂运营模型的B2B组织。
feature: B2B, Companies
role: Admin
hide: false
hidefromtoc: false
exl-id: a277ed95-7935-4d27-adb2-35116972732b
source-git-commit: 6b06f52eb4ee8ca136a1c60fd6dc04a9ac96bbfa
workflow-type: tm+mt
source-wordcount: '474'
ht-degree: 0%

---

# 管理[!UICONTROL Company Hierarchy]

管理员可以通过将相关公司分配给指定的母公司（位于组织层次结构顶部的公司）来构建[!UICONTROL Company Hierarchy]。

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

   - 要将其他公司分配给现有的母公司，请选择母公司的&#x200B;**[!UICONTROL Edit]**&#x200B;操作。
   - 要创建母公司，请为指定为母公司的公司选择&#x200B;**[!UICONTROL Edit]**&#x200B;操作。

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

   - 在要删除的公司的[!UICONTROL Action]列中，**[!UICONTROL Select]** > **[!UICONTROL Unassign from parent]**。

     ![从组织中删除公司](./assets/company-hierarchy-grid-unassign.png){width="640" zoomable="yes"}

   - 出现提示时，通过选择&#x200B;**[!UICONTROL Unassign]**&#x200B;从层次结构中删除分配的公司。

## 管理组织的公司设置

更新组织的[高级设置](account-company-create.md#advanced-settings)配置以将父配置应用于所有子公司，或将相同的设置应用于组织中选定的公司。

在更新过程中，初始配置值默认为为父公司配置的当前值。 您必须至少更改一个设置以更新选定公司的配置。

**更改多个公司的高级设置配置**

1. 在&#x200B;_管理员_&#x200B;侧边栏中，导航到&#x200B;**[!UICONTROL Customers]** > **[!UICONTROL Companies]**。

1. 从[!UICONTROL Companies]网格中，通过从&#x200B;**[!UICONTROL Action]**&#x200B;列中选择&#x200B;**[!UICONTROL Edit]**&#x200B;来编辑父公司。

1. 在父公司详细信息页面上，展开&#x200B;**[!UICONTROL Company Hierarchy]**&#x200B;部分以查看组织中包含的公司。

1. 选择要配置的公司。

   ![从公司层次结构中选择公司](assets/company-hierarchy-select-companies.png){width="675" zoomable="yes"}

1. 从网格上方的&#x200B;**[!UICONTROL Actions]**&#x200B;控件中选择&#x200B;**[!UICONTROL Change company settings]**。

   ![更改公司层次结构的公司设置](assets/company-hierarchy-change-company-settings-action.png){width="675" zoomable="yes"}

1. 更改设置配置。

   - 在[!UICONTROL Change company settings]页面上，找到要修改的配置设置。

   - 选中&#x200B;**[!UICONTROL Change]**&#x200B;复选框以启用设置。

   - 根据需要更新值。

     ![更改多个公司的公司设置](assets/company-hierarchy-change-settings-config.png){width="575" zoomable="yes"}

1. 更新配置后，选择&#x200B;**[!UICONTROL Apply Changes]**。

1. 出现提示时，选择&#x200B;**[!UICONTROL Change settings]**&#x200B;以更新所选公司的配置。

>[!TIP]
>
>通过编辑公司行项目来管理单个公司的高级设置配置。

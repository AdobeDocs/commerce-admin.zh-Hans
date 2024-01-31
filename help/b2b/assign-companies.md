---
title: 管理公司层次结构
description: 了解如何通过构建公司层次结构来管理具有复杂运营模型的B2B组织
feature: B2B, Companies
role: Admin
hide: false
hidefromtoc: false
exl-id: a277ed95-7935-4d27-adb2-35116972732b
source-git-commit: 582f15c422e43af9acec6313c7b777b3126030f8
workflow-type: tm+mt
source-wordcount: '327'
ht-degree: 0%

---

# 管理 [!UICONTROL Company Hierarchy]

[!BADGE 1.5.0（测试版）]{type=Informative url="/help/b2b/release-notes.md" tooltip="仅供测试版计划参与者使用"}

管理员可以构建 [!UICONTROL Company Hierarchy] 将关联公司分配给指定的母公司，即位于组织顶部的公司。 如果 [!UICONTROL Company Type] 是 `Company`，则该公司不是组织的一部分，并且有资格成为母公司，或者被分配到现有的母公司。

在“管理员”中，您可以通过编辑公司，然后更新 [!UICONTROL Company Hierarchy] 用于分配或取消分配公司的配置。

![公司层次结构网格](./assets/company-detail-hierarchy-current-flag.png){width="700"}

>[!NOTE]
>
>欲知关于 [!UICONTROL Company Hierarchy] 网格，请参见 [公司层次结构](account-company-create.md#company-hierarchy) 字段描述。

## 将公司分配给组织

1. 从 _管理员_ 侧栏，导航到 **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

   ![公司网格](./assets/companies-grid-view.png){width="700" zoomable="yes"}

1. 在 [!UICONTROL Companies] 网格，打开公司详细信息页面以创建分配。

   - 要将其他公司分配给现有母公司，请选择 **[!UICONTROL Edit]** 针对母公司的操作。
   - 要创建母公司，请选择 **[!UICONTROL Edit]** 公司要指定为母公司的操作。

     您无法从现有的父公司或子公司创建父公司。

1. 在公司详细信息页面上，展开 **[!UICONTROL Company Hierarchy]**.

   ![公司层次结构网格](./assets/company-detail-hierarchy-current-flag.png){width="700" zoomable="yes"}

   该网格显示现有公司分配（如果存在）。 母公司始终位于 [!UICONTROL Company Hierarchy] 网格。 此 `[!UICONTROL Current]` 标记表示正在编辑的公司。

1. 将公司添加到父组织。

   - 通过选择 **[!UICONTROL Assign Companies]**.

   - **在此页上选择全部**，或选择一个或多个特定的公司行项目。

   - 选择 **[!UICONTROL Assign Selected Companies]**.

   - 通过选择完成公司分配 **[!UICONTROL Assign]**.

     ![将公司分配给组织](./assets/assign-selected-companies-hierarchy.png){width="675" zoomable="yes"}

## 从母公司取消分配公司

1. 在 _管理员_ 侧栏，导航到 **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

   ![公司网格](./assets/companies-grid-view.png){width="700" zoomable="yes"}

1. 在 [!UICONTROL Companies] 网格，通过选择以打开母公司的公司详细信息页面 **[!UICONTROL Edit]**.

1. 通过展开查看已分配公司的列表 **[!UICONTROL Company Hierarchy]**.

1. 从 [!UICONTROL Company Hierarchy] 网格，使用取消分配公司 **[!UICONTROL Select]** 要选择的操作控件 **[!UICONTROL Unassign from parent]**.

   ![从父组织取消分配公司](./assets/company-hierarchy-grid-unassign.png){width="700" zoomable="yes"}

1. 出现提示时，通过选择从层次结构中删除分配的公司 **[!UICONTROL Unassign]**.

---
title: 公司帐户结构
description: 了解公司结构以及公司管理员如何定义它以支持其业务工作流和策略。
exl-id: 4724b208-b6ac-4de5-9a4c-bc4d68402506
feature: B2B, Companies
role: Admin
source-git-commit: fec72b792cf3149c05803874795c45f9f4e28673
workflow-type: tm+mt
source-wordcount: '709'
ht-degree: 0%

---

# 公司帐户结构

公司账目可设立以反映业务结构。 最初，公司结构仅包括公司管理员，但可以扩展到包括用户团队。 用户可与团队相关联，或在公司内部门和子部门的层次结构中进行组织。

![公司结构（含部门）](./assets/company-structure-diagram.svg){width="500"}

在店面的公司管理员帐户仪表板中，公司结构表示为树，最初仅由公司管理员组成。

![公司结构，公司管理员为](./assets/company-structure-tree-admin.png){width="700" zoomable="yes"}

对于商家，完整的公司结构反映在管理员中的&#x200B;_公司_&#x200B;和&#x200B;_客户_&#x200B;网格中。 “公司”网格会列出所有公司，而不管其状态如何。

![公司网格](./assets/companies-grid.png){width="700" zoomable="yes"}

以下示例显示带有每个公司的初始公司管理员帐户的[!UICONTROL Customers]网格。

![具有公司管理员帐户的客户网格](./assets/company-admin-user-account.png){width="700" zoomable="yes"}

创建帐户后，公司管理员可以定义包含[团队](account-company-structure.md)的公司结构，设置[公司用户](account-company-users.md)，并为每个用户建立[角色和权限](account-company-roles-permissions.md)。

>[!NOTE]
>
>添加公司用户后，公司用户最初会添加到根公司结构中，从属于公司管理员。 如果公司管理员在公司内执行多个角色，请创建单独的公司用户帐户，并为每个角色使用不同的电子邮件地址。

## 公司结构图标

| 图标 | 描述 |
| ---- | ----------------- |
| ![公司管理员图标](./assets/company-icon-admin.png) | 表示公司结构中的公司管理员。 |
| ![团队图标](./assets/company-icon-team.png) | 表示公司结构中的团队。 |
| ![用户图标](./assets/company-icon-user.png) | 表示公司结构中的用户。 |
| ![移动图标](./assets/company-icon-move.png) | 将团队移至公司结构中的另一个位置。 |
| ![扩展图标](./assets/company-icon-expand.png) | 在公司结构中展开团队。 |
| ![折叠图标](./assets/company-icon-collapse.png) | 折叠公司结构中的团队。 |

{style="table-layout:auto"}

## 创建公司团队

公司帐号的结构应反映采购组织，无论采购组织是简单平整，还是公司各个部门、部门拥有不同团队的复杂组织。

如果商店[配置为](enable-basic-features.md)以允许公司管理自己的帐户，则设置公司结构是公司管理员在帐户获得批准后要完成的首要任务之一。 在公司帐户中，公司结构表示为树状结构，公司管理员位于顶部。

![包含团队的公司结构](./assets/company-structure-teams-diagram.svg){width="450"}

1. 公司管理员登录其帐户。

1. 在左侧面板中，选择&#x200B;**[!UICONTROL Company Structure]**。

1. 在&#x200B;**[!UICONTROL Business Structure]**&#x200B;下，单击&#x200B;**[!UICONTROL Add Team]**&#x200B;并执行以下操作：

   - 输入&#x200B;**[!UICONTROL Team Title]**&#x200B;和&#x200B;**[!UICONTROL Description]**。

     “团队标题”可以是表示公司结构的任何内容，例如团队、办公室或公司内的部门

     ![添加团队](./assets/company-structure-add-team.png){width="700" zoomable="yes"}

   - 完成后，单击&#x200B;**[!UICONTROL Save]**。

   - 根据需要创建任意数量的团队。

1. 要创建团队层次结构，管理员执行以下操作：

   - 选择父团队，然后单击&#x200B;**[!UICONTROL Add Team]**。

     ![公司结构（含部门）](./assets/company-structure-northwest-division.png){width="600" zoomable="yes"}

   - 输入&#x200B;**[!UICONTROL Team Title]**&#x200B;和&#x200B;**[!UICONTROL Description]**。

   - 单击&#x200B;**[!UICONTROL Save]**。

1. 重复这些步骤以根据需要创建尽可能多的团队或部门和细分。

   ![公司结构，包括部门和子部门](./assets/company-structure-divisions.png){width="600" zoomable="yes"}

## 移动团队

当公司管理员处理公司结构时，可以将团队或部门拖到结构中的其他位置。

1. 公司管理员找到要移动的团队。

1. 单击并将团队拖到公司结构中的新位置。

## 删除团队

>[!NOTE]
>
>在删除团队之前，建议确保选择正确的团队 — 无法恢复已删除的团队。

1. 公司管理员选择要删除的团队。

1. 单击&#x200B;**[!UICONTROL Delete Selected]**。

1. 提示确认时，单击&#x200B;**[!UICONTROL Delete]**。

## 展开或折叠团队结构

当公司管理员处理公司结构时，他们可以折叠或展开树：

- 单击&#x200B;**[!UICONTROL Collapse All]**&#x200B;或&#x200B;**[!UICONTROL Expand All]**。

- 单击![展开图标](../assets/icon-display-collapse.png)可折叠团队，单击![折叠图标](../assets/icon-display-expand.png)可展开团队。

## 将用户分配给团队

首次将团队和用户添加到[公司结构](account-company-structure.md)时，它们会被置于公司管理员下的同一级别。

![包含用户和团队的公司结构](./assets/company-users-added.png){width="700" zoomable="yes"}

| 控件 | 描述 |
|--- |--- |
| [!UICONTROL Collapse All / Expand All] | 折叠或展开业务结构树 |
| [!UICONTROL Add User] | 在当前团队下创建用户 |
| [!UICONTROL Add Team] | 创建团队 |
| [!UICONTROL Edit Selected / Remove from Structure] | 编辑用户信息或从业务树中删除用户。 有关详细信息，请参阅[管理公司用户帐户](account-company-users.md)。 |

{style="table-layout:auto"}

1. 在左侧面板中，公司管理员选择&#x200B;**[!UICONTROL Company Structure]**。

1. 要将用户分配给现有团队，他们将用户拖动（![移动图标](../assets/icon-move.png)）到相应的团队下。

   ![团队分配](./assets/company-structure-teams-users-assigned.png){width="700" zoomable="yes"}

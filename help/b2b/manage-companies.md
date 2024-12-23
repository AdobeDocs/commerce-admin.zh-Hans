---
title: 公司管理
description: 简化具有复杂运营模型的B2B组织的管理和管理。
feature: B2B, Companies, Storefront
role: Admin
hide: false
hidefromtoc: false
exl-id: 8246be3d-ff9f-4f9f-875d-1b999befc534
source-git-commit: 6b06f52eb4ee8ca136a1c60fd6dc04a9ac96bbfa
workflow-type: tm+mt
source-wordcount: '313'
ht-degree: 0%

---

# 公司管理

公司管理简化了具有复杂组织结构的公司的业务运营。 管理员用户可以通过将公司分配给指定的母公司来构建公司层次结构以镜像B2B组织。 此分配允许父公司管理员查看和管理组织内的公司。

从&#x200B;*[!UICONTROL Companies]*&#x200B;视图启动公司管理任务。 从管理员转到&#x200B;**[!UICONTROL Customers]** > **[!UICONTROL Companies]**。

![B2B管理公司网格](./assets/companies-grid-view.png){width="700" zoomable="yes"}

*[!UICONTROL Company Type]*&#x200B;列指示公司是作为组织的一部分进行管理，还是作为单独的公司管理。

- `Parent`是一个拥有一个或多个已分配公司的业务组织。 不能将母公司分配为其他公司的子公司。

- `Child`是已分配给组织的公司。 公司只能分配给一个母公司。

- `Company`表示单个公司。 单个公司可以通过将其设为母公司或将其分配给现有母公司而成为组织的一部分。

编辑父公司或子公司时，展开&#x200B;*[!UICONTROL Company Hierarchy]*&#x200B;以查看组织中的所有公司。 `Current`标志表示您正在编辑的公司。

![B2B公司层次结构网格](./assets/company-detail-hierarchy-current-flag.png){width="700" zoomable="yes"}

## 查看和配置[!UICONTROL Company Hierarchy]

在初始公司创建时，*[!UICONTROL Company Hierarchy]*&#x200B;网格为空。 如果公司是单一公司，则此区域也是空的。

![B2B公司层次结构网格](./assets/company-hierarchy-grid.png){width="700" zoomable="yes"}

如果公司是组织的母公司，并且组织中其他公司的公司帐户已在Adobe Commerce中配置，则具有相应权限的管理员用户可以分配公司并使用&#x200B;*[!UICONTROL Company Hierarchy]*&#x200B;网格完成其他公司管理任务：

- 查看与母公司关联的所有公司。
- 从父公司详细信息页面，为组织分配更多公司。
- 使用&#x200B;*[!UICONTROL Unassign from parent]*&#x200B;操作从组织中删除公司。
- 更新&#x200B;*[!UICONTROL Advanced Settings]*&#x200B;配置以将相同的设置应用于多个公司。

有关详细说明，请参阅[管理公司层次结构](manage-company-hierarchy.md)。


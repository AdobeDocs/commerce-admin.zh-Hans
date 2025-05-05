---
title: 共享目录概述
description: 了解Adobe Commerce B2B提供的共享目录，以及如何使用它们为不同的公司帐户维护具有自定义定价的封闭目录。
exl-id: cf7c9099-9b7d-407b-adb9-06a4815624ee
feature: B2B, Companies, Catalog Management
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '595'
ht-degree: 0%

---

# 共享目录概述

Adobe Commerce B2B允许您为不同的公司维护带自定义定价的门控&#x200B;_共享_&#x200B;目录。 除标准&#x200B;_主要_&#x200B;产品目录外，它还允许客户访问具有不同定价结构的两种共享目录。

如果在配置中启用了[共享目录功能](enable-basic-features.md)，则管理员仍可看到原始主目录，但店面中只能看到默认（常规）公共共享目录。 此外，可以创建仅对特定[公司](account-companies.md)帐户成员可见的自定义目录。

对于`Default (General)`公共共享目录，您必须分配产品以在店面中显示该目录。 默认情况下，为空，不包含任何产品。

>[!NOTE]
>
>**[B2B 1.3.0](release-notes.md#b2b-v130)及更高版本** — 在创建共享目录时，对于在目录权限设置中分配了此类访问权限的客户组，目录的每个[类别权限](../catalog/category-permissions.md)均设置为&#x200B;_[!UICONTROL Allow for the Display Product Prices]_&#x200B;和_[!UICONTROL Add to Cart]_。 以前，即使将目录权限设置为`Allow`，这些设置也会自动设置为`Deny`。

>[!IMPORTANT]
>
>启用&#x200B;**_[!UICONTROL Shared Catalog]_**&#x200B;功能后，目录中的&#x200B;**_所有_**&#x200B;类别将忽略所有现有[组权限设置](../configuration-reference/catalog/catalog.md#category-permissions)。 [!UICONTROL Shared Catalog]在启用时完全控制目录中的所有类别权限。

_[!UICONTROL Shared Catalogs]_&#x200B;页提供对用于管理共享目录的工具的访问权限。 该页面类似于标准[管理员工作区](../getting-started/admin-workspace.md)，具有过滤器和操作控件。 网格会列出所有共享目录，包括默认的公共共享目录以及已设置的任何自定义目录。

![共享目录](./assets/shared-catalogs-grid.png){width="700" zoomable="yes"}

## 访问[!UICONTROL Shared Catalogs]页面

在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**。

## 操作控件

左上角的[操作控件](../getting-started/admin-actions-control.md)可与批量操作控件一起使用，以删除不再需要的所选共享目录。 在网格中，_[!UICONTROL Actions]_&#x200B;列包含用于管理共享目录的完整工具选择。

![共享目录操作](./assets/shared-catalog-grid-action-column-controls.png){width="350"}

| 控件 | 描述 |
|------|-----------|
| [[!UICONTROL Set Pricing and Structure]](catalog-shared-pricing-structure.md) | 确定共享目录中可用的产品选择和自定义定价。 |
| [[!UICONTROL Assign Companies]](catalog-shared-assign-companies.md) | 确定哪些公司可以访问共享目录。 |
| [[!UICONTROL General Settings]](catalog-shared-manage.md) | 确定目录详细信息，包括名称、目录类型、客户税分类和说明。 |
| [!UICONTROL Delete] | 删除所选的共享目录。 |

{style="table-layout:auto"}

## 列描述

| 标题 | 描述 |
|--- |--- |
| [!UICONTROL Select] | 选择要应用操作的共享目录记录。 标头中的控件可用于选择网格中的所有共享目录记录或取消选择网格中的所有共享目录记录。 要选择单个共享目录，请选中复选框。 |
| [!UICONTROL ID] | 创建目录时按顺序分配的唯一数字标识符。 |
| [!UICONTROL Name] | 共享目录的名称。 默认情况下，默认（常规）共享目录可用。 |
| [!UICONTROL Type] | 将共享目录的类型标识为： <br/>**[!UICONTROL Public]**— 在安装Adobe Commerce B2B时，将自动创建默认的公共共享目录。 它最初被分配给`General`和`Not Logged In`客户组，并对未与公司关联的来宾和个人登录客户可见。 系统一次仅支持一个公共共享目录。<br/>**[!UICONTROL Custom]** — 自定义共享目录包含的定价仅对分配的公司帐户的登录关联可见。 您可以根据需要创建任意数量的自定义共享目录。 |
| [!UICONTROL Customer Tax Class] | 分配给相应客户组的税分类。 此列未显示在默认网格中，但可通过更改列布局进行添加。 |
| [!UICONTROL Created At] | 创建共享目录的日期和时间。 |
| [!UICONTROL Created By] | 创建共享目录的存储管理员的名字和姓氏。 |
| [!UICONTROL Action] | 列出应用于选定目录的操作。 选项： `Set Pricing and Structure` / `Assign Companies` / `General Settings` / `Delete` |

{style="table-layout:auto"}

---
title: 管理共享目录
description: 了解共享目录页面提供的信息和工具。
exl-id: a01ac292-240d-42e7-b4c9-2982f293c521
feature: B2B, Companies, Catalog Management
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '964'
ht-degree: 0%

---

# 管理共享目录

此 _[!UICONTROL Shared Catalogs]_页面提供管理共享目录所需工具的访问权限。 该页面类似于标准管理员工作区，具有过滤器和操作控件。 网格会列出所有共享目录，包括默认的公共共享目录以及已设置的任何自定义目录。

## 更新产品选择

任何共享目录中的产品选择都可以通过以下位置轻松更新： _[!UICONTROL Action]_共享目录网格的列。 您所做的更改对任何关联公司帐户的成员可见。 该过程基本上与为新产品选择产品相同 [目录结构](catalog-shared-pricing-structure.md)，但配置的范围无法更改。

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**.

1. 对于网格中的共享目录，请转到 **[!UICONTROL Action]** 列并选择 **[!UICONTROL Set Pricing and Structure]**.

   ![共享目录网格和操作菜单](./assets/shared-catalog-set-pricing-structure.png){width="700" zoomable="yes"}

1. 请按照 [步骤2：选择产品](catalog-shared-pricing-structure.md#step-2-choose-the-products).

   您可以跳过第一项，因为共享目录的范围在首次保存后无法更改。

如果您使用特定产品，则 _[!UICONTROL Products In Shared Catalog]_部分列出了产品可用的每个共享目录。 要了解更多信息，请参阅 [将产品添加到共享目录](catalog-shared-product-add.md).

![共享目录中的产品](./assets/shared-catalog-assigned.png){width="600" zoomable="yes"}

## 更新自定义定价

可以从“共享目录”网格的“操作”列轻松更新任何共享目录中的产品的自定义定价。 您所做的更改将在店面中向关联公司或客户组的成员可见。 此过程与为新应用程序设置自定义定价的过程基本相同 [共享目录](catalog-shared-pricing-structure.md)，但配置的范围无法更改。

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**.

1. 对于网格中要更新的共享目录，请转到 **[!UICONTROL Action]** 列并选择 **[!UICONTROL Set Pricing and Structure]**.

1. 在 _[!UICONTROL Catalog Structure]_页面，单击&#x200B;**[!UICONTROL Configure]**并执行以下操作之一：

   - 在页面顶部的进度指示器中，单击 **[!UICONTROL Pricing]**.
   - 在右上角，单击 **[!UICONTROL Next]**.

1. 请按照 [步骤3：设置自定义价格](catalog-shared-pricing-structure.md#step-3-set-custom-prices).

## 更新类别权限

[类别权限](../catalog/category-permissions.md) 自动设置为 `Allow` 从类别树添加到共享目录的产品。 您可以稍后根据需要调整权限或创建其他规则。

>[!NOTE]
>
>**[B2B 1.3.0版](release-notes.md#b2b-v130) 及更高版本**  — 创建共享目录时，每个 [类别权限](../catalog/category-permissions.md) （对于目录），设置为 `Allow` 对于 _[!UICONTROL Display Product Prices]_和_[!UICONTROL Add to Cart]_ 对于在目录权限设置中分配了此访问权限的客户组。 以前，这些设置自动设置为 `Deny` 即使将目录权限设置为 `Allow`.

>[!IMPORTANT]
>
>所有现有 [组权限设置](../configuration-reference/catalog/catalog.md#category-permissions) 被忽略 **_所有_** 目录中的类别，当 **_[!UICONTROL Shared Catalog]_** 功能已启用。 [!UICONTROL Shared Catalog] 完全控制启用目录后目录中的所有类别权限。

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. 在类别树中，选择要更新的产品类别。

   要包含所有产品，请在树中选择顶级类别。

1. 向下滚动并展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Category Permissions]** 部分。

1. 单击 **[!UICONTROL New Permission]** 并执行以下操作：

   ![新建权限](./assets/category-permissions-new.png){width="600" zoomable="yes"}

   - 选择 **[!UICONTROL Customer Group]** 共享目录对应的权限设置，并根据需要更改权限设置。

     ![类别权限规则](./assets/shared-catalog-category-permissions.png){width="600" zoomable="yes"}

   - 要为其他客户组创建权限规则，请单击 **[!UICONTROL New Permissions]** 然后重复这个过程。

   - 要删除权限规则，请单击 _删除_ ![垃圾桶](../assets/icon-delete-trashcan-solid.png) 图标。

1. 完成后，单击 **[!UICONTROL Save]**.

## 更新目录详细信息

可以从“共享目录”网格的“操作”列轻松更新任何共享目录的详细信息。 您所做的更改会反映在任何关联的公司帐户中。

![常规设置](./assets/shared-catalog-grid-general-settings.png){width="700" zoomable="yes"}

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**.

1. 对于要更新的共享目录，请转到 **[!UICONTROL Action]** 列并选择 **[!UICONTROL General Settings]**.

   ![目录详细信息](./assets/shared-catalog-update-details.png){width="600" zoomable="yes"}

1. 根据需要更新目录详细信息。

   - 更改共享目录的名称，也会更改相应客户组的名称。
   - 更改目录类型 `Custom` 到 `Public` 将现有的公共目录转换为自定义目录。 与原始公共目录关联的任何公司都会被重新分配给替代公司。 公共目录无法转换为自定义目录。

1. 完成后，单击 **[!UICONTROL Save]**.

## 共享目录页面引用

### 按钮栏

| 按钮 | 描述 |
|--- |--- |
| [!UICONTROL Back] | 返回到“共享目录”页而不保存新的共享目录。 |
| [!UICONTROL Delete] | 删除目录，并将任何关联公司及其成员重新分配给公共共享目录。 |
| [!UICONTROL Reset] | 清除所有未保存的更改的形式，并恢复原始目录详细信息。 |
| [!UICONTROL Duplicate] | 创建 [目录副本](catalog-shared-create.md). 对于自定义目录，为原始目录的定价模型和结构，但不包括公司关联。 如果公共共享目录重复，则重复目录的类型将更改为 `custom`. 系统还会创建对应的客户组，其名称与重复目录相同。 默认情况下，将命名重复目录 _重复_ 原始目录。 |
| [!UICONTROL Save and Continue Edit] | 保存所有更改，并保持表单在编辑模式下打开。 |
| [!UICONTROL Save] | 保存更改，关闭表单，然后返回到“共享目录”页。 |

{style="table-layout:auto"}

### 目录详细信息

| 字段 | 描述 |
|--- |--- |
| [!UICONTROL Name] | 在整个管理员以及可用目录的客户帐户中标识共享目录。 目录名称应为描述性的，长度不超过32个字符。 不能有两个名称相同的共享目录。 最大字符数：32 |
| [!UICONTROL Type] | **[!UICONTROL Custom]**  — 标识具有自定义定价的目录，该目录仅对分配该目录的特定公司可用。<br/>**[!UICONTROL Public]**— 标识可供所有来宾访客以及未与公司关联的已登录客户使用的共享目录。 安装B2B for Adobe Commerce时会创建“默认”公共共享目录，但必须由管理员配置。 一次只能存在一个公共共享目录。 |
| [!UICONTROL Customer Tax Class] | 确定用于从目录采购的税分类。 这些选项包括所有可用的税分类。 |
| [!UICONTROL Description] | 有关如何使用目录的简要说明。 |

{style="table-layout:auto"}

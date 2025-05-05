---
title: 创建共享目录
description: 了解如何创建共享目录和复制现有的共享目录。
exl-id: 969c352c-ff88-4902-8347-334ee8b79afb
feature: B2B, Companies, Catalog Management
role: Admin
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '871'
ht-degree: 0%

---

# 创建共享目录

创建[共享目录](catalog-shared.md)时，系统自动创建具有相同名称的[客户组](account-company-customer-group.md)。 例如，如果您创建名为&#x200B;_ABC目录_&#x200B;的共享目录，则系统还会创建相应的&#x200B;_ABC目录_&#x200B;客户组。 将公司分配给共享自定义目录与将公司分配给客户组大致相同。

新的共享目录不包括产品、自定义定价或公司关联。 公共目录（启用共享目录时创建的默认共享目录）会自动分配给来宾以及未与公司关联的客户。

![共享目录](./assets/shared-catalogs-grid.png){width="700" zoomable="yes"}

必须先设置共享目录的以下方面，然后才能使用它：

- 目录范围
- 产品选择
- 自定义价格
- 公司分配

## 价格范围

如果您安装的是多站点，请确保在创建共享目录之前配置价格范围。 [价格范围](../catalog/catalog-price-scope.md)可以设置为`Global`或`Website`。 但是，只能在设置过程开始时设置它。 网站选择器出现在[共享目录设置](catalog-shared-pricing-structure.md)的步骤2中。

![网站选择器](./assets/shared-catalog-scope-pricing.png){width="600" zoomable="yes"}

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧面板中，展开&#x200B;**目录**&#x200B;并在下面选择&#x200B;**目录**。

1. 展开&#x200B;**价格**&#x200B;部分的![扩展选择器](../assets/icon-display-expand.png)。

1. 将&#x200B;**目录价格范围**&#x200B;设置为`Website`。

   ![目录价格范围](../configuration-reference/catalog/assets/catalog-price.png){width="600" zoomable="yes"}

1. 单击&#x200B;**[!UICONTROL Save Config]**。

## 第1步：创建共享目录

创建共享目录的方法有两种。 您可以创建任一类型的共享目录，也可以复制现有的共享目录。 新的共享目录不包含任何产品，且尚未分配给公司。

### 方法1：添加新共享目录

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**。

1. 单击右上角的&#x200B;**[!UICONTROL Add Shared Catalog]**&#x200B;并执行以下操作：

   - 为共享目录输入&#x200B;**[!UICONTROL Name]**。

     您分配的名称将在管理员和客户控制面板中使用（如果适用）以引用共享目录。 它还会成为相应的客户组的名称。

   - 选择&#x200B;**[!UICONTROL Type]** ： `Custom`或`Public`。

   - 选择适用于从共享目录进行的购买的相应&#x200B;**[!UICONTROL Customer Tax Class]**。

     有关税分类设置和定义的详细信息，请参阅[税分类](../stores-purchase/tax-class.md)。

     以下示例显示了一个适用于特定批发客户的新自定义目录。

     ![新共享目录](./assets/shared-catalog-new.png){width="600" zoomable="yes"}

   - 输入&#x200B;**[!UICONTROL Description]**

1. 完成后，单击&#x200B;**[!UICONTROL Save]**。

   新目录显示在&#x200B;_[!UICONTROL Shared Catalogs]_&#x200B;网格中。

### 方法2：复制现有的共享目录

重复的自定义目录会保留原始目录的定价模型和结构，但不保留公司关联。 系统还会创建对应的客户组，其名称与重复目录相同。 默认情况下，重复的目录在原始目录中名为&#x200B;_Duplicate of_。

如果公共共享目录重复，则重复目录的类型将更改为`custom`。

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**。

1. 对于网格中要复制的共享目录，转到&#x200B;**[!UICONTROL Action]**&#x200B;列并选择&#x200B;**[!UICONTROL General Settings]**。

1. 在页面顶部的选项中，单击&#x200B;**[!UICONTROL Duplicate]**。

   ![重复的共享目录](./assets/shared-catalog-duplicate.png){width="600" zoomable="yes"}

1. 为新目录更新以下字段：

   - **[!UICONTROL Name]**
   - **[!UICONTROL Type]**
   - **[!UICONTROL Customer Tax Class]**
   - **[!UICONTROL Description]**

1. 完成后，单击&#x200B;**[!UICONTROL Save]**。

   此重复项显示在&#x200B;_[!UICONTROL Shared Catalogs]_&#x200B;网格中，具有唯一的ID。

## 第2步：完成设置

创建新共享目录后，必须为它配置相应的产品选择、[公司分配](catalog-shared-assign-companies.md)和[类别权限](../catalog/category-permissions.md)。 若要继续，请参阅[设置定价和结构](catalog-shared-pricing-structure.md)。

>[!NOTE]
>
>**[B2B 1.3.0](release-notes.md#b2b-v130)及更高版本** — 在创建共享目录时，对于在目录权限设置中分配了此类访问权限的客户组，目录的每个[类别权限](../catalog/category-permissions.md)均设置为&#x200B;_[!UICONTROL Allow for the Display Product Prices]_&#x200B;和_[!UICONTROL Add to Cart]_。 以前，即使将目录权限设置为`Allow`，这些设置也会自动设置为`Deny`。

## 共享目录演示

要查看共享目录管理的演示，请观看此视频：

>[!VIDEO](https://video.tv.adobe.com/v/3410751?quality=12&learn=on&captions=chi_hans)

## 共享目录页面引用

### 按钮栏

| 按钮 | 描述 |
|--- |--- |
| [!UICONTROL Back] | 返回到“共享目录”页而不保存新的共享目录。 |
| [!UICONTROL Reset] | 清除所有未保存的更改的形式，并恢复原始目录详细信息。 |
| [!UICONTROL Save and Continue Edit] | 保存所有更改，并保持表单在编辑模式下打开。 |
| [!UICONTROL Save] | 保存更改，关闭表单，然后返回到“共享目录”页。 |

{style="table-layout:auto"}

### 目录详细信息

| 字段 | 描述 |
|--- |--- |
| [!UICONTROL Name] | 在整个管理员以及可用目录的客户帐户中标识共享目录。 目录名称应为描述性的，长度不超过32个字符。 不能有两个名称相同的共享目录。 最大字符数：32 |
| [!UICONTROL Type] | **[!UICONTROL Custom]** — 标识具有自定义定价的目录，该目录仅对分配该目录的特定公司可用。<br/>**[!UICONTROL Public]**— 标识可供所有来宾访客以及未与公司关联的登录客户使用的共享目录。 安装[!DNL Adobe Commerce B2B]时创建默认公共共享目录，但必须由存储管理员配置。 一次只能存在一个公共共享目录。 |
| [!UICONTROL Customer Tax Class] | 确定用于从目录采购的税分类。 这些选项包括所有可用的税分类。 |
| [!UICONTROL Description] | 有关如何使用目录的简要说明。 |

{style="table-layout:auto"}

### 网格列

| 字段 | 描述 |
|--- |--- |
| [!UICONTROL ID] | 分配给共享目录实体的唯一数字标识符。 |
| [!UICONTROL Name] | 共享目录的名称。 |
| [!UICONTROL Type] | 指示共享目录的类型。 可以是`Public`或`Custom`。 |
| [!UICONTROL Created At] | 在系统中创建共享目录的日期。 |
| [!UICONTROL Created By] | 创建共享目录的管理员用户的名称。 |
| [!UICONTROL Action] | 操作列表。 选项： `Set Pricing and Structure`、`Assign Companies`、`General Settings`、`Delete`。 |

{style="table-layout:auto"}

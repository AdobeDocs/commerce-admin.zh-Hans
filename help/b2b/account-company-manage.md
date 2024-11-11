---
title: 管理公司帐户
description: 了解如何使用公司页面和网格中可用的工具管理Adobe Commerce商店的公司帐户。
exl-id: 9e125fc2-d20e-463e-a391-582fa0bcb68d
feature: B2B, Companies, Configuration
source-git-commit: d930c2294f0313cfa36d81c8a153b3cb35183f85
workflow-type: tm+mt
source-wordcount: '2726'
ht-degree: 0%

---

# 管理公司帐户

_[!UICONTROL Companies]_页面列出了所有当前公司帐户，无论状态如何。 任何待处理的审批请求都将显示在列表顶部。

![公司网格](./assets/companies-grid-view.png){width="700" zoomable="yes"}

使用&#x200B;*[!UICONTROL Columns]*&#x200B;控件自定义网格中显示的列。 使用搜索和筛选功能自定义视图中显示的公司。

- 使用&#x200B;_[!UICONTROL Search]_在&#x200B;**公司**网格中查找公司。 搜索对&#x200B;**公司名称**和&#x200B;**父项**列编制索引。

- 使用[!UICONTROL Filter]自定义视图以包含符合特定条件的记录。 例如，如果B2B站点配置为同时管理单个公司帐户和[公司层次结构](manage-companies.md)，则可以按`[!UICONTROL Company Type - Company]`进行筛选以仅显示单个公司，或按`[!UICONTROL Company Type - Parent]`进行筛选以仅显示每个层次结构的父公司。

使用网格上方的&#x200B;_[!UICONTROL Actions]_控件将操作应用到多个公司记录。 例如，您可以选择多个请求来在单个操作中激活帐户，而不是批准每个公司请求。 可用的操作取决于分配给管理员用户帐户的角色的[权限](../systems/permissions.md)。

## 公司角色资源

[角色资源](../systems/permissions-user-roles.md#role-resources)设置确定以下能力：

- 添加公司
- 删除公司
- 应用余额报销
- 查看公司

必须为分配给管理员用户帐户的[用户角色](../systems/permissions-user-roles.md)设置这些角色资源。

## 从“公司”网格管理公司帐户

通过选择&#x200B;**[!UICONTROL Customers]** > **[!UICONTROL Companies]**&#x200B;以打开&#x200B;*[!UICONTROL Companies]*&#x200B;页面，从“管理员”菜单中查看和管理公司的用户帐户。

您可以单独管理帐户，也可以按组管理帐户。

- 通过在公司帐户记录的&#x200B;**[!UICONTROL Action]**&#x200B;列中选择&#x200B;**[!UICONTROL Edit]**，查看或更改单个公司帐户的配置设置。

  ![选择要应用于选定公司的操作](assets/companies-change-settings-edit-selection.png){width="675" zoomable="yes"}

- 使用网格上方的[!UICONTROL Actions]控件中的可用选项查看或更改一组选定的公司帐户**

  ![选择要应用于选定公司的操作](assets/companies-change-settings-mass-action-selection.png){width="675" zoomable="yes"}

有关应用每个操作的说明，请参阅以下部分。

### 激活公司帐户

1. 从&#x200B;**[!UICONTROL Actions]**&#x200B;控件中选择&#x200B;**[!UICONTROL Set Active]**。

1. 提示确认时，单击&#x200B;**[!UICONTROL OK]**。

### 设置活动/不活动

具有非活动帐户的客户无法登录或从他们的帐户中进行购买。 可使用以下两种方法将客户帐户设置为活动或非活动：

方法1：来自客户网格&#x200B;**的**

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;[!UICONTROL **客户**] > [!UICONTROL **所有客户**]。

1. 从&#x200B;**[!UICONTROL Actions]**&#x200B;菜单中，选择以下选项之一：

   - **[!UICONTROL Active]**
   - **[!UICONTROL Inactive]**

1. 出现提示时，选择&#x200B;**[!UICONTROL OK]**&#x200B;以应用更改。

方法2：**从帐户编辑页**

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;[!UICONTROL **客户**] > [!UICONTROL **所有客户**]。

1. 在网格中，查找要编辑的客户记录。

1. 在最右侧的&#x200B;_操作_&#x200B;列中，选择&#x200B;[!UICONTROL **编辑**]。

1. 选择&#x200B;[!UICONTROL **帐户信息**]&#x200B;选项卡。

1. 将&#x200B;[!UICONTROL **客户活动**]&#x200B;设置为`Yes`或`No`。

1. 单击&#x200B;[!UICONTROL **保存客户**]。

### 阻止公司帐户

与被阻止的公司帐户关联的用户可以登录并访问目录，但不能进行购买。 如果一家公司的账号不能正常运作，公司可能会被暂时封锁，直到问题得到解决。

1. 从&#x200B;**[!UICONTROL Actions]**&#x200B;控件中选择&#x200B;**[!UICONTROL Block]**。

1. 提示确认时，单击&#x200B;**[!UICONTROL OK]**。

### 删除公司帐户

无法恢复已删除的公司帐户。 与公司关联的用户帐户状态设置为`Inactive`，并且公司ID将从用户帐户的配置文件中删除。 有关公司活动和交易的信息保留在系统中。

1. 从&#x200B;**[!UICONTROL Actions]**&#x200B;控件中选择&#x200B;**[!UICONTROL Delete]**。

1. 提示确认时，单击&#x200B;**[!UICONTROL OK]**。

### 更改公司设置

更新[高级设置](account-company-create.md#advanced-settings)配置以将相同的设置应用到&#x200B;*公司网格*&#x200B;上选择的多个公司。

>[!NOTE]
>
>从[公司层次结构视图](manage-company-hierarchy.md#change-company-settings)管理具有父公司和关联子公司的公司组织的高级设置配置。

1. 从&#x200B;**[!UICONTROL Actions]**&#x200B;控件中选择&#x200B;**[!UICONTROL Change company settings]**。

   在&#x200B;*[!UICONTROL Change company settings]*&#x200B;窗体上，初始配置设置设为默认值。

1. 对于每个要更改的配置设置，选中&#x200B;**[!UICONTROL Change]**&#x200B;复选框以启用该设置。 然后，根据需要更新设置。

   ![更改多个公司的公司设置](assets/companies-change-advanced-settings-action.png){width="675" zoomable="yes"}

1. 更新配置设置后，选择&#x200B;**[!UICONTROL Apply Changes]**。

1. 出现提示时，选择&#x200B;**[!UICONTROL Change settings]**&#x200B;以更新所选公司的配置。

>[!TIP]
>
>您可以通过选择公司帐户记录的&#x200B;**[!UICONTROL Action]**&#x200B;列中的&#x200B;**[!UICONTROL Edit]**&#x200B;来更改单个公司的高级设置配置。

### 转换贷方货币

所选公司帐户中的贷项将转换为所选货币的当前汇率。

1. 从&#x200B;**[!UICONTROL Actions]**&#x200B;控件中选择&#x200B;**[!UICONTROL Convert Currency]**。

1. 提示确认时，单击&#x200B;**[!UICONTROL OK]**。

1. 选择要用于所选公司帐户的&#x200B;**[!UICONTROL Credit Currency]**。

   金额根据现行兑换率（如有）重新计算。 如果不可用，您可以手动输入自定义转化率。 系统将显示所选公司使用的信用货币所需的兑换计算数量。

1. 单击&#x200B;**[!UICONTROL Proceed]**&#x200B;以完成转换。

## 编辑公司帐户

方法1： **快速编辑**

1. 在第一列中，选中要编辑的公司帐户的复选框。

1. 从&#x200B;**[!UICONTROL Actions]**&#x200B;控件中选择&#x200B;**[!UICONTROL Edit]**。

   每个可更新的值都会显示在文本框中。

   公司帐户![快速编辑](./assets/companies-grid-quick-edit.png){width="675" zoomable="yes"}

1. 根据需要更新以下任意值：

   - **[!UICONTROL Company Name]**

   - **[!UICONTROL Company Email]**

   - **[!UICONTROL Phone Number]**

1. 单击&#x200B;**[!UICONTROL Save]**。

方法2：**完全编辑**

1. 在网格中，查找要编辑的公司记录。

1. 从&#x200B;_[!UICONTROL Action]_列中选择&#x200B;**[!UICONTROL Edit]**。

1. 对公司信息进行必要的更改。

   有关字段说明，请参阅[创建公司帐户](account-company-create.md)。

1. 完成后，单击&#x200B;**[!UICONTROL Save]**。

## 分配销售代表

销售代表是[管理员用户](../systems/permissions.md)，被分配为公司帐户的联系人，并接收与公司相关的所有自动[电子邮件](../b2b/enable-basic-features.md#configure-company-email-options)。 每个公司帐户只能分配一个销售代表，但单个销售代表可以管理多个公司帐户。 除非分配了其他管理员用户，否则默认管理员用户帐户将被分配为销售代表。

公司帐户和报价页中的公司成员可以看到已分配销售代表的姓名和电子邮件地址。

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Customers]** > **[!UICONTROL Companies]**。

1. 在网格中查找公司，并以编辑模式打开。

1. 将&#x200B;**[!UICONTROL Sales Representative]**&#x200B;设置为要指定为公司联系点的管理员用户。

1. 完成后，单击&#x200B;**[!UICONTROL Save]**。

   分配的销售代表会收到分配的电子邮件通知。

## 更新公司配置文件

公司配置文件可由公司管理员从店面维护，也可由店面管理员从管理员进行维护。

![公司配置文件](./assets/company-update.png){width="700" zoomable="yes"}

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Customers]** > **[!UICONTROL Companies]**。

1. 在网格中查找公司，然后单击&#x200B;_[!UICONTROL Action]_列中的&#x200B;**[!UICONTROL Edit]**。

1. 使用字段描述根据需要更新每个部分中的字段值，以供参考。

1. 完成后，单击&#x200B;**[!UICONTROL Save]**。

## 公司帐户演示

通过观看以下视频，您可以了解有关管理公司帐户的信息：

>[!VIDEO](https://video.tv.adobe.com/v/344447?quality=12)

## 公司管理

创建公司后，具有相应权限的管理员用户可以使用[!UICONTROL Company Hierarchy]部分通过编辑指定的母公司并分配相关公司来构建母公司组织。

如果已将公司添加到层次结构，则[!UICONTROL Company Hierarchy]网格将显示父公司和网格中所有分配的公司。

有关详细信息，请参阅[管理公司层次结构](manage-company-hierarchy.md)。

## 公司选项和列

以下各节提供了可用于管理公司帐户的可用操作、选项和显示信息的参考。

### 操作控制选项

| 选项 | 描述 |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Set Active] | 将所有选定公司记录的状态设置为`Active`。 公司管理员将收到设置密码的说明，这样他们就可以从店面访问帐户和管理公司。 |
| [!UICONTROL Block] | 限制信誉不佳的公司帐户，同时保留帐户。 公司成员可以登录并访问目录，但不能代表公司下订单。 |
| [!UICONTROL Delete] | 删除所选的公司帐户。 与已删除的公司关联的用户帐户状态设置为`Inactive`，并且公司ID将从用户帐户的配置文件中删除。 有关公司活动和交易的信息保留在系统中。 |
| [!UICONTROL Edit] | 允许从网格编辑所选公司记录的某些值。 默认情况下，公司名称、公司电子邮件和电话号码值可用于快速编辑。 |
| [!UICONTROL Change company settings] | 打开&#x200B;*更改公司设置*&#x200B;表单以更新[高级设置](account-company-create.md#advanced-settings)配置并将更改应用于所选公司。 |
| [!UICONTROL Convert Credit] | 根据指定货币的汇率换算所选公司的记帐贷项。 |

{style="table-layout:auto"}

### 列描述


#### 默认列布局

| 列 | 描述 |
|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Select] | 用于选择要作为操作主体的公司记录或使用列标题中的选择控件来选择/取消选择所有内容的复选框。 |
| [!UICONTROL ID] | 提交创建公司的请求时分配的唯一数字标识符。 |
| [!UICONTROL Company Name] | 公司名称在首次创建公司帐户时输入，可以是完整法律名称的缩写版本。 |
| [!UICONTROL Company Type] | [公司](manage-companies.md)的类型。 选项： <br/>**[!UICONTROL Company]**— 默认情况下，新公司是作为单个公司创建的。<br/>**[!UICONTROL Parent]** — 该公司是其他公司的母公司。 <br/>**[!UICONTROL Child]**— 此公司与母公司相关。 |
| [!UICONTROL Parent] | 显示此特定公司行的母公司。 |
| [!UICONTROL Company Email] | 与公司帐户关联的电子邮件地址。 |
| [!UICONTROL Phone Number] | 公司的主要电话号码。 |
| [!UICONTROL Country] | 公司注册经营的国家/地区。 |
| [!UICONTROL State Province] | 公司注册地所在国家或省。 |
| [!UICONTROL City] | 公司注册地城市，开展业务。 |
| [!UICONTROL Group/Shared Catalog] | 列名称取决于配置中是否启用了共享目录。 选项： <br/>**[!UICONTROL Customer Group]**— 如果未在配置中启用共享目录，请指定公司所属的[客户组](../customers/customer-groups.md)的名称。<br/>**[!UICONTROL Shared Catalog]** — 如果在配置中启用了共享目录，请指定分配给客户的共享目录的名称。 |
| [!UICONTROL Outstanding Balance] | 公司帐户中的未清余额。 如果公司没有信用记录，并且信用限额为零，则该列为空。 |
| [!UICONTROL Company Admin] | 公司管理员的名字和姓氏。 |
| [!UICONTROL Job Title] | 公司管理员的职务。 |
| [!UICONTROL Work Phone Number] | 公司管理员的工作电话号码。 |
| [!UICONTROL Email] | 公司管理员的电子邮件地址。 |
| [!UICONTROL Action] | **[!UICONTROL Edit]** — 在编辑模式下打开公司帐户。 |

{style="table-layout:auto"}

#### 其他列

可通过更改网格的[列布局](../getting-started/admin-grid-controls.md)来使用以下列。

| 列 | 描述 |
|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Company Legal Name] | 公司的完整法定名称。 |
| [!UICONTROL Street Address] | 公司开展业务的注册街道地址。 |
| [!UICONTROL ZIP] | 公司注册开展业务的邮政编码。 |
| [!UICONTROL Reseller ID] | 为纳税申报目的而分配给公司的转售编号。 |
| [!UICONTROL VAT/TAX ID] | 某些管辖区为报税目的而分配给公司的[增值税](../stores-purchase/vat.md)编号。 要将客户VAT/TAX ID配置为显示在店面，请参阅[新建帐户选项](../configuration-reference/customers/customer-configuration.md)。 |
| [!UICONTROL Credit Limit] | 扩展到公司帐户的信用额度。 |
| [!UICONTROL Credit Currency] | 商店接受以公司贷记进行购买的货币。 |
| [!UICONTROL Status] | 指示公司帐户的[状态](account-company-approve.md)。 选项： <br/>**[!UICONTROL Active]**— 公司帐户由存储管理员批准。 公司管理员和关联成员可以从店面登录帐户并进行购买。<br/>**[!UICONTROL Pending Approval]** — 已提交打开公司帐户的请求，但尚未获得商店管理员的批准。 <br/>**[!UICONTROL Rejected]**— 已提交打开公司帐户的请求，但未获得商店管理员的批准。 用于提交请求的初始登录凭据被阻止。<br/>**[!UICONTROL Blocked]** — 公司成员可以登录并访问目录，但不能进行购买。 商店管理员可能会阻止信誉不佳的公司帐户。 商店管理员可随时删除帐户上的块。 |
| [!UICONTROL Gender] | 公司管理员的性别。 选项：男/女/未指定 |
| [!UICONTROL Comment] | 公司帐户的相关注释，以供参考并仅从管理员处可见。 |

{style="table-layout:auto"}

### 按钮栏

| 按钮 | 描述 |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Back] | 返回到“公司”页而不保存更改。 |
| [!DNL Delete Company] | 删除公司帐户。 与公司关联的用户帐户状态设置为`Inactive`，并且公司ID将从用户帐户的配置文件中删除。 有关公司活动和交易的信息保留在系统中。 |
| [!DNL Reset] | 将原始值还原到具有未保存更改的任何字段。 |
| [!DNL Reimburse Balance] | 允许管理员根据采购单编号偿还商店贷项的余额。 |
| [!DNL Save] | 将更改保存到公司并保持配置文件打开。 |
| [!UICONTROL Save & Close] | 保存对公司所做的更改并关闭用户档案。 |

{style="table-layout:auto"}

### 字段描述

| 字段 | 描述 |
|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Company Name] | 公司名称在首次创建公司帐户时输入，可以是完整法律名称的缩写版本。 |
| [!UICONTROL Status] | 指示公司帐户的[状态](account-company-approve.md)。 选项： <br/>**[!UICONTROL Active]**— 公司帐户由存储管理员批准。 公司管理员和关联成员可以从店面登录帐户并进行购买。<br/>**[!UICONTROL Pending Approval]** — 已提交打开公司帐户的请求，但尚未获得商店管理员的批准。 <br/>**[!UICONTROL Rejected]**— 已提交打开公司帐户的请求，但未获得商店管理员的批准。 用于提交请求的初始登录凭据被阻止。<br/>**[!UICONTROL Blocked]** — 公司成员可以登录并访问目录，但不能进行购买。 商店管理员可能会阻止信誉不佳的公司帐户。 商店管理员可随时删除帐户上的块。 |
| [!UICONTROL Company Email] | 与公司帐户关联的电子邮件地址。 |
| [!UICONTROL Sales Representative] | 公司帐户的主要联系人管理员用户。 |

{style="table-layout:auto"}

#### [!UICONTROL Account Information]

| 字段 | 描述 |
|---------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Company Legal Name] | 公司的完整法定名称。 |
| [!UICONTROL VAT / TAX ID] | 为报税目的而分配给公司的税或[增值税](../stores-purchase/vat.md)编号。 |
| [!UICONTROL Reseller ID] | 为纳税申报目的而分配给公司的转售编号。 |
| [!UICONTROL Comment] | 有关公司帐户的这些注释仅供管理员参考和查看。 |

{style="table-layout:auto"}

#### [!UICONTROL Company Hierarchy]

| 列 | 描述 |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Company ID] | 公司的ID号。 |
| [!UICONTROL Company Name] | 公司的全名。 <br/>正在编辑的公司行中出现一个`current company indicator`。 |
| [!UICONTROL Company Email] | 与公司帐户关联的电子邮件地址。 |
| [!UICONTROL Phone Number] | 公司的主要电话号码。 |
| [!UICONTROL State/Province] | 公司注册地所在国家或省。 |
| [!UICONTROL City] | 公司注册地城市，开展业务。 |
| [!UICONTROL Customer Group] | （仅限管理员）指示分配给公司的[客户组](../customers/customer-groups.md)或[共享目录](catalog-shared.md)。 |
| [!UICONTROL Company Admin] | 公司管理员的全名。 |
| [!UICONTROL Action] | 公司行可能执行的操作列表。 |

{style="table-layout:auto"}

#### [!UICONTROL Legal Address]

| 列 | 描述 |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Street Address] | 公司开展业务的注册街道地址。 |
| [!UICONTROL City] | 公司注册地城市，开展业务。 |
| [!UICONTROL Country] | 公司注册经营的国家/地区。 |
| [!UICONTROL State/Province] | 公司注册地所在国家或省。 |
| [!UICONTROL ZIP/Postal Code] | 公司注册开展业务的邮政编码。 |
| [!UICONTROL Phone Number] | 公司的主要电话号码。 |

{style="table-layout:auto"}

#### [!UICONTROL Company Admin]

| 字段 | 描述 |
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Website] | 为公司帐户设置[网站范围](../getting-started/websites-stores-views.md)。 默认为&#x200B;*[!UICONTROL Main Website]*。 |
| [!UICONTROL Job Title] | 管理公司帐户的公司管理员的职务。 |
| [!UICONTROL Work Phone Number] | 管理公司帐户的公司管理员的电话号码。 |
| [!UICONTROL Email] | 公司管理员的电子邮件地址可以与公司电子邮件地址相同。 如果输入了不同的电子邮件地址，则除了公司帐户外，还会为公司管理员创建单独的个人帐户。 |
| [!UICONTROL Prefix] | 如果适用，与公司管理员的姓名关联的前缀（如`Mr.`、`Ms.`、`Mrs.`或`Dr.`）。 根据配置，输入字段可能是文本字段或列表。 |
| [!UICONTROL First Name] | 公司管理员的名字。 |
| [!UICONTROL Middle Name/Initial] | 公司管理员的中间名或首字母。 |
| [!UICONTROL Last Name] | 公司管理员的姓氏。 |
| [!UICONTROL Suffix] | 如果适用，则为与公司管理员的姓名关联的后缀（如`Jr.`、`Sr.`或`III`）。 根据配置，输入字段可能是文本字段或列表。 |
| [!UICONTROL Gender] | 公司管理员的性别。 选项： `Male` / `Female` / `Not Specified` |
| [!UICONTROL Send Welcome Email From] | 设置向新公司管理员发送欢迎电子邮件时要使用的存储审阅（如果您不想使用&#x200B;*[!UICONTROL Default Store View]*）。 |

{style="table-layout:auto"}

#### [!UICONTROL Company Credit]

| 字段 | 描述 |
|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Credit Currency] | 商店接受以公司贷记进行购买的货币。 |
| [!UICONTROL Credit Limit] | 扩展到公司帐户的信用额度。 |
| [!UICONTROL Allow to Exceed Credit Limit] | 指示公司是否有权超出信用额度。 选项：是/否 |
| [!UICONTROL Reason for Change] | 说明公司在哪些情况下可以或不能超过信贷限额的注释。 仅当超出信用限制的权限发生变化时，此字段才处于活动状态。 |

{style="table-layout:auto"}

#### [!UICONTROL Advanced Settings]

| 字段 | 描述 |
|-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Customer Group] | 指示分配给公司的[客户组](../customers/customer-groups.md)或[共享目录](catalog-shared.md)。 |
| [!UICONTROL Allow Quotes] | 确定公司成员是否可以代表公司准备并提交可协商报价。 |
| [!UICONTROL Enable Purchase Orders] | 确定公司是否允许采购订单。 要使采购订单适用于公司成员帐户，公司管理员还必须在店面中启用此功能。 |
| [!UICONTROL Applicable Payment Methods] | 指示可用于公司购买的支付方式。 选项： `B2B Payment Methods` / `All Enabled Payment Methods` / `Specific Payment Methods` |
| [!UICONTROL Payment Methods] | （仅限管理员）如果指定了特定的支付方式，则变为活动状态。 要选择多种支付方式，请按住Ctrl键(PC)或Command键(Mac)并单击每个选项。 |

{style="table-layout:auto"}

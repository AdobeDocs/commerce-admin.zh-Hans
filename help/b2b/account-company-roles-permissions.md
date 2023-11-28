---
title: 公司角色和权限
description: 了解公司管理员可应用于公司用户的角色和权限，允许对订单信息和资源进行各种级别的访问。
exl-id: 9fe20d6a-2c9c-4618-a395-805d64dcf0de
feature: B2B, Companies, Roles/Permissions
role: Admin
source-git-commit: 03d1892799ca5021aad5c19fc9f2bb4f5da87c76
workflow-type: tm+mt
source-wordcount: '595'
ht-degree: 0%

---

# 公司角色和权限

公司用户的角色被设置为具有访问销售信息和资源的各种级别权限。 默认情况下，公司管理员是 _超级用户_ 具有完全权限。 此 [访问被拒绝](../content-design/pages.md#access-denied) 如果用户没有访问该页面的权限，则会显示该页面。

![具有默认角色的“角色和权限”页面](./assets/company-roles-permissions.png){width="700" zoomable="yes"}

系统具有一个预定义的默认用户角色，您可以使用该角色 _原样_ 或修改以符合您的需要。 您可以根据需要创建任意数量的角色，以匹配您的公司结构和组织职责，如下所示：

- **默认用户**  — 默认用户具有对与销售和报价相关的活动的完全访问权限，以及对公司配置文件和信用信息的仅查看访问权限。

- **高级买家**  — 高级购买者可能有权访问所有“销售”和“报价”资源，并且有权仅查看公司配置文件、用户和团队、支付信息和公司业绩。

- **助理购买者**  — 助理购买者可能有权使用以下方式下订单： _使用引号结帐_，并在公司配置文件中查看订单、报价和信息。

## 管理角色和权限

1. 公司管理员登录其商店帐户。

1. 在左侧面板中，选择 **[!UICONTROL Roles and Permissions]**.

1. 完成以下任一任务。

### 创建角色

1. 点击次数 **[!UICONTROL Add New Role]**.

   ![添加新角色](./assets/company-roles-permissions-add-storefront.png){width="600" zoomable="yes"}

1. 输入描述性 **[!UICONTROL Role Name]**.

1. 下 _[!UICONTROL Role Permissions]_，执行以下操作之一：

   - 选中分配了角色的用户有权访问的每个资源或活动的复选框。

   - 选择 **[!UICONTROL All]** 复选框，并清除分配给该角色的用户无权访问的每个资源或活动的复选框。

1. 点击次数 **[!UICONTROL Save Role]**.

1. 重复这些步骤，根据需要创建任意数量的角色。

### 修改角色

1. 对于要修改的角色，公司管理员单击 **[!UICONTROL Edit]** 在 _[!UICONTROL Actions]_列。

1. 对名称和权限设置进行必要的更改。

1. 完成后，单击 **[!UICONTROL Save Role]**.

### 复制角色

1. 对于要复制的角色，公司管理员单击 **[!UICONTROL Duplicate]** 在 _[!UICONTROL Actions]_列。

1. 对名称和权限设置进行必要的更改。

1. 完成后，单击 **[!UICONTROL Save Role]**.

### 删除角色

1. 公司管理员在角色列表中找到要删除的角色。

   只能删除未分配用户的角色。

1. 点击次数 **[!UICONTROL Delete]** 在 _[!UICONTROL Actions]_列。

1. 提示确认时，单击 **[!UICONTROL OK]**.

## 操作

| 操作 | 描述 |
|-----------| ----------- |
| [!UICONTROL Duplicate] | 创建所选角色的副本。 重复角色的名称具有 `- Duplicated` 已添加到末尾。 |
| [!UICONTROL Edit] | 更改名称和/或权限集。 |
| [!UICONTROL Delete] | 删除角色。 只能删除未分配用户的角色。 |

{style="table-layout:auto"}

## 角色权限

- 全部
   - 销售
      - 允许结帐（下单）
         - 使用分期付款方法
      - 查看订单
         - 查看下属用户的订单
- 引号
   - 视图
      - 请求、编辑、删除
      - 使用引号结帐
      - 查看下属用户的引号
- 订单审批
   - 查看我的采购订单
      - 下属视图
      - 查看所有公司
   - 自动批准在此角色中创建的PO
   - 审批没有其他审批的采购订单
   - 查看审批规则
      - 创建、编辑和删除
- 公司配置文件
   - 帐户信息（视图）
      - 编辑
   - 合法地址
      - 编辑
   - 联系人（查看）
   - 付款信息（查看）
   - 送货信息（视图）
- 公司用户管理
   - 查看角色和权限
      - 管理角色和权限
   - 查看用户和团队
      - 管理用户和团队
- 公司信用
   - 视图

## 将角色分配给公司用户

定义所需的角色后，公司管理员会为每个公司用户分配一个角色。

1. 以公司管理员身份登录到他们的公司帐户。

1. 在左侧面板中，选择 **[!UICONTROL Company Users]**.

   ![公司用户](./assets/company-users-list-storefront.png){width="700" zoomable="yes"}

1. 在列表中查找用户并单击 **[!UICONTROL Edit]**.

1. 选择合适的 **[!UICONTROL User Role]** 对于用户。

   ![编辑用户 — 选择用户角色](./assets/company-user-assign-role.png){width="700" zoomable="yes"}

1. 点击次数 **[!UICONTROL Save]**.

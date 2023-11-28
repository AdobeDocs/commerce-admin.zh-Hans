---
title: 为购物者提供帮助
description: 使用“作为客户登录”功能时，您可以看到客户看到的内容，并代表他们进行更新。
exl-id: 6842ae7a-6440-45f1-af18-e6427088d29d
feature: Customers, Customer Service
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '587'
ht-degree: 0%

---

# 为购物者提供帮助

有时，客户需要帮助来安排订单。 商店管理员可以使用 _客户登录_，让他们能够查看客户看到的内容，并进行更新以帮助他们。

以客户身份登录时执行的任何操作将应用于实际客户的帐户。

为以下项启用时 _管理员_ 用户， _[!UICONTROL Login as Customer]_按钮会显示在多个页面中：

* [客户编辑页面](../customers/update-account.md)
* [订单查看页面](../stores-purchase/order-processing.md)
* [发票查看页](../stores-purchase/invoices.md)
* [装运视图页](../stores-purchase/shipments.md)
* [贷项通知单视图页](../stores-purchase/credit-memo-create.md)

![客户登录](assets/login-as-customer.png){width="600" zoomable="yes"}

## 启用客户登录

正在启用 _客户登录_ 要求您在Commerce实例中启用该功能，然后在用户角色权限中为管理员用户启用访问权限。

### 启用该功能

1. 在管理员侧边栏上，转到  **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中，展开 **[!UICONTROL Customers]** 并选择  **[!UICONTROL Login as Customer]**.

   ![配置选项 — 客户登录](../configuration-reference/customers/assets/login-as-customer.png){width="600" zoomable="yes"}

1. 设置 **[!UICONTROL Enable Login as Customer]** 到 `Yes`.

1. _（可选）_ 设置 **[!UICONTROL Disable Page Cache for Admin User]** 到 `No` 在管理员用户以客户身份登录时启用页面缓存。

   >[!WARNING]
   >
   > 禁用页面缓存(`Yes`  — 默认)确保客户获得最新的未缓存数据时用户登录。

1. _（可选）_ 设置 **[!UICONTROL Store View to Log in]** 到 `Manual Selection` 如果您设置了多站点和/或多商店，并且希望管理员用户在以客户身份登录时选择商店视图。

1. 完成后，单击 **[!UICONTROL Save Config]**.

### 为管理员用户启用访问权限

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL System]** > _权限_ > **[!UICONTROL User Roles]**.

1. 单击列表中的角色。

1. 在 [!UICONTROL _角色信息_] 左侧面板，单击 **[!UICONTROL Role Resources]**.

1. 更改 **[!UICONTROL Role Resources]** 在页面至 `Custom`.

   >[!INFO]
   >
   > 选中此选项后，资源层次结构将显示在页面中。

1. 滚动到  **[!UICONTROL Customers]** 父项目和 **[!UICONTROL Login as Customer]** 下的项目。 然后，选择要为角色启用的资源：

   * **[!UICONTROL Allow Login as Customer]**  — 允许管理员用户使用 _客户登录_ 功能。
   * **[!UICONTROL View Login as Customer Log]**  — 允许管理员用户查看 _客户登录_ 日志。

   ![角色资源 — 客户登录](assets/customers-login-as-customer-role-resources.png){width="400" zoomable="yes"}

1. 单击 **[!UICONTROL Save Role]**.

## 以客户身份从管理员登录

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Customers]** > [!UICONTROL _所有客户_].

1. 在编辑模式下打开用户。

1. 在 **[!UICONTROL Customer Information]** 面板，选择 **[!UICONTROL Account Information]** 部分。

1. 设置 **[!UICONTROL Allow remote shopping assistance]** 到 `Yes`.

   >[!INFO]
   >
   >管理员现在可以用户身份登录，而无需从店面获得权限。

## 用于远程购物协助的客户帐户权限

要从管理员为商店支持人员启用帐户访问权限，客户必须为其帐户启用该功能：

1. 客户访问 **[!UICONTROL Account Information]** 页面。

1. 选择 **[!UICONTROL Allow remote shopping assistance]** 复选框。

1. 客户点击 **[!UICONTROL Save]**.

![帐户信息页面](assets/permission.png){width="700" zoomable="yes"}

>[!WARNING]
>
>如果没有此权限，管理员用户将无法以此客户身份登录。

## 使用客户身份登录

>[!INFO]
>
>使用 _客户登录_，确保按照之前所述配置您的管理员。

_客户登录_ 允许您像客户一样查看站点，并允许您为客户排除故障和执行其他操作。 如果您分配了具有所需权限的用户角色：

1. 您可以单击 **[!UICONTROL Login as Customer]** （在上一节中列出的页面上）。
1. “作为客户登录”操作在“操作报表”中可用。

>[!WARNING]
>
>登录时执行的任何操作 [!UICONTROL _作为客户_] （例如添加/删除产品）应用于实际客户的订单。 店面会显示横幅 `logged in as customer_name` 提供特殊状态的提醒。

## 以客户日志记录身份登录

{{ee-feature}}

Adobe Commerce为以下对象提供日志记录： _客户登录_ 操作。 它列出了管理员用户访问功能的所有会话。 要访问记录的操作，请转到 [管理操作报表](../systems/action-log-report.md).

您可以筛选报表设置 **[!UICONTROL Action Group]** 到 `Login As Customer` ，然后单击 **[!UICONTROL Search]**.

![筛选操作报表](assets/customers-login-as-customer-log-filter.png){width="700" zoomable="yes"}

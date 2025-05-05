---
title: 管理客户帐户
description: 使用[!UICONTROL Customers]网格查找任何客户帐户并访问单个客户帐户的信息。
exl-id: 5f817ca8-9d1f-4498-b3bd-989713f0b6ad
source-git-commit: 0316475a37ee09948b9ba3649e059155212ab1ae
workflow-type: tm+mt
source-wordcount: '882'
ht-degree: 0%

---

# 管理客户帐户

使用&#x200B;_[!UICONTROL Customers]_&#x200B;网格查找任何客户帐户。 您可以使用标准[工作区控件](../getting-started/admin-workspace.md)筛选列表、更改[列布局](../getting-started/admin-grid-controls.md)、保存视图和导出数据。 网格上方的[操作控件](../getting-started/admin-actions-control.md)可用于将操作应用于多个客户记录。

![所有客户](assets/customers-all-customers.png){width="700" zoomable="yes"}

有关对客户帐户进行手动更新的信息，请参阅[更新客户配置文件](update-account.md)。

## 客户帐户操作

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Customers]** > **[!UICONTROL All Customers]**。

1. 在网格的第一列中，选中要更新的每个记录的复选框。

1. 按照要应用的操作的说明进行操作。

   >[!INFO]
   >
   >以下操作可应用于单个或多个记录。

1. 完成后，单击&#x200B;**[!UICONTROL Save Config]**。

### 订阅新闻稿

在具有全局[客户帐户范围](../customers/customer-account-scope.md)的多商店和多站点设置中，客户帐户可以订阅多个网站或商店的新闻稿。 如果将&#x200B;_订阅_&#x200B;操作应用于客户帐户，它将仅为默认网站/商店视图激活新闻稿订阅。

* 将&#x200B;**[!UICONTROL Actions]**&#x200B;控件设置为`Subscribe to newsletter`。

有关管理客户的新闻稿订阅的详细信息，请参阅[管理订阅者](../merchandising-promotions/newsletter-subscribers.md)。

### 取消订阅新闻稿

在具有全局[客户帐户范围](customer-account-scope.md)的多商店和多站点设置中，客户帐户可以订阅多个网站/商店的新闻稿。 如果对客户帐户应用&#x200B;_取消订阅_&#x200B;操作，则所有活动订阅都将取消订阅。

1. 将&#x200B;**[!UICONTROL Actions]**&#x200B;控件设置为`Unsubscribe to newsletter`。

1. 提示确认时，单击&#x200B;**确定**。

### 分配客户组

1. 将&#x200B;**[!UICONTROL Actions]**&#x200B;控件设置为`Assign a customer group`。

1. 选择要将所有选定客户记录分配到的客户组。

1. 提示确认时，单击&#x200B;**[!UICONTROL OK]**。

### 删除客户帐户

无法恢复已删除的客户帐户。 有关客户活动和交易的信息保留在系统中。

1. 将&#x200B;**[!UICONTROL Actions]**&#x200B;控件设置为`Delete`。

1. 提示确认时，单击&#x200B;**[!UICONTROL OK]**。

## 导出客户帐户

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Customers]** > **[!UICONTROL All Customers]**。

1. 在“表标题”菜单中，单击&#x200B;**[!UICONTROL Export]**&#x200B;并选择所需的格式：

   * CSV
   * Excel XML

1. 单击&#x200B;**[!UICONTROL OK]**。

   该文件将转到您的默认下载文件夹。

上述说明可导出所有客户帐户。 如果要导出有限的客户集，请选中要导出的帐户对应的复选框，或使用控制面板上的过滤器选择一系列客户帐户。

## 操作/控制

| 选项 | 描述 |
|--- |--- |
| **[!UICONTROL Delete]** | 删除所选客户帐户。 如果客户帐户属于B2B存储区的公司管理员，则必须先将另一个公司用户指定为管理员，然后才能删除客户帐户。 |
| **[!UICONTROL Subscribe to Newsletter]** | 为选定的客户订阅新闻稿。 |
| **[!UICONTROL Unsubscribe from Newsletter]** | 取消订阅新闻稿中的选定客户。 |
| **[!UICONTROL Assign a Customer Group]** | 将所选客户分配给客户组。 |
| **[!UICONTROL Edit]** | 允许从网格编辑单个选定客户记录的某些值。 默认情况下，以下值可用于快速编辑：电子邮件、组、电话、ZIP、网站、增值税号码和性别。 |

{style="table-layout:auto"}

## 列

| 列 | 描述 |
|--- |--- |
| **[!UICONTROL Select]** | 管理用于应用操作的客户记录的复选框选择。 您还可以使用列标题中的选择控件来选择/取消选择全部。 |
| **[!UICONTROL ID]** | 创建客户帐户时分配的唯一数字标识符。 |
| **[!UICONTROL Name]** | 客户的名字和姓氏。 |
| **[!UICONTROL Email]** | 客户的电子邮件地址。 |
| **[!UICONTROL Group]** | 客户分配到的客户组。 |
| **[!UICONTROL Phone]** | 客户的电话号码。 |
| **[!UICONTROL ZIP]** | 客户的邮政编码。 |
| **[!UICONTROL Country]** | 客户所在的国家/地区。 |
| **[!UICONTROL State/Province]** | 客户所在的省/市/自治区。 |
| **[!UICONTROL Customer Since]** | 客户帐户的创建日期和时间。 |
| **[!UICONTROL Web Site]** | 商店层次结构中与客户帐户关联的网站。 |
| **[!UICONTROL Confirmed Email]** | 指示是否需要确认电子邮件。 |
| **[!UICONTROL Account Created In]** | 指示从中创建客户帐户的商店视图。 |
| **[!UICONTROL Date of Birth]** | 客户的出生日期。 按照最新的安全和隐私最佳实践，了解将客户的完整出生日期（月、日、年）与其他个人标识符一起存储可能会带来的任何法律和安全风险。 建议限制存储客户的完整出生日期，并建议使用客户出生年份作为替代方法。 |
| **[!UICONTROL Tax / VAT Number]** | 如果适用，为客户分配的税号或[增值税](../stores-purchase/vat.md)编号。 <br/><br/>此字段与增值税号不同。 |
| **[!UICONTROL Gender]** | 客户的性别。 |
| **[!UICONTROL Action]** | 编辑 — 在编辑模式下打开公司帐户。 |

{style="table-layout:auto"}

### 其他列

可通过更改网格的[列布局](../getting-started/admin-grid-controls.md)使用这些列。

| 列 | 描述 |
|--- |--- |
| **[!UICONTROL Company]** | 客户的公司名称。 |
| **[!UICONTROL Street Address]** | 客户的街道地址。 |
| **[!UICONTROL City]** | 客户所在的城市。 |
| **[!UICONTROL Fax]** | 客户的传真号码（如果适用）。 |
| **[!UICONTROL Billing Firstname]** | 客户帐单地址中的名字。 |
| **[!UICONTROL Billing Lastname]** | 客户帐单地址中的姓氏。 |
| **[!UICONTROL Billing Address]** | 将发送账单信息的地址。 |
| **[!UICONTROL Shipping Address]** | 将发送订单的地址。 |
| **[!UICONTROL VAT Number]** | 与客户地址关联的增值税编号。 对于在欧盟销售的[数字商品](../stores-purchase/taxes.md)，增值税基于客户的帐单地址。 <br/><br/>此字段与税务/增值税编号不同。 |
| **[!UICONTROL Account Lock]** | 指示帐户的状态。 作为安全措施，如果登录尝试次数过多，则客户帐户可能被[锁定](../customers/password-options.md)。 值： `Locked` / `Unlocked` |
| **[!UICONTROL Status]** | 当前用户状态。 选项： `Active` / `Inactive` |
| **[!UICONTROL Customer Type]** | 客户分类。 选项： `Individual user` / `Company admin` / `Company user` |
| **[!UICONTROL Sales Representative]** | 被指定为公司帐户的联系人并接收与公司相关的所有自动电子邮件的销售代表。 |

{style="table-layout:auto"}

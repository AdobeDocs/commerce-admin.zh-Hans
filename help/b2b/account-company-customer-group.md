---
title: 将客户组分配给公司
description: 了解如何在Adobe Commerce商店中将客户组分配给公司帐户。
exl-id: fba3c17e-95df-4e9e-84b8-67409c6da72d
feature: B2B, Companies, Configuration, Customers
role: Admin, User
source-git-commit: 581d2cf82880552432471171b69a1a597da54c30
workflow-type: tm+mt
source-wordcount: '236'
ht-degree: 0%

---

# 将客户组分配给公司

将客户组分配给公司基本上与分配共享目录相同。 如果配置](enable-basic-features.md)中未启用[共享目录，则会将客户组（而不是共享目录）分配给公司。

- 一次只能将一个客户组或共享目录分配给公司。 无法删除与共享目录关联的客户组。
- 更改分配给公司的客户组将更新所有公司成员的配置文件。
- 如果客户组分配从共享目录更改为常规客户组，则公司成员将失去对共享目录的访问权限，并且他们可以从店面获得主目录。
- 更改公司组后，公司用户必须注销并登录店面才能在目录中查看新价格。

## 更改客户组

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Customers]** > **[!UICONTROL Companies]**。

1. 在网格中查找公司，然后单击&#x200B;_[!UICONTROL Action]_列中的&#x200B;**[!UICONTROL Edit]**。

   ![编辑公司](./assets/companies-grid-edit.png){width="700" zoomable="yes"}

1. 在公司页面上，向下滚动并展开![扩展选择器](../assets/icon-display-expand.png) **[!UICONTROL Advanced Settings]**&#x200B;部分。

1. 设置适当的&#x200B;**[!UICONTROL Customer Group]**。

   [!UICONTROL Customer Group]列表包括所有现有的共享目录，即使配置中禁用了共享目录也是如此。

   ![更改客户组或共享目录](./assets/company-advanced-settings-customer-group-admin.png){width="600"}

1. 提示确认时，单击&#x200B;**[!UICONTROL Proceed]**。

1. 单击&#x200B;**[!UICONTROL Save]**。

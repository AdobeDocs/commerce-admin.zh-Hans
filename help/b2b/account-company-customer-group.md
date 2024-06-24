---
title: 将客户组分配给公司
description: 了解如何在Adobe Commerce商店中将客户组分配给公司帐户。
exl-id: fba3c17e-95df-4e9e-84b8-67409c6da72d
feature: B2B, Companies, Configuration, Customers
role: Admin, User
source-git-commit: a5a8da076d6cd91eb6c3e573fec5b3fb9d2d3341
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 0%

---

# 将客户组分配给公司

将客户组分配给公司基本上与分配共享目录相同。 如果共享目录不是 [已在配置中启用](enable-basic-features.md)，即客户组（而不是共享目录）被分配给公司。

>[!NOTE]
>
> 一次只能将一个客户组或共享目录分配给公司。 无法删除与共享目录关联的客户组。

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

1. 在网格中查找公司并单击 **[!UICONTROL Edit]** 在 _[!UICONTROL Action]_列。

   ![编辑公司](./assets/companies-grid-edit.png){width="700" zoomable="yes"}

1. 在公司页面上，向下滚动并展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Advanced Settings]** 部分。

1. 设置适当的 **[!UICONTROL Customer Group]**.

   >[!NOTE]
   >
   >此 [!UICONTROL Customer Group] 列表包含所有现有的共享目录，即使配置中禁用了共享目录也是如此。

   更改分配给公司的客户组将更新所有公司成员的配置文件。

   >[!NOTE]
   >
   >更改公司组后，公司用户必须注销并登录店面才能在目录中查看新价格。

   ![更改客户组或共享目录](./assets/company-advanced-settings-customer-group-admin.png){width="600"}

   >[!NOTE]
   >
   >如果客户组分配从共享目录更改为常规客户组，则公司成员将失去对共享目录的访问权限，并且他们可以从店面获得主目录。

1. 提示确认时，单击 **[!UICONTROL Proceed]**.

1. 单击 **[!UICONTROL Save]**.

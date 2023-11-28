---
title: 商店视图
description: 了解如何添加和编辑商店视图。
exl-id: aa1f7f1c-a6d0-4ec2-83fe-15fb9646634a
feature: Site Management, System
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '281'
ht-degree: 1%

---

# 商店视图

商店视图通常用于使商店在不同的区域设置中可用。 购物者可以使用商店标题中的语言选择器来更改商店视图。

![范围 — 多个存储视图](./assets/scope-multiview.svg){width="550"}

## 添加商店视图

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**.

   ![所有商店](./assets/stores-all.png){width="700" zoomable="yes"}

1. 单击 **[!UICONTROL Create Store View]**.

   ![创建商店视图](./assets/create-store-view.png){width="600" zoomable="yes"}

1. 设置 **[!UICONTROL Store]** 到此视图的父存储。

1. 输入 **[!UICONTROL Name]** 用于此商店视图。

   该名称显示在商店标题的语言选择器中。 例如： `Spanish`.

1. 对象 **[!UICONTROL Code]**，输入用于标识视图的代码（以小写字符表示）。

   例如： `spanish`.

1. 要激活视图，请设置 **[!UICONTROL Status]** 到 `Enabled`.

1. （可选）输入 **[!UICONTROL Sort Order]** 用于确定此视图与其他视图一起列出的顺序的编号。

1. 单击 **[!UICONTROL Save Store View]**.

## 编辑商店视图

由于视图名称显示在语言选择器中，因此您最终可能希望将默认视图的名称更改为更具描述性的名称。 此 _名称_ 字段只是标签，可以轻松更改。

如果您的Adobe Commerce或Magento Open Source安装具有多站点或多存储设置，则请勿更改存储区代码字段，除非验证该值未在 `index.php` 文件。 如果您无权访问服务器来检查文件，请向开发人员寻求帮助。

| 字段 | 原始值 | 已更新值 |
| ----- | -------------- | ------------- |
| [!UICONTROL Name] | `Default Store View` | `English` |
| [!UICONTROL Code] | `default` | `english` |

{style="table-layout:auto"}

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** >  _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**.

1. 在 _[!UICONTROL Store View]_的列中，单击要编辑的视图的名称。

   编辑默认视图时， _[!UICONTROL Store]_和_[!UICONTROL Status]_ 字段不可用。

   ![存储视图 — 编辑默认视图](./assets/edit-store-view-info.png){width="600" zoomable="yes"}

1. 根据需要更新以下字段：

   - **[!UICONTROL Store]** （仅限非默认视图）
   - **[!UICONTROL Name]**
   - **[!UICONTROL Code]** (仅当未用于 `index.php`)
   - **[!UICONTROL Status]** （仅限非默认视图）
   - **[!UICONTROL Sort Order]**

1. 单击 **[!UICONTROL Save Store View]**.

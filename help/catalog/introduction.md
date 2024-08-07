---
title: 目录管理简介
description: 了解目录和产品范围如何在目录管理中起作用。
exl-id: 3c58fc1c-d7a3-4f51-8a78-6bf2fd0dbeee
source-git-commit: f36925217230e558043078fdc274f5e69c096c1e
workflow-type: tm+mt
source-wordcount: '775'
ht-degree: 0%

---

# 目录管理简介

Adobe Commerce和Magento Open Source使用术语&#x200B;_catalog_&#x200B;来引用整个产品数据库。

创建和管理商店的最重要领域之一是产品创建和类别。 管理员提供了多种工具，可用于初始设置商店、维护商店和优化业务。

>[!TIP]
>
>适用于Adobe Commerce和Magento Open Source的Inventory management为您提供了用于管理产品库存的工具。 只有一家商店到多个仓库、商店、提货地点、卸货托运人等的商家可以使用这些功能来维护销售数量，并处理发运以完成订单。 有关这些功能以及如何使用这些功能管理多个位置的库存的详细信息，请参阅[Inventory management用户指南](../inventory-management/introduction.md)。

## 目录范围

对目录数据的访问由几个因素决定，包括[作用域](../getting-started/websites-stores-views.md#scope-settings)设置、目录配置和分配给存储的[根类别](category-root.md)。 该目录包括已启用且可供销售的产品，以及当前不提供以供销售的产品。

在销售中，术语&#x200B;_目录_&#x200B;通常是指精选的可销售产品。 例如，商店可能具有“Spring Catalog”和“Fall Catalog”。

与打印目录的目录类似，商店的主菜单（或&#x200B;_顶部导航_）按类别组织产品，以便客户轻松找到所需内容。 主菜单基于&#x200B;_根类别_，它是分配给商店的菜单的容器。 由于特定菜单选项是在商店视图级别定义的，因此每个视图可以具有基于同一根类别的不同主菜单。 在每个菜单中，您都可以提供适合该商店的精选产品。

![目录层次结构图](./assets/catalog-hierarchy-scope.svg){width="550"}

## 产品范围

对于具有多个网站、商店和视图的安装，[范围](../getting-started/websites-stores-views.md#scope-settings)设置确定产品在何处可供销售，以及每个商店视图可用的产品信息。 最初，您创建的所有产品都会发布到默认的网站、商店和商店视图。

![多站点存储关系图](./assets/scope-multisite.svg){width="550"}

如果您只有一个默认视图的商店，则可以在[单商店模式](../getting-started/websites-stores-views.md#single-store-mode)下运行商店以隐藏作用域设置。 但是，如果您的存储有多个视图，则每个字段的名称下方会显示一个范围指示器。

- 要编辑特定视图的产品信息，请使用左上角的&#x200B;_存储视图_&#x200B;控件来选择视图。 其他控件将可用于可在存储视图级别编辑的任何字段。

- 要定义多站点安装中产品的范围，请参阅产品信息的“网站”中的[产品](settings-basic-websites.md)部分。

为商店视图编辑产品的过程与添加特定于视图的产品信息层类似。

您只能编辑或分配您具有权限的站点的产品，而不能编辑或分配所有已分配产品的站点的产品。

虽然在以下示例中选择了&#x200B;_Spanish_&#x200B;商店视图，但产品信息仍以默认商店视图的原始语言显示。 若要翻译产品信息，必须切换到&#x200B;_西班牙语_&#x200B;商店视图并翻译文本字段，如产品标题、描述和元数据。 有关详细信息，请参阅[本地化产品](../stores-purchase/store-localize.md#localize-products)。

## 编辑其他视图的产品

>[!NOTE]
>
>当产品也发布在允许的范围之外时，对限制在特定范围内的管理员用户禁用了&#x200B;_所有存储视图_&#x200B;范围。 默认情况下会选择第一个可编辑的作用域，因为受限用户无法执行会影响他们无权访问的作用域的&#x200B;_全局_&#x200B;操作或操作。

1. 在左上角，将&#x200B;**[!UICONTROL Store View]**&#x200B;设置为要编辑的特定视图。

1. 要确认范围更改，请单击&#x200B;**[!UICONTROL OK]**。

1. 使用商店视图的新值更新字段。

   可在商店视图中编辑的任何字段下方都会出现一个复选框。 要覆盖默认值，请取消选中&#x200B;**使用默认值**&#x200B;复选框。

   ![正在翻译西班牙商店视图的产品名称](./assets/product-translate-field-french.png){width="600" zoomable="yes"}

1. 完成后，单击&#x200B;**[!UICONTROL Save]**。

1. 在左上角，将&#x200B;**[!UICONTROL Store View]**&#x200B;选择器设置为默认值。

1. 要在您的商店中验证更改，请执行以下操作：

   - 单击右上角的&#x200B;_管理员_&#x200B;菜单箭头并选择&#x200B;**[!UICONTROL Customer View]**。

     ![客户视图](./assets/product-admin-menu-customer-view.png){width="600" zoomable="yes"}

   - 在商店的右上角，将&#x200B;**[!UICONTROL Language Chooser]**&#x200B;设置为您编辑的产品的商店视图，并查找您为该视图编辑的产品。

     ![语言选择器](./assets/storefront-language-chooser.png){width="700" zoomable="yes"}

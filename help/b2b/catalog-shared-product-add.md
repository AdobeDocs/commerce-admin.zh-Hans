---
title: 将产品添加到共享目录
description: 了解如何单独或按类别分组将产品添加到共享目录。
exl-id: c88b46b4-cea8-4f65-b7e4-6681bab64d41
feature: B2B, Companies, Catalog Management
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '400'
ht-degree: 0%

---

# 将产品添加到共享目录

产品可以单独或按类别以多个产品的组添加到共享目录中。

复杂产品（例如捆绑包、分组或可配置）必须满足以下要求，才能从共享目录的店面中可见：

- 全部 [关联的产品](../catalog/product-configurations.md) 和选项必须分配到同一共享目录并在主目录中启用。
- 对象 [可配置](../catalog/product-create-configurable.md) 和 [已分组](../catalog/product-create-grouped.md) 产品，则只会显示启用的关联产品。
- 对于 [捆绑](../catalog/product-create-bundle.md) 产品，所有选项都必须包含在共享目录中。

  ![为目录选择产品](./assets/shared-catalog-select-products-step-1.png){width="600" zoomable="yes"}

## 方法1：添加单个产品

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. 对于网格中要添加的产品，请转到 _[!UICONTROL Action]_列并单击&#x200B;**[!UICONTROL Edit]**.

1. 向下滚动，展开 ![扩展选择器](../assets/icon-display-expand.png) 该 _[!UICONTROL Product in Shared Catalogs]_部分，并执行以下操作：

   - 选中产品应出现的每个共享目录的复选框。 要选择所有目录，请单击 **[!UICONTROL Select all]**.

     ![共享目录中的产品](./assets/shared-catalog-assign-from-product.png){width="600" zoomable="yes"}

     每个所选目录的名称都会显示在 _[!UICONTROL Shared Catalogs]_字段。

     ![已分配的共享目录](./assets/shared-catalog-assigned.png){width="600" zoomable="yes"}

   - 单击 **[!UICONTROL Done]** 以保存设置。

1. 完成后，单击 **[!UICONTROL Save]**.

## 方法2：添加多个产品

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**.

1. 对于网格中的共享目录，请转到 _[!UICONTROL Action]_列并选择&#x200B;**[!UICONTROL Set Pricing and Structure]**.

1. 在类别树中，执行以下任一操作：

   - 要包含所有产品，请单击 **[!UICONTROL Select all]** 或选中父类别的复选框。
   - 要包含特定类别的产品，请选中要包含的每个类别的复选框。
   - 要包含或排除单个产品，请选中或取消选中产品的复选框。

   树中每个类别下面的表示法显示当前包含在共享目录中的类别中的产品数量。 下面的表示法 [根类别](../catalog/category-root.md) 显示当前为共享目录选择的所有类别中的产品总数。

1. 要查看网格中的类别产品，请单击树中类别的名称。

   选择类别时，会发生以下情况：

   - 将网格第一列中的切换设置为 `On` 每个所选产品的。
   - 如果将产品分配给多个类别，并且其中一个类别中省略了该产品，则它仍可通过其他类别和以下类别使用 [目录搜索](../catalog/search.md).
   - 系统自动设置 [类别权限](../catalog/category-permissions.md) 到 `Allow` 所选产品的。

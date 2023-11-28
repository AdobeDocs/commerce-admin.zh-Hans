---
title: 顶部导航
description: 了解如何定义商店的主菜单，该菜单的功能类似于向不同部门发送目录。
exl-id: 8b71fe73-2716-4820-9e57-4cb1e6888132
feature: Catalog Management, Categories, Site Navigation
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '569'
ht-degree: 0%

---

# 顶部导航

商店的主菜单类似于商店中不同部门的目录。 每个选项代表不同的产品类别。 顶部导航的位置和显示方式可能因主题而异，但其工作方式基本上相同。

![顶部导航](./assets/storefront-top-navigation.png){width="700" zoomable="yes"}

目录的类别结构会影响搜索引擎为您的网站编制索引的效果。 嵌套的类别越深，就越不可能将其完全编入索引。 通常，使用可见级别一到三个之间是最有效的。 此 [根类别](category-root.md) 尽管未显示在菜单中，但计为第一级。 顶部导航中可用级别的最大数量由配置决定。 此外，您的商店主题支持的菜单级别数量可能会受到限制。 例如，示例Luma主题最多支持五个级别，包括根。

## 对菜单级别计数

| 项目 | 描述 |
|--- |--- |
| 1级 | 第一级是根类别，在示例数据中将其命名为“Default Category”（默认类别）。 根是菜单的容器，其名称在菜单中不会显示为选项。 |
| 2级 | 在桌面显示屏上，顶部导航是显示在页面顶部的主菜单。 在移动设备上，主菜单通常显示为选项的弹出菜单。 Luma存储中的第二级选项为 _新增功能_， _女性_， _男子_， _齿轮_， _培训_、和 _销售_. |
| 3级 | 第三级显示在每个主菜单选项的下方。 例如，在 _女性_，第三级选项为 _顶部_ 和 _底部_. |
| 4级 | 第四级选项是从第三级选项弹出来的子类别。 例如，在 _顶部_，第四级菜单选项为 _夹克_， _连帽衫和运动衫_， _T恤_、和 _胸罩和坦克_. |

{style="table-layout:auto"}

## 设置顶部导航

对于要显示在商店顶部导航中的类别，请完成以下步骤：

### 步骤1：创建类别

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. 设置 **[!UICONTROL Store View]** 以确定新类别在何处可用。

1. 在类别树中，选择新类别的父类别。

   如果您从头开始，没有任何数据，则列表中可能只存在两个类别： _默认类别_，根目录，以及 _示例类别_.

1. 单击 **[!UICONTROL Add Subcategory]**.

1. 使用以下设置完成基本信息：

   - **[!UICONTROL Enable Category]** 设置为 `Yes`
   - **[!UICONTROL Include in Menu]** 设置为 `Yes`

1. 在显示设置设置中 **[!UICONTROL Anchor]** 到 `Yes`.

1. 完成任何其他必需的 [类别设置](category-create.md).

1. 完成后，单击 **[!UICONTROL Save]**.

对于多存储安装，可以将不同的主菜单指定为 [根类别](category-root.md) 每个 [存储](../stores-purchase/stores.md#add-stores).

### 第2步：设置顶部导航的深度

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中，展开 **[!UICONTROL Catalog]** 并选择 **[!UICONTROL Catalog]** 下方。

1. 展开 **[!UICONTROL Category Top Navigation]** 部分。

   ![类别顶部导航](../configuration-reference/catalog/assets/catalog-category-top-navigation.png){width="600" zoomable="yes"}

   因为顶部导航的深度具有全局性 [配置范围](../getting-started/websites-stores-views.md#scope-settings)，设置适用于Commerce安装中的所有网站、商店和商店视图。 此 _[!UICONTROL Category Top Navigation]_配置部分仅在以下情况下可用_[!UICONTROL Store View]_ （位于左上角）设置为 `Default Config`.

   有关这些选项的详细列表，请参阅 [类别顶部导航](../configuration-reference/catalog/catalog.md#layered-navigation) 在 _配置引用_.

1. 要限制显示在顶部导航中的子类别数，请输入 **[!UICONTROL Maximal Depth]**.

   默认值为 `0`，不对子类别级别的数量进行限制。

1. 完成后，单击 **[!UICONTROL Save Config]**.

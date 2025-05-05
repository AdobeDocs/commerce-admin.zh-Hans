---
title: 类别权限
description: 了解如何使用类别来控制产品价格的显示，确定哪些客户组可以将产品添加到购物车，以及指定登陆页面。
exl-id: d80a0545-918e-4c08-9f37-4aa3cd7771f4
feature: Catalog Management, Categories, Customers, Configuration
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '779'
ht-degree: 0%

---

# 类别权限

{{ee-feature}}

类别访问可以限制为特定客户组，也可以完全限制。 您可以控制产品价格的显示，确定哪些客户组可以将产品添加到购物车，并指定登陆页面。

>[!NOTE]
>
>类别权限具有全局范围，启用时，会根据每个类别的个别权限限制每个类别的访问。 默认情况下，“类别权限”处于未启用状态。

例如，如果您只向批发客户销售，则可以允许任何人浏览目录，但只显示&#x200B;_批发_&#x200B;客户组中的购物者的价格并允许他们购买。 在以下示例中，仅登录用户有权访问“收藏集”类别。 对于来宾，“收藏集”选项不会出现在主菜单中。

![登录用户看到“收藏集”类别](./assets/storefront-category-permissions-logged-in.png){width="600" zoomable="yes"}

启用后，“类别”页面上将显示一个新的&#x200B;_[!UICONTROL Category Permissions]_&#x200B;部分，通过该部分，您可以对每个类别应用所需的访问权限。 您可以为不同的网站和客户组向每个类别添加多个权限规则。

## 步骤1：配置类别权限

>[!IMPORTANT]
>
>启用&#x200B;**_[!UICONTROL Shared Catalog]_**&#x200B;功能后，目录中的&#x200B;**_所有_**&#x200B;类别将忽略所有现有[组权限设置](../configuration-reference/catalog/catalog.md#category-permissions)。 [!UICONTROL Shared Catalog]在启用时完全控制目录中的所有类别权限。

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧面板中，展开&#x200B;**[!UICONTROL Catalog]**&#x200B;并在下面选择&#x200B;**[!UICONTROL Catalog]**。

1. 展开&#x200B;**[!UICONTROL Category Permissions]**&#x200B;部分的![扩展选择器](../assets/icon-display-expand.png)。

   ![类别权限](../configuration-reference/catalog/assets/catalog-category-permissions.png){width="600" zoomable="yes"}

   有关这些选项的详细列表，请参阅&#x200B;_配置引用_&#x200B;中的[类别权限](../configuration-reference/catalog/catalog.md#category-permissions)。

1. 将&#x200B;**[!UICONTROL Enable]**&#x200B;设置为`Yes`。

1. 根据您希望对存储允许或限制的内容完成其他选项（请参阅以下部分）。

1. 完成后，单击&#x200B;**[!UICONTROL Save Config]**。

1. 提示更新缓存时，单击系统消息中的&#x200B;**[!UICONTROL Cache Management]**&#x200B;链接，然后按照说明刷新缓存。

### [!UICONTROL Allow Browsing Category]

此选项适用于[网站](../getting-started/websites-stores-views.md)中的所有类别。

要允许&#x200B;**_特定客户组_**&#x200B;的成员浏览类别产品，请执行以下操作：

1. 将&#x200B;**[!UICONTROL Allow Browsing Category]**&#x200B;设置为`Specified Customer Groups`。

1. 在&#x200B;**[!UICONTROL Customer Groups]**&#x200B;框中，选择允许浏览类别中产品的每个组。

   要选择多个组，请在单击每个组时按住Ctrl键(PC)或Command键(Mac)。

   ![允许批发客户组浏览](./assets/category-permissions-allow-browsing-customer-groups.png){width="600" zoomable="yes"}

要&#x200B;**_限制访问并重定向到登陆页面_**，请执行以下操作：

1. 将&#x200B;**[!UICONTROL Allow Browsing Category]**&#x200B;设置为`No, Redirect to Landing Page`。

1. 选择将访客重定向到的&#x200B;**[!UICONTROL Landing Page]**。

   ![重定向到主页](./assets/category-permissions-browse-category-landing-page.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >虽然&#x200B;_[!UICONTROL Allow Browsing Category]_&#x200B;设置适用于网站中的所有类别，但您可以为每个商店视图配置不同的登陆页面。

### [!UICONTROL Display Product Prices]

此选项适用于[网站](../getting-started/websites-stores-views.md)中的所有类别。

要仅允许&#x200B;**_特定客户组_**&#x200B;的成员查看该类别中的产品价格，请执行以下操作：

1. 将&#x200B;**[!UICONTROL Display Product Prices]**&#x200B;设置为`Yes, for Specified Customer Groups`。

1. 在&#x200B;**[!UICONTROL Customer Groups]**&#x200B;框中，选择每个允许查看该类别中产品价格的组。

   要选择多个组，请在单击每个组时按住Ctrl键(PC)或Command键(Mac)。)

   ![只有批发客户组才能看到价格](./assets/category-permissions-price-customer-groups.png){width="600" zoomable="yes"}

### [!UICONTROL Allow Adding to Cart]

此选项适用于[网站](../getting-started/websites-stores-views.md)中的所有类别。

要仅允许&#x200B;**_特定客户组_**&#x200B;的成员将类别产品放入购物车，请执行以下操作：

1. 将&#x200B;**[!UICONTROL Allow Adding to Cart]**&#x200B;设置为`Yes, for Specified Customer Groups`。

1. 在&#x200B;**[!UICONTROL Customer Groups]**&#x200B;框中，选择允许将产品从类别添加到购物车的每个组。

   要选择多个组，请在单击每个组时按住Ctrl键(PC)或Command键(Mac)。

   ![只有批发客户组才能将产品放入购物车](./assets/category-permissions-cart-customer-groups.png){width="600" zoomable="yes"}

### [!UICONTROL Disallow Catalog Search]

设置此选项可阻止特定客户组的成员使用目录搜索。 它适用于[网站](../getting-started/websites-stores-views.md)中的所有类别。

- 要允许&#x200B;**_仅登录客户_**&#x200B;使用目录搜索，请选择`NOT LOGGED IN`。

- 要仅允许&#x200B;**_特定客户组_**&#x200B;使用目录搜索，请选择每个要使用类别搜索排除的组。

  要选择多个组，请在单击每个组时按住Ctrl键(PC)或Command键(Mac)。

  ![不允许对常规客户组进行目录搜索](./assets/category-permissions-disallow-category-search.png){width="600" zoomable="yes"}

## 步骤2：应用类别权限

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Catalog]** > **[!UICONTROL Categories]**。

1. 在类别树中，选择目标类别。

1. 展开页面上的![扩展选择器](../assets/icon-display-expand.png) **[!UICONTROL Category Permissions]**&#x200B;并执行以下操作：

   - 要创建权限规则，请单击&#x200B;**[!UICONTROL New Permission]**。

     ![类别权限部分](./assets/category-permissions-section-admin.png){width="600" zoomable="yes"}

   - 选择适用的&#x200B;**[!UICONTROL Website]**&#x200B;和&#x200B;**[!UICONTROL Customer Group]**。

   - 根据需要设置各个权限。

   >[!NOTE]
   >
   >为任何父类别设置`Browsing Category` = `Deny`权限时，该权限不会显示在子类别页面的[痕迹导航路径](navigation-breadcrumb-trail.md)上。

1. 完成后，单击&#x200B;**[!UICONTROL Save]**。

>[!NOTE]
>
>如果为`Root Category`设置了任何&#x200B;**_允许_**&#x200B;权限，则这些权限会自动应用于`Catalog`中的所有子类别和所有产品。 如果有任何产品被分配给多个类别，并且它至少有一个类别具有任何&#x200B;**_允许_**&#x200B;权限，则它自动对所有分配的类别具有相同的&#x200B;**_允许_**&#x200B;权限。

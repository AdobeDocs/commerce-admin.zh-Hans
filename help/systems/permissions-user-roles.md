---
title: 用户角色
description: 了解如何创建用户角色和相关权限以管理对管理员功能的访问。
exl-id: a70f74d4-72b4-4639-a67d-9fc13df65924
feature: Admin Workspace, Roles/Permissions, Security
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '659'
ht-degree: 0%

---

# 用户角色

要授予某人对管理员的有限访问权限，第一步是创建具有适当权限级别的角色。 保存角色后，您可以添加新用户并分配受限角色，以授予管理员受限访问权限。

![管理员 — 用户角色](./assets/permissions-role-grid.png){width="600" zoomable="yes"}

## 定义角色

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL User Roles]**.

1. 在右上角，单击 **[!UICONTROL Add New Role]**.

1. 完成以下步骤以定义角色：

### 步骤1：添加角色名称

1. 下 _[!UICONTROL Role Information]_，输入描述性&#x200B;**[!UICONTROL Role Name]**.

1. 下 _[!UICONTROL Current User Identity Verification]_，输入您的密码。

   ![系统权限 — 角色信息](./assets/permissions-role-info.png){width="600" zoomable="yes"}

### 步骤2：分配资源

>[!IMPORTANT]
>
>在分配资源时，如果您限制给定角色的访问权限，请确保禁用对权限工具的访问权限。 否则，用户能够修改自己的权限。

1. 设置 **[!UICONTROL Role Scopes]** 更改为以下任一项：

   - `All`
   - `Custom`

   如果设置为 `Custom` 对于多站点安装，选中将使用该角色的网站和商店的复选框。

   ![用户角色资源 — 自定义范围](./assets/permissions-role-scope-custom.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >具有的用户 `Custom` 角色范围无法创建网站和类别、将产品分配给类别或编辑产品 _[!UICONTROL All Store Views]_将它们分配给受限存储时的范围。 这些用户也无法执行其他操作_&#x200B;全局&#x200B;_影响他们无权访问的范围的操作。

1. 下 _[!UICONTROL Roles Resources]_，设置&#x200B;**[!UICONTROL Resource Access]**到 `Custom`.

1. 在 **[!UICONTROL Resource]** 树结构中，选中角色可以访问的每个管理员功能的复选框。

   要创建有权访问税设置的管理员角色，请选择销售/税和系统/税资源。 如果为不同于默认区域的区域设置网站 [装运原点](../stores-purchase/shipping-settings.md#point-of-origin)中，您必须允许角色访问系统/配送资源。 配送设置确定用于目录价格的商店税率。

   ![已分配的用户角色资源](./assets/permissions-role-resources-product.png){width="600" zoomable="yes"}

   可用权限列表可能包含适用于捆绑扩展和已安装扩展的其他选项。 通过选择每个功能的最上层权限，可为用户分配所有可用权限。

   >[!NOTE]
   >
   >管理员用户必须具有 **[!UICONTROL Sales / Archive]** 其角色作用域的权限，以查看 _[!UICONTROL Invoices]_，_[!UICONTROL Credit Memos]_、和 _[!UICONTROL Shipments]_订购 [选项卡](../stores-purchase/order-processing.md).

1. 完成后，单击 **[!UICONTROL Save Role]**.

   该角色现在显示在网格中，可以分配给用户帐户。

## 向用户分配角色

1. 从 _[!UICONTROL Roles]_网格，在编辑模式下打开记录。

1. 下 _[!UICONTROL Current User Identity Verification]_，输入您的用户帐户密码。

1. 在左侧面板中，选择 **[!UICONTROL Role Users]**.

   此 _[!UICONTROL Role Users]_选项仅在保存新角色后显示。

   ![分配给角色的用户帐户](./assets/permissions-role-users.png){width="600" zoomable="yes"}

1. 要搜索特定用户记录，请执行以下操作：

   - 在列顶部的搜索过滤器中输入值，然后按 **输入**.

   - 当您准备好返回完整列表时，请单击 **[!UICONTROL Reset Filter]**.

1. 选中要分配给角色的任何用户的复选框。

1. 单击 **[!UICONTROL Save Role]**.

## 编辑角色

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL User Roles]**.

1. 使用网格上方的筛选器找到角色，然后单击角色名称。

1. 进行所需的更改。

   有关角色设置的信息，请查看创建用户角色的步骤。

1. 出现提示时，输入密码以确认您的身份。

1. 单击 **[!UICONTROL Save Role]**.

## 删除角色

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL User Roles]**.

1. 使用网格上方的筛选器找到角色，并在编辑模式下打开。

1. 在右上角，单击 **[!UICONTROL Delete Role]**.

1. 要确认操作，请单击 **[!UICONTROL OK]**.

## 用户角色演示

观看本视频，了解如何管理用户角色：

>[!VIDEO](https://video.tv.adobe.com/v/343654?quality=12)

## 角色资源

可将对以下资源的访问权限分配给自定义角色。 请参阅链接的页面，了解有关与每个资源关联的功能的更多信息。

![Adobe Commerce](../assets/adobe-logo.svg)  — 仅限Adobe Commerce

![适用于Adobe Commerce的B2B](../assets/b2b.svg)  — 仅适用于Adobe Commerce的B2B版本

| 资源 |   |   |
| --- | --- | --- |
| [`Dashboard`](../getting-started/admin-dashboard.md) |  |  |
| [`Sales`](../stores-purchase/sales-menu.md) | [`Operations`](../stores-purchase/orders.md) |  |
|  | [`Quotes`](../b2b/quotes.md) ![适用于Adobe Commerce的B2B](../assets/b2b.svg) <br/>[`Orders`](../stores-purchase/orders.md)<br/>[`Invoices`](../stores-purchase/invoices.md)<br/>[`Shipments`](../stores-purchase/shipments.md)<br/>[`Credit Memos`](../stores-purchase/credit-memos.md)<br/>[`Billing Agreements`](../stores-purchase/paypal-billing-agreements.md)<br/>[`Returns`](../stores-purchase/returns.md) ![Adobe Commerce](../assets/adobe-logo.svg)<br/>[`Transactions`](../stores-purchase/transactions.md) |
|  | [`Archive`](action-log-archive.md)![Adobe Commerce] |  |
|  | [`Shopping Cart Management`](../stores-purchase/cart.md) |  |
| [`Catalog`](../catalog/catalog-menu.md) | [`Category Permissions`](../catalog/categories.md) ![Adobe Commerce](../assets/adobe-logo.svg) |  |
|  | [`Inventory`](../inventory-management/introduction.md) | [`Products`](../catalog/products-list.md)<br/>[`Categories`](../catalog/categories.md) |
|  | [`Shared Catalog`](../b2b/catalog-shared-create.md) ![适用于Adobe Commerce的B2B](../assets/b2b.svg) | [`Manage Shared Catalog`](../b2b/catalog-shared-manage.md) |
| [`Customers`](../customers/guide-overview.md) | [`All Customers`](../customers/customers-all.md)<br/>[`Now Online`](../customers/now-online.md)<br/>[`Customer Groups`](../customers/customer-groups.md)<br/>[`Segments`](../customers/customer-segments.md) ![Adobe Commerce](../assets/adobe-logo.svg) |  |
|  | [`Login as Customer`](../customers/login-as-customer.md) | `Allow Login as Customer Button`<br/>`View Login as Customer Log` ![Adobe Commerce](../assets/adobe-logo.svg) |
|  | [`Companies`](../b2b/account-companies.md) ![适用于Adobe Commerce的B2B](../assets/b2b.svg) | [`Manage Companies`](../b2b/account-company-manage.md) <br/>`Add New Company` <br/>`Delete Company` <br/>`Reimburse Balance` |
| [`Carts`](../stores-purchase/shopping-assisted-cart-manage.md) | [`Manage carts`](../stores-purchase/shopping-assisted-cart-manage.md) |  |
| [`My Account`](../customers/account-dashboard-my-account.md) |  |  |
| [`Marketing`](../merchandising-promotions/marketing-menu.md) | [`Promotions`](../merchandising-promotions/marketing-menu.md#uicontrol-promotions) | [`Catalog Price Rule`](../merchandising-promotions/price-rules-catalog.md) <br/>[`Cart Price Rules`](../merchandising-promotions/price-rules-cart.md) <br/>[`Related Products Rules`](../merchandising-promotions/product-related-rules.md)![Adobe Commerce](../assets/adobe-logo.svg)<br/>[`Gift Card Accounts`](../stores-purchase/product-gift-card-accounts.md) ![Adobe Commerce](../assets/adobe-logo.svg) |
|  | [`Private Sales`](../merchandising-promotions/events-private-sales.md) ![Adobe Commerce](../assets/adobe-logo.svg) | [`Events`](../merchandising-promotions/event-create.md) <br/>[`Invitations`](../merchandising-promotions/invitations.md) |
|  | `Communications` | [`Email Templates`](email-templates.md) <br/>[`Newsletter Template`](../merchandising-promotions/newsletter-template.md) <br/>[`Newsletter Queue`](../merchandising-promotions/newsletter-queue.md) <br/>[`Newsletter Subscribers`](../merchandising-promotions/newsletter-subscribers.md) <br/>[`Email Reminders`](../merchandising-promotions/email-reminder-rules.md) |
|  | `Sales Channel` | [`Amazon Sales Channel`](https://experienceleague.adobe.com/docs/commerce-channels/amazon/overview.html) |
|  | [`SEO & Search`](../merchandising-promotions/marketing-menu.md#uicontrol-seo--search) | [`Search Terms`](../catalog/search-terms.md) <br/>[`Search Synonyms`](../catalog/search-terms.md#search-synonyms) ![Adobe Commerce](../assets/adobe-logo.svg)<br/>[`URL Rewrites`](../merchandising-promotions/url-rewrite-custom.md) <br/>[`Site Map`](../merchandising-promotions/sitemap-xml.md) |
|  | [`User Content`](../merchandising-promotions/product-reviews-moderate.md) | [`All Reviews`](../merchandising-promotions/product-reviews.md) <br/>[`Pending Reviews`](../merchandising-promotions/product-reviews-moderate.md) <br/> |  |
| [`Content`](../content-design/content-menu.md) | [`Elements`](../content-design/content-menu.md#uicontrol-elements)) | [`Pages`](../content-design/pages.md)<br/>[`Hierarchy`](../content-design/page-hierarchy.md) ![Adobe Commerce](../assets/adobe-logo.svg)<br/>[`Blocks`](../content-design/blocks.md)<br/>[`Dynamic Blocks`](../content-design/dynamic-blocks.md) ![Adobe Commerce](../assets/adobe-logo.svg)<br/>[`Widgets`](../content-design/widgets.md)<br/>[`Media Gallery`](../content-design/media-gallery.md) |  |
|  | [`Design`](../content-design/introduction.md#design) | [`Themes`](../content-design/themes.md)<br/>[`Schedule`](../content-design/schedule.md) |  |
|  | [内容暂存](../content-design/content-staging.md) ![Adobe Commerce](../assets/adobe-logo.svg)<br /> |  |
| [`Reports`](../getting-started/reports-menu.md) | [`Marketing`](../getting-started/marketing-reports.md) | `Shopping Cart`<br />[`Search Terms`](../catalog/search-terms.md#search-terms-report)<br />`Newsletter Problem Reports` |  |
|  | [`Reviews`](../getting-started/review-reports.md)<br /> |  |
|  | [`Sales`](../getting-started/sales-reports.md) |  |
|  | `System Insights` ![Adobe Commerce](../assets/adobe-logo.svg) | [`Site-Wide Analysis Tool`](https://experienceleague.adobe.com/docs/commerce-operations/tools/site-wide-analysis-tool/access.html) |
|  | [`Customers`](../getting-started/customer-reports.md)<br/>[`Products`](../getting-started/product-reports.md)<br/>[`Private Sales`](../getting-started/private-sales-reports.md) ![Adobe Commerce](../assets/adobe-logo.svg)<br />[`Statistics`](../getting-started/reports-menu.md#uicontrol-statistics)<br />[`Business Intelligence`](../getting-started/business-intelligence.md) |  |
| [`Stores`](../stores-purchase/stores.md) | [`Settings`](../stores-purchase/stores-menu.md) | [`All Stores`](../stores-purchase/stores.md)<br/>[`Configuration`](../configuration-reference/guide-overview.md)<br/>[`Terms and Conditions`](../stores-purchase/terms-and-conditions.md)<br/>[`Order Status`](../stores-purchase/order-status.md) |  |
|  | [`Inventory`](../inventory-management/sources-stocks.md) | [`Sources`](../inventory-management/sources-manage.md)<br/>[`Stocks`](../inventory-management/stocks-manage.md) |  |
|  | [`Taxes`](../stores-purchase/taxes.md) |  |  |
|  | [`Currency`](../stores-purchase/currency.md) | [`Currency Rates`](../stores-purchase/currency-update.md)<br/>[`Currency Symbols`](../stores-purchase/currency-configuration.md#step-5-customize-currency-symbols-optional) |  |
|  | [`Attributes`](../catalog/product-attributes.md) | [`Product`](../catalog/attribute-product-create.md)<br/>[`Update Attributes`](../catalog/attribute-product-create.md)<br/>[`Attribute Set`](../catalog/attribute-sets.md)<br/>[`Ratings`](../merchandising-promotions/product-reviews.md#create-custom-ratings) |
|  | [`Other Settings`](../stores-purchase/stores-menu.md) | [`Customer Groups`](../customers/customer-groups.md) |
| [`System`](system-menu.md) | [`Data Transfer`](data-transfer.md) | [`Import`](data-import.md)<br/>[`Export`](data-export.md)<br/>[`Import/Export Tax Rates`](data-transfer-tax-rates.md)<br/>[`Import History`](data-import.md#import-history) |  |
|  | [`Magento Connect`](../getting-started/commerce-marketplace.md) | `Connect Manager`<br/>`Package Extensions` |  |
|  | [`Tools`](system-menu.md#tools) | [`Cache Management`](cache-management.md)<br/>[`Backups`](backups.md)<br/>[`Index Management`](index-management.md)<br/>[`Change Indexer Mode`](index-management.md) |  |
|  | [`Permissions`](permissions.md) | [`All Users`](permissions-users-all.md)<br/>[`Locked Users`](permissions-users-all.md#locked-users)<br/>[`User Roles`](permissions-user-roles.md) |
| [`Action Log`](action-log.md)![Adobe Commerce](../assets/adobe-logo.svg) | [`Report`](action-log.md)<br/>[`Archive`](action-log-archive.md) |
|  | [`Other Settings`](system-menu.md) | [`Notifications`](notifications.md)<br/>[`Custom Variables`](variables-custom.md)<br/>[`Manage Encryption Key`](encryption-key.md) |  |
| [`Global Search`](../getting-started/admin-workspace.md#workspace-search) |  |  |

{style="table-layout:auto"}

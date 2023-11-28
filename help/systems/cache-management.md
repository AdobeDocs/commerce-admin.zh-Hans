---
title: 缓存管理
description: 了解如何使用缓存管理工具，这些工具提供了一种提高站点性能的简单方法。
exl-id: c87f85ca-81b9-4cbf-9817-3d779397eefd
feature: Cache, System
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '1422'
ht-degree: 0%

---

# 缓存管理

Adobe Commerce和Magento Open Source缓存管理系统提供了一种提高站点性能的简单方法。 每当缓存需要刷新时，工作区顶部都会显示一条通知，引导您完成该过程。 按照指向缓存管理的链接刷新无效缓存。

![保存产品属性 — 更新缓存消息](./assets/product-attribute-save-msg-update-cache.png){width="500"}

>[!NOTE]
>
>当目录实体发生更改时，可能会影响其他页面，同时使多个缓存失效。 在查看缓存管理页面时，您可能会看到需要刷新的无效项目 _**未直接编辑**_. 例如，当您编辑目录中的任何产品并将其分配给任何类别时，或者当您更改任何相关的产品规则时，会发生此失效。

此 _[!UICONTROL Cache Management]_页面显示每个主缓存及其关联标记的状态。 右上角的大按钮可用于刷新缓存或包含所有内容的缓存存储。 页面底部提供了额外的按钮，用于刷新目录产品图像缓存和JavaScript/CSS缓存。

清除缓存后，请始终刷新浏览器，以确保您能够看到最新文件。 清除Commerce缓存不会清除Web浏览器缓存。 您可能需要清除浏览器缓存才能查看更新的内容。

有关其他技术信息，请参阅 [缓存概述](https://developer.adobe.com/commerce/frontend-core/guide/caching/){：target=&quot;_blank&quot;}在 _Commerce前端开发指南_.

访问 _[!UICONTROL Cache Management]_执行下列操作之一，创建页面：

- 单击 **[!UICONTROL Cache Management]** 工作区上方消息中的链接。
- 在 _管理员_ 侧栏，转到 **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**.

![缓存管理](./assets/cache-management-invalid.png){width="700" zoomable="yes"}

## 缓存最佳实践

在Commerce中，重新索引和缓存具有不同的目的。 [索引](index-management.md) 跟踪数据库信息以提高搜索性能、加快存储前端的数据检索等等。 缓存可保存加载的数据、图像、格式等，以提高加载和访问店面的性能。

- 安装扩展/模块后，请始终刷新缓存。 您可以安装一个或多个扩展，然后刷新缓存。
- 安装Commerce后刷新缓存。 对于全新安装，您还应重新编入索引。
- 从一种开源版本或商业版本升级到另一种版本后刷新缓存。
- 刷新缓存时，请考虑缓存类型并计划在非高峰期进行刷新。 例如，选择一个很少客户访问网站的时间，如深夜或清晨。 高峰期清除某些缓存类型会导致管理员负载过高，并可能导致站点停机，直到运行完毕。
- 时间 [重新索引](index-management.md)，您无需同时执行刷新缓存。

## 缓存管理角色资源

特定缓存维护操作的访问权限可以按角色分配给用户，包括查看、切换和刷新缓存的选项。 Adobe建议仅对管理员级别的用户启用刷新操作。 提供对所有缓存管理功能的访问可能会影响您店面的性能。

![角色资源 — 缓存管理](./assets/permissions-role-resources-cache-management.png){width="600" zoomable="yes"}

有关分配资源以授予管理员用户帐户访问权限的信息，请参阅 [角色资源](permissions-user-roles.md#role-resources). 以下资源控制对缓存管理工具的访问：

- [!UICONTROL Clean Cache Actions]

   - [!UICONTROL Flush Cache Storage]
   - [!UICONTROL Flush Magento Cache]

- [!UICONTROL Cache Type Management]

   - [!UICONTROL Toggle Cache Type]
   - [!UICONTROL Refresh Cache Type]

- [!UICONTROL Additional Cache Management]

   - [!UICONTROL Catalog Images Cache]
   - [!UICONTROL Flush Js/Css]
   - [!UICONTROL Flush Static Files]

## 刷新特定缓存

1. 对于每个要刷新的缓存，选中行开头的复选框。

1. 设置 **[!UICONTROL Actions]** 到 `Refresh` 并单击 **[!UICONTROL Submit]**.

## 执行成批活动刷新

1. 要选择一组缓存，请设置 **[!UICONTROL Mass Actions]** 更改为以下任一项：

   - `Select All`
   - `Select Visible`

1. 选中操作要定位的每个缓存对应的复选框。

1. 设置 **[!UICONTROL Actions]** 到 `Refresh` 并单击 **[!UICONTROL Submit]**.

## 刷新产品图像缓存

1. 下 _[!UICONTROL Additional Cache Management]_，单击&#x200B;**[!UICONTROL Flush Catalog Images Cache]**以清除预生成的产品图像文件。

   此 `Image cache was cleaned` 消息显示在工作区顶部。

1. 清除浏览器的缓存。

## 刷新JavaScript/CSS缓存

1. 下 _[!UICONTROL Additional Cache Management]_，单击&#x200B;**[!UICONTROL Flush JavaScript/CSS Cache]**清除已合并到单个文件中的任何JavaScript和CSS文件。

   此 `The JavaScript/CSS cache has been cleaned` 消息显示在工作区顶部。

1. 清除浏览器的缓存。

## 使用命令行刷新

Commerce使用命令行提供了额外的刷新缓存选项。 这些选项可能需要开发人员支持才能完成。 有关完整的详细信息和命令选项，请参见 [管理缓存](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/manage-cache.html){：target=&quot;_blank&quot;}在 _配置指南_.

## 控件

| 控件 | 描述 |
|--- |--- |
| [!UICONTROL Mass Actions] | 选中多个缓存的复选框。 选项： <br/>**[!UICONTROL Select All]**— 选中所有缓存的复选框。<br/>**&#x200B;取消全选&#x200B;**— 清除所有缓存的复选框。<br/>**[!UICONTROL Select Visible]**  — 选中所有可见缓存的复选框。 <br/>**[!UICONTROL Unselect Visible]**— 清除所有可见缓存的复选框。 |
| [!UICONTROL Actions] | 确定要应用于所有选定缓存的操作。 选项： <br/>**[!UICONTROL Enable]**— 启用所有选定的缓存。<br/>**[!UICONTROL Disable]**  — 禁用所有选定的缓存。 <br/>**[!UICONTROL Refresh]**— 刷新所有选定的缓存。 |
| [!UICONTROL Submit] | 将操作应用于所有选定的缓存。 |

{style="table-layout:auto"}

### 按钮

| 按钮 | 描述 |
|--- |--- |
| [!UICONTROL Flush Magento Cache] | 删除默认Commerce缓存中的所有项目(`var/cache`)，根据他们关联的Commerce标记。 |
| [!UICONTROL Flush Cache Storage] | 从缓存中删除所有项目，而不考虑Commerce标记。 如果您的系统使用备用缓存位置，则其他应用程序使用的任何缓存文件都将在此过程中删除。 |
| [!UICONTROL Flush Catalog Images Cache] | 删除存储在中的所有自动调整大小的带水印的目录图像 `media/catalog/product/cache`. 如果最近上传的图像未反映在目录中，请尝试刷新目录并刷新浏览器。 |
| [!UICONTROL Flush JavaScript/CSS Cache] | 从缓存中删除JavaScript和CSS文件的合并副本。 如果最近对样式表或JavaScript所做的更改未反映在存储中，请尝试刷新JavaScript/CSS缓存并刷新浏览器。 |
| [!UICONTROL Flush Static Files Cache] | 删除预处理视图文件和静态文件。 |

{style="table-layout:auto"}

### 缓存

| 缓存 | 描述 | 关联的标记 |
| ----- | ----------- | -------------- |
| [!UICONTROL Configuration] | 跨模块收集并合并的各种XML配置。<br>**[!UICONTROL System]**-  `config.xml`，`local.xml`<br>**[!UICONTROL Module]** -  `config.xml` | `CONFIG` |
| [!UICONTROL Layouts] | 布局构建说明。 | `LAYOUT_GENERAL_CACHE_TAG` |
| [!UICONTROL Blocks HTML output] | 页块HTML。 | `BLOCK_HTML` |
| [!UICONTROL Collections Data] | 收藏集数据文件。 | `COLLECTION_DATA` |
| [!UICONTROL Reflection Data] | 清除通常在运行时生成的API接口反射数据。 | `REFLECTION` |
| [!UICONTROL Database DDL operations] | DDL查询的结果，如描述表或索引。 | `DB_DDL` |
| [!UICONTROL Compiled Config] | 代码编译的结果。 | `COMPILED_CONFIG` |
| [!UICONTROL EAV types and attributes] | 实体类型声明缓存。 | `EAV` |
| [!UICONTROL Customer Notification] | 显示在用户界面中的临时通知。 | `CUSTOMER_NOTIFICATION` |
| [!UICONTROL Integrations Configuration] | 集成配置文件。 | `INTEGRATION` |
| [!UICONTROL Integrations API Configuration] | 集成API配置文件。 | `INTEGRATION_API_CONFIG` |
| [!UICONTROL Page Cache] | 全页缓存。 | `FPC` |
| [!UICONTROL Translations] | 翻译文件。 | `TRANSLATE` |
| [!UICONTROL Web Services Configuration] | REST和SOAP配置，生成的WSDL文件。 | `WEBSERVICE` |
| [!UICONTROL Target Rule] | Target规则索引 | `TARGET_RULE` |

{style="table-layout:auto"}

## 全页缓存

Adobe Commerce和Magento Open Source使用服务器上的全页缓存快速显示类别、产品和CMS页面。 全页缓存可缩短响应时间并降低服务器的负载。 如果没有缓存，每个页面可能需要运行代码块并从数据库中检索信息。 但是，在启用全页缓存的情况下，可以直接从缓存中读取完全生成的页面。

>[!NOTE]
>
>建议 [清漆缓存](https://varnish-cache.org/){：target=&quot;_blank&quot;}只能在生产环境中使用。

缓存的内容可用于处理来自类似访问类型的请求。 因此，向临时访客显示的页面可能与向客户显示的页面不同。 对于缓存，每次访问属于以下三种类型之一：

- `Non-sessioned`  — 在非会话访问期间，购物者会查看页面，但不会与商店进行交互。 系统缓存每个查看页面的内容，并将它们提供给其他无会话购物者。
- `Sessioned`  — 在会话访问期间，会为通过比较产品或向购物车添加产品等活动与商店进行交互的购物者分配一个会话ID。 会话期间生成的缓存页面仅供该购物者在会话期间使用。
- `Customer`  — 为已在您的商店和商店中注册了帐户并登录到其帐户的用户创建客户会话。 在该会议中，可以向客户显示基于其分配的客户组的特殊优惠、促销和价格。

有关技术信息，请参阅 [配置和使用清漆](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cache/varnish/config-varnish.html){：target=&quot;_blank&quot;}和 [将Redis用于Commerce页面和默认缓存](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cache/redis/redis-pg-cache.html){：target=&quot;_blank&quot;}在 _配置指南_.

**_要配置全页缓存，请执行以下操作：_**

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中，展开 **[!UICONTROL Advanced]** 并选择 **[!UICONTROL System]**.

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Full Page Cache]** 部分。

   ![高级配置 — 全页缓存](../configuration-reference/advanced/assets/system-full-page-cache.png){width="600" zoomable="yes"}

1. 设置 **[!UICONTROL Caching Application]** 更改为以下任一项：

   - `Built-in Application`
   - `Varnish Caching`

1. 要设置页面缓存的超时，请输入 **[!UICONTROL TTL for public content]**. (默认值为 `86400`)

1. 如果使用清漆，请完成 **[!UICONTROL Varnish Configuration]** 部分如下所示：

   - **[!UICONTROL Access list]**  — 输入可以清除Varnish配置以生成配置文件的IP地址。 用逗号分隔多个条目。 默认值为 `localhost`.

   - **[!UICONTROL Backend host]**  — 输入生成配置文件的后端主机的IP地址。 默认值为 `localhost`.

   - **[!UICONTROL Backend port]**  — 标识用于生成配置文件的后端端口。 默认值为： `8080`.

   - **[!UICONTROL Grace period]**  — 指定用作生成配置文件的宽限期的秒数。 请参阅 [高级清漆配置](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cache/config-varnish-advanced.html) 在 _配置指南_.

   - 要将配置导出为 `varnish.vcl` 文件，单击您使用的Varnish版本的按钮。

   ![高级配置 — 全页缓存清漆](../configuration-reference/advanced/assets/system-full-page-cache-varnish.png){width="600" zoomable="yes"}

1. 完成后，单击 **[!UICONTROL Save Config]**.

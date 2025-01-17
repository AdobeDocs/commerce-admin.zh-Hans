---
title: '[!UICONTROL General] &amp；gt； [!UICONTROL General]'
description: 查看Commerce管理员的[!UICONTROL General] &amp；gt； [!UICONTROL General]页面上的配置设置。
exl-id: 67760d24-ad12-4c49-9649-0607c57f5cf0
feature: Configuration, System
source-git-commit: 54f6c7abf38e4368a843b7cf042ccd9af19239b2
workflow-type: tm+mt
source-wordcount: '999'
ht-degree: 0%

---

# [!UICONTROL General] > [!UICONTROL General]

{{config}}

## [!UICONTROL Country Options]

有关这些配置字段和选项的更多详细信息，请参阅[国家选项](../../getting-started/store-details.md#country-options)。

![常规>国家/地区选项](./assets/general-country-options.png)<!-- zoom -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Default Country] | 商店视图 | 您的商店所在的国家/地区。 |
| [!UICONTROL Allow Countries] | 网站 | 您接受订单的国家/地区。 |
| [!UICONTROL Zip/Postal Code is Optional for] | 全局 | 在配送地址中不需要邮政编码的国家/地区。 |
| [!UICONTROL European Union Countries] | 全局 | 欧洲联盟成员国。 |
| [!UICONTROL Top Destinations] | 商店视图 | 您定位销售的主要国家/地区。 |

{style="table-layout:auto"}

## [!UICONTROL State Options]

有关这些配置字段和选项的更多详细信息，请参阅[状态选项](../../getting-started/store-details.md#state-options)。

![常规>状态选项](./assets/general-state-options.png)<!-- zoom -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL State is required for] | 全局 | 要求将地区或州包含在邮政地址中的国家/地区（您开展业务的国家/地区）。 |
| [!UICONTROL Allow to Choose State if It is Optional for Country] | 全局 | 对于不需要的国家/地区，确定&#x200B;_地区/州_&#x200B;字段是否包含在客户的邮政地址中。<br /> <br />**`Yes`**— 在客户地址中包含&#x200B;_地区/州_字段，即使该国家/地区不要求填写此字段也是如此。<br />**`No`** — 如果国家/地区不要求，则省略客户地址中的地区/州字段。 |

{style="table-layout:auto"}

## [!UICONTROL Locale Options]

有关这些配置字段和选项的更多详细信息，请参阅[区域设置选项](../../getting-started/store-details.md#locale-options)。

![常规>区域设置选项](./assets/general-locale-options.png)<!-- zoom -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Timezone] | 网站 | 网站提供服务的主要市场的时区。 通常，时区与企业实际地点使用的时区相同。 |
| [!UICONTROL Locale] | 商店视图 | 商店视图提供的市场中使用的语言、货币和测量系统。 |
| [!UICONTROL Weight Unit] | 商店视图 | 通常用于来自区域设置的装运的度量单位。 选项： `lbs` / `kgs` |
| [!UICONTROL First Day of Week] | 商店视图 | 该天被视为商店视图提供的一周中的第一天。 |
| [!UICONTROL Weekend Days] | 商店视图 | 周末在商店景象所服务的市场里度过的日子。 |

{style="table-layout:auto"}

## [!UICONTROL Website Restrictions]

{{ee-feature}}

![常规>网站限制](./assets/general-website-restrictions.png)<!-- zoom -->

有关更改这些设置的详细信息，请参阅&#x200B;_促销和促销指南_&#x200B;中的[访问限制](../../merchandising-promotions/event-configure.md#access-restrictions)。

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Access Restriction] | 网站 | 确定网站是否正在受限模式下运行。<br /> <br />**`Yes`**— 以下字段中设置的方式限制了网站访问。<br />**`No`** — 已禁用限制，以下设置无效。 |
| [!UICONTROL Restriction Mode] | 网站 | 确定适用于网站的访问限制的类型。<br /> <br />**`Website Closed`**— 对店面的所有访问都受到限制，店面URL会暂时重定向到登陆页面。 此设置在站点维护期间或启动之前很有用。<br />**`Private Sales: Login Only`** — 只有注册客户才能登录以访问店面。 所有店面URL会暂时重定向到指定的登陆页面或登录表单。 用户无法在此模式下创建帐户。<br />**`Private Sales: Login and Register`**— 用户必须登录才能访问店面。 所有店面URL会暂时重定向到登录表单，直到用户登录为止。 当网站处于此模式时，用户可以注册帐户。 |
| [!UICONTROL Startup Page] | 商店视图 | 当网站处于“私人销售”模式时，此设置将确定在客户登录之前显示的页面。<br />  <br />**`To login form`**— 用户将被重定向到登录表单，直到他们登录。<br />**`To landing page`** — 用户被重定向到下面指定的静态页面，直到他们登录。<br /> <br />**_重要信息！_**确保包含指定登陆页面中的登录页面链接，以便客户可以登录访问整个网站。 |
| [!UICONTROL Landing Page] | 商店视图 | 确定网站处于“专用销售”模式时显示的第一个页面。 |
| [!UICONTROL HTTP Response] | 网站 | 确定在网站关闭且机器人、爬虫程序或爬虫程序尝试连接时发送的HTTP响应。<br /> <br />**`503 Service unavailable`**— 页面不可用，但爬虫程序不应更新索引。<br />**`200 OK`** — 登陆页面正确，爬虫程序应将登陆页面视为网站上的唯一页面。 |
| [!UICONTROL Enable Autocomplete on login/forgot password forms] | 网站 | 确定&#x200B;_登录_&#x200B;和&#x200B;_忘记密码_&#x200B;表单上的字段是否自动填写以前的条目。 选项： `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Store Information]

![常规>存储信息](./assets/general-store-information.png)<!-- zoom -->

有关更改这些设置的详细信息，请参阅&#x200B;_入门指南_&#x200B;中的[存储信息](../../getting-started/store-details.md)。

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Store Name] | 商店视图 | 与存储视图关联的存储的名称。 |
| [!UICONTROL Store Phone Number] | 商店视图 | 商店的主电话号码（与商店视图关联）已针对商业开放。 例如：周一 — 周五，9-5，星期六9 — 中午PST |
| 国家/地区 | 网站 | 运营网站的企业的国家/地区。 |
| [!UICONTROL Region/State] | 网站 | 运营网站的业务的地区或省/自治区/直辖市。 |
| [!UICONTROL ZIP/Postal Code] | 网站 | 运营网站的业务的邮政编码。 |
| [!UICONTROL City] | 网站 | 运营网站的企业的城市位置。 |
| [!UICONTROL Street Address] | 网站 | 运营网站的企业的街道或邮寄地址。 |
| [!UICONTROL Street Address Line 2|]网站 | 商业街道地址的第二行（如果需要）。 |
| [!UICONTROL VAT Number] | 网站 | 拥有Commerce安装的业务的增值税号（如果适用）。 |
| [!UICONTROL Validate VAT Number] |  | 验证增值税标识号。 |

{style="table-layout:auto"}

## [!UICONTROL Single-Store Mode]

![常规>单存储模式](./assets/general-single-store-mode.png)<!-- zoom -->

有关更改这些设置的详细信息，请参阅&#x200B;_入门指南_&#x200B;中的[单商店模式](../../getting-started/websites-stores-views.md#single-store-mode)。

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Enable Single-Store Mode] | 全局 | 为单存储安装启用时，将隐藏配置作用域框和相关字段标签选项： `Yes` / `No` <br/>**_注意：_**对于具有多个视图的存储区，将忽略单存储模式。<br/>启用单商店模式会将所有目录和产品商店特定数据从默认商店视图复制到所有商店视图范围。 如果该商店只有一个商店审核，则它仅会复制目录和产品数据。 如果存储有一个禁用了的存储和一个启用的存储，则它将不会复制目录和产品数据。<br/>启用单存储模式会忽略特定于内容的数据的存储审核特定配置设置。 而是使用在全局级别范围中定义的配置设置，以确保管理员UI与店面之间的一致性。 |

{style="table-layout:auto"}

## [!UICONTROL Data Services]

![常规>数据服务](./assets/general-data-services.png)<!-- zoom -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Commerce Events Enabled] | 全局 | 如果您是医疗保健客户，并且安装了[数据服务HIPAA](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/hipaa-readiness.html#installation)扩展，则默认情况下会关闭此配置。 因此，将不再捕获Live Search和产品Recommendations使用的店面事件数据。 这是因为店面事件数据是在客户端生成的。 要继续捕获和发送店面事件数据以供[实时搜索](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/overview)和[产品Recommendations](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/product-recommendations/guide-overview)服务使用，请将&#x200B;**已启用Commerce事件**&#x200B;设置为`Yes`。 |

{style="table-layout:auto"}

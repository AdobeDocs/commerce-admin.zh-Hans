---
title: ’[!UICONTROL General] &gt； [!UICONTROL General]’
description: 查看 [!UICONTROL General] &gt； [!UICONTROL General] 商务管理员页面。
exl-id: 67760d24-ad12-4c49-9649-0607c57f5cf0
feature: Configuration, System
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '830'
ht-degree: 0%

---

# [!UICONTROL General] > [!UICONTROL General]

{{config}}

## [!UICONTROL Country Options]

请参阅 [国家/地区选项](../../getting-started/store-details.md#country-options) 以了解有关这些配置字段和选项的更多详细信息。

![常规>国家/地区选项](./assets/general-country-options.png)<!-- zoom -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Default Country] | 商店视图 | 您的商店所在的国家/地区。 |
| [!UICONTROL Allow Countries] | 网站 | 您接受订单的国家/地区。 |
| [!UICONTROL Zip/Postal Code is Optional for] | 全局 | 在配送地址中不需要邮政编码的国家/地区。 |
| [!UICONTROL European Union Countries] | 全局 | 欧洲联盟成员国。 |
| [!UICONTROL Top Destinations] | 商店视图 | 您定位销售的主要国家/地区。 |

{style="table-layout:auto"}

## [!UICONTROL State Options]

请参阅 [状态选项](../../getting-started/store-details.md#state-options) 以了解有关这些配置字段和选项的更多详细信息。

![“常规”>“状态选项”](./assets/general-state-options.png)<!-- zoom -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL State is required for] | 全局 | 要求将地区或州包含在邮政地址中的国家/地区（您开展业务的国家/地区）。 |
| [!UICONTROL Allow to Choose State if It is Optional for Country] | 全局 | 对于不需要的国家/地区，确定 _地区/州_ 字段包含在客户的邮政地址中。<br /> <br />**`Yes`**— 包括 _地区/州_ 客户地址中的字段，即使国家/地区不要求也是如此。<br />**`No`**  — 如果国家/地区不要求，则省略客户地址中的“地区/州”字段。 |

{style="table-layout:auto"}

## [!UICONTROL Locale Options]

请参阅 [区域设置选项](../../getting-started/store-details.md#locale-options) 以了解有关这些配置字段和选项的更多详细信息。

![常规>区域设置选项](./assets/general-locale-options.png)<!-- zoom -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
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

有关更改这些设置的详细信息，请参阅 [访问限制](../../merchandising-promotions/event-configure.md#access-restrictions) 在 _Merchandising and Promotions指南_.

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Access Restriction] | 网站 | 确定网站是否正在受限模式下运行。<br /> <br />**`Yes`**— 按照以下字段中设置的方式限制网站访问。<br />**`No`**  — 已禁用限制，并且以下设置无效。 |
| [!UICONTROL Restriction Mode] | 网站 | 确定适用于网站的访问限制的类型。<br /> <br />**`Website Closed`**— 对店面的所有访问都受到限制，店面URL会暂时重定向到登陆页面。 此设置在站点维护期间或启动之前很有用。<br />**`Private Sales: Login Only`**  — 只有注册客户才能登录访问店面。 所有店面URL会暂时重定向到指定的登陆页面或登录表单。 用户无法在此模式下创建帐户。<br />**`Private Sales: Login and Register`**— 用户必须登录才能访问店面。 所有店面URL会暂时重定向到登录表单，直到用户登录为止。 当网站处于此模式时，用户可以注册帐户。 |
| [!UICONTROL Startup Page] | 商店视图 | 当网站处于“私人销售”模式时，此设置将确定在客户登录之前显示的页面。<br />  <br />**`To login form`**— 用户将被重定向到登录表单，直到他们登录。<br />**`To landing page`**  — 用户将被重定向到下面指定的静态页面，直到他们登录。<br /> <br />**_重要提示！_**确保包含指定登陆页面中的登录页面链接，以便客户能够登录以访问整个网站。 |
| [!UICONTROL Landing Page] | 商店视图 | 确定网站处于“专用销售”模式时显示的第一个页面。 |
| [!UICONTROL HTTP Response] | 网站 | 确定在网站关闭且机器人、爬虫程序或爬虫程序尝试连接时发送的HTTP响应。<br /> <br />**`503 Service unavailable`**— 页面不可用，但爬虫程序不应更新索引。<br />**`200 OK`**  — 登陆页面正确，爬虫程序应将登陆页面视为网站上的唯一页面。 |
| [!UICONTROL Enable Autocomplete on login/forgot password forms] | 网站 | 确定 _登录_ 和 _忘记密码_ 表单会自动从先前的条目中填写。 选项： `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Store Information]

![常规>存储信息](./assets/general-store-information.png)<!-- zoom -->

有关更改这些设置的详细信息，请参阅 [存储信息](../../getting-started/store-details.md) 在 _快速入门指南_.

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Store Name] | 商店视图 | 与存储视图关联的存储的名称。 |
| [!UICONTROL Store Phone Number] | 商店视图 | 商店的主电话号码（与商店视图关联）已针对商业开放。 例如：周一 — 周五，9-5，星期六9 — 中午PST |
| 国家/地区 | 网站 | 运营网站的企业的国家/地区。 |
| [!UICONTROL Region/State] | 网站 | 运营网站的业务的地区或省/自治区/直辖市。 |
| [!UICONTROL ZIP/Postal Code] | 网站 | 运营网站的业务的邮政编码。 |
| [!UICONTROL City] | 网站 | 运营网站的企业的城市位置。 |
| [!UICONTROL Street Address] | 网站 | 运营网站的企业的街道或邮寄地址。 |
| [!UICONTROL Street Address Line 2|]网站 | 商业街道地址的第二行（如果需要）。 |
| [!UICONTROL VAT Number] | 网站 | Commerce安装所属业务的增值税号（如果适用）。 |
| [!UICONTROL Validate VAT Number] |  | 验证增值税标识号。 |

{style="table-layout:auto"}

## [!UICONTROL Single-Store Mode]

![常规>单存储模式](./assets/general-single-store-mode.png)<!-- zoom -->

有关更改这些设置的详细信息，请参阅 [单存储模式](../../getting-started/websites-stores-views.md#single-store-mode) 在 _快速入门指南_.

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Enable Single-Store Mode] | 全局 | 为单存储安装启用时，将隐藏配置范围框和相关字段标签选项： `Yes` / `No` <br/>**_注意：_**对于具有多个视图的商店，将忽略单商店模式。 |

{style="table-layout:auto"}

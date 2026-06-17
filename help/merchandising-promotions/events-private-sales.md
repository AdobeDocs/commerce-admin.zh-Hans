---
title: 私人销售和活动
description: 了解如何利用私人销售和其他目录活动增加对现有客户群的销售，并产生新的商机和新的潜在客户。
exl-id: 0b890463-b1e5-4327-8d8a-372afd53312a
feature: Reporting, Promotions/Events
badgePaas: label="仅限PaaS" type="Informative" url="https://experienceleague.adobe.com/zh-hans/docs/commerce/user-guides/product-solutions" tooltip="仅适用于云项目（Adobe管理的PaaS基础架构）和内部部署项目上的Adobe Commerce 。"
TQID: https://experienceleague.adobe.com/8MvnlOp5muOQbx3b7dSKguc4wf-k47v9AtaHXu7b9pU
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
  - id: f42e0a1a-0d79-488d-a83f-f2c30672b137
subfeature_v2:
  - id: bd0aa680-a881-4f35-9dcf-843b0574bc5f
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 458
ht-degree: 0%

---

# 私人销售和活动

{{ee-feature}}

私人销售和其他目录活动是利用现有客户群来产生轰动效应和新商机，或卸载剩余库存的一种好方法。 您可以创建限时销售、将销售限定于特定成员，或创建独立的专用销售页。 您还可以定义邀请和活动详细信息。 通过为最佳客户提供VIP待遇，提高品牌忠诚度并产生轰动。 提供对仅会员销售或私人销售的排他性访问权限，以提高品牌忠诚度。 你也可以用这些销售来清算多余的商品。 客户组在仅设置这些类型的成员和VIP销售人员时非常有用。

![示例店面 — 主页上的事件](./assets/storefront-event-home-page.png){width="700" zoomable="yes"}

## 事件管理组件

- **类别** — 每个事件都与您目录中的[类别](../catalog/category-create.md)关联。

- **事件** — 事件销售额基于开始和结束日期。 您可以使用[倒计时记号](#event-ticker)来显示剩余时间。

- **目录事件轮播** — 在配置中启用[目录事件小组件](../content-design/widget-event-carousel.md)后，它可作为打开和即将发生的事件的列表放置在存储页面上，并按结束日期排序。 如果两个或更多事件的结束日期相同，则事件将根据配置中指定的顺序排序。

- **[!UICONTROL Websites]** — 类别权限主要基于[客户组](../customers/customer-groups.md)。

- **类别权限** - [类别权限](../catalog/category-permissions.md)可让您完全控制给定类别中可能发生的特定活动。

- **访问限制** — 通过重定向到登陆页面、登录页面或注册页面，阻止公共[访问](event-configure.md#restrict-access)网站。

- **邀请** — 发送电子邮件时，会附上在商店中创建帐户的链接。 您可以将创建帐户的能力限制为仅接收[邀请](invitations.md)的用户。

- **私人销售报告** - [私人销售报告](../getting-started/private-sales-reports.md)提供了有关已发送的邀请、已邀请的客户和转换的信息。

## 事件记号

滚动条块会为未结事件显示一个倒计时滚动条，其中包含即将发生的事件的开始和结束日期。 如果某个事件已关闭，则滚动条会显示开始日期和结束日期。

![店面示例 — 活动轮播](./assets/storefront-event-ticker-carousel.png){width="700" zoomable="yes"}

如果为某个事件启用了类别页面滚动条，则滚动条块将显示在类别列表的顶部。 如果启用了产品页面滚动条，则滚动条块也会出现在与类别关联的任何产品的产品页面的顶部。

当您[创建事件](event-create.md)时，可以启用事件记号。

![店面示例 — 事件侧栏](./assets/storefront-event-sidebar.png){width="700" zoomable="yes"}

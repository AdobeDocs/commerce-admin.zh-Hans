---
title: 大规模个性化
description: 了解Adobe Commerce中的哪些功能允许您为购物者创建个性化体验。
feature: Customers, Storefront, Personalization
exl-id: 9546e1b8-796b-4694-8396-773a2b0e9c12
source-git-commit: 5f40c98324c3033cdeb8a11e89a71497ced890b8
workflow-type: tm+mt
source-wordcount: '1341'
ht-degree: 0%

---

# 大规模个性化

大规模&#x200B;个性化使企业能够根据即时上下文和之前观察到的行为对每个客户接触点的购物体验进行个性化。 目标是每次都提供最相关、最个性化的体验。

要了解提供个性化购物体验的好处，请下载 [_大规模个性化快速入门_](https://business.adobe.com/resources/reports/getting-started-with-personalization-at-scale.html) 报告。

创建个性化的购物体验需要您了解了解了解客户上下文所需的数据类型。 从那里，您将了解Adobe Commerce的一些功能，这些功能使用这些数据解锁创建个性化购物体验所需的客户洞察。

下图说明了个性化购物体验所涉及的概念：

![构建个性化管道](assets/personalization-journey.png){width="700" zoomable="yes"}

本文更详细地讨论了上述各个概念。

## 如何个性化购物体验

成功的个性化始于客户上下文。 在此部分中，您将了解可用于帮助您构建客户上下文的数据类型。

### 店面数据

店面数据（也称为行为或浏览器数据）可揭示关于购物者如何与您的网站交互的洞察。 例如：

- 我的购物者最感兴趣的产品和类别是什么？
- 我的购物者最热衷使用哪种搜索查询器？
- 我的购物者是否在将产品添加到购物车后放弃它？
- 我的购物者使用台式机还是移动设备浏览器？

以下店面事件会捕获可帮助您回答这些问题的数据：

- [pageView](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [searchRequestSent](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [searchResponseReceived](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [productPageView](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [addToCart](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [openCart](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [登录](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [注销](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [startCheckout](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [completeCheckout](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [createRequisitionList](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [addToRequisitionList](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [removeFromRequisitionList](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)

### 后台数据

后台数据（也称为服务器端数据）可揭示对订单生命周期的洞察。 例如：

- 是否有根据季节更频繁购买的产品？
- 我的购物者是否返回产品？
- 如何计算存留期客户值？

以下后台事件捕获的数据可帮助您回答这些问题：

- [orderPlaced](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice)
- [orderItemsReturnedInitiated](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice)
- [orderItemsShipped](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice)
- [orderCanceled](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice)

### 客户个人资料和区段数据

客户配置文件数据可以揭示关于您的购物者是什么以及他们符合哪些区段的洞察。 例如：

- 名称
- 性别
- 地址
- 忠诚度状态
- 电话号码
- 电子邮件地址
- 忠诚度状态
- 电话号码
- 电子邮件地址
- 升级资格
- 跨渠道购物者
- 新产品前景
- 金牌、银牌或铜牌忠诚会员

以下配置文件事件会捕获帮助您回答这些问题的数据：

- [个人资料记录](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-profilerecord)
- [帐户已创建](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice)
- [帐户已更新](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice)
- [帐户已删除](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice)

店面、后台和配置文件数据构成了Commerce客户和订单上下文的基础，这有助于您了解客户正在查看并最终购买的产品。 然后，您可以定位他们的兴趣并个性化他们的体验。 在下一部分中，您将了解可与购物者互动的个性化体验类型。

## 个性化体验的类型

Commerce中的客户和订单上下文数据可激发以下类型的个性化体验：

| 体验 | 描述 |
|---|---|
| **产品发现** | 包含的促销服务 [部署为SaaS](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/user-guides/integration-services/saas). 这些功能允许您使用行为数据、产品属性和库存级别，从而跨搜索结果、产品推荐和浏览页面自动个性化产品发现。 这些功能都使用 [Adobe Sensei人工智能](https://business.adobe.com/products/sensei/adobe-sensei.html). |
| **网站内容** | 是指能够根据当前客户浏览您的网站来部署个性化的动态内容块。 |
| **优惠和营销活动** | 允许您根据区段数据部署个性化促销内容。 |
| **测量** | 使用数据智能更好地了解您的业务，包括收入、渠道和商品表现、促销活动等。 |

在接下来的两个部分中，您将了解如何使用此数据在中创建个性化体验 [Adobe Experience Platform](#using-commerce-data-in-adobe-experience-platform) 和 [原生Commerce功能](#using-commerce-data-in-native-commerce-features).

## 在Adobe Experience Platform中使用Commerce数据

要为所有渠道的购物者创建个性化体验，请使用将您的Commerce数据发送到Experience PlatformEdge Network [[!DNL Data Connection]](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/overview) 扩展。

![数据如何流向Experience Platform边缘](assets/commerce-edge.png){width="700" zoomable="yes"}

在上图中，您的店面、后台和客户个人资料数据使用SDK、API和源连接器发送到Experience Platform边缘。 您无需完全了解这些部分的工作方式，因为扩展会为您处理数据共享的复杂性。 当事件数据位于边缘时，您可以将该数据提取到其他Experience Platform应用程序中。

下表重点介绍了一些可用的Experience Platform应用程序以及这些应用程序如何使用您的Commerce数据。

| 体验 | 应用程序 | 如何使用Commerce数据 |
|---|---|---|
| **网站内容** | [Adobe [!DNL Real-Time CDP]](https://experienceleague.adobe.com/en/docs/experience-platform/rtcdp/intro/rtcdp-intro/overview) | Adobe Commerce数据有助于建立统一的客户档案，Real-Time CDP可将来自不同来源(ERP、CRM、CMS、POS)的数据拼合到单个档案中。 Real-Time CDP还可以创建基于规则和基于人工智能的区段，以便在您的营销解决方案集中使用。 您还可以使用Real-Time CDP受众来个性化内容块、促销活动和相关产品规则。 请参阅 [[!DNL Audience Activation]](../customers/audience-activation.md) 以了解更多信息。&#x200B; |
|  | [Adobe [!DNL Target]](https://experienceleague.adobe.com/en/docs/target/using/introduction/intro) | Adobe Commerce数据可在Adobe中激活 [!DNL Target] 用于测试、优化和创建动态登陆页面。 您可以根据发送的Commerce数据，个性化设置内容在页面上的显示顺序，例如描述、规范、审查和推荐产品。 |
| **优惠和营销活动** | [Adobe [!DNL Journey Optimizer]](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/get-started) | Adobe Commerce行为和后台数据可以触发个性化的全渠道历程，包括电子邮件营销活动、短信、推送通知等&#x200B;。 |
| **测量** | [Adobe [!DNL Analytics]](https://experienceleague.adobe.com/en/docs/analytics/analyze/admin-overview/analytics-overview) 和 [客户 [!DNL Journey Analytics]](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-overview) | Commerce将店面和后台数据发送给客户 [!DNL Journey Analytics] (并且只要Adobe店面数据 [!DNL Analytics])，以允许在Adobe Commerce Intelligence中实现超出基本指标（如收入、商品和促销）的更丰富分析&#x200B;。 |

要详细了解如何将Commerce数据发送到Experience Platform，请参阅 [数据连接](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/overview).

## 在本机Commerce功能中使用Commerce数据

在以下部分中，您将了解如何使用本机Commerce功能(如产品Recommendations和Live Search)创建个性化的购物体验。 您还将了解名为的功能 [!DNL Audience Activation]，后者使用来自Experience Platform中可用的Real-Time CDP产品的数据，如前所述 [以前](#using-commerce-data-in-adobe-experience-platform). 虽然Real-Time CDP不是Commerce的原生版本，但可以通过将其信息摄取到Commerce [[!DNL Audience Activation]](../customers/audience-activation.md) 扩展。

下表突出显示可用于将Commerce客户和订单上下文数据转换为可操作洞察的Commerce功能。

| 体验 | 功能 | 描述 |
|---|---|---|
| **产品发现** | [实时搜索](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/guide-overview) | 使用AI排名算法，根据购物者的网站行为操作对搜索结果进行个性化和优化，从而提高搜索相关性和转化率。 |
|  | [产品Recommendations](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/product-recommendations/guide-overview) | 根据购物者的行为、趋势、产品相似性等显示人工智能驱动的产品推荐。 与您的Adobe Commerce目录结合使用时，产品推荐可提供极具吸引力、相关性和个性化的体验。 |
|  | [类别促销](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/live-search-admin/category-merch) | 通过实时搜索管理员访问，类别促销使用人工智能自动重新排列每个类别页面上的产品序列，以提高每个购物者的相关性和转化率。 您可以创建和管理AI支持的规则，以根据购物者操作和相关性自动在类别页面上重新排列产品顺序。 |
| **网站内容** | [受本机Commerce功能通知的动态块](https://experienceleague.adobe.com/en/docs/commerce-admin/content-design/elements/dynamic-blocks/dynamic-blocks) | 允许您根据在价格规则和客户区段中配置的逻辑提供个性化的网站内容。 |
|  | [由Real-Time CDP受众通知的动态块](../customers/audience-activation.md) | 使商家能够根据Real-Time CDP中配置的受众提供个性化的网站内容。 |
| **优惠和营销活动** | [购物车价格规则](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart) | 允许您根据一组条件将折扣应用于购物车中的商品。 |
|  | [受本机Commerce功能通知的动态块](https://experienceleague.adobe.com/en/docs/commerce-admin/content-design/elements/dynamic-blocks/dynamic-blocks) | 允许您根据Commerce中本机配置的客户区段显示个性化的横幅促销活动。 |
|  | [由Real-Time CDP受众通知的动态块](../customers/audience-activation.md) | 允许您根据Real-Time CDP中配置的受众显示个性化促销。 |
| **测量** | [Adobe Commerce Intelligence](https://experienceleague.adobe.com/en/docs/commerce-business-intelligence/mbi/getting-started) | (以前称为Magento Business Intelligence)是一个云平台，提供最佳实践见解，帮助您制定数据驱动型决策并采取清晰、知情的操作。 Adobe Commerce Intelligence可以分析您的数据，帮助您回答有关订单增长、客户行为和促销策略有效性的问题。 |

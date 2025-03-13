---
title: 大规模创建引人入胜的个性化体验
description: 了解Adobe [!DNL Commerce] 中的哪些功能允许您为购物者创建个性化体验。
feature: Customers, Storefront, Personalization
exl-id: 9546e1b8-796b-4694-8396-773a2b0e9c12
source-git-commit: 5da244a548b15863fe31b5df8b509f8e63df27c2
workflow-type: tm+mt
source-wordcount: '1808'
ht-degree: 0%

---

# 大规模创建引人入胜的个性化体验

Adobe [!DNL Commerce]为您提供强大的工具包，可个性化每个客户接触点，从而提高购物者参与度、转化率和收入。

在本文中，您将了解：

- 什么是个性化？
- 实现个性化需要哪些数据？
- Adobe [!DNL Commerce]如何解锁个性化？
- 可用的个性化用例

## 什么是个性化？

Personalization意味着定制每个客户购买体验的各个方面，以满足其独特需求、上下文和偏好。 Personalization不仅限于站点内容或推荐最适合的产品，而且还涵盖客户历程中的所有接触点，包括：

- **营销活动和通信** — 通过营销活动和通信提供相关且一致的消息
- **产品发现** — 在适当的时间向适当的客户显示适当的产品
- **促销和优惠** — 定位促销和优惠以推动每位客户进行转化
- **内容体验** — 定制网站内容，以觉得与每个客户及其历程高度相关

![Personalization的类型](assets/types-personalization.png){width="700" zoomable="yes"}

虽然这些类型的个性化体验似乎对于一小部分客户来说是可以实现的，但对于每个接触点和渠道中的数千或数百万客户来说，大规模个性化是无法做到的，所有这些实时体验都是不可能的。 在以下部分中，您将了解Adobe [!DNL Commerce]和Adobe Experience Cloud如何提供帮助。

## 实现个性化需要哪些数据？

有效的个性化需要上下文或信号，它们提供有关客户的信息，然后可以使用这些信息修改其体验。 下表提供了各种数据类型，以及Adobe [!DNL Commerce]在支持收集和激活这些数据方面所起的作用。

| 数据类型 | 店面数据（行为事件） | 后台数据（服务器端事件） | 客户个人资料和区段数据 |
|---|---|---|---|
| **定义** | 客户在您的网站上采取的点击或操作。 | 关于生命周期的信息和每个订单的详细信息（过去和当前）。 | 您的购物者是谁，他们符合哪些区段的条件。 |
| Adobe Commerce捕获的&#x200B;**事件** | [pageView](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events#pageview)<br>[productPageView](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events)<br>[searchRequestSent](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events#searchrequestsent)<br>[searchResponseReceived](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events#searchresponsereceived)<br>[addToCart](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events#addtocart)<br>[openCart](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events#opencart)<br>[signIn](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events#signin)<br>[注销](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events#signout)<br>[startCheckout](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events#startcheckout)<br>[completeCheckout](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events#completecheckout)<br>[createRequisitionList](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events#createrequisitionlist)<br>[AddList{addAddList toRequisitionList](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events#addtorequisitionlist)<br>[removeFromRequisitionList](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events#removefromrequisitionlist) | **订单状态**：<br>[订单已下达](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events-backoffice#orderplaced)<br>[订单项目已返回已启动](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events-backoffice#orderitemsreturnedinitiated)<br>[订单项目已发运](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events-backoffice#orderitemsshipped)<br>[订单已取消](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events-backoffice#ordercancelled)<br>[**订单历史记录**](https://experienceleague.adobe.com/en/docs/commerce/data-connection/fundamentals/connect-data#send-historical-order-data)：<br>- SKU，名称，价格数量，折扣<br> — 产品类别<br> — 付款金额，类型，货币<br> — 配送方式和金额<br> — 退款ID，金额，金额货币<br> — 返回原因、条件、分辨率<br> — 地址<br> — 电子邮件 | [**个人资料记录**](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events-profilerecord)：（姓名、性别、地址、忠诚度状态、电话号码、电子邮件地址）<br>**帐户状态**：<br>[帐户已创建](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events-backoffice#accountcreated)<br>[帐户已更新](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events-backoffice#accountupdated)<br>[帐户已删除](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events-backoffice#accountdeleted) |

借助所有这些丰富的第一方[!DNL Commerce]数据，您可以定位每个购物者的体验并使其个性化。 在下一部分中，您将了解[!DNL Commerce]和Adobe Experience Cloud如何帮助您创建个性化体验以及可以激活的用例。

## Adobe [!DNL Commerce]如何增强个性化功能？

通过Adobe [!DNL Commerce]数据共享，您可以收集上表中的数据类型，并将其与其他Adobe Experience Cloud产品共享，以便形成统一的客户配置文件和受众、个性化的促销活动以及丰富的分析和见解。

![数据如何流向Experience Platform Edge](assets/commerce-edge.png){width="700" zoomable="yes"}

Adobe [!DNL Commerce]数据共享包括两个关键组件：

1. [数据连接](https://experienceleague.adobe.com/en/docs/commerce/data-connection/overview)：将店面、后台和客户配置文件数据从Adobe [!DNL Commerce]共享到Adobe Experience Platform边缘网络，以便在Adobe Experience Cloud应用程序中使用，包括：

   - [Adobe [!DNL Real-Time CDP]](https://experienceleague.adobe.com/en/docs/experience-platform/rtcdp/intro/rtcdp-intro/overview)：将跨源(ERP、CRM、POS)的客户数据拼合到统一的用户档案中，并创建基于规则或基于人工智能的区段。
   - [Adobe [!DNL Journey Optimizer]](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/get-started)：启动个性化的全渠道历程，包括电子邮件营销活动、短信、推送通知等。
   - [Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-overview)和[Adobe [!DNL Analytics]](https://experienceleague.adobe.com/en/docs/analytics/analyze/admin-overview/analytics-overview)：深入了解客户和业务。
   - [Adobe [!DNL Target]](https://experienceleague.adobe.com/en/docs/target/using/introduction/intro)：测试和优化内容、推荐的产品、选件、导航等。

1. [[!DNL Audience Activation]](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/audience-activation)：使用[!DNL Real-Time CDP]受众在Adobe [!DNL Commerce]网站上个性化动态内容块、促销活动和相关产品规则。

### 跨任何渠道大规模个性化店面体验

Adobe [!DNL Commerce]可以充分利用名为[Edge Delivery Services](https://experienceleague.adobe.com/developer/commerce/storefront/)的高性能店面，在所有渠道中提供个性化体验，以AI功能为核心，速度为基础。

借助Edge Delivery Services，您可以：

- **制作个性化内容**：使用基于文档的创作、具有创作AI文本和图像变体的本机试验大规模个性化体验。 使用Assets和Generative AI内容创建可大规模生成产品和营销图像。

- **生成变体**：允许内容作者使用Generative AI创建大量个性化的AI驱动的[文本内容和图像变体](https://experienceleague.adobe.com/en/docs/experience-manager-learn/sites/generative-ai/generate-variations)Adobe Firefly。

- **通过Edge Delivery Services Storefront进行部署**：通过内置组件提供支持的Edge和Commerce功能上的内容，以便为受众创建定制的可购物体验。

- **Commerce和Adobe Experience Manager Assets**：大规模创建创作AI产品资源和变体。 跨任何渠道创建、交付和监控内容交付。

![插件：产品详细信息页面](assets/drop-in.png){width="700" zoomable="yes"}

### 开箱即用的Personalization：开始使用本机Adobe [!DNL Commerce]功能

Adobe [!DNL Commerce]通过其现成的本机功能提供强大的个性化功能。 下表描述了您可以立即激活以开始个性化历程的[!DNL Commerce]功能。

| 类别 | 功能 |
|---|---|
| 个性化产品发现 | [[!DNL Live Search]](https://experienceleague.adobe.com/en/docs/commerce/live-search/overview)：根据购物者的现场行为操作以及与AI支持的搜索的相关性，个性化和优化搜索结果。<br>[智能类别促销](https://experienceleague.adobe.com/en/docs/commerce/live-search/live-search-admin/category-merch)：根据购物者的现场行为操作和亲和力，在类别页面上进行AI驱动的产品排名。<br>[产品推荐](https://experienceleague.adobe.com/en/docs/commerce/product-recommendations/guide-overview)：基于购物者行为、趋势和亲和力的AI支持的产品推荐。<br>[相关产品规则](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/product-relationships/product-related-rules)：定义自定义规则以显示目录中的产品，以促进交叉销售和向上销售。 |
| 个性化网站内容 | [动态内容块](https://experienceleague.adobe.com/en/docs/commerce-admin/content-design/elements/dynamic-blocks/dynamic-blocks)：根据Adobe Commerce中的客户区段显示个性化内容块，例如横幅。 |
| 个性化优惠和促销 | [购物车价格规则](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart)：根据一组条件(包括Adobe [!DNL Commerce]中的客户区段)，对购物车中的商品应用折扣。 |
| 洞察和测量 | [Adobe [!DNL Commerce] 智能](https://experienceleague.adobe.com/en/docs/commerce-business-intelligence/mbi/getting-started)：了解您的个性化策略如何随着时间推移发挥作用并改进。 |

## 热门个性化用例

Adobe [!DNL Commerce]客户正在使用现成功能并将数据共享到Adobe Experience Cloud以用于各种用例。 以下部分重点介绍主要用例，并介绍如何使用Adobe [!DNL Commerce]或[!DNL Commerce]加上Experience Cloud应用程序实现这些用例。

### 个性化的营销活动和通信

| 用例 | 解决方案 |
|---|---|
| **放弃的购物车和浏览** — 当客户在展示高参与度后放弃购物车或浏览会话时，提供个性化的重新参与电子邮件或通知 | **仅Adobe [!DNL Commerce]**：<br>[电子邮件提醒](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/communications/email-reminders/email-reminder-rules)<br>**包含Adobe Journey Optimizer**：<br>[!DNL Commerce]数据的Adobe [!DNL Commerce]用作全渠道放弃历程的触发器。 根据客户属性、他们放弃的内容、其他购物行为和过去购买，个性化该历程。使用Adobe Journey Optimizer和Real-Time CDP的<br>Commerce：根据统一的客户配置文件和集中管理的受众定制放弃促销活动，例如创建高放弃率的受众。 |
| **集中受众创建** — 根据现场行为、过去的购买情况、配置文件属性、类别亲和度、忠诚度状态、客户价值等，创建基于规则或由AI支持的受众 | **仅Adobe [!DNL Commerce]**：<br>当[!DNL Commerce]客户创建帐户时，收集客户配置文件信息。 创建基于规则的[客户区段](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/segments/customer-segments)和客户组以个性化内容和促销活动。使用Adobe Real-Time CDP的&#x200B;<br>**Adobe [!DNL Commerce]**：<br> 跨数据源和渠道的[统一配置文件](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/home)；基于规则的受众或AI支持的受众。 |
| **基于购物者行为的个性化电子邮件/短信优惠** — 通过基于过去购买和购物者行为的定向电子邮件向客户发送个性化优惠，例如，发送客户已查看或参与的产品或类别的优惠。 | **仅Adobe [!DNL Commerce]**：<br>导出用于营销自动化解决方案的数据。带有Adobe Journey Optimizer和Real-Time CDP的&#x200B;<br>**Adobe [!DNL Commerce]**：<br>[!DNL Commerce]数据用作电子邮件或短信优惠的触发器，并提供要基于其进行个性化的信号（购物者行为）。 Real-Time CDP不是必需的，但通常情况下，这些选件和营销活动是围绕受众创建的，将在Real-Time CDP中创建和管理。 |
| **交叉或追加销售兼容的产品/品牌** — 如果客户购买了一个兼容的产品或品牌，或者该产品或品牌表示与另一个产品或品牌高度相关，请发送营销活动（电子邮件/短信）以提高交叉销售转化率。 | **仅Adobe [!DNL Commerce]**：<br>使用Adobe [!DNL Commerce] [产品推荐](https://experienceleague.adobe.com/en/docs/commerce/product-recommendations/guide-overview)推荐网站上的特定产品。 您还可以使用[相关产品规则](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/product-relationships/product-related-rules)来建议其他产品。具有&#x200B;[!DNL Target]**：<br>Adobe [!DNL Target]的<br>**[!DNL Commerce]还具有一个内置的产品推荐引擎，该引擎具有强大的功能，如类别亲和度。 这可用于交叉销售或追加销售。使用Adobe Journey Optimizer的<br>**[!DNL Commerce]**：<br>使用[!DNL Target]或[!DNL Commerce]确定要推荐的产品，然后通过Adobe Journey Optimizer交付。 |

### 个性化的网站体验

| 用例 | 解决方案 |
|---|---|
| **个性化网站内容** — 根据购物者操作（如产品浏览和类别亲和度）个性化网站横幅和其他页面内容。 根据A/B测试的结果或业务目标部署最适合的内容。 | **仅Adobe [!DNL Commerce]**：<br>部署特定于区段的[动态内容块](https://experienceleague.adobe.com/en/docs/commerce-admin/content-design/elements/dynamic-blocks/dynamic-blocks)。带有Real-Time CDP的<br>**[!DNL Commerce]**：<br>使用[Audience Activation](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/audience-activation)部署特定于受众的动态内容块，这些内容块响应实时操作和统一的客户配置文件数据，同时集中管理Real-Time CDP中的配置文件和受众。使用[!DNL Target]**&#x200B;的<br>**[!DNL Commerce]：<br>在Adobe [!DNL Target]中使用Adobe [!DNL Commerce]数据对网站体验的每个部分进行个性化，包括内容、导航项、完整页面布局等。 A/B测试内容，为每个客户自动选择和部署入选内容。使用AEM Assets **：<br>在Adobe Experience Manager Assets中存储您的所有内容。 <br>**[!DNL Commerce]从Adobe Commerce中以本机方式访问该内容。 使用创作AI创建内容变体以针对不同的区段或受众进行个性化。 |
| **基于行为的个性化现场优惠** — 基于购物者操作（如产品浏览和类别亲和度）对促销活动进行个性化设置。 根据A/B测试的结果或业务目标部署下一个最佳选件。 | **仅Adobe [!DNL Commerce]**：<br>部署特定于区段的目录和[购物车价格规则](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart)。带有Real-Time CDP的&#x200B;<br>**Adobe [!DNL Commerce]**：<br>使用[Audience Activation](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/audience-activation)部署特定于受众的选件，同时集中管理Real-Time CDP中的用户档案/受众。带有&#x200B;[!DNL Target]**的<br>** Commerce：使用Offer Decisioning确定要部署的选件、A/B测试或设置业务目标以指导Adobe Commerce中部署的选件。 |

### 分析和见解

| 用例 | 解决方案 |
|---|---|
| **按渠道划分的客户行为** — 了解客户参与每个渠道（Web、现场、应用程序等）的细微差别以影响每个渠道的营销策略；了解购物者漏斗和客户体验中的弱点。 | **仅Adobe [!DNL Commerce]**：<br>[Adobe [!DNL Commerce] Intelligence](https://experienceleague.adobe.com/en/docs/commerce-business-intelligence/mbi/getting-started)在数字[!DNL Commerce]渠道上提供丰富的分析，但不提供跨渠道或更广泛的客户历程部分。具有Customer Journey Analytics的&#x200B;<br>**Adobe [!DNL Commerce]**：<br>[!DNL Commerce]数据馈送数据仪表板，可获取有关客户体验所有阶段（跨渠道）的完整丰富详细信息。 了解每个接触点和更广泛的漏斗，以识别客户历程中可能会流失的客户弱点。 |
| **购买趋势** — 了解特定时间范围内的购买行为（例如，购物篮分析、产品分析），以识别趋势、季节性并根据历史购买模式优化营销。 | **仅Adobe [!DNL Commerce]**：<br>[Adobe [!DNL Commerce] Intelligence](https://experienceleague.adobe.com/en/docs/commerce-business-intelligence/mbi/getting-started)在数字[!DNL Commerce]渠道上提供丰富的分析，但不提供跨渠道或更广泛的客户历程部分。具有Customer Journey Analytics的&#x200B;<br>**Adobe [!DNL Commerce]**：<br>[!DNL Commerce]数据馈送数据仪表板，可获取有关客户体验所有阶段（跨渠道）的完整丰富详细信息。 了解每个接触点和更广泛的漏斗，以识别客户历程中可能会流失的客户弱点。 |

## 示例用例

- 了解如何使用Adobe Journey Optimizer来[发送放弃的购物车电子邮件](https://experienceleague.adobe.com/en/docs/commerce/data-connection/use-cases/using-ajo)。
- 了解如何[在Real-Time CDP](https://experienceleague.adobe.com/en/docs/commerce/data-connection/use-cases/create-audience)中创建受众以通知Adobe [!DNL Commerce]中的购物车价格规则。

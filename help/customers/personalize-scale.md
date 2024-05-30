---
title: 大规模创建引人入胜的个性化体验
description: 了解Adobe中的哪些功能 [!DNL Commerce] 可让您为购物者创建个性化体验。
feature: Customers, Storefront, Personalization
exl-id: 9546e1b8-796b-4694-8396-773a2b0e9c12
source-git-commit: 9884d0991cceda7c2917f723467230d3702b2d0f
workflow-type: tm+mt
source-wordcount: '1648'
ht-degree: 0%

---

# 大规模创建引人入胜的个性化体验

Adobe [!DNL Commerce] 为您提供强大的工具包，使每个客户接触点个性化，从而提高购物者参与度、转化率和收入。

在本文中，您将了解：

- 什么是个性化？
- 实现个性化需要哪些数据？
- 如何Adobe [!DNL Commerce] 解锁个性化？
- 可用的个性化用例

## 什么是个性化？

个性化意味着定制每个客户购买体验的各个方面，以满足其独特需求、上下文和偏好。 个性化不仅限于网站上的内容，或推荐最适合的产品，而是涵盖客户历程中的所有接触点，包括：

- **营销活动和通信**  — 通过营销活动和通信提供相关且一致的消息
- **产品发现**  — 在适当的时间向适当的客户展示适当的产品
- **促销和优惠**  — 定位促销和优惠以促使每位客户进行转化
- **内容体验**  — 定制站点内容，以便与每个客户及其历程高度相关

![个性化类型](assets/types-personalization.png){width="700" zoomable="yes"}

虽然这些类型的个性化体验似乎对于一小部分客户来说是可以实现的，但对于每个接触点和渠道中的数千或数百万客户来说，大规模个性化是无法做到的，所有这些实时体验都是不可能的。 在以下部分中，您将了解如何Adobe [!DNL Commerce] Adobe Experience Cloud会有所帮助。

## 实现个性化需要哪些数据？

有效的个性化需要上下文或信号，它们提供有关客户的信息，然后可以使用这些信息修改其体验。 下表提供了各种数据类型以及Adobe的角色 [!DNL Commerce] 在支持收集和激活该数据方面发挥作用。

| 数据类型 | 店面数据（行为事件） | 后台数据（服务器端事件） | 客户个人资料和区段数据 |
|---|---|---|---|
| **定义** | 客户在您的网站上采取的点击或操作。 | 关于生命周期的信息和每个订单的详细信息（过去和当前）。 | 您的购物者是谁，他们符合哪些区段的条件。 |
| **Adobe Commerce捕获的事件** | [pageView](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#pageview)<br>[productPageView](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)<br>[searchRequestSent](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#searchrequestsent)<br>[searchResponseReceived](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#searchresponsereceived)<br>[addToCart](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#addtocart)<br>[openCart](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#opencart)<br>[登录](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#signin)<br>[注销](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#signout)<br>[startCheckout](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#startcheckout)<br>[completeCheckout](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#completecheckout)<br>[createRequisitionList](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#createrequisitionlist)<br>[addToRequisitionList](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#addtorequisitionlist)<br>[removeFromRequisitionList](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#removefromrequisitionlist) | **订单状态**：<br>[orderPlaced](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice#orderplaced)<br>[orderItemsReturnedInitiated](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice#orderitemsreturnedinitiated)<br>[orderItemsShipped](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice#orderitemsshipped)<br>[orderCanceled](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice#ordercancelled)<br>[**订单历史记录**](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/fundamentals/connect-data#send-historical-order-data)：<br>- SKU、名称、价格数量、折扣<br> — 产品类别<br> — 付款金额、类型、币种<br> — 配送方式和金额<br> — 退款ID、金额、币种<br> — 退货原因、条件、解决方法<br> — 地址<br> — 电子邮件 | [**个人资料记录**](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-profilerecord)：（姓名、性别、地址、忠诚度状态、电话号码、电子邮件地址）<br>**帐户状态**：<br>[帐户已创建](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice#accountcreated)<br>[帐户已更新](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice#accountupdated)<br>[帐户已删除](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice#accountdeleted) |

有这么多有钱的第一党人 [!DNL Commerce] 数据，您可以定位每个购物者的体验并使其个性化。 在下一部分中，您将了解如何 [!DNL Commerce] 和Adobe Experience Cloud可帮助您创建个性化体验和可激活的用例。

## 如何Adobe [!DNL Commerce] 是否增强个性化？

Adobe [!DNL Commerce] 通过数据共享，您可以收集上表中的数据类型，并将其与其他Adobe Experience Cloud产品共享，以便形成统一的客户配置文件和受众、个性化的促销活动以及丰富的分析和见解。

![数据如何流向Experience Platform边缘](assets/commerce-edge.png){width="700" zoomable="yes"}

Adobe [!DNL Commerce] 数据共享包括两个关键组件：

1. [数据连接](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/overview)：共享Adobe中的店面、后台和客户档案数据 [!DNL Commerce] 到Adobe Experience Platform edge network以便跨Adobe Experience Cloud应用程序使用，包括：

   - [Adobe [!DNL Real-Time CDP]](https://experienceleague.adobe.com/en/docs/experience-platform/rtcdp/intro/rtcdp-intro/overview)：将跨源(ERP、CRM、POS)的客户数据拼合到统一的用户档案中，并创建基于规则或基于人工智能的区段。
   - [Adobe [!DNL Journey Optimizer]](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/get-started)：启动个性化的全渠道历程，包括电子邮件营销活动、短信、推送通知等。
   - [Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-overview) 和 [Adobe [!DNL Analytics]](https://experienceleague.adobe.com/en/docs/analytics/analyze/admin-overview/analytics-overview)：深入了解客户和业务。
   - [Adobe [!DNL Target]](https://experienceleague.adobe.com/en/docs/target/using/introduction/intro)：测试和优化内容、推荐的产品、优惠、导航等。

1. [[!DNL Audience Activation]](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/audience-activation)：使用 [!DNL Real-Time CDP] 受众可个性化Adobe上的动态内容块、促销活动和相关产品规则 [!DNL Commerce] 站点。

### 开箱即用的个性化：本地Adobe入门 [!DNL Commerce] 功能

Adobe [!DNL Commerce] 通过其原生开箱即用的功能提供强大的个性化功能。 下表介绍了 [!DNL Commerce] 可立即激活的功能以开始您的个性化历程。

| 类别 | 功能 |
|---|---|
| 个性化产品发现 | [[!DNL Live Search]](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/overview)：通过AI支持的搜索，根据购物者的现场行为操作和亲和力个性化并优化搜索结果。<br>[智能类别促销](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/live-search-admin/category-merch)：根据购物者的现场行为操作和亲和力，在类别页面上对AI驱动的产品进行排名。<br>[产品Recommendations](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/product-recommendations/guide-overview)：基于购物者行为、趋势和亲和力的AI支持的产品推荐。<br>[相关产品规则](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/product-relationships/product-related-rules)：定义自定义规则以显示目录中的产品，促进交叉销售和向上销售。 |
| 个性化网站内容 | [动态内容块](https://experienceleague.adobe.com/en/docs/commerce-admin/content-design/elements/dynamic-blocks/dynamic-blocks)：根据Adobe Commerce中的客户区段显示个性化的内容块，例如横幅。 |
| 个性化优惠和促销 | [购物车价格规则](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart)：根据一组条件(包括Adobe中的客户区段)对购物车中的项目应用折扣 [!DNL Commerce]. |
| 洞察和测量 | [Adobe [!DNL Commerce] Intelligence](https://experienceleague.adobe.com/en/docs/commerce-business-intelligence/mbi/getting-started)：了解您的个性化策略如何工作并随着时间改进。 |

## 热门个性化用例

Adobe [!DNL Commerce] 客户正在使用现成功能并将数据共享到Adobe Experience Cloud以用于各种用例。 以下部分突出显示主要用例，并描述如何使用Adobe实施它们 [!DNL Commerce] 仅限或 [!DNL Commerce] 加上Experience Cloud应用程序。

### 个性化的营销活动和通信

| 用例 | 解决方案 |
|---|---|
| **放弃的购物车和浏览**  — 当客户在展示高参与度后放弃购物车或浏览会话时，提供个性化的重新参与电子邮件或通知 | **Adobe [!DNL Commerce] 仅**：<br>[电子邮件提醒](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/communications/email-reminders/email-reminder-rules)<br>**Adobe [!DNL Commerce] 使用Adobe Journey Optimizer**：<br>[!DNL Commerce] 数据会用作全渠道放弃历程的触发器。 根据客户属性、他们放弃的内容、其他购物行为和过去购买，个性化该历程。<br>Commerce与Adobe Journey Optimizer和Real-Time CDP：根据统一的客户配置文件和集中管理的受众定制放弃活动，例如创建高放弃率的受众。 |
| **集中创建受众**  — 根据现场行为、过去的购买、配置文件属性、类别亲和度、忠诚度状态、客户价值等，创建基于规则或由AI支持的受众 | **Adobe [!DNL Commerce] 仅**：<br>收集客户个人资料信息时 [!DNL Commerce] 客户创建帐户。 创建基于规则的 [客户区段](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/segments/customer-segments) 和客户组来对内容和促销进行个性化。<br>**Adobe [!DNL Commerce] 使用Adobe Real-Time CDP**：<br> [统一的用户档案](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/home) 数据源和渠道之间的对应；基于规则的受众或AI支持的受众。 |
| **基于购物者行为的个性化电子邮件/短信优惠**  — 通过基于过去购买和购物者行为的定向电子邮件向客户发送个性化优惠，例如，发送客户已查看或参与的产品或类别的优惠。 | **Adobe [!DNL Commerce] 仅**：<br>导出数据以用于营销自动化解决方案。<br>**Adobe [!DNL Commerce] Adobe Journey Optimizer和Real-Time CDP**：<br>[!DNL Commerce] 数据会用作电子邮件或短信优惠的触发器，并提供要根据进行个性化的信号（购物者行为）。 Real-Time CDP不是必需的，但通常情况下，这些选件和营销活动是围绕受众创建的，将在Real-Time CDP中创建和管理。 |
| **交叉或追加销售兼容的产品/品牌**  — 如果客户购买了一个兼容的产品或品牌，或者表明与另一个产品或品牌高度相关，请发送营销活动（电子邮件/短信）以促进交叉销售转化。 | **Adobe [!DNL Commerce] 仅**：<br>使用Adobe [!DNL Commerce] [产品Recommendations](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/product-recommendations/guide-overview) 推荐网站上的特定产品。 您还可以使用 [相关产品规则](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/product-relationships/product-related-rules) 推荐其他产品。<br>**[!DNL Commerce] 替换为 [!DNL Target]**：<br>Adobe [!DNL Target] 还内置了一个产品推荐引擎，具有强大的功能，例如类别亲和力。 这可用于交叉销售或追加销售。<br>**[!DNL Commerce] 使用Adobe Journey Optimizer**：<br>使用 [!DNL Target] 或 [!DNL Commerce] 确定要推荐的产品，然后通过Adobe Journey Optimizer交付。 |

### 个性化的网站体验

| 用例 | 解决方案 |
|---|---|
| **个性化网站内容**  — 根据购物者操作（如产品浏览和类别亲和度）个性化网站横幅和其他页面内容。 根据A/B测试的结果或业务目标部署最适合的内容。 | **Adobe [!DNL Commerce] 仅**：<br>部署特定于区段 [动态内容块](https://experienceleague.adobe.com/en/docs/commerce-admin/content-design/elements/dynamic-blocks/dynamic-blocks).<br>**[!DNL Commerce] 使用Real-Time CDP **：<br>使用 [Audience Activation](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/audience-activation) 用于部署特定于受众的动态内容块，这些内容块对实时操作和统一的客户个人资料数据做出响应，同时在Real-Time CDP中集中管理个人资料和受众。<br>**[!DNL Commerce] 替换为[!DNL Target]**：<br>使用Adobe将网站体验的每个部分个性化，包括内容、导航项目、完整页面布局等 [!DNL Commerce] Adobe中的数据 [!DNL Target]. A/B测试内容，为每个客户自动选择和部署入选内容。<br>**[!DNL Commerce] 使用AEM Assets **：<br>将您的所有内容存储在Adobe Experience Manager Assets中。 从Adobe Commerce中以本机方式访问该内容。 使用GenAI创建内容变体，为不同的区段或受众进行个性化。 |
| **基于行为的个性化现场服务**  — 根据购物者操作（如产品浏览和类别亲和度）个性化促销活动。 根据A/B测试的结果或业务目标部署下一个最佳选件。 | **Adobe [!DNL Commerce] 仅**：<br>部署特定于区段的目录和 [购物车价格规则](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart).<br>**Adobe [!DNL Commerce] 使用Real-Time CDP**：<br>使用 [Audience Activation](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/audience-activation) 以部署特定于受众的选件，同时在Real-Time CDP中集中管理用户档案/受众。<br>**Commerce与[!DNL Target]**：使用offer decisioning确定要部署的选件、A/B测试或设置业务目标以指导Adobe Commerce中部署的选件。 |

### 分析和见解

| 用例 | 解决方案 |
|---|---|
| **按渠道划分的客户行为**  — 了解客户参与每个渠道（Web、现场、应用程序等）的细微差别以影响每个渠道的营销策略；了解购物者漏斗以及客户体验中的弱点。 | **Adobe [!DNL Commerce] 仅**：<br>[Adobe [!DNL Commerce] Intelligence](https://experienceleague.adobe.com/en/docs/commerce-business-intelligence/mbi/getting-started) 提供对数字化的丰富分析 [!DNL Commerce] 渠道，但不跨渠道或客户历程的更广泛部分。<br>**Adobe [!DNL Commerce] 带有Customer Journey Analytics**：<br>[!DNL Commerce] 数据馈送数据仪表板，以全面详细了解客户体验的所有阶段（跨渠道）。 了解每个接触点和更广泛的漏斗，以识别客户历程中可能会流失的客户弱点。 |
| **购买趋势**  — 了解特定时间范围内的购买行为（例如，购物篮分析、产品分析），以识别趋势、季节性并根据历史购买模式优化营销。 | **Adobe [!DNL Commerce] 仅**：<br>[Adobe [!DNL Commerce] Intelligence](https://experienceleague.adobe.com/en/docs/commerce-business-intelligence/mbi/getting-started) 提供对数字化的丰富分析 [!DNL Commerce] 渠道，但不跨渠道或客户历程的更广泛部分。<br>**Adobe [!DNL Commerce] 带有Customer Journey Analytics**：<br>[!DNL Commerce] 数据馈送数据仪表板，以全面详细了解客户体验的所有阶段（跨渠道）。 了解每个接触点和更广泛的漏斗，以识别客户历程中可能会流失的客户弱点。 |

## 示例用例

- 了解如何使用Adobe Journey Optimizer来 [发送已放弃的购物车电子邮件](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/use-cases/using-ajo).
- 了解如何 [在Real-Time CDP中创建受众](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/use-cases/create-audience) 在Adobe中通知购物车价格规则 [!DNL Commerce].

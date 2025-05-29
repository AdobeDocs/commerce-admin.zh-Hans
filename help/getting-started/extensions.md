---
title: Adobe中的扩展
description: 查看由Adobe发布的Adobe Commerce和Magento Open Source扩展信息。
exl-id: 86338edc-c32a-41c8-9594-6aec26f53ac6
feature: Extensions
badgePaas: label="仅限PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="仅适用于云项目(Adobe管理的PaaS基础架构)和内部部署项目上的Adobe Commerce 。"
source-git-commit: 77e7eb00e9f8d5af6361059c287707993180c4c4
workflow-type: tm+mt
source-wordcount: '1357'
ht-degree: 0%

---

# Adobe中的扩展

本主题介绍由Adobe发布的Adobe Commerce和Magento Open Source的PHP扩展信息。

扩展为管理员和店面添加了功能、功能、服务和集成。 其中一些扩展是通过Magento Open Source社区贡献开发的。 默认情况下，会安装某些扩展，而其他扩展则需要单独安装。

+++了解有关扩展Adobe Commerce的更多信息

Adobe提供了两种主要方法来扩展或自定义您的Adobe Commerce项目：

- 进程内可扩展性：使用在Adobe Commerce应用程序进程（如PHP扩展）中运行的自定义代码和扩展。 这种传统方法允许深度集成，但在升级期间需要仔细管理。

- 进程外可扩展性：使用独立于核心软件的自定义代码和应用程序。 此现代方法有助于通过以下方式降低总拥有成本：

   - 由于扩展与核心分离，因此简化了升级
   - 使开发人员能够更好地控制实施时间和方法
   - 实现扩展组件的独立扩展和维护

Adobe Commerce提供了策略和工具来支持这两种类型的可扩展性。 要了解更多信息，请参阅[Adobe Commerce可扩展性](https://developer.adobe.com/commerce/extensibility/)。

+++

## 默认安装的Adobe扩展

Adobe Commerce附带以下Adobe扩展，并随Adobe Commerce应用程序自动安装。 某些扩展需要在管理员中进行进一步配置或启用，如扩展描述中所述。

### [!DNL Inventory Management]

[!DNL Commerce] [[!DNL Inventory Management]](../inventory-management/introduction.md)通过并发结帐保护和装运匹配算法，在一个或多个位置和销售渠道中提供增强的库存和装运管理。 跟踪库存数量，向客户提供准确的可销售库存量，并根据建议或人工选择发运以控制整个库存。 按源和产品全局配置管理设置。

>[!NOTE]
>
>此扩展是通过社区工程计划作为[[!DNL Inventory Management]](https://github.com/magento/inventory)（以前为MSI）项目的一部分开发的。

[!DNL Inventory Management]安装，默认启用所有功能。 无需执行其他步骤即可启用这些清单功能。 有关[!DNL Inventory Management]功能的详细信息，请参阅[[!DNL Inventory Management] 用户指南](../inventory-management/guide-overview.md)。

### Braintree

PayPal和Gene Commerce共同为Commerce 2.4.x商店开发了官方的Braintree扩展。 这些更新包括了PayLater选项，改善了旨在促进转化的结账体验，这些选项可在购物和结账期间自动向消费者显示相关的PayLater消息和按钮。

此扩展默认已安装，但需要为你的存储启用[Braintree帐户](https://www.braintreepayments.com/)以及管理员中的配置。 要确定使用Braintree处理交易时适用的费用，请检查[Braintree定价](https://www.braintreepayments.com/braintree-pricing)。

有关管理员中Braintree配置的信息，请参阅&#x200B;_销售和购买体验指南_&#x200B;中的[Braintree](../stores-purchase/braintree.md)主题。

### Google reCAPTCHA

Google reCAPTCHA与标准CAPTCHA相比，为店面和管理员UI提供了更高级别的安全性，并让您能够：

- 验证客户何时创建帐户、检索密码、登录到其帐户或联系您的公司。
- 增强管理员用户登录时的安全性。

它可以减少输入验证码时可能的用户错误，并鼓励在结账期间不添加障碍的购物车转换。 [使用不可见或交互式检查启用并配置reCAPTCHA](../systems/security-google-recaptcha.md)，以增强对[!DNL Commerce]管理员和店面的安全访问。

### 双重身份验证

[!DNL Commerce]管理员提供对您的商店、订单和客户数据的所有访问权限。 [双重身份验证](../systems/security-two-factor-authentication.md) （2FA或TFA）要求从所有设备访问[!DNL Commerce]管理员时，除了标准登录名和密码之外，还需要其他身份验证，从而提高安全性。 该扩展支持多个身份验证器，包括Google Authenticator、Authy、[!DNL Duo]和U2F键。 此身份验证仅适用于管理员用户。 它不适用于店面客户。

默认情况下，将启用这些功能。 每个Admin用户必须安装和配置一个受支持的身份验证器。

>[!NOTE]
>
>为管理员启用了Adobe Identity Management Services (IMS)身份验证的Adobe Commerce存储已禁用本机Commerce 2FA。 使用其Adobe凭据登录到管理员的用户不需要对许多管理员任务重新进行身份验证。 当管理员用户登录到其当前会话时，身份验证由Adobe IMS处理。 请参阅[Adobe Identity Management Service (IMS)集成概述](./adobe-ims-integration-overview.md)。

## 需要安装的Adobe扩展

Adobe提供了必须使用编辑器单独安装的其他扩展。 这些扩展可通过不同的渠道使用：

- 存储库访问(repo.magento.com)

  要安装以下扩展，需要设置帐户和凭据。 请联系您的Adobe客户代表寻求帮助。

   - [Adobe Commerce B2B](#adobe-commerce-b2b)
   - [适用于Commerce的AEM Assets集成](#assets-integration-for-commerce)

- Adobe Commerce市场

  以下Adobe扩展可在[marketplace.magento.com](https://marketplace.magento.com)中公开访问。 这些扩展无需额外付费。

   - [实时搜索](#live-search)
   - [产品推荐](#product-recommendations)
   - [目录服务](#catalog-service)
   - [支付服务](#payment-services)

### [!DNL Adobe Commerce B2B]

仅![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce，需要单独的许可证。

[!DNL Adobe Commerce B2B]是一个集成的扩展，可将标准Commerce存储区转换为全面的企业对企业平台。 它使公司能够在统一的公司帐户下管理具有多个购买者、自定义角色和购买权限的复杂组织结构。 关键功能包括特定于公司的目录和定价、可协商的报价、采购订单管理、申购单和快速订购功能。 该解决方案在单个实例上同时支持B2B和B2C模型，使其能够灵活地满足各种业务需求。 该扩展需要单独的许可证并与Adobe Commerce的核心功能无缝集成，以提供完整的B2B电子商务解决方案。

要进行配置，请联系您的Adobe客户代表。 有关实施详细信息和配置步骤，请参阅[[!DNL B2B for Adobe Commerce] 用户指南](https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html)。

### [!DNL AEM Assets Integration for Commerce]

仅![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce还需要Adobe Experience Manager (AEM) Assets和AEM Dynamic Media的许可证。

[!DNL AEM Assets Integration for Commerce]将Adobe Commerce与Adobe Experience Manager的数字资产管理(DAM)系统连接起来，以集中控制所有数字资产。 此集成支持跨商业存储场的自动资产同步、实时更新和高效的内容重用。 通过将AEM强大的资产管理功能与Commerce相结合，企业可以从简化的工作流、一致的品牌体验以及通过基于云的基础架构优化的媒体投放中受益。

要进行配置，请联系您的Adobe客户代表。 有关实施详细信息和配置步骤，请参阅[[!DNL Assets Integration] 用户指南](../content-design/aem-assets-integration.md)。

### [!DNL Live Search]

仅![Adobe Commerce](../assets/adobe-logo.svg)Adobe Commerce

Live Search是Adobe Commerce独有的功能，它为AI支持的搜索解决方案提供了实时“随类型搜索”功能。 它可以在购物者键入内容时，通过产品缩览图提供快速的相关结果，同时还可以根据购物行为自动调整过滤器的智能分面。 该解决方案包括用于产品提升和掩藏、同义词管理和搜索分析的推销功能。 随Adobe Commerce一起提供，[!DNL Live Search]免费使用更复杂、基于SaaS的搜索体验来替换默认搜索功能。 它需要最少的配置才能开始。

有关实施详细信息和技术要求，请参阅[实时搜索用户指南](https://experienceleague.adobe.com/docs/commerce/live-search/overview.html)。

### [!DNL Product Recommendations]

仅![Adobe Commerce](../assets/adobe-logo.svg)Adobe Commerce

[!DNL Product Recommendations]是Adobe Commerce独有的功能，由Adobe Sensei AI技术提供支持，可在整个客户购物历程中提供个性化的产品建议。 该解决方案可实时分析购物者行为和产品关系，以自动生成相关推荐，无需手动促销规则。 这种人工智能驱动的方法有助于提高转化率和收入潜力，同时为购物者创造更吸引人的产品发现体验。

有关实施详细信息和最佳实践，请参阅[[!DNL Product Recommendations] 用户指南](https://experienceleague.adobe.com/docs/commerce/product-recommendations/overview.html)。

### [!DNL Catalog Service]

[!BADGE 支持]{type=Informative tooltip="支持"}Adobe Commerce和Magento Open Source安装

[!DNL Catalog Service]是Adobe Commerce和Magento Open Source的高性能解决方案，它通过GraphQL端点提供对目录数据的优化访问。 它维护一个单独的同步数据库，用于存放产品详细信息和相关信息，从而绕过直接的应用程序通信来加快页面加载时间。 此服务对于产品详细信息页面、类别列表和搜索结果页面尤其有用，因此非常适合传统和Headless商务实施。

有关设置说明和技术详细信息，请参阅[[!DNL Catalog Service] 用户指南](https://experienceleague.adobe.com/docs/commerce/catalog-service/guide-overview.html)。

>[!NOTE]
>
>启用实时搜索或产品推荐后，将自动安装目录服务。 不需要手动安装。

### [!DNL Payment Services]

[!BADGE 支持]{type=Informative tooltip="支持"}Adobe Commerce和Magento Open Source安装

[!DNL Payment Services]是适用于Adobe Commerce和Magento Open Source商店的全包支付解决方案，可提供全面的支付处理功能。 该服务将安全支付网关功能与内置的欺诈保护功能集成，同时提供多种支付选项，包括信用卡/借记卡、PayPal、Venmo (US)和PayLater计划。 它通过Commerce管理界面提供统一的交易报告和订单管理，使得商家能够轻松地在一个地方跟踪支付、管理现金流和对账财务数据。

有关详细配置步骤和付款选项，请参阅[[!DNL Payment Services] 用户指南](https://experienceleague.adobe.com/en/docs/commerce/payment-services/overview)。

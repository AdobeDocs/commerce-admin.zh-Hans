---
title: 片段
description: 重复使用的注释和可视元素，以注释应用于特定版本的功能或页面
source-git-commit: e82b979ee2c5f51caba6a2aa416c5f20dbce110a
workflow-type: tm+mt
source-wordcount: '650'
ht-degree: 0%

---

# 片段

## 仅供查看的功能 {#ee-feature}

<table style="border:1px solid red">
<tr><td><img alt="Adobe Commerce功能" src="../assets/adobe-logo.svg" width="20" height="20" /> 仅在Adobe Commerce中独占的功能（<a href="https://experienceleague.adobe.com/docs/commerce-admin/user-guides/home.html#product-editions">了解更多</a>）</td></tr>
</table>

## 仅B2B功能 {#b2b-feature}

<table style="border:1px solid green">
<tr><td><img alt="Adobe Commerce B2B功能" src="../assets/b2b.svg" width="20" height="20" /> 仅对<a href="https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html?lang=en">Adobe Commerce B2B</a>提供独家功能</td></tr>
</table>

## 仅限CE的功能 {#ce-feature}

<table style="border:1px solid orange">
<tr><td><img alt="Magento Open Source功能" src="../assets/open-source.svg" width="20" height="20" /> Magento Open Source需要替代方法（<a href="https://experienceleague.adobe.com/docs/commerce-admin/user-guides/home.html#product-editions">了解更多</a>）</td></tr>
</table>

## IMS管理员身份验证说明 {#ims-admin-note}

>[!NOTE]
>
>拥有Adobe ID并希望简化登录Adobe Commerce和Adobe业务产品的Adobe Commerce商家可以将Commerce管理员身份验证与Adobe IMS身份验证工作流集成。 为您的Commerce商店启用此集成后，每个管理员用户必须使用其Adobe凭据(而不是其Commerce帐户凭据)登录。 请参阅[将Adobe Commerce与Adobe IMS集成概述](/help/getting-started/adobe-ims-integration-overview.md)。

## GTag API注释 {#gtag-api-note}

>[!NOTE]
>
>从2.4.5版本开始，更新了Google服务集成以支持使用GTag API。 GTag是一种用于与Google网页功能集成的统一机制，它支持通过Google服务跟踪和管理内容的最新功能和机会。 有关详细信息，请参阅[Google Analytics开发人员文档](https://developers.google.com/analytics/devguides/collection/gtagjs)。

## URL重写自动跳过注释 {#url-rewrite-skip}

>[!NOTE]
>
>如果启用了自动重定向，并且保存了类别，则所有产品和类别重写都将实时生成，并默认存储在重写表中。 对于具有许多已分配产品的类别，此过程可能会导致严重的性能问题。 解决方案是更改此默认设置，并跳过为类别保存生成产品的category/products URL重写。 在这种情况下，将仅为规范的产品URL生成产品重写。 有关详细信息，请参阅[自动产品重定向](/help/merchandising-promotions/url-redirect-product-automatic.md)。

## URL重写参数注释 {#url-rewrite-params}

>[!IMPORTANT]
>
>在重定向过程中，出于安全原因，将删除URL中指定的所有GET参数。

## 新的价格规则 {#new-price-rule}

>[!NOTE]
>
>价格规则将自动与其他系统规则一起处理。 处理频率取决于[cron配置](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html)。 创建价格规则时，请为其留出足够的时间以使其进入系统。 如果确定它位于系统中，请测试该规则。

## 配置设置 {#config}

要访问存储配置设置，请从&#x200B;_管理员_&#x200B;侧边栏中选择&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

## UPS API弃用 {#ups-api}

>[!IMPORTANT]
>
>从2024年6月开始，Adobe Commerce商户无法再使用当前的UPS集成进行交易。 这是因为本机Adobe Commerce集成使用的United Parcel Service (UPS) API当前不支持所需的OAuth 2.0安全模型。 要启用集成，请[在UPS开发人员平台](https://developer.ups.com/get-started)上创建应用程序以获取OAuth 2.0所需的凭据。在Commerce UPS配送配置中将新凭据用作`username`和`password`。 若要了解有关安全模型更改的详细信息，请参阅[开发人员门户访问密钥迁移指南_](https://developer.ups.com/oauth-developer-guide)。<br/>
>
>商家应在其存储中[应用质量修补程序更新](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/known-issues-patches-attached/ups-shipping-method-integration-migration-from-soap-to-restful-api.html)，以便从SOAP API迁移到支持OAuth 2.0身份验证协议的RESTful API。


## 可用文档 {#docs-links}

| 文档资源 | 描述 |
|----------------------- | ----------- |
| [Adobe Commerce 2.4管理员用户指南](../landing/home.md) | 面向在管理员中工作的商家的文档和资源。 |
| [Adobe Commerce文档服务](https://experienceleague.adobe.com/docs/commerce/user-guides/home.html) | 支持一系列促销服务的文档，可帮助商家将其业务的关键组件与商店集成。 |
| 云基础架构上的[Commerce指南](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/overview.html) | 在托管的自动托管云平台上部署Adobe Commerce的分步过程。 |
| [Adobe Commerce 2.4操作指南](https://experienceleague.adobe.com/docs/commerce-operations/operational-guides/home.html) | 有关开发、部署和维护云端Adobe Commerce和内部项目概念、流程、工具和最佳实践的系统文档。 |
| [Adobe Commerce 2.4开发人员文档](https://developer.adobe.com/commerce/docs) | 用于自定义Adobe Commerce并与第三方系统集成且侧重于开发人员的文档。 |

{style="table-layout:auto"}

## B2B兼容性 {#b2b-compatibility}

>[!IMPORTANT]
>
>Adobe Commerce B2B版本1.4.2+与PHP 8.2兼容。如果将Commerce实例升级到版本2.4.7+，请确保该实例使用PHP版本8.2来保持与Adobe Commerce B2B版本的兼容性。 此外，B2B 1.4.2+版本不支持[GraphQL Application Server](https://experienceleague.adobe.com/en/docs/commerce-operations/performance-best-practices/concepts/application-server)。

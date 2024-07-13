---
title: 代码片段
description: 重用注释和可视化元素来注释应用于特定版本的功能或页面
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '551'
ht-degree: 0%

---

# 代码片段

## EE专用功能 {#ee-feature}

<table style="border:1px solid red">
<tr><td><img alt="Adobe Commerce功能" src="../assets/adobe-logo.svg" width="20" height="20" /> 仅在Adobe Commerce中独占的功能（<a href="https://experienceleague.adobe.com/docs/commerce-admin/user-guides/home.html#product-editions">了解更多</a>）</td></tr>
</table>

## 仅限B2B的功能 {#b2b-feature}

<table style="border:1px solid green">
<tr><td><img alt="Adobe Commerce B2B功能" src="../assets/b2b.svg" width="20" height="20" /> 仅在<a href="https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html?lang=en">Adobe Commerce B2B</a>中提供了独占功能</td></tr>
</table>

## 仅限CE的功能 {#ce-feature}

<table style="border:1px solid orange">
<tr><td><img alt="Magento Open Source功能" src="../assets/open-source.svg" width="20" height="20" /> Magento Open Source需要替代方法（<a href="https://experienceleague.adobe.com/docs/commerce-admin/user-guides/home.html#product-editions">了解更多</a>）</td></tr>
</table>

## IMS管理员身份验证说明 {#ims-admin-note}

>[!NOTE]
>
>具有Adobe ID并希望简化登录Adobe Commerce和Adobe业务产品的Adobe Commerce商家可以将Commerce管理员身份验证与Adobe IMS身份验证工作流集成。 为您的Commerce商店启用此集成后，每个管理员用户必须使用其Adobe凭据(而不是其Commerce帐户凭据)登录。 请参阅[将Adobe Commerce与Adobe IMS集成概述](/help/getting-started/adobe-ims-integration-overview.md)。

## GTag API注释 {#gtag-api-note}

>[!NOTE]
>
>从2.4.5版本开始，更新了Google服务集成以支持使用GTag API。 GTag是一种用于与Google网页功能集成的统一机制，它支持通过Google服务跟踪和管理内容的最新功能和机会。 有关详细信息，请参阅[Google Analytics开发人员文档](https://developers.google.com/analytics/devguides/collection/gtagjs)。

## URL重写自动跳过注释 {#url-rewrite-skip}

>[!NOTE]
>
>启用自动重定向并保存类别后，所有产品和类别重写都将实时生成，并默认存储在重写表中。 此过程可能会导致分配了许多产品的类别出现严重的性能问题。 解决方案是更改此默认设置并跳过为类别保存生成产品的类别/产品URL重写。 在这种情况下，仅为规范产品URL生成产品重写。 有关详细信息，请参阅[自动产品重定向](/help/merchandising-promotions/url-redirect-product-automatic.md)。

## URL重写参数注释 {#url-rewrite-params}

>[!IMPORTANT]
>
>在重定向过程中，出于安全原因，将删除URL中指定的所有GET参数。

## 新的价格规则 {#new-price-rule}

>[!NOTE]
>
>价格规则将自动与其他系统规则一起处理。 处理频率取决于[cron配置](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html)。 在创建价格规则时，请留出足够的时间使其进入系统。 如果确定它在系统中，则测试规则。

## 配置设置 {#config}

要访问商店配置设置，请从&#x200B;_管理员_&#x200B;侧边栏中选择&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

## 弃用UPS API {#ups-api}

>[!IMPORTANT]
>
>从2024年6月开始，Adobe Commerce商户无法再使用当前的UPS集成进行交易。 这是因为本机Adobe Commerce集成使用的United Parcel Service (UPS) API当前不支持所需的OAuth 2.0安全模型。 要了解有关此更改的更多信息，请参阅&#x200B;[_开发人员门户访问密钥迁移指南_](https://developer.ups.com/oauth-developer-guide)。<br/>
>
>商家应在其存储中[应用质量修补程序更新](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/known-issues-patches-attached/ups-shipping-method-integration-migration-from-soap-to-restful-api.html)，以便从SOAP API迁移到支持OAuth 2.0身份验证协议的RESTful API。


## 可用文档 {#docs-links}

| 文档资源 | 描述 |
|----------------------- | ----------- |
| [Adobe Commerce 2.4商家文档](../landing/home.md) | Adobe Commerce以商家为中心的文档 |
| [Adobe Commerce服务文档](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/home.html) | 支持服务集合的文档，可帮助商家将其业务的关键组件与商店集成。 |
| 云基础架构上的[Commerce指南](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/overview.html) | 在托管的自动托管云平台上部署Adobe Commerce的分步过程。 |
| [Adobe Commerce 2.4操作指南](https://experienceleague.adobe.com/docs/commerce-operations/operational-guides/home.html) | 有关开发、部署和维护Adobe Commerce项目的概念、流程、工具和最佳实践的系统文档。 |
| [Adobe Commerce 2.4开发人员文档](https://developer.adobe.com/commerce/docs) | 以开发人员为中心的文档，用于自定义Adobe Commerce并与第三方系统集成 |

{style="table-layout:auto"}

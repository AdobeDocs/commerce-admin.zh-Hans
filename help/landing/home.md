---
title: Adobe Commerce管理员用户指南
description: 浏览 Adobe Commerce 产品文档
seo-title: Services for Adobe Commerce
seo-description: Documentation and resources for Adobe Commerce and Magento Open Source users working in the Admin.
breadcrumb-title: 管理员用户指南
exl-id: e30f769f-9140-4370-943e-75007b39ebc0
source-git-commit: d5120cf04de400ce875309f6eb71596430e27401
workflow-type: tm+mt
source-wordcount: '1199'
ht-degree: 0%

---

# &#x200B;<!-- use banner as heading -->![管理员文档](./assets/banner-user-home.png) {#documentation}

欢迎来到世界领先的下一代数字商务平台。 Adobe Commerce为在线商户提供了无与伦比的灵活性，让他们可以控制在线商店的外观、内容和功能。 管理员具有强大的营销、搜索引擎优化和产品管理工具，使您能够创建针对独特业务需求定制的站点。

《管理员用户指南》中的信息旨在容纳使用Adobe Commerce Admin或Magento Open Source代码库的业务用户。 Adobe Commerce或扩展功能集独有的特性和功能均带有符号。

## Adobe Commerce {#product-editions}

Adobe Commerce是一个敏捷的B2B和B2C商业平台，使商家和品牌能够通过以客户为中心的数字商业体验在线和实体空间增加收入。 它是中型企业组织的首选，因为它提供了从内部部署到具有保证SLA的受管云的最灵活的部署模型。 Adobe Commerce实现了API优先的集成和完全可自定义的扩展，以及最丰富的企业级商务体验功能（从营销到销售和履行）。 Adobe Commerce基于开源代码构建，具有其他商务平台无法比拟的灵活性和可扩展性。

有关Adobe Commerce中包含的高级功能的列表，请参阅&#x200B;_发行信息_&#x200B;中的[Commerce功能](https://experienceleague.adobe.com/docs/commerce-operations/release/features.html?lang=en)。

## Magento Open Source代码库

Magento Open Source是Adobe正式提供的代码库，用于确保与Adobe Commerce过渡的兼容性。 此代码库是Adobe增强个人开发人员能力并培养渴望快速发展的小型企业的计划的一部分。

## 管理员用户指南

<table>
<tr>
   <td valign="top" width="60px">
       <img alt="快速入门" src="./assets/icon-lightbulb.svg" width="40" height="40" /></td>
   <td valign="top">
   <a href="https://experienceleague.adobe.com/docs/commerce-admin/start/guide-overview.html"><strong>快速入门</strong></a>
    <div>
    <em>大多数商家在第一次学习时向管理员提出的“原因、地点和方式”问题，以及资源和参考信息。 本指南是更高级主题的跳板。</em>
    <br> </div>
  </td>
  </tr>
<tr>
  <td valign="top">
      <img alt="Adobe Commerce B2B" src="./assets/icon-building.svg" width="40" height="40"/></td>
   <td valign="top"><a href="https://experienceleague.adobe.com/docs/commerce-admin/b2b/guide-overview.html"><strong>Adobe Commerce B2B</strong></a> [!BADGE PaaS only]{type=Informational url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="仅适用于云项目上的Adobe Commerce (Adobe管理的PaaS基础结构)和内部部署项目。"}
    <div><em>此功能集旨在满足销售商（商家）的需求，这些商家的客户主要是公司 — 可能具有复杂的组织结构以及拥有各种角色和购买权限级别的多个员工。</em>
    <br></div>
  </td>
</tr>
<tr>
  <td valign="top">
    <img alt="目录管理" src="./assets/icon-shop.svg" width="40" height="40"/></td>
   <td valign="top"><a href="https://experienceleague.adobe.com/docs/commerce-admin/catalog/guide-overview.html"><strong>目录管理</strong></a>
    <div><em>创建和管理商店时最重要的领域之一是产品目录和类别。 管理员为商店和产品目录的初始设置提供了许多工具。</em>
    <br></div>
  </td>
    </tr>
<tr>
    <td valign="top">
       <img alt="Inventory management" src="./assets/icon-transfer.svg" width="40" height="40"/></td>
   <td valign="top"><a href="https://experienceleague.adobe.com/docs/commerce-admin/inventory/guide-overview.html"> <strong>[!DNL Inventory Management]</strong></a>
    <div><em>通过[!DNL Inventory Management]功能，只有一家商店的商家可以前往多个仓库、商店、取货地点、托运人等。 使用这些功能可以维护销售数量并处理发运以完成订单。</em></div>
  </td>
</tr>
<tr>
    <td valign="top">
       <img alt="促销和促销" src="./assets/icon-labels.svg" width="40" height="40"/></td>
   <td valign="top"><a href="https://experienceleague.adobe.com/docs/commerce-admin/marketing/guide-overview.html"> <strong>促销活动</strong></a>
    <div><em>创建有针对性的促销活动和客户参与机会，将购物者转化为购买者。 通过支持购买后活动并向回头客户提供特别折扣来管理客户关系。 了解支持您的SEO计划的最佳实践和技术。</em></div>
  </td>
</tr>
<tr>
    <td valign="top">
       <img alt="内容和设计" src="./assets/icon-color-wheel.svg" width="40" height="40"/></td>
   <td valign="top"><a href="https://experienceleague.adobe.com/docs/commerce-admin/content-design/guide-overview.html"> <strong>内容和设计</strong></a>
    <div><em>您的内容定义客户在访问您的商店时看到的页面和元素。 为您的页面定义基本元素，如文本和图像，以及更高级的元素，这些元素提供交互和动态内容以增强购物体验。</em></div>
  </td>
</tr>
<tr>
    <td valign="top">
       <img alt="页面生成器" src="./assets/icon-web-pages.svg" width="40" height="40"/></td>
   <td valign="top"><a href="https://experienceleague.adobe.com/docs/commerce-admin/page-builder/guide-overview.html"> <strong>[!DNL Page Builder]</strong></a> [!BADGE PaaS only]{type=Informational url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="仅适用于云项目(Adobe管理的PaaS基础结构)和本地项目上的Adobe Commerce。"}
    <div><em>[!DNL Page Builder]使您可以轻松创建具有自定义版面的内容丰富的页面。 这些功能旨在提高质量，并减少生成自定义页面的时间和费用。</em></div>
  </td>
</tr>
<tr>
    <td valign="top">
       <img alt="客户管理" src="./assets/icon-demographic.svg" width="40" height="40"/></td>
   <td valign="top"><a href="https://experienceleague.adobe.com/docs/commerce-admin/customers/guide-overview.html"> <strong>客户管理</strong></a>
    <div><em>当您继续维护和扩展商店时，请在“管理员”中管理客户帐户和客户组。</em></div>
  </td>
</tr>
<tr>
    <td valign="top">
       <img alt="商店和购买体验" src="./assets/icon-shopping-cart.svg" width="40" height="40"/></td>
   <td valign="top"><a href="https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/guide-overview.html"> <strong>存储和购买体验</strong></a>
    <div><em>购物车位于购买路径的末尾，购买和放弃的交集。 设置购买点以及可将购物车项目转换为已完成订单的支持功能。</em></div>
  </td>
</tr>
<tr>
    <td valign="top">
       <img alt="管理系统" src="./assets/icon-globe-grid.svg" width="40" height="40"/></td>
   <td valign="top"><a href="https://experienceleague.adobe.com/docs/commerce-admin/systems/guide-overview.html"> <strong>管理系统</strong></a>
    <div><em>管理员提供了多种工具来管理您的系统和优化其性能。 本指南包含有关管理员用户帐户管理以及关联的角色和权限的信息。</em></div>
  </td>
</tr>
<tr>
    <td valign="top">
       <img alt="配置引用" src="./assets/icon-settings.svg" width="40" height="40"/></td>
   <td valign="top"><a href="https://experienceleague.adobe.com/docs/commerce-admin/config/guide-overview.html"> <strong>配置引用</strong></a>
    <div><em>一个方便快捷的参考，为管理员中的每个配置设置提供字段说明。</em></div>
  </td>
</tr>
</table>

## 《管理员用户指南》的新增功能

>[!TIP]
>
>您还可以查看[Commerce Services文档的新增功能](https://experienceleague.adobe.com/docs/commerce/user-guides/home.html#what%E2%80%99s-new)和[操作指南的新增功能](https://experienceleague.adobe.com/docs/commerce-operations/operational-guides/home.html#what%E2%80%99s-new)。

| 描述 | 类型 | 日期 |
| ----------- | ---- | ---- |
| **1.4.0 B2B版本** - Adobe Commerce B2B发行说明介绍了[1.4.0版本](../b2b/release-notes.md#b2b-v140)的更改和添加内容。 | 更新 | 06/13/23 |
| **1.4.0 B2B版本** - _Adobe Commerce B2B指南_&#x200B;中现在包含购买者[&#128279;](../b2b/sales-rep-initiates-quote.md)主题的Initiate报价。 它描述了卖方如何为特定采购员创建报价以开始洽谈流程。 | 新建 | 06/13/23 |
| **1.4.0 B2B版本** - [协商报价](../b2b/quote-price-negotiation.md)、[可协商报价](../b2b/quotes.md)和[启用B2B功能](../b2b/enable-basic-features.md)主题已更新，以反映卖方发起的报价和默认功能的更改。 | 更新 | 06/13/23 |
| **2.2.0 Adobe IMS集成版本** - _快速入门指南_&#x200B;现已包含[禁用Commerce与Adobe ID的管理员集成](../getting-started/adobe-ims-disable.md)主题。 它描述了用于禁用Adobe Commerce管理员与Adobe IMS集成的可选过程。 | 新建 | 06/13/23 |
| **2.2.0 Adobe IMS集成版本** - [Adobe Identity Management服务(IMS)集成概述](../getting-started/adobe-ims-integration-overview.md)和[配置Commerce与Adobe ID的管理员集成](../getting-started/adobe-ims-config.md)主题中的更改以反映更新的功能。 | 更新 | 06/13/23 |
| **[!DNL Audience Activation]** - [[!DNL Audience Activation]](../customers/audience-activation.md)主题中包含新增和更新及改进的信息，以反映[!DNL Experience Platform Connector]配置UI以及如何将headless Commerce实例与购物车价格规则和动态块结合使用。 | 更新 | 06/13/23 |
| **UPS API弃用** — 更新了[United Parcel Service (UPS)](../stores-purchase/ups.md)主题和[交付方法](../configuration-reference/sales/delivery-methods.md#ups)配置参考页面，以反映临时弃用UPS API以生成新的API密钥。 | 更新 | 06/08/23 |
| **2.4.6版本** — 更新了[产品列表](../catalog/products-list.md)和[管理员配置引用](../configuration-reference/advanced/admin.md)主题，以包含有关产品显示限制的信息，这些信息可用于提高大型目录的性能。 | 更新 | 03/14/23 |
| **2.4.6版本** — 更新了[创建和删除客户区段](../customers/customer-segment-create.md)和[客户配置引用](../configuration-reference/customers/customer-configuration.md)主题，以包含有关区段实时验证的信息。 | 更新 | 03/14/23 |
| **2.4.6版本** — 更新了[Braintree](../stores-purchase/braintree.md)和[Braintree配置引用](../configuration-reference/sales/braintree.md)主题，以反映捆绑的Braintree集成支持的更新和新的付款选项。 | 更新 | 03/14/23 |
| **2.4.6版本** — 已更新[货币配置](../stores-purchase/currency-configuration.md)和[货币设置配置](../configuration-reference/general/currency-setup.md)主题以包含新的[!DNL Fixer API] (APILayer)选项。 | 更新 | 03/14/23 |
| **2.4.6版本** — 更新了[配置电子邮件通信](../systems/email-communications.md)和[系统配置引用](../configuration-reference/advanced/system.md#uicontrol-mail-sending-settings)主题以包含用于电子邮件通信的新SMTP选项。 | 更新 | 03/14/23 |
| **2.4.6版本** — 使用最新捆绑的扩展版本(v1.2.6)中包含的描述性修复列表更新了[Inventory management发行说明](../inventory-management/release-notes.md)。 | 更新 | 03/14/23 |
| **2.4.6版本** — 使用最新扩展版本(v1.3.5)中包含的描述性修复列表更新了[B2B发行说明](../b2b/release-notes.md)。 | 更新 | 03/14/23 |
| **新主题** — 已将[受众激活](../getting-started/commerce-account-transfer.md)主题添加到&#x200B;_客户管理指南_&#x200B;中，该指南提供了有关在Adobe Commerce中激活Real-Time CDP受众的详细信息。 | 新建 | 03/13/23 |
| **新主题** — 已将[转移Commerce帐户](../getting-started/commerce-account-transfer.md)主题添加到&#x200B;_入门指南_。 | 新建 | 02/27/23 |

{style="table-layout:auto"}

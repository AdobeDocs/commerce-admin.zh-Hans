---
title: ' [!DNL Adobe Commerce B2B]简介'
description: 了解如何使用集成的 B2B 功能来满足公司客户的需求。
exl-id: fc7e8147-5fd5-4e4b-b16e-0b0d54c415da
feature: B2B
source-git-commit: 8e4e070f41f7d3bf872e81c9805e7c24779b812d
workflow-type: tm+mt
source-wordcount: '813'
ht-degree: 2%

---

# [!DNL Adobe Commerce B2B]简介

与标准的B2B(Business to Business)模式不同，集成B2B(Business to Business)功能旨在满足拥有企业客户的销售商(Adobe Commerce商家)的需求。 它可容纳组织结构复杂的公司和具有不同角色和购买权限级别的多个用户。 典型的B2B客户可能是零售店的经理，也可能是代表公司进行购买的买家。 在这两种情况下，交易都发生在您的企业与他们的企业之间。 您也可以将产品直接销售给消费者。 [!DNL Adobe Commerce B2B]是一个支持B2B和B2C模型的集成解决方案。

在您的Adobe Commerce商店中安装[B2B扩展](install.md)并启用[B2B扩展](enable-basic-features.md)后，即可通过特定于客户的目录和定价以及有针对性的内容和促销活动，实现个性化的购买体验。

## 公司帐户

公司帐户组件是B2B中的关键实体，所有其他功能在某种程度上都依赖于它。 它允许将属于单个公司的多个购买者加入单个公司帐户（或公司帐户）。 公司管理员可以构建公司结构（部门、子部门和用户），以反映公司的运营模式，并为公司成员提供不同的用户角色和权限。 此结构允许公司管理员控制公司帐户的用户活动：订购、报价、购买、访问公司信用信息或个人资料等。

通过管理员，Commerce站点管理员可以配置公司在网站上的操作方式。 配置确定可供公司用户使用的B2B功能，包括付款方法、定价级别、使用报价议价的能力、创建申请列表的能力等。

有关详细信息，请参阅[公司帐户](account-companies.md)。

>[!NOTE]
>
>启用后，您的商店可以为公司提供&#x200B;_按帐户付款_&#x200B;的选项，这意味着使用公司信用额度进行购买。 作为商人，您可以为公司帐户分配信用，管理公司的信用设置，以及信用报销。

## 公司管理

[!BADGE 1.5.0-beta]{type=Informative url="/help/b2b/release-notes.md" tooltip="仅适用于Beta计划参与者"}

公司管理可帮助商家管理员简化具有复杂运营模型的B2B组织的管理和管理。

从管理员那里，具有适当权限的用户可以生成一个&#x200B;**[!UICONTROL Company Hierarchy]**，该结构反映了由多个公司组成的企业企业的组织结构。 此层次结构允许他们查看和管理公司作为一个组。 例如，管理员可以指定一个母公司，并分配作为母公司的子公司运营的所有公司。 然后，父公司管理员可以查看和管理所有已分配公司的公司帐户。

有关详细信息，请参阅[公司管理](manage-companies.md)。

## Adobe Commerce 的服务

Adobe Commerce的服务是托管服务，可为Adobe Commerce和Magento Open Source提供扩展功能。 支持B2B工作流的服务包括：

* [目录服务](https://experienceleague.adobe.com/docs/commerce-merchant-services/catalog-service/guide-overview.html)
* [实时搜索](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/guide-overview.html)
* [产品Recommendations](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/guide-overview.html)

## 共享目录

共享目录是一种定价级别，允许在一个或多个网站上为不同公司设置每个产品的自定义价格。 通过使用共享目录，您可以通过为不同的客户组应用不同的定价级别来销售产品。 只有配置为支持公司帐户的Commerce商店才支持共享目录。

有关详细信息，请参阅[使用共享目录](catalog-shared.md)。

## 快速订购

配置快速订单，在登录客户知道要订购的产品名称或SKU时，将订单流程减少为多次单击。

有关详细信息，请参阅[快速订购](quick-order.md)。

## 可转让报价

使用“报价”功能在公司买方和卖方之间起动价格洽谈。

* 授权购买者可以从购物车中启动报价。

* 卖方可从Admin为买方启动报价。

买方和卖方使用报价单管理洽谈过程（如添加物料、更新数量、请求和应用折扣），直至他们达成协议。 管理员中的&#x200B;_Quotes_&#x200B;网格列出了收到的每个报价，并维护了买方与卖方之间的通信历史记录。

仅对配置为支持公司帐户的Commerce商店支持可转让报价。

有关详细信息，请参阅[可转让报价](quotes.md)。

## 采购订单审批

在为公司帐户激活采购订单时，所有订单都会自动创建为采购订单(PO)。 具有所需权限的公司用户可以创建、编辑和删除他们创建的PO以及下属用户创建的PO。 根据其角色和顺序，公司用户可能需要遵守多个批准规则。

有关详细信息，请参阅[公司的采购订单](purchase-order-flow.md)。

## 申请列表

客户在购买经常订购的产品时，可以使用申购单列表来节省时间，因为他们可以直接从列表将商品添加到购物车。 他们可以维护多个列表，重点关注来自不同供应商、购买者、团队、营销活动或简化其工作流程的任何其他供应商的产品。

有关详细信息，请参阅[申请列表](requisition-lists.md)。

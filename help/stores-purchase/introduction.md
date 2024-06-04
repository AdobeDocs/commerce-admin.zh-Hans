---
title: 商店和购买体验简介
description: 了解用于构建和管理在线商店的功能以及客户的购买体验。
exl-id: 7ced9cbc-49b4-48f7-aae2-fcb48fdb888f
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '671'
ht-degree: 0%

---

# 商店和购买体验简介

Adobe Commerce和Magento Open Source提供了一系列全面的功能，用于构建和管理您的在线商店以及客户的购买体验。 在Commerce实例中，您可以管理网站、商店和视图的商店层次结构。 您还可以配置为多个区域设置运行商店所需的税和汇率，包括产品和客户组的税分类。

## 存储结构

Adobe Commerce或Magento Open Source的单个实例可以支持使用不同属性和内容的多个网站、商店或商店视图。 一种典型的情况是，在不同的域中设置具有不同选项的存储区。 例如，您可能希望一个域上的一组类别和产品，以及不同域上另一组类别和产品，并使用另一种语言。 商家可以在“管理员”中配置网站、商店和商店视图。

当 [层级](stores.md) 定义，您可以根据以下各项应用配置设置 [范围](../getting-started/websites-stores-views.md#scope-settings) 以便每个站点、商店和商店视图提供您想要的产品目录和店面体验。

## 购买点

Adobe Commerce和Magento Open Source通过在提交订单之前自动验证所有项目的SKU和可用性，从而减少订购错误。 您可以配置 [购物车](cart.md) 和 [签出选项](checkout-process.md) 从交易到交付，提供最佳购买体验。 登录到其帐户的客户可以快速完成结帐，因为许多信息都已在他们的帐户中。 此 _结帐_ 页面将引导客户完成订单事务处理的流程的每个步骤。 如果您激活 [即时购买](checkout-instant-purchase.md)，客户可以使用其帐户中保存的信息来加速结账过程。

>[!TIP]
>
>![Adobe Commerce B2B](../assets/b2b.svg) 安装和启用Adobe Commerce B2B后，您可以 _快速订购_ 适用于与公司帐户关联的客户。 当客户知道其要订购的产品的名称或SKU时，此函数会减少订单处理过程中的多次点击。 您还可以为公司帐户配置对可转让报价的支持。 有关B2B功能的详细信息，请参见 [Adobe Commerce B2B用户指南](https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html).

## 购物帮助

客户有时需要帮助才能完成购买。 有些客户喜欢网上购物，但喜欢通过电话订购。 对于在商店中注册了帐户的访客和客户，您可以立即提供帮助。

- [管理购物车](shopping-assisted-cart-manage.md)
- [创建订单](customer-account-create-order.md) （适用于注册客户）
- [更新订单](order-update.md)

![购物车](./assets/storefront-cart-price-group-discount.png){width="700" zoomable="yes"}

通过观看以下视频了解卖家辅助购物：

>[!VIDEO](https://video.tv.adobe.com/v/343662/?quality=12)

## 订单管理和操作

在Admin中，商家可以访问订单工作流和订单处理流程各个阶段的信息：

- 此 [订购](orders.md) 页面为商家提供了所有当前订单的易访问列表，并包括编辑和处理现有订单以及代表客户创建订单的工具。

- 此 [发票](invoices.md) 页列表发票基于临时销售订单并提供该订单的永久记录。

- 此 [装运](shipments.md) 页列出了准备发运的每张发票的发运记录。

- 此 [贷项通知单](credit-memos.md) 页面允许商家处理和管理贷项通知单，它是一个显示缺客户的金额的文档。 金额可用于购买或退款给客户。

- ![Adobe Commerce](../assets/adobe-logo.svg) (仅限Adobe Commerce) [返回](returns.md) 页面列出当前返回的商品请求(RMA)，并用于输入新的退货请求。

- 此 [交易](transactions.md) 页面列出了您的商店和支付系统之间发生的所有支付活动，并可访问更多详细信息。

## 运输和交付

研究表明，商店为顾客提供了多种选择 [投放方法](delivery.md) 比使用单一方法的存储具有更高的转化率。 管理员提供多种工具，商家可以利用这些工具设置多种交付方法并 [装运承运人](carriers.md)，并打印 [配送标签](shipping-labels.md).

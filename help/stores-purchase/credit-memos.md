---
title: 贷项通知单
description: 了解贷项通知单以及如何使用它们签发部分或全部退款。
exl-id: dc2faf86-0182-4661-9543-bc6e00e06dbf
feature: Orders, Invoices, Returns
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '580'
ht-degree: 0%

---

# 贷项通知单

_贷项通知单_&#x200B;是显示客户全部或部分退款的应付金额的文档。 金额可用于购买或退款给客户。 您可以打印单个订单的贷项通知单，或将多个订单的贷项通知单打印为一个批。 必须先为订单生成贷项通知单，然后才能打印贷项通知单。 _贷项通知单_&#x200B;页列出了已发给客户的贷项通知单。

![贷项通知单](./assets/credit-memos.png){width="700" zoomable="yes"}

## 退款方法

订单的[付款方式](payments.md)在一定程度上决定了您退款的方法。

您可以通过三种方式退单：

- 帐户贷项 — 使用贷项帐户支付的订单可以作为帐户贷项退款：
   - ![Adobe Commerce](../assets/adobe-logo.svg) (仅限Adobe Commerce) [商店积分](../customers/store-credit-using.md)
   - ![Adobe Commerce B2B](../assets/b2b.svg) (适用于Adobe Commerce B2B) [帐户付款](../b2b/enable-basic-features.md#configure-payment-on-account) （脱机方法）
   - ![Adobe Commerce B2B](../assets/b2b.svg) (适用于Adobe Commerce B2B) [公司积分](../b2b/credit-company.md)
- [在线退款](payments.md#online-payment-methods) — 通过付款网关(如PayPal或Braintree)以信用卡支付的订单通过付款处理器在线退款。
- [离线退款](payments.md#offline-payment-methods) — 由货到付款（[货到付款](cash-on-delivery.md)）或[支票或汇票](check-money-order.md)支付的订单离线退款。

您可以为任何付款方法签发离线退款或帐户贷项（如果已启用）。

由“货到付款”（[货到付款](cash-on-delivery.md)）或[支票或汇票](check-money-order.md)支付的订单已离线退款。

## 退款工作流

1. **付款操作** — 如果[付款操作](credit-memo-create.md#payment-action-setting)配置设置为`Authorize`，则必须在创建贷项通知单之前生成发票 — 请继续执行步骤2。 如果设置为`Authorize and Capture`，则已生成发票 — 请继续执行步骤3。

1. **生成发票** - [为订单创建发票](invoices.md#create-an-invoice)，以便您可以通过贷项通知单向客户发送退款。

1. **创建贷项通知单** - [&#128279;](credit-memo-create.md)在管理员中为[信用购买](credit-memo-create.md#issue-a-refund-for-a-credit-purchase)或为[支票或汇票](credit-memo-create.md#issue-an-offline-refund-for-check-or-money-order)签发贷项通知单。

## 列描述

| 列 | 描述 |
|--- |--- |
| [!UICONTROL Select] | 选中要执行活动的贷项通知单项目的复选框，或使用列题头中的选择控件。 选项： `Select All` / `Deselect All` |
| [!UICONTROL Credit Memo] | 提交贷项通知单请求时分配的唯一数字标识符。 |
| [!UICONTROL Created] | 买方首次提交贷项通知单请求的日期和时间。 |
| [!UICONTROL Order#] | 正在返回其产品的订单的订单ID。 |
| [!UICONTROL Order Date] | 采购员下达订单的日期和时间。 |
| [!UICONTROL Bill-to Name] | 负责支付订单的人员姓名。 |
| [!UICONTROL Status] | 指示贷项通知单请求的当前状态。 |
| [!UICONTROL Refunded] | 从订单中退款的总金额。 |
| [!UICONTROL Actions] | **[!UICONTROL View]** — 打开贷项通知单请求并维护买方与卖方之间的洽谈记录。 |
| [!UICONTROL Order Status] | 指示订单状态。 |
| [!UICONTROL Purchased From] | 指示下订单的网站、商店和商店视图。 |
| [!UICONTROL Billing Address] | 下订单的客户的帐单地址。 |
| [!UICONTROL Shipping Address] | 将发运订单的地址。 |
| [!UICONTROL Customer Name] | 下订单的客户的名字和姓氏。 |
| [!UICONTROL Email] | 下订单的人员的电子邮件地址。 |
| [!UICONTROL Customer Group] | 客户分配到的客户组。 |
| [!UICONTROL Payment Method] | 用于付款的付款方式。 |
| [!UICONTROL Shipping Information] | 用于装运订单的方法。 |
| [!UICONTROL Subtotal] | 订单小计，不包括运费和手续费以及税金。 |
| [!UICONTROL Shipping & Handling] | 运费和包装费。 |
| [!UICONTROL Adjustment Refund] | 作为额外退款添加到已退款总金额中的金额。 |
| [!UICONTROL Adjustment Fee] | 从退款总额中减去的金额。 |
| [!UICONTROL Grand Total] | 订单总计。 |

{style="table-layout:auto"}

---
title: ’[!UICONTROL Sales] 菜单
description: Commerce管理员包括 [!UICONTROL Sales] 菜单，根据订单在工作流中的位置，提供对用于处理订单的工具的访问权限。
exl-id: 105106a4-85f7-4143-8411-69ff67ff9331
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '435'
ht-degree: 0%

---

# [!UICONTROL Sales] 菜单

“销售”菜单根据交易在订单工作流中的位置列出交易。 您可能会将每个选项视为订单生命周期中的不同阶段。

![销售菜单](./assets/admin-menu-sales.png){width="450" zoomable="yes"}

## 显示 [!UICONTROL Sales] 菜单

在 _管理员_ 侧栏，单击 **[!UICONTROL Sales]**.

## 菜单选项

### [!UICONTROL Quotes]

![Adobe Commerce B2B](../assets/b2b.svg) (适用于Adobe Commerce B2B)

授权购买者可以 [协商价格](../b2b/quotes.md) 与卖家联系，向其 [请求](../b2b/quote-request.md) 从购物车中。

### [!UICONTROL Orders]

当 [订购](orders.md) 之后，将创建销售订单作为交易记录的临时记录。 尚未处理付款，仍可取消订单。

### [!UICONTROL Invoices]

An [发票](invoices.md) 是订单付款的接收记录。 可以为单个订单创建多张发票，每张发票包含您指定的相同数量的或相同数量的已购产品。 根据付款活动，可以在生成发票时自动获取付款。

### [!UICONTROL Shipments]

A [装运](shipments.md) 是已发运订单中产品的记录。 与发票一样，多个发运可以与单个订单关联，直到该订单中的所有产品都已发运。

### [!UICONTROL Credit Memos]

A [贷项通知单](credit-memos.md) 是一个文档，它显示全部或部分退款应向客户支付的金额。 金额可用于购买或退款给客户。

### [!UICONTROL Returns]

![Adobe Commerce](../assets/adobe-logo.svg) (仅限Adobe Commerce)

A [退回商品授权](returns.md) (RMA)适用于要求退回部件以便更换或退款的客户。 可以针对简单、分组、可配置和捆绑产品类型发布RMA。 但是，RMA不适用于虚拟和可下载的产品或礼品卡。

### [!UICONTROL Billing Agreements]

A [billing agreement（计费协议）](paypal-billing-agreements.md) 与采购订单类似，不同之处在于它不限于单次购买。 在结帐过程中，客户选择“开单协议”作为付款方式。 由于客户不必为每次购买输入付款信息，因此开单协议可简化结帐流程。

### [!UICONTROL Transactions]

此 [交易](transactions.md) 页面列出了在您的商店和所有支付系统之间发生的所有支付活动，并提供了对更多详细信息的访问。

### [!UICONTROL Braintree Virtual Terminal]

在“Braintree虚拟终端”页面上，管理员用户可以接受所选金额的付款。 要使终端功能可用，商家应配置basic [Braintree设置](braintree.md). Braintree通过欺诈检测和PayPal集成，提供完全可自定义的结账体验。

### [!UICONTROL Archive]

![Adobe Commerce](../assets/adobe-logo.svg) (仅限Adobe Commerce)

（必须启用存档选项） [存档订单](order-archive.md) 和其他销售文档会定期改进性能，使您的工作区免受不必要信息的影响。

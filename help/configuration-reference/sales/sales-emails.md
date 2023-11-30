---
title: ’[!UICONTROL Sales] &gt； [!UICONTROL Sales Emails]’
description: 查看 [!UICONTROL Sales] &gt； [!UICONTROL Sales Emails] 商务管理员页面。
exl-id: f770e202-6f7e-4f84-9251-7d8a760260b4
feature: Configuration, Communications
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '2331'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Sales Emails]

{{config}}

## [!UICONTROL General Settings]

![常规设置](./assets/sales-emails-general-settings.png)<!-- zoom -->

<!-- [General Settings](https://docs.magento.com/user-guide/system/email-communications.html) -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Asynchronous sending] | 全局 | 确定是否异步发送销售电子邮件。 建议您启用异步发送。 选项： <br/>**`Disable`**— （默认）由事件触发时会发送销售电子邮件。<br/>**`Enable`**  — （推荐）以预先确定的固定时间间隔发送销售电子邮件。 |

{style="table-layout:auto"}

## [!UICONTROL Order]

![订购](./assets/sales-emails-order.png)<!-- zoom -->

<!-- [Order](https://docs.magento.com/user-guide/sales/orders.html) -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Enabled] | 商店视图 | 启用后，会为每个下订单发送事务型电子邮件。 选项： `Yes` / `No` |
| [!UICONTROL New Order Confirmation Email Sender] | 商店视图 | 标识显示为邮件发件人的商店联系人。 默认发件人： `Sales Representative` |
| [!UICONTROL New Order Confirmation Template] | 商店视图 | 标识为确认客户下达的新订单而发送的模板。 默认模板： `New Order` |
| [!UICONTROL New Order Confirmation Template for Guest] | 商店视图 | 标识为确认来宾下达的新订单而发送的模板。 默认模板： `New Order for Guest` |
| [!UICONTROL Send Order Email Copy To] | 商店视图 | 提供接收订单电子邮件副本的任何人的电子邮件地址。 用逗号分隔多个地址。 |
| [!UICONTROL Send Order Email Copy Method] | 商店视图 | 指示用于发送副本的电子邮件方法。 选项包括： <br/>**`Bcc`**— 在发送给客户的同一电子邮件的标题中包含收件人，从而发送礼貌的密文。 客户看不到密件抄送收件人。<br/>**`Separate Email`**  — 将副本作为单独的电子邮件发送。 |

{style="table-layout:auto"}

## [!UICONTROL Order Comments]

![订单备注](./assets/sales-emails-order-comments.png)<!-- zoom -->

<!-- [Order Comments](https://docs.magento.com/user-guide/sales/order-processing.html) -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Enabled] | 商店视图 | 启用后，会为每个订单注释发送事务型电子邮件。 选项： `Yes` / `No` |
| [!UICONTROL Order Comment Email Sender] | 商店视图 | 标识显示为邮件发件人的商店联系人。 默认发件人： `Sales Representative` |
| [!UICONTROL Order Comment Email Template] | 商店视图 | 标识在向客户订单添加评论时发送的模板。 默认模板： `Order Update` |
| [!UICONTROL New Order Confirmation Template for Guest] | 商店视图 | 标识向访客订单添加评论时发送的模板。 默认模板： `Order Update for Guest` |
| [!UICONTROL Send Order Email Copy To|Store View] | 提供接收订单评论电子邮件副本的任何人的电子邮件地址。 用逗号分隔多个地址。 |
| [!UICONTROL Send Order Email Copy Method] | 商店视图 | 指示用于发送副本的方法。 选项包括： <br/>**`Bcc`**— 在发送给客户的同一电子邮件的标题中包含收件人，从而发送礼貌的密文。 客户看不到密件抄送收件人。<br/>**`Separate Email`**  — 将副本作为单独的电子邮件发送。 |

{style="table-layout:auto"}

## [!UICONTROL Invoice]

![发票](./assets/sales-emails-invoice.png)<!-- zoom -->

<!-- [Invoice](https://docs.magento.com/user-guide/sales/invoices.html) -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Enabled] | 商店视图 | 启用后，将为生成的每个发票发送事务型电子邮件。 选项： `Yes` / `No` |
| [!UICONTROL Invoice Email Sender] | 商店视图 | 标识显示为邮件发件人的商店联系人。 默认发件人： `Sales Representative` |
| [!UICONTROL Invoice Email Template] | 商店视图 | 标识在为客户生成发票时发送的模板。 默认模板： `New Invoice` |
| [!UICONTROL Invoice Email Template for Guest] | 商店视图 | 标识在为来宾生成发票时发送的模板。 默认模板： `New Invoice for Guest` |
| [!UICONTROL Send Invoice Email Copy To] | 商店视图 | 提供接收发票电子邮件副本的任何人的电子邮件地址。 用逗号分隔多个地址。 |
| [!UICONTROL Send Invoice Email Copy Method] | 商店视图 | 指示用于发送副本的方法。 选项包括： <br/>**`Bcc`**— 在发送给客户的同一电子邮件的标题中包含收件人，从而发送礼貌的密文。 客户看不到密件抄送收件人。<br/>**`Separate Email`**  — 将副本作为单独的电子邮件发送。 |

{style="table-layout:auto"}

## [!UICONTROL Invoice Comments]

![发票注释](./assets/sales-emails-invoice-comments.png)<!-- zoom -->

<!-- [Invoice Comments](https://docs.magento.com/user-guide/sales/invoice-create.html) -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Enabled] | 商店视图 | 启用后，会为每个发票注释发送事务型电子邮件。 选项： `Yes` / `No` |
| [!UICONTROL Invoice Comment Email Sender] | 商店视图 | 标识显示为邮件发件人的商店联系人。 默认发件人： `Sales Representative` |
| [!UICONTROL Invoice Comment Email Template] | 商店视图 | 标识向客户发票添加注释时发送的模板。 默认模板： `Invoice Update` |
| [!UICONTROL Invoice Comment Email Template for Guest] | 商店视图 | 标识向来宾发票添加注释时发送的模板。 默认模板： `Invoice Update for Guest` |
| [!UICONTROL Send Invoice Comment Email Copy To] | 商店视图 | 提供接收发票注释电子邮件副本的任何人的电子邮件地址。 用逗号分隔多个地址。 |
| [!UICONTROL Send Invoice Comments Email Copy Method] | 商店视图 | 指示用于发送副本的电子邮件方法。 选项包括： <br/>**`Bcc`**— 在发送给客户的同一电子邮件的标题中包含收件人，从而发送礼貌的密文。 客户看不到密件抄送收件人。<br/>**`Separate Email`**  — 将副本作为单独的电子邮件发送。 |

{style="table-layout:auto"}

## [!UICONTROL Shipment]

![装运](./assets/sales-emails-shipment.png)<!-- zoom -->

<!-- [Shipment](https://docs.magento.com/user-guide/sales/shipments.html) -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Enabled] | 商店视图 | 启用后，将为生成的每次装运发送事务性电子邮件。 选项： `Yes` / `No` |
| [!UICONTROL Shipment Email Sender] | 商店视图 | 标识显示为邮件发件人的商店联系人。 默认发件人： `Sales Representative` |
| [!UICONTROL Shipment Email Template] | 商店视图 | 标识在为客户生成装运时发送的模板。 默认模板： `New Shipment` |
| [!UICONTROL Shipment Email Template for Guest] | 商店视图 | 标识在为来宾生成装运时发送的模板。 默认模板： `New Shipment for Guest` |
| [!UICONTROL Send Shipment Email Copy To] | 商店视图 | 提供应接收装运电子邮件副本的任何人的电子邮件地址。 用逗号分隔多个地址。 |
| [!UICONTROL Send Shipment Email Copy Method] | 商店视图 | 指示用于发送副本的方法。 选项包括： <br/>**`Bcc`**— 在发送给客户的同一电子邮件的标题中包含收件人，从而发送礼貌的密文。 客户看不到密件抄送收件人。<br/>**`Separate Email`**  — 将副本作为单独的电子邮件发送。 |

{style="table-layout:auto"}

## [!UICONTROL Shipment Comments]

![装运注释](./assets/sales-emails-shipment-comments.png)<!-- zoom -->

<!-- [Shipment Comments](https://docs.magento.com/user-guide/sales/shipments.html) -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Enabled] | 商店视图 | 启用后，会为每个装运注释发送事务性电子邮件。 选项： `Yes` / `No` |
| [!UICONTROL Shipment Comment Email Sender] | 商店视图 | 标识显示为邮件发件人的商店联系人。 默认发件人： `Sales Representative` |
| [!UICONTROL Shipment Comment Email Template] | 商店视图 | 标识在向客户发运添加注释时发送的模板。 默认模板： `Shipment Update` |
| [!UICONTROL Shipment Comment Email Template for Guest] | 商店视图 | 标识向来宾装运添加注释时发送的模板。 默认模板： `Shipment Update for Guest` |
| [!UICONTROL Send Shipment Comment Email Copy To] | 商店视图 | 提供接收装运注释电子邮件副本的任何人的电子邮件地址。 用逗号分隔多个地址。 |
| [!UICONTROL Send Shipment Comments Email Copy Method] | 商店视图 | 指示用于发送副本的电子邮件方法。 选项包括： <br/>**`Bcc`**— 在发送给客户的同一电子邮件的标题中包含收件人，从而发送礼貌的密文。 客户看不到密件抄送收件人。<br/>**`Separate Email`**  — 将副本作为单独的电子邮件发送。 |

{style="table-layout:auto"}

## [!UICONTROL Credit Memo]

![贷项通知单](./assets/sales-emails-credit-memo.png)<!-- zoom -->

<!-- [Credit Memo](https://docs.magento.com/user-guide/sales/credit-memos.html) -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Enabled] | 商店视图 | 为生成的每个贷项通知单激活事务型电子邮件。 选项： `Yes` / `No` |
| [!UICONTROL Credit Memo Email Sender] | 商店视图 | 标识显示为邮件发件人的商店联系人。 默认发件人： `Sales Representative` |
| [!UICONTROL Credit Memo Email Template] | 商店视图 | 标识在为客户生成贷项通知单时发送的模板。 默认模板： `New Credit Memo` |
| [!UICONTROL Credit Memo Email Template for Guest] | 商店视图 | 标识在为来宾生成贷项通知单时发送的模板。 默认模板： `New Credit Memo for Guest` |
| [!UICONTROL Send Credit Memo Email Copy To] | 商店视图 | 提供应接收贷项通知单电子邮件副本的人员的电子邮件地址。 用逗号分隔多个地址。 |
| [!UICONTROL Send Credit Memo Email Copy Method] | 商店视图 | 指示用于发送副本的方法。 选项包括： <br/>**`Bcc`**— 在发送给客户的同一电子邮件的标题中包含收件人，从而发送礼貌的密文。 客户看不到密件抄送收件人。<br/>**`Separate Email`**  — 将副本作为单独的电子邮件发送。 |

{style="table-layout:auto"}

## [!UICONTROL Credit Memo Comments]

![贷项通知单备注](./assets/sales-emails-credit-memo-comments.png)<!-- zoom -->

<!-- [Credit Memo Comments](https://docs.magento.com/user-guide/sales/credit-memo-create.html) -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Enabled] | 商店视图 | 启用后，会为每个贷项通知单注释发送事务型电子邮件。 选项： `Yes` / `No` |
| [!UICONTROL Credit Memo Comment Email Sender] | 商店视图 | 标识显示为邮件发件人的商店联系人。 默认发件人： `Sales Representative` |
| [!UICONTROL Credit Memo Comment Email Template] | 商店视图 | 标识向客户贷项通知单添加注释时发送的模板。 默认模板： `Credit Memo Update` |
| [!UICONTROL Credit Memo Comment Email Template for Guest] | 商店视图 | 标识向访客贷项通知单添加注释时发送的模板。 默认模板： `Credit Memo Update for Guest` |
| [!UICONTROL Send Credit Memo Comment Email Copy To] | 商店视图 | 指定要接收贷项通知单评论电子邮件副本的任何人的电子邮件地址。 用逗号分隔多个地址。 |
| [!UICONTROL Send Credit Memo Comments Email Copy Method] | 商店视图 | 指示用于发送副本的电子邮件方法。 选项包括： <br/>**`Bcc`**— 在发送给客户的同一电子邮件的标题中包含收件人，从而发送礼貌的密文。 客户看不到密件抄送收件人。<br/>**`Separate Email`**  — 将副本作为单独的电子邮件发送。 |

{style="table-layout:auto"}

## [!UICONTROL Order Ready For Pickup in Store]

![订单已准备好到店内提货](./assets/sales-emails-ready-pickup.png)<!-- zoom -->

<!-- [Order Ready For Pickup in Store](https://docs.magento.com/user-guide/shipping/shipping-in-store-delivery.html) -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Enabled] | 商店视图 | 启用后，会在订单准备好进行店内提货时发送事务型电子邮件。 选项： `Yes` / `No` |
| [!UICONTROL Order Ready For Pickup Email Sender] | 商店视图 | 标识显示为邮件发件人的商店联系人。 默认发件人： `General Contact` |
| [!UICONTROL Order Ready For Pickup Email Template] | 商店视图 | 标识用于事务型电子邮件的模板，该模板适用于已注册客户准备在商店中提货的每个订单。 默认模板： `Order is Ready for Pickup` |
| [!UICONTROL Order Ready For Pickup Email Template for Guest] | 商店视图 | 标识用于事务型电子邮件的模板，该模板适用于准备好在商店中提货的访客的每个订单。 默认模板： `Order is Ready for Pickup for Guest` |
| 将订单准备取货电子邮件副本发送至 | 商店视图 | 指定要接收副本的任何人的电子邮件地址 _订单准备提货_ 电子邮件。 用逗号分隔多个地址。 |
| [!UICONTROL Send Order Ready For Pickup Email Copy Method] | 商店视图 | 指示用于发送副本的电子邮件方法。 选项： <br/>**`Bcc`**— 在发送给客户的同一电子邮件的标题中包含收件人，从而发送礼貌的密文。 客户看不到密件抄送收件人。<br/>**`Separate Email`**  — 将副本作为单独的电子邮件发送。 |

{style="table-layout:auto"}

## [!UICONTROL Purchase Order Approval]

{{b2b-feature}}

![采购订单审批](./assets/sales-emails-purchase-order-approval.png)<!-- zoom -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Enabled] | 商店视图 | 启用后，将在采购订单流程中发送电子邮件。 选项： `Yes` / `No` |
| [!UICONTROL Created and requires Approval Purchase Order (to Buyer)] | 商店视图 | 向采购订单创建者发送电子邮件确认。 |
| [!UICONTROL Created and Automatically approved Purchase Order (to Buyer)] | 商店视图 | 向采购订单创建者发送电子邮件确认。 |
| [!UICONTROL Approved Purchase Order (to Buyer)] | 商店视图 | 在采购订单批准时向创建者发送电子邮件。 |
| [!UICONTROL Rejected Purchase Order (to Buyer)] | 商店视图 | 在采购订单被拒绝时向创建者发送电子邮件。 |
| [!UICONTROL Comment added to Purchase Order] | 商店视图 | 向PO中添加评论时向创建者发送电子邮件。 |
| [!UICONTROL Error creating Order from Purchase Order (to Buyer)] | 商店视图 | 通知创建者在将采购单转换为订单时出错。 |
| [!UICONTROL Purchase Order required Approval (to Approver)] | 商店视图 | 发送电子邮件，通知批准者采购订单需要其批准。 |

{style="table-layout:auto"}

## [!UICONTROL Quote]

{{b2b-feature}}

![引用](./assets/sales-emails-quote.png)<!-- zoom -->

<!-- [Quotes](https://docs.magento.com/user-guide/customers/account-dashboard-quotes.html) -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Enabled] | 商店视图 | 允许从当前商店视图发送报价电子邮件。 选项： `Yes` / `No` |
| [!UICONTROL Updated Quote Template (to Buyer)] | 商店视图 | 确定在有更新的报价可用时用于通知采购员的电子邮件模板。 默认模板： `Updated Quote` |
| [!UICONTROL Declined Quote Template (to Buyer)] | 商店视图 | 确定在报价被拒绝时用于通知买方电子邮件模板。 默认模板： `Declined Quote` |
| [!UICONTROL New Quote Template (to Seller)] | 商店视图 | 确定在收到新报价请求时用于通知销售方的电子邮件模板。 默认模板： `New Quote` |
| [!UICONTROL Updated Quote Template (to Seller)] | 商店视图 | 确定在收到更新的报价时用于通知卖方的电子邮件模板。 默认模板： `Updated Quote` |
| [!UICONTROL Quote Expiration (in 48 hrs)] | 商店视图 | 指定用于报价过期前48小时发送的过期通知的电子邮件模板。 默认模板： `Expiration Warning` |
| [!UICONTROL Quote Expiration (in 24 hrs)] | 商店视图 | 指定用于报价过期前24小时发送的过期通知的电子邮件模板。 默认模板： `Expiration Warning 1` |
| [!UICONTROL Expiration Date Reset] | 商店视图 | 指定在过期日期更改时用于发送通知的电子邮件模板。 默认模板： `Expiration Date Reset` |
| [!UICONTROL Send Quote Email Copy To] | 商店视图 | 指定每个要接收报价电子邮件副本的人员的电子邮件地址。 用逗号分隔多个地址。 |
| [!UICONTROL Send Quote Email Copy Method] | 商店视图 | 指示用于发送副本的电子邮件方法。 选项包括： <br/>**`Bcc`**— 在发送给客户的同一电子邮件的标题中包含收件人，从而发送礼貌的密文。 客户看不到密件抄送收件人。<br/>**`Separate Email`**  — 将副本作为单独的电子邮件发送。 |

{style="table-layout:auto"}

## [!UICONTROL RMA]

{{ee-feature}}

![RMA](./assets/sales-emails-rma.png)<!-- zoom -->

<!-- [RMA](https://docs.magento.com/user-guide/sales/returns.html) -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Enabled] | 商店视图 | 为生成的每个RMA激活电子邮件通知。 选项： `Yes` / `No` |
| [!UICONTROL RMA Email Sender] | 商店视图 | 标识 [商店联系人](../../getting-started/store-details.md#store-email-addresses) 显示为消息的发送者。 默认值： `Sales Representative` |
| [!UICONTROL RMA Email Template] | 商店视图 | 确定 [电子邮件模板](../../systems/email-templates.md) ，用于在为客户生成RMA时发送通知。 默认模板： `New RMA` |
| [!UICONTROL RMA Email Template for Guest] | 商店视图 | 确定在为来宾生成RMA时发送的模板。 默认模板： `New RMA for Guest` |
| [!UICONTROL Send RMA Email Copy To] | 商店视图 | 提供应接收RMA电子邮件副本的人员的电子邮件地址。 用逗号分隔多个地址。 |
| [!UICONTROL Send RMA  Email Copy Method] | 商店视图 | 指示用于发送副本的电子邮件方法。 选项包括： <br/>**`Bcc`**— 在发送给客户的同一电子邮件的标题中包含收件人，从而发送礼貌的密文。 客户看不到密件抄送收件人。<br/>**`Separate Email`**  — 将副本作为单独的电子邮件发送。 |

{style="table-layout:auto"}

## [!UICONTROL RMA Authorization]

{{ee-feature}}

![RMA授权](./assets/sales-emails-rma-auth.png)<!-- zoom -->

<!-- [RMA Authorization](https://docs.magento.com/user-guide/sales/rma-configure.html) -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Enabled] | 商店视图 | 启用后，会为每个RMA授权发送电子邮件通知。 选项： `Yes` / `No` |
| [!UICONTROL RMA Authorization Email Sender] | 商店视图 | 标识 [商店联系人](../../getting-started/store-details.md#store-email-addresses) 显示为邮件发件人。 默认值： `Sales Representative` |
| [!UICONTROL RMA Authorization Email Template] | 商店视图 | 确定 [电子邮件模板](../../systems/email-templates.md) 发送RMA授权通知时使用该字段。 默认模板： `RMA Authorization` |
| [!UICONTROL RMA Authorization Email Template for Guest] | 商店视图 | 确定向来宾发送RMA授权通知时使用的模板。 默认模板： `RMA Authorization for Guest` |
| [!UICONTROL Send RMA Authorization Email Copy To] | 商店视图 | 提供接收RMA授权电子邮件副本的任何人的电子邮件地址。 用逗号分隔多个地址。 |
| [!UICONTROL Send RMA Authorization Email Copy Method] | 商店视图 | 指示用于发送副本的电子邮件方法。 选项包括： <br/>**`Bcc`**— 在发送给客户的同一电子邮件的标题中包含收件人，从而发送礼貌的密文。 客户看不到密件抄送收件人。<br/>**`Separate Email`**  — 将副本作为单独的电子邮件发送。 |

{style="table-layout:auto"}

## [!UICONTROL RMA Admin Comments]

{{ee-feature}}

![RMA管理注释](./assets/sales-emails-rma-admin-comments.png)<!-- zoom -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Enabled] | 商店视图 | 启用后，会为每个RMA管理员注释发送电子邮件通知。 选项： `Yes` / `No` |
| [!UICONTROL RMA Comment Email Sender] | 商店视图 | 标识 [商店联系人](../../getting-started/store-details.md#store-email-addresses) 显示为邮件发件人。 默认值： `Sales Representative` |
| [!UICONTROL RMA Comment Email Template] | 商店视图 | 确定 [电子邮件模板](../../systems/email-templates.md) 当管理员为客户向RMA添加注释时使用。 默认模板： `RMA Admin Comments` |
| [!UICONTROL RMA Comment Email Template for Guest] | 商店视图 | 确定管理员在来宾的RMA中添加评论时使用的模板。 默认模板： `RMA Admin Comments for Guest` |
| [!UICONTROL Send RMA Comment Email Copy To] | 商店视图 | 提供接收通知副本的任何人的电子邮件地址。 用逗号分隔多个地址。 |
| [!UICONTROL Send RMA Comments Email Copy Method] | 商店视图 | 指示用于发送副本的电子邮件方法。 选项包括： <br/>**`Bcc`**— 在发送给客户的同一电子邮件的标题中包含收件人，从而发送礼貌的密文。 客户看不到密件抄送收件人。<br/>**`Separate Email`**  — 将副本作为单独的电子邮件发送。 |

{style="table-layout:auto"}

## [!UICONTROL RMA Customer Comments]

{{ee-feature}}

![RMA客户备注](./assets/sales-emails-rma-customer-comments.png)<!-- zoom -->

<!-- [RMA Customer Comments](https://docs.magento.com/user-guide/sales/returns.html) -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Enabled] | 商店视图 | 启用后，会为每个RMA客户备注发送电子邮件通知。 选项： `Yes` / `No` |
| [!UICONTROL RMA Comment Email Sender] | 商店视图 | 标识 [商店联系人](../../getting-started/store-details.md#store-email-addresses) 显示为邮件发件人。 默认值： `Customer Support` |
| [!UICONTROL RMA Comment Email Recipient] | 商店视图 | 标识作为客户评论电子邮件收件人的商店联系人。 默认值： `Sales Representative` |
| [!UICONTROL RMA Comment Email Template] | 商店视图 | 确定 [电子邮件模板](../../systems/email-templates.md) 当客户向RMA添加注释时使用该选项。 默认模板： `RMA Admin Comments` |
| [!UICONTROL Send RMA Comment Email Copy To] | 商店视图 | 提供接收通知副本的任何人的电子邮件地址。 用逗号分隔多个地址。 |
| [!UICONTROL Send RMA Comments Email Copy Method] | 商店视图 | 指示用于发送副本的电子邮件方法。 选项包括： <br/>**`Bcc`**— 在发送给客户的同一电子邮件的标题中包含收件人，从而发送礼貌的密文。 客户看不到密件抄送收件人。<br/>**`Separate Email`**  — 将副本作为单独的电子邮件发送。 |

{style="table-layout:auto"}

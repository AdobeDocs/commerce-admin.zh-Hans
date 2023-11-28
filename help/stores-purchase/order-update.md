---
title: 更新订单
description: 了解如何在管理员中更新客户订单。
exl-id: 15c73d27-f4bd-47d6-8d36-902074f9c3e6
feature: Orders, Customer Service
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '767'
ht-degree: 0%

---

# 更新订单

在帮助已下订单的客户时，您必须确定订单的状态。 的可用选项 `Pending` 顺序不同于 `Processing` 顺序。 有关更多信息，请参阅 [处理订单](order-processing.md).

## 待处理订单

客户下订单后，但在收到付款之前，订单处于 `Pending` 状态。 您可以编辑订单、将其置于暂停状态或完全取消订单。 待定订单的按钮栏列出了订单可用的操作。

![待定订单选项](./assets/order-button-bar-pending.png){width="600" zoomable="yes"}

如果修改了订单的主要部分，则会取消原始订单并生成新订单。 但是，您可以更改帐单或送货地址而不生成新订单。

| 按钮 | 描述 |
|--- |--- |
| **[!UICONTROL Back]** | 返回到“订单”页而不保存更改。 |
| **[!UICONTROL Login as Customer]** | 允许管理员用户协助客户完成订单。 |
| **[!UICONTROL Cancel]** | 取消待处理订单。 |
| **[!UICONTROL Send Email]** | 向客户发送有关待处理订单的电子邮件。 |
| **[!UICONTROL Hold]** / **[!UICONTROL Unhold]** | 将待处理订单的状态更改为 `On Hold`. 要释放暂挂，请选择 _[!UICONTROL Unhold]_. |
| **[!UICONTROL Invoice]** | 创建 [发票](invoices.md#create-an-invoice) 通过将订单转换为发票，并将订单状态更改为 `processing`. |
| **[!UICONTROL Ship]** | 创建 [装运](shipments.md#create-a-shipment) 订单记录。 |
| **[!UICONTROL Reorder]** | 创建与当前待处理订单重复的新待处理订单。 |
| **[!UICONTROL Edit]** | 在编辑模式下打开待处理订单。 “编辑”按钮仅适用于待定订单，或适用于基于洽谈的订单 [引号](../b2b/quotes.md). |

{style="table-layout:auto"}

## 处理订单

订单输入 `Processing` 状态时间：

* 当付款活动设置为时，接收/捕获订单付款并生成发票 `Authorize and Capture`.
* 当付款活动设置为时，授权订单事务处理，但尚未获取付款 `Authorize`.

此 [付款活动配置](../configuration-reference/sales/payment-methods.md#payment-actions) 确定创建订单后可用的订单操作。

您不能对 `Processing` 订单，但您可以编辑帐单和送货地址。

![处理顺序选项](./assets/order-button-bar-processing.png){width="600" zoomable="yes"}

>[!NOTE]
>
>当付款方法的付款活动设置为时 `Authorize and Capture`，客户下达订单时会自动创建发票。 在这种情况下，您可以使用 [贷项通知单](credit-memo-create.md)，但无法 [取消](#cancel-a-pending-order) 或 [空白](#void-a-processing-order) 订单。

| 按钮 | 描述 |
|--- |--- |
| **[!UICONTROL Back]** | 返回到“订单”页而不保存更改。 |
| **[!UICONTROL Send Email]** | 向客户发送有关订单的电子邮件。 |
| **[!UICONTROL Void]** | [空洞](#void-a-processing-order) 订单事务处理，或部分订单事务处理。 |
| **[!UICONTROL Credit Memo]** | 启动流程以创建 [贷项通知单](credit-memo-create.md). |
| **[!UICONTROL Hold]** / **[!UICONTROL Unhold]** | 将销售订单的状态更改为 `On Hold`. 要释放销售订单的暂挂，请选择 _[!UICONTROL Unhold]_. |
| **[!UICONTROL Reorder]** | 根据当前订单创建新的待处理订单。 |
| **[!UICONTROL Create Returns]** | ![Adobe Commerce](../assets/adobe-logo.svg) (仅限Adobe Commerce)启动流程以 [返回](returns.md) 订单中的一个或多个项目。 |

{style="table-layout:auto"}

## 撤消处理订单

当订单仍然在 `Processing` 状态，并且付款集成设置为 `Authorize` (非 `Authorize and Capture`)，您只能撤消事务处理或取消订单。 [取消订单](#cancel-a-pending-order) 也会使授权失效。

使用付款方法下达订单，且付款活动设置为时 `Authorize and Capture` 您可以通过贷项通知单退还资金，但不能取消它，因为已开票并且已获取付款。

您的付款方式决定了可用的付款活动。 请参阅 [付款操作](../configuration-reference/sales/payment-methods.md#payment-actions) 以了解更多信息。

**_要撤消订单，请执行以下操作：_**

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. 在 **[!UICONTROL Action]** 要编辑的订单的列，请单击 **[!UICONTROL View]**.

1. 单击 **[!UICONTROL Void]** 使订单失效。

1. 出现提示时，单击 **[!UICONTROL OK]** 使订单失效。

您可以使用发放任何所需的退款 [贷项通知单](credit-memo-create.md) 资金被抓获之后。 您还可以创建 [退货授权(RMA)](returns.md) 颁发给退货商。 要了解更多信息，请参阅 [处理订单](order-processing.md).

## 编辑待处理订单

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. 在 **[!UICONTROL Action]** 要编辑的订单的列，请单击 **[!UICONTROL View]**.

1. 单击 **[!UICONTROL Edit]**.

   ![编辑顺序](./assets/order-edit.png){width="600" zoomable="yes"}

1. 出现提示时，单击 **[!UICONTROL OK]** 以继续编辑。

1. 根据需要更新订单。

1. 应用更改：
   * 要保存对帐单或送货地址所做的更改，请单击 **[!UICONTROL Save]**.
   * 要保存对行项目所做的更改并重新处理订单，请单击 **[!UICONTROL Submit Order]**.

## 暂停订单

如果客户的首选付款方式不可用，或者如果物料暂时缺货，您可以暂挂订单。

1. 在 _订购_ 网格，查找 `Pending` 要暂停的订单。

1. 在 _操作_ 列，单击 **[!UICONTROL View]**.

1. 单击 **[!UICONTROL Hold]** 以暂停订单。

要删除订单暂挂，请再次编辑该订单并单击 **[!UICONTROL Unhold]**.

## 取消待处理订单

取消订单会将其状态从 `Pending` 到 `Canceled`.

1. 在 _[!UICONTROL Orders]_网格，查找要取消的待处理订单。

1. 在 _[!UICONTROL Action]_列，单击&#x200B;**[!UICONTROL View]**.

1. 单击 **[!UICONTROL Cancel]** 取消订单。

订单的状态现在为 `Canceled`.

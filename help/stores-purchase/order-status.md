---
title: 订单状态
description: 了解预定义的订单状态，以及如何定义自定义订单状态以满足您的操作需求。
exl-id: d1153558-a721-4643-a70c-7fc20072983c
feature: Orders
source-git-commit: c2d5e9b41a76ba58d1343a8b3ee5122104d5bfe0
workflow-type: tm+mt
source-wordcount: '1223'
ht-degree: 0%

---

# 订单状态

所有订单都具有与订单处理[工作流](order-processing.md)中的阶段关联的订单状态。\
顺序状态和顺序状态之间的区别在于&#x200B;**[!UICONTROL order states]**&#x200B;是以编程方式使用的。 他们不是
对客户或管理员用户可见。 它们决定订单的流程，以及可以执行的操作
按一定状态订购。\
**[!UICONTROL Order statuses]**&#x200B;用于将订单的状态传达给客户和管理用户。
您可以创建附加订单状态以满足运营需求。 订单状态显示方便
Adobe Commerce外部的进度，例如订单领料和交货进度。 它们对订单没有任何影响
正在处理工作流。\
每个订单状态都与一个订单状态相关联。 您的商店有一组预定义的订单状态和
订单状态设置。

![订单状态和状态](./assets/order-states-and-statuses.png){width="700" zoomable="yes"}

每个订单的状态显示在&#x200B;_订单_&#x200B;网格的&#x200B;_状态_&#x200B;列中。

![订单状态](./assets/stores-order-status-column.png){width="700" zoomable="yes"}

>[!TIP]
>
>部分退款的订单在&#x200B;**_所有_**&#x200B;订购物料（包括退款物料）发运之前仍处于`Processing`状态。 在订单中的每个项目都已发运之前，订单状态不会更改为`Complete`。

## 订单状态工作流

![订单状态工作流](./assets/order-state-workflow.png)

## 预定义状态

| 订单状态 | 状态代码 |                                                                                                                                                                                                                                                                                        |
|--------------------------|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 已接收 | `received` | 此状态是启用异步订单下达时下达的订单的初始状态。 |
| 可疑欺诈 | `fraud` | 有时通过PayPal或其他付款网关支付的订单会被标记为&#x200B;_可疑欺诈_。 此状态表示该订单未开具发票，并且未发送确认电子邮件。 |
| 正在处理 | `processing` | 当新订单的状态设置为“正在处理”时，_自动为所有项目开票_&#x200B;选项将在配置中变得可用。 对于使用礼品卡、商店信用、奖励积分或其他离线付款方式下单的订单，不会自动创建发票。 |
| 待处理付款 | `pending_payment` | 如果创建了订单并且使用了PayPal或类似的支付方式，则会使用此状态。 这意味着客户被定向到支付网关网站，但尚未收到退货信息。 客户付款时，此状态会更改。 |
| 付款复核 | `payment_review` | 打开PayPal付款审核时，将出现此状态。 |
| 待处理 | `pending` | 此状态表示尚未提交任何发票和发运。 |
| 保持 | `holded` | 此状态只能手动分配。 您可以暂停任何订单。 |
| 完成 | `complete` | 此状态表示订单已创建、已支付并已发运给客户。 |
| 已关闭 | `closed` | 此状态表示订单已分配了贷项通知单，并且客户已收到退款。 |
| 已取消 | `canceled` | 当客户未在指定时间内付款时，可以在管理员中手动分配此状态，对于某些付款网关，也可以手动分配。 |
| 被拒绝 | `rejected` | 此状态表示订单在异步订单处理期间被拒绝。 在异步下订单期间出现en错误时，会发生这种情况。 |
| PayPal已取消冲销 | `paypay_canceled_reversal` | 此状态表示PayPal已取消冲销。 |
| 待处理PayPal | `pending_paypal` | 此状态表示PayPal已收到订单，但尚未处理付款。 |
| PayPal已撤消 | `paypal_reversed` | 此状态表示PayPal已冲销交易记录。 |

{style="table-layout:auto"}

## 自定义订单状态

除了预设的订单状态设置外，您还可以创建自己的自定义订单状态设置，将其分配给订单状态，并为订单状态设置默认订单状态。 订单状态指示订单在订单处理工作流中的位置，并且订单状态为订单的位置分配有意义的可翻译标签。 例如，您可能需要自定义订单状态，如`packaging"`、`backordered`，或特定于您需求的状态。 您可以为自定义状态创建一个描述性名称，并将其分配给工作流中关联的订单状态。

>[!NOTE]
>
>订单工作流中仅使用默认自定义订单状态值。 未设置为默认值的自定义状态值只能在该顺序的注释部分中使用。

![订单状态设置](./assets/order-status.png){width="700" zoomable="yes"}

### 创建自定义订单状态

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Order Status]**。

1. 单击右上角的&#x200B;**[!UICONTROL Create New Status]**。

   ![创建新订单状态](./assets/order-status-new.png){width="600" zoomable="yes"}

1. 更新&#x200B;_[!UICONTROL Order Status Information]_&#x200B;部分：

   - 输入&#x200B;**[!UICONTROL Status Code]**&#x200B;供内部引用。 第一个字符必须是字母(a-z)，其余字符可以是字母和数字(0-9)的任意组合。 请使用下划线字符而不是空格。

   - 对于&#x200B;**[!UICONTROL Status Label]**，请输入一个标签，该标签在管理员和店面中标识状态设置。

1. 在&#x200B;_[!UICONTROL Store View Specific Labels]_&#x200B;部分中，输入不同商店视图所需的任何标签。

1. 单击&#x200B;**[!UICONTROL Save Status]**。

### 将订单状态分配给状态

1. 在&#x200B;_订单状态_&#x200B;页面上，单击&#x200B;**[!UICONTROL Assign Status to State]**。

   ![分配状态](./assets/store-status-assign-status.png){width="600" zoomable="yes"}

1. 更新&#x200B;**[!UICONTROL Assignment Information]**&#x200B;部分，请执行以下操作：

   - 选择要分配的&#x200B;**[!UICONTROL Order Status]**。 它们按状态标签列出。

   - 将&#x200B;**[!UICONTROL Order State]**&#x200B;设置为工作流中订单状态所属的位置。

     >[!NOTE]
     >
     >**_[!UICONTROL Order State]_**&#x200B;列表包含默认分配的订单状态。 例如，显示`Pending`默认订单状态，而不是`New`订单状态值。

   - 要使此状态成为订单状态的默认状态，请选中&#x200B;**[!UICONTROL Use Order Status as Default]**&#x200B;复选框。

     >[!NOTE]
     >
     >订单工作流中仅使用默认订单状态。 只能在管理员的&#x200B;**[!UICONTROL Order Comments]**&#x200B;部分中设置非默认状态。

   - 若要使此状态在店面中可见，请选中&#x200B;**[!UICONTROL Visible On Storefront]**&#x200B;复选框。

   ![将状态分配给状态](./assets/order-status-assign-state.png){width="600" zoomable="yes"}

1. 单击&#x200B;**[!UICONTROL Save Status Assignment]**。

### 编辑现有订单状态

1. 在&#x200B;_[!UICONTROL Order Status]_&#x200B;网格中，以编辑模式打开状态记录。

1. 根据需要更新状态设置。

1. 单击&#x200B;**[!UICONTROL Save Status]**。

### 从已分配状态中删除订单状态

>[!NOTE]
>
>如果状态正在使用中，则无法从状态中取消分配状态设置。

1. 在&#x200B;_[!UICONTROL Order Status]_&#x200B;网格中，找到要取消分配的订单状态记录。

1. 在该行最右侧的&#x200B;_[!UICONTROL Action]_&#x200B;列中，单击&#x200B;**[!UICONTROL Unassign]**&#x200B;链接。

   工作区顶部将显示一条消息，表明订单状态已取消分配。 尽管订单状态标签仍显示在列表中，但不再将其分配给状态。 无法删除订单状态设置。

>[!NOTE]
>
>如果默认订单状态是从订单状态中取消分配的，则&#x200B;_&#x200B;**另一个**&#x200B;_&#x200B;订单状态是&#x200B;_&#x200B;**自动设置**&#x200B;_&#x200B;作为此订单状态的默认值。

## 通知

如果配置中启用了订单RSS源，客户可以通过[RSS源](../merchandising-promotions/social-rss.md)跟踪其订单的状态。 启用后，每张订单上都会显示指向RSS馈送的链接。

### 启用订单状态通知

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧面板中，展开&#x200B;**[!UICONTROL Catalog]**&#x200B;并在下面选择&#x200B;**[!UICONTROL RSS Feeds]**。

1. 展开&#x200B;**[!UICONTROL Order]**&#x200B;部分的![扩展选择器](../assets/icon-display-expand.png)。

1. 将&#x200B;**[!UICONTROL Customer Order Status Notification]**&#x200B;设置为`Enable`。

   ![客户订单状态通知](../configuration-reference/catalog/assets/rss-feeds-order.png){width="600" zoomable="yes"}

1. 完成后，单击&#x200B;**[!UICONTROL Save Config]**。

### 配置新订单电子邮件通知

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧面板中，展开&#x200B;**[!UICONTROL Sales]**&#x200B;并在下面选择&#x200B;**[!UICONTROL Sales Emails]**。

1. 展开&#x200B;**[!UICONTROL Order]**&#x200B;部分的![扩展选择器](../assets/icon-display-expand.png)。

   ![配置 — 订单选项](../configuration-reference/sales/assets/sales-emails-order.png){width="600" zoomable="yes"}

1. 将&#x200B;**[!UICONTROL New Order Confirmation Email Sender]**&#x200B;设置为以下项之一：

   - `General Contact`
   - `Sales Representative`
   - `Customer Support`
   - `Custom Email 1`
   - `Custom Email 2`

1. 选择要用于每种客户类型的模板：

   - **[!UICONTROL New Order Confirmation Template]** — 选择一个模板以用于拥有注册商店帐户的客户。
   - **[!UICONTROL New Order Confirmation Template for Guest]** — 选择用于没有注册商店帐户的来宾客户的模板。

1. 若要将新订单通知其他人员（如业务经理），请输入电子邮件地址&#x200B;**[!UICONTROL Send Order Email Copy To]**。

   如果需要多个收件人，则可以添加多个电子邮件地址。

1. 将&#x200B;**[!UICONTROL Send Order Email Copy Method]**&#x200B;设置为以下项之一：

   - `Bcc` — 只向客户和其他收件人发送一封有关新订单的电子邮件，但客户看不到他们收到的电子邮件也发送给其他收件人。
   - `Separate Email` — 发送了两封单独的电子邮件，一封发送给收件人，一封发送给客户。

1. 完成后，单击&#x200B;**[!UICONTROL Save Config]**。

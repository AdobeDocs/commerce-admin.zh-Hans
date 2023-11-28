---
title: PayPal计费协议
description: 了解如何在您的商店中支持PayPal计费协议和支付方式。
exl-id: b0800b41-816a-4c48-a54d-41ddc1d586ce
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '791'
ht-degree: 0%

---

# PayPal计费协议

为简化结账过程，客户可与PayPal作为支付服务提供商签订账单协议。 结账时，客户选择帐单协议作为付款方式。 付款系统通过其唯一编号验证计费协议，并对客户帐户计费。 建立帐单协议后，客户不再需要为每次购买输入付款信息。 客户可以从其客户帐户的仪表板管理其计费协议，其中每个协议的状态显示为 _活动_ 或 _已取消_. 取消帐单协议后，无法重新激活该协议。

## 计费协议工作流

1. **客户注册计费协议**. 建立帐单协议后，只能从客户帐户添加其他帐单协议。 客户可创建的计费协议数量没有限制。 客户可以使用以下任意方法注册开单协议：

   - **注册客户帐户**  — 客户可以从其客户帐户注册账单协议。
   - **在结帐时注册**  — 使用PayPal Express结帐付款的客户可以标记用于创建计费协议的复选框。 尽管开单协议不适用于当前订单，但在客户下次下订单时，它可用作付款方式选项。
   - **由商店管理员注册**  — 根据客户请求，商店管理员可以使用客户帐单协议创建销售订单。

1. **PayPal验证并记录协议**. 当客户下订单并通过帐单协议付款时，帐单协议参考ID和销售订单付款详细信息将传输到PayPal并记录在客户帐户中，以及参考信息。 如果付款获得授权，将在Commerce中创建订单。 计费协议参考ID将发送给客户和商店。

## 管理帐单协议

此 _[!UICONTROL Billing Agreements]_页面列出了您的商店与其客户之间的所有计费协议。 商家可以按客户或开单协议信息过滤记录，包括开单协议参考ID、状态和创建日期。 每个记录包括有关开单协议的一般信息，以及将其用作付款方法的所有销售订单。 您可以查看、取消或删除客户开单协议。 取消的帐单协议只能由存储管理员删除。

### 查看计费协议

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Billing Agreements]**.

1. 在列表中查找计费协议，然后单击以将其打开。

每个开单协议页均由两个标签组成： _[!UICONTROL General Information]_和_[!UICONTROL Related Orders]_.

#### 一般信息

此选项卡包括有关计费协议的一般信息：

- [!UICONTROL Reference ID]：分配给当前计费协议的唯一数字标识符。
- [!UICONTROL Customer]：分配给当前计费协议的客户帐户。
- [!UICONTROL Status]：支付协议状态。
- [!UICONTROL Created At]：创建日期。
- [!UICONTROL Updated At]：更新日期。

![计费协议视图](./assets/billing-agreement-view.png){width="600" zoomable="yes"}

#### 相关订单

此标签显示使用当前开单协议下达的订单列表。

![计费协议视图](./assets/billing-agreement-related-orders.png){width="600" zoomable="yes"}

### 取消帐单协议

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Billing Agreements]**.

1. 在列表中查找计费协议，然后单击以将其打开。

1. 在右上角，单击 **[!UICONTROL Cancel]**.

1. 要确认操作，请单击 **[!UICONTROL OK]**.

### 删除帐单协议

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Billing Agreements]**.

1. 在列表中查找计费协议，然后单击以将其打开。

1. 在右上角，单击 **[!UICONTROL Delete]**.

1. 要确认操作，请单击 **[!UICONTROL OK]**.

### 列描述

| 列 | 描述 |
|--- |--- |
| [!UICONTROL ID] | 分配给每个计费协议的唯一数字标识符 |
| [!UICONTROL Email] | 客户的联系人电子邮件 |
| [!UICONTROL First Name] | 客户的名字 |
| [!UICONTROL Last Name] | 客户的姓氏 |
| [!UICONTROL Reference ID] | 分配给每个计费协议的唯一数字引用标识符 |
| [!UICONTROL Status] | 付款协议状态。 选项： `Active` 或 `Canceled` |
| [!UICONTROL Created] | 创建日期 |
| [!UICONTROL Updated] | 更新日期 |

{style="table-layout:auto"}

## 店面体验

根据协议，与付款提供商签订账单协议的客户可以现在购买产品，以后再付款。 此

![客户仪表板中的帐单协议列表](./assets/billing-agreements-dashboard.png){width="700" zoomable="yes"}

| 列 | 描述 |
|--- |--- |
| [!UICONTROL Reference ID] | 分配给每个计费协议的唯一数字引用标识符 |
| [!UICONTROL Status] | 付款协议状态。 选项： `Active` 或 `Canceled` |
| [!UICONTROL Created At] | 创建日期 |
| [!UICONTROL Updated At] | 更新日期 |
| [!UICONTROL Payment Method] | 计费协议的付款提供商 |
| [!UICONTROL View] | 用于查看开单协议的按钮 |

{style="table-layout:auto"}

### 创建计费协议

1. 客户从其帐户信息板中选择 **[!UICONTROL Billing Agreements]**.

1. 下 **[!UICONTROL New Billing Agreement]**，选择支付提供商。

1. 单击 **[!UICONTROL Create]**.

此操作可将客户重定向到付款系统网站。

![客户帐户仪表板中的新记帐协议](./assets/create-billing-agreement-dashboard.png){width="700" zoomable="yes"}

### 查看计费协议

1. 客户从其帐户信息板中选择 **[!UICONTROL Billing Agreements]**.

1. 选择帐单协议并单击 **[!UICONTROL View]**.

![在客户的仪表板中查看帐单协议](./assets/view-billing-agreement.png){width="700" zoomable="yes"}

### 取消帐单协议

1. 客户从其帐户信息板中选择 **[!UICONTROL Billing Agreements]**.

1. 选择帐单协议并单击 **[!UICONTROL View]**.

1. 在右上角，单击 **[!UICONTROL Cancel]** 然后 **[!UICONTROL OK]** 以确认。

>[!NOTE]
>
>如果管理员用户（商家）取消计费协议，则无法在店面取消该协议。 此 _已取消_ 将显示此协议的状态。

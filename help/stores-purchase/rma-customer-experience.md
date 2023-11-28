---
title: 返回店面体验
description: 了解客户如何通过店面帐户管理其产品退货。
exl-id: c276ca2c-3d8b-4019-a9aa-e7631080f331
feature: Returns, Storefront
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 1%

---

# 返回店面体验

{{ee-feature}}

客户可以使用以下任一方式从店面请求RMA：

- [订单和退货小组件](../content-design/widget-orders-returns.md) 在侧栏中
- _订单和退货_ 页脚中的链接

作为最佳实践，请确保在客户服务策略中包含RMA要求和流程的描述。

>[!NOTE]
>
>如果要收集与退货相关的其他信息，可以添加自己的自定义 [返回属性](attributes-returns.md).

所有客户RMA信息均显示在 **[!UICONTROL My Returns]** 客户帐户仪表板中的页面。

![我的退货](./assets/my-returns-page.png){width="700" zoomable="yes"}

## 请求RMA

客户在店面完成以下步骤以提交RMA：

1. 在页脚中，单击 **[!UICONTROL Orders and Returns]**.

1. 输入订单信息：

   - 订单ID
   - 帐单姓氏
   - 电子邮件

1. 点击次数 **[!UICONTROL Continue]**.

   ![订单和退货](./assets/storefront-orders-and-returns.png){width="700" zoomable="yes"}

1. 在订购日期下，单击 **[!UICONTROL Return]**.

   ![订单详细信息](./assets/storefront-orders-and-returns-order-information.png){width="700" zoomable="yes"}

1. 选择要返回的项目并输入 **[!UICONTROL Quantity to Return]**.

1. 集 **[!UICONTROL Resolution]** 更改为以下任一项：

   - Exchange
   - [退款](../customers/refunds-customer-account.md)
   - [商店点数](../customers/store-credit-using.md)

1. 集 **[!UICONTROL Item Condition]** 更改为以下任一项：

   - `Unopened`
   - `Opened`
   - `Damaged`

1. 集 **[!UICONTROL Reason to Return]** 更改为以下任一项：

   - `Wrong Color`
   - `Wrong Size`
   - `Out of Service`
   - `Other`

   ![创建新退货](./assets/storefront-orders-and-returns-create-new-return.png){width="700" zoomable="yes"}

1. 如果需要，设置 **[!UICONTROL Contact Email Address]** 和 **[!UICONTROL Comments]**.

   >[!NOTE]
   >
   >如果订单包含多个项目，而客户希望返回另一个项目，则可以单击 **[!UICONTROL Add Item To Return]**，选择项目，然后设置所有提及的选项。

1. 点击次数 **[!UICONTROL Submit]**.

---
title: 创建订单
description: 了解如何在Commerce管理员中为客户创建订单。
exl-id: 8a766a5b-55d6-4d78-859e-38937e0183d3
feature: Orders, Customer Service
TQID: https://experienceleague.adobe.com/0TUx-cDuonSkm4G0zWaU95ZKDuB-yhPb0aaEW57K-3g
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 376
ht-degree: 0%

---

# 创建订单

对于需要帮助的注册客户，您可以直接从管理员创建整个订单。 _[!UICONTROL Create New Order]_&#x200B;表单包含正常结账流程所需的所有信息，以及客户帐户信息板中的活动摘要。

![为客户创建订单](./assets/create-new-order.png){width="700" zoomable="yes"}

## 第1步：创建订单

1. 在&#x200B;_管理员_&#x200B;侧边栏上，单击&#x200B;**[!UICONTROL Customers]**。

1. 在网格中查找客户。

1. 在&#x200B;_操作_&#x200B;列中，单击&#x200B;**[!UICONTROL Edit]**。

1. 在工作区标题中，单击&#x200B;**[!UICONTROL Create Order]**。

   ![Workspace标头](./assets/order-create-buttons.png){width="700" zoomable="yes"}

   您还可以通过单击&#x200B;**[!UICONTROL Create New Order]**&#x200B;在[订单工作区](orders.md#orders-workspace)中创建订单。

## 步骤2：添加产品

如果您的商店有多个视图，请选择将要下订单的商店视图。

### 从[!UICONTROL Customer's Activities]侧栏添加产品

您可以将客户的愿望清单或任何最近查看、比较或订购的商品中的商品传输到购物车。

1. 展开![扩展选择器](../assets/icon-display-expand.png)以下部分之一：

   - **[!UICONTROL Wish List]**
   - **[!UICONTROL Last Ordered Items]**
   - **[!UICONTROL Products in Comparison List]**
   - **[!UICONTROL Recently Compared Products]**
   - **[!UICONTROL Recently Viewed Products]**

1. 选中左侧面板中每个产品的复选框。

1. 向下滚动并单击&#x200B;**[!UICONTROL Update Changes]**。

   项目会显示在订购单中。

   ![添加到购物车](./assets/create-order-add-wishlist.png){width="600" zoomable="yes"}

### 从目录添加产品

1. 单击&#x200B;**[!UICONTROL Add Products]**。

   ![添加产品](./assets/account-add-wishlist-product.png){width="600" zoomable="yes"}

1. 在网格中，选中要添加到购物车的每个产品的复选框，然后输入要购买的&#x200B;**[!UICONTROL Qty]**。

   ![选择产品](./assets/create-order-from-catalog.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >产品选择网格始终显示产品的常规基本价格，而不提供折扣以及应用的任何购物车或组价格规则。 仅当将产品添加到订单/购物车时，才计算最终产品价格。

1. 配置可用的产品选项：

   - 单击&#x200B;**[!UICONTROL Configure]**。

   - 根据需要完成选项。

   - 单击&#x200B;**[!UICONTROL OK]**。

   - 单击&#x200B;**[!UICONTROL Add Selected Product(s) to Order]**&#x200B;以更新购物车。

1. 如果为[礼品选项](../catalog/product-gift-options.md)配置了产品，请根据需要设置选项。

1. 覆盖物料价格（如有必要）：

   - 选中&#x200B;**[!UICONTROL Custom Price]**&#x200B;复选框，然后在下面的框中输入新价格。

   - 要更新购物车总计，请单击&#x200B;**[!UICONTROL Update Items and Quantities]**。

   ![自定义价格](./assets/create-order-custom-price.png){width="600" zoomable="yes"}

1. 根据订单的需要完成以下部分：

   - [!UICONTROL Order Currency]
   - [!UICONTROL Apply Coupon Codes / Gift Card Code]
   - [!UICONTROL Payment Method]
   - [!UICONTROL Shipping Method]
   - [!UICONTROL Order Comments]
   - [[!UICONTROL [自定义订单属性]]](../stores-purchase/order-processing.md#custom-order-attributes)

>[!NOTE]
>
>有关安装和配置Payment Services扩展时支持此功能的付款方法的详细信息，请参阅[付款服务指南](https://experienceleague.adobe.com/en/docs/commerce/payment-services/guide-overview)。

## 步骤3：提交订单

单击&#x200B;**[!UICONTROL Submit Order]**。

向客户发送确认，客户可以从其帐户查看订单详细信息。

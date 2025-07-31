---
title: 管理购物车
description: 了解如何直接从管理员协助客户处理其购物车。
exl-id: beb41dfa-ef87-4065-96fd-0649a5c4c21c
feature: Customer Service, Shopping Cart
source-git-commit: 69cd571b66a81159c2c99e6652907f22142568cb
workflow-type: tm+mt
source-wordcount: '746'
ht-degree: 0%

---

# 管理购物车

{{ee-feature}}

要开始辅助购物会话，客户必须从店面登录其帐户才能使信息可用。 如果客户没有帐户，您可以[创建帐户](../customers/account-create.md)。

![客户帐户中的购物车](./assets/customer-account-manage-cart-items.png){width="600" zoomable="yes"}

## 操作控制

| 选项 | 描述 |
|--- |--- |
| [!UICONTROL Remove] | 从当前购物车中删除项目 |
| [!UICONTROL Move to Wish List] | 将项目移至所选客户的愿望清单 |

{style="table-layout:auto"}

## 控制按钮

| 按钮 | 描述 |
|--- |--- |
| [!UICONTROL Clear my shopping cart] | 从购物车中删除所有项目。 |
| [!UICONTROL Update Items and Quantities|]在&#x200B;**[!UICONTROL Qty]**&#x200B;字段中输入所需的数量并更新购物车中的项目数。 |
| [!UICONTROL Add selections to my cart] | 将所有部分的产品添加到购物车。 |

{style="table-layout:auto"}

## 验证客户是否已登录

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Customers]** > **[!UICONTROL Now Online]**。

   商店的所有访客和登录的客户都会显示在列表中。

   ![客户现在联机](./assets/customers-now-online.png){width="700" zoomable="yes"}

## 优惠辅助购物

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Customers]** > **[!UICONTROL All Customers]**。

1. 在列表中，以编辑模式打开客户记录。

   >[!TIP]
   >
   >若要快速查找客户记录，请使用[筛选器](../getting-started/admin-grid-controls.md)控件。

   在&#x200B;_[!UICONTROL Personal Information]_&#x200B;下的客户配置文件中，_[!UICONTROL Last Logged In]_&#x200B;日期和时间显示客户处于在线状态。

   ![在线客户的客户个人资料](./assets/customer-account-manage-cart.png){width="600" zoomable="yes"}

1. 要进入辅助购物模式，请单击顶部按钮栏中的&#x200B;**[!UICONTROL Manage Shopping Cart]**。

   ![辅助购物模式](./assets/customer-manage-shopping-cart.png){width="600" zoomable="yes"}

## 按属性将产品添加到购物车

1. 展开![部分的](../assets/icon-display-expand.png)扩展选择器&#x200B;**[!UICONTROL Products]**。

1. 使用每列顶部的任意过滤器查找产品。

1. 单击&#x200B;**[!UICONTROL Search]**。

1. 根据产品类型，执行以下一系列步骤之一：

### 添加简单产品

1. 单击要订购的产品。

   此操作选择记录并将&#x200B;**[!UICONTROL Quantity]**&#x200B;设置为默认值`1`。

1. 如有必要，请更新订购数量。

1. 在网格的左上方，单击&#x200B;**[!UICONTROL Add selections to my cart]**。

   ![将产品添加到购物车](./assets/customer-account-manage-cart-order-products.png){width="600" zoomable="yes"}

   行项目将添加到页面顶部的购物车。

   ![购物车已更新](./assets/customer-account-manage-cart-update-cart.png){width="600" zoomable="yes"}

### 添加包含配置的产品

在添加到购物车之前必须配置三种类型的产品： `Bundle Product`、`Configurable Product`和`Grouped Product`。

1. 在网格中，单击产品名称旁边的&#x200B;**[!UICONTROL Configure]**。

   ![配置产品](./assets/customer-account-manage-cart-order-configurable-product.png){width="600" zoomable="yes"}

1. 在&#x200B;_关联产品_&#x200B;对话框中，选择每个产品选项以描述要订购的项，输入&#x200B;**[!UICONTROL Quantity]**，然后单击&#x200B;**[!UICONTROL OK]**。

   选择带有复选标记的产品，订购数量会显示在网格中。

1. 要将产品添加到购物车，请单击&#x200B;**[!UICONTROL Add selections to my cart]**。

   购物车中的![可配置产品](./assets/customer-account-manage-cart-order-configurable-product-cart.png){width="600" zoomable="yes"}

1. 根据需要更新购物车中的产品选项：

   - 单击&#x200B;**[!UICONTROL Configure]**。

   - 更新选项，然后单击&#x200B;**[!UICONTROL OK]**。

## 按SKU添加产品

1. 展开![部分的](../assets/icon-display-expand.png)扩展选择器&#x200B;**[!UICONTROL Add to Shopping Cart by SKU]**。

1. 通过&#x200B;**[!UICONTROL SKU]**&#x200B;单独添加产品，或通过上传CSV文件添加产品。

### 按SKU单独添加项目

1. 输入要订购的项的&#x200B;**[!UICONTROL SKU]**&#x200B;和&#x200B;**[!UICONTROL Qty]**。

1. 要订购其他产品，请单击&#x200B;**[!UICONTROL Add another]**。

   ![按SKU添加产品](./assets/customer-account-manage-cart-order-product-by-sku.png){width="600" zoomable="yes"}

1. 单击&#x200B;**[!UICONTROL Add selections to my cart]**。

1. 如果项目是可配置的产品，请在提示时选择产品选项，然后单击&#x200B;**[!UICONTROL Add to Shopping Cart]**。

### 通过上传CSV文件添加产品

1. 准备包含要添加到购物车的项目的[csv文件](../systems/data-csv.md)。

   文件必须只包含两列，标题中包含`sku`和`qty`。

1. 上载准备的文件：

   - 单击&#x200B;**[!UICONTROL Choose File]**。

   - 选择要从目录中上传的文件。

## 转移项目

您可以将客户愿望清单中的商品以及最近查看、比较或订购的商品传输到购物车。 每个部分中的项目数都显示在部分标题后面的括号中。

1. 展开![扩展选择器](../assets/icon-display-expand.png)以下部分之一：

   - [!UICONTROL Wish List]
   - [!UICONTROL Products in the Comparison List]
   - [!UICONTROL Recently Compared Products]
   - [!UICONTROL Recently Viewed Products]
   - [!UICONTROL Last Ordered Items]

1. 在网格中，选择要订购的每个产品并输入&#x200B;**[!UICONTROL Quantity]**。

1. 要输入可配置产品的选项，请单击&#x200B;**[!UICONTROL Configure]**&#x200B;并根据需要设置产品选项。

1. 单击&#x200B;**[!UICONTROL Add selections to my cart]**。

1. 应用一个或多个优惠券代码（如果可用）：

   - 对于&#x200B;**[!UICONTROL Apply Coupon Code]**，请输入有效的优惠券代码。

   - 单击&#x200B;_应用_ （![箭头图标](../assets/icon-apply-arrow.png) ）箭头。

1. 根据需要调整订购数量：

   - 在要调整的产品的&#x200B;**[!UICONTROL Qty]**&#x200B;列中，输入正确的金额。

   - 单击&#x200B;**[!UICONTROL Update Items and Quantities]**。

## 创建订单

1. 单击&#x200B;**[!UICONTROL Create Order]**。

   _[!UICONTROL Create New Order]_&#x200B;页面显示购物车中的商品，以及配送和付款信息。

1. 填写送货和付款信息。

1. 单击&#x200B;**[!UICONTROL Submit Order]**。

若要了解详细信息，请参阅[创建订单](customer-account-create-order.md)。

## 从购物车中删除所有项目

在辅助购物模式下，如果客户想要重新开始、添加了不正确的项目或需要在下达新订单之前清除其购物车，则从客户的购物车中删除所有项目会很有用。 这有助于确保购物车仅包含客户实际希望购买的产品。

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Customers]** > **[!UICONTROL All Customers]**。

1. 在列表中，以编辑模式打开客户记录。

1. 单击顶部按钮栏中的&#x200B;**[!UICONTROL Manage Shopping Cart]**。

1. 单击&#x200B;**[!UICONTROL Clear my shopping cart]**。

   ![清除我的购物车](./assets/customer-manage-shopping-cart-clear.png){width="600" zoomable="yes"}

1. 提示确认操作时，单击&#x200B;**[!UICONTROL OK]**。

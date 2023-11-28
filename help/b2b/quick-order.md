---
title: 快速订单
description: 了解快速订购功能并为您的客户启用。
exl-id: 7007e1b4-a64f-46fe-a235-3ca9f64e77e4
feature: B2B, Orders
source-git-commit: c94d4e8d13c32c1c1b1d37440fdb953c8527b76c
workflow-type: tm+mt
source-wordcount: '435'
ht-degree: 0%

---

# 快速订单

此 _快速订购_ 对于知道要订购产品的产品名称或SKU的客户，功能可将订购过程减少到单击几次。 您可以手动输入具有多个SKU的订单，或将其导入“快速订购”表单。 快速订购可供登录到其帐户的客户和来宾使用。 启用后， _快速订购_ 链接将显示在页面顶部的客户名称旁边。

![快速订购链接](./assets/quick-order-link.png){width="700" zoomable="yes"}

## 为您的商店启用快速订单

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在 _[!UICONTROL General]_部分，选择&#x200B;**[!UICONTROL B2B Features]**.

1. 设置 **[!UICONTROL Enable Quick Order]** 到 `Yes`.

   ![启用快速订购](./assets/quick-orders-config.png){width="600" zoomable="yes"}

1. 单击 **[!UICONTROL Save Config]**.

1. 出现提示时，单击 [缓存管理](../systems/cache-management.md) 并刷新任何无效的缓存。

## 快速订购工作流

客户可以使用以下任一方法为快速订单指定产品。

### 方法1：输入单个产品

1. 客户单击 **[!UICONTROL Quick Order]** 链接。

1. 按SKU或产品名称选择产品：

   要放置 **按SKU快速订购**，则客户会执行以下操作：

   - 进入 **[!UICONTROL SKU]**.

   - 点击次数 **[!UICONTROL Add to List]**.

     SKU显示在输入行中，产品详细信息如下。

     ![快速订单详细信息](./assets/quick-order-product-detail.png){width="600" zoomable="yes"}

   要放置 **按产品名称快速排序**，则客户会执行以下操作：

   - 输入的前几个字符 **[!UICONTROL Product Name]**.

     >[!NOTE]
     >
     >请勿使用 _输入_ 用于选择产品名称的键。

   - 出现可能的匹配项列表时，客户单击要订购的产品。

     ![单击以选择产品名称](./assets/quick-order-product-name.png){width="700" zoomable="yes"}

1. 进入 **[!UICONTROL Qty]**.

1. 使用下一输入行，根据需要重复此过程。

1. 点击次数 **[!UICONTROL Add to Cart]**.

### 方法2：输入多个产品

1. 在 **[!UICONTROL Enter Multiple SKUs]** 框中，客户执行下列操作之一：

   - 每行输入一个SKU

   - 在同一行中输入所有SKU，用逗号分隔，不带空格。

     ![输入多个SKU](./assets/quick-order-skus.png){width="600" zoomable="yes"}

1. 要将产品添加到列表，请单击 **[!UICONTROL Add to List]**.

1. 进入 **[!UICONTROL Qty]** 按列表中的每个项目排序。

   ![快速订购列表](./assets/quick-order-skus-detail.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >如果产品具有所需的选项，则系统会提示客户选择选项。 他们可以等到到达购物车以添加产品选项。

   ![选择选项](./assets/quick-order-skus-product-options.png){width="600" zoomable="yes"}

### 方法3：上传产品列表

1. 在 _[!UICONTROL Add from File]_部分，单击&#x200B;**[!UICONTROL Download Sample]**以下载订单模板。

   ![从文件添加](./assets/quick-order-skus-add-from-file.png){width="600" zoomable="yes"}

1. 打开下载的文件。

1. 使用模板添加要上传以用于快速订购列表的产品SKU。

1. 完成后，单击 **[!UICONTROL Save]**.

   ![要上载的SKU](./assets/quick-order-skus-add-from-file-sample.png){width="400" zoomable="yes"}

1. 要上传文件，请单击 **[!UICONTROL Choose]** 并从其系统中选择文件。

   项目即添加到“快速订购”列表中。

1. 准备就绪后，单击 **[!UICONTROL Add to Cart]**.

客户创建快速订单后，可以照常完成结帐。

![快速订购](./assets/quick-order-add-to-cart.png){width="700" zoomable="yes"}

---
title: 快速订单
description: 了解快速订购功能并为您的客户启用。
exl-id: 7007e1b4-a64f-46fe-a235-3ca9f64e77e4
feature: B2B, Orders
TQID: https://experienceleague.adobe.com/iwH1JStasz7KM-ECeWAvP-x4niVm-QFg4-GMw8r3SoI
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2:
  - id: f56d26ed-050b-4fb7-b29b-8e6e994e80a2
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 438
ht-degree: 0%

---

# 快速订单

“_快速订购_”功能可将订购过程减少为知道要订购产品的产品名称或SKU的客户几次点击。 您可以手动输入具有多个SKU的订单，或将其导入“快速订购”表单。 快速订购可供登录到其帐户的客户和来宾使用。 启用后，_快速订购_&#x200B;链接将显示在页面顶部的客户名称旁边。

![快速订购链接](./assets/quick-order-link.png){width="700" zoomable="yes"}

## 为您的商店启用快速订单

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧面板的&#x200B;_[!UICONTROL General]_&#x200B;部分中，选择&#x200B;**[!UICONTROL B2B Features]**。

1. 将&#x200B;**[!UICONTROL Enable Quick Order]**&#x200B;设置为`Yes`。

   ![启用快速订购](./assets/quick-orders-config.png){width="600" zoomable="yes"}

1. 单击&#x200B;**[!UICONTROL Save Config]**。

1. 出现提示时，单击[缓存管理](../systems/cache-management.md)并刷新任何无效的缓存。

## 快速订购工作流

客户可以使用以下任一方法为快速订单指定产品。

### 方法1：输入单个产品

1. 客户单击&#x200B;**[!UICONTROL Quick Order]**&#x200B;链接。

1. 按SKU或产品名称选择产品：

   要通过SKU **快速下单**，客户将执行以下操作：

   - 进入&#x200B;**[!UICONTROL SKU]**。

   - 单击&#x200B;**[!UICONTROL Add to List]**。

     SKU显示在输入行中，产品详细信息如下。

     ![快速订单详细信息](./assets/quick-order-product-detail.png){width="600" zoomable="yes"}

   若要按产品名称&#x200B;**快速下单**，客户将执行以下操作：

   - 输入&#x200B;**[!UICONTROL Product Name]**&#x200B;的前几个字符。

     >[!NOTE]
     >
     >请勿使用&#x200B;_Enter_&#x200B;键选择产品名称。

   - 出现可能的匹配项列表时，客户单击要订购的产品。

     ![单击选择产品名称](./assets/quick-order-product-name.png){width="700" zoomable="yes"}

1. 进入&#x200B;**[!UICONTROL Qty]**。

1. 使用下一输入行，根据需要重复此过程。

1. 单击&#x200B;**[!UICONTROL Add to Cart]**。

### 方法2：输入多个产品

1. 在&#x200B;**[!UICONTROL Enter Multiple SKUs]**&#x200B;框中，客户执行以下操作之一：

   - 每行输入一个SKU

   - 在同一行中输入所有SKU，用逗号分隔，不带空格。

     ![输入多个SKU](./assets/quick-order-skus.png){width="600" zoomable="yes"}

1. 要将产品添加到列表，请单击&#x200B;**[!UICONTROL Add to List]**。

1. 输入要为列表中的每个项排序的&#x200B;**[!UICONTROL Qty]**。

   ![快速订购列表](./assets/quick-order-skus-detail.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >如果产品具有所需的选项，则系统会提示客户选择选项。 他们可以等到到达购物车以添加产品选项。

   ![选择选项](./assets/quick-order-skus-product-options.png){width="600" zoomable="yes"}

### 方法3：上传产品列表

1. 在&#x200B;_[!UICONTROL Add from File]_&#x200B;部分中，单击&#x200B;**[!UICONTROL Download Sample]**&#x200B;以下载订单模板。

   ![从文件添加](./assets/quick-order-skus-add-from-file.png){width="600" zoomable="yes"}

1. 打开下载的文件。

1. 使用模板添加要上传以用于快速订购列表的产品SKU。

1. 完成后，单击&#x200B;**[!UICONTROL Save]**。

   要上载的![SKU](./assets/quick-order-skus-add-from-file-sample.png){width="400" zoomable="yes"}

1. 要上传文件，请单击&#x200B;**[!UICONTROL Choose]**&#x200B;并从其系统中选择文件。

   项目即添加到“快速订购”列表中。

1. 准备就绪后，单击&#x200B;**[!UICONTROL Add to Cart]**。

客户创建快速订单后，可以照常完成结帐。

![快速订购](./assets/quick-order-add-to-cart.png){width="700" zoomable="yes"}

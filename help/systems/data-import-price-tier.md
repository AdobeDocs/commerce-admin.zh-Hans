---
title: 导入层价格
description: 了解如何导出层定价数据和导入更新的数据。
exl-id: b19d0208-68b3-45ba-9896-318e12ff4131
feature: Products, Data Import/Export
source-git-commit: 55b0672984ce8cdb853daf024299919beaf7ce0b
workflow-type: tm+mt
source-wordcount: '341'
ht-degree: 0%

---

# 导入层价格

不要输入 [层价格](../catalog/product-price-tier.md) 手动选择每种产品可以更有效 [导入](data-import.md) 定价数据。 在开始之前，请创建一个导出层价格数据的样例文件，以将其用作模板。

![示例店面 — 分层定价](./assets/storefront-tier-pricing-water-bottle.png){width="700" zoomable="yes"}

## 步骤1：导出层价格数据

以下示例导出单个产品的层定价数据。 然后，您可以使用导出的数据作为批量导入层价格数据的模板。 要了解有关导出高级定价数据的更多信息，请参阅 [高级定价数据](data-attributes-product.md#advanced-pricing-attributes).

![产品分层定价](./assets/price-tier-customer-group-discount.png){width="600" zoomable="yes"}

1. 开启 _管理员_ 侧栏，转到  **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Export]**.

1. 下 _[!UICONTROL Export Settings]_，设置&#x200B;**[!UICONTROL Entity Type]**到 `Advanced Pricing`.

1. 在 **[!UICONTROL Entity Attributes]** 网格，向下滚动到SKU属性并执行以下操作：

   - 对于基于折扣百分比的层价格，输入要导出的每个产品的SKU，以逗号分隔。

     ![数据导出 — 产品SKU](./assets/price-tier-export-sku.png){width="600" zoomable="yes"}

   - 对于基于固定金额的层价格，请输入每个产品的SKU。

   - 向下滚动并单击 **[!UICONTROL Continue]**.

1. 在Web浏览器的下载位置找到导出文件，然后打开该文件。

   ![示例 — 导出的客户组折扣层价格数据](./assets/price-tier-customer-group-discount-export.png){width="600" zoomable="yes"}

**_导出的层价格数据_**

导出的数据中包含以下列：

- `sku`
- `tier_price_website`
- `tier_price_customer_group`
- `tier_price_qty`
- `tier_price`
- `tier_price_value_type`

您可以使用导出的数据作为模板来导入层价格数据。

## 步骤2：更新数据

1. 根据需要更新每个产品的层价格数据。

   任何没有层价格更新的产品都可以从CSV文件删除。 无需重新导入未更改的产品。

1. **[!UICONTROL Save]** 更新的CSV文件。

>[!NOTE]
>
>导入文件的大小不能大于2 MB。

## 步骤3：导入更新的数据

1. 开启 _管理员_ 侧栏，转到 **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Import]**.

1. 下 _导入设置_，设置 **[!UICONTROL Entity Type]** 到 `Advanced Pricing`.

1. 设置 **[!UICONTROL Import Behavior]** 到 `Add/Update`.

1. 下 **[!UICONTROL File to Import]**，单击 **[!UICONTROL Choose File]** 并选择您准备从目录导入的文件。

1. 在右上角，单击 **[!UICONTROL Check Data]**.

1. 如果文件有效，请单击 **[!UICONTROL Import]**.

   否则，请纠正消息中列出的数据存在的每个问题，然后再次尝试导入文件。

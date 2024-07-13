---
title: 按SKU排序
description: 了解如何配置您的商店，以便支持为方便客户而通过SKU进行订购。
exl-id: cb39554f-ab76-46d5-8217-e43bc8f9f88d
feature: Orders, Storefront, Configuration
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '586'
ht-degree: 0%

---

# 按SKU排序

{{ee-feature}}

“SKU”是“库存单位”。 SKU通常可帮助在线销售商识别最重要的产品特征，例如：尺寸、颜色、价格和材质。 产品ID与SKU不同：

- `Product ID`是内部用于标识产品的连续数字系列，客户无法查看。
- `SKU`由卖方生成，通常基于产品名称和属性进行营销或内部跟踪。 例如：蓝色棉色T恤，中号：T-COT-MED-BL。 如有必要，卖方可以更改SKU。

通常，SKU包括一组缩写，用于指示产品的区别特征。 最大SKU长度为64个字符。 SKU对于有效跟踪和管理库存非常重要，因此正确设置它们对于电子商务至关重要。

_Order by SKU_&#x200B;是一个[小组件](../content-design/widgets.md)，可在商店中显示以方便所有购物者，或仅提供给特定客户群中的购物者。 购物者可以将SKU和数量信息直接输入到“按SKU排序”块中，也可以从其客户帐户上传csv文件。 无论配置如何，存储管理员始终可以按SKU排序。

![在店面中按SKU订购](./assets/storefront-order-by-sku.png){width="700" zoomable="yes"}

## 按SKU配置订单

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧面板中，展开&#x200B;**[!UICONTROL Sales]**&#x200B;部分并在下面选择&#x200B;**[!UICONTROL Sales]**。

1. 展开&#x200B;**[!UICONTROL Order by SKU Settings]**&#x200B;部分的![扩展选择器](../assets/icon-display-expand.png)。

1. 将&#x200B;**[!UICONTROL Enable Order by SKU on my Account in Storefront]**&#x200B;设置为以下项之一：

   - `Yes, for Everyone` - Order by SKU块在商店中可供每位购物者使用。
   - `Yes, for Specified Customer Groups` - Order by SKU仅适用于特定客户组（如`Wholesale`）的成员。
   - `No` - Order by SKU块未出现在店面中，Order by SKU页面在客户帐户中不可用。

   ![按SKU设置排序](../configuration-reference/sales/assets/sales-order-by-sku-settings.png){width="600" zoomable="yes"}

1. 单击&#x200B;**[!UICONTROL Save Config]**。

![Adobe Commerce B2B](../assets/b2b.svg)(仅限Adobe Commerce B2B) _**要启用“按SKU排序”功能，请禁用“快速排序”功能：**_

1. 转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧面板中的&#x200B;_[!UICONTROL General]_下，选择&#x200B;**[!UICONTROL B2B Features]**

1. 展开&#x200B;**[!UICONTROL B2B Features]**&#x200B;部分的![扩展选择器](../assets/icon-display-expand.png)。

1. 将&#x200B;**[!UICONTROL Enable Quick Order]**&#x200B;设置为`No`。

   [快速订购功能](../b2b/quick-order.md)允许客户和来宾根据SKU或产品名称快速下订单。

## 店面体验

为商店配置功能后，客户可以从任何包含&#x200B;_按SKU订购_&#x200B;小组件的页面或其帐户仪表板中按SKU订购。

### 按页面块中的SKU排序

1. 在&#x200B;_Order by SKU_&#x200B;块中，客户输入要订购项目的&#x200B;**[!UICONTROL SKU]**&#x200B;和&#x200B;**[!UICONTROL Qty]**。

1. 要添加另一项，请单击&#x200B;**[!UICONTROL Add Row]**&#x200B;并重复该过程。

1. 单击&#x200B;**[!UICONTROL Add to Cart]**。

### 按客户帐户的SKU排序

1. 客户从店面登录到他们的帐户。

1. 在左侧的面板中，选择&#x200B;**[!UICONTROL Order by SKU]**。

1. 根据首选项添加单个项目：

   _**按SKU添加每个项：**_

   - 输入要订购的项的&#x200B;**[!UICONTROL SKU]**&#x200B;和&#x200B;**[!UICONTROL Qty]**。

   - 若要根据需要添加其他项目，请单击&#x200B;_添加行_ ![加号按钮](../assets/button-add-item.png)并根据需要重复添加任意数量的项目。

   - 单击&#x200B;**[!UICONTROL Add to Cart]**。

   _**上载包含多个项目的CSV文件：**_

   - 准备一个[导入数据CSV](../systems/data-csv.md) （逗号分隔值）文件，该文件包含`SKU`和`Qty`的列。

   要导入的![SKU](./assets/account-dashboard-order-by-sku-import.png){width="500" zoomable="yes"}

   - 要上传CSV文件，请单击&#x200B;**[!UICONTROL Choose File]**&#x200B;并选择要上传的文件。

   - 单击&#x200B;**[!UICONTROL Add to Cart]**。

   如果有任何产品具有其他选项，则会从购物车中提示客户需要关注该产品。

   ![产品需要注意](./assets/account-dashboard-order-by-sku-cart-product-requires-attention.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >如果存在重复的SKU，则数量将合并到购物车中的一个行项目中。 客户可以更改任何项目的数量，然后单击&#x200B;**[!UICONTROL Update Shopping Cart]**&#x200B;重新计算总计。


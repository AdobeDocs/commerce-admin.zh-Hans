---
title: 虚拟产品
description: 了解如何创建表示无形项目的虚拟产品，如会员资格、服务、保修或订阅。
exl-id: 8788ba04-e911-429e-9e48-ce589f0c9fa1
feature: Catalog Management, Products
source-git-commit: 4a3aa2aa32b692341edabd41fdb608e3cff5d8e0
workflow-type: tm+mt
source-wordcount: '645'
ht-degree: 0%

---

# 虚拟产品

虚拟产品或数字商品是指无形项目，如会员资格、服务、保修或书籍、音乐、视频或其他产品的订阅和数字下载。 虚拟产品可以单独销售，也可以作为[分组产品](product-create-grouped.md)、[可配置产品](product-create-configurable.md)或[捆绑产品](product-create-bundle.md)产品类型的一部分包含在内。

除了缺少&#x200B;_[!UICONTROL Weight]_&#x200B;字段之外，创建虚拟产品和简单产品的过程是相同的。 以下说明演示了使用[产品模板](attribute-sets.md)、必填字段和基本设置创建虚拟产品的过程。 完成基础知识后，您可以根据需要完成其他产品设置。

>[!NOTE]
>
>PayPal不再支持通过PayPal Express Checkout销售数字商品。 他们建议您使用[PayPal Payments Standard](../stores-purchase/paypal-payments-standard.md)或任何其他PayPal支付网关来处理包含虚拟产品的任何订单。

![虚拟产品](./assets/product-virtual-membership.png){width="700" zoomable="yes"}

## 步骤1：选择产品类型

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Catalog]** > **[!UICONTROL Products]**。

1. 在右上角的&#x200B;_[!UICONTROL Add Product]_（![菜单箭头](../assets/icon-menu-down-arrow-red.png){width="25"} ）菜单中，选择&#x200B;**[!UICONTROL Virtual Product]**。

   ![添加虚拟产品](./assets/product-add-virtual.png){width="700" zoomable="yes"}

## 步骤2：选择属性集

要选择用作产品模板的[属性集](attribute-sets.md)，请执行以下操作之一：

- 单击&#x200B;**[!UICONTROL Attribute Set]**&#x200B;字段并输入属性集的全部或部分名称。

- 在显示的列表中，选择要使用的属性集。

将更新表单以反映更改。

![选择属性集](./assets/product-create-choose-attribute-set.png){width="600" zoomable="yes"}

## 第3步：完成所需的设置

1. 输入&#x200B;**[!UICONTROL Product Name]**。

1. 接受基于产品名称的默认&#x200B;**[!UICONTROL SKU]**&#x200B;或输入其他名称。

1. 输入产品&#x200B;**[!UICONTROL Price]**。

1. 由于产品尚未准备好发布，请将&#x200B;**[!UICONTROL Enable Product]**&#x200B;设置为`No`。

1. 单击&#x200B;**[!UICONTROL Save]**&#x200B;并继续。

   保存产品后，[商店视图](introduction.md#product-scope)选择器将显示在左上角。

1. 选择要提供产品的&#x200B;**[!UICONTROL Store View]**。

   ![选择商店视图](./assets/product-create-store-view-choose.png){width="600" zoomable="yes"}

## 步骤4：完成基本设置

1. 将&#x200B;**[!UICONTROL Tax Class]**&#x200B;设置为以下项之一：

   - `None`
   - `Taxable Goods`

1. 输入有库存的产品的&#x200B;**[!UICONTROL Quantity]**，并执行以下操作：

   - 接受&#x200B;**[!UICONTROL Stock Status]**&#x200B;的默认`In Stock`设置。

     由于虚拟产品未发货，因此未使用&#x200B;**[!UICONTROL Weight]**&#x200B;字段。

   - 接受&#x200B;**[!UICONTROL Visibility]**&#x200B;的默认`Catalog, Search`设置。

   >[!NOTE]
   >
   >如果启用[Inventory management](../inventory-management/introduction.md)，则单个来源商家将设置此部分中的数量。 多源商家在“来源”部分中添加来源和数量。 请参阅以下&#x200B;_分配来源和数量(Inventory management)_&#x200B;部分。

1. 要将&#x200B;**[!UICONTROL Categories]**&#x200B;分配给产品，请单击&#x200B;**[!UICONTROL Select…]**&#x200B;框并执行以下任一操作：

   **选择现有类别**：

   - 在框中开始键入，直到找到匹配项为止。

   - 选中要分配的类别的复选框。

   **创建类别**：

   - 单击&#x200B;**[!UICONTROL New Category]**。

   - 输入&#x200B;**[!UICONTROL Category Name]**&#x200B;并选择&#x200B;**[!UICONTROL Parent Category]**&#x200B;以确定其在菜单结构中的位置。

   - 单击&#x200B;**[!UICONTROL Create Category]**。

   可能有其他单个属性用于描述产品。 选择因属性集而异，您可以稍后完成它们。

### 分配来源和数量([!DNL Inventory Management])

{{$include /help/_includes/inventory-assign-sources.md}}

## 第5步：完成产品信息

根据需要完成以下部分中的信息：

- [内容](product-content.md)
- [图像和视频](product-images-and-video.md)
- [搜索引擎优化](product-search-engine-optimization.md)
- [相关产品、向上销售和交叉销售](related-products-up-sells-cross-sells.md)
- [可自定义的选项](settings-advanced-custom-options.md)
- [网站中的产品](settings-basic-websites.md)
- [设计](settings-advanced-design.md)
- [礼品选项](product-gift-options.md)

>[!NOTE]
>
>默认情况下，_[!UICONTROL Is this downloadable product?]_&#x200B;选项处于禁用状态。 为虚拟产品启用此功能可使产品[可下载](product-create-downloadable.md#downloadable-product)。

## 步骤6：发布产品

1. 如果您已准备好发布目录中的产品，请将&#x200B;**[!UICONTROL Enable Product]**&#x200B;设置为`Yes`。

1. 执行以下操作之一：

   - **方法1：**&#x200B;保存并预览

      - 单击右上角的&#x200B;**[!UICONTROL Save]**。

      - 要查看您商店中的产品，请在&#x200B;**[!UICONTROL Customer View]**&#x200B;管理员&#x200B;_（_&#x200B;菜单箭头![ ）菜单上选择](../assets/icon-menu-down-arrow-black.png)。

     该存储将在新的浏览器选项卡中打开。

     ![客户视图](./assets/product-admin-customer-view.png){width="600" zoomable="yes"}

   - **方法2：**&#x200B;保存并关闭

     在&#x200B;_[!UICONTROL Save]_（![菜单箭头](../assets/icon-menu-down-arrow-red.png){width="25"} ）菜单中，选择&#x200B;**[!UICONTROL Save & Close]**。

## 注意事项

- 虚拟产品用于无形产品，如服务、订购和保修。

- 虚拟产品与简单产品非常相似，只是没有重量。

- 除非购物车中有实际产品，否则在结账期间不会显示送货选项。

<!-- Last updated from includes: 2023-05-19 17:14:58 -->

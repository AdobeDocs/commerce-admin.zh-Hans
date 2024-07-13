---
title: 礼品卡产品
description: 了解如何创建礼品卡产品，该产品会生成一个唯一代码，以供收件人客户在结账时兑换。
exl-id: bc4b60fe-10b3-4d17-85ce-35c2720c90a2
feature: Catalog Management, Products, Gift
source-git-commit: e72977596c4479d2e94b1e066ee166d22cb12405
workflow-type: tm+mt
source-wordcount: '962'
ht-degree: 0%

---

# 礼品卡产品

{{ee-feature}}

每个礼品卡都有一个唯一代码，在结账时只能由一位客户兑换。 必须先建立[代码池](../stores-purchase/product-gift-card-accounts.md#step-3-establish-the-gift-card-code-pool)，然后才能销售礼品卡。 请参阅[礼品卡工作流程](../stores-purchase/product-gift-card-workflow.md)，以了解如何在购物车中兑换礼品卡。

![礼品卡产品页](./assets/storefront-giftcard-product-page.png){width="700" zoomable="yes"}

礼品卡产品有三种：

- **虚拟** — 将虚拟礼品卡发送到收件人的电子邮件地址，在购买礼品卡时需要此地址。 送货地址不是必需的。

- **实际** — 实际礼品卡已发往接收者的地址，这是购买礼品卡时必需的。

- **组合** — 组合礼品卡已发运，并通过电子邮件发送给收件人。 购买礼品卡时需要收件人的电子邮件和送货地址。

## 创建礼品卡产品

以下说明演示了使用[产品模板](attribute-sets.md)、必填字段和基本设置创建礼品卡的过程。 每个必填字段都标有红色星号(`*`)。 完成基础知识后，您可以根据需要完成其他产品设置。

### 步骤1：选择产品类型

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Catalog]** > **[!UICONTROL Products]**。

1. 在&#x200B;_[!UICONTROL Add Product]_的右上角(![菜单箭头](../assets/icon-menu-down-arrow-red.png){width="25"}  )菜单，选择&#x200B;**[!UICONTROL Gift Card]**。

   ![添加礼品卡](./assets/product-add-gift-card.png){width="700" zoomable="yes"}

### 步骤2：选择属性集

您可以使用默认的`Gift Card`属性集或选择其他属性集。 要选择用作产品模板的属性集，请执行下列操作之一：

- 单击&#x200B;**[!UICONTROL Attribute Set]**&#x200B;字段并输入属性集的全部或部分名称。

- 在显示的列表中，选择要使用的属性集。

![选择属性集](./assets/product-create-choose-attribute-set-gift-card.png){width="600" zoomable="yes"}

### 第3步：完成所需的设置

1. 输入礼品卡的&#x200B;**[!UICONTROL Product Name]**。

   您还可以在名称中指明礼品卡的类型。 例如，_Luma虚拟礼品卡_。

1. 输入产品的&#x200B;**[!UICONTROL SKU]**。

   默认情况下，产品名称用作默认SKU。

1. 将&#x200B;**[!UICONTROL Card Type]**&#x200B;设置为以下项之一：

   - `Virtual` — 虚拟礼品卡通过电子邮件发送给收件人。
   - `Physical` — 实体礼品卡可以提前批量生产并使用唯一代码进行浮雕。
   - `Combined` — 组合礼品卡具有虚拟和物理礼品卡的特征。

   ![礼品卡类型](./assets/product-create-gift-card-type.png){width="600" zoomable="yes"}

1. 若要为客户选择固定金额，请单击&#x200B;**[!UICONTROL Add Amount]**&#x200B;并输入卡片第一个固定值作为小数。

   要输入固定金额的选择，请为每个重复此步骤。

1. 为了让客户能够设置礼品卡的值，请执行以下操作：

   - 将&#x200B;**[!UICONTROL Open Amount]**&#x200B;设置为`Yes`。

   - 要定义可接受的最小值和最大值的范围，请输入&#x200B;**[!UICONTROL Open Amount From]**&#x200B;和&#x200B;**[!UICONTROL To]**&#x200B;值。

   您可以创建具有固定定价和/或未结金额定价的礼品卡。

   >[!NOTE]
   >
   >礼品卡产品在目录中没有自己的价格。 礼品卡价格由采购期间选定的礼品卡金额得出。

   ![礼品卡金额](./assets/product-create-gift-card-amounts.png){width="600" zoomable="yes"}

### 步骤4：完成基本设置

1. 对于实际或组合礼品卡，输入库存中的&#x200B;**[!UICONTROL Quantity]**。

1. 如果要发运的礼品卡，请输入包装的&#x200B;**[!UICONTROL Weight]**。

1. 在&#x200B;**[!UICONTROL Categories]**&#x200B;字段中，选择`Gift Card`。

可能有其他单个属性用于描述产品。 所选内容会改变属性集，您可以稍后完成它们。

### 步骤5：填写礼品卡信息

产品设置的&#x200B;_[!UICONTROL Gift Card Information]_部分可用于覆盖用于确定如何管理礼品卡的[礼品卡配置](../configuration-reference/sales/gift-cards.md)设置。

1. 向下滚动到&#x200B;_[!UICONTROL Gift Card Information]_部分。

   此部分中的默认设置由系统配置决定。

   ![礼品卡信息](./assets/product-gift-card-information.png){width="600" zoomable="yes"}

1. 根据您希望礼品卡正常工作的方式更改其他字段：

   - **[!UICONTROL Treat Balance as Store Credit]** — 确定礼品卡持有者是否可以将余额兑换为商店信用。

   - **[!UICONTROL Lifetime (days)]** — 确定购买后到礼品卡过期的天数。 如果您不想为信息卡的生命周期设置限制，请将此字段留空。

   - **[!UICONTROL Allow Message]** — 确定礼品卡的购买者是否可以为收件人输入消息。 虚拟（通过电子邮件）和实体（已发货）礼品卡均可包含礼品消息。

   - **[!UICONTROL Email Template]** — 确定用于发送给礼品卡收件人的通知的电子邮件模板。

### 步骤6：完成产品信息

根据需要完成以下部分中的信息：

- [内容](product-content.md)
- [图像和视频](product-images-and-video.md)
- [相关产品、向上销售和交叉销售](related-products-up-sells-cross-sells.md)
- [搜索引擎优化](product-search-engine-optimization.md)
- [可自定义的选项](settings-advanced-custom-options.md)
- [网站中的产品](settings-basic-websites.md)
- [设计](settings-advanced-design.md)
- [礼品选项](product-gift-options.md)

### 步骤7：Publish产品

1. 如果您已准备好发布目录中的产品，请将&#x200B;**启用产品**&#x200B;开关设置为`Yes`。

1. 执行以下操作之一：

   **方法1：**&#x200B;保存并预览

   - 单击右上角的&#x200B;**[!UICONTROL Save]**。

   - 要查看您商店中的产品，请在&#x200B;_管理员_ （![菜单箭头](../assets/icon-menu-down-arrow-black.png) ）菜单上选择&#x200B;**[!UICONTROL Customer View]**，

   ![客户视图](./assets/product-admin-customer-view.png){width="600" zoomable="yes"}

   **方法2：**&#x200B;保存并关闭

   在&#x200B;_[!UICONTROL Save]_（![菜单箭头](../assets/icon-menu-down-arrow-red.png){width="25"} ）菜单中，选择&#x200B;**[!UICONTROL Save & Close]**。

## 注意事项

- 必须先生成唯一编号的&#x200B;_代码池_，然后才能提供礼品卡销售。

- 礼品卡可设置为`Redeemable`或`Non-Redeemable`。

- 在礼品卡购买期间，未对礼品卡征税&#x200B;**__**。 只有当购买的礼品卡用于购买产品时，才会对产品征税。

- 礼品卡的存留期可以不受限制，也可以设置为指定的天数。

- 礼品卡的值可以设置为固定金额，也可以设置为具有最小值和最大值的未结金额。

- 礼品卡产品在目录中没有自己的价格。 礼品卡价格由采购期间选定的礼品卡金额得出。

- 可以在下订单时或开票时为客户创建礼品卡帐户。

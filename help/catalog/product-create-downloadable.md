---
title: 可下载的产品
description: 了解如何创建可作为数字文件交付的可下载产品。
exl-id: c3dd4c5f-adc1-4a8f-a9da-7f0dedd1ee34
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '1619'
ht-degree: 0%

---

# 可下载的产品

可下载的产品可以是任何可以作为文件提供的产品，例如电子书、音乐、视频、软件应用程序或更新。 您可以提供专辑进行销售，并单独销售每首歌曲。 您还可以使用可下载的产品来交付产品目录的电子版本。

由于下载在购买之后才可用，因此您可以提供示例，例如书籍中的摘录、音频文件中的剪辑或视频中的预告片。 示例是客户在购买产品之前可以尝试的东西。 可供下载的文件可以上载到您的服务器或从其他服务器上载。

![可下载的产品](./assets/storefront-product-downloadable.png){width="700" zoomable="yes"}

可下载的产品可以配置为要求客户登录到帐户以接收链接，也可以通过电子邮件发送并与他人共享。 下载可用之前的订单状态，在配置中设置默认值和其他提交选项。 在计划可下载的目录添加时，请注意以下事项：

- 可下载的产品可以上传到服务器，也可以从Internet上的其他服务器链接到。

- 您可以确定客户下载产品的次数。

- 购买可下载产品的客户可能需要先登录，然后才能结帐。

- 当订单位于以下任一位置时，可以交付可下载的产品 `Pending` 或 `Invoiced` 状态。

- 由于可下载产品尚未发货，因此 _配送_ 当购物车仅包含可下载的产品时，会跳过结帐步骤。


## 配置下载选项

可下载配置设置可确定可下载产品的默认值和交付选项，并指定来宾是否可以购买下载。

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中，展开 **[!UICONTROL Catalog]** 并选择 **[!UICONTROL Catalog]** 下方。

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 _[!UICONTROL Downloadable Product Options]_部分。

   ![可下载的产品选项](../configuration-reference/catalog/assets/catalog-downloadable-product-options.png){width="700" zoomable="yes"}

   有关这些配置选项的详细列表，请参见 [_可下载的产品选项_](../configuration-reference/catalog/catalog.md#downloadable-product-options) 在 _配置引用_.

1. 要确定下载可用时订购流程的状态，请设置 **[!UICONTROL Order Item Status to Enable Downloads]** 更改为以下任一项：

   - `Pending`
   - `Invoiced`

1. 要设置单个客户可进行的下载次数的默认限制，请输入以下数字： **[!UICONTROL Default Maximum Number of Downloads]**.

1. 设置 **[!UICONTROL Shareable]** 更改为以下任一项：

   - `Yes`  — 允许客户通过电子邮件将下载链接发送给其他人。
   - `No`  — 通过要求客户登录其帐户以访问下载链接，阻止客户与其他人共享下载链接。

1. 对象 **[!UICONTROL Default Sample Title]**，输入要显示在样本选择上方的标题。

   ![示例标题](./assets/product-downloadable-config-sample-title.png){width="400"}

1. 对象 **[!UICONTROL Default Link Title]**，输入要用于下载链接的默认文本。

1. 如果希望下载链接在新的浏览器窗口中打开，请设置 **[!UICONTROL Opens Links in New Window]** 到 `Yes`.

   此设置用于保持商店的浏览器窗口处于打开状态。

1. 要确定可下载内容的交付方式，请设置 **[!UICONTROL Use Content Disposition]** 更改为以下任一项：

   - `Attachment`  — 通过电子邮件将下载链接作为附件发送。
   - `Inline`  — 将下载链接作为网页上的链接交付。

1. 如果您希望要求购买者在购买下载之前注册客户帐户并登录，请设置 **[!UICONTROL Disable Guest Checkout if Cart Contains Downloadable Items]** 到 `Yes`.

1. 完成后，单击 **[!UICONTROL Save Config]**.

## 创建可下载的产品

下面的说明演示了使用创建可下载产品的过程。 [产品模板](attribute-sets.md)、必填字段和基本设置。 每个必填字段都标有红色星号(`*`)。 完成基础知识后，您可以根据需要完成其他产品设置。

>[!NOTE]
>
>可下载的文件名可包含字母和数字。 可以使用短划线或下划线字符来表示单词之间的空格。 文件名中的任何无效字符都将替换为下划线。

### 步骤1：选择产品类型

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. 在 _[!UICONTROL Add Product]_( ![菜单箭头](../assets/icon-menu-down-arrow-red.png){width="25"} )菜单，然后选择 `Downloadable Product`.

   ![添加可下载的产品](./assets/product-add-downloadable.png){width="700" zoomable="yes"}

### 步骤2：选择属性集

示例数据包括 [属性集](attribute-sets.md) 已调用 _可下载_ 具有可下载产品的特殊字段。 您可以使用现有模板或在保存产品之前创建另一个模板。

要选择用作产品模板的属性集，请执行下列操作之一：

- 对象 **[!UICONTROL Search]**，输入属性集的名称。

- 在列表中，选择 `Downloadable` 属性集。

将更新表单以反映更改。

![选择属性集](./assets/product-create-choose-attribute-set-downloadable.png){width="600" zoomable="yes"}

### 第3步：完成所需的设置

1. 输入 **[!UICONTROL Product Name]**.

1. 接受默认值 **[!UICONTROL SKU]** 基于产品名称或输入其他名称。

1. 输入产品 **[!UICONTROL Price]**.

1. 由于产品尚未准备好发布，请设置 **[!UICONTROL Enable Product]** 到 `No`.

1. 单击 **[!UICONTROL Save]** 并继续。

   保存产品后， [商店视图](introduction.md#product-scope) 选择器显示在左上角。

1. 选择 **[!UICONTROL Store View]** 在产品可用的位置。

   ![选择商店视图](./assets/product-create-store-view-choose.png){width="600" zoomable="yes"}

### 步骤4：完成基本设置

1. 设置 **[!UICONTROL Tax Class]** 更改为以下任一项：

   - `None`
   - `Taxable Goods`

1. 输入 **[!UICONTROL Quantity]** 有库存的产品的ID。

   请注意以下事项：

   - 默认情况下， **[!UICONTROL Stock Status]** 设置为 `Out of Stock`.

   - 由于可下载产品尚未发货，因此 **[!UICONTROL Weight]** 未使用字段。 如果启用此功能，它将变为 [简单产品](product-create-simple.md) 和 _此产品是否可下载？_ 制表符无法使用。

   >[!NOTE]
   >
   >如果您启用 [Inventory management](../inventory-management/introduction.md)，单一来源商家可设置此部分中的数量。 多源商家在“源”部分中添加源和数量。 请参阅以下内容 _分配来源和数量(Inventory management)_ 部分。

1. 接受默认值 **[!UICONTROL Visibility]** 设置 `Catalog, Search`.

1. 要在中突出显示该产品，请执行以下操作 [新产品列表](../content-design/widget-new-products-list.md)，选择 **[!UICONTROL Set Product as New]** 复选框。

1. 要分配 _[!UICONTROL Categories]_对于产品，单击&#x200B;**[!UICONTROL Select…]**框并执行以下任一操作：

   **选择现有类别**：

   - 在框中开始键入，直到找到匹配项为止。

   - 选中要分配的每个类别的复选框。

   **创建类别**：

   - 单击 **[!UICONTROL New Category]**.

   - 输入 **[!UICONTROL Category Name]** 并选择 **[!UICONTROL Parent Category]**，确定它在 [菜单结构](category-root.md).

   - 单击 **[!UICONTROL Create Category]**.

1. 设置 **[!UICONTROL Format]** 更改为以下任一项：

   - `Download`
   - `DVD`

   如有必要，您可以编辑 [属性](attribute-product-create.md) 以添加更多值。

   可能有其他属性用于描述产品。 选择因属性集而异，您可以稍后完成它们。

#### 分配来源和数量([!DNL Inventory Management])

{{$include /help/_includes/inventory-assign-sources.md}}

### 步骤5：完成可下载的信息

向下滚动，展开 ![扩展选择器](../assets/icon-display-expand.png) 该 _[!UICONTROL Downloadable Information]_部分，然后选择&#x200B;**[!UICONTROL Is this downloadable product?]**复选框。

启用后， _[!UICONTROL Downloadable Information]_部分包含两部分。 第一部分描述了每个下载链接，第二部分描述了每个示例文件。 其中许多选项的缺省值可在 [配置](#configure-the-download-options).

![可下载的信息](./assets/product-downloadable-information.png){width="600" zoomable="yes"}

#### 完成链接

1. 在 _[!UICONTROL Links]_部分，输入&#x200B;**[!UICONTROL Title]**要用作下载链接的标题的位置。

1. 如果适用，请选择 **[!UICONTROL Links can be purchased separately]** 复选框。

1. 单击 **[!UICONTROL Add Link]** 并执行以下操作：

   - 输入 **[!UICONTROL Title]** 和 **[!UICONTROL Price]** 下载的。

   - 对于两者 **[!UICONTROL File]** 和 **[!UICONTROL Sample]** 文件，选择下列分发方法之一进行下载：

      - `Upload File`  — 选择此方法以将分发文件上载到服务器。 浏览到文件并选择要上传的文件。
      - `URL`  — 选择此方法可从URL访问分发文件。 输入下载文件的完整URL。

   >[!NOTE]
   >
   >不能将指向外部资源的链接用作可下载的产品。 有效的链接域在中以编程方式预定义 `env.php` 文件(请参阅 [env.php参考](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/files/config-reference-envphp.html) 在 _配置指南_)。

   - 设置 **[!UICONTROL Shareable]** 更改为以下任一项：

      - `No`  — 要求客户登录其帐户以访问下载链接。

      - `Yes`  — 通过电子邮件发送链接，客户可以与其他人共享。

      - `Use Config`  — 使用 [可下载的产品选项](../configuration-reference/catalog/catalog.md) 配置。

   - 执行以下操作之一：

      - 要限制每个客户的下载次数，请输入 **[!UICONTROL Max. Downloads]**.
      - 要允许无限下载，请选择 **[!UICONTROL Unlimited]** 复选框。

   ![链接详细信息](./assets/product-downloadable-link-detail.png){width="600" zoomable="yes"}

1. 要添加其他链接，请单击 **[!UICONTROL Add Link]** 并重复这些步骤。

#### 完成示例

1. 在 _[!UICONTROL Samples]_部分，输入&#x200B;**[!UICONTROL Title]**要用作示例标题的标题。

1. 要填写每个示例的信息，请单击 **[!UICONTROL Add Link]**.

   ![示例](./assets/product-downloadable-samples.png){width="600" zoomable="yes"}

1. 按如下方式填写链接详细信息：

   - 输入 **[!UICONTROL Title]** 单个样本的URL。

   - 选择以下分配方法之一：

      - `Upload File`  — 选择此方法以将分发文件上载到服务器。 浏览到文件并选择要上传的文件。
      - `URL`  — 选择此方法可从URL访问分发文件。 输入下载文件的完整URL。

   - 要添加另一个示例，请单击 **[!UICONTROL Add Link]** 并重复这些步骤。

   - 要更改样本的顺序，请抓取 _更改顺序_ ( ![位置控制器](../assets/icon-sort-order.png) )图标并将示例拖到新位置。

### 步骤6：完成产品信息

根据需要向下滚动并完成以下部分中的信息：

- [内容](product-content.md)
- [图像和视频](product-images-and-video.md)
- [搜索引擎优化](product-search-engine-optimization.md)
- [相关产品、向上销售和交叉销售](related-products-up-sells-cross-sells.md)
- [可自定义的选项](settings-advanced-custom-options.md)
- [网站中的产品](settings-basic-websites.md)
- [设计](settings-advanced-design.md)
- [礼品选项](product-gift-options.md)

### 步骤7：发布产品

如果您已准备好在目录中发布产品，请设置 **[!UICONTROL Enable Product]** 到 `Yes` 并执行以下操作之一：

**方法1：** 保存并预览

- 在右上角，单击 **[!UICONTROL Save]**.

- 要查看您商店中的产品，请选择 **[!UICONTROL Customer View]** 在 _管理员_ ( ![菜单箭头](../assets/icon-menu-down-arrow-black.png) )菜单。

  该存储将在新的浏览器选项卡中打开。

  ![客户视图](./assets/product-admin-customer-view.png){width="600" zoomable="yes"}

**方法2：** 保存并关闭

在 _[!UICONTROL Save]_( ![菜单箭头](../assets/icon-menu-down-arrow-red.png){width="25"} )菜单，选择&#x200B;**[!UICONTROL Save & Close]**.

## 店面体验

在客户帐户仪表板中， _[!UICONTROL My Downloadable Products]_指向每个可下载产品订单的页面链接。 订购完成后，可以从客户帐户下载内容。

![我的可下载产品](./assets/customer-account-my-downloadable-products.png){width="700" zoomable="yes"}

下表描述了 _我的可下载产品_ 值：

| 列 | 描述 |
|--- |--- |
| [!UICONTROL Order#] | 此 [订购](../stores-purchase/orders.md) 购买可下载产品的位置。 提供订单详细信息的链接。 |
| [!UICONTROL Date] | 订单创建日期。 |
| [!UICONTROL Title] | 与订单一起购买的可下载产品的名称。 提供指向可下载产品的链接。 |
| [!UICONTROL Status] | 订单处理状态。 |
| [!UICONTROL Remaining Downloads] | 已下载产品的可用下载次数。 |

_**从帐户仪表板下载产品文件**_

1. 在其帐户信息板中，客户选择 **[!UICONTROL My Downloadable Products]**.

1. 查找列表中的顺序，然后单击标题后的链接。

1. 在下载窗口的右下角，单击 _下载_ 图标。

1. 在其下载位置查找文件，并将文件保存到所需位置。

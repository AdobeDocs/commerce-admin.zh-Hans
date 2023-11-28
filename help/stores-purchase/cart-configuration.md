---
title: 购物车配置
description: 了解您可以配置的购物车功能，以支持您商店中的购买体验。
exl-id: b98ec7ce-9354-4f03-b67e-dd1587f0c866
feature: Shopping Cart, Configuration
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '2445'
ht-degree: 0%

---

# 购物车配置

购物车配置决定了购物车如何为商店客户运行，包括何时将客户重定向到购物车页面以及哪些图像用于产品缩略图。 您还可以要求订单达到结账流程开始前的最小数量，指定报价保持有效的天数，并指定中项目的顺序 _订单总计_ 部分。

[**迷你购物车**](#mini-cart)  — 配置此选项以确定购物车链接/图标是显示购物车中不同产品（或SKU）的数量，还是显示所有商品的总数量。

[**迷你购物车链接**](#configure-the-cart-link)  — 配置此选项，以确定当客户单击商店页面顶部的购物车图标中的项目数时，是否显示迷你购物车。

[**重定向到购物车**](#redirect-to-cart) — 配置此选项，以确定每次将项目添加到购物车时，还是仅当客户选择转到购物车页面时，才会显示购物车页面。

[**引用生命周期**](#quote-lifetime)  — 配置此选项以指定价格的有效时间。

[**最小订单金额**](#minimum-order-amount)  — 配置这些选项，以指定在应用折扣后需要满足订单小计的最小金额，以及购物车中显示的消息。

[**最小订货量**](#minimum-order-quantity)  — 配置这些选项以指定下单所需的最小项目数。

[**购物车缩略图**](#cart-thumbnails)   — 配置购物车缩略图选项以确定购物车中显示的用于分组或可配置产品的缩略图。

[**赠品选项**](#gift-options)  — 配置礼品选项，以确定客户是否可以添加礼品消息或贺卡，以及是否提供礼品包装选项。

>[!NOTE]
>
>有关配置签出过程的信息，请参见 [签出选项](checkout-process.md).

## 迷你购物车

此 _迷你购物车_ 显示购物车中项目的摘要。 默认情况下，该设置处于启用状态，当您单击页面顶部的“购物车”链接时会显示该设置。
可将链接配置为显示购物车中不同产品（或SKU）的数量，或显示所有商品的总数量。

![购物者显示产品页面中的购物车侧栏](./assets/storefront-mini-cart-watch.png){width="700" zoomable="yes"}

>[!NOTE]
>
>对于 _已注册_ 在有些情况下，Mini Cart可能无法在多个设备和浏览器之间自动同步。 在这种情况下，要同步Mini Cart，客户只需打开 [购物车](cart.md) 页面时，不会向其发送电子邮件。

### 配置迷你购物车

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中，展开 **[!UICONTROL Sales]** 并选择 **[!UICONTROL Checkout]**.

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 _[!UICONTROL Mini Cart]_部分。

   ![配置迷你购物车](../configuration-reference/sales/assets/checkout-mini-cart.png){width="600" zoomable="yes"}

1. 如果设置适用于特定的商店视图， [选择商店视图](../configuration-reference/scope-change.md#set-the-scope) 配置适用的位置。

   出现提示时，单击 **[!UICONTROL OK]** 以继续。

1. 设置 **[!UICONTROL Display Mini Cart]** 更改为以下任一项：

   - `Yes`  — 在商店页面上显示迷你购物车。 侧栏的外观取决于主题。
   - `No`  — 禁用在商店页面上显示迷你购物车。

1. 如果已启用显示，请更新其他选项以配置显示：

   - 对象 **[!UICONTROL Number of Items to Display Scrollbar]**，输入在触发滚动条之前可以显示在侧栏中的项目数。
   - 对象 **[!UICONTROL Maximum Display Recently Added Item(s)]**，输入您希望在迷你购物车中显示的最近添加项目的最大数量。

1. 单击 **[!UICONTROL Save Config]**.

### 配置购物车链接

1. 在 _管理员_ 侧栏，必须 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中，展开 **[!UICONTROL Sales]** 并选择 **[!UICONTROL Checkout]**.

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL My Cart Link]** 部分。

1. 设置 **[!UICONTROL Display Cart Summary]** 到以下设置之一：

   - `Display item quantities`  — 此设置显示购物车中的产品总数，并添加每个产品的数量。
   - `Display number of items in cart`  — 此设置显示购物车中的产品项目数，与数量无关。

   ![我的购物车链接的配置选项](../configuration-reference/sales/assets/checkout-my-cart-link.png){width="600" zoomable="yes"}

1. 单击 **[!UICONTROL Save Config]**.

## 重定向到购物车

可将购物车页面配置为在每次将项目添加到购物车时显示，或仅在客户选择转到该页面时显示。 有关购物车中当前商品的基本信息始终在以下位置提供： [迷你购物车](#mini-cart). 该决策是一个平衡问题，即让客户继续购物带来的好处与鼓励客户结账带来的好处。 这可能是个人喜好的一个简单问题。 但是，如果要使用数字对其进行备份，则可以运行A/B测试，以查看哪种方法生成的转化率更高。

**_要在显示购物车时进行配置，请执行以下操作：_**

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中，展开 **[!UICONTROL Sales]** 并选择 **[!UICONTROL Checkout]**.

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Shopping Cart]** 部分。

   ![页面上展开的购物车配置设置](../configuration-reference/sales/assets/checkout-shopping-cart.png){width="600" zoomable="yes"}

1. 如果设置适用于特定的商店视图， [选择商店视图](../configuration-reference/scope-change.md#set-the-scope) 配置适用的位置。

   出现提示时，单击 **[!UICONTROL OK]** 以继续。

1. 设置 **[!UICONTROL After Adding a Product Redirect to Shopping Cart]** 更改为以下任一项：

   - `Yes`  — 在将产品添加到购物车后立即显示购物车页面。
   - `No`  — 在将产品添加到购物车后禁用重定向到购物车。

1. 单击 **[!UICONTROL Save Config]**.

## 引用生命周期

通过安装和启用Adobe Commerce的B2B，您可以添加对 _引号_ 功能。 此功能允许授权买方通过从购物车提交请求来启动价格洽谈流程。 此 _引号_ grid列出收到的每一份报价，并维护买卖双方之间的通信历史。 有关B2B功能的详细信息，请参阅 [议价报价](../b2b/quotes.md) 在 _《 B2B for Adobe Commerce用户指南》_.

您可以通过设置配置中的购物车报价生命周期来确定价格的有效时间。 例如，如果购物者在几天后离开购物车无人看管，则某些商品的报价可能不再相同。 默认情况下，报价生命周期设置为30天。

**_要配置报价生命周期，请执行以下操作：_**

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中，展开 **[!UICONTROL Sales]** 并选择 **[!UICONTROL Checkout]**.

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Shopping Cart]** 部分。

   ![页面上展开的购物车配置设置](../configuration-reference/sales/assets/checkout-shopping-cart.png){width="600" zoomable="yes"}

1. 如果设置适用于特定的商店视图， [选择商店视图](../configuration-reference/scope-change.md#set-the-scope) 配置适用的位置。

   出现提示时，单击 **[!UICONTROL OK]** 以继续。

1. 对象 **[!UICONTROL Quote Lifetime (days)]**，输入报价保持有效的天数。

1. 单击 **[!UICONTROL Save Config]**.

## 最小订单金额

利用配置，可指定在应用折扣后需要满足订单小计的最小金额。 要达到每个地址的最低订单金额，可能需要向多个地址发运订单。 只有在达到最小订单量后，“结帐”按钮才可用。

![购物车显示最小订单消息](./assets/storefront-cart-minimum-order-amount.png){width="700" zoomable="yes"}

**_要配置最小订单金额，请执行以下操作：_**

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中，展开 **[!UICONTROL Sales]** 并选择 **[!UICONTROL Sales]** 下方。

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Minimum Order Amount]** 部分。

   ![页面上展开的最低订单配置选项](../configuration-reference/sales/assets/sales-minimum-order-amount.png){width="600" zoomable="yes"}

1. 要要求最小订单金额，请设置 **[!UICONTROL Enable]** 到 `Yes`.

1. 如果启用了最小订单，请设置以下选项以配置需求：

   - 输入 **[!UICONTROL Minimum Amount]** 小计中扣除折扣后所需的金额。

   - 设置 **[!UICONTROL Include Discount Amount]** 更改为以下任一项：

      - `Yes`  — 要求小计满足包含任何折扣的最小金额。 以$50为最小值的示例，如果购物车中包含$60的上部并应用25%的折扣，则结果小计为$45，并且购物车不符合最小值。
      - `No`  — 要求小计在不打任何折扣的情况下达到最小金额。

   - 设置 **[!UICONTROL Include Tax to Amount]** 更改为以下任一项：

      - `Yes`  — 要求小计满足包含税的最低金额。
      - `No`  — 要求小计达到不含税的最低金额。

1. （可选）自定义最小订单金额消息设置：

   - 对象 **[!UICONTROL Description Message]**，输入要使用的文本，以自定义当小计不符合最小数量时显示在购物车顶部的消息。

   - 对象 **[!UICONTROL Error to Show in Shopping Cart]**，输入要用于自定义购物车错误消息的文本。

   将消息描述字段留空以使用默认消息。

1. 如果需要，请配置多地址订单的最小订单金额设置：

   - 要要求多地址订单中的每个地址均满足最小订单金额，请设置 **[!UICONTROL Validate Each Address Separately in Multi-address Checkout]** 到 `Yes`.

   - （可选）自定义最小订单金额消息设置：

      - **[!UICONTROL Multi-address Description Message]**  — 输入用于自定义消息内容的文本，该消息显示在不符合最小值的多个地址订单的购物车顶部。

      - **[!UICONTROL Multi-address Error to Show in Shopping Cart]**  — 输入用于自定义不符合最小值的多地址订单的购物车错误消息的文本，在框中输入文本。

     将消息描述字段留空以使用默认消息。

1. 单击 **[!UICONTROL Save Config]**.

## 最小订货量

您可以设置订单允许的最小数量。 也可以根据每个客户组配置最小数量。

1. 转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中，展开 **[!UICONTROL Catalog]** 并选择 **[!UICONTROL Inventory]**.

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Product Stock Options]** 部分。

   ![产品股票期权](../configuration-reference/catalog/assets/catalog-inventory-product-stock-options.png){width="600" zoomable="yes"}

1. 对象 **[!UICONTROL Minimum Qty Allowed in Shopping Cart]**，设置订单产品的最小数量。

   如有需要，清除 **[!UICONTROL Use system value]** 复选框，以修改这些设置。

   - 更改 **[!UICONTROL Customer Group]** 设置到特定组，然后输入 **[!UICONTROL Minimum Qty]** 为那个组别准备的。 要添加其他组和数量限制，请单击 **[!UICONTROL Add Minimum Qty]**.

   - 若要为所有客户设置相同的最低数量限制，请保留 `ALL GROUPS` 选择并输入 **[!UICONTROL Minimum Qty]**.

1. 单击 **[!UICONTROL Save Config]**.

   ![购物车中的最小数量要求](./assets/minimum-qty-allowed-in-shopping-cart.png){width="700" zoomable="yes"}

## 购物车缩略图

![Adobe Commerce](../assets/adobe-logo.svg) (仅限Adobe Commerce)

购物车中显示的缩略图图像可为客户快速概述他们即将购买的项目。 但是，对于具有多个选项的产品，图像可能与购物车中产品的变体不匹配。 如果客户购买特定颜色的商品，理想情况下，购物车中的缩略图应该相匹配。

分组和可配置产品的缩略图图像均可以设置为显示“父”产品或产品变体的图像。

![购物车显示每个产品的缩略图](./assets/storefront-cart.png){width="700" zoomable="yes"}

**_要配置购物车缩略图，请执行以下操作：_**

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中，展开 **[!UICONTROL Sales]** 并选择 **[!UICONTROL Checkout]**.

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Shopping Cart]** 部分。

   ![页面上展开的购物车配置设置](../configuration-reference/sales/assets/checkout-shopping-cart.png){width="600" zoomable="yes"}

1. 设置 **[!UICONTROL Grouped Product Image]** 以确定购物车中使用的缩略图 [分组的产品](../catalog/product-create-grouped.md)：

   - `Product Thumbnail Itself`  — 使用分配给添加到购物车的产品变体的缩略图。
   - `Parent Product Thumbnail`  — 使用分配给父产品的缩略图。

1. 设置 **[!UICONTROL Configurable Product Image]** 以确定购物车中使用的缩略图 [可配置产品](../catalog/product-create-configurable.md)：

   - `Product Thumbnail Itself`  — 使用分配给添加到购物车的产品变体的缩略图。
   - `Parent Product Thumbnail`  — 使用分配给父产品的缩略图。

1. 单击 **[!UICONTROL Save Config]**.

## 赠品选项

在结帐流程开始之前，购物车中会显示可用的礼品选项选项。 礼品选项配置确定客户是否可以添加礼品消息或贺卡，以及礼品包装选项是否可用。 订单中的每件物品都可以有单独的消息和礼品包装。 在对整个订单进行核销时，客户还可以添加礼品收据和贺卡。

![示例店面 — 购物车中的礼品选项](./assets/storefront-cart-gift-options-for-products-or-order.png){width="700" zoomable="yes"}

礼品选项配置适用于整个网站，但可以在产品级别覆盖。

### 启用礼品选项

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中，展开 **[!UICONTROL Sales]** 并选择 **[!UICONTROL Sales]** 下方。

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) **[!UICONTROL Gift Options]** 在页面上。

   ![销售配置 — 赠品选项设置](../configuration-reference/sales/assets/sales-gift-options.png){width="600" zoomable="yes"}

1. 根据您的喜好设置礼品消息选项：

   - 对象 **[!UICONTROL Allow Gift Messages on Order Level]**，选择 `Yes` 为整个订单启用单个礼品消息。
   - 对象 **[!UICONTROL Allow Gift Messages for Order Items]**，选择 `Yes` 为客户购物车中的单个项目添加单独的礼品消息。

1. ![Adobe Commerce](../assets/adobe-logo.svg) (仅限Adobe Commerce)根据您的偏好设置礼品包装选项：

   - 对象 **[!UICONTROL Allow Gift Wrapping on Order Level]**，选择 `Yes` 为整个订单启用单个礼品包装。
   - 对象 **[!UICONTROL Allow Gift Wrapping for Order Items]**，选择 `Yes` 启用将礼品包装单独添加到客户购物车中的每个项目。

   您还可以定义不同的 [礼品包装设计](#gift-wrap) 以便客户可以选择包装。

1. ![Adobe Commerce](../assets/adobe-logo.svg) (仅限Adobe Commerce)为向客户提供包含礼品收据的选项，请设置 **[!UICONTROL Allow Gift Receipt]** 到 `Yes`.

1. ![Adobe Commerce](../assets/adobe-logo.svg) (仅限Adobe Commerce)为客户提供包含打印卡的选项，请设置 **[!UICONTROL Allow Printed Card]** 到 `Yes`.

1. ![Adobe Commerce](../assets/adobe-logo.svg) (仅限Adobe Commerce)输入 **[!UICONTROL Default Price for Printed Card]**.

1. 单击 **[!UICONTROL Save Config]**.

### 礼品包装

![Adobe Commerce](../assets/adobe-logo.svg) (仅限Adobe Commerce)

礼品包装适用于任何可发运的产品，并且可以针对单个项目或整个订单提供。 您可以对每个礼品包装设计单独收费，并为购物车中作为产品选项显示的每个设计上传缩略图。 当客户单击礼品包装缩略图时，会显示全尺寸图像。 在结帐审核期间，礼品包装费用会与其他项一起显示 [签出总计](checkout-totals-sort-order.md) 在 _订单摘要_ 部分。

礼品包装图像应是显示重复图案的色板，也可以包含要使用的带子示例。 您可以扫描纸张，或者为包装好的包裹拍照。 上传的图像可以是GIF、JPG或PNG图像，且应为正方形。 在以下示例中，上传的礼品包装图像为230 x 230像素。

![购物车中的礼品选项](./assets/storefront-cart-gift-options-gift-wrap.png){width="700" zoomable="yes"}

#### 添加礼品包装设计

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Gift Wrapping]**.

   ![礼品包装网格](./assets/gift-wrapping.png){width="700" zoomable="yes"}

1. 在右上角，单击 **[!UICONTROL Add Gift Wrapping]**.

1. 输入名称 **[!UICONTROL Gift Wrapping Design]** 将在结账过程中显示。

   如果需要，您可以更改 **[!UICONTROL Scope]** 并为每个商店视图配置不同的名称。

1. 选择 **[!UICONTROL Websites]** 提供礼品包装设计。

1. 设置 **[!UICONTROL Status]** 到 `Enabled`.

   如果您有季节性的包装选项，则可以将其设置为 `Disabled` 当您不希望该选项可用时。

1. 输入 **[!UICONTROL Price]** 礼品包装设计。

   此设置可以由产品层设置的礼品包装价格覆盖。

   ![新礼品包装](./assets/gift-wrapping-new.png){width="600" zoomable="yes"}

1. 上传缩略图 **[!UICONTROL Image]** 在礼品包装中，单击 **[!UICONTROL Choose File]** 并从目录中选择要上载的文件。

   图像的缩略图显示在 _[!UICONTROL Gift Wrapping Information]_在保存记录之后。

1. 单击 **[!UICONTROL Save]**.

#### 编辑礼品包装设计

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Gift Wrapping]**.

1. 在列表中查找礼品包装记录。

1. 在 _操作_ 列，单击 **[!UICONTROL Edit]**.

   ![编辑礼品包装信息](./assets/gift-wrapping-edit.png){width="600" zoomable="yes"}

1. 进行必要的更改。

1. 单击 **[!UICONTROL Save]**.

#### 删除礼品包装设计

使用 _礼品包装_ 网格打开，请使用以下方法之一删除环绕设计。

**_方法1：删除单个礼品包装设计_**

1. 在编辑模式下打开礼品包装设计。

1. 在工作区顶部，单击 **[!UICONTROL Delete]**.

1. 出现提示时，单击 **[!UICONTROL OK]** 以确认。

**_方法2：删除多个礼品包装设计_**

1. 在 _礼品包装_ 在网格中，选中要删除的每个礼品包装设计的复选框。

1. 设置 **[!UICONTROL Actions]** 控制对象 `Delete`.

1. 单击 **[!UICONTROL Submit]**.

### 赠品期权税

![Adobe Commerce](../assets/adobe-logo.svg) (仅限Adobe Commerce)

礼品包装和打印的礼品卡价格可以配置为含税或免税，或者同时显示这两个选项。 您还可以在全局或网站级别为这些项目指定税分类。

**_要配置赠品选项税，请执行以下操作：_**

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中，展开 **[!UICONTROL Sales]** 并选择 **[!UICONTROL Tax]**.

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Tax Classes]** 部分。

   ![税分类配置](../configuration-reference/sales/assets/tax-tax-classes.png){width="600" zoomable="yes"}

1. 设置 **[!UICONTROL Tax Class for Gift Options]** 至适用税分类。

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Orders, Invoices, Credit Memos Display Settings]** 部分。

   ![订单、发票、贷项通知单显示设置](../configuration-reference/sales/assets/tax-orders-invoices-credit-memos-display-settings.png){width="600" zoomable="yes"}

1. 设置 **[!UICONTROL Display Gift Wrapping Prices]** 更改为以下任一项：

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. 设置 **[!UICONTROL Display Printed Card Prices]** 更改为以下任一项：

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. 单击 **[!UICONTROL Save Config]**.

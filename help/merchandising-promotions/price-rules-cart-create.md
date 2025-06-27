---
title: 创建购物车价格规则
description: 了解如何根据购物车或产品属性创建购物车价格规则。
exl-id: 7260e7c3-3b1e-43e5-9c09-c40538e37378
feature: Merchandising, Price Rules, Shopping Cart
source-git-commit: d981a0365cc7768394ca03f4352be45caef87a73
workflow-type: tm+mt
source-wordcount: '3382'
ht-degree: 0%

---

# 创建购物车价格规则

完成以下步骤以添加规则、描述条件和定义操作。 还要完成标签并测试规则。 价格规则条件可以基于购物车或[产品属性](../catalog/product-attributes.md)或[Real-Time CDP受众](#use-real-time-cdp-audiences-to-set-a-condition)，但不能基于[可自定义选项](../catalog/settings-advanced-custom-options.md)。

## 步骤1：添加规则

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Cart Price Rules]**。

1. 单击&#x200B;**[!UICONTROL Add New Rule]**&#x200B;并执行以下操作：

   - 在&#x200B;_[!UICONTROL Rule Information]_下，完成&#x200B;**[!UICONTROL Rule Name]**和&#x200B;**[!UICONTROL Description]**。

   - 如果不希望规则立即生效，请将&#x200B;**[!UICONTROL Active]**&#x200B;设置为`No`。

   ![购物车价格规则 — 规则信息](./assets/price-rule-cart-new.png){width="600" zoomable="yes"}

1. 要建立规则的[范围](../getting-started/websites-stores-views.md#scope-settings)，请执行以下操作：

   - 选择要提供促销的&#x200B;**[!UICONTROL Websites]**。

   - 选择将应用促销的&#x200B;**[!UICONTROL Customer Groups]**。

     如果您希望促销活动仅对注册客户可用，请&#x200B;**_不要_**&#x200B;选择`NOT LOGGED IN`选项。

1. 按如下方式设置要应用或不应用[优惠券](price-rules-cart-coupon.md)的规则：

   - 若要在不使用优惠券代码的情况下应用购物车规则，请将&#x200B;**[!UICONTROL Coupon]**&#x200B;设置为`No Coupon`并跳至步骤5。

   - 要将优惠券与价格规则关联，请将&#x200B;**[!UICONTROL Coupon]**&#x200B;设置为`Specific Coupon`并执行以下操作：

      - 输入客户必须输入才能获得折扣的自由文本&#x200B;**[!UICONTROL Coupon Code]**。

      - 要设置优惠券可用次数的限制，请完成以下选项：

     | 选项 | 描述 |
     |------|-----------|
     | `Uses per Coupon` | 确定优惠券代码的使用次数。 如果没有限制，请将该字段留空。 |
     | `Uses per Customer` | 确定属于任何选定客户组的同一注册客户可以使用购物车价格规则的次数。 设置不适用于属于NOT LOGGED IN客户组的访客购物者，也不适用于未登录到其帐户进行购买的客户。 如果没有限制，请将该字段留空。 |

     {style="table-layout:auto"}

     若要了解详细信息，请参阅[优惠券代码](price-rules-cart-coupon.md)。

     ![购物车价格规则 — 优惠券设置](./assets/price-rule-cart-coupon-settings-ee.png){width="600" zoomable="yes"}

   - ![Magento Open Source](../assets/open-source.svg)(仅限Magento Open Source)使用&#x200B;_日历_ （![日历图标](../assets/icon-calendar.png)）为促销选择&#x200B;**[!UICONTROL From]**&#x200B;和&#x200B;**[!UICONTROL To]**&#x200B;日期范围。

1. 输入一个数字，以定义与此同时处于活动状态的其他价格规则的“操作”设置相关的此价格规则的&#x200B;**[!UICONTROL Priority]**。

   当同一产品应用了多个购物车规则或优惠券时，将首先应用具有最高优先级（最低编号）的规则。 具有相同优先级的规则不会合并；它们会根据规则ID单独应用。 要控制应用折扣的顺序，请分配唯一的优先级，并考虑在“操作”步骤中使用[放弃后续价格规则](#step-3-define-the-actions)以防止折扣栈叠。

1. 若要将规则应用于已发布的[RSS源](social-rss.md#rss-feeds)，请将RSS源&#x200B;**中的**&#x200B;公共设置为`Yes`。

1. 单击&#x200B;**[!UICONTROL Save and Continue Edit]**。

   - ![Magento Open Source](../assets/open-source.svg)(仅限Magento Open Source)保存规则后，购物车价格规则的名称将显示在页面顶部。

   - ![Adobe Commerce](../assets/adobe-logo.svg)(仅限Adobe Commerce)保存规则后，购物车价格规则的名称和[计划的更改](price-rule-cart-scheduled-changes.md)框将显示在页面顶部。

     ![购物车价格规则 — 计划的更改](./assets/price-rule-cart-scheduled-changes.png){width="600" zoomable="yes"}

## 第2步：描述条件

>[!NOTE]
>
>如果您使用的是Real-Time CDP中的受众，请跳至[此部分](#use-real-time-cdp-audiences-to-set-a-condition)。

在此步骤中，将说明订单必须符合哪些条件才能获得促销资格。 条件会以下列方式影响购物车价格规则：

- 当满足&#x200B;_[!UICONTROL Conditions]_选项卡中的条件集时，购物车价格规则将应用于购物车中的每个&#x200B;**_产品_**。 要限制受购物车价格规则影响的产品数，请在_[!UICONTROL Actions]_&#x200B;选项卡中添加条件以限制受购物车价格规则影响的产品数。

- 如果至少一个条件产品属性的值为空，则购物车价格规则不适用于该产品。

1. 在左侧面板中，选择&#x200B;**[!UICONTROL Conditions]**。

   ![购物车价格规则 — 条件](./assets/conditions.png){width="600" zoomable="yes"}

   默认情况下，将显示第一个条件，其状态为：

   `If **ALL** of these conditions are **TRUE**:`

   语句有两个粗体链接，单击这两个链接可显示语句该部分的选项选择。 您可以通过更改这些值的组合来创建不同的条件。 执行以下任一操作：

   - 单击&#x200B;**[!UICONTROL ALL]**&#x200B;并选择`ALL`或`ANY`。
   - 单击&#x200B;**[!UICONTROL TRUE]**&#x200B;并选择`TRUE`或`FALSE`。
   - 保持不变，以将规则应用于所有产品。

1. 单击下一行开头的&#x200B;_添加_ （![添加图标](../assets/icon-add-green-circle.png)），然后选择条件的选项，如购物车属性、产品子选择或组合。

   对于此示例，请完成条件的下一部分，如下所示：

   - 当系统提示&#x200B;**[!UICONTROL Choose the condition to add]**&#x200B;时，请选择`Products Subselection`。

     ![购物车价格规则条件 — 产品子选择](./assets/price-rule-cart-condition-products-subselection.png){width="600" zoomable="yes"}

   - 在条件语句中，单击&#x200B;**[!UICONTROL total quantity]**&#x200B;并选择`total quantity`或`total amount`。

   >[!IMPORTANT]
   >
   >[!UICONTROL Total amount]是行总计，因此对于[!UICONTROL Products Subselection]购物车价格规则条件，税不包含在`total amount`中。 使用[!UICONTROL Subtotal (Incl. Tax)]条件包括税费。

   - 在条件语句中，单击&#x200B;**[!UICONTROL is]**&#x200B;并选择`greater than`。

1. 当条件的下一部分出现时，单击语句的元素，以便您能够查看每个带变量值的链接的位置。

1. 单击“更多”(...)链接，然后输入`100`。

   此条件要求购物车的总数量为`101`或更大。

   ![购物车价格规则条件 — 总数量值](./assets/condition-products-subselection3.png){width="600" zoomable="yes"}

1. 在下一行的开头单击&#x200B;**添加** （![添加图标](../assets/icon-add-green-circle.png)），然后添加基于&#x200B;**类别**&#x200B;的条件。

   ![购物车价格规则条件 — 产品属性类别](./assets/condition-products-subselection4.png){width="600" zoomable="yes"}

1. 在条件的下一部分，单击&#x200B;_更多_ (**...**)链接以显示输入字段，然后打开&#x200B;_选择器_ （![列表图标](../assets/icon-list-chooser.png)）以显示类别树。

1. 选中要用作价格规则条件的类别的复选框，然后单击![添加图标](../assets/icon-checkmark-green-circle.png)图标以接受类别选择。

   该条件可以基于作为存储的[根类别](../catalog/category-root.md)的子级的任何类别。

   ![购物车价格规则条件 — 产品类别](./assets/subselection-category.png){width="600" zoomable="yes"}

1. 要添加更多条件，请单击&#x200B;_添加_ （![添加图标](../assets/icon-add-green-circle.png)）并定义另一个条件。

   您可以根据需要多次重复此过程，以说明价格规则必须满足的条件。 以下是一些示例：

   **示例1：**&#x200B;区域价格规则

   要创建区域价格规则，请使用以下购物车属性之一：

   - `Shipping Postcode`
   - `Shipping Region`
   - `Shipping State/Province`
   - `Shipping Country`

   **示例2：**&#x200B;购物车总计

   要根据购物车总数确定条件，请使用以下购物车属性之一：

   - `Subtotal`
   - `Total Items Quantity`
   - `Total Weight`

>[!NOTE]
>
>在多个并行促销的情况下，_小计_&#x200B;条件应用于&#x200B;_**折扣之前的&#x200B;_基本_购物车小计**_。

>[!IMPORTANT]
>
>**仅适用于采购订单**：如果购物车价格规则是基于一个或多个特定付款方式设置的，则折扣将应用于创建采购订单时的总计。 创建采购订单后，如果付款方式更改为购物车价格规则未涵盖的付款方式，则折扣仍应用于合计。

### 将产品属性添加到购物车价格规则

1. 转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**并打开产品属性。

1. 在左侧面板中，选择&#x200B;**[!UICONTROL Storefront Properties]**。

1. 将&#x200B;**[!UICONTROL Use for Promo Rule Conditions]**&#x200B;设置为`Yes`。

1. 单击&#x200B;**[!UICONTROL Save Attribute]**。

1. 转到&#x200B;**[!UICONTROL Marketing]** > **[!UICONTROL Cart Price Rules]**&#x200B;并打开所需的购物车价格规则。

1. 展开![扩展选择器](../assets/icon-display-expand.png) **[!UICONTROL Condition]**&#x200B;部分并选择&#x200B;**[!UICONTROL Product attribute combination]**。

1. 将此条件设置为以下值之一：

   - 单击&#x200B;**[!UICONTROL FOUND]**&#x200B;并选择`FOUND`或`NOT FOUND`。

   - 单击&#x200B;**[!UICONTROL ALL]**&#x200B;并选择`ALL`或`ANY`。

1. 单击&#x200B;_添加_ （![添加图标](../assets/icon-add-green-circle.png)）图标并选择您为促销规则条件设置的&#x200B;**[!UICONTROL Product Attribute]**。

1. 单击&#x200B;**[!UICONTROL Save]**。

>[!NOTE]
>
>在将`is not one of`条件与&#x200B;_SKU_&#x200B;产品属性和可配置产品一起使用时，必须同时选择父产品和子产品SKU。 要避免在规则中列出所有子SKU，您可以将`does not contain`条件与可配置产品及其子产品的公共SKU部件一起使用。

### 使用Real-Time CDP受众设置条件

您可以根据Real-Time CDP [audience](../customers/audience-activation.md)为购物车价格规则设置条件。

1. 展开&#x200B;**[!UICONTROL Conditions]**，单击“+”图标，然后从列表中选择&#x200B;**[!UICONTROL Real-Time CDP Audience]**。

   ![选择Real-Time CDP受众条件](./assets/rtcdp-conditions.png){width="300"}

1. 选择&#x200B;_更多_ (**...**)图标，单击&#x200B;**[!UICONTROL Open Chooser]**，然后查看所有可用的Real-Time CDP受众。

   ![查看Real-Time CDP受众](./assets/rtcdp-conditions-chooser.png){width="600" zoomable="yes"}

1. 选择要用于购物车价格规则的Real-Time CDP受众。

   | 选项 | 描述 |
   |------|-----------|
   | `ID` | 管理员中使用的受众的内部标识符 |
   | `Real-Time CDP Audience ID` | 在Experience Platform中创建受众时的唯一标识符 |
   | `Name` | 受众的名称，如`Orders over $50` |
   | `Description` | 受众的描述，如`People who placed an order over $50 in the last month.`。 |
   | `Source` | 指示受众的来源，如`Experience Platform`。 |
   | `Website` | 指示您已链接到包含受众的数据流的网站。 当您通过[[!DNL Data Connection]](https://experienceleague.adobe.com/docs/commerce/data-connection/fundamentals/connect-data.html)扩展将Commerce实例连接到Experience Platform时，将创建此链接。 |

   {style="table-layout:auto"}

在下一步中，您将定义满足条件时要执行的操作。

## 步骤3：定义操作

购物车价格规则操作描述在满足条件时如何更新价格。

1. 向下滚动到&#x200B;**[!UICONTROL Actions]**，并展开![扩展选择器](../assets/icon-display-expand.png)部分。

   ![购物车价格规则 — 操作](./assets/price-rule-cart-actions.png){width="600" zoomable="yes"}

1. 将&#x200B;**[!UICONTROL Apply]**&#x200B;设置为以下折扣选项之一：

   | 选项 | 描述 |
   |------|-----------|
   | `Percent of product price discount` | 通过从原始价格中减去百分比来折扣物料。 折扣适用于购物车中的每个合格项目。 例如：在[!UICONTROL Discount Amount]中输入`10`以获取比原始价格低10%的更新价格。 |
   | `Fixed amount discount` | 通过从购物车中每个合格项目的原始价格减去固定金额来折扣项目。 例如：在[!UICONTROL Discount Amount]中输入`10`以获取比原始价格低10美元的更新价格。 |
   | 整个购物车的固定金额折扣 | 通过从购物车总计中减去固定金额对整个购物车进行折扣。 例如：在[!UICONTROL Discount Amount]中输入10将从购物车总计中减去$10。 默认情况下，折扣仅适用于购物车小计。 要将折扣分别应用于小计和运费，请使用&#x200B;_[!UICONTROL Apply to Shipping Amount]_选项。 |
   | `Buy X get Y free` | 定义客户必须购买的数量X以免费接收相同产品/变体&#x200B;**的数量Y**。 （[!UICONTROL Discount Amount]为Y。）购物车中必须存在X+Y相同项目的总数量/已添加到购物车中，才能应用折扣。 |

   {style="table-layout:auto"}

   - 要在使用不同货币的网站中一致地应用固定金额折扣（不从全局基础货币进行转换），请将&#x200B;**[!UICONTROL Catalog Price Scope]**&#x200B;选项设置为`Website`并为每个网站定义一个基础货币。

   - 将&#x200B;**[!UICONTROL Discount Amount]**&#x200B;输入为不带符号的数字。 例如，根据所选的折扣选项，数字10可能表示百分比、固定金额或物料数量。

   - 对于&#x200B;_购买X获取Y免费_&#x200B;折扣，请在客户必须购买的单个产品/SKU/行项目的&#x200B;**[!UICONTROL Discount Qty Step (Buy X)]**&#x200B;字段中输入数量以获取Y数量的折扣。 X和Y均引用同一SKU的数量，并且必须将项目的特定数量（可配置产品的变体单独计数）手动添加到购物车中。

   - 在&#x200B;**[!UICONTROL Maximum Qty Discount is Applied To]**&#x200B;字段中，输入同一采购中符合折扣条件的相同产品的最大数量。

   - 按如下方式设置&#x200B;**[!UICONTROL Apply to Shipping Amount]** （![选项切换](../assets/toggle-yes.png)）：

     | 选项 | 描述 |
     |------|-----------|
     | `Yes` | 将折扣金额单独应用于小计和装运金额。 |
     | `No` | 仅将折扣金额应用于小计。 |

     {style="table-layout:auto"}

   - 要在应用此规则后停止处理其他规则，请将&#x200B;**[!UICONTROL Discard Subsequent Rules]** （![选项切换](../assets/toggle-yes.png)）设置为`Yes`。 此设置可防止对同一产品应用多个折扣。

     | 选项 | 描述 |
     |------|-----------|
     | `Yes` | 阻止应用可能应用于产品的任何其他定价规则。 当多个定价规则应用于同一产品时，只有具有最高定义优先级的定价规则（在规则[!UICONTROL Priority]字段中）应用于合格产品。 这可以防止多个定价规则栈叠并提供意外的额外折扣。 |
     | `No` | 允许对同一产品应用多个定价规则。 这可能会导致栈叠并提供与您的挂牌价格对应的多个折扣。 |

     {style="table-layout:auto"}

     >[!IMPORTANT]
     >
     >要放弃后续规则，定价规则必须使用在每个规则的优先级字段中设置的已定义优先级，并且多个规则不应定义相同的优先级。 请参阅&#x200B;_添加新规则_&#x200B;步骤中的&#x200B;**[!UICONTROL Priority]**。

1. 要定义购物车中受购物车价格规则影响的&#x200B;**_完全_**&#x200B;产品，请添加操作所需的&#x200B;**_其他_**&#x200B;条件。

   要确定免费配送是否适用于符合条件的订单，请将&#x200B;**[!UICONTROL Free Shipping]**&#x200B;设置为以下项之一：

   | 选项 | 描述 |
   |------|-----------|
   | `No` | 不提供免费送货服务。 |
   | `For matching items only` | 只有符合规则条件的项目才提供免运费。 |
   | `For shipment with matching items` | 包含匹配物料的任何装运均提供免运费。 必须启用[免运费](../stores-purchase/shipping-free.md)交货方式才能使用此选项。 |

   {style="table-layout:auto"}

1. ![Adobe Commerce](../assets/adobe-logo.svg)(仅限Adobe Commerce)对于&#x200B;**[!UICONTROL Add Rewards Points]**，输入当应用购物车价格规则时，客户每张订单可获得&#x200B;**_次_**&#x200B;的固定点数。

   如果未启用奖励积分，请将此字段留空。

1. 完成后，单击&#x200B;**[!UICONTROL Save and Continue Edit]**。

## 第4步：完成标签

该标签显示在订单的总数部分，用于标识折扣。 标签文本在单词`Discount`后面用括号括起来。 您可以为所有商店视图输入默认标签，也可以为每个视图输入不同的标签。

![店面购物车 — 折扣标签](./assets/order-totals-section-discount-special.png){width="600"}

1. 向下滚动到&#x200B;**[!UICONTROL Labels]**，并展开![扩展选择器](../assets/icon-display-expand.png)部分。

1. 输入要用作&#x200B;**[!UICONTROL Default Rule Label for All Store Views]**&#x200B;的文本。

   ![购物车价格规则 — 默认标签](./assets/label-default.png){width="600" zoomable="yes"}

1. 如果您的商店有多个视图，或多个网站有多个视图，请为每个视图输入相应的标签文本。

   例如，如果每个商店视图使用不同的语言，则为每个视图输入标签的翻译。

   ![存储特定标签](./assets/label-store-specific.png){width="600" zoomable="yes"}

## 步骤5：添加相关的动态块（可选）

{{ee-feature}}

当满足条件时，与规则关联的[动态块](../content-design/dynamic-blocks.md)会出现在店面中。

1. 展开&#x200B;**[!UICONTROL Related Dynamic Blocks]**&#x200B;部分的![扩展选择器](../assets/icon-display-expand.png)。

1. 使用[搜索筛选器](../getting-started/admin-workspace.md)查找要与规则关联的块。

1. 选中第一列中的复选框可将块与规则关联。

   若要了解更多信息，请参阅价格规则中的[动态块](../content-design/dynamic-blocks-price-rules.md)。

## 步骤6：保存并测试规则

1. 完成后，单击&#x200B;**[!UICONTROL Save Rule]**。

1. 测试规则以确保其正常工作。

   价格规则每晚都会与其他系统规则一起自动处理。 在创建价格规则时，请留出足够的时间使其进入系统。 还要测试规则以确保其正确运行。 随着新规则的添加，Commerce会相应地重新计算价格和优先级。

## 购物车价格规则演示

观看以下视频，了解如何创建购物车价格规则：

>[!VIDEO](https://video.tv.adobe.com/v/343835?quality=12&learn=on)

## 字段描述

### [!UICONTROL Rule Information]

| 字段 | 描述 |
|--- |--- |
| [!UICONTROL Rule Name] | （必需）规则的名称供内部参考。 |
| [!UICONTROL Description] | 规则的描述应包括规则的用途，并解释其使用方式。 |
| [!UICONTROL Active] | （必需）确定规则在存储中是否处于活动状态。 选项： `Yes` / `No` |
| [!UICONTROL Websites] | （必需）标识可以使用规则的网站。 |
| [!UICONTROL Customer Groups] | （必需）标识应用规则的客户组。 |
| [!UICONTROL Coupon] | （必需）指示优惠券是否与规则关联。 选项： <br/>**[!UICONTROL No Coupon]**— 没有与规则关联的优惠券。<br/>**[!UICONTROL Specific Coupon]** — 特定优惠券与规则关联。 <br/>**[!UICONTROL Coupon Code]**— 出现提示时，输入客户必须输入才能利用促销的优惠券代码。<br/>**[!UICONTROL Use Auto Generation]** — 选中此复选框可自动生成多个可用于促销的优惠券代码。 <br/>**[!UICONTROL Auto]**— 显示&#x200B;_[!UICONTROL Manage Coupon Codes]_部分以定义要生成的优惠券代码的格式。 |
| [!UICONTROL Uses per Coupon] | 确定优惠券代码的使用次数。 如果没有限制，请将该字段留空。 |
| [!UICONTROL Uses per Customer] | 确定属于任何选定客户组的同一注册客户可以使用购物车价格规则的次数。 不适用于属于NOT LOGGED IN客户组的访客购物者，或者不适用于未登录到其帐户进行购买的客户。 对于无限制，请留空。 |
| [!UICONTROL Priority] | 指示此规则相对于其他规则的优先级的数字。 从最高到最低的优先级为`0,1,2,3...` |
| [!UICONTROL Public in RSS Feed] | 确定促销活动是否包含在商店的公共RSS信息源中。 选项：  `Yes` / `No` |
| [!UICONTROL From] | ![Magento Open Source](../assets/open-source.svg)(仅限Magento Open Source)可以使用优惠券的第一个日期。 |
| [!UICONTROL To] | ![Magento Open Source](../assets/open-source.svg)(仅限Magento Open Source)可使用优惠券的最后日期。 |

{style="table-layout:auto"}

### [!UICONTROL Conditions]

指定在购物车价格规则生效之前必须满足的条件。 如果留空，该规则将应用于购物车中的所有产品。 条件可以基于购物车和产品属性的任意组合。 但是，无法在购物车价格规则条件中引用[可自定义选项](../catalog/settings-advanced-custom-options.md)。

| 字段 | 描述 |
|--- |--- |
| [!UICONTROL **购物车项目属性**] |  |
| [!UICONTROL Price in cart] | 产品价格。 如果满足购物车中的产品价格条件，则该规则适用。 |
| [!UICONTROL Quantity in cart] | 产品数量。 如果满足购物车中的产品数量条件，则应用规则。 |
| [!UICONTROL Row total in cart] | 产品行总计。 如果满足购物车中的产品行总计条件，则该规则适用。 |
| [!UICONTROL **产品属性**] |  |
| [!UICONTROL Attribute Set] | 产品属性集。 如果产品满足产品属性条件，则应用规则。 |
| [!UICONTROL Category/Other attribute] | 产品类别/其他属性。 如果产品本身或子项满足类别/其他属性条件，则该规则适用。 属性必须将[!UICONTROL Use for Promo Rule Conditions]设置为`Yes`。 |
| [!UICONTROL Category/Other attribute (Children Only)] | 子产品类别/其他属性。 如果只有产品子项满足类别/其他属性条件（此处不选中产品本身），则该规则适用。 属性必须具有[!UICONTROL Use for Promo Rule Conditions]到`Yes`。 |
| [!UICONTROL Category/Other attribute (Parent Only)] | 父产品类别/其他属性。 如果只有产品本身满足类别/其他属性条件（此处不选中子产品），则该规则适用。 属性必须将[!UICONTROL Use for Promo Rule Conditions]设置为`Yes`。 |
| [!UICONTROL **购物车属性**] |  |
| [!UICONTROL Subtotal (Excl. Tax)] | 购物车小计（不含税）。 如果购物车满足小计（不含税）条件，则该规则适用。 |
| [!UICONTROL Subtotal (Incl. Tax)] | 购物车小计（包括税费）。 如果购物车满足小计（包括税费）条件，则该规则适用。 |
| [!UICONTROL Subtotal] | 购物车小计。 如果购物车满足小计条件，则应用规则。 支票根据当前税务设置包含或排除税。 |
| [!UICONTROL Total Items Quantity] | 购物车中所有产品的总数。 如果购物车满足项目总数量条件，则应用规则。 |
| [!UICONTROL Total Weight] | 购物车中所有产品的总重量。 如果购物车满足总重量条件，则应用规则。 |
| [!UICONTROL Payment Method] | 结账时选择的付款方式。 如果满足付款方式条件，则应用规则。 |
| [!UICONTROL Shipping Method] | 结账时选择了配送方式。 如果满足配送方式条件，则应用规则。 |
| [!UICONTROL Shipping Postcode] | 配送地址邮政编码。 如果送货地址符合邮政编码条件，则应用规则。 |
| [!UICONTROL Shipping Region] | 配送地址区域。 如果送货地址符合区域条件，则应用规则。 |
| [!UICONTROL Shipping State/Province] | 配送地址所在省/市/自治区。 如果配送地址满足省/市/自治区条件，则适用该规则。 |
| [!UICONTROL Shipping Country] | 配送地址国家/地区。 如果装运地址满足国家/地区条件，则应用规则。 |
| [!UICONTROL Customer Segment] | 如果注册客户或来宾客户满足客户细分条件，则该规则适用。 |

### [!UICONTROL Actions]

| 字段 | 描述 |
|--- |--- |
| [!UICONTROL Apply] | 确定应用于购买的计算类型。 选项： <br/>**[!UICONTROL Percent of product price discount]**— 通过从原始价格中减去百分比来折扣项目。 例如：在&#x200B;_[!UICONTROL Discount Amount]_中输入`10`以获取比原始价格低10%的更新价格。<br/>**[!UICONTROL Fixed amount discount]**— 通过从购物车中每个合格项目的原始价格减去固定金额来折扣项目。 例如：在_[!UICONTROL Discount Amount]_&#x200B;中输入`10`以获取比原始价格低10美元的更新价格。 <br/>**[!UICONTROL Fixed amount discount for whole cart]**— 通过从购物车小计中减去固定金额对整个购物车进行折扣。 例如：在&#x200B;_[!UICONTROL Discount Amount]_中输入`10`将从购物车小计中扣除$10。 默认情况下，折扣仅适用于购物车小计。 若要将折扣分别应用到小计和运费，请参阅_应用到运费金额&#x200B;_。<br/>**[!UICONTROL Buy X Get Y Free (discount amount is Y)]**— 定义客户必须购买才能免费接收数量的数量。 （_[!UICONTROL Discount Amount]_&#x200B;为Y。） |
| [!UICONTROL Discount Amount] | （必需）提供的折扣金额。 |
| [!UICONTROL Maximum Qty Discount is Applied To] | 设置在同一购买中可以应用折扣的最大产品数。 |
| [!UICONTROL Discount Qty Step (Buy X)] | 设置`X`在`Buy X Get Y Free`促销活动中表示的产品数。 此外，定义必须一起将多少个产品批量添加到购物车中以应用`Fixed amount discount`和`Percent of product price discount`促销。 |
| [!UICONTROL Apply to Shipping Amount] | 确定是否将折扣单独应用于小计金额和装运金额。 否则，它仅应用于小计。 选项： `Yes` / `No` |
| [!UICONTROL Discard Subsequent Rules] | 确定当此购物车价格规则匹配时，是否可将较低优先级的规则（1为最高优先级）应用于产品。 启用此选项可防止将多个折扣应用于同一产品。 选项： `Yes` / `No` |
| [!UICONTROL Free Shipping] | 确定促销中是否包含免运费，如果包含，则确定哪些项目。 选项： <br/>**[!UICONTROL No]**— 当前规则不提供免运费。<br/>**[!UICONTROL For matching items only]** — 只有购物车中与规则匹配的特定项目才提供免运费。 <br/>**[!UICONTROL For shipment with matching items]**— 购物车中的所有商品都提供免运费。 必须启用[免运费](../stores-purchase/shipping-free.md)交货方式才能使用此选项。 |
| [!UICONTROL Add Reward Points] | ![Adobe Commerce](../assets/adobe-logo.svg)(仅限Adobe Commerce)指定应用价格规则时客户获得的[奖励积分](rewards-loyalty.md)的数量。 |

{style="table-layout:auto"}

### [!UICONTROL Labels]

| 字段 | 描述 |
|--- |--- |
| [!UICONTROL Default Rule Label for All Store Views] | 标识折扣的默认标签，可用于所有商店视图。 |
| [!UICONTROL Store View Specific Labels] | 如果适用，请指定其他标签以标识每个商店视图的折扣。 |

{style="table-layout:auto"}

### [!UICONTROL Related Dynamic Blocks]

{{ee-feature}}

标识与规则关联的任何[动态块](../content-design/dynamic-blocks.md)。

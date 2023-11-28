---
title: 按国家/地区列出的税务指南
description: 根据国家/地区审核建议的税务设置。
exl-id: 027da0a2-0ff4-40a7-9b9c-eefad888bb7a
feature: Taxes
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '1324'
ht-degree: 0%

---

# 按国家/地区列出的税务指南

## 美国税务配置

这些建议的设置可用于美国境内商店的大多数税务配置。

| 税务期权 | 推荐 |
|--- |--- |
| 加载目录价格 | 不含税 |
| FPT | 不，因为FPT不征税。 |
| 税金依据 | 装运原点 |
| 计税 | 总计 |
| 运税？ | 否 |
| 应用折扣 | 税前 |
| 注释 | 所有税区具有相同的优先级；理想情况下，一个州分区和一个或更多地区用于查找邮政编码。 |

{style="table-layout:auto"}

### 税种

| 税分类 | 建议的设置 |
|--- |--- |
| 用于装运的税类 | 无 |

{style="table-layout:auto"}

### 计算设置

| 选项 | 建议的设置 |
|--- |--- |
| [!UICONTROL Tax Calculation Method Based On] | `Total` |
| [!UICONTROL Tax Calculation Based On] | `Shipping Origin` |
| [!UICONTROL Catalog Prices] | `Excluding Tax` |
| [!UICONTROL Shipping Prices] | `Excluding Tax` |
| [!UICONTROL Apply Customer Tax] | `After Discount` |
| [!UICONTROL Apply Discount on Prices] | `Excluding Tax` |

{style="table-layout:auto"}

### 默认纳税目标计算

| 选项 | 建议的设置 |
|--- |--- |
| [!UICONTROL Default Country] | `United States` |
| [!UICONTROL Default State] | 企业所在的州。 |
| [!UICONTROL Default Post Code] | 在您所在税区中使用的邮政编码。 |

{style="table-layout:auto"}

### 价格显示设置

| 选项 | 建议的设置 |
|--- |--- |
| [!UICONTROL Display Product Prices in Catalog] | `Excluding Tax` |
| [!UICONTROL Display Shipping Prices] | `Excluding Tax` |

{style="table-layout:auto"}

### 购物车显示设置

| 选项 | 建议的设置 |
|--- |--- |
| [!UICONTROL Display Prices] | `Excluding Tax` |
| [!UICONTROL Display Subtotal] | `Excluding Tax` |
| [!UICONTROL Display Shipping Amount] | `Excluding Tax` |
| [!UICONTROL Display Gift Wrapping Prices] | `Excluding Tax` |
| [!UICONTROL Display Printed Card Prices] | `Excluding Tax` |
| [!UICONTROL Include Tax in Grand Total] | `Yes` |
| [!UICONTROL Display Full Tax Summary] | `Yes` |
| [!UICONTROL Display Zero Tax Subtotal] | `Yes` |

{style="table-layout:auto"}

### 订单、发票、贷项通知单和显示设置

| 选项 | 建议的设置 |
|--- |--- |
| [!UICONTROL Display Prices] | `Excluding Tax` |
| [!UICONTROL Display Subtotal] | `Excluding Tax` |
| [!UICONTROL Display Shipping Amount] | `Excluding Tax` |
| [!UICONTROL Include Tax in Grand Total] | `Yes` |
| [!UICONTROL Display Full Tax Summary] | `Yes` |
| [!UICONTROL Display Zero Tax Subtotal] | `Yes` |

{style="table-layout:auto"}

### 固定产品税(FPT)

| 选项 | 建议的设置 |
|--- |--- |
| [!UICONTROL Enable FPT] | `No`除了加利福尼亚。 |

{style="table-layout:auto"}

## 英国税务配置

这些建议的设置可用于英国境内商店的大多数税务配置。

### 英国B2C税务配置

| 税务期权 | 推荐 |
|--- |--- |
| 加载目录价格 | 不含税 |
| FPT | 是，包括FPT和说明 |
| 税金依据 | [!UICONTROL Shipping Address] |
| 计税 | 总计 |
| 运税？ | 是 |
| 应用折扣 | 税前折扣，含税。 |
| 注释 | 用于商家标记供应商发票（包括增值税） |

{style="table-layout:auto"}

### 英国B2B税务配置

| 税务期权 | 推荐 |
|--- |--- |
| 加载目录价格 | 不含税 |
| FPT | 是，包括FPT和说明 |
| 税金依据 | [!UICONTROL Shipping Address] |
| 计税 | 在项目上 |
| 运税？ | 是 |
| 应用折扣 | 税前折扣，含税。 |
| 注释 | 以便B2B商家提供更简单的增值税供应链注意事项。 行上的计税同样有效；但是，请与您的税务管辖区核实。 设置假定商户位于供应链中，并且销售的商品被其他供应商用于增值税退税等。 此定义使按项目识别税变得容易，从而更快地生成返点。 <br/><br/>**_注意：_**某些司法管辖区要求采用商业目前不支持的不同舍入策略，而且并非所有司法管辖区都允许对项目或行层征税。 |

{style="table-layout:auto"}

## 加拿大税务配置

>[!IMPORTANT]
>
>位于GST/PST省（蒙特利尔）的商家应创建一个税则并显示合并税额。 如有任何问题，请务必咨询符合条件的税务机关。 有关特定省份的纳税要求的信息，请参阅以下内容： [魁北克省][1]， [萨斯喀彻温政府][2]、和 [面向供应商的Manitoba信息][3]

| 税务期权 | 推荐 |
|--- |--- |
| 加载目录价格 | 不含税 |
| FPT | 是，包括FPT、说明，并对FPT应用税。 |
| 税金依据 | 装运原点 |
| 计税 | 总计 |
| 运税？ | 是 |
| 应用折扣 | 税前 |

{style="table-layout:auto"}

以下示例说明如何设置加拿大的GST税率以及萨斯喀彻温省的PST税率，以及计算并显示这两种税率的税则。 此信息概述了示例配置；请确保验证税务管辖区的正确税率和规则。 设置税时，设置商店范围以将配置应用于所有适用的商店和网站。

- 相关货物的固定产品税作为产品属性包括在内。
- 在魁北克，PST称为TVQ。 如果要为魁北克设置费率，请确保使用TVQ作为标识符。

### 步骤1：完成计税设置

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 对于多站点配置，设置 **[!UICONTROL Store View]** 到作为配置目标的网站和商店。

1. 在左侧面板中，展开 **[!UICONTROL Sales]** 并选择 **[!UICONTROL Tax]**.

1. 单击以展开页面上的每个部分，并完成以下设置：

#### 计税设置

| 字段 | 建议的设置 |
|--- |--- |
| [!UICONTROL Tax Calculation Method Based On] | `Total` |
| [!UICONTROL Tax Calculation Based On] | `Shipping Address` |
| [!UICONTROL Catalog Prices] | `Excluding Tax` |
| [!UICONTROL Shipping Prices] | `Excluding Tax` |
| [!UICONTROL Apply Customer Tax] | `After Discount` |
| [!UICONTROL Apply Discount on Prices] | `Excluding Tax` |
| [!UICONTROL Apply Tax On] | `Custom Price` （如果可用） |

{style="table-layout:auto"}

#### 税分类

| 字段 | 建议的设置 |
|--- |--- |
| [!UICONTROL Tax Class for Shipping] | `Shipping` （运输需纳税） |

{style="table-layout:auto"}

#### 默认纳税目标计算

| 字段 | 建议的设置 |
|--- |--- |
| [!UICONTROL Default Country] | `Canada` |
| [!UICONTROL Default State] | （视情况而定） |
| [!UICONTROL Default Postal Code] | `*` （星号） |

{style="table-layout:auto"}

#### 购物车显示设置

| 字段 | 建议的设置 |
|--- |--- |
| [!UICONTROL Include Tax in Grand Total] | `Yes` |
| [!UICONTROL Display Full Tax Summary] | `Yes` |
| [!UICONTROL Display Zero in Tax Subtotal] | `Yes` |

{style="table-layout:auto"}

#### 固定产品税

| 字段 | 建议的设置 |
|--- |--- |
| [!UICONTROL Enable FPT] | `Yes` |
| 所有FPT显示设置 | `Including FPT and FPT description` |
| [!UICONTROL Apply Discounts to FPT] | `No` |
| [!UICONTROL Apply Tax to FPT] | `Yes` |
| [!UICONTROL Include FPT in Subtotal] | `No` |

{style="table-layout:auto"}

### 第2步：设置加拿大商品和服务税(GST)

要在发票和其它销售单据上打印GST编号，请将其包含在适用税率的名称中。 在任何订单汇总中，GST均显示为GST金额的一部分。

#### 管理税区和税率

| 字段 | 建议的设置 |
|--- |--- |
| [!UICONTROL Tax Identifier] | `Canada-GST` |
| [!UICONTROL Country] | `Canada` |
| [!UICONTROL State] | `*` （星号） |
| [!UICONTROL Zip/Post is Range] | `No` |
| [!UICONTROL Zip/Post Code] | `*` （星号） |
| [!UICONTROL Rate Percent] | `5.0000` |

{style="table-layout:auto"}

### 步骤3：设置加拿大省增值税(PST)

为适用省份设置其他税率。

#### 税率信息

| 字段 | 建议的设置 |
|--- |--- |
| [!UICONTROL Tax Identifier] | `Canada-SK-PST` |
| [!UICONTROL Country] | `Canada` |
| [!UICONTROL State] | `Saskatchewan` |
| [!UICONTROL Zip/Post is Range] | `No` |
| [!UICONTROL Zip/Post Code] | `*` （星号） |
| [!UICONTROL Rate Percent] | `5.0000` |

{style="table-layout:auto"}

### 步骤4：创建GST税则

要避免复合税，并且要为GST和PST将已计算的税正确显示为单独的行项目，请为每个规则设置不同的优先级，然后选择 **仅计算小计** 复选框。 每项税均显示为单独的行项目，但税额并不复合。

#### 税则信息

| 字段 | 建议的设置 |
|--- |--- |
| 名称 | `Retail-Canada-GST` |
| [!UICONTROL Customer Tax Class] | `Retail Customer` |
| [!UICONTROL Product Tax Class] | `Taxable GoodsShipping` |
| [!UICONTROL Tax Rate] | `Canada-GST` |
| [!UICONTROL Priority] | `0` |
| [!UICONTROL Calculate off subtotal only] | 选中此复选框。 |
| [!UICONTROL Sort Order] | `0` |

{style="table-layout:auto"}

### 步骤5：为萨斯喀彻温省创建PST税则

对于此税则，请确保将优先级设置为0，然后选择 **仅计算小计** 复选框。 每项税均显示为单独的行项目，但税额并不复合。

#### 税则信息

| 字段 | 建议的设置 |
|--- |--- |
| [!UICONTROL Name] | `Retail-Canada-PST` |
| [!UICONTROL Customer Tax Class] | `Retail Customer` |
| [!UICONTROL Product Tax Class] | `Taxable GoodsShipping` |
| [!UICONTROL Tax Rate] | `Canada-SK-PT` |
| [!UICONTROL Priority] | `1` |
| [!UICONTROL Calculate off subtotal only] | 选中此复选框。 |
| [!UICONTROL Sort Order] | `0` |

{style="table-layout:auto"}

### 步骤6：保存并测试结果

1. 完成后，单击 **[!UICONTROL Save Config]**.

1. 返回到店面并创建一个示例订单来测试结果。

## 欧盟税务配置

以下示例描述了一家位于法国的商店，它在法国销售10万欧元以上的商品，在德国销售10万欧元以上的商品。

- 税项计算在网站层级管理。
- 货币兑换和纳税显示选项在商店视图级别单独控制（选中“使用网站”复选框可覆盖默认值）。
- 通过设置默认税务国家（地区），您可以动态显示管辖区的正确税额。
- 相关货物的固定产品税作为产品属性包括在内。
- 可能需要编辑目录，以确保该目录显示在正确的类别/网站/商店视图中。

### 步骤1：创建三个产品税分类

在本例中，假定不需要多个增值税扣减产品税分类。

1. 创建增值税标准产品税分类。

1. 创建增值税减少的产品税分类。

1. 创建免增值税产品税分类。

### 步骤2：为法国和德国创建税率

创建以下税率：

| 税率 | 设置 |
|--- |--- |
| 法国 — StandardVAT | 国家/地区：法国 <br/>省/市/自治区/直辖市： * <br/>邮政编码：* <br/>比率：20% |
| 法国 — 减少的增值税 | 国家/地区：法国 <br/>省/市/自治区/直辖市： * <br/>邮政编码：* <br/>比率：5% |
| 德国 — 标准VAT | 国家：德国 <br/>省/市/自治区/直辖市： * <br/>邮政编码： *费率：19% |
| 德国 — 削减的增值税 | 国家：德国 <br/>省/市/自治区/直辖市： * <br/>邮政编码：* <br/>比率：7% |

{style="table-layout:auto"}

### 步骤3：设置税则

创建以下税则：

| 税则 | 设置 |
|--- |--- |
| Retail-France-StandardVAT | 客户类别：零售客户 <br/>税分类：VAT-Standard <br/>税率：France-StandardVAT <br/>优先级：0 <br/>排序顺序： 0 |
| Retail-France-ReducedVAT | 客户类别：零售客户 <br/>税分类：减少增值税 <br/>税率：法国 — 减额增值税 <br/>优先级：0 <br/>排序顺序： 0 |
| 零售 — 德国 — 标准增值税 | 客户类别：零售客户 <br/>税分类：VAT-Standard <br/>税率：德国 — 标准VAT <br/>优先级：0 <br/>排序顺序： 0 |
| 零售 — 德国 — 增值税减少 | 客户类别：零售客户 <br/>税分类：减少增值税 <br/>税率：德国 — 减少的增值税 <br/>优先级：0 <br/>排序顺序： 0 |

{style="table-layout:auto"}

### 步骤4：设置德国的商店视图

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**.

1. 在默认网站下，创建商店视图 **[!UICONTROL Germany]**.

1. 接下来，执行以下操作：

   - 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

   - 在左上角，设置 **[!UICONTROL Default Config]** 去法国商店。

   - 在“一般信息”页上，展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Countries Options]** 部分，并将默认国家/地区设置为 `France`.

   - 根据需要完成区域设置选项。

1. 选择左上角的德语 **[!UICONTROL Store View]**.

1. 在 _常规_ 页面，展开 ![扩展选择器](../assets/icon-display-expand.png) **[!UICONTROL Countries Options]** 并将默认国家/地区设置为 `Germany`.

1. 根据需要完成区域设置选项。

### 步骤5：配置法国的税务设置

完成以下常规税务设置：

| 字段 | 建议的设置 |
|--- |--- |
| [[!UICONTROL Tax Classes]](../configuration-reference/sales/tax.md#tax-classes) |  |
| [!UICONTROL Tax Class for Shipping] | `Shipping` （运输需纳税） |
| [[!UICONTROL Calculation Settings]](../configuration-reference/sales/tax.md#calculation-settings) |  |
| [!UICONTROL Tax Calculation Method Based On] | `Total` |
| [!UICONTROL Tax Calculation Based On] | `Shipping Address` |
| [!UICONTROL Catalog Prices] | `Including Tax` |
| [!UICONTROL Shipping Prices] | `Including Tax` |
| [!UICONTROL Apply Customer Tax] | `After Discount` |
| [!UICONTROL Apply Discount on Prices] | `Including Tax` |
| [!UICONTROL Apply Tax On] | `Custom Price if available` |
| [[!UICONTROL Default Tax Destination Calculation]](../configuration-reference/sales/tax.md#default-tax-destination-calculation) |  |
| [!UICONTROL Default Country] | `France` |
| [!UICONTROL Default State] |  |
| [!UICONTROL Default Postal Code] | `*` （星号） |
| [[!UICONTROL Fixed Product taxes]](../configuration-reference/sales/tax.md#fixed-product-taxes) |  |
| [!UICONTROL Enable FPT] | `Yes` |
| [!UICONTROL All FPT Display Settings] | `Including FPT and FPT description` |
| [!UICONTROL Apply Discounts to FPT] | `No` |
| [!UICONTROL Apply Tax to FPT] | `Yes` |
| [!UICONTROL Include FPT in Subtotal] | `Yes` |

{style="table-layout:auto"}

### 步骤6：配置德国的税务设置

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在右上角，设置 **[!UICONTROL Store View]** 前往德国商店，然后单击 **[!UICONTROL OK]** 以确认。

1. 在左侧面板中，展开 **[!UICONTROL Sales]** 并选择 **[!UICONTROL Tax]**.

1. 在 **[!UICONTROL Default Tax Destination Calculation]** 部分，执行以下操作：

   - 清除 **[!UICONTROL Use Website]** 每个字段后面的复选框，

   - 匹配您站点的配送设置 [原点](shipping-settings.md#point-of-origin)，请更新以下值：

      - 默认国家/地区
      - 默认状态
      - 默认邮政编码

     此设置可确保当产品价格含税时正确计算税款。

     ![默认纳税目标计算](./assets/destination-calc-french.png){width="600" zoomable="yes"}

1. 完成后，单击 **[!UICONTROL Save Config]**.

[1]: https://www.revenuquebec.ca/en/businesses/
[2]: https://www.saskatchewan.ca/finance
[3]: https://www.gov.mb.ca/finance/taxation/bulletins/004.pdf

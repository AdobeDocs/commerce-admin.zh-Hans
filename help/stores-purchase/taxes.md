---
title: 税金
description: 了解如何配置您的商店，以根据区域设置要求计算税额。
exl-id: bf807132-416f-497a-82c4-b00dba4d3092
feature: Taxes
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '1115'
ht-degree: 0%

---

# 税金

根据区域设置要求配置商店以计算税金。 您可以设置 [税种](tax-class.md) 产品和客户组，并创建 [税则](tax-rules.md) 将产品和客户类别、税区和税率三者结合起来。 Commerce还提供固定产品税、复合税的配置设置，以及跨国界价格的显示。 如果您需要收集 [增值税](vat.md)，您可以设置商店，通过验证自动计算相应的金额。

>[!NOTE]
>
>Adobe Commerce和Magento Open Source版本2.4.0到2.4.3包含了Vertex供应商开发的扩展，该扩展用于与Vertex Cloud集成，以提供税务管理和地址清理。 从2.4.4版本开始，此扩展不再与核心版本捆绑在一起，必须从Commerce Marketplace或直接从供应商处安装和更新。 [接触顶点](https://marketplace.magento.com/partner/vertex_inc) 有关扩展和文档的信息。<br><br>
>
>如果已启用并配置捆绑的扩展，则必须在升级2.4.4的过程中更新您的composer.json文件，并且以后要管理扩展更新。 请参阅 [升级模块](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html) 在 _升级指南_.

## 快速参考

某些税务设置可以选择确定税额计算方式并向客户显示的选项。 有关更多信息，请参阅 [国际税务准则](international-tax-guidelines.md).

配置计税设置时，请参考以下各表：

### 计税方法

计税方法选项包括 [!UICONTROL Unit Price]， [!UICONTROL Row Total]、和 [!UICONTROL Total]. 下表说明了不同设置如何处理舍入（到两位数）。

| 设置 | 计算和显示 |
|--- |--- |
| [!UICONTROL Unit Price] | Commerce计算每个项目的税并显示含税价格。 要计算税额合计，它会舍入每个项目的税额，然后将它们相加。 |
| [!UICONTROL Row Total] | Commerce计算每行的税额。 要计算税额合计，它会舍入每个行项目的税额，然后将它们相加。 |
| [!UICONTROL Total] | Commerce计算每个项目的税并添加这些税值以计算订单的未舍入总税额。 然后，它会将指定的舍入模式应用于税总额，以确定订单的税总额。 |

{style="table-layout:auto"}

### 含税或不含税的目录价格

根据计算方法以及目录价格是否包含税费，显示的字段可能会有所不同。 在正常计算中，显示字段具有两位小数精度。 某些价格设置组合会显示包含和排除税的价格。 当两者显示在同一行项目上时，可能会让客户感到困惑，并触发 [警告](taxes.md#warning-messages).

| 设置 | 计算和显示 |
|--- |--- |
| [!UICONTROL Excluding Tax] | 使用此设置，在输入基本物料价格时使用该价格，并且应用计税方法。 |
| [!UICONTROL IncludingTax] | 使用此设置，首先计算不含税的基本物料价格。 此值用作基本价格，并且应用计税方法。 |

{style="table-layout:auto"}

>[!IMPORTANT]
>
>对于欧盟商户或其他增值税商户来说，这些商户与显示含税价格并在多个国家（地区）经营且拥有多个商店视图的较早版本相比有一些变化。 如果您加载的价格的精度超过两位数，Commerce会自动将所有价格舍入为两位数，以确保为买家提供一致的价格。

### 含税或不含税的运输价格

| 设置 | 显示 | 计算 |
|--- |--- |--- |
| [!UICONTROL Excluding Tax] | 显示时不含税。 | 正常计算。 配送费会添加到购物车合计，通常显示为单独的商品。 |
| [!UICONTROL Including Tax] | 税可以含税，也可以单独显示。 | 使用相同的计算，将配送视为含税购物车中的其他商品。 |

{style="table-layout:auto"}

### 行项目形式的税额

要将两个不同的税额显示为单独的行项目（如加拿大商店的GST和PST），您必须为相关税则设置不同的优先级。 但是，在以前的计税方法中，不同优先顺序的税将自动合并。 要正确显示单独的税额而没有不正确的税额组合，您可以设置不同的优先级，也可以选择 _仅计算小计_ 复选框。 此设置会生成正确计算的税额，这些税额显示为单独的行项目。

## 警告消息

某些与税务相关的选项组合可能会让客户感到困惑，并触发警告。 当计税方法设置为时，可能会出现这些情况 `Row` 或 `Total`，向客户呈现不含税和含税价格。 当购物车中按商品计税时，也会发生这种情况。 由于计税已四舍五入，因此购物车中显示的金额可能与客户预计支付的金额不同。

如果计税基于有问题的配置，则会出现以下警告：

![感叹号](../assets/icon-warning.png) **警告**. `Tax discount configuration might result in different discounts than a customer might expect for store(s); Europe Website (French), Europe Website (German). Please see source for more details.`

![感叹号](../assets/icon-warning.png) **警告**. `Tax configuration can result in rounding errors for store(s): Europe Websites (French), Europe Websites (German).`

## 数字商品的供应地（欧盟）

欧盟(EU)商家必须按季度向每个成员国报告其数字商品销售情况。 数字商品需按客户的配送地址纳税。 该法要求商户提交税务报表，并确定数字商品（而非实物商品）的相关税额。

商家必须每季度向中央税务管理局报告欧盟成员国出售的所有数字商品，以及在此期间，应收的税款。

尚未达到阈值（年营业额50k/10万欧元）的商家必须继续报告已注册增值税号的欧盟国家所销售的实物商品。

商户为支付数码产品税金进行审核时，必须提供两项支持信息以建立客户居住地。

- 客户的送货地址和成功付款交易的记录可用于建立客户的居住地。 （仅当送货地址与付款提供商信息匹配时才接受付款。）
- 该信息也可以直接从Commerce数据库表的数据存储中捕获。

_**要收集数字商品的税务信息，请执行以下操作：**_

1. 加载所有欧盟成员国的税率。

1. 创建数字商品产品税分类。

1. 将您的所有数字商品分配给数字商品产品税分类。

1. 创建 [税则](tax-rules.md) 请对实物进行纳税分类，并将这些分类与相应的税率相关联。

1. 使用数字商品的产品税分类，为您的数字商品创建税则，并将它们与欧盟成员国适用的税率关联。

1. 运行相应期间的税务报表，并收集所需的数字商品信息。

1. 导出与数字货物产品税分类的税率相关的税额。

其他资源：

- [欧洲委员会税收和关税联盟][1]
- [欧盟1015年供应地点变动][2]

[1]: https://europa.eu/youreurope/business/taxation/vat/vat-rules-rates/index_en.htm
[2]: https://www2.deloitte.com/global/en/services/tax.html

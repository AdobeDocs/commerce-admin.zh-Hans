---
title: “配置 [!DNL Inventory Management]”
description: 了解 [!DNL Inventory Management] 选项的配置，这些选项决定源可用性、店面产品和订单装运。
exl-id: 1696999e-77b1-45c7-9b0b-dd1512427cff
feature: Inventory, Configuration
source-git-commit: 67cbb0d05f9f63ef51ccff3580cd27df86645fd0
workflow-type: tm+mt
source-wordcount: '770'
ht-degree: 0%

---

# 配置[!DNL Inventory Management]

[!DNL Inventory Management]模块支持产品和全局级别的库存配置设置，并且还提供影响源可用性、店面产品和订单发运的其他设置。 配置设置适用于：

- 整个目录：转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。 然后，展开左侧面板中的&#x200B;**[!UICONTROL Catalog]**并选择&#x200B;**[!UICONTROL Inventory]**。

- 特定产品：转到&#x200B;**[!UICONTROL Catalog]** > **[!UICONTROL Products]**。 然后，在编辑模式下打开产品，并单击&#x200B;_[!UICONTROL Sources]_部分中的&#x200B;**[!UICONTROL Advanced Inventory]**。

您的目录可以配置为在店面中显示库存数据、管理活动购物车等。 将每个项目的可用性显示为&#x200B;_缺货_&#x200B;或&#x200B;_缺货_，并在库存不足时显示可用库存。

缺货阈值指明何时应对产品重新排序，从库存的可销售数量中减去产品数量，并且可以设置为支持启用或禁用的延交订单。 允许您的商店延交订单，设置所有或特定产品的最大订单数量。

您可以使用库存可用性阈值的另一种方式是管理高需求产品。 如果您希望吸引新客户，而不是向高数量采购员销售，则可以设置最大数量，以防止单个采购员取出您的全部库存。

![示例有库存，剩余1个](assets/storefront-stock-options-1-left.png)

## 配置选项

[!DNL Commerce]商店和产品支持以下用于管理产品、库存、通知等的配置。 [!DNL Commerce]为批量操作和距离优先级算法提供了额外的配置设置。

| 选项 | 描述 |
|--|--|
| [!UICONTROL Manage Stock] | 允许[!DNL Commerce]管理所有库存。 如果对此产品或[!DNL Commerce]中的所有产品使用库存控制，则进行设置。 当设置为`Yes`时显示更多选项。 |
| [!UICONTROL Only X left Threshold] | 设置某个数量，该数量在某个特定数量可购买时通知。 此金额在库存级别进行跟踪。 |
| [!UICONTROL Out-of-Stock Threshold] | 您的安全库存，用于触发缺货通知并减轻缺货风险的数量。 此值会影响延交订单。 选项：<br />**[!UICONTROL No Backorders]**：产品缺货时不接受延交。<br />**[!UICONTROL Allow Qty Below 0]**：在数量低于零时接受延交订单。<br />**[!UICONTROL Allow Qty Below 0 and Notify Customer]**：在数量低于零时接受延交订单，但通知客户仍然可以下订单。<br /><br />**[!UICONTROL Backorders disabled]**：建议输入大于0的正值，如5或25。 <br/>**[!UICONTROL Backorders enabled]**：为允许延期交货的最大数量输入负阈值，如–5或–25。 值为0表示无限库存。 正值将被忽略并视为0。 |
| [!UICONTROL Minimum Qty Allowed in Shopping Cart] | 设置单个订单中可购买产品的最小数量。 |
| [!UICONTROL Maximum Qty Allowed in Shopping Cart] | 设置单个订单中可购买产品的最大数量。 |
| [!UICONTROL Qty Uses Decimals] | 允许产品数量的小数金额而不是整数。 此设置有助于按重量、体积或长度销售产品。 在Source级别指定，根据分配的源在库存级别计算。 |
| [!UICONTROL Allow Multiple Boxes for Shipping] | 确定产品部件是否可以单独发运。 当&#x200B;**[!UICONTROL Qty Uses Decimals]** = `Yes`时，此选项可见。 |
| [!UICONTROL Backorders] | 指示是否允许延交订单。 在Source级别指定，根据分配的源在库存级别计算。 如果启用以允许延交，则建议为缺货阈值设置负值（请参阅[配置延交](backorders.md)）。 选项：<br />**[!UICONTROL No Backorders]**：产品缺货时不接受延交。<br />**[!UICONTROL Allow Qty Below 0]**：在数量低于零时接受延交订单。<br />**[!UICONTROL Allow Qty Below 0 and Notify Customer]**：在数量低于零时接受延交订单，但通知客户仍然可以下订单。 |
| [!UICONTROL Notify for Quantity Below] | 设置触发“低于数量”通知（库存不足警告）的数量。 此金额从可销售数量中扣除，而不是从库存数量中扣除。 |
| [!UICONTROL Enable Qty Increments] | 确定产品是否可以按数量递增销售。 如果启用，请输入增量步骤中必须购买的产品数量。 增量设置作为单个产品以及可配置、分组和捆绑产品的子产品必须购买的产品项目数。 |
| [!UICONTROL Automatically Return Credit Memo Item to Stock] | [!DNL Inventory Management]不使用此值。 当您完成退货或贷项通知单时，产品数量会自动返回至受影响的来源数量。 请参阅[配置产品选项](product-options.md)。 |

## 配置回退和继承

配置覆盖或应用于以下继承路径：产品&#x200B;_[!UICONTROL Sources]_部分覆盖产品_[!UICONTROL Advanced Options]_&#x200B;覆盖全局&#x200B;_[!UICONTROL Inventory]_存储配置。

当[!DNL Commerce]检查要应用的自定义设置时，它遵循以下顺序：

1. 在&#x200B;_[!UICONTROL Sources]_分区中的产品级别检查自定义设置。 一些设置可供使用。

1. 检查产品&#x200B;_[!UICONTROL Advanced Inventory]_设置。

1. 如果为产品设置选择了`Use Config Settings`，则会从全局&#x200B;_清单_&#x200B;存储配置页面检查值。

例如，您可以使用类似于以下内容的配置，在商店中按不同方式配置延交订单：

- _全局：_&#x200B;启用商店的延期交货，将缺货阈值设置为`-50`

- _产品：_&#x200B;禁用特定产品的延期交货，将缺货阈值设置为`10`

---
title: “配置 [!DNL Inventory Management] 延期交货”
description: 了解如何配置延期交货以支持缺货产品的销售。
exl-id: 2fe778df-781e-4cda-8b85-47cf973c9e94
feature: Inventory, Orders
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '742'
ht-degree: 0%

---

# 配置[!DNL Inventory Management]个延交

延交订单使您的商店能够在数量达到零或实际缺货后继续销售产品。 当客户订单为延交订单时，系统将立即授权并获取资金，订单的处理状态不会更改，并且发运将保持暂挂状态，直到库存可用为止。

根据您的商店和销售情况，您可能要在以下层启用或禁用延交订单：

- **[!UICONTROL Global]** — 您在网站级别的目录中的所有产品

- **[!UICONTROL Product]** — 特定产品正在覆盖站点、源和库存的设置

## 了解延期交货设置

强烈建议您配置特定阈值和设置以最佳支持延交订单。

### 缺货阈值

使用此阈值的负值可设置实际视为缺货之前可以延交的最大产品数量。 此数量添加至可销售数量。 在产品级别设置的值将覆盖在全局级别设置的任何值。

可销售数量的公式为`(Quantity - (Out-of-Stock Threshold))`。

以下是示例：

- 数量：25
- 通知以下数量：10
- 仅X剩余阈值：5
- 缺货阈值：-50

此产品的可销售数量为`75 (25 - (-50))`。

![启用延交订单之前的可销售数量示例](assets/inventory-backorders-before.png){width="600" zoomable="yes"}

![启用延交订单后的可销售数量示例](assets/inventory-backorders-after.png){width="600" zoomable="yes"}

当客户购买可用的25种产品时，新订单将输入为延交订单。 由于产品的可销售数量减少到5（已销售70个项目），_产品_&#x200B;页面在店面显示消息`Only 5 left`。 当可销售数量达到`0`时，产品在店面中显示为`Out of Stock`。

>[!NOTE]
>
>当客户使用&#x200B;_[!UICONTROL backorder qty]_下达订单时，[!DNL Inventory Management]会自动从可销售数量中减去该数量。 如果订单未发运并且被取消，则数量将返回至汇总的虚拟可销售数量。**_取消的订单数量未分配给任何来源_**，而是返回到可供销售的产品总数（“产品”网格上的_[!UICONTROL Salable Quantity]_&#x200B;列）。

<!--### Notify for Quantity Below JIRA MDVA-8099 MDVA-33783

The _Notify for Quantity Below_ configuration option is configurable at the global, source, and product levels. When it is enabled, the system sends an email notification when the product quantity reaches a level at or below the configured value. For this example, a notification is triggered when the product has a quantity of 10 or less. When backorders are enabled, _Notify for Quantity Below_ is determined by the Salable Quantity (`Salable Quantity = Quantity - (Out-of-Stock Threshold)`). -->

### 库存状态

启用延期交货时，产品必须设置为`In Stock`状态。 您可以从&#x200B;_Product_&#x200B;页面设置此值。 对于多源商家，必须至少有一个源标记为`In Stock`。 通过&#x200B;_Product_&#x200B;页面访问和设置状态，并分配了&#x200B;_源_&#x200B;网格。

## 全局配置延期交货

这些步骤可为站点级别的所有产品启用延交。

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 将&#x200B;**[!UICONTROL Store View]**&#x200B;设置为`Default Config`。

1. 在左侧面板中，展开&#x200B;**[!UICONTROL Catalog]**&#x200B;并选择&#x200B;**[!UICONTROL Inventory]**。

1. 展开![扩展选择器](../assets/icon-display-expand.png) **[!UICONTROL Product Stock Options]**。

1. 对于&#x200B;**[!UICONTROL Backorders]**，取消选中&#x200B;**[!UICONTROL Use system value]**&#x200B;复选框并选择选项：

   | 选项 | 描述 |
   | -- | -- |
   | `No Backorders` | 产品缺货时不接受延交订单。 |
   | `Allow Qty Below 0` | 要在数量低于零时接受延交订单，请执行以下操作： |
   | `Allow Qty Below 0 and Notify Customer` | 在数量低于零时接受延交订单，并通知客户仍然可以下订单。 |

1. 对于&#x200B;**[!UICONTROL Out-of-Stock Threshold]**，取消选中&#x200B;**[!UICONTROL Use system value]**&#x200B;复选框并输入其他金额。

   | 值 | 描述 |
   | -- | -- |
   | 正数 | 禁用“延交订单”后，请输入正值。 |
   | 零 | 启用延交订单后，输入`0`将允许无限延交订单。 |
   | 负金额 | 启用延交订单后，建议输入负值。 该金额将添加到可销售数量。 例如，输入`-50`以允许订单数量不超过此金额。 |

1. 单击&#x200B;**[!UICONTROL Save Config]**。

## 配置产品的延交订单

产品级别配置将覆盖全局配置。 您可能需要在产品层配置延交订单以覆盖全局商店或来源层的设置。 例如，您的商店可能全局支持延期交货。 通过产品设置，您可以禁用延交订单或更改缺货阈值，而不影响其他产品和来源。

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Catalog]** > **[!UICONTROL Products]**。

1. 在&#x200B;**[!UICONTROL Edit]**&#x200B;模式下打开产品，然后向下滚动页面至&#x200B;_[!UICONTROL Sources]_区域。

   对于未配置[!DNL Inventory Management]的产品，该选项卡不会显示。 `Advanced Inventory`按钮显示在&#x200B;_[!UICONTROL Quantity]_字段下方。

1. 单击&#x200B;**[!UICONTROL Advanced Inventory]**。

   此操作显示产品特定配置的页面。 任何列为`global`的设置都会显示存储的当前全局设置。

1. 对于&#x200B;**[!UICONTROL Backorders]**，取消选中&#x200B;**[!UICONTROL Use Config Setting]**&#x200B;复选框并选择选项：

   | 选项 | 描述 |
   | -- | -- |
   | `No Backorders` | 产品缺货时不接受延交订单。 |
   | `Allow Qty Below 0` | 要在数量低于零时接受延交订单，请执行以下操作： |
   | `Allow Qty Below 0 and Notify Customer` | 在数量低于零时接受延交订单，并通知客户仍然可以下达订单。 |

1. 对于&#x200B;**[!UICONTROL Out-of-Stock Threshold]**，取消选中&#x200B;**[!UICONTROL Use Config Setting]**&#x200B;复选框并输入金额：

   | 值 | 描述 |
   | -- | -- |
   | 正数 | 禁用“延交订单”后，请输入正值。 |
   | 零 | 启用延交订单后，输入`0`将允许无限延交订单。 |
   | 负金额 | 启用延交订单后，建议输入负值。 该金额将添加到可销售数量。 例如，输入`-50`以允许订单数量不超过该金额。 |

   ![为延期交货配置了高级库存](assets/inventory-backorders-product-settings.png){width="600" zoomable="yes"}

1. 单击&#x200B;**[!UICONTROL Done]**，然后单击&#x200B;**[!UICONTROL Save]**。

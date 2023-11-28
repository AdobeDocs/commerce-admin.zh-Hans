---
title: “配置 [!DNL Inventory Management] 全局选项”
description: 了解如何配置默认值 [!DNL Inventory Management] 网站产品和库存的配置选项。
exl-id: 1a8c9605-ae61-4d45-b549-64911b329203
feature: Inventory, Configuration
source-git-commit: 7384481d1a4a2a04882d4c99448cca75abc9be31
workflow-type: tm+mt
source-wordcount: '644'
ht-degree: 1%

---

# 配置 [!DNL Inventory Management] 全局选项

为网站的产品和库存配置默认配置选项。 可以通过为每个产品覆盖其中的某些设置 [配置产品选项](product-options.md). 要配置“距离优先级”设置，请参阅 [配置距离优先级算法](distance-priority-algorithm.md).

## 全局配置产品和股票选项

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中，展开 **[!UICONTROL Catalog]** 并选择 **[!UICONTROL Inventory]**.

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Stock Options]** 并设置以下选项：

   ![股票期权](assets/config-catalog-inventory-stock-options.png){width="600" zoomable="yes"}

   - 要在下达订单时调整现有量，请设置 **[!UICONTROL Decrease Stock When Order is Placed]** 到 `Yes`.

   - 要在订单被取消时将物料退回至库存，请执行以下操作： **[!UICONTROL Set Items' Status to be in Stock When Order in Cancelled]** 到 `Yes`.

   - 要继续显示目录中不再有库存的产品，请设置 **[!UICONTROL Display Out of Stock Products]** 到 `Yes`.

   - 如果 [价格警报](alert-setup.md) 启用后，客户可以注册，以便在产品重新上架时收到通知。

   - 要设置产品页上显示最后剩余库存金额的起始时间，请输入金额 **[!UICONTROL Only X left Threshold]**.

     当库存量达到阈值时，将开始显示消息。 例如，如果设置为 `3`，消息 `Only 3 left` 库存量达到三时显示。 消息会调整以反映库存中的数量，直到数量达到零。

   - 要在产品页面上显示“缺货”或“缺货”消息，请设置 **[!UICONTROL Display Products Availability In Stock on Storefront]** 到 `Yes`.

   - 要在购物车中加载产品时检查库存，请设置 **[!UICONTROL Enable Inventory Check On Cart Load]** 到 `Yes`. 禁用此选项后，将跳过清单检查。 禁用此选项可加快结帐速度，尤其是当购物车中有许多商品时。 但是，如果您跳过预验证，客户稍后在结账过程中可能会看到“缺货”错误。

   - 要保持清单和目录之间的一致性，请设置 **[!UICONTROL Synchronize with Catalog]** 到 `Yes`. 启用此选项后，库存数据将根据目录变化（例如删除了产品、更改了产品SKU以及更改了产品类型）进行调整。

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Product Stock Options]** 并设置以下选项：

   - 激活 [库存控制](enable.md) 对于目录，设置 **[!UICONTROL Manage Stock]** 到 `Yes`.

     ![产品股票期权](assets/config-catalog-inventory-product-stock-options.png){width="600" zoomable="yes"}

   - 设置 **[!UICONTROL Backorders]** 更改为以下任一项：

     | 选项 | 描述 |
     | ----- | ----- |
     | `No Backorders` | [延期交货](backorders.md) 产品缺货时不被接受。 |
     | `Allow Qty Below 0` | 当数量降至零以下时，将接受延交订单。 |
     | `Allow Qty Below 0 and Notify Customer` | 当数量低于零时，系统会接受延交订单，并通知客户仍然可以下达订单。 |

   - 输入 **[!UICONTROL Maximum Qty Allowed in Shopping Cart]**.

   - 输入金额 **[!UICONTROL Out-of-Stock Threshold]**：

     | 值 | 描述 |
     | ----- |-----|
     | 正数 | 禁用“延交订单”后，请输入正金额。 |
     | 零 | 启用延交订单后，输入 `0` 允许无限延交。 |
     | 负金额 | 启用延交订单后，建议输入负金额。 该金额将添加到可销售数量。 例如，输入 `-50` 允许订单数量不超过此金额。 |

   - 输入 **[!UICONTROL Minimum Qty Allowed in Shopping Cart]** 选定组和金额。

   - 对象 **[!UICONTROL Notify for Quantity Below]**，输入触发物料缺货通知的库存级别。

   - 要激活产品的数量增量，请设置 **[!UICONTROL Enable Qty Increments]** 到 `Yes`. 然后，用于 **[!UICONTROL Qty Increments]**，输入为了满足要求而必须购买的项目数。

     例如，以6为增量销售的物料可以按数量购买 `6`， `12`， `18`，等等。

   - 对象 [!DNL Inventory Management]， **[!UICONTROL Automatically Return Credit Memo Item to Stock]** 设置为 `No`. 在提交贷项通知单时，您可以输入并选择将库存退回给来源。

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Admin bulk operations]** 并设置以下选项：

   ![管理员批量操作](assets/config-catalog-inventory-admin-bulk-operations.png){width="600" zoomable="yes"}

   - 设置 **[!UICONTROL Run asynchronously]** 要为批量产品操作异步运行批量操作

     这些操作包括批量 [分配和取消分配源](bulk-assignment.md)、和 [将库存转移到来源](inventory-transfer.md). 它会收集批量操作（最大为异步批次大小），然后运行这些操作。 默认禁用此选项。建议在启用之前检查批量操作的性能。

     >[!NOTE]
     >
     >配置和支持 _异步队列管理器_&#x200B;中，您必须使用命令行发出命令。 此步骤可能需要开发人员帮助。 请参阅 [启动消息队列使用者](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/start-message-queues.html) 在 _配置指南_.

   - 如果启用，请设置 **[!UICONTROL Asynchronous batch size]**. 默认批次大小为100。 当批量进程达到此数量时，系统会触发该数量。

1. 完成后，单击 **[!UICONTROL Save Config]**.

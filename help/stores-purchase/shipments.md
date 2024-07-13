---
title: 装运
description: 了解如何为发票创建发运记录并取消发运。
exl-id: 6df83549-ba38-43f7-aab1-dbf3f6b89d74
feature: Shipping/Delivery, Invoices
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '948'
ht-degree: 0%

---

# 装运

_[!UICONTROL Shipments]_网格列出了已准备要装运的所有发票的装运记录。 当订单为[开票](invoices.md)或更高版本时，可以生成装运记录。

Adobe Commerce和Magento Open Source支持部分或全部订单装运，并且还提供[Inventory management](../inventory-management/introduction.md)和第三方扩展中的其他选项。

![装运网格](./assets/shipments.png){width="600" zoomable="yes"}

## 列描述

| 列或控件 | 描述 |
|--- |--- |
| [!UICONTROL Select] | 选中要执行操作的每个报价的复选框，或使用列标题中的选择控件。 选项： `Select All` / `Deselect All` |
| [!UICONTROL Shipment] | 首次保存新装运时分配的唯一连续编号 |
| [!UICONTROL Ship Date] | 配送日期 |
| [!UICONTROL Order] | 订单的唯一编号 |
| [!UICONTROL Order Date] | 下订单的日期和时间 |
| [!UICONTROL Ship-to Name] | 接收订单的人员姓名 |
| [!UICONTROL Total Quantity] | 要装运的物料总数 |
| [!UICONTROL Action] | 查看以编辑模式打开装运 |

{style="table-layout:auto"}

其他列：

| 列 | 描述 |
|--- |--- |
| [!UICONTROL Order Status] | 指示订单状态 |
| [!UICONTROL Purchased From] | 指示下订单的网站、商店和商店视图 |
| [!UICONTROL Customer Name] | 下订单的客户或购买者的名称 |
| [!UICONTROL Email] | 注册客户的电子邮件地址 |
| [!UICONTROL Customer Group] | 客户分配到的客户组或共享目录的名称 |
| [!UICONTROL Billing Address] | 下订单的客户或购买者的名称 |
| [!UICONTROL Shipping Address] | 接收订单的人员姓名 |
| [!UICONTROL Payment Method] | 订单使用的付款方式 |
| [!UICONTROL Shipping Information] | 用于装运订单的方法 |

{style="table-layout:auto"}

## 创建装运

以下说明将指导您完成在Adobe Commerce或Magento Open Source中创建装运的过程。 如果已启用Inventory management，则可能需要复查[创建多Source发运](../inventory-management/shipments-create.md)，并选择源（或地点）和每个行项目要发送的数量。

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Sales]** > **[!UICONTROL Orders]**。

1. 在网格中查找顺序并将其打开。

1. 如果订单已付费、已开票并准备发货，请单击&#x200B;**[!UICONTROL Ship]**。

   装运顶部的部分包含销售订单中的名称、地址和付款信息。

1. 按照以下各节中的说明完成装运单的各个部分。

### [!UICONTROL Items to Ship]

对于订单中的每个行项目，根据需要修改&#x200B;**[!UICONTROL Qty to Ship]**。

### [!UICONTROL Shipping Information]

**方法1：**&#x200B;使用订单页

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Sales]** > **[!UICONTROL Orders]**。

1. 在选定订单的&#x200B;**[!UICONTROL Action]**&#x200B;列中，单击&#x200B;**[!UICONTROL View]**。

1. 单击&#x200B;**[!UICONTROL Ship]**。

1. 向下滚动到&#x200B;_[!UICONTROL Payment & Shipping Method]_块并单击&#x200B;**[!UICONTROL Add Tracking Number]**。

1. 设置&#x200B;**[!UICONTROL Carrier]**：

   - `Custom Value`
   - `DHL`
   - `Federal Express`
   - `United Parcel Service`
   - `United States Postal Service`

1. 要跟踪装运，请输入&#x200B;**[!UICONTROL Title]**&#x200B;和&#x200B;**[!UICONTROL Number]** 。

**方法2：**&#x200B;使用装运页

仅当已从订单页创建订单发运时，才允许使用此方法。
您可以使用直接发运页面根据需要修改发运和跟踪信息：

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Sales]** > **[!UICONTROL Shipments]**。

1. 在编辑模式下查找并打开装运。

1. 向下滚动到&#x200B;_[!UICONTROL Payment & Shipping Method]_块。

1. 选择&#x200B;**[!UICONTROL Carrier]**。

1. 输入包的&#x200B;**[!UICONTROL Title]**。

1. 输入跟踪&#x200B;**[!UICONTROL Number]**。

1. 单击&#x200B;**[!UICONTROL Add]**。

1. 若要向客户发送包含跟踪信息的电子邮件，请单击&#x200B;**[!UICONTROL Send Tracking Information]**，然后确认操作。

   若要跟踪任何装运的位置，请在编辑模式下打开所需的装运，然后单击&#x200B;**[!UICONTROL Track this shipment]**。

   ![送货和跟踪信息](./assets/tracking-information.png){width="600" zoomable="yes"}

### 按钮

| 按钮 | 描述 |
|--- |--- |
| **[!UICONTROL Back]** | 关闭“新建发运”表单，并返回至订单 |
| **[!UICONTROL Submit Shipment]** | 添加订单的装运。 |
| **[!UICONTROL Reset]** | 将所有字段恢复为原始值。 |

{style="table-layout:auto"}

### 送货备注

1. 如果需要，请为装运输入&#x200B;**注释**。

1. 装运就绪后，单击&#x200B;**提交装运**。

## 设置装运的注释

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在&#x200B;_[!UICONTROL Sales]_下，选择&#x200B;**[!UICONTROL Sales Email]**。

1. 展开&#x200B;**装运注释**&#x200B;部分，并根据需要修改设置：

   ![装运注释配置](../configuration-reference/sales/assets/sales-emails-shipment-comments.png){width="600" zoomable="yes"}

   - 默认情况下，**[!UICONTROL Enabled]**&#x200B;选项设置为`Yes`，这意味着在输入送货注释时将电子邮件发送给客户。

   - 对于&#x200B;**[!UICONTROL Shipment Comment Email Sender]**，选择发送装运注释电子邮件的发件人。 默认提供五个电子邮件地址。

   - 对于&#x200B;**[!UICONTROL Shipment Comment Email Template]**，请根据需要选择模板或选择默认选项。

   - 对于&#x200B;**[!UICONTROL Shipment Comment Email Template for Guests]**，请选择用于商店中没有帐户的客户的模板。

   - 对于&#x200B;**[!UICONTROL Shipment Comment Email Copy To]**，请输入发送装运注释电子邮件副本的电子邮件地址。 用逗号分隔多个电子邮件地址。

   - 对于&#x200B;**[!UICONTROL Shipment Comment Email Copy Method]**，根据您的喜好选择`bcc` （密件抄送）或`separate email copy`方法。

1. 单击&#x200B;**[!UICONTROL Save Config]**。

## 取消装运

在将货物分派给承运人之前，如果承运人支持取消，则可以通过打开订单并导航到货物来取消货物。 有些运营商会在预订后限制取消次数。 例如，UPS允许取消，但要求在预订装运后等待24小时。 如果取消发运，则无法撤消取消。 唯一的办法是重新创建订单。

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Sales]** > **[!UICONTROL Orders]**。

1. 在网格中查找顺序。

1. 在&#x200B;_操作_&#x200B;列中，选择&#x200B;**[!UICONTROL View]**。

1. 在左侧面板中，选择&#x200B;**[!UICONTROL Shipments]**。

   如果可以取消装运，则顶部按钮栏中会显示&#x200B;_[!UICONTROL Cancel Shipment]_作为选项。

1. 单击&#x200B;**[!UICONTROL Cancel Shipment]**。

1. 提示确认时，单击&#x200B;**[!UICONTROL OK]**。

装运的状态更改为`Canceled`。 如果承运人不支持取消，则会出现一条错误消息，并解释为何无法取消发运。

## 装运字段描述

### [!UICONTROL Shipping Information]

| 字段 | 描述 |
|-----|-----------|
| [!UICONTROL Carrier] | 所选运营商的名称 |
| [!UICONTROL Title] | 运营商分配给包装的描述性名称。 |
| [!UICONTROL Number] | 分配给包的链接跟踪编号。 |
| [!UICONTROL Action] | ![垃圾桶图标](../assets/icon-delete-trashcan-solid.png) — 从装运记录中删除包信息。 |
| [!UICONTROL Add] | 向装运添加另一个包装。 |

{style="table-layout:auto"}

### [!UICONTROL Route Information]

| 字段 | 描述 |
|-----|-----------|
| [!UICONTROL Origin Location] | 显示可用位置的列表。 |
| [!UICONTROL International] | 如果选中，则将装运标识为国际装运。 |

{style="table-layout:auto"}

### [!UICONTROL Items Ordered]

| 字段 | 描述 |
|-----|-----------|
| [!UICONTROL Description] | 物料的描述。 |
| [!UICONTROL SKU] | 物料的库存单位。 |
| [!UICONTROL Weight] | 物料的重量。 |
| [!UICONTROL Qty Ordered] | 已订购的物料数量。 |
| [!UICONTROL Qty Shipped] | 已发运的项目数量。 |
| [!UICONTROL Qty Packed] | 此包中包含的项目数。 |

{style="table-layout:auto"}

### [!UICONTROL Shipment Comments]

| 字段 | 描述 |
|-----|-----------|
| [!UICONTROL Comments] | 有关装运的注释供内部使用。 |

{style="table-layout:auto"}

### [!UICONTROL Documentation]

| 字段 | 描述 |
|-----|-----------|
| [!UICONTROL Package Label] | **PNG** — 下载装运包标签。 尺寸：A6（105 x 148毫米；4.1 x 5.6英寸） |

{style="table-layout:auto"}

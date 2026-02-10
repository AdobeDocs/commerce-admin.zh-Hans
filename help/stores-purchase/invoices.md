---
title: 发票
description: 了解如何创建和打印发票，以支持订单处理和客户服务操作。
exl-id: 6141b182-1467-4416-a07f-864333318428
feature: Invoices, Admin Workspace
source-git-commit: 80cc27c4247230eb5e43bca46a34d358f9f0bcea
workflow-type: tm+mt
source-wordcount: '1181'
ht-degree: 0%

---

# 发票

发票是订单付款记录的记录。 可以为单个订单[创建多张发票](#create-an-invoice)，每张发票可以包含您指定的任意数量的已购产品。 您还可以创建[打印就绪的PDF发票](#print-invoices)作为客户的销售单据。

在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Sales]** > _操作_ > **发票**&#x200B;以打开&#x200B;_发票_&#x200B;网格并访问您创建的发票。

![发票网格](./assets/invoices.png){width="700" zoomable="yes"}

## 列描述

| 列 | 描述 |
|--- |--- |
| [!UICONTROL Select] | 选中要执行操作的引号对应的复选框，或使用列标题中的选择控件。 选项： `Select All` / `Deselect All` |
| [!UICONTROL Invoice] | 在管理员提交发票时分配的唯一数字标识符。 查看发票详细信息时，此编号将显示在页面顶部，而不是报价单名称。 |
| [!UICONTROL Invoice Date] | 管理员首次提交发票的日期和时间。 |
| [!UICONTROL Order#] | 买方下订单时分配的唯一数字标识符。 查看发票详细信息时，此编号将显示为“订单和帐户信息”块中的链接。 |
| [!UICONTROL Order Date] | 客户首次成功下订单的日期和时间。 |
| [!UICONTROL Bill-to Name] | 负责支付订单的人员姓名。 |
| [!UICONTROL Status] | 指示发票的当前状态。 只能通过买方或卖方一方采取行动来更改状态。 |
| [!UICONTROL Grand Total (Base)] | 要购买的产品总价。 总金额以网站的基本货币和店面的货币显示。 |
| [!UICONTROL Grand Total (purchase)] | 订单中购买的产品总数。 总金额以网站的基本货币和店面的货币显示。 |
| [!UICONTROL Purchased From] | 从中创建发票的网站/商店/商店视图。 |
| [!UICONTROL Billing Address] | 下订单的客户的帐单地址。 |
| [!UICONTROL Shipping Address] | 将发运订单的地址。 |
| [!UICONTROL Customer Name] | 接收发票的客户的姓氏。 |
| [!UICONTROL Email] | 接收发票的客户的电子邮件地址。 |
| [!UICONTROL Customer Group] | 分配给接收发票的客户的客户组。 |
| [!UICONTROL Payment Method] | 用于付款的付款方式。 |
| [!UICONTROL Shipping Information] | 用于装运订单的方法。 |
| [!UICONTROL Subtotal] | 订单小计，不包括运费和手续费以及税金。 |
| [!UICONTROL Shipping and Handling] | 运费和包装费。 |
| [!UICONTROL Action] | **[!UICONTROL View]** — 在编辑模式下打开发票。 |

{style="table-layout:auto"}

## 创建发票

为订单创建发票会将其移至无法取消或更改的状态。 新发票页类似于已完成的订单，带有一些其他字段。 发票的“备注”部分中记录了每个与订单相关的活动。

通常，在发运流程开始时，系统会为订单开票并获取订单。 如果付款方式是采购订单，或者如果[付款操作](../configuration-reference/sales/payment-methods.md#payment-actions)设置为`Authorize and Capture`，则将对订单开票并在结帐期间捕获付款。 您可以生成带装箱单的发票，也可以从承运人帐户打印发运标签。 单个订单可以分为部分发运，如有必要，这些发运将单独开票。

当新订单的状态设置为`Processing`时，_自动为所有项目开票_&#x200B;的选项在配置中变得可用。 当[付款操作](../configuration-reference/sales/payment-methods.md#payment-actions)设置为`Authorize and Capture`时，某些信用卡付款方法会在流程中完成开票步骤。 在这种情况下，不会出现“发票”按钮，并且订单已准备就绪，可以发运。

>[!NOTE]
>
>对于使用`Gift Card`、`Store Credit`、`Reward Points`或其他离线付款方式下单的订单，不会自动创建发票。

必须先生成订单发票，然后才能打印该发票。 要查看或打印PDF，请先下载并安装PDF阅读器，如[Adobe Acrobat Reader](https://www.adobe.com/acrobat/pdf-reader.html "获取Adobe Reader")。

**_为订单开票:_**

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**。

1. 在网格中查找状态为`Processing`的销售订单。 然后，执行以下操作：

1. 在&#x200B;_操作_&#x200B;列中，单击&#x200B;**[!UICONTROL View]**。

1. 在销售订单的标题中，选择&#x200B;**[!UICONTROL Invoice]**&#x200B;选项。

   >[!NOTE]
   >
   >将您的特定&#x200B;_[!UICONTROL Invoice]_付款方式[的](../configuration-reference/sales/payment-methods.md#payment-actions)付款操作[设置为](../configuration-reference/sales/payment-methods.md)时，不会显示`Authorize and Capture`选项，该付款方式会自动生成发票。 如果下达了订单并且付款方法的付款活动设置为`Authorize`并且已对订单开票，情况也是如此。

   ![发票销售订单](./assets/invoice-sales-order.png){width="700" zoomable="yes"}

   新发票页类似于已完成的订单页，带有可编辑的附加字段。

1. 如果物料准备发运，则在创建发票的同时生成发运的装箱单：

   - 在&#x200B;_送货信息_&#x200B;部分中，单击&#x200B;**[!UICONTROL Create Shipment]**&#x200B;复选框以将其选中。

     在生成发票的同时创建装运记录。

   - 包括一个跟踪号：

      - 单击&#x200B;**[!UICONTROL Add Tracking Number]**。
      - 输入跟踪信息： _[!UICONTROL Carrier]_、_[!UICONTROL Title]_&#x200B;和&#x200B;_[!UICONTROL Number]_

     ![创建Fedex装运](./assets/invoice-create-shipment-fedex.png){width="600" zoomable="yes"}

   - （可选）生成部分发票：

      - 在&#x200B;_发票项目_&#x200B;部分中，更新&#x200B;**[!UICONTROL Qty to Invoice]**&#x200B;列以仅包含发票上的特定项目。
      - 然后，单击&#x200B;**[!UICONTROL Update Qty's]**。

        ![发票项目](./assets/invoice-items-to-invoice.png){width="600" zoomable="yes"}

1. 如果订单使用了在线付款方式，请将&#x200B;**[!UICONTROL Amount]**&#x200B;设置为相应的选项。

1. 要在生成发票时通过电子邮件通知客户，请执行以下操作：

   - 选中&#x200B;**[!UICONTROL Email Copy of Invoice]**&#x200B;复选框。

   - 输入任意&#x200B;**[!UICONTROL Invoice Comments]**。 要在通知电子邮件中包含注释，请标记&#x200B;**[!UICONTROL Append Comments]**&#x200B;复选框。

1. 完成后，单击页面底部的&#x200B;**[!UICONTROL Submit Invoice]**。

   **_在线付款方式:_**

   ![提交发票 — 联机付款方式](./assets/invoice-submit-invoice-capture-online.png){width="600" zoomable="yes"}

   **_离线付款方式:_**

   ![提交发票 — 脱机付款方式)](./assets/invoice-submit-invoice.png){width="600" zoomable="yes"}

   订单的状态从`Pending`更改为`Complete`。

   ![已完成发票摘要](./assets/invoice-complete.png){width="600" zoomable="yes"}

## 打印发票

发票可以单独打印，也可以作为批打印。 但是，必须先为订单生成发票，然后才能打印发票。 您可以为可供打印的PDF发票上传高分辨率徽标，并在标题中包含[订单ID](../stores-purchase/sales-documents.md#add-reference-ids)。 若要使用您的徽标和地址自定义发票模板，请参阅[PDF徽标要求](../stores-purchase/sales-documents.md#image-formats)。

>[!NOTE]
>
>要查看或打印PDF，您必须具有PDF阅读器。 您可以免费下载[Adobe Reader](https://www.adobe.com/acrobat/pdf-reader.html "获取Adobe Reader")。

### 打印单张发票

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Invoices]**。

1. 在&#x200B;_[!UICONTROL Invoices]_网格中，找到发票，然后单击&#x200B;**[!UICONTROL View]**操作_&#x200B;列中的&#x200B;_。

1. 在发票顶部，单击&#x200B;**[!UICONTROL Print]**&#x200B;以生成发票的PDF。

1. 将生成的PDF保存至文件或打印该文件。

### 打印多张发票

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Invoices]**。

1. 在&#x200B;_[!UICONTROL Invoices]_网格中，选中要打印的每张发票所对应的复选框。

1. 将&#x200B;**[!UICONTROL Actions]**&#x200B;控件设置为`PDF Invoices`。

   ![打印多张发票](./assets/invoices-print-batch.png){width="600" zoomable="yes"}

这些发票保存在一个PDF文件中，可将其发送到打印机或进行保存。

## 自定义捕获金额

仅[!BADGE SaaS]{type=Positive url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="仅适用于Adobe Commerce as a Cloud Service项目(Adobe管理的SaaS基础架构)。"}

为了向商家提供更大的灵活性以用于部分捕获和专用支付方案，发票API支持使用扩展属性的自定义捕获金额。

您可以在创建发票时发起REST调用以捕获自定义金额。  使用[`POST V1/order/:orderId/invoice`](https://developer.adobe.com/commerce/webapi/reference/rest/saas/) REST终结点并在有效负载的`extension_attributes.custom_capture_amount`字段中指定自定义数量。

>[!NOTE]
>
>请联系您的支持代表以启用此功能。
>
>由于法律限制，自定义捕获金额仅在北美(NA)地区和允许付款超额捕获的其他地区可用。

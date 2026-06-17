---
title: 配送标签
description: 了解定期装运和带退货授权产品的装运标签工作流。
exl-id: 5da03cf9-5e92-4bb8-ba53-67c6469665ed
feature: Shipping/Delivery, Orders
TQID: https://experienceleague.adobe.com/Cjf9-372TRGIfWXpWR20OUII5XorPdfO1qgG-b2yPYI
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 314
ht-degree: 0%

---

# 配送标签

Commerce包括与主要运输运营商的高级集成，让您能够访问运营商运输系统以跟踪订单、创建运输标签等。 可为常规装运和获退货商品授权的产品创建装运标签。 除了航运承运人提供的信息外，标签还包括Commerce订单号、包裹编号和航运的包裹总数。

![USPS优先送货标签](./assets/shipping-usps-priority-label.png){width="300"}

- [配置配送标签](shipping-label-configure.md)
- [创建装运标签和包装](shipping-label-create.md)

## 装运标签工作流

可以在创建装运时或稍后生成装运标签。 装运标签以PDF格式存储，并下载到您的计算机。

### 步骤1：商家提交发运标签请求

商家/商店经理完成生成标签所需的信息，并提交请求。

### 步骤2：请求已发送到运营商

Commerce与装运承运人联系，并在该承运人的系统中创建订单。 系统会为每个已发运的包创建单独的订单。

### 步骤3：运营商发送标签和跟踪号

承运人发送装运的装运标签和跟踪编号。

- 具有多个包装的单个装运可接收多个装运标签。

- 如果多次生成相同的配送标签，则会保留原始跟踪编号。

- 对于退回的具有RMA编号的产品，旧的跟踪编号将替换为新的跟踪编号。

### 步骤4：商家下载并打印标签

生成装运标签后，保存新装运并打印标签。 如果由于连接问题或任何其他原因无法创建装运标签，则不会创建装运。 根据您的浏览器设置，可以打开和打印PDF文件。 在PDF中，每个标签都会显示在单独的页面上。

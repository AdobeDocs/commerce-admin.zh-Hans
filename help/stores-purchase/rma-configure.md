---
title: 配置退货
description: 了解如何为您的商店启用退货并配置支持的配送方式。
exl-id: a1b508fc-7e42-4d37-bf7e-dea17a40d39b
feature: Returns, Configuration
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '353'
ht-degree: 0%

---

# 配置退货

{{ee-feature}}

启用后，客户可以从店面提交RMA请求。 仅当订单中存在可用于退货的项目时，才能生成RMA。 返回单个项目的请求由管理 _启用RMA_ 属性。 默认情况下，配置设置将应用于产品(_[!UICONTROL Use Config Settings]_（已选中）。 如果_[!UICONTROL Enable RMA]_ 设置为 `No`，则该产品不会出现在可返回的项目列表中。 如果您更改 _启用RMA_ 设置，它同时适用于新订单和现有订单。

## 为您的存储启用RMA

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中，展开 **[!UICONTROL Sales]** 并选择 **[!UICONTROL Sales]** 下方。

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL RMA Settings]** 部分。

   ![RMA设置](../configuration-reference/sales/assets/sales-rma-settings.png){width="600" zoomable="yes"}

1. 设置 **[!UICONTROL Enable RMA on Storefront]** 到 `Yes`.

   该设置确定客户是否可以从店面创建和查看RMA请求。 RMA可同时应用于新订单和现有订单。

1. 设置 **[!UICONTROL Enable RMA on Product Level]** 到 `Yes`.

   此设置确定 _启用RMA_ 店面中各个产品的属性：

   - 时间 [!UICONTROL Enable RMA on Product Level] 设置为 `Yes`，店面客户可返回所有单个产品。 它包含两者 _[!UICONTROL Enable RMA]_= `Yes` 和_[!UICONTROL Enable RMA]_ = `No` 产品属性值。
   - 时间 [!UICONTROL Enable RMA on Product Level] 设置为 `No`，店面的客户只能返回带有 _[!UICONTROL Enable RMA]_= `Yes` 产品属性值。

1. 设置 **[!UICONTROL Use Store Address]** 更改为下列值之一：

   - `Yes`  — 将返回的产品发送到商店地址。
   - `No`  — 输入产品退货的替代地址。

   ![具有备用地址的RMA设置](../configuration-reference/sales/assets/sales-rma-settings.png){width="600" zoomable="yes"}

1. 单击 **[!UICONTROL Save Config]**.

## 配置退货的配送方式

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中，展开 **[!UICONTROL Sales]** 并选择 **[!UICONTROL Delivery Methods]**.

1. 展开要用于退货服务的承运人的部分，例如 **[!UICONTROL UPS]**.

   ![为运营商启用RMA服务](./assets/rma-delivery-method.png){width="600" zoomable="yes"}

1. 设置 **[!UICONTROL Enabled for RMA]** 到 `Yes`.

1. 单击 **[!UICONTROL Save Config]**.

## 在产品级别更改允许的RMA

如果为商店启用RMA，并且目录中包含一些不允许退货的产品，则可以在产品级别修改设置，

1. 在编辑模式下打开产品。

1. 向下滚动并展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Autosettings]** 部分。

1. 清除 **[!UICONTROL Use Config Setting]** 复选框（如果需要）。

1. 切换 **[!UICONTROL Enable RMA]** 将设置为 `No`.

   ![为产品禁用RMA](./assets/product-advanced-autosettings-enable-rma.png){width="600" zoomable="yes"}

1. 单击 **[!UICONTROL Save]**.

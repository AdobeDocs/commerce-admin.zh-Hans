---
title: 店内投放
description: 了解如何为商店设置店内投放选项。
exl-id: bd64b110-5c39-41c6-8a0c-38561b2a5bf4
feature: Shipping/Delivery
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '627'
ht-degree: 0%

---

# 店内投放

使用店内交货方法，客户可以在结账期间选择用作取货地点的来源。

![结账时的店内交付方法](./assets/luma-in-store-example.png){width="700" zoomable="yes"}

在店面结帐期间：

1. 客户点击 **[!UICONTROL Pick In Store]** 或选择 _[!UICONTROL In-Store Pickup Delivery]_配送方式。
1. 此 _[!UICONTROL Pick In Store]_“结帐”选项卡将打开。

客户有地址，或以前填写过送货地址表单后再切换到 _[!UICONTROL Pick In Store]_选项卡：

- 在配置的半径内，与客户地址最接近的来源会自动预选为提货商店。
- 客户点击时 **[!UICONTROL Select Other]**， _[!UICONTROL Select Store]_搜索表单打开。 在列表中仅显示与预先选定的商店之间的配置距离（半径）内的商店。 列表中的所有商店都按到预选商店的距离排序。
- 当客户在搜索字段中输入邮政编码或城市名称时，列表中只显示距搜索位置的配置距离（半径）内的商店。 列表中的所有存储都按到搜索位置的距离排序。
- 当客户从搜索字段清除邮政编码或城市名称时，分配给购物车中产品的所有提货商店都会显示给客户。 列表中的所有存储都按源代码的升序排序，没有任何距离（半径）限制。

如果客户没有地址或以前未填写送货地址表单，则切换到 _[!UICONTROL Pick In Store]_选项卡：

- 页面显示 _无法根据可用信息预先选择取车地点_ 消息。
- 客户点击时 **[!UICONTROL Select Store]**， _[!UICONTROL Select Store]_搜索表单打开。
- 分配给购物车中产品的所有提货商店按源代码的升序显示，没有任何距离（半径）限制。
- 当客户在搜索字段中输入邮政编码或城市名称时，列表中只显示距搜索位置的配置距离（半径）内的商店。 列表中的所有存储都按到搜索位置的距离排序。

## 设置之前

- 确保您拥有非默认库存和来源。 有关如何将源配置为接收位置的更多信息，请参阅 [添加源](../inventory-management/sources-add.md).
- 确保已配置距离优先级算法。 有关更多信息，请参阅 [配置距离优先级算法](../inventory-management/distance-priority-algorithm.md).
- 确保您拥有 [已下载和导入](../inventory-management/cli.md#import-geocodes) 用于离线计算的所有必要地理代码。
- 确保您已配置 [默认纳税目标计算](../configuration-reference/sales/tax.md#default-tax-destination-calculation) 设置。

>[!IMPORTANT]
>
>**在店面，搜索结果按距离（半径）过滤以显示相关结果：**<br><br>
>如果客户有送货地址，则计算距离（半径）的基本位置取自送货地址。<br><br>
>如果客户没有送货地址，则计算距离的基本地点取自 [默认纳税目标计算](../configuration-reference/sales/tax.md#default-tax-destination-calculation) 设置。 这些设置是按商店视图设置的，您必须配置默认纳税目标计算设置以确保拣选商店搜索正常工作。

## 设置店内投放

首先，检查是否已启用店内交付。

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中，展开 **[!UICONTROL Sales]** 并选择 **[!UICONTROL Delivery Methods]**.

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL In-Store Delivery]** 部分。

   ![店内投放](../configuration-reference/sales/assets/delivery-methods-in-store-delivery.png){width="600" zoomable="yes"}

1. 设置 **[!UICONTROL Enabled]** 到 `Yes`.

   >[!NOTE]
   >
   >如有需要，清除 **[!UICONTROL Use system value]** 复选框以更改任何字段的默认值。

1. 输入 **[!UICONTROL Method Name]** 描述用于生成装运估计的计算方法。

   方法名称显示在购物车中计算的预计费率旁边。

1. 输入 **[!UICONTROL Title]** 您希望显示的 _店内投放_ 部分。

   默认标题为 `In-Store Pickup Delivery`.

1. 要向客户收取店内接送服务的费用，请在 **[!UICONTROL Price]** 字段。

1. 输入 **[!UICONTROL Search Radius]** 以公里为单位，在店面结帐时搜寻店铺取货地点。

1. 对象 **[!UICONTROL Displayed Error Message]**，输入当店内投放变得不可用时显示的消息。

   默认消息为 `In-Store Delivery is not available. To use this delivery method, please contact us.`

1. 单击 **[!UICONTROL Save Config]**.

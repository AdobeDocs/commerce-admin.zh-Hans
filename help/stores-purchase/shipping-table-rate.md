---
title: 表格费率运费
description: 了解如何为您的商店设置表费率配送选项。
exl-id: f73adc9a-4c6c-477d-9553-3a3f28647bdd
feature: Shipping/Delivery
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '999'
ht-degree: 3%

---

# 表格费率运费

此 _表速率_ 发运方法引用数据表以根据各种条件的组合计算运费，包括：

- 权重v.目标
- 价格v.目标
- 项目数对目标

例如，如果您的仓库位于洛杉矶，则发往圣地亚哥的成本比发往佛蒙特州更低。 您可以使用表费率配送将节省额转嫁给客户。

用于计算表格比率的数据在电子表格中准备并导入到您的存储中。 当客户请求报价时，结果会显示在购物车的送货估价部分中。

>[!NOTE]
>
>一次只能激活一组表速率数据。

![购物车订单摘要中的表费率发运选项](./assets/storefront-cart-table-rate.png){width="700" zoomable="yes"}

## 步骤1：完成默认设置

第一步是完成表速率的默认设置。 您可以在不更改配置范围的情况下完成此步骤。

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在 _[!UICONTROL Sales]_部分，选择&#x200B;**[!UICONTROL Delivery Methods]**.

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Table Rates]** 部分。

   >[!NOTE]
   >
   >如有必要，请先清除 **[!UICONTROL Use system value]** 复选框，以按所述更改以下设置。

   ![表费率](../configuration-reference/sales/assets/delivery-methods-table-rates.png){width="600" zoomable="yes"}

1. 设置 **[!UICONTROL Enabled]** 到 `Yes`.

1. 输入 **[!UICONTROL Title]** 您希望在结账期间针对表费率部分显示的附加费。

   默认标题为 `Best Way`.

1. 输入 **[!UICONTROL Method Name]** ，以标签形式显示在购物车的计算费率旁边。

1. 设置 **[!UICONTROL Condition]** 更改为以下计算方法之一：

   - `Weight v. Destination`
   - `Price v. Destination`
   - `Number of Items v. Destination`

1. 对于包含虚拟产品的订单，请设置 **[!UICONTROL Include Virtual Products in Price Calculation]** 到 `Yes` 如果您希望能够在计算中包括虚拟产品。

   >[!NOTE]
   >
   >由于虚拟产品（如服务）没有权重，因此它们无法更改基于“权重v.目标”条件的计算结果。 但是，虚拟产品可以更改基于“价格v.目标”或“项目数vs.目标”条件的计算结果。

1. 根据您的要求配置手续费选项。

   手续费是可选的，显示为添加到运输成本中的额外费用。 如果要包括手续费，请执行以下操作：

   - 设置 **[!UICONTROL Calculate Handling Fee]**：

      - `Fixed`
      - `Percent`

   - 输入 **[!UICONTROL Handling Fee]** 根据用于计算费用的方法的费率。

     例如，如果费用基于固定费用，则以小数形式输入金额，如 `4.90`. 但是，如果手续费基于订单的百分比，则按百分比输入金额。 例如，如果您对订单的6%计费，则输入值为 `.06`.

1. 如果需要，请更改 **[!UICONTROL Displayed Error Message]**.

   此文本框已预设为默认消息，但您可以输入其他消息，以便在此投放方法不可用时显示。

1. 设置 **[!UICONTROL Ship to Applicable Countries]**：

   - `All Allowed Countries`  — 来自所有客户的客户 [国家/地区](../getting-started/store-details.md#country-options) 在商店配置中指定的可使用此投放方法。
   - `Specific Countries`  — 选择此选项时， _[!UICONTROL Ship to Specific Countries]_列表出现。 选择列表中可使用此投放方法的每个国家/地区。

1. 设置 **[!UICONTROL Show Method if Not Applicable]** 到 `Yes` 如果要始终显示表费率

1. 对象 **[!UICONTROL Sort Order]**，请输入一个数字以确定在结账期间与其他交付方法一起列出表费率传送时的显示顺序。

   `0` =第一个， `1` =秒， `2` =第三，依此类推。

1. 单击 **[!UICONTROL Save Config]**.

## 步骤2：准备表速率数据

1. 在左上角，设置 **[!UICONTROL Store View]** 到 `Main Website`，或适用于配置适用的任何其他网站。

   >[!NOTE]
   >
   >如有必要，请首先取消选择 **[!UICONTROL Use system value]** 复选框，以按所述更改以下设置。

1. 更改 **[!UICONTROL Condition]** 根据需要。

1. 单击 **[!UICONTROL Export CSV]**.

   ![导出CSV](./assets/shipping-table-rates-export.png){width="700" zoomable="yes"}

1. 保存 `tablerates.csv` 文件到您的系统。

1. 在电子表格应用程序中打开文件。

1. 使用适合装运计算条件的值填写该表。

   - 使用星号(*)作为通配符，表示任何类别中的所有可能值。
   - 此 _[!UICONTROL Country]_列必须包含 [有效的三字符代码][1] 每一行。
   - 数据排序依据 _[!UICONTROL Region/State]_因此，特定位置位于列表顶部，通配符位置位于底部。 使用此方法会先处理具有绝对值的规则，稍后再处理通配符值。
   - 中的值 _[!UICONTROL Weight (and above)]_列最多可以有四位小数(例如 `2.5075`)。 在数据中使用更多小数位会导致导入失败。

   ![重量与目的地（澳大利亚）](./assets/table-rates-weight-destination-csv.png){width="500"}

1. 保存 `tablerates.csv` 文件。

## 步骤3：导入表费率数据

1. 返回到 **[!UICONTROL Table Rates]** 区域进行存储配置。

1. 在左上角，设置 **[!UICONTROL Store View]** 到使用此方法的网站。

1. 对象 **[!UICONTROL Import]**，单击 **[!UICONTROL Choose File]** 并选择您完成的 `tablerates.csv` 文件导入费率。

   ![导入表费率](./assets/shipping-table-rates-import.png){width="600" zoomable="yes"}

1. 单击 **[!UICONTROL Save Config]**.

## 步骤4：验证费率

为确保表费率数据正确，请使用多个不同的地址完成付款流程，以确保正确计算运费和包装费。

### 示例1：价格和目标

此示例使用Price v. Destination条件根据美国大陆、阿拉斯加和夏威夷的订单小计金额创建一组三种不同的运费。 星号(*)是表示所有值的通配符。

| 国家/地区 | 地区/州 | 邮政编码 | 订单小计（及以上） | 运费 |
|--- |--- |--- |--- |--- |
| 美国 | 您好 | * | 100 | 10 |
| 美国 | 您好 | * | 50 | 15 |
| 美国 | 您好 | * | 0 | 20 |
| 美国 | AK | * | 100 | 10 |
| 美国 | AK | * | 50 | 15 |
| 美国 | AK | * | 0 | 20 |
| 美国 | * | * | 100 | 5 |
| 美国 | * | * | 50 | 10 |
| 美国 | * | * | 0 | 15 |

{style="table-layout:auto"}

### 示例2：权重和目标

此示例使用“重量v.目标”条件根据订单的重量创建不同的发运费率。

| 国家/地区 | 地区/州 | 邮政编码 | 权重（及以上） | 运费 |
|--- |--- |--- |--- |--- |
| AUS | NT | * | 9 | 39.95 |
| AUS | NT | * | 0 | 19.95 |
| AUS | VIC | * | 9 | 19.95 |
| AUS | VIC | * | 0 | 5.95 |
| AUS | 华盛顿 | * | 9 | 39.95 |
| AUS | 华盛顿 | * | 0 | 19.95 |
| AUS | * | * | 9 | 29.95 |
| AUS | * | * | 0 | 9.95 |

{style="table-layout:auto"}

### 示例3：限制美国大陆的免费运输

1. 创建 `tablerates.csv` 包含您愿意提供免费送货服务的所有州目的地的文件。

1. 使用以下设置完成表速率配置：

   | 设置 | 值 |
   |----------|-------|
   | [!UICONTROL Condition] | `Price v. Destination` |
   | [!UICONTROL Method Name] | `Free Shipping` |
   | [!UICONTROL Ship to Applicable Countries] | `Specific Countries` |
   | [!UICONTROL Ship to Specific Countries] | `Select only United States` |
   | [!UICONTROL Show method if not applicable] | `No` |

   {style="table-layout:auto"}

1. 在左上角，设置 **[!UICONTROL Store View]** 到 `Main Website`，或适用于配置适用的任何其他网站。

1. 对象 **[!UICONTROL Import]**，单击 **[!UICONTROL Choose File]** 并选择您完成的 `tablerates.csv` 文件导入费率。


[1]: https://en.wikipedia.org/wiki/ISO_3166-1_alpha-3

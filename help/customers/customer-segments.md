---
title: 客户区段
description: 通过客户区段，您可以向特定客户动态显示内容和促销活动。
exl-id: b254a6ac-cb0b-46c1-9ef7-ffc97360a98e
source-git-commit: 0b9f394a792171e93ee72f3b4ebb904b96ea1051
workflow-type: tm+mt
source-wordcount: '484'
ht-degree: 0%

---

# 客户区段

客户区段允许您根据各种属性向特定客户动态显示内容和促销活动。 例如，客户地址、订单历史记录和购物车内容。 您可以根据具有购物车价格规则的目标区段优化营销计划。 您还可以生成报告并导出目标客户的列表。 由于客户区段信息会不断刷新，因此在您商店中购物时，客户可能会与区段相关联或取消关联。

要更好地了解[客户组](../customers/customer-groups.md)与客户区段之间的区别，请注意它们的使用位置：

|  | 客户区段 | 客户组 |
|--- |--- |--- |
| 目录价格规则 |  | ✔️ |
| 购物车价格规则 | ✔️ | ✔️ |
| 层价格 |  | ✔️ |
| 相关产品规则 | ✔️ |  |
| 动态块 | ✔️ |  |
| 奖励汇率 |  | ✔️ |
| 类别权限 |  | ✔️ |
| 邀请 |  | ✔️ |

{style="table-layout:auto"}

## 客户区段属性

客户区段属性的定义方式与购物车和目录价格规则类似。 对于要在客户区段条件中使用的属性，_[!UICONTROL Use in Customer Segment]_[属性](attribute-properties.md#)必须设置为`Yes`。 客户区段条件可以合并以下类型的属性：

| 属性 | 描述 |
|---|---|
| `Customer Address Fields` | 您可以定义任何地址字段，如城市或国家/地区。 客户通讯簿中的任何地址都可以匹配这些条件，以便客户匹配。 或者，您可以指定仅使用默认帐单或送货地址来匹配客户。 客户地址属性仅适用于登录到其帐户的客户。 |
| `Customer Information Fields` | 可以定义其他客户信息，包括客户组、名称、电子邮件、新闻稿订阅状态和商店贷方余额。 客户信息仅适用于登录到其帐户的客户。 |
| `Cart Fields` | 购物车属性可以基于购物车内容的数量（行项目或总数量）或值（例如总计、税和礼品卡）。 |
| `Products` | 您可以引用当前位于购物车或愿望清单中的产品，或者以前查看过或订购过的产品。 您还可以设置发生该事件的日期范围。 使用产品属性定义产品。 |
| `Order Fields` | 可以根据订单中的帐单/发运地址、订单的总额（或平均值）或数量或订单总数来定义过去订单的订单特性。 您还可以设置发生日期范围，以及符合这些条件的订单的订单状态。 仅适用于已登录的客户。 为未登录的购物者设置的条件在登录时停止工作。 |

{style="table-layout:auto"}

有关定义客户区段的详细信息，请参阅[创建和删除客户区段](../customers/customer-segment-create.md)。

## eBooks

- **客户分段** — 获取[电子书](https://business.adobe.com/cn/resources/identifying-your-most-profitable-customers-introduction-customer-segmentation.html)以了解如何提高利润和整体客户满意度。
- **分段策略** — 获取[电子书](https://business.adobe.com/cn/resources/3-segmentation-tactics-ignite-conversion.html)以改进消息和促销活动的定位，从而与客户进行有意义的对话。

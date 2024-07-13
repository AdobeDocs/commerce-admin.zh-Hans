---
title: "[!UICONTROL My Purchase Orders]"
description: 了解采购订单以及公司如何使用它们管理其采购。
exl-id: b7348bc8-b874-4642-a372-530883d9d94c
feature: B2B, Companies, Purchase Orders
source-git-commit: c94d4e8d13c32c1c1b1d37440fdb953c8527b76c
workflow-type: tm+mt
source-wordcount: '475'
ht-degree: 0%

---

# [!UICONTROL My Purchase Orders]

当为公司](purchase-order-flow.md)启用采购订单时，[客户登录到公司用户帐户的任何订单都会自动创建为采购订单(PO)。 具有所需权限的公司用户可以创建、编辑和删除他们创建的PO，以及下属用户创建的PO。

![我的采购订单](./assets/account-dashboard-my-purchase-orders.png){width="700" zoomable="yes"}

>[!NOTE]
>
>采购订单在创建订单时创建物料价格、折扣和装运价格的&#x200B;_快照_。 如果项目价格在创建PO后发生变化，则使用原始价格。

## 管理采购订单

从&#x200B;_查看采购订单_&#x200B;页面，客户可以根据其[角色权限](account-company-roles-permissions.md)管理该PO。

- 要查看PO，请单击&#x200B;**[!UICONTROL View]**。
- 要查看有关PO的任何备注，请单击&#x200B;**[!UICONTROL Comments]**&#x200B;选项卡。
- 要查看完整的订单历史记录，请单击&#x200B;**[!UICONTROL History Log]**&#x200B;选项卡。

>[!IMPORTANT]
>
>如果采购订单中的物料缺货，或可用数量不足，则在采购订单转换为实际订单时，会发生错误。 如果启用了延交订单，则会正常处理订单。

## 从现有采购订单新建采购订单

如果客户具有现有的采购订单，并且希望添加新物料，则他们可以通过将新产品添加到新PO来生成重复的采购订单。 客户完成以下步骤：

1. 在&#x200B;_我的采购订单_&#x200B;页面上，客户找到该采购订单并单击&#x200B;**[!UICONTROL View]**&#x200B;链接。

1. 客户单击&#x200B;**[!UICONTROL Add Items to Shopping Cart]**。

   将打开“购物车”页面，其中列出了所有项目。

1. 进行任何添加或更改。

1. （可选）使用&#x200B;**[!UICONTROL Custom Reference Number]**&#x200B;向订单添加内部发票/PO编号。

1. 遵循正常的签出工作流并单击&#x200B;**[!UICONTROL Place Purchase Order]**。

如果在单击&#x200B;_[!UICONTROL Add Items to Shopping Cart]_时购物车中有商品，系统将显示一个对话框。 通过此对话框，他们可以选择将购物车项目与新项目合并，还是将购物车中的项目替换为PO中的项目。

如果不再需要原始采购订单，则可以将其关闭。

## 采购订单审批

对于根据公司结构或分配的公司角色指定为批准者的客户，_[!UICONTROL My Purchase Orders]_仪表板页面显示&#x200B;**[!UICONTROL Requires My Approval]**选项卡。 客户单击此标签可复查等待其批准的PO。 计数器显示等待批准的订单数。

在单击采购订单的&#x200B;**[!UICONTROL View]**&#x200B;并查看详细信息后，审批者可以单击&#x200B;**[!UICONTROL Approve]**&#x200B;或&#x200B;**[!UICONTROL Reject]**。

### 批量批准/拒绝

从Adobe Commerce 2.4.1开始，审批者可以同时批准或拒绝多个采购订单。

1. 在&#x200B;_[!UICONTROL My Purchase Order]_页面上，单击&#x200B;**[!UICONTROL Requires My Approval]**选项卡。

1. 选中要批准或拒绝的每个采购订单的复选框。

1. 单击&#x200B;**[!UICONTROL Approve Selected]**&#x200B;或&#x200B;**[!UICONTROL Reject Selected]**。

客户只能选择状态允许某项活动的采购订单。 公司管理员可以对公司中的任何有效采购订单进行批量批准或拒绝。

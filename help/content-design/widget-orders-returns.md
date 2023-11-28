---
title: 订单和退货小组件
description: 了解如何使用订单和退货小组件，使客户能够检查其订单的状态、打印发票以及跟踪发运。
exl-id: 1c3948e6-a0de-4ee4-8abf-10ab845a94a7
feature: Page Content, Orders, Returns
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '354'
ht-degree: 0%

---

# 订单和退货小组件

此 _订单和退货_ 通过小组件，来宾能够检查其订单的状态、打印发票并跟踪发货情况。 将小组件添加到店面后，它仅对来宾和未登录其帐户的客户可见。 客人可以通过提供订单ID、账单姓氏以及电子邮件地址或邮政编码来查找订单。

![店面侧栏中的订单和退货小组件](./assets/storefront-widget-orders-returns-sidebar.png){width="600" zoomable="yes"}

## 店面上的订单和退货小组件

1. 客户可以使用 **[!UICONTROL Find Order By]** 选项以选择以下参数之一来查找订单：

   - 电子邮件地址
   - 邮政编码

1. 客户输入 **[!UICONTROL Order ID]** 和 **[!UICONTROL Billing Last Name]**.

1. 输入任一帐单 **[!UICONTROL Email Address]** 或 **[!UICONTROL ZIP Code]** 与订单关联的属性。

1. 点击次数 **[!UICONTROL Search]** 以检索订单。

   ![店面中显示的订单信息](./assets/storefront-widget-orders-returns-view.png){width="700" zoomable="yes"}

## 设置订单和退货小组件

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. 在右上角，单击 **[!UICONTROL Add Widget]**.

1. 在 _[!UICONTROL Settings]_部分，执行以下操作：

   - 设置 **[!UICONTROL Type]** 到 `Orders and Returns`.

   - 选择 **[!UICONTROL Design Theme]** 店里用的那个。

1. 单击 **[!UICONTROL Continue]**.

1. 在 _[!UICONTROL Storefront Properties]_部分，执行以下操作：

   - 对象 **[!UICONTROL Widget Title]**，为构件输入描述性标题。

     此标题仅从管理员中可见。

   - 对象 **[!UICONTROL Assign to Store Views]**，选择显示小部件的商店视图。

     您可以选择特定的商店视图，或者 `All Store Views`. 要选择多个视图，请按住Ctrl键(PC)或Command键(Mac)并单击每个选项。

   - （可选）对于 **[!UICONTROL Sort Order]**，请输入一个数字以确定此项目在页面同一部分中与其他项目一起显示的顺序。 (`0` =第一个， `1` =秒， `3` =第三，依此类推。)

1. 在 _[!UICONTROL Layout Updates]_部分，单击&#x200B;**[!UICONTROL Add Layout Update]**并执行以下操作：

   - 设置 **[!UICONTROL Display On]** 到您希望小组件显示的页面类型。

   - 要确定小组件在页面上显示的位置，请完成其余布局更新信息。

1. 完成后，单击 **[!UICONTROL Save]**.

1. 提示刷新缓存时，单击页面顶部消息中的链接，然后按照说明操作。

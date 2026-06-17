---
title: 订单和退货小组件
description: 了解如何使用订单和退货小组件，使客户能够检查其订单的状态、打印发票以及跟踪发运。
exl-id: 1c3948e6-a0de-4ee4-8abf-10ab845a94a7
feature: Page Content, Orders, Returns
badgePaas: label="仅限PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="仅适用于云项目（Adobe管理的PaaS基础架构）和内部部署项目上的Adobe Commerce 。"
TQID: https://experienceleague.adobe.com/jWpFWPBwvKr5EnMXdV5-3zAqagGuzPrvOL6-gMiEw-M
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: bd989d82-1e15-4534-88db-f1f51dd77ffaid: c1256247-af4b-46d8-9dca-0c654ecfa157id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 382
ht-degree: 0%

---

# 订单和退货小组件

_订单和退货_&#x200B;构件使来宾能够检查其订单的状态、打印发票以及跟踪发货。 将小组件添加到店面后，它仅对来宾和未登录其帐户的客户可见。 客人可以通过提供订单ID、账单姓氏以及电子邮件地址或邮政编码来查找订单。

店面侧栏中的![订单和退货小组件](./assets/storefront-widget-orders-returns-sidebar.png){width="600" zoomable="yes"}

## 店面上的订单和退货小组件

1. 客户可以使用&#x200B;**[!UICONTROL Find Order By]**&#x200B;选项选择以下参数之一来查找订单：

   - 电子邮件地址
   - 邮政编码

1. 客户输入了&#x200B;**[!UICONTROL Order ID]**&#x200B;和&#x200B;**[!UICONTROL Billing Last Name]**。

1. 输入与订单关联的帐单&#x200B;**[!UICONTROL Email Address]**&#x200B;或&#x200B;**[!UICONTROL ZIP Code]**。

1. 单击&#x200B;**[!UICONTROL Search]**&#x200B;以检索订单。

   ![店面中显示的订单信息](./assets/storefront-widget-orders-returns-view.png){width="700" zoomable="yes"}

## 设置订单和退货小组件

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**。

1. 单击右上角的&#x200B;**[!UICONTROL Add Widget]**。

1. 在&#x200B;_[!UICONTROL Settings]_部分中，执行以下操作：

   - 将&#x200B;**[!UICONTROL Type]**&#x200B;设置为`Orders and Returns`。

   - 选择商店使用的&#x200B;**[!UICONTROL Design Theme]**。

1. 单击&#x200B;**[!UICONTROL Continue]**。

1. 在&#x200B;_[!UICONTROL Storefront Properties]_部分中，执行以下操作：

   - 对于&#x200B;**[!UICONTROL Widget Title]**，输入小部件的描述性标题。

     此标题仅从管理员中可见。

   - 对于&#x200B;**[!UICONTROL Assign to Store Views]**，选择显示小组件的存储视图。

     您可以选择特定的商店视图，或`All Store Views`。 要选择多个视图，请按住Ctrl键(PC)或Command键(Mac)并单击每个选项。

   - （可选）为&#x200B;**[!UICONTROL Sort Order]**&#x200B;输入一个数字，以确定该项在页面的同一部分中与其他项一起出现的顺序。 （`0` =第一，`1` =第二，`3` =第三，依此类推。）

1. 在&#x200B;_[!UICONTROL Layout Updates]_部分中，单击&#x200B;**[!UICONTROL Add Layout Update]**并执行以下操作：

   - 将&#x200B;**[!UICONTROL Display On]**&#x200B;设置为您希望小组件显示的页面类型。

   - 要确定小组件在页面上显示的位置，请完成其余布局更新信息。

1. 完成后，单击&#x200B;**[!UICONTROL Save]**。

1. 提示刷新缓存时，单击页面顶部消息中的链接，然后按照说明操作。

---
title: 客户现已上线
description: '[!UICONTROL Customers &#x200B;]菜单上的_Now Online_选项列出了您商店中当前在线的所有客户和访客。'
exl-id: 69af669d-f9aa-471b-9d62-5657f3fb2103
source-git-commit: c855a691ed33e1e6e74865ebdfb30ddad21ad83e
workflow-type: tm+mt
source-wordcount: '340'
ht-degree: 0%

---

# 客户现已上线

[!DNL Customers]菜单上的&#x200B;**[!UICONTROL Now Online]**&#x200B;选项列出了您商店中当前在线的所有客户和访客。 在配置中设置客户显示为当前在线的时间间隔，并确定[!DNL Customer's]活动从管理员那里可见的时长。 默认情况下，间隔为15分钟。 如果在此期间未使用键盘，则会话结束，客户必须再次登录其帐户才能继续购物。 需要注意的是，购物车的内容会被保存以供以后访问。

![在线客户](assets/customers-now-online.png){width="700" zoomable="yes"}

客户的在线状态仅在客户登录、注册或任何其他状态更改事件时更新。 它包括与购物车相关的事件，如添加、删除和修改产品。

>[!NOTE]
>
>仅页面访问不会更新客户的在线状态。 若要收集此类信息，建议[设置Google Analytics](../merchandising-promotions/google-analytics.md)(单独或与[Google Tag Manager](../merchandising-promotions/google-tag-manager.md)一起使用)，或将其他Analytics软件与Adobe Commerce一起使用。

## 查看当前在线的所有客户

在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Customers]** > **[!UICONTROL Online Now]**。

>[!TIP]
>
>有关帮助在线客户完成购买的信息，请参阅[购物帮助](../stores-purchase/introduction.md#shopping-assistance)。

## 配置时间间隔

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧面板中，展开&#x200B;**[!UICONTROL Customers]**&#x200B;并选择&#x200B;**[!UICONTROL Customer Configuration]**。

1. 展开&#x200B;**[!UICONTROL Online Customers Options]**&#x200B;部分并执行以下操作：

   ![在线客户选项](../configuration-reference/customers/assets/customer-configuration-online-customers-options.png){width="600" zoomable="yes"}

   - 对于&#x200B;**[!UICONTROL Online Minutes Interval]**，输入管理员看到的客户会话的分钟数。 将该字段留空以接受默认间隔15分钟。

   - 对于&#x200B;**[!UICONTROL Customer Data Lifetime]**，请输入客户输入的任何未保存数据过期前的分钟数。

1. 完成后，单击&#x200B;**[!UICONTROL Save Config]**。

## 列描述

| 列 | 描述 |
| --- | --- |
| **[!UICONTROL ID]** | 已注册客户的客户ID。 |
| **[!UICONTROL First Name]** | 已注册客户的名字。 |
| **[!UICONTROL Last Name]** | 已注册客户的姓氏。 |
| **[!UICONTROL Email]** | 注册客户的电子邮件地址。 |
| **[!UICONTROL Last Activity]** | 客户上次在商店中活动的日期和时间。 |
| **[!UICONTROL Type]** | 选项： `Customer` / `Visitor` |
| **[!UICONTROL Last URL]** | 客户访问的最后一个URL。 |
| **[!UICONTROL Company]** | 用户所属公司的名称。 |

{style="table-layout:auto"}

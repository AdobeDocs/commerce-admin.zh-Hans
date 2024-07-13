---
title: '[!UICONTROL Customers] &amp；gt； [!UICONTROL Persistent Shopping Cart]'
description: 查看Commerce管理员的[!UICONTROL Customers] &amp；gt； [!UICONTROL Persistent Shopping Cart]页面上的配置设置。
exl-id: d6c5ae46-32ed-4fcd-bcd6-ee3a07d7db5f
feature: Configuration, Shopping Cart
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '493'
ht-degree: 0%

---

# [!UICONTROL Customers] > [!UICONTROL Persistent Shopping Cart]

{{config}}

>[!NOTE]
>
>[永久购物车](../../stores-purchase/cart-persistent.md)允许保留购物车中剩余的未购买的项目，并将其保存在&#x200B;_持久生命周期_&#x200B;中配置的期间。 客户浏览器中应允许Cookie使用永久购物车。

## [!UICONTROL General Options]

![常规选项](./assets/persistent-shopping-cart-general.png)<!-- zoom -->

<!-- [General Options](https://docs.magento.com/user-guide/sales/cart-persistent-configuration.html) -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Enable Persistence] | 网站 | 确定是否启用持久性。 |
| [!UICONTROL Persistence Lifetime (seconds)] | 网站 | 定义永久性Cookie的生命周期（以秒为单位）。 允许的最大值为3153600000秒（100年）。 |
| [!UICONTROL Enable "Remember Me"] | 网站 | 定义&#x200B;_记住我_&#x200B;复选框是否显示在应用商店的登录和注册页面上。 选项： <br/>**`Yes`**— 显示&#x200B;_记住我_复选框。<br/>**`No`** — 不显示&#x200B;_记住我_&#x200B;复选框，永久性Cookie仅用于已拥有该永久性Cookie的客户。 |
| [!UICONTROL "Remember Me" Default Value] | 网站 | 定义&#x200B;_记住我_&#x200B;复选框的默认状态。 |
| [!UICONTROL Clear Persistence on Log Out] | 网站 | 定义在商店客户注销时是否删除永久性Cookie。 无论如何配置，如果客户未注销，但会话Cookie过期，则仍会使用永久性Cookie。 |
| [!UICONTROL Persist Shopping Cart] | 网站 | 定义使用永久性Cookie是否授予对往来行帐户的购物车数据的访问权限。 选项： <br/>**`Yes`**— 在会话结束后保存购物车内容。<br/>**`No`** — 会话结束后未保存购物车内容。 |
| [!UICONTROL Persist Wish List] | 网站 | ![Adobe Commerce](../../assets/adobe-logo.svg)(仅限Adobe Commerce)确定会话结束时是否保留客户愿望清单的状态。 选项： <br/>**`Yes`**— 会话结束时保存了希望列表内容。<br/>**`No`** — 会话结束时未保存希望列表。 |
| [!UICONTROL Persist Recently Ordered Items] | 网站 | ![Adobe Commerce](../../assets/adobe-logo.svg)(仅限Adobe Commerce)确定会话结束时是否保留最近排序项目的状态。 选项： <br/>**`Yes`**— 会话结束时保存最近排序项目的状态。<br/>**`No`** — 会话结束时未保存最近订购项目的状态。 |
| [!UICONTROL Persist Currently Compared Products] | 网站 | ![Adobe Commerce](../../assets/adobe-logo.svg)(仅限Adobe Commerce)确定会话结束时当前比较的产品的状态是否保留。 选项： <br/>**`Yes`**— 会话结束时保存当前比较产品的状态。<br/>**`No`** — 会话结束时未保存当前比较的产品的状态。 |
| [!UICONTROL Persist Comparison History] | 网站 | ![Adobe Commerce](../../assets/adobe-logo.svg)(仅限Adobe Commerce)确定会话结束时是否保留比较历史记录的状态。 选项： <br/>**`Yes`**— 会话结束时保存比较历史记录的状态。<br/>**`No`** — 会话结束时未保存比较历史记录的状态。 |
| [!UICONTROL Persist Recently Viewed Products] | 网站 | ![Adobe Commerce](../../assets/adobe-logo.svg)(仅限Adobe Commerce)确定会话结束时是否保留最近查看产品的状态。 选项： <br/>**`Yes`**— 会话结束时，将保存最近查看的产品的状态。<br/>**`No`** — 会话结束时未保存最近查看的产品的状态。 |
| [!UICONTROL Persist Customer Group Membership and Segmentation] | 网站 | ![Adobe Commerce](../../assets/adobe-logo.svg)(仅限Adobe Commerce)确定会话结束时是否保留客户群组成员资格的状态和分段条件。 选项： <br/>**`Yes`**— 会话结束时保存客户的组成员资格和分段数据的状态。<br/>**`No`** — 会话结束时未保存客户的组成员资格状态和分段数据。 |

{style="table-layout:auto"}

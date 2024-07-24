---
title: 永久购物车的配置参考
description: 永久购物车的配置参考的可重用内容。
source-git-commit: d23cb0d63409e533cf950d8d14514d9f9157fd05
workflow-type: tm+mt
source-wordcount: '358'
ht-degree: 0%

---


# [!UICONTROL General Options]

![常规选项](/help/configuration-reference/customers/assets/persistent-shopping-cart-general.png)<!-- zoom -->

<!-- [General Options](https://docs.magento.com/user-guide/sales/cart-persistent-configuration.html) -->

| 字段 | [作用域](/help/getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |------------------------------------------------------------------------|--- |
| [!UICONTROL Enable Persistence] | 网站 | 确定是否启用持久性功能。 |
| [!UICONTROL Persistence Lifetime (seconds)] | 网站 | 定义永久性Cookie的生命周期（以秒为单位）。 允许的最大值为34560000秒（400天）。 这是建议的最长Cookie使用期的限制。 |
| [!UICONTROL Enable "Remember Me"] | 网站 | 定义&#x200B;_记住我_&#x200B;复选框是否显示在应用商店的登录和注册页面上。 选项： <br/>**`Yes`**— 显示&#x200B;_记住我_复选框。<br/>**`No`** — 不显示&#x200B;_记住我_&#x200B;复选框，永久性Cookie仅用于已拥有该永久性Cookie的客户。 |
| [!UICONTROL "Remember Me" Default Value] | 网站 | 定义&#x200B;_记住我_&#x200B;复选框的默认状态。 |
| [!UICONTROL Clear Persistence on Log Out] | 网站 | 定义在商店客户注销时是否删除永久性Cookie。 无论如何配置此选项，如果客户未注销，但会话Cookie过期，则仍会使用永久性Cookie。 |
| [!UICONTROL Persist Shopping Cart] | 网站 | 定义使用永久性Cookie是否授予对相应帐户的购物车数据的访问权限。 选项： <br/>**`Yes`**或&#x200B;**`No`**。 |
| [!UICONTROL Persist Wish List] | 网站 | ![Adobe Commerce](/help/assets/adobe-logo.svg)(仅限Adobe Commerce)确定会话结束时是否保留客户愿望清单的状态。 选项： <br/>**`Yes`**— 会话结束时保存了希望列表内容。<br/>**`No`** — 会话结束时未保存希望列表。 |
| [!UICONTROL Persist Recently Ordered Items] | 网站 | ![Adobe Commerce](/help/assets/adobe-logo.svg)(仅限Adobe Commerce)确定会话结束时是否保存最近排序的项目的状态。 选项： <br/>**`Yes`**或&#x200B;**`No`**。 |
| [!UICONTROL Persist Currently Compared Products] | 网站 | ![Adobe Commerce](/help/assets/adobe-logo.svg)(仅限Adobe Commerce)确定会话结束时当前比较的产品的状态是否保留。 选项： <br/>**`Yes`**或&#x200B;**`No`**。 |
| [!UICONTROL Persist Comparison History] | 网站 | ![Adobe Commerce](/help/assets/adobe-logo.svg)(仅限Adobe Commerce)确定会话结束时是否保留比较历史记录的状态。 选项： <br/>**`Yes`**或&#x200B;**`No`**。 |
| [!UICONTROL Persist Recently Viewed Products] | 网站 | ![Adobe Commerce](/help/assets/adobe-logo.svg)(仅限Adobe Commerce)确定会话结束时是否保留最近查看的产品的状态。 选项： <br/>**`Yes`**或&#x200B;**`No`**。 |
| [!UICONTROL Persist Customer Group Membership and Segmentation] | 网站 | ![Adobe Commerce](/help/assets/adobe-logo.svg)(仅限Adobe Commerce)确定会话结束时是否保留客户群组成员资格的状态和分段条件。 选项： <br/>**`Yes`**— 会话结束时保存客户的组成员资格和分段数据的状态。<br/>**`No`** — 会话结束时未保存客户的组成员资格状态和分段数据。 |

{style="table-layout:auto"}

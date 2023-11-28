---
title: 客户会话生命周期
description: 客户会话生命周期决定了客户购物会话的生命周期。
exl-id: 7180631a-3233-40f3-92bf-b329fc260cf9
feature: Customers, Configuration, Security
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '401'
ht-degree: 0%

---

# 客户会话生命周期

客户购物会话的生命周期由几个因素决定，包括服务器会话的长度，使用 [永久购物车](../stores-purchase/cart-persistent.md)以及存储在浏览器中的信息的生命周期。 尽管这些请求与相同的客户体验相关，但它们是具有不同过期事件和生命周期的单独流程。

| 进程 | 描述 |
| --- | --- |
| 会话 | 存储在服务器上的信息，如购物车的内容。 如果服务器会话在Cookie过期之前过期，则客户可能会丢失购物车内容并降低安全风险。 |
| 会话Cookie | 以字符数或字符串形式存储在浏览器中的信息。 如果会话Cookie在服务器会话之前过期，则客户会注销。 当客户关闭浏览器窗口时，会话Cookie将被删除。 默认情况下，Cookie生命周期设置为3600秒，即一小时。 如果在此期间没有键盘活动，则当前会话结束，客户必须登录回其帐户才能继续购物。 |

{style="table-layout:auto"}

如果 [永久购物车](../stores-purchase/cart-persistent.md) 启用后，购物车内容将在客户下次登录其帐户时保存。 使用持久性购物车时，建议将服务器会话和会话Cookie的生命周期设置为较长时间。

在服务器上，会话的长度由 `php.ini` 文件和多个变量。 目前，Adobe Commerce没有可控制服务器会话长度的管理员配置设置。

## 配置Cookie生命周期

1. 在 _管理员_ 侧栏，转到 [!UICONTROL **商店**] > _[!UICONTROL Settings]_>[!UICONTROL **配置**].

1. 如果您有多个商店，请设置 **[!UICONTROL Store View]** 选择器位于应用配置的商店右上角。

1. 在左侧面板中的 **[!UICONTROL General]**，选择 **[!UICONTROL Web]**.

1. 展开 **[!UICONTROL Default Cookie Settings]** 部分。

   ![默认Cookie设置](../configuration-reference/general/assets/web-default-cookie-settings.png){width="600" zoomable="yes"}

1. 要更改默认值，请清除 **[!UICONTROL Use system value]** 复选框，并以秒为单位输入新值。

1. 完成后，单击 **[!UICONTROL Save Config]**.

## 配置 _记住我_ 功能

为简化登录过程， **[!UICONTROL Remember Me]** 函数允许用户帐户持有人避免在每次进入店面时输入其凭据。 出于安全原因，默认情况下将禁用持久性功能。

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中，展开 **[!UICONTROL Customers]** 并选择 **[!UICONTROL Persistent Shopping Cart]**.

1. 展开 **[!UICONTROL General Options]** 部分。

1. 对象 **[!UICONTROL Enable Persistence]**，设置为 `Yes`. (清除 **[!UICONTROL Use system value]** 复选框，允许更改默认设置。)

1. 对象 **[!UICONTROL Enable "Remember Me"]**，设置为 `Yes` 或 `No` 根据您的要求。

1. 完成后，单击 **[!UICONTROL Save Config]**.

---
title: 购物车持久性
description: 了解永久性购物车如何跟踪未购买的购物车项目并保存信息以供客户下次访问。
exl-id: 95c336b3-77ac-4cf6-8fb5-23f4ac4b67d6
feature: Shopping Cart, Configuration
source-git-commit: 26d4bb35c6e1878a8ea8c5f05a982559e5d6dc35
workflow-type: tm+mt
source-wordcount: '1473'
ht-degree: 0%

---

# 购物车持久性

永久购物车将跟踪购物车中留下的未购买项目，并保存信息以供客户下次访问。 以下客户： _纪念_ 可以在下次访问您的商店时恢复其购物车的内容。

使用永久性购物车可以帮助减少放弃的购物车的数量并提高销售量。 请务必了解一点，永久性购物车不会在任何时间泄露敏感帐户信息。 永久购物车在使用中，注册客户和访客购物者都需要登录现有帐户，或在结账前创建帐户。 对于访客购物者而言，持久购物车是从上一个会话检索信息的唯一方法。

要管理您的站点或特定商店视图中的购物车持久性的使用，您可以 [配置永久购物车](#configure-a-persistent-cart) 设置。 有关这些设置如何影响店面购物者体验的更多信息，请参阅 [持久性购物车工作流](#persistent-cart-workflow).

>[!NOTE]
>
>使用持久性购物车时，建议将服务器会话和会话Cookie的生命周期设置为较长时间。 请参阅 [会话生命周期](../customers/customer-online-options.md) 以了解更多信息。

要使用持久性购物车，必须将客户的浏览器设置为允许Cookie。 有两种类型的Cookie用于购物车操作：

- **会话Cookie**  — 短期会话Cookie在客户单次访问您的网站时存在，并在客户离开时或设定的时间段后过期。

- **永久性Cookie**  — 会话结束后，长期、永久性Cookie继续存在，并保存客户的购物车内容记录以供将来参考。

## 持久性购物车工作流

当永久购物车为 [已启用](#configure-a-persistent-cart)，工作流依赖于：

- 的值 _启用记住我_ 和 _注销时清除持久性_ 设置
- 客户选择或清除 _记住我_ 复选框
- 清除永久性Cookie时

应用永久性Cookie时， `Not Jane Smith?` 链接显示在页眉中。 此提示使客户能够终止永久会话并以来宾身份开始工作，或以其他客户身份登录。 系统保留购物车内容的记录，即使客户以后使用不同的设备在您的商店中购物也是如此。 例如，客户可以从便携式计算机向购物车中添加一件商品，从移动设备添加更多商品，以及从平板电脑完成结账过程。

每个浏览器都有一个独立的永久性Cookie。 如果客户在单个永久性会话期间访问您的商店时使用了多个浏览器，则页面刷新时，在一个浏览器中所做的更改会反映在任何其他浏览器中。 启用永久购物车后，您的商店将为客户用于登录或创建帐户的每个浏览器创建和维护一个单独的永久性Cookie。

### 示例：共享计算机上的打开会话

Jane即将结束她的节日购物，她将持续进行节日购物。 她往购物车里加了件给约翰的礼物，还有一件给母亲的礼物。 然后她去厨房吃点心。

简在厨房里，约翰坐在电脑前快速购物。 而不注意 `Not Jane Smith?` 链接到页面顶部，他找到一份送给Jane的漂亮礼物，并将其添加到购物车中。 当他结帐并以自己的身份登录时，Jane购物车中的两个商品都会添加到他的购物车中。 John赶时间，在此期间他没注意到其他物品。 _订单查看_，并提交订单。 珍的购物车现在空了，约翰买了所有的礼物。

### 记住我

客户可以选择 _记住我_ 复选框，用于保存购物车的内容。

| 还记得我吗？ | 结果 |
| ------------ |  ------ |
| 已选择 | 创建永久性Cookie并保存购物车的内容，以供客户下次登录会话时使用。 |
| 未选择 | 不创建永久性Cookie，也不保存客户下次登录会话的购物车信息。 |

{style="table-layout:auto"}

### 在注销时继续保留 — 否

| 操作 | 结果 |
| ------ | ------ |
| 客户登录 | 除了会调用已使用的会话Cookie之外，还会调用永久性Cookie。 |
| 客户注销 | 删除会话Cookie，但永久性Cookie仍然有效。 客户下次登录时，将恢复购物车项目或将其添加到购物车中的任何新项目。 |
| 客户未注销，且会话Cookie过期 | 永久性Cookie将保持有效。 |

{style="table-layout:auto"}

### 注销时清除持久性

| 操作 | 结果 |
| ------ | ------ |
| 客户登录 | 除了会调用已使用的会话Cookie之外，还会调用永久性Cookie。 |
| 客户注销 | 删除两个Cookie。 |
| 客户未注销，但会话Cookie过期 | 永久性Cookie将保持有效。 |

{style="table-layout:auto"}

## 持久购物车设置和效果

| 设置 | 效果 |
|----------|--------|
| **[!UICONTROL Enable Remember Me]** 设置为 `No`.<br/><br/>**[!UICONTROL Clear Persistence on Log Out]**具有任何值。<br/><br/>此**&#x200B;记住我&#x200B;**此复选框在登录和注册页面上不可用。 | 未使用永久性Cookie。 |
| **[!UICONTROL Enable Remember Me]** 设置为 `Yes`.<br/><br/>**[!UICONTROL Clear Persistence on Log Out]**具有任何值。<br/><br/>**&#x200B;记住我&#x200B;**未选中。 | 会话Cookie按常规方式应用；不使用永久性Cookie。 |
| **[!UICONTROL Enable Remember Me]** 设置为 `Yes`.<br/><br/>**[!UICONTROL Clear Persistence on Log Out]**设置为 `Yes`.<br/><br/>**&#x200B;记住我&#x200B;**设置为 `Yes`. | 当客户登录时，两个Cookie都将被应用。 当客户注销时，两个Cookie都会被删除。 如果客户未登录，但会话Cookie过期，则仍会使用永久性Cookie。 除了注销，永久性Cookie在其生命周期耗尽或客户单击 `Not Jane Smith` 链接。 |
| **[!UICONTROL Enable Remember Me]** 设置为 `Yes`.<br/><br/>**[!UICONTROL Clear Persistence on Log Out]**设置为 `No`.<br/><br/>**&#x200B;记住我&#x200B;**设置为 `Yes` | 当客户登录时，两个Cookie都将被应用。 当客户注销时，会话Cookie被删除，永久会话继续。 永久性Cookie在其生命周期耗尽或客户单击 `Not Jane Smith` 链接。 |

{style="table-layout:auto"}

## 配置持久购物车

在设置永久性购物车期间，您可以指定Cookie的生命周期，以及要为各种客户活动提供的选项。

有关如何根据这些设置确定客户工作流的更多信息，请参阅 [持久性购物车工作流](#persistent-cart-workflow).

>[!NOTE]
>
>如果会话Cookie在客户登录时过期，则永久性Cookie将保持活动状态。

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中，展开 **[!UICONTROL Customers]** 并选择 **[!UICONTROL Persistent Shopping Cart]**.

1. 要启用持久性购物车并显示其他选项，请设置 **[!UICONTROL Enable Persistence]** 到 `Yes`.

   ![启用和配置购物车持久性](../configuration-reference/customers/assets/persistent-shopping-cart-general.png){width="600" zoomable="yes"}

   有关每个配置设置的详细信息，请参见 [_配置引用_](../configuration-reference/customers/persistent-shopping-cart.md)

   >[!NOTE]
   >
   >如有需要，清除 **[!UICONTROL Use system value]** 复选框，以修改这些设置。

1. 对象 **[!UICONTROL Persistence Lifetime (seconds)]**，输入永久性Cookie持续存在的时间（以秒为单位）。

   默认值31,536,000秒等于一年。 允许的最长时间为100年。

1. 设置 **[!UICONTROL Enable "Remember Me"]** 更改为以下任一项：

   - `Yes`  — 显示 _记住我_ 复选框，以便客户可以选择保存其购物车信息。

   - `No`  — 仍可以启用持久性，但客户无权选择是否要保存其信息。

1. 要预选 _记住我_ 客户复选框，设置 **[!UICONTROL Remember Me Default Value]** 到 `Yes`.

   客户可以选择清除此选项。

1. 设置 **[!UICONTROL Clear Persistence on Log Out]** 更改为以下任一项：

   - `Yes`  — 当注册客户注销时，将清除购物车。

   - `No`  — 当注册客户注销时，将保存购物车。

   >[!NOTE]
   >
   >如果会话Cookie在客户仍然登录时过期，则永久性Cookie仍会保持使用状态。

1. 设置 **[!UICONTROL Persist Shopping Cart]** 更改为以下任一项：

   - `Yes`  — 如果会话Cookie过期，则会保留永久性Cookie。 如果访客购物者稍后登录或创建帐户，则购物车将恢复。

   - `No`  — 会话Cookie过期后，不会为访客保留购物车。

1. ![Adobe Commerce](../assets/adobe-logo.svg) (仅限Adobe Commerce)设置 **[!UICONTROL Persist Wish List]** 要确定会话结束时是否保留客户愿望清单的状态，请执行以下操作：

   - `Yes`  — 会话结束时保存希望列表内容。

   - `No`  — 会话结束时未保存希望列表。

1. ![Adobe Commerce](../assets/adobe-logo.svg) (仅限Adobe Commerce)设置 **[!UICONTROL Persist Recently Ordered Items]** 要确定在会话结束时是否保留最近排序项目的状态，请执行以下操作：

   - `Yes`  — 会话结束时保存最近订购项目的状态。

   - `No`  — 会话结束时不会保存最近订购项目的状态。

1. 设置 **[!UICONTROL Persist Currently Compared Products]** 到 `Yes` 或 `No`.

1. 设置 **[!UICONTROL Persist Comparison History]** 到 `Yes` 或 `No`.

1. 设置 **[!UICONTROL Persist Recently Viewed Products]** 到 `Yes` 或 `No`.

1. ![Adobe Commerce](../assets/adobe-logo.svg) (仅限Adobe Commerce)设置 **[!UICONTROL Persist Customer Group Membership and Segmentation]** 要确定会话结束时是否保留客户的组成员资格状态和分段标准，请执行以下操作：

   - `Yes`  — 会话结束时保存客户的组成员资格状态和分段数据。

   - `No`  — 会话结束时，不会保存客户的组成员资格状态和分段数据。

1. 单击 **[!UICONTROL Save Config]**.

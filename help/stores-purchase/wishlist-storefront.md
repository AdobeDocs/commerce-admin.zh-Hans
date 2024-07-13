---
title: 希望列表店面体验
description: 了解您的客户在店面中可用的愿望清单管理工具。
exl-id: df8cf89a-c897-4a9a-9e84-3bae946683a4
feature: Customers, Storefront
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '860'
ht-degree: 0%

---

# 希望列表店面体验

愿望清单是客户回忆自己喜欢但还没准备好购买的产品的一种便捷方式。 可以将愿望清单中的商品与他人共享或添加到购物车。 如果客户有多个愿望清单，则当前愿望清单的名称将显示在页面顶部。 客户可以从其帐户信息板管理其愿望清单。 商店管理员还可以帮助客户从管理员那里管理他们的愿望清单。

![店面示例 — 我的愿望清单](./assets/storefront-my-wishlist.png){width="700" zoomable="yes"}

![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce支持每个客户帐户使用多个愿望清单。

![Magento Open Source](../assets/open-source.svg)Magento Open Source代码库支持每个客户帐户使用单一愿望清单。

## 创建愿望清单

![Adobe Commerce](../assets/adobe-logo.svg)(仅限Adobe Commerce)

在店面，客户可以从其帐户仪表板、产品页面、目录页面和购物车创建愿望清单。

### 方法1：来自客户帐户

1. 在其帐户仪表板的侧边栏中，客户选择&#x200B;**[!UICONTROL My Wish List]**。

1. 在右上角，单击&#x200B;**[!UICONTROL Create New Wish List]**。

1. 输入愿望清单名称。

1. 若要允许其他人查看其愿望清单，请选中&#x200B;**[!UICONTROL Public Wish List]**&#x200B;复选框。

   >[!NOTE]
   >
   >`Public`和`Private`愿望清单的主要区别在于，个人愿望清单不是通过愿望清单[可搜索的](wishlist-configuration.md#add-wish-list-search)。

1. 完成后，单击&#x200B;**[!UICONTROL Save]**。

   ![新建愿望清单](./assets/account-dashboard-wishlist-create-new.png){width="700" zoomable="yes"}

### 方法2：从目录页面

1. 从店面，客户转到目录页面，其中包含要添加到愿望清单中的产品。

1. 将鼠标悬停在产品上。

1. 客户单击&#x200B;_添加到愿望清单_&#x200B;图标旁边的箭头并选择&#x200B;**[!UICONTROL Create New Wish List]**。

1. 输入愿望清单名称。

1. 若要允许其他人查看其愿望清单，请选中&#x200B;**[!UICONTROL Public Wish List]**&#x200B;复选框。

1. 完成后，单击&#x200B;**[!UICONTROL Save]**。

### 方法3：从产品详细信息页面

1. 从店面，客户进入要添加到愿望清单中的产品的详细页面。

1. 单击&#x200B;**[!UICONTROL Add to Wish List]**&#x200B;旁边的箭头并选择&#x200B;**[!UICONTROL Create New Wish List]**。

1. 进入&#x200B;**[!UICONTROL Wish List Name]**。

1. 若要允许其他人查看其愿望清单，请选中&#x200B;**[!UICONTROL Public Wish List]**&#x200B;复选框。

1. 完成后，单击&#x200B;**[!UICONTROL Save]**。

   ![从产品详细信息页面创建新的愿望清单](./assets/account-dashboard-wishlist-create-from-pdp.png){width="700" zoomable="yes"}

### 方法4：从购物车

1. 客户打开&#x200B;**[!UICONTROL Shopping Cart]**&#x200B;页面。

1. 在该项下，单击&#x200B;**[!UICONTROL Move to Wishlist]**&#x200B;旁边的箭头并选择&#x200B;**[!UICONTROL Create New Wish List]**。

1. 进入&#x200B;**[!UICONTROL Wish List Name]**。

1. 若要允许其他人查看其愿望清单，请选中&#x200B;**[!UICONTROL Public Wish List]**&#x200B;复选框。

1. 完成后，单击&#x200B;**[!UICONTROL Save]**。

![从购物车页面创建新的愿望清单](./assets/account-dashboard-wishlist-create-from-cart.png){width="700" zoomable="yes"}

## 更新产品清单

1. 在愿望清单中，客户指向产品以显示选项。

1. 要添加有关产品的&#x200B;**[!UICONTROL Comment]**，请在价格下方的框中输入文本。

   ![编辑选项](./assets/account-dashboard-wishlist-edit-options.png){width="700" zoomable="yes"}

1. 要更改产品选项的选择，请单击&#x200B;**[!UICONTROL Edit]**&#x200B;并执行以下操作：

   - 更新产品详细信息页面上的选项。
   - 单击&#x200B;**[!UICONTROL Update Wish List]**。

## 将愿望清单产品添加到购物车

1. 在愿望清单中，客户指向要添加的产品。

1. 更新&#x200B;**[!UICONTROL Qty]**&#x200B;并根据需要编辑其他选项。

1. 单击&#x200B;**[!UICONTROL Add to Cart]**。

## 共享愿望清单

1. 客户单击&#x200B;**[!UICONTROL Share Wishlist]**。

1. 输入每个要接收愿望清单的人员的电子邮件地址，用逗号分隔。

1. 添加要包含在电子邮件中的&#x200B;**[!UICONTROL Message]**。

1. 单击&#x200B;**[!UICONTROL Share Wish List]**。

   ![共享您的愿望清单](./assets/account-dashboard-wishlist-sharing.png){width="700" zoomable="yes"}

   该邮件由您的主要[商店联系人](../getting-started/store-details.md#store-email-addresses)发送，并包含每个产品的缩略图图像，以及指向您商店的链接。

   ![共享愿望清单电子邮件](./assets/account-dashboard-wishlist-sharing-email.png){width="500" zoomable="yes"}

## 编辑愿望清单

客户可以从其帐户仪表板以多种方式修改其愿望清单。

### 将项目移动到其他列表

![Adobe Commerce](../assets/adobe-logo.svg)(仅限Adobe Commerce)

1. 客户选中要移动的每个项目的复选框。

1. 单击&#x200B;**[!UICONTROL Move Selected to Wish List]**&#x200B;并执行下列操作之一：

   - 选择现有的愿望清单。
   - 单击&#x200B;**[!UICONTROL Create New Wish List]**。

### 将项目复制到其他列表

![Adobe Commerce](../assets/adobe-logo.svg)(仅限Adobe Commerce)

1. 选中要移动的每个项目的复选框。

1. 单击&#x200B;**[!UICONTROL Copy Selected to Wish List]**&#x200B;并执行下列操作之一：

   - 选择现有的愿望清单。
   - 单击&#x200B;**[!UICONTROL Create New Wish List]**。

## 删除愿望清单

![Adobe Commerce](../assets/adobe-logo.svg)(仅限Adobe Commerce)

1. 客户打开要删除的愿望清单。

1. 单击&#x200B;**[!UICONTROL Delete Wish List]**。

1. 提示确认时，单击&#x200B;**[!UICONTROL OK]**。

>[!IMPORTANT]
>
>此操作无法撤消。

## 将愿望清单项目转移到购物车

要将所有愿望清单项目转移到购物车，客户单击&#x200B;**[!UICONTROL Add All to Cart]**。

要添加单个物料，客户将执行以下操作：

1. 将鼠标悬停在该项目上并输入要添加到购物车的&#x200B;**[!UICONTROL Qty]**。

1. 单击&#x200B;**[!UICONTROL Add to Cart]**。

## 查找客户的愿望清单

如果您的商店页面中包含的[愿望清单搜索小组件](wishlist-configuration.md#add-wish-list-search)，则客户可以按愿望清单所有者的姓名或电子邮件地址进行搜索。

1. 客户从愿望清单搜索小部件中选择搜索选项。

1. 输入愿望清单所有者的姓名或电子邮件地址，然后单击&#x200B;**[!UICONTROL Search]**。

   将打开&#x200B;_愿望清单搜索_&#x200B;页，任何匹配的愿望清单都显示在搜索结果部分中。

   >[!NOTE]
   >
   >搜索结果中仅显示公开的愿望清单 — 客户的私人愿望清单不会公开显示。

1. 要查看希望列表项的列表，请单击&#x200B;**[!UICONTROL View]**。

   将显示每个愿望清单的所有者名称和上次更新日期。

1. 要将产品添加到购物车，客户将选中产品下方的复选框并单击&#x200B;**[!UICONTROL Add to Cart]**。

   您也可以将喜欢的其他客户的愿望清单中的商品添加到您自己的愿望清单中。

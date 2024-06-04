---
title: 客户帐户范围
description: 客户帐户的范围可以限制为创建帐户的网站，或与商店层次结构中的所有网站和商店共享。
exl-id: c401bee2-763e-4fad-88cd-5d5a43c46186
feature: Customers, Configuration
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '355'
ht-degree: 0%

---

# 客户帐户范围

您商店中每一页的页眉邀请购物者前往 _登录或注册_ 以取得你商店的帐户。 开户的客户可享受一系列好处，包括：

* **创建客户帐户**  — 访客可创建一个客户帐户，以便将该店面用作注册客户。
* **创建公司帐户** 根据配置，您商店的访客可以选择创建公司帐户。 有关更多信息，请参阅 [Adobe Commerce B2B](../b2b/introduction.md).
* **更快速的结账**  — 注册客户结账速度更快，因为他们的帐户中已有许多信息。
* **自助服务**  — 注册客户可以更新其信息，检查订单状态，甚至从其帐户重新订购。

客户可以通过单击 **[!UICONTROL My Account]** 商店标题中的链接。 客户可以通过其帐户查看和修改信息，包括过去和当前地址、帐单和送货偏好设置、新闻稿订阅、愿望清单等。

![我的帐户](assets/account-dashboard-my-account.png){width="600" zoomable="yes"}

## 设置客户帐户的范围

客户帐户的范围可以限制为创建帐户的网站，或与商店层次结构中的所有网站和商店共享。

>[!NOTE]
>
>如果网站从客户组中排除，则当客户帐户的范围仅限于该网站或与所有网站共享时，不允许该客户登录该网站。 请参阅 [创建客户组](customer-groups.md#create-a-customer-group) 有关将网站从组中排除的更多信息。

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > [!UICONTROL _[!UICONTROL Settings]_] > **[!UICONTROL Configuration]**.

1. 在左侧面板中，展开 **[!UICONTROL Customers]** 并选择 **[!UICONTROL Customer Configuration]**.

1. 展开 **[!UICONTROL Account Sharing Options]** 部分。

   ![帐户共享选项](assets/customer-configuration-account-sharing-options.png){width="600" zoomable="yes"}

1. 设置 **[!UICONTROL Share Customer Accounts]** 更改为以下任一项：

   | 选项 | 描述 |
   | --- | --- |
   | `Global` | 与安装中的每个网站和商店共享客户帐户信息。 |
   | `Per Website` | 将客户帐户信息限制在创建帐户的网站上。 |

   {style="table-layout:auto"}

   >[!INFO]
   >
   > 如有必要，请清除 **[!UICONTROL User system value]** 复选框以进行更改。

1. 完成后，单击 **[!UICONTROL Save Config]**.

   >[!NOTE]
   >
   >时间 `Global` 已选中中的客户信息 **我的帐户** （地址和帐户信息，如联系人详细信息）共享。

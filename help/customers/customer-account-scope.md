---
title: 客户帐户范围
description: 客户帐户的范围可以限制为创建帐户的网站，或与商店层次结构中的所有网站和商店共享。
exl-id: c401bee2-763e-4fad-88cd-5d5a43c46186
feature: Customers, Configuration
TQID: https://experienceleague.adobe.com/ah5XmCeeX4Kc9czcllRq9zZX4W3rkkqkzcoUXtJjo5I
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2:
  - id: b01a71b7-d17a-42b2-a9ac-af4b8d9d2ef5
  - id: f56d26ed-050b-4fb7-b29b-8e6e994e80a2
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 356
ht-degree: 0%

---

# 客户帐户范围

您商店中每个页面的页眉都会邀请购物者&#x200B;_登录或在您的商店中注册_&#x200B;帐户。 开户的客户可享受一系列好处，包括：

* **创建客户帐户** — 访客可以创建客户帐户，以便将该店面用作注册客户。
* **创建公司帐户**&#x200B;根据配置，您商店的访客可以选择创建公司帐户。 有关详细信息，请参阅[Adobe Commerce B2B](../b2b/introduction.md)。
* **更快结帐** — 注册客户在结帐过程中移动得更快，因为很多信息都已在他们的帐户中。
* **自助服务** — 注册客户可以更新其信息、检查订单状态，甚至从其帐户重新订购。

客户可以通过单击商店标题中的&#x200B;**[!UICONTROL My Account]**&#x200B;链接访问其帐户。 客户可以通过其帐户查看和修改信息，包括过去和当前地址、帐单和送货偏好设置、新闻稿订阅、愿望清单等。

![我的帐户](assets/account-dashboard-my-account.png){width="600" zoomable="yes"}

## 设置客户帐户的范围

客户帐户的范围可以限制为创建帐户的网站，或与商店层次结构中的所有网站和商店共享。

>[!NOTE]
>
>如果网站从客户组中排除，则当客户帐户的范围仅限于该网站或与所有网站共享时，不允许该客户登录该网站。 有关将网站从群组中排除的详细信息，请参阅[创建客户群](customer-groups.md#create-a-customer-group)。

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > [!UICONTROL _[!UICONTROL Settings]_] > **[!UICONTROL Configuration]**。

1. 在左侧面板中，展开&#x200B;**[!UICONTROL Customers]**&#x200B;并选择&#x200B;**[!UICONTROL Customer Configuration]**。

1. 展开&#x200B;**[!UICONTROL Account Sharing Options]**&#x200B;部分。

   ![帐户共享选项](assets/customer-configuration-account-sharing-options.png){width="600" zoomable="yes"}

1. 将&#x200B;**[!UICONTROL Share Customer Accounts]**&#x200B;设置为以下项之一：

   | 选项 | 描述 |
   | --- | --- |
   | `Global` | 与安装中的每个网站和商店共享客户帐户信息。 |
   | `Per Website` | 将客户帐户信息限制在创建帐户的网站上。 |

   {style="table-layout:auto"}

   >[!INFO]
   >
   > 如有必要，请清除&#x200B;**[!UICONTROL User system value]**&#x200B;复选框以进行更改。

1. 完成后，单击&#x200B;**[!UICONTROL Save Config]**。

   >[!NOTE]
   >
   >当选择`Global`时，将共享&#x200B;**我的帐户**&#x200B;中的客户信息（地址和帐户信息，如联系人详细信息）。

---
title: 共享 [!DNL Commerce] 帐户
description: 了解如何授予对的有限访问权限 [!DNL Commerce] 其他帐户 [!DNL Commerce] 账户持有人。
exl-id: adc4fed4-89f4-4b0c-811c-fcf6f94dbc22
feature: User Account
source-git-commit: 4c16436d9fd756ed33ca4b90924be58714f971d4
workflow-type: tm+mt
source-wordcount: '674'
ht-degree: 0%

---

# 共享 [!DNL Commerce] 帐户

您的 [!DNL Commerce] 帐户包含的信息可供信任员工和帮助管理网站的服务提供商使用。 作为主要帐户持有者，您有权向其他帐户授予有限的访问权限 [!DNL Commerce] 账户持有人。 共享访问权限可以撤销，但无法从一个用户转移到另一个用户。

此 [!DNL Commerce] 支持团队无权访问该帐户，也无法为您设置共享访问权限。 只有具有适当权限的主要帐户持有人才能设置共享访问权限。 在共享您的帐户时，所有敏感信息（如账单历史记录或信用卡信息）都会受到保护，并且不会随时与其他用户共享。

>[!NOTE]
>
>具有共享访问权限的用户执行的所有操作由主要帐户持有人全权负责。 对于已共享您的帐户访问权限的用户执行的任何操作，Adobe概不负责。

![共享访问设置](./assets/shared-access.png){width="600" zoomable="yes"}

## 设置共享帐户

1. 在开始之前，请从以下位置获取以下信息： [!DNL Commerce] 的帐户 **新用户**：

   - 此 `Account ID` 左上角显示的 _[!UICONTROL Magento]_选项卡，在&#x200B;**注销**链接。
   - 此 `Email` 与帐户关联的地址。

1. 登录 [[!DNL Commerce] 帐户](commerce-account-create.md).

1. 在左侧导航面板中，单击 **[!UICONTROL Shared Access]**.

1. 单击 **[!UICONTROL Add New User]**.

   ![添加新用户](./assets/shared-access-add.png){width="600" zoomable="yes"}

1. 下 [!UICONTROL _New User Information]_，执行以下操作：

   - 输入 **[!UICONTROL Account ID]** 来自新用户的 [!DNL Commerce] 帐户。
   - 输入 **[!UICONTROL Email]** 与新用户的关联的地址 [!DNL Commerce] 帐户。

   ![新建用户信息](./assets/shared-new-user.png){width="600"}

1. 下 _[!UICONTROL Shared Information]_，请执行以下操作：

   - 要标识共享帐户，请输入 **[!UICONTROL Share Name]**. 此名称供内部参考，仅对您以及与您共享帐户的人可见。
   - 如果要与新用户共享您的个人联系信息，请输入 **[!UICONTROL Your Email]** 和 **[!UICONTROL Your Phone]**.

1. 下 _[!UICONTROL Grant Account Permissions]_，选中每个页面的 [!DNL Commerce] 要共享的产品和服务。

   ![授予帐户权限](./assets/shared-permissions.png){width="600"}

1. 完成后，单击 **[!UICONTROL Create Shared Access]**.

   新的用户信息显示在 _[!UICONTROL Manage Permissions]_“共享访问”页面的部分，并且会向新用户发送一封电子邮件邀请，其中包含访问共享帐户的说明。

   ![管理共享访问的权限](./assets/shared-manage-permissions.png){width="600" zoomable="yes"}

## 访问共享帐户

以下说明是从收到共享帐户邀请的共享用户的角度编写的。

1. 当您收到共享帐户的邀请时，请按照电子邮件中的说明登录到您自己的帐户 [!DNL Commerce] 帐户。

   您帐户的左侧导航面板中有一个 _[!UICONTROL Shared with me]_选项卡。 此_[!UICONTROL Switch Accounts]_ 右上角的控件具有 `My Account` 以及共享帐户的名称。

   ![与我共享](./assets/shared-with-me.png){width="600" zoomable="yes"}

1. 要获得对共享帐户的访问权限，请设置 **[!UICONTROL Switch Accounts]** 共享帐户的名称。

   ![切换到共享帐户](./assets/shared-switch.png){width="600" zoomable="yes"}

   共享帐户显示欢迎消息和联系信息。 左侧导航面板仅包含您有权使用的项目。

1. 要将共享帐户连接到帮助中心，请单击 **[!UICONTROL Support]** 在共享帐户的左侧导航面板中。

   ![支持](./assets/shared-support.png){width="600" zoomable="yes"}

   您可以使用 [Adobe Commerce帮助中心](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/overview.html) 从共享帐户中搜索文章和疑难解答信息、查找已知问题的修补程序以及创建支持工单。

   >[!NOTE]
   >
   >在收到共享访问权限后，用户必须登录到其 [[!DNL Commerce] 帐户](https://account.magento.com/customer/account/login)，导航到 _共享访问_，然后单击 **[!UICONTROL Support]** 选项卡。 此操作仅在第一次运行时需要，以确保 [Adobe Commerce支持知识库](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/overview.html) 已通过 `SSO` 呼叫。

1. 要返回到您自己的帐户，请单击 **返回** 在您的浏览器中控制和设置 **[!UICONTROL Switch Accounts]** 到 `My Account`.

## 撤销共享访问权限

1. 登录到您的Commerce帐户。

1. 在左侧导航面板中，单击 **[!UICONTROL Shared Access]**.

1. 查找要撤销的帐户 _[!UICONTROL Managing Users & Permissions]_并单击&#x200B;**[!UICONTROL Delete]**.

1. 提示确认时，单击 **[!UICONTROL Delete User]**.

>[!NOTE]
>
>您无法删除共享名称为的用户 _来自MAG的云共享访问[XYZ]_ 在此界面中。 有关更多详细信息，请参阅 [如何删除通过Cloud项目被授予共享访问权限的用户？](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html?lang=en#remove-cloud-shared-access-users).

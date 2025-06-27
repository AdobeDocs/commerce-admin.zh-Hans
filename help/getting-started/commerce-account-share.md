---
title: 共享 [!DNL Commerce] 帐户
description: 了解如何为其他 [!DNL Commerce] 帐户持有人授予您 [!DNL Commerce] 帐户的有限访问权限。
exl-id: adc4fed4-89f4-4b0c-811c-fcf6f94dbc22
feature: User Account
source-git-commit: 0ed338044734ac95bd3421c162b01043de49bf77
workflow-type: tm+mt
source-wordcount: '864'
ht-degree: 0%

---

# 共享[!DNL Commerce]帐户

您的[!DNL Commerce]帐户包含的信息可供受信任的员工和帮助管理您网站的服务提供商使用。 作为主要帐户持有人，您有权授予其他[!DNL Commerce]帐户持有人的有限访问权限。 共享访问权限可以撤销，但无法从一个用户转移到另一个用户。

[!DNL Commerce]支持团队没有访问帐户的权限，无法为您设置共享访问权限。 只有具有适当权限的主要帐户持有人才能设置共享访问权限。 当您共享帐户访问权限时，所有敏感信息（如账单历史记录或信用卡信息）都会受到保护，其他用户将永远无法访问。

>[!NOTE]
>
>具有共享访问权限的用户执行的所有操作由主要帐户持有人全权负责。 对于已共享您的帐户访问权限的用户执行的任何操作，Adobe概不负责。

![共享访问设置](./assets/shared-access.png){width="600" zoomable="yes"}

## 设置共享帐户

1. 在开始之前，请从&#x200B;**新共享访问被授权者**&#x200B;的[!DNL Commerce]帐户获取以下信息：

   - 用户必须在account.adobe.com上注册帐户，并通过account.magento.com登录。 有关详细信息，请参阅[创建Commerce帐户](https://experienceleague.adobe.com/zh-hans/docs/commerce-admin/start/commerce-account/commerce-account-create#create-a-commerce-account)。
   - `MAGE ID/Account ID (MAG00XXXXXXX)`显示在&#x200B;_[!UICONTROL Magento]_&#x200B;选项卡的左上角，**注销**&#x200B;链接正上方。
   - 与帐户关联的`Email`地址。

1. 登录到您的[[!DNL Commerce] 帐户](commerce-account-create.md)。

1. 在左侧导航面板中，单击&#x200B;**[!UICONTROL Shared Access]**。

1. 单击&#x200B;**[!UICONTROL Add New User]**。

   ![添加新用户](./assets/shared-access-add.png){width="600" zoomable="yes"}

1. 在[!UICONTROL _New User Information]_下，执行以下操作：

   - 输入新用户的[!DNL Commerce]帐户中的&#x200B;**[!UICONTROL Account ID]**。
   - 输入与新用户的[!DNL Commerce]帐户关联的&#x200B;**[!UICONTROL Email]**&#x200B;地址。

   ![新用户信息](./assets/shared-new-user.png){width="600"}

1. 在&#x200B;_[!UICONTROL Shared Information]_&#x200B;下，执行以下操作：

   - 要识别共享帐户，请输入&#x200B;**[!UICONTROL Share Name]**。 此名称供内部参考，仅对您以及与您共享帐户的人可见。

     最佳做法是将您的组织名称用作[!UICONTROL Share Name]。 不要使用以`CLOUD SHARED ACCESS FROM MAG XYX`开头的名称。
   - 如果要与新用户共享您的个人联系信息，请输入&#x200B;**[!UICONTROL Your Email]**&#x200B;和&#x200B;**[!UICONTROL Your Phone]**。

1. 在&#x200B;_[!UICONTROL Grant Account Permissions]_&#x200B;下，选中要共享的每个[!DNL Commerce]产品和服务的复选框。

   ![授予帐户权限](./assets/shared-permissions.png){width="600"}

1. 单击&#x200B;**[!UICONTROL Create Shared Access]**。

   新用户信息显示在“共享访问”页面的&#x200B;_[!UICONTROL Manage Permissions]_&#x200B;部分中，并且会向新用户发送一封电子邮件邀请，其中包含访问共享帐户的说明。

   ![管理共享访问的权限](./assets/shared-manage-permissions.png){width="600" zoomable="yes"}

>[!NOTE]
>
>无需共享对&#x200B;_[!UICONTROL Security Tool]_&#x200B;的访问权限 — 任何具有MAGE ID的用户都可以使用自己的帐户设置安全扫描工具。 他们只需要必要的权限即可更改网站并使用[所需方法](https://experienceleague.adobe.com/zh-hans/docs/commerce-admin/systems/security/security-scan)之一验证域的所有权。

## 访问共享帐户

以下说明是从收到共享帐户邀请的共享用户的角度编写的。

1. 当您收到共享帐户的邀请时，请按照电子邮件中的说明登录到您自己的[!DNL Commerce]帐户。

   您帐户的左侧导航面板具有新的&#x200B;_[!UICONTROL Shared with me]_&#x200B;选项卡。 右上角的&#x200B;_[!UICONTROL Switch Accounts]_&#x200B;控件具有`My Account`的选项和共享帐户的名称。

   ![与我共享](./assets/shared-with-me.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >   如果您没有看到&#x200B;_[!UICONTROL Switch Accounts]_&#x200B;控件，请与主要帐户持有人联系，并确认他们输入了正确的[帐户信息](#set-up-a-shared-account)。


1. 若要获得对共享帐户的访问权限，请将&#x200B;**[!UICONTROL Switch Accounts]**&#x200B;设置为共享帐户的名称。

   ![切换到共享帐户](./assets/shared-switch.png){width="600" zoomable="yes"}

   共享帐户显示欢迎消息和联系信息。 左侧导航面板仅包含您有权使用的项目。

1. 要将共享帐户连接到帮助中心，请单击共享帐户左侧导航面板中的&#x200B;**[!UICONTROL Support]**。

   ![支持](./assets/shared-support.png){width="600" zoomable="yes"}

   您可以使用共享帐户中的[Adobe Commerce帮助中心](https://experienceleague.adobe.com/zh-hans/docs/commerce-knowledge-base/kb/overview)来搜索文章和疑难解答信息、查找已知问题的修补程序以及创建支持工单。

   >[!NOTE]
   >
   >收到共享访问权限后，要在Experience League上[提交支持案例](https://experienceleague.adobe.com/zh-hans/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide#support-case)，请确保首先在左列中选择以“([!DNL Commerce])”结尾的组织名称。

1. 若要返回您自己的帐户，请在浏览器控件中单击&#x200B;**返回**，并将&#x200B;**[!UICONTROL Switch Accounts]**&#x200B;设置为`My Account`。

## 撤销共享访问权限

1. 登录到您的Commerce帐户。

1. 在左侧导航面板中，单击&#x200B;**[!UICONTROL Shared Access]**。

1. 查找要在&#x200B;_[!UICONTROL Managing Users & Permissions]_&#x200B;下撤消的帐户，然后单击&#x200B;**[!UICONTROL Delete]**。

   >[!NOTE]
   >
   > 如果未显示&#x200B;**[!UICONTROL Delete]**，请检查&#x200B;**[!UICONTROL Share Name]**&#x200B;是否包含命名模式`Cloud Shared Access from MAG0XYZ`。 如果该帐户具有[命名模式且无法删除](https://experienceleague.adobe.com/zh-hans/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide#remove-cloud-shared-access-users)，则这是因为共享访问是由API创建的，而不是直接从[Commerce帐户](https://account.magento.com/)创建的。
   > 
   > 如果不能删除，只需让帐户所有者修改共享访问帐户，并在授予帐户权限下取消选中每个项目。 在该更新之后，用户将无法再访问任何帐户资源。
   > ![图像](https://git.corp.adobe.com/AdobeDocs/commerce-admin.en/assets/38345/55f383e5-89c7-4832-bada-f765b522f4b5)
   >
   > 此外，确保从项目中删除用户，以便他们不再收到电子邮件通知： [前团队成员将收到Adobe Commerce云通知电子邮件](https://experienceleague.adobe.com/zh-hans/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/former-teammembers-receive-cloud-notification-emails)


1. 提示确认时，单击&#x200B;**[!UICONTROL Delete User]**。

>[!NOTE]
>
>您无法在此界面中从MAG[XYZ ]_删除共享名称为_&#x200B;云共享访问的用户。 请参阅[如何删除通过云项目被授予共享访问权限的用户？](https://experienceleague.adobe.com/zh-hans/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide#remove-cloud-shared-access-users)。

## 相关阅读

[共享访问疑难解答](https://experienceleague.adobe.com/zh-hans/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/shared-access-troubleshooting)


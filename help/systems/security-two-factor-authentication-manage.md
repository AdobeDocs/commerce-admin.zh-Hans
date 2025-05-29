---
title: 管理双重身份验证
description: 了解如何为管理员用户管理双重身份验证和重置身份验证器。
exl-id: 68256214-2d50-4c42-846f-306ffc305f25
role: Admin
feature: Configuration, Security, User Account
badgePaas: label="仅限PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="仅适用于云项目(Adobe管理的PaaS基础架构)和内部部署项目上的Adobe Commerce 。"
source-git-commit: 9a68d9702cec9b812414d39e8d04c71751121a37
workflow-type: tm+mt
source-wordcount: '312'
ht-degree: 0%

---

# 管理双重身份验证

无法使用双重身份验证(2FA)登录&#x200B;_管理员_&#x200B;的用户可以尝试同步或解决此问题。 您还可以重置与帐户关联的验证者。 重置后，用户必须再次登录并重新配置所需的身份验证器。

如果您在使用2FA登录时遇到问题，请考虑以下事项：

- 某些移动设备应用程序包含同步选项。 此选项将重新连接应用程序和服务器，并同步设备和服务器上的时间设置。
- 撤销设备或重置身份验证程序可以帮助用户连接。
- 清除Adobe Commerce或Magento Open Source安装的Web缓存和Cookie也很有帮助。 身份验证者(如Google)使用生成的Cookie来保存访问权和持续时间。 清除特定浏览器和存储域的Cookie。
- 阻止Cookie会阻止某些验证者（如[!DNL Google Authenticator]）完成验证过程。 向浏览器添加一条规则，以允许为Adobe Commerce安装提供Cookie。

若要从命令行重置验证器和更高级的故障排除信息，请参阅开发人员文档中的[双重身份验证](https://developer.adobe.com/commerce/testing/functional-testing-framework/two-factor-authentication/)。

**_要重置用户帐户的验证者：_**

>[!NOTE]
>
>要为其他用户重置2FA提供程序，您必须是具有`All`权限的&#x200B;_管理员_，或者对您的角色具有`Custom`权限，其中已选择[!UICONTROL System] > [!UICONTROL Permissions] > [!UICONTROL Two Factor Auth]和[!UICONTROL System] > [!UICONTROL Permissions] > [!UICONTROL All Users]。 若要了解详细信息，请参阅[用户角色](permissions-user-roles.md)。

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL All Users]**。

1. 选择用户并在编辑模式下打开帐户。

1. 向下滚动到&#x200B;_[!UICONTROL Current User Identity Verification]_部分并输入密码。

1. 在左侧面板中，单击&#x200B;**[!UICONTROL 2FA]**。

1. 在&#x200B;_[!UICONTROL Configuration reset]_部分中，单击&#x200B;**[!UICONTROL Reset]**和&#x200B;**[!UICONTROL OK]**以确认。

   ![用户帐户 — 启用2FA](./assets/admin-2fa-config-reset-providers.png){width="600" zoomable="yes"}

   如果用户希望将所需的2FA方法还原到其帐户，他们必须从&#x200B;_登录_&#x200B;页面重新配置每个方法。

1. 完成后，单击&#x200B;**[!UICONTROL Save User]**。

---
title: 管理双重身份验证
description: 了解如何为管理员用户管理双重身份验证和重置身份验证器。
exl-id: 68256214-2d50-4c42-846f-306ffc305f25
role: Admin
feature: Configuration, Security, User Account
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '300'
ht-degree: 0%

---

# 管理双重身份验证

无法登录的用户 _管理员_ 使用双重身份验证(2FA)可以尝试同步或解决问题。 您还可以重置与帐户关联的验证者。 重置后，用户必须再次登录并重新配置所需的身份验证器。

如果您在使用2FA登录时遇到问题，请考虑以下事项：

- 某些移动设备应用程序包含同步选项。 此选项将重新连接应用程序和服务器，并同步设备和服务器上的时间设置。
- 撤销设备或重置身份验证程序可以帮助用户连接。
- 清除Adobe Commerce或Magento Open Source安装的Web缓存和Cookie也很有帮助。 身份验证者(如Google)使用生成的Cookie来保存访问权和持续时间。 清除特定浏览器和存储域的Cookie。
- 阻止Cookie可阻止某些验证者，例如 [!DNL Google Authenticator]，以完成验证过程。 向浏览器添加一条规则，以允许为Adobe Commerce安装提供Cookie。

要从命令行重置验证器和更多高级故障排除信息，请参见 [双重身份验证](https://developer.adobe.com/commerce/testing/functional-testing-framework/two-factor-authentication/) 在开发人员文档中。

**_要重置用户帐户的验证者，请执行以下操作：_**

>[!NOTE]
>
>要为其他用户重置2FA提供商，您必须是 _管理员_ 替换为 `All` 权限，或具有 `Custom` 您角色的权限 [!UICONTROL System] > [!UICONTROL Permissions] > [!UICONTROL Two Factor Auth] 和 [!UICONTROL System] > [!UICONTROL Permissions] > [!UICONTROL All Users] 已选定。 要了解更多信息，请参阅 [用户角色](permissions-user-roles.md).

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL All Users]**.

1. 选择用户并在编辑模式下打开帐户。

1. 向下滚动到 _[!UICONTROL Current User Identity Verification]_并输入您的密码。

1. 在左侧面板中，单击 **[!UICONTROL 2FA]**.

1. 在 _[!UICONTROL Configuration reset]_部分，单击&#x200B;**[!UICONTROL Reset]**和&#x200B;**[!UICONTROL OK]**以确认。

   ![用户帐户 — 启用2FA](./assets/admin-2fa-config-reset-providers.png){width="600" zoomable="yes"}

   如果用户希望将所需的2FA方法恢复到其帐户，他们必须从 _登录_ 页面。

1. 完成后，单击 **[!UICONTROL Save User]**.

---
title: 管理管理员用户帐户
description: 了解如何创建管理员用户帐户并分配角色以向管理员功能授予权限。
exl-id: 65cca7a8-3d44-4c8c-a758-c0de03d53e11
role: Admin
feature: Admin Workspace, Roles/Permissions, User Account, Security
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '1025'
ht-degree: 0%

---

# 管理管理员用户帐户

首次安装存储时，将使用授予您完全管理访问权限的登录凭据创建默认的Admin帐户。 作为最佳实践，您应创建另一个具有完全管理员访问权限的用户帐户。 这样，您可以将一个帐户用于日常管理活动，并将另一个帐户保留为“超级管理员”帐户。 如果您忘记了常规凭据，或者凭据变得不可用，这可能会很有帮助。

如果您的团队或服务提供商中有其他人需要访问权限，您可以为每个人创建单独的用户帐户，并根据他们的业务知情需要分配受限访问权限。 要限制用户可在“管理员”中访问的网站或商店，您必须首先 [创建角色](permissions-user-roles.md) 范围有限，并且只选择了必要的资源。 然后，您可以将角色分配给特定的用户帐户。 分配给受限角色的管理员用户只能查看和更改与该角色关联的网站或商店的数据，但不能更改任何全局设置或数据。

>[!NOTE]
>
>具有Adobe ID并希望简化登录Adobe Commerce和Adobe业务产品的Adobe Commerce商家可以将Commerce身份验证与Adobe IMS身份验证工作流集成。 为您的Commerce商店启用此集成后，每个管理员用户必须使用其Adobe凭据（而非其Commerce凭据）登录。 请参阅 [AdobeIdentity Management服务(IMS)集成概述](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/ims/adobe-ims-integration-overview.html).

对于临时用户或角色，您还可以设置用户帐户的到期日期。

<!--  update this to a better info-graphic ![User types for your Admin](./assets/merchant-admin-users.png) -->

## 创建用户

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL All Users]**.

1. 在右上角，单击 **[!UICONTROL Add New User]**.

   要编辑现有用户，请单击网格中的用户名。 您可以修改 _[!UICONTROL User Info]_和_[!UICONTROL User Role]_ 部分。

1. 在 _[!UICONTROL Account Information]_部分，执行以下操作：

   ![用户帐户信息](./assets/permissions-user-new.png){width="600" zoomable="yes"}

   - 输入 **[!UICONTROL User Name]** 帐户。

     用户名应该容易记忆。 不区分大小写。 例如，如果用户名为 `John`，他们还可以以 `john`.

   - 完成以下信息：

      - **[!UICONTROL First Name]**
      - **[!UICONTROL Last Name]**
      - **[!UICONTROL Email address]**

     每个用户帐户必须具有唯一的电子邮件地址。

   - 输入 **[!UICONTROL Password]** 用于帐户。

     >[!NOTE]
     >
     >管理员密码长度必须为7个或更多字符，且包含字母和数字。 有关其他密码选项，请参阅 [配置管理员安全](security-admin.md).

   - 对象 **[!UICONTROL Password Confirmation]**，请重新输入密码以确保正确输入。

   - 如果您的商店使用多种语言，请设置 **[!UICONTROL Interface Locale]** 更改为管理员界面使用的语言。

1. 设置 **[!UICONTROL This Account is]** 到 `Active`.

1. 单击日历图标以设置 **[!UICONTROL Expiration Date]** （对于用户帐户）。

   当用户或角色为临时角色时，定义到期日期会很有帮助。 过期日期后，用户帐户状态将更改为 `Inactive` 并且可以根据需要进行更新。

1. 下 _[!UICONTROL Current User Identity Verification]_，输入您的用户帐户密码。

>[!IMPORTANT]
>
>使用 _[!UICONTROL Account Information]_部分完成，您可以保存用户。 新用户将显示在_[!UICONTROL Users]_ 网格，但在分配角色之前，用户名无法登录。

## 分配用户角色

1. 在左侧面板中，单击 **[!UICONTROL User Role]**.

   网格会列出所有现有的用户角色。 要开一家新店， _[!UICONTROL Administrators]_是唯一可用的角色。

   ![管理员 — 添加新用户角色](./assets/permissions-user-roles.png){width="600" zoomable="yes"}

1. 在 _[!UICONTROL Assigned]_列中，选择一个用户角色。

   您可以 [查看现有或定义其他用户角色](permissions-user-roles.md). 定义角色后，必须编辑用户帐户以分配新角色。

## 验证或重置2FA提供程序

1. 打开管理员用户帐户。

1. 在左侧面板中，单击 **[!UICONTROL 2FA]**.

   ![管理员 — 添加新用户角色](./assets/permissions-user-2fa.png){width="600" zoomable="yes"}

1. 验证可用于以下项的2FA解决方案： _管理员_ 建议每个用户在登录之前安装他们要使用的解决方案。

   只需通过一个2FA解决方案即可登录到 _管理员_.

1. 如果用户需要重新安装2FA解决方案，您可以重置当前2FA配置。

   这要求用户重复设置过程，然后才能再次登录。 例如，用户可能有一部新的智能手机，需要重新安装Google Authenticator。 要清除用户的当前2FA设置，请单击 **[!UICONTROL Reset (Provider)]** 清除的每个解决方案。 出现提示时，单击 **[!UICONTROL OK]** 以确认。

   用户将收到一封电子邮件，其中包含指向的链接 [配置2FA](security-two-factor-authentication.md). 该链接只能使用一次。 如果用户尝试多次登录，则在每次尝试后都会发送一个新链接。

1. 单击 **[!UICONTROL Save User]**.

1. 出现提示时，输入密码以确认身份，然后再次单击 **[!UICONTROL Save User]**.

   此 _[!UICONTROL Users]_网格将打开并列出所有用户。

## 删除管理员用户

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL All Users]**.

1. 使用网格上方的筛选器找到用户帐户，然后单击用户名。

1. 出现提示时，输入密码以确认您的身份。

1. 在右上角，单击 **[!UICONTROL Delete User]**.

1. 要确认操作，请单击 **[!UICONTROL OK]**.

## 忘记密码并重置电子邮件

管理员电子邮件模板配置可确定用户忘记并重置密码时发送的电子邮件。 此配置指定作为邮件发件人显示的商店联系人，以及密码恢复链接保持有效的时间。

**_要配置管理员电子邮件模板，请执行以下操作：_**

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Setting]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中，展开 **[!UICONTROL Advanced]** 并选择 **[!UICONTROL Admin]**.

1. 展开 ![扩展切换器](../assets/icon-display-expand.png) 该 **[!UICONTROL Admin User Emails]** 部分。

   ![高级配置 — 管理员电子邮件模板设置](../configuration-reference/advanced/assets/admin-admin-user-emails.png){width="600" zoomable="yes"}

1. 设置 **[!UICONTROL Forgot Password Email Template]** 到管理员用户忘记密码时发送的模板。

1. 设置 **[!UICONTROL Forgot and Reset Email Sender]** 将显示为邮件发件人的商店联系人。

1. 设置 **[!UICONTROL User Notification Template]** 默认用于管理员通知的电子邮件模板。

1. 完成后，单击 **[!UICONTROL Save Config]**.

## 锁定的用户

为了您的企业安全，默认情况下，用户帐户在六次尝试失败后会被锁定。 [登录](../getting-started/admin-signin.md) 发送给管理员。 当前锁定的用户帐户将显示在“锁定的用户”网格中。 具有完全管理员权限的任何其他用户都可以解锁帐户。

其他密码安全措施可在 [高级管理员](../configuration-reference/advanced/admin.md#security) 配置。 请参阅 [管理员安全](security-admin.md).

![登录屏幕警报 — 帐户暂时禁用](./assets/admin-login-locked-out-message.png){width="300"}

**_要解锁管理员帐户，请执行以下操作：_**

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL Locked Users]**.

1. 在网格中，选中锁定帐户的复选框。

   ![权限 — 锁定的用户帐户](./assets/permissions-locked-users-grid.png){width="600" zoomable="yes"}

1. 在左上角，设置 **[!UICONTROL Actions]** 到 `Unlock`.

1. 单击 **[!UICONTROL Submit]** 以解锁帐户。

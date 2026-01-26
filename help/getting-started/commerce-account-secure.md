---
title: 保护您的 [!DNL Commerce] 帐户
description: 了解如何使用双重身份验证来保护您的 [!DNL Commerce] 帐户。
exl-id: 4847b5cb-a93a-40d0-8c31-c30afa27c0ce
feature: User Account
source-git-commit: cace9d1de00955494d8bc607c017778ff7df4806
workflow-type: tm+mt
source-wordcount: '1677'
ht-degree: 0%

---

# 保护您的[!DNL Commerce]帐户

双重身份验证（TFA或2FA）是添加的安全层，可更好地保护您的[!DNL Commerce]帐户免遭未经授权的访问。 要完成登录过程，除了标准用户名和密码凭据外，TFA还需要&#x200B;_秒因子_。 第二个因素采用临时验证代码的形式，这些代码由安装在您的移动设备上并与您的[!DNL Commerce]帐户配对的TFA应用程序持续生成。

启用TFA后，您的帐户将更加安全。 未经授权的用户无法登录，除非他们同时拥有您的用户名和密码凭据（第一个因素）以及您个人设备上的TFA应用程序的有效验证代码（第二个因素）。

>[!NOTE]
>
>保护存储区&#x200B;_管理员_&#x200B;的双重身份验证具有单独的设置。 若要了解详细信息，请参阅[双重身份验证](../systems/security-two-factor-authentication.md)。

## 开始之前

要使用TFA，您必须在个人设备（如智能手机、平板电脑、计算机）上安装TFA应用程序。 这里有很多种可供选择的方式，但也有一些颇受欢迎且免费的选项，包括：

- Google身份验证器(iOS、Android™、BlackBerry®)

- 奥西(iOS、Android™)

- Microsoft® Authenticator(iOS、Android™、Windows Phone)

## 启用双重身份验证

1. 登录到您的[[!DNL Commerce] 帐户](https://account.magento.com/customer/account/login){:target="_blank"}。

1. 在左侧导航窗格中，选择&#x200B;**[!UICONTROL Account Settings]**，然后选择&#x200B;**[!UICONTROL Two-factor Authentication]**。

   ![启用TFA](./assets/2fa-enable.png){width="600" zoomable="yes"}

1. 选择&#x200B;**[!UICONTROL Enable]**&#x200B;开始双重身份验证设置过程。

1. 输入发送到您的电子邮件的&#x200B;**[!UICONTROL Verification Code]**，然后选择&#x200B;**[!UICONTROL Verify Code]**&#x200B;以继续。

   ![输入验证码](./assets/2fA-verification-code-prompt.png){width="400"}

1. 打开您下载并安装在个人设备上的双重身份验证应用程序。

1. 在[!UICONTROL SETUP TWO-FACTOR AUTHENTICATION]表单上，使用&#x200B;**[!UICONTROL Setup Code]**&#x200B;将Adobe Commerce添加到您的TFA应用程序。

   ![将Adobe Commerce添加到TFA应用](./assets/commerce-account-2fa-setup-app.png){width="400"}

   您可以通过使用TFA应用程序扫描二维码或手动输入来添加代码。 此代码将您的TFA应用程序与您的[!DNL Commerce]帐户配对，并启用生成TFA应用程序的权限以生成验证代码以便安全访问帐户。

1. 完成设置。

   - 在[!UICONTROL SETUP TWO FACTOR-AUTHENTICATION]窗体上，输入双重身份验证应用程序中的验证码。

   - 选择&#x200B;**[!UICONTROL Verify Code]**。

   >[!NOTE]
   >
   >为安全起见，TFA应用程序中的验证代码会不断过期并重新生成。 **_始终_**&#x200B;使用当前显示的代码。

1. 将所显示的&#x200B;**[!UICONTROL Recovery Codes]**&#x200B;保存在安全且可访问的位置。

   ![存储恢复代码](./assets/commerce-account-2fa-store-recovery-codes.png){width="400"}

   如果您在登录到[!DNL Commerce]帐户时无法提供验证码，则必须使用恢复码来重新获得帐户访问权限。

   每个恢复代码只能使用一次，但您可以[生成](#generate-new-recovery-codes)新恢复代码。 恢复代码区分大小写。

1. 选中确认复选框并选择&#x200B;**[!UICONTROL Submit]**&#x200B;以继续。

1. 为确保恢复对帐户的访问权限，请输入&#x200B;**[!UICONTROL Recovery Email]**。

   如果您无法从双重身份验证应用程序生成验证码，并且您无权访问未使用的预生成恢复码，则需要此电子邮件地址。

   每24小时生成一次临时恢复代码并将其发送到指定的恢复电子邮件地址。 使用此代码可重新获得帐户访问权限。

   >[!IMPORTANT]
   >
   >保持对恢复电子邮件帐户的访问权限。 否则，无法使用发送到该帐户的临时恢复代码。

   ![设置恢复电子邮件](./assets/commerce-account-2fa-set-recovery-email.png){width="400"}

1. 选中确认复选框并选择&#x200B;**[!UICONTROL Submit]**&#x200B;以完成双重身份验证设置过程。

   - 将向与您的[!DNL Commerce]帐户关联的电子邮件地址发送通知，以确认您已成功启用双重身份验证。

   - 系统会向您的恢复电子邮件帐户发送通知，以确认配置。

>[!TIP]
>
>如果丢失个人设备或获得新设备，您可以[更改双重身份验证应用](#change-your-two-factor-authentication-application)并生成新的恢复代码。

## 使用验证码登录

1. 转到[!DNL Commerce] [帐户登录](https://account.magento.com/customer/account/login){:target="_blank"}。

1. 输入用户名和密码凭据，然后选择&#x200B;**[!UICONTROL Login]**。

1. 在出现提示时，输入双因素身份验证应用程序中显示的&#x200B;**[!UICONTROL Verification Code]**。

   ![输入验证码](./assets/commerce-account-2fa-login-verification-code.png){width="600"}

1. 选择&#x200B;**[!UICONTROL Submit]**&#x200B;以完成登录过程。

## 使用恢复代码登录

1. 转到[!DNL Commerce] [帐户登录](https://account.magento.com/customer/account/login){:target="_blank"}。

1. 输入用户名和密码凭据，然后选择&#x200B;**[!UICONTROL Login]**。

1. 选择&#x200B;**[!UICONTROL Use recovery code]**&#x200B;以绕过验证码提示。

1. 出现提示时输入未使用的&#x200B;**[!UICONTROL Recovery Code]**。

   ![输入恢复代码](./assets/2fa-recovery-code.png){width="600"}

1. 选择&#x200B;**[!UICONTROL Submit]**&#x200B;以完成登录过程。

## 使用恢复电子邮件登录

1. 登录到您的[[!DNL Commerce] 帐户](https://account.magento.com/customer/account/login){:target="_blank"}。

1. 输入用户名和密码凭据，然后选择&#x200B;**[!UICONTROL Login]**。

1. 选择&#x200B;**[!UICONTROL Use recovery code]**&#x200B;以绕过验证码提示。

1. 要通过电子邮件获取临时恢复代码，请选择&#x200B;**[!UICONTROL recovery email]**&#x200B;链接。

   ![使用恢复电子邮件](./assets/2fa-recovery-email.png){width="600"}

1. 打开恢复电子邮件帐户以获取临时代码，然后在指定字段中输入该代码。

1. 选择&#x200B;**[!UICONTROL Submit]**&#x200B;以完成登录过程。

使用临时恢复代码访问帐户后，[生成新的恢复代码](#generate-new-recovery-codes)并保存这些代码以防止进一步的帐户访问问题。

## 查看您的恢复代码

1. 转到[!DNL Commerce] [帐户登录](https://account.magento.com/customer/account/login){:target="_blank"}。

1. 输入用户名和密码凭据，然后选择&#x200B;**[!UICONTROL Login]**。

1. 使用前面介绍的双重身份验证方法之一完成登录过程。

1. 在左侧导航窗格中，选择&#x200B;**[!UICONTROL Account Settings]**，然后选择&#x200B;**[!UICONTROL Two-factor Authentication]**。

   ![2FA设置](./assets/commerce-account-2fa-manage.png){width="600" zoomable="yes"}

1. 要查看预生成的恢复代码，请选择&#x200B;**查看恢复代码**。

1. 输入发送到您的电子邮件的&#x200B;**[!UICONTROL Verification Code]**，然后选择&#x200B;**[!UICONTROL Verify Code]**&#x200B;以继续。

   ![输入验证码](./assets/2fA-verification-code-prompt.png){width="400"}

1. 将所显示的&#x200B;**恢复代码**&#x200B;保存在安全且可访问的位置。

   如果您无法提供验证代码以登录到[!DNL Commerce]帐户，则使用恢复代码是重新获得帐户访问权限的唯一方法。

   每个恢复代码仅供一次使用，但您始终可以[生成](#generate-new-recovery-codes)新恢复代码。 恢复代码区分大小写。

   ![查看恢复代码](./assets/2fa-view-recovery.png){width="400"}

1. 选中确认复选框，然后选择&#x200B;**[!UICONTROL Submit]**&#x200B;关闭对话框。

## 生成新的恢复代码

1. 转到[!DNL Commerce] [帐户登录](https://account.magento.com/customer/account/login){:target="_blank"}。

1. 输入用户名和密码凭据，然后选择&#x200B;**[!UICONTROL Login]**。

1. 使用前面介绍的双重身份验证方法之一完成登录过程。

1. 在左侧导航窗格中，选择&#x200B;**[!UICONTROL Account Settings]**，然后选择&#x200B;**[!UICONTROL Two-factor Authentication]**。

1. 要生成新的预生成的恢复代码，请选择&#x200B;**生成新的恢复代码**。

1. 输入发送到您的电子邮件的&#x200B;**[!UICONTROL Verification Code]**，然后选择&#x200B;**[!UICONTROL Verify Code]**&#x200B;以继续。

1. 将所显示的&#x200B;**恢复代码**&#x200B;保存在安全且可访问的位置。

   如果您在登录到[!DNL Commerce]帐户时无法提供验证代码，则使用恢复代码是重新获得帐户访问权限的唯一方法。

   现在，所有以前生成的恢复代码都将变为无效，应将其丢弃（只有当前生成的恢复代码集才能正常工作）。 恢复代码区分大小写。

1. 选中确认复选框，然后选择&#x200B;**[!UICONTROL Submit]**&#x200B;关闭对话框。

## 更改恢复电子邮件

1. 转到[!DNL Commerce] [帐户登录](https://account.magento.com/customer/account/login){:target="_blank"}。

1. 输入用户名和密码凭据，然后选择&#x200B;**[!UICONTROL Login]**。

1. 使用前面介绍的双重身份验证方法之一完成登录过程。

1. 在左侧导航窗格中，选择&#x200B;**[!UICONTROL Account Settings]**，然后选择&#x200B;**[!UICONTROL Two-factor Authentication]**。

1. 选择&#x200B;**更改恢复电子邮件**&#x200B;以更改您帐户的文件的恢复电子邮件。

1. 输入发送到您的电子邮件的&#x200B;**[!UICONTROL Verification Code]**，然后选择&#x200B;**[!UICONTROL Verify Code]**&#x200B;以继续。

1. 若要帮助确保您可以恢复对帐户的访问，请输入&#x200B;**恢复电子邮件**。

   如果您无法从双重身份验证应用程序生成验证码，并且您无权访问未使用的预生成恢复码，则需要此电子邮件地址。

   每24小时生成一次临时恢复代码并将其发送到指定的恢复电子邮件地址。 您可以使用此代码重新获得帐户访问权限。

   >[!IMPORTANT]
   >
   >保持对恢复电子邮件帐户的访问权限。 否则，无法使用发送到该帐户的临时恢复代码。

1. 选中确认复选框，然后选择&#x200B;**[!UICONTROL Submit]**&#x200B;关闭对话框。

   系统会向您指定的恢复电子邮件发送电子邮件通知，以确认特定电子邮件地址已归档为接收临时恢复代码的恢复电子邮件。

## 更改您的双重身份验证应用程序

1. 转到[!DNL Commerce] [帐户登录](https://account.magento.com/customer/account/login){:target="_blank"}。

1. 输入用户名和密码凭据，然后选择&#x200B;**[!UICONTROL Login]**。

1. 使用前面介绍的双重身份验证方法之一完成登录过程。

1. 在左侧导航窗格中，选择&#x200B;**[!UICONTROL Account Settings]**，然后选择&#x200B;**[!UICONTROL Two-factor Authentication]**。

1. 选择&#x200B;**更改TFA应用程序**&#x200B;以使用其他TFA应用程序与您的magento.com帐户。

1. 输入发送到您的电子邮件的&#x200B;**[!UICONTROL Verification Code]**，然后选择&#x200B;**[!UICONTROL Verify Code]**&#x200B;以继续。

1. 在个人设备上打开双重身份验证应用程序。

1. 在双重身份验证应用程序中输入&#x200B;**设置代码**。

   您可以使用TFA应用程序扫描二维码或手动输入来添加代码。 此代码将您的TFA应用程序与您的[!DNL Commerce]帐户配对，并允许TFA应用程序的权限生成验证代码以便安全访问帐户。

   >[!NOTE]
   >
   >为安全起见，TFA应用程序中的验证代码会不断过期并重新生成。 **_始终_**&#x200B;使用当前显示的代码。

1. 现在您的TFA应用程序已与[!DNL Commerce]帐户配对，请输入TFA应用程序中显示的&#x200B;**[!UICONTROL Verification Code]**，然后选择&#x200B;**[!UICONTROL Verify Code]**&#x200B;以继续。

1. 将所显示的&#x200B;**恢复代码**&#x200B;保存在安全且可访问的位置。

   如果您在登录到[!DNL Commerce]帐户时无法提供验证码，则重新获得帐户访问权限的唯一方法是使用恢复码。

   每个恢复代码仅供一次使用，但您始终可以[生成](#generate-new-recovery-codes)新恢复代码。 恢复代码区分大小写。 恢复代码区分大小写。

1. 选中复选框以确认，选择&#x200B;**[!UICONTROL Submit]**&#x200B;以继续。

1. 若要帮助确保您可以恢复对帐户的访问，请输入&#x200B;**恢复电子邮件**。

   如果您无法从双重身份验证应用程序生成验证码，并且您无权访问未使用的预生成恢复码，则需要此电子邮件地址。

   每24小时生成一次临时恢复代码并将其发送到指定的恢复电子邮件地址。 使用此代码可重新获得帐户访问权限。

   >[!IMPORTANT]
   >
   >保持对恢复电子邮件帐户的访问权限。 否则，无法使用发送到该帐户的临时恢复代码。

1. 选中确认复选框并选择&#x200B;**[!UICONTROL Submit]**&#x200B;以完成双重身份验证设置过程。

   系统会向您指定的恢复电子邮件发送电子邮件通知，以确认特定电子邮件地址已归档为恢复电子邮件，用于接收临时恢复代码。

## 禁用双重身份验证

>[!IMPORTANT]
>
>如果您的组织安全策略要求对Adobe Commerce帐户进行多重身份验证，则无法禁用双重身份验证。

1. 转到[!DNL Commerce] [帐户登录](https://account.magento.com/customer/account/login){:target="_blank"}。

1. 输入用户名和密码凭据，然后选择&#x200B;**[!UICONTROL Login]**。

1. 使用前面介绍的双重身份验证方法之一完成登录过程。

1. 在左侧导航窗格中，选择&#x200B;**[!UICONTROL Account Settings]**，然后选择下面的&#x200B;**[!UICONTROL Two-factor Authentication]**。

1. 选择&#x200B;**[!UICONTROL Disable]**&#x200B;以开始TFA停用过程。

1. 输入发送到您的电子邮件的&#x200B;**[!UICONTROL Verification Code]**，然后选择&#x200B;**[!UICONTROL Verify Code]**&#x200B;以继续。

1. 选中确认复选框并选择&#x200B;**[!UICONTROL Submit]**&#x200B;以完成双重身份验证的停用。

   系统发送电子邮件确认，指示已在您的[!DNL Commerce]帐户上禁用TFA。

   ![禁用TFA](./assets/2fa-disable.png){width="400"}

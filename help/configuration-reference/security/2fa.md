---
title: ’[!UICONTROL Security] &gt； [!UICONTROL 2FA]’
description: 查看 [!UICONTROL Security] &gt； [!UICONTROL 2FA] 商务管理员页面。
exl-id: d3f6e16b-6eba-47db-a9dd-cb3268d1a13f
feature: Configuration, Security
source-git-commit: d6f9c5186276b28cada318cbe765e2271d34bb58
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 1%

---

# [!UICONTROL Security] > [!UICONTROL 2FA]

>[!NOTE]
>
>启用了AdobeIdentity Management服务(IMS)身份验证的存储已禁用本地Adobe Commerce和Magento Open Source双重身份验证(2FA)。 使用Adobe凭据登录到其Adobe Commerce实例的管理员用户不需要对许多管理员任务重新进行身份验证。 当管理员用户登录到其当前会话时，身份验证由Adobe IMS处理。 请参阅 [将Adobe Commerce与Adobe IMS集成概述](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/ims/adobe-ims-integration-overview.html).

{{config}}

有关更改这些设置的详细信息，请参阅 [双重身份验证(2FA)](../../systems/security-two-factor-authentication.md) 在 _管理系统指南_.

## [!UICONTROL General]

![常规](./assets/2fa-general.png)<!-- zoom -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Providers to use] | 全局 | 指示所需的双重身份验证方法。 如果选择多个提供程序，则每个用户在下次登录时都需要配置每个2FA方法。 |
| [!UICONTROL Configuration Email URL for Web API] | 全局 | 对于自定义实施，发送到的备用电子邮件配置链接的URL _管理员_ 首次登录的用户。 在电子邮件模板中，使用占位符 `:tfat` 指示令牌的注入位置。 |

{style="table-layout:auto"}

## [!UICONTROL Google]

![Google](./assets/2fa-google.png)<!-- zoom -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL OTP Window] | 全局 | 确定系统在管理员的一次性密码(OTP)过期后接受多长时间（以秒为单位）。 不能超过单个OTP的生命周期（通常为30秒）。 默认： `29` |

{style="table-layout:auto"}

## [!UICONTROL Duo Security]

![双核安全性](./assets/2fa-duo-security.png)<!-- zoom -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Integration Key] | 全局 | 来自您的的集成密钥 [!DNL Duo Security] 帐户。 |
| [!UICONTROL Secret Key] | 全局 | 来自您的密钥 [!DNL Duo Security] 帐户。 |
| [!UICONTROL API Hostname] | 全局 | 来自您的 [!DNL Duo Security] 帐户。 |

{style="table-layout:auto"}

## [!UICONTROL Authy]

![authy](./assets/2fa-authy.png)<!-- zoom -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL API Key] | 全局 | 来自您的 [!DNL Authy] 帐户。 |
| [!UICONTROL OneTouch Message] | 全局 | 显示在 [!DNL Authy] 登录时验证者。 默认： `Login request to your Magento Admin` |

{style="table-layout:auto"}

## [!UICONTROL U2F Key]

![U2F密钥](./assets/2fa-u2f-key.png)<!-- zoom -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL WebApi Challenge Domain] | 全局 | 用于发出和处理的域 [!DNL WebAuthn] 自定义WebAPI实施面临的挑战。 |

{style="table-layout:auto"}

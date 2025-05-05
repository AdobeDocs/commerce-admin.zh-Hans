---
title: AdobeIdentity Management服务(IMS)集成概述
description: 引入了Adobe Commerce管理员登录与Adobe IMS的可选集成
exl-id: 106d731c-a541-4a19-a38c-221e80740508
feature: Identity Management
source-git-commit: 3ff5807fd0a3ebf2e9d4f9c085852dd7777a1103
workflow-type: tm+mt
source-wordcount: '767'
ht-degree: 0%

---

# AdobeIdentity Management服务(IMS)集成概述

{{ee-feature}}

拥有Adobe帐户的Adobe Commerce管理员用户现在可以使用其Adobe ID登录到Adobe Commerce。 AdobeIdentity Management服务(IMS)是Adobe的基于OAuth 2.0的身份管理功能，支持身份验证。 将Commerce管理员身份验证集成到Adobe业务产品的IMS身份验证工作流中，可以简化与其他Adobe产品一起工作的用户的身份验证过程。 此集成是可选的，并且是按实例启用的。 启用此集成后，只有管理员用户工作流会受到影响。 

Commerce Admin IMS集成所需的模块打包到`adobe-ims-metapackage`中，该版本与Adobe Commerce核心版本捆绑在一起。

要实施此集成，请参阅[配置Commerce与IMS的管理员集成](./adobe-ims-config.md)。

## 与IMS集成后对管理员工作流和界面所做的更改

启用此集成后，Commerce管理员用户将体验更改为默认的Commerce管理员登录和身份验证工作流，因为他们需要在管理员中执行需要重新身份验证的例行任务，例如创建管理员用户。 启用模块需要在Adobe组织级别实施双重身份验证(2FA)。 默认管理员登录和2FA被禁用，_[!UICONTROL Sign In with Adobe ID]_&#x200B;按钮取代了默认管理员登录表单。 权限仍由管理员进行管理。

## 管理员与IMS集成如何影响Commerce密码

与Adobe IMS集成的Commerce部署需要拥有Adobe ID帐户，该帐户有权访问IMS启用过程中为Commerce应用程序配置的Adobe IMS组织。  启用IMS集成后，管理员用户将使用其Adobe凭据通过Adobe登录页面进行身份验证。 只要启用了Adobe IMS集成，管理员用户的Commerce密码和用户名就不会再用于身份验证。

如果禁用了IMS集成，则管理员用户必须使用其Commerce用户名和密码再次通过Adobe Commerce进行身份验证。 管理员用户在启用此集成之前，应该保存其Commerce管理员凭据（用户名和密码）和2FA凭据。

用户身份验证中涉及的某些后端组件仍需要非null密码。 为满足此要求，Commerce在`admin_user`表中为新创建的管理员用户创建随机密码。

Commerce应用程序的用户帐户和角色权限仍由Commerce管理员进行管理。


## 使用IMS凭据生成Web API令牌

在Commerce实例中启用与Adobe IMS的管理员身份验证后，Commerce管理员API会受到影响。 管理员用户无法再使用Commerce实例颁发的凭据。 这些是登录到管理员并获取访问令牌所需的凭据，服务可以使用这些凭据向管理员REST和SOAP API发出请求。

启用Adobe IMS集成后，管理员用户必须为需要身份验证的Adobe Commerce API端点使用[Adobe IMS OAuth令牌](https://developer.adobe.com/developer-console/docs/guides/authentication/OAuthIntegration/)。 客户端解决方案可动态获取令牌以供Web API使用。 在配置此集成时，将为REST和SOAP Web API区域启用此身份验证机制。

有关Web API如何使用Commerce访问令牌（包括IMS访问令牌）的概述，请参阅[基于令牌的身份验证](https://developer.adobe.com/commerce/webapi/get-started/authentication/gs-authentication-token/)。

## Commerce会话管理和Adobe IMS访问令牌

访问令牌包含用户凭据和登录会话信息。 用户经过身份验证并启动会话后，这两个变量将添加到用户的会话中：

`token_last_check_time`。 标识当前时间，并由`\Magento\AdminAdobeIms\Plugin\BackendAuthSessionPlugin`插件使用。

`adobe_access_token` — 标识在授权期间收到的`ACCESS_TOKEN`值。

`\Magento\AdminAdobeIms\Plugin\BackendAuthSessionPlugin`插件检查`token_last_check_time`是否在10分钟前更新。 如果十分钟前检查了`token_last_check_time`，则身份验证工作流会对IMS进行API调用以验证访问令牌，并且会话会继续进行。 如果访问令牌有效，则`token_last_check_time`值将更新为当前时间。 如果令牌无效，会话将终止。

## 重要文件

`adminAdobeIms` — 提供基于`AdobeImsApi`模块的管理员登录的实现。

`admin_adobe_ims_webapi` — 维护所有已验证访问令牌的记录。 当令牌被验证或失效时，其状态的记录将保留在此表中。

`adobeIms` — 实现与Adobe IMS集成相关的所有业务逻辑（保留以防止向后不兼容）。

`adobeImsApi` — 声明支持与Adobe IMS集成的接口。

`adminadobe-ims.log` — 错误日志文件。

## 启用集成

Adobe IMS中继随Adobe Commerce 2.4.5及更高版本一起安装，但必须配置才能使用。 它扩展`AdobeIms`模块以支持启用身份验证逻辑(`AdminAdobeIms`)的模块。

有关启用集成的更多信息，请参阅[配置Commerce与Adobe IMS的管理员集成](./adobe-ims-config.md)。

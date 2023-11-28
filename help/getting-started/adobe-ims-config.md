---
title: 使用ID配置Commerce管理集成
description: 请按照以下可选过程操作，以将Adobe Commerce管理员用户帐户的登录与Adobe ID集成。
exl-id: 518b7c21-e6b3-47d7-81a5-c34fbe0f197c
feature: Identity Management
source-git-commit: 20b2560ce2b8071c740907292544519f8b1c3ddf
workflow-type: tm+mt
source-wordcount: '758'
ht-degree: 1%

---

# 配置Commerce管理员与Adobe ID的集成

{{ee-feature}}

此集成支持拥有管理员用户的Commerce商家，这些管理员用户具有Adobe ID并想要简化对Adobe Commerce和Adobe业务产品的登录。 它是可选的，并且会按实例启用。 启用后，只有管理员用户工作流受影响。 

>[!IMPORTANT]
>
>管理员用户应在启用此集成之前保存其Commerce管理员凭据（用户名和密码）和2FA凭据。 如果禁用IMS集成，则需要这些凭据。

## 先决条件

* Adobe Commerce 2.4.5或更高版本
* Adobe.com帐户，有权访问 [Adobe Admin Console](https://adminconsole.adobe.com/).

配置此集成的管理员在启用模块期间需要以下凭据：

* 组织ID(获取自 [Adobe Admin Console](https://adminconsole.adobe.com/))，长度必须至少为24个字符。 经过身份验证的用户必须属于此IMS组织。 有关查找组织ID的信息，请参阅 [Experience Cloud中的组织](https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html).
* 应在Adobe Admin Console中的组织级别强制执行2FA以启用该模块。 Check [身份验证设置](https://helpx.adobe.com/enterprise/using/authentication-settings.html#two-step-verification).
* 客户端ID
* 客户端密码
* 从检索API密钥后，可以使用客户端ID和客户端密钥 [Adobe Developer控制台](https://developer.adobe.com/developer-console/docs/guides/credentials/).

Commerce管理员用户必须创建具有Adobe ID的帐户才能登录。

## 常规步骤

* 从获取Adobe组织ID [Adobe Admin Console](https://adminconsole.adobe.com/)
* 从生成新项目、IMS API密钥和密码 [Adobe Developer控制台](https://developer.adobe.com/)
* 启用 `AdminAdobeIms` 模块
* 在Adobe Admin Console中配置Adobe Commerce用户。

要成功集成，需要所有Adobe Commerce用户具有具有相同名称和主电子邮件地址的管理员用户帐户。 如果不存在匹配的管理员用户帐户，则必须手动分配具有所需权限（通常分配了管理员角色）的用户 [创建管理员用户帐户](../systems/permissions-users-all.md#create-a-user) 和电子邮件相同。

## 配置集成

具有系统访问权限的管理员或开发人员完成以下步骤后， _[!UICONTROL Sign into Adobe Commerce with Adobe IMS]_按钮将显示在所有管理员用户的Commerce管理员登录页面中。

### 步骤1：获取Adobe组织ID

要启用此功能，需要至少拥有一个IMS组织的成员资格。 如果您拥有Adobe ID，则默认情况下您至少属于一个Adobe组织。 登录到 [Adobe Admin Console](https://adminconsole.adobe.com/) 以检索您的组织ID。

### 步骤2：生成新项目、IMS API密钥和密码

要为组织创建项目，组织的Adobe管理员帐户必须具有系统管理员或开发人员角色。 请参阅 [开发人员控制台指南](https://developer.adobe.com/developer-console/docs/guides/projects/).

1. 登录 [Adobe Developer控制台](https://developer.adobe.com/).
1. 转到 **[!UICONTROL Projects]** 选项卡(adobe.io/projects)，然后单击 **[!UICONTROL Create a new project]**.
1. 单击 **[!UICONTROL Add API]** 在新创建的项目页面上。
1. 选择 **[!UICONTROL Adobe Services]** > **[!UICONTROL Adobe Commerce with Adobe ID]**.
1. 选择 **[!UICONTROL Oauth 2.0 Web]**.
1. 指定 **[!UICONTROL Redirect URI]**： `https://<hostname>/`
1. 指定 **[!UICONTROL Redirect URI pattern]**： `https://<hostname>/.*`

   通过在主机名中的任何点之前添加以下内容来转义这些点 `\\`. 在URL末尾添加通配符可支持Adobe Commerce管理员密钥。

1. 单击 **[!UICONTROL Save configured API]**.
1. 复制 [!UICONTROL Client ID] 和 [!UICONTROL Client Secret] 键创建项目。

### 步骤3：启用AdminAdobeIms模块

此 `AdminAdobeIms` 模块负责Adobe Commerce/Adobe IMS集成。 在设置新项目并复制组织ID、客户端ID和客户端密钥后，您可以启用 `AdminAdobeIms` 模块。

输入 `bin/magento admin:adobe-ims:enable`. 系统将提示您输入以下参数。 使用项目创建期间生成的值。

* 组织ID
* 客户端ID
* 客户端密码
* 2FA已启用

Adobe Commerce会显示一条消息，指示启用是成功还是失败。

成功启用此功能后，您可以将其他Adobe Commerce用户帐户迁移到Adobe IMS帐户。 Adobe Commerce用户必须属于配置的Adobe组织，才能使用Adobe ID登录。

### 步骤4：在Adobe Admin Console中配置Adobe Commerce用户

成功启用此功能后，您可以将其他Adobe Commerce用户帐户迁移到Adobe IMS帐户。 Adobe Commerce用户必须至少属于一个Adobe组织，才能使用Adobe ID登录。

1. 在 [Admin Console](https://helpx.adobe.com/cn/enterprise/using/admin-console.html)，导航到 **[!UICONTROL Users]**  > **[!UICONTROL Users]**.

1. 单击 **[!UICONTROL Add User]**.

1. 输入用户的电子邮件地址。

   如果适用，将自动填充推荐的ID类型。 您可以根据贵组织的购买计划，将此设置更改为列表中的产品ID之一。

   一次最多可以添加十个用户。 要添加更多内容，请在保存更改后重复上述步骤。

1. 单击 **[!UICONTROL Save]**.

用户即添加并显示在 [!UICONTROL Users] 列表。

---
title: 禁用Commerce管理员与Adobe ID的集成
description: 请按照以下可选过程禁用与Adobe IMS的Adobe Commerce管理集成。
exl-id: 0cd02b23-873e-4e65-ae1f-dbe4f7d0a476
feature: Identity Management
source-git-commit: f84667a7bbc93504499279d77967796bcd11791c
workflow-type: tm+mt
source-wordcount: '313'
ht-degree: 0%

---

# 禁用Commerce管理员与Adobe ID的集成

{{ee-feature}}

已将其商务实例与Adobe IMS身份验证工作流集成的商家可能需要禁用此可选集成。

在禁用IMS集成后，Commerce部署还原为默认的Commerce身份验证工作流和密码策略。 如果启用或禁用此集成，则只有管理员用户工作流受影响。

请参阅 [您的管理员帐户](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/admin-signin.html) 有关Commerce管理员登录的概述。

## 步骤1：禁用集成

无法从管理员中禁用此集成。 要禁用Adobe IMS与Commerce的集成并使Commerce身份验证恢复到其默认状态，您必须从命令行界面禁用集成。

要禁用集成，请执行以下操作：

```bash
bin/magento admin:adobe-ims:disable
```

Adobe Commerce在成功时显示以下消息：

```terminal
Admin Adobe IMS integration is disabled.
```

## 步骤2：创建或检索您的Commerce密码

禁用集成后，管理员用户必须使用Commerce密码登录到管理员。

* 记住先前存在的Commerce密码的Commerce管理员用户（即在IMS集成之前创建的Commerce密码）可以使用该密码登录到管理员。

* 不具有预先存在的Commerce密码或忘记密码的Commerce管理员用户必须创建新密码。 要创建新密码，管理员用户可以使用 [!UICONTROL Forgot your password?] 用于创建新密码的Commerce登录页面上的功能。 请参阅 [重置客户密码](https://experienceleague.adobe.com/docs/commerce-admin/customers/customer-accounts/configure/password-reset.html). Commerce不接受空密码字段。

## 禁用集成后

禁用IMS集成后，默认商务身份验证工作流恢复，并再次提示管理员用户输入密码。

禁用IMS集成将删除启用集成时输入的凭据(`Organization ID`， `Client ID`、和 `Client Secret` 值)。

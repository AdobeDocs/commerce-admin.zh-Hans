---
title: 管理员是什么？
description: 了解 [!DNL Commerce] 管理员，商家在这里设置产品和促销活动、管理订单以及执行其他管理任务。
exl-id: 065cf14f-80e7-4695-8922-c761a2191d72
source-git-commit: b657db7e486fec591d5a6239d554376f00707e8c
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 0%

---

# 管理员是什么？

您的商店 _管理员_ 是受密码保护的后台，您可以在此以商户身份设置产品和促销活动、管理订单以及执行其他管理任务。 所有基本配置任务和存储管理操作均从 _管理员_.

为了增加安全性， _管理员_ 登录受保护 [双重身份验证](../systems/security-two-factor-authentication.md)，并且可以配置为需要 [验证码](../systems/security-captcha.md). 要了解更多信息，请访问 [配置管理员安全](../systems/security-admin.md).

![管理员侧边栏和功能板](./assets/admin-dashboard.png){width="700" zoomable="yes"}

您的初始 [登录](admin-signin.md) 凭据是在Adobe Commerce或Magento Open Source安装期间设置的。 如果您忘记了密码，则会将临时密码发送到与帐户关联的电子邮件地址。 为了提高安全性，请将存储配置为需要区分大小写的用户名和强密码。

除了默认的Admin用户帐户外，您的企业还可以创建最多 [其他帐户](../systems/permissions-users-all.md) 您需要用来管理商店和支持客户帐户的帐户。 每个帐户都可以与特定的 [角色](../systems/permissions-user-roles.md) 和访问级别，基于业务 _需要知道_. 与每个管理员用户帐户关联的电子邮件地址必须是唯一的。

{{ims-admin-note}}

## 使用情况数据收集

首次登录到 _管理员_，您需要授予Adobe收集所有管理员用户使用情况数据的权限。 通过允许收集管理员使用情况数据，您可以帮助Adobe改善使用Adobe Commerce管理员以及相关产品和服务的体验。

![允许收集管理员使用情况数据](./assets/admin-usage-data.png){width="600"}

在使用数据中未标识个别用户。 您的数据收集设置可以随时更改，从 [管理员使用情况](../configuration-reference/advanced/admin.md#admin-usage) 配置。

对于Adobe Commerce，允许数据收集还支持 _产品内指南_，旨在为用户提供交互式内容 _管理员_. 它提供了帮助、工具提示、演练指南、入门信息、功能公告等。

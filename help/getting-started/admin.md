---
title: 管理员是什么？
description: 了解 [!DNL Commerce] 管理员，商家可以在这个位置设置产品和促销活动、管理订单以及执行其他管理任务。
exl-id: 065cf14f-80e7-4695-8922-c761a2191d72
TQID: https://experienceleague.adobe.com/A0DuYohA907-EHXQ6fyy2Sz83Y6cFZ7PDY5SmtBa14Y
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: cc72dcf1-72e1-48cc-b434-e7c27d62d67c
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: d3cdead0-685a-4489-9250-4bb709942f66
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 324
ht-degree: 0%

---

# 管理员是什么？

您的商店&#x200B;_管理员_&#x200B;是受密码保护的后台，您作为商家可以在这里设置产品和促销活动、管理订单以及执行其他管理任务。 从&#x200B;_管理员_&#x200B;执行所有基本配置任务和存储管理操作。

为了提高安全性，_管理员_&#x200B;登录受[双重身份验证](../systems/security-two-factor-authentication.md)保护，并且可以配置为需要[验证码](../systems/security-captcha.md)。 若要了解详细信息，请转到[配置管理员安全](../systems/security-admin.md)。

![管理员侧边栏和仪表板](./assets/admin-dashboard.png){width="700" zoomable="yes"}

您的[初始登录](admin-signin.md)凭据是在Adobe Commerce或Magento Open Source安装期间设置的。 如果您忘记了密码，则会将临时密码发送到与帐户关联的电子邮件地址。 为了提高安全性，请将存储配置为需要区分大小写的用户名和强密码。

除了默认的Admin用户帐户外，您的企业还可以创建管理商店和支持客户帐户所需的最多[个其他帐户](../systems/permissions-users-all.md)。 每个帐户都可以与特定的[角色](../systems/permissions-user-roles.md)和访问级别相关联，具体取决于业务&#x200B;_需要知道_。 与每个管理员用户帐户关联的电子邮件地址必须是唯一的。

{{ims-admin-note}}

## 使用情况数据收集

首次登录&#x200B;_管理员_&#x200B;时，系统会要求您授予Adobe权限，以收集所有管理员用户的使用情况数据。 通过允许收集管理员使用情况数据，您可以帮助Adobe改善使用Adobe Commerce管理员以及相关产品和服务的体验。

![允许管理员使用数据收集](./assets/admin-usage-data.png){width="600"}

在使用数据中未标识个别用户。 您的数据收集设置可以随时从[管理员使用情况](../configuration-reference/advanced/admin.md#admin-usage)配置中进行更改。

对于Adobe Commerce，允许数据收集还支持&#x200B;_产品内指南_，该指南旨在将交互式内容带给&#x200B;_管理员_。 它提供了帮助、工具提示、演练指南、入门信息、功能公告等。

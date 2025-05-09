---
title: 配置日志轮换
description: 为Commerce的AEM Assets集成配置日志轮换。
feature: CMS, Media, Integration
exl-id: f735d086-048c-4555-bc58-ac6736c281b0
source-git-commit: c71fd243d809e2b86c5c8e781d527892965838ae
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 0%

---

# 配置Experience Manager Assets

适用于Commerce的AEM Assets集成在您的Commerce实例中提供以下日志文件：

- `/var/log/aem-assets-integration.log`
- `/var/log/aem-assets-integration-errors.log`

请要求系统管理员检查这些日志的日志文件轮换计划，以防止它们变得太大。 在某些环境中，日志文件会自动轮换，但在其他环境中，您必须手动设置日志轮换。 有关详细信息，请参阅以下主题：

- 对于Adobe Commerce内部部署，请要求系统管理员设置[日志轮换](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/next-steps/configuration.html#server-settings)。
- 有关云基础架构项目上的Adobe Commerce，请参阅[查看和管理日志](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/test/log-locations.html)。

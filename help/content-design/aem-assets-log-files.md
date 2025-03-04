---
title: 配置日志轮换
description: 为Commerce的AEM Assets集成配置日志轮换。
feature: CMS, Media, Integration
source-git-commit: 9e1f80d24eed078b5b28ae2d102c3f3df457081d
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 0%

---

# 配置Experience Manager Assets

适用于Commerce的AEM Assets集成提供了以下日志文件：

- `/var/log/aem-assets-integration.log`
- `/var/log/aem-assets-integration-errors.log`

请要求系统管理员检查这些日志的日志文件轮换计划，以防止它们变得太大。 在某些环境中，日志文件会自动轮换，但在其他环境中，您必须手动设置日志轮换。 有关详细信息，请参阅以下主题：

- 对于Adobe Commerce内部部署，请要求系统管理员设置[日志轮换](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/next-steps/configuration.html#server-settings)。
- 有关云基础架构项目上的Adobe Commerce，请参阅[查看和管理日志](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/test/log-locations.html)。



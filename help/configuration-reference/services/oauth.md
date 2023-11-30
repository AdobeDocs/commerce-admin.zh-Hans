---
title: ’[!UICONTROL Services] &gt； [!UICONTROL OAuth]’
description: 查看 [!UICONTROL Services] &gt； [!UICONTROL OAuth] 商务管理员页面。
exl-id: 984793e0-6ac9-443b-b234-e0cea717dada
feature: Configuration, Security
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 1%

---

# [!UICONTROL Services] > [!UICONTROL OAuth]

{{config}}

## [!UICONTROL Access Token Expiration]

![访问令牌过期](./assets/oauth-token-expire.png)<!-- zoom -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Customer Token Lifetime (hours]) | 全局 | 确定客户API令牌过期前的小时数。 如果字段为空，则客户令牌永不过期。 默认值： `1` |
| [!UICONTROL Admin Token Lifetime (hours)] | 全局 | 确定管理员API令牌过期前的小时数。 如果字段为空，则管理令牌永不过期。 默认值： `4` |

{style="table-layout:auto"}

>[!NOTE]
>
>持有者客户和管理员API令牌生命周期和加密算法由控制 [JWT身份验证](magento-web-api.md#jwt-authentication) 配置设置。

## [!UICONTROL Cleanup Settings]

![清理设置](./assets/oauth-cleanup.png)<!-- zoom -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Cleanup Probability] | 全局 | 指定启动清理之前的OAuth请求数。 请勿输入 `0` 以禁用清理。 |
| [!UICONTROL Enable WSDL Cache] | 全局 | 确定条目在清理之前的保留时间（以分钟为单位）。 |

{style="table-layout:auto"}

## [!UICONTROL Consumer Settings]

![使用者设置](./assets/oauth-consumer-settings.png)<!-- zoom -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL OAuth consumer credentials HTTP Post timeout] | 全局 | 指定客户发布凭据时系统超时所需的秒数。 |
| [!UICONTROL OAuth consumer credentials HTTP Post maxredirects] | 全局 | 指定与发布使用者凭据相关的最大重定向数。 |
| [!UICONTROL Expiration Period] | 全局 | 确定OAuth令牌交换开始后，未使用的密钥/密钥过期前的秒数。 |

{style="table-layout:auto"}

## [!UICONTROL Authentication Locks]

![身份验证锁定](./assets/oauth-locks.png)<!-- zoom -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Maximum Login Failures to Lock Out Account] | 全局 | 指定锁定帐户的最大身份验证失败数。 |
| [!UICONTROL Lockout Time (seconds)] | 全局 | 指定帐户解锁之前经过的时间段（以秒为单位）。 |

{style="table-layout:auto"}

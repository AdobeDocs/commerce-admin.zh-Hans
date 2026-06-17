---
title: '[!UICONTROL Services] > [!UICONTROL Magento Web API]'
description: 查看Commerce管理员的[!UICONTROL Services] &gt； [!UICONTROL Magento Web API]页面上的配置设置。
exl-id: 9e9857e7-6f5c-4273-9e82-c861e627827a
feature: Configuration, Integration
TQID: https://experienceleague.adobe.com/62cy3cPVxGeI-W1LElSg1TEBEb0cZN30vGZQ74UNhm8
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: ba9e5be9-7de1-4f71-a5d2-baead0e425eeid: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: d095671a-1355-40aa-8b5f-06c33c68080bid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 325
ht-degree: 1%

---

# [!UICONTROL Services] > [!UICONTROL Magento Web API]

{{config}}

<!-- [X-ref](../systems/integrations.md) -->

## [!UICONTROL SOAP Settings]

![SOAP设置](./assets/web-api-soap-settings.png)<!-- zoom -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Default Response Charset] | 商店视图 | 确定默认字符集。 如果为空，则使用UTF-8。 |

{style="table-layout:auto"}

## [!UICONTROL GraphQl Input Limits]

![GraphQl输入限制](./assets/web-api-graphql-input-limits.png)<!-- zoom -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Enable Input Limits] | 商店视图 | 确定是否为GraphQL调用启用输入限制。 默认值： `No`。 |
| [!UICONTROL Maximum Page Size] | 商店视图 | 设置GraphQL响应中分页搜索结果允许的最大项目数。 当&#x200B;_启用输入限制_ = `No`时，此选项不可用。 |

{style="table-layout:auto"}

## [!UICONTROL Web Api Input Limits]

![Web Api输入限制](./assets/web-api-input-limits.png)<!-- zoom -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Enable Input Limits] | 商店视图 | 确定是否为Web API调用启用输入限制。 默认值： `No`。 |
| 输入列表限制 | 商店视图 | 在Web API请求中设置实体数组属性中允许的最大项数。 当&#x200B;_启用输入限制_ = `No`时，此选项不可用。 |
| [!UICONTROL Maximum Page Size] | 商店视图 | 设置Web API响应的分页搜索结果中允许的最大项目数。 当&#x200B;_启用输入限制_ = `No`时，此选项不可用。 |
| [!UICONTROL Default Page Size] | 商店视图 | 在Web API响应中设置分页搜索结果中的默认项目数。 |

{style="table-layout:auto"}

## [!UICONTROL Web API Security]

![Web API安全性](./assets/web-api-security.png)<!-- zoom -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Allow Anonymous Guest Access] | 全局 | 确定访客是否可以从SOAP和REST API匿名访问CMS、目录和存储资源。 默认情况下，不允许匿名访客访问。 选项： `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL JWT Authentication]

![JWT身份验证](./assets/web-api-jwt-authentication.png)<!-- zoom -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Algorithm to sign/encrypt JWTs used for authentication] | 全局 | 指定用于JWT （JSON Web令牌）加密的JWS或JWE算法的类型 |
| [!UICONTROL Content encryption algorithm for JWEs] | 全局 | 指定在选择了JWE算法时用于JWT加密的内容加密算法类型。 对于JWS算法，此选项被忽略。 |
| [!UICONTROL Customer JWT Expires In] | 全局 | 设置客户JWT持有者令牌过期之前的时长（以分钟为单位）。 如果此字段为空或其为负值，则客户JWT持有者令牌将在30分钟后过期。 默认值： `60` |
| [!UICONTROL Admin User JWT Expires In] | 全局 | 设置管理员JWT持有者令牌过期之前的时长（以分钟为单位）。 如果此字段为空或其为负值，则管理员JWT持有者令牌将在30分钟后过期。 默认值： `60` |

{style="table-layout:auto"}

---
title: ’[!UICONTROL Services] &gt； [!UICONTROL Commerce Services Connector]’
description: 查看 [!UICONTROL Services] &gt； [!UICONTROL Commerce Services Connector] 商务管理员页面。
exl-id: 3570e846-c8ab-4a36-b020-1b536bbd377d
feature: Configuration, Saas
source-git-commit: 76bd1b1af9b55d69bd98209d70fb5518f190a3e1
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 1%

---

# [!UICONTROL Services] > [!UICONTROL Commerce Services Connector]

要了解如何将您的应用商店连接到Adobe Commerce服务，请参阅 [Commerce服务](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/integration-services/saas.html).

{{config}}

## [!UICONTROL Sandbox API Keys]

![沙盒API密钥](./assets/sandbox-key-saas-configuration.png)<!-- zoom -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Sandbox public API key] | 全局 | 标识作者及其权利的API密钥（如果有）。 |
| [!UICONTROL Sandbox private API key] | 全局 | 与API密钥关联的私钥。 |

{：style=&quot;table-layout：auto&quot;}

## [!UICONTROL Production Keys]

![生产API密钥](./assets/prod-key-saas-configuration.png)<!-- zoom -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Production public API key] | 全局 | 标识作者及其权利的API密钥（如果有）。 |
| [!UICONTROL Production private API key] | 全局 | 与API密钥关联的私钥。 |

{：style=&quot;table-layout：auto&quot;}

## [!UICONTROL SaaS Identifier]

![SaaS标识符](./assets/saas-identifier.png)<!-- zoom -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Project] | 全局 | 对所有SaaS数据空间进行分组的SaaS项目的名称。 A _创建项目_ 如果没有SaaS项目，则会显示按钮。 |
| [!UICONTROL Data Space] | 全局 | 列出指定SaaS项目中的SaaS数据空间。 SaaS数据空间的数量取决于 [商业许可证](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/integration-services/saas.html)：<br />Adobe Commerce — 一个生产数据空间；两个测试数据空间；<br />Magento Open Source — 一个生产数据空间；无测试数据空间 |

{：style=&quot;table-layout：auto&quot;}

## [!UICONTROL IMS Organization]

![IMS组织](./assets/ims-organization.png)<!-- zoom -->

| 字段 | 描述 |
|--- |--- |
| [!UICONTROL Sign in using Adobe ID] | 您的Adobe ID通常是您在启动会员资格或购买Adobe应用程序或服务时首先使用的电子邮件地址。 您的Adobe ID是访问Adobe帐户所需的密钥。 |

{：style=&quot;table-layout：auto&quot;}

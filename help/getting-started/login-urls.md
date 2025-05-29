---
title: 登录凭据和URL
description: 了解用于访问管理员和店面的Commerce URL和帐户凭据。
exl-id: fa16b7e9-e05f-4eb8-bc32-596946c57e1c
feature: System
role: Admin, Leader
source-git-commit: 77e7eb00e9f8d5af6361059c287707993180c4c4
workflow-type: tm+mt
source-wordcount: '351'
ht-degree: 0%

---

# 登录凭据和URL

在继续设置和配置之前，请确保您拥有访问存储管理员和Commerce帐户所需的信息。

## 店面URL

[storefront](storefront.md)的地址通常是分配给您IP地址的域。 某些存储安装在根目录或最顶部目录中。 其他则安装在根目录下的目录中。 存储可能驻留在与主域关联的子域中。 您的商店的URL可能类似于以下内容之一：

- `http://mydomain.com`
- `http://www.mydomain.com/mystore`
- `http://xxx.xxx.xxx.xxx`秒

如果您还没有域，则商店URL包含一系列四个数字，每个数字以&#x200B;_点状四_&#x200B;表示法用句点分隔。

## 管理员URL

您的商店[Admin](admin.md)的地址是在安装期间设置的。 默认地址与您的商店相同，但结尾是`/admin`。 尽管本指南中的示例使用默认目录，但最佳实践是从存储特有的位置运行管理员。

- `http://mydomain.com/admin`
- `http://www.mydomain.com/admin`

## [!DNL Commerce]帐户

您的[Commerce帐户](commerce-account-create.md)可以访问有关您的产品和服务、帐户设置、帐单历史记录以及支持资源的信息。 要访问您的帐户，请转到Commerce主网站，然后单击右上角的&#x200B;**[!UICONTROL My Account]**。

## 客户帐户

当您在商店中学习时，请确保设置一个测试[客户帐户](../customers/account-dashboard.md)，这样您就可以从客户的角度体验商店和结账过程。

## 示例数据

仅[!BADGE PaaS]{type=Informative url="https://experienceleague.adobe.com/zh-hans/docs/commerce/user-guides/product-solutions" tooltip="仅适用于云项目(Adobe管理的PaaS基础架构)和内部部署项目上的Adobe Commerce 。"}

Adobe提供了一个示例数据集，其中包括一个包含250多种产品（其中大约200种是可配置产品）、类别、促销价格规则、CMS页面、横幅等的示例商店。 示例数据使用店面上的&#x200B;_Luma_&#x200B;主题。 [安装此示例数据](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/next-steps/sample-data/overview.html?lang=zh-Hans)是可选的，但有助于测试和开发电子商务业务的自定义项。

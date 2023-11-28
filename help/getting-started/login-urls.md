---
title: 登录凭据和URL
description: 了解用于访问管理员和店面的Commerce URL和帐户凭据。
exl-id: fa16b7e9-e05f-4eb8-bc32-596946c57e1c
feature: System
role: Admin, Leader
source-git-commit: 3ff5807fd0a3ebf2e9d4f9c085852dd7777a1103
workflow-type: tm+mt
source-wordcount: '339'
ht-degree: 0%

---

# 登录凭据和URL

在继续设置和配置之前，请确保您拥有访问商店管理员和商务帐户所需的信息。

## 店面URL

您的地址 [店面](storefront.md) 通常是分配给IP地址的域。 某些存储安装在根目录或最顶部目录中。 其他则安装在根目录下的目录中。 存储可能驻留在与主域关联的子域中。 您的商店的URL可能类似于以下内容之一：

- `http://mydomain.com`
- `http://www.mydomain.com/mystore`
- `http://xxx.xxx.xxx.xxx`s

如果您还没有域，则商店URL将包含一系列四个数字，每个数字之间用句点分隔 _点状四边形_ 表示法。

## 管理员URL

您的商店地址 [管理员](admin.md) 会在安装期间进行设置。 默认地址与您的商店相同，但使用 `/admin` 在结尾处。 尽管本指南中的示例使用默认目录，但最佳实践是从存储特有的位置运行管理员。

- `http://mydomain.com/admin`
- `http://www.mydomain.com/admin`

## [!DNL Commerce] 帐户

您的 [Commerce帐户](commerce-account-create.md) 允许访问有关您的产品和服务、帐户设置、账单历史记录和支持资源的信息。 要访问您的帐户，请转到主要Commerce网站并单击 **[!UICONTROL My Account]** 在右上角。

## 客户帐户

当您在商店中学习时，请确保设置测试 [客户帐户](../customers/account-dashboard.md)，以便从客户的角度体验存储和结账过程。

## 示例数据

Adobe提供了一个示例数据集，其中包括一个包含250多种产品（其中约200种为可配置产品）、类别、促销价格规则、CMS页面、横幅等的示例商店。 示例数据使用 _Luma_ 店面上的布景主题。 [安装此示例数据](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/next-steps/sample-data/overview.html) 是可选的，但有助于测试和开发电子商务业务的自定义项。

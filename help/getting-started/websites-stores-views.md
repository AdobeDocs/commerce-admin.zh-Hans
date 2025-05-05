---
title: 站点、存储和查看范围
description: 了解可用于为客户提供购物体验的网站、商店和商店视图的层次结构。
exl-id: 80fc1b73-c869-4f1c-b1a1-d61823b91d83
feature: System, Site Management
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '672'
ht-degree: 0%

---

# 站点、存储和查看范围

每个Adobe Commerce和Magento Open Source安装都有一个[层级](../stores-purchase/stores.md)网站、商店和商店视图。 术语&#x200B;_scope_&#x200B;确定数据库实体（如产品、属性或类别）内容元素或配置设置在层次结构中应用的位置。 网站、商店和商店视图具有一对多的父/子关系。 单个安装可以具有多个网站，每个网站可以具有多个商店和商店视图。

>[!NOTE]
>
>若要了解更多信息，请参阅[!DNL Commerce]开发人员文档中的[多个网站或商店](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/multi-sites/ms-overview.html?lang=zh-Hans)。

## 网站

安装从单个[网站](../stores-purchase/stores.md#add-websites)开始，默认情况下称为&#x200B;_主网站_。 您还可以为单个安装设置多个网站，每个网站都有自己的IP地址和域。

## 商店

单个网站可以有多个[商店](../stores-purchase/stores.md#add-stores)，每个商店都有自己的主菜单。 商店共享产品目录，但可以有不同的产品和设计选择。 同一网站下的所有商店共享管理员和结账。

## 商店视图

根据特定的&#x200B;_[视图](../stores-purchase/store-views.md)_&#x200B;呈现客户可用的每个商店。 最初，商店有一个默认视图。 可添加其他商店视图以支持不同语言或用于其他目的。 客户可以使用标头中的语言选择器来更改商店视图。

在使用网站、商店和商店视图时，请牢记以下几点：

- Commerce实例具有级联模型：全局→网站→商店→览。
- 每个网站至少有一个默认商店和商店视图。
- 每个商店视图可以具有不同的基本URL。
- 网站的主要功能是进行顶级功能配置。
- 存储的主要功能是根类别配置。
- 商店视图的主要功能是翻译信息和货币符号配置。

## 范围设置

如果您的Adobe Commerce或Magento Open Source安装具有网站、商店或视图的层次结构，则可以设置上下文或配置设置的&#x200B;_范围_。 还可以为许多数据库实体的上下文分配特定范围，以确定如何在存储层次结构中使用它。 若要了解详细信息，请参阅[产品范围](../catalog/introduction.md#product-scope)和[价格范围](../catalog/catalog-price-scope.md)。

某些配置设置（如邮政编码）具有全局范围，因为在整个系统中使用相同的值。 [网站](../stores-purchase/stores.md#add-websites)范围适用于层次结构中低于该级别的所有商店，包括所有商店及其视图。 每个存储视图[存储视图](../stores-purchase/store-views.md)范围的任何项都可以进行不同的设置，通常用于支持多种语言。 要覆盖配置设置的默认值，请参阅[设置作用域](../configuration-reference/scope-change.md#set-the-scope)。

除非存储在[单存储模式](#single-store-mode)下运行，否则每个配置设置的范围都显示在字段标签下方的小文本中。 如果您的安装包含多个网站、商店或视图，请选择应用设置的[商店视图](../stores-purchase/store-views.md)，然后再进行任何更改。

![网站、商店和商店视图的层次结构](./assets/scope-multisite.svg){width="550"}

| 范围 | 描述 |
|--- |--- |
| [!UICONTROL Global] | 在整个安装过程中可用的系统范围设置和资源。 |
| [!UICONTROL Website] | 仅限于当前网站的设置和资源。 每个网站都有一个默认商店。 |
| [!UICONTROL Store] | 仅限于当前商店的设置和资源。 每个存储都有一个默认的根类别（主菜单）和默认的存储视图。 |
| [!UICONTROL Store View] | 设置为和限制为当前存储视图的资源。 |

{style="table-layout:auto"}

## 单存储模式

如果Commerce安装只有单个商店和商店视图，则可以通过关闭所有商店视图选项和范围指示器来简化显示。 如果稍后[添加更多商店视图](../stores-purchase/store-views.md)，将覆盖单商店模式。

![范围 — 单个视图](./assets/scope-single-view.svg){width="550"}

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在&#x200B;**[!UICONTROL General]**&#x200B;下，向下滚动到页面底部并展开&#x200B;**[!UICONTROL Single-Store Mode]**&#x200B;部分。

1. 将&#x200B;**[!UICONTROL Enable Single-Store Mode]**&#x200B;设置为`Yes`。

   ![常规配置 — 启用单存储模式](./assets/general-single-store-mode.png){width="400"}

1. 单击&#x200B;**[!UICONTROL Save Config]**。

1. 当提示刷新缓存时，执行以下操作：

   - 单击页面顶部系统消息中的&#x200B;**[!UICONTROL Cache Management]**&#x200B;链接。

     ![系统消息 — 缓存管理](../catalog/assets/msg-cache-management.png){width="600" zoomable="yes"}

   - 选中&#x200B;**[!UICONTROL Page Cache]**&#x200B;复选框。

   - 在&#x200B;**[!UICONTROL Actions]**&#x200B;设置为`Refresh`的情况下，单击&#x200B;**[!UICONTROL Submit]**

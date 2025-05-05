---
title: '[!UICONTROL Customers] &amp；gt； [!UICONTROL Gift Registry]'
description: 查看Commerce管理员的[!UICONTROL Customers] &amp；gt； [!UICONTROL Gift Registry]页面上的配置设置。
exl-id: c5153c4e-897a-41d2-bde1-8483855d1a37
feature: Configuration, Gift
source-git-commit: 5a4417373f6dc720e8e14f883c27348a475ec255
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 1%

---

# [!UICONTROL Customers] > [!UICONTROL Gift Registry]

{{ee-feature}}

{{config}}

有关使用这些设置为商店客户启用礼品注册的详细信息，请参阅[配置礼品注册](../../merchandising-promotions/gift-registry-configure.md)。 有关在店面中包括礼品注册搜索的信息，请参阅[添加礼品注册搜索](../../merchandising-promotions/gift-registry-search.md)。

## [!UICONTROL General Options]

![常规选项](./assets/gift-registry-general-options.png)<!-- zoom -->

<!-- [General Options](https://experienceleague.adobe.com/zh-hans/docs/commerce-admin/marketing/merchandising/gift-registry/gift-registry-configure) -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Enable Gift Registry] | 商店视图 | 确定礼品登记是否可用。 选项： <br/>**`Yes`**— 为所选商店视图启用礼品登记簿。 “礼品注册表”标签将显示在已注册客户的帐户控制面板中。<br/>**`No`** — 礼品注册表不可用于商店视图。 |
| [!UICONTROL Maximum Registrants] | 商店视图 | 设置客户可添加到礼品注册表的人员数量。 客户与每位注册者共享礼品注册表。 在店面中，_添加注册者_&#x200B;按钮可供客户使用，直到达到最大数量为止。 |

{style="table-layout:auto"}

## [!UICONTROL Owner Notification]

![所有者通知](./assets/gift-registry-owner-notification.png)<!-- zoom -->

<!-- [Owner Notification](https://experienceleague.adobe.com/zh-hans/docs/commerce-admin/marketing/merchandising/gift-registry/gift-registry-configure) -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Email Template] | 商店视图 | 确定在创建礼品注册时发送的所有者通知电子邮件所使用的模板。 默认模板：礼品注册所有者通知 |
| [!UICONTROL Email Sender] | 商店视图 | 标识显示为礼品注册所有者通知电子邮件发件人的[商店联系人](../../getting-started/store-details.md#store-email-addresses)。 默认值： `General Contact` |

{style="table-layout:auto"}

## 礼品注册共享

![礼品注册共享](./assets/gift-registry-gift-registry-sharing.png)<!-- zoom -->

<!-- Gift Registry Sharing](https://experienceleague.adobe.com/zh-hans/docs/commerce-admin/marketing/merchandising/gift-registry/gift-registry-configure) -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Email Template] | 商店视图 | 确定在创建礼品注册时发送的礼品注册共享电子邮件所使用的模板。 当所有者单击&#x200B;_共享礼品注册表_&#x200B;时，电子邮件将发送给每个收件人。 默认模板： `Gift Registry Sharing` |
| [!UICONTROL Email Sender] | 商店视图 | 标识显示为礼品注册共享电子邮件发件人的[商店联系人](../../getting-started/store-details.md#store-email-addresses)。 默认值： `General Contact` |
| [!UICONTROL Maximum Sent Emails Threshold] | 商店视图 | 一次可以发送的礼品注册共享电子邮件通知消息的最大数量。 |

{style="table-layout:auto"}

## [!UICONTROL Gift Registry Update]

![礼品注册更新](./assets/gift-registry-gift-registry-update.png)<!-- zoom -->

<!-- [Gift Registry Update](https://experienceleague.adobe.com/zh-hans/docs/commerce-admin/marketing/merchandising/gift-registry/gift-registry-configure) -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Email Template] | 商店视图 | 确定在从礼品注册处进行购买时发送给礼品注册所有者的礼品注册更新电子邮件所使用的模板。 更新包括有关项目和采购数量的信息，但不包括下订单人员的姓名。 默认模板： `Gift Registry Update` |
| [!UICONTROL Email Sender] | 商店视图 | 标识显示为礼品注册更新电子邮件发件人的[商店联系人](../../getting-started/store-details.md#store-email-addresses)。 默认值： `General Contact` |

{style="table-layout:auto"}

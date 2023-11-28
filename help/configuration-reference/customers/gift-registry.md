---
title: ’[!UICONTROL Customers] &gt； [!UICONTROL Gift Registry]’
description: 查看 [!UICONTROL Customers] &gt； [!UICONTROL Gift Registry] 商务管理员页面。
exl-id: c5153c4e-897a-41d2-bde1-8483855d1a37
feature: Configuration, Gift
source-git-commit: 76bd1b1af9b55d69bd98209d70fb5518f190a3e1
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 1%

---

# [!UICONTROL Customers] > [!UICONTROL Gift Registry]

{{ee-feature}}

{{config}}

有关使用这些设置为商店客户启用礼品登记的详细信息，请参阅 [配置礼品登记簿](../../merchandising-promotions/gift-registry-configure.md). 有关在店面中包括礼品注册搜索的信息，请参阅 [添加礼品注册搜索](../../merchandising-promotions/gift-registry-search.md).

## [!UICONTROL General Options]

![常规选项](./assets/gift-registry-general-options.png)<!-- zoom -->

<!-- [General Options](https://docs.magento.com/user-guide/marketing/gift-registry-configure.html) -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Enable Gift Registry] | 商店视图 | 确定礼品登记是否可用。 选项： <br/>**`Yes`**— 为选定的商店视图启用礼品登记簿。 “礼品注册表”标签将显示在已注册客户的帐户控制面板中。<br/>**`No`**  — 无法查看礼品注册表。 |
| [!UICONTROL Maximum Registrants] | 商店视图 | 设置客户可添加到礼品注册表的人员数量。 客户与每位注册者共享礼品注册表。 在店面 _添加注册者_ 按钮可供客户使用，直到达到最大数量为止。 |

{style="table-layout:auto"}

## [!UICONTROL Owner Notification]

![所有者通知](./assets/gift-registry-owner-notification.png)<!-- zoom -->

<!-- [Owner Notification](https://docs.magento.com/user-guide/marketing/gift-registry-configure.html) -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Email Template] | 商店视图 | 确定在创建礼品注册时发送的所有者通知电子邮件所使用的模板。 默认模板：礼品注册所有者通知 |
| [!UICONTROL Email Sender] | 商店视图 | 标识 [商店联系人](../../getting-started/store-details.md#store-email-addresses) 显示为“礼品注册所有者通知”电子邮件的发件人。 默认值： `General Contact` |

{style="table-layout:auto"}

## 礼品注册共享

![礼品注册共享](./assets/gift-registry-gift-registry-sharing.png)<!-- zoom -->

<!-- Gift Registry Sharing](https://docs.magento.com/user-guide/marketing/gift-registry-configure.html) -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Email Template] | 商店视图 | 确定在创建礼品注册时发送的礼品注册共享电子邮件所使用的模板。 当所有者单击时 _共享礼品注册_，则会将电子邮件发送给每个收件人。 默认模板： `Gift Registry Sharing` |
| [!UICONTROL Email Sender] | 商店视图 | 标识 [商店联系人](../../getting-started/store-details.md#store-email-addresses) 将显示为礼品注册共享电子邮件的发件人。 默认值： `General Contact` |
| [!UICONTROL Maximum Sent Emails Threshold] | 商店视图 | 一次可以发送的礼品注册共享电子邮件通知消息的最大数量。 |

{style="table-layout:auto"}

## [!UICONTROL Gift Registry Update]

![礼品注册更新](./assets/gift-registry-gift-registry-update.png)<!-- zoom -->

<!-- [Gift Registry Update](https://docs.magento.com/user-guide/marketing/gift-registry-configure.html) -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Email Template] | 商店视图 | 确定在从礼品注册处进行购买时发送给礼品注册所有者的礼品注册更新电子邮件所使用的模板。 更新包括有关项目和采购数量的信息，但不包括下订单人员的姓名。 默认模板： `Gift Registry Update` |
| [!UICONTROL Email Sender] | 商店视图 | 标识 [商店联系人](../../getting-started/store-details.md#store-email-addresses) 显示为“礼品注册更新”电子邮件的发件人。 默认值： `General Contact` |

{style="table-layout:auto"}

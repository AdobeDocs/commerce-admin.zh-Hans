---
title: '[!UICONTROL General] &amp；gt； [!UICONTROL Currency Setup]'
description: 查看Commerce管理员的[!UICONTROL General] &amp；gt； [!UICONTROL Currency Setup]页面上的配置设置。
exl-id: a84be30f-f2eb-4c86-942c-2d49e5cf23af
role: Admin
feature: Currency, Configuration, Data Import/Export
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '351'
ht-degree: 1%

---

# [!UICONTROL General] > [!UICONTROL Currency Setup]

{{config}}

>[!NOTE]
>
>有关这些配置的更多详细信息，请参阅[货币配置](../../stores-purchase/currency-configuration.md)。

## [!UICONTROL Currency Options]

![货币设置>货币选项](./assets/currency-setup-currency-options.png)<!-- zoom -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Base Currency] | 网站 | 用于所有联机付款交易记录的主要币种。 对于多个商店视图，必须在[目录](../catalog/catalog.md)配置中设置价格范围。 |
| [!UICONTROL Default Display Currency] | 商店视图 | 用于显示价格的主要货币。 |
| [!UICONTROL Allowed Currencies] | 商店视图 | 您的商店接受的付款币种。 |

{style="table-layout:auto"}

## [!UICONTROL Fixer.io (legacy)]

>[!IMPORTANT]
>
>从2.4.6版本开始，[[!DNL Fixer.io]](https://fixer.io/)服务已弃用，并替换为[[!DNL Fixer API] (APILayer)](https://apilayer.com/marketplace/fixer-api)服务。 强烈建议您使用APILayer帐户，而不是已弃用的[!DNL Fixer.io]帐户。

![货币设置> Fixer.io](./assets/currency-setup-fixer.png)<!-- zoom -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL API key] | 全局 | 用于通过您的[!DNL fixer.io]帐户访问转换服务的密钥。 有关详细信息，请参阅[[!DNL fixer.io]](https://fixer.io/)。 |
| [!UICONTROL Connection Timeout in Seconds] | 全局 | 确定Fixer.io会话超时之前处于非活动状态的秒数。 默认值： `100` |

{style="table-layout:auto"}

## [!UICONTROL Fixer Api (APILayer)]

![货币设置>修复器Api (APILayer)](./assets/currency-setup-fixer-api.png)<!-- zoom -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL API key] | 全局 | 用于通过您的[!DNL APILayer]帐户访问转换服务的密钥。 有关详细信息，请参阅[[!DNL APILayer]](https://apilayer.com/)。 |
| [!UICONTROL Connection Timeout in Seconds] | 全局 | 确定[!DNL APILayer]会话超时之前处于非活动状态的秒数。 默认值为`100`。 |

{style="table-layout:auto"}

## [!UICONTROL Currency Converter API]

![货币设置>货币转换器API](./assets/currency-setup-converter.png)<!-- zoom -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL API key] | 全局 | 用于访问转换服务的键。 有关详细信息，请参阅[[!DNL Currency Convertor] API](https://free.currencyconverterapi.com/)。 |
| [!UICONTROL Connection Timeout in Seconds] | 全局 | 确定[!DNL Currency Converter]会话超时之前处于非活动状态的秒数。 默认值： `100` |

{style="table-layout:auto"}

## [!UICONTROL Scheduled Import Settings]

![货币设置>计划导入设置](./assets/currency-setup-scheduled-import-settings.png)<!-- zoom -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Enabled] | 商店视图 | 确定是否已为汇率启用计划导入。 选项： `Yes` / `No` |
| [!UICONTROL Service] | 商店视图 | 指定为计划导入提供数据的服务。 默认值为`fixer.io` |
| [!UICONTROL Start Time] | 商店视图 | 按24小时制以小时、分钟和秒表示开始时间。 |
| [!UICONTROL Frequency] | 商店视图 | 确定计划导入发生的频率。 选项： `Daily` / `Weekly` / `Monthly` |
| [!UICONTROL Error Email Recipient] | 商店视图 | 标识通过电子邮件接收有关计划导入错误通知的每个人的电子邮件地址。 对于多个收件人，请使用逗号分隔每个条目。 |
| [!UICONTROL Error Email Sender] | 网站 | 标识显示为错误电子邮件通知发件人的商店联系人。 默认发件人： `General Contact` |
| [!UICONTROL Error Email Template] | 网站 | 指定用作错误电子邮件通知基础的模板。 默认模板： `Currency Update Warnings` |

{style="table-layout:auto"}

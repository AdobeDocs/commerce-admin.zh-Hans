---
title: '[!UICONTROL Sales] &amp；gt； [!UICONTROL Quotes]'
description: 查看Commerce管理员的[!UICONTROL Sales] &amp；gt； [!UICONTROL Quotes]页面上的配置设置。
exl-id: 9382552d-1be5-47f2-b0e3-931e5c6298d4
feature: Configuration, Quotes
source-git-commit: 5a4417373f6dc720e8e14f883c27348a475ec255
workflow-type: tm+mt
source-wordcount: '188'
ht-degree: 1%

---

# [!UICONTROL Sales] > [!UICONTROL Quotes]

{{b2b-feature}}

>[!TIP]
>
>通过安装和启用Adobe Commerce B2B，您可以利用公司的特定功能个性化购买体验。 Adobe Commerce B2B是一个集成式解决方案，同时支持B2B和B2C模型。 有关B2B功能的详细信息，请参阅[Adobe Commerce B2B用户指南](https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html?lang=zh-Hans)。

{{config}}

<!-- [Quotes](https://experienceleague.adobe.com/zh-hans/docs/commerce-admin/b2b/quotes/quotes) -->

## [!UICONTROL General]

![常规](./assets/quotes-general.png)<!-- zoom -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Minimum Amount] | 网站 | 客户提交报价请求之前所需的购物车小计的最小金额（扣除任何折扣后）。 默认值： `0` |
| [!UICONTROL Minimum Amount Message] | 商店视图 | 当客户尝试提交询价但未满足所需最小金额时购物车中显示的消息。 |
| [!UICONTROL Default Expiration Period] | 网站 | 确定[报价](../../b2b/quote-price-negotiation.md)的默认有效期为自提交报价请求之日起的时间段。 选项： `Days` / `Weeks` / `Months` |

{style="table-layout:auto"}

## [!UICONTROL Attached Files]

![附加文件](./assets/quotes-attached-files.png)<!-- zoom -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL File formats for upload] | 全局 | 确定可以附加到引号的文件格式。 支持的默认值： `doc`、`docx`、`xls`、`xlsx`、`pdf`、`txt`、`jpg`、`png`和`jpeg` |
| [!UICONTROL Maximum file size] | 全局 | 确定附加到引号的文件的最大大小。 服务器配置可以覆盖此设置。 |

{style="table-layout:auto"}

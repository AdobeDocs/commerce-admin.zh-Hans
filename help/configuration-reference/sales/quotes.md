---
title: ’[!UICONTROL Sales] &gt； [!UICONTROL Quotes]’
description: 查看 [!UICONTROL Sales] &gt； [!UICONTROL Quotes] 商务管理员页面。
exl-id: 9382552d-1be5-47f2-b0e3-931e5c6298d4
feature: Configuration, Quotes
source-git-commit: 76bd1b1af9b55d69bd98209d70fb5518f190a3e1
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Quotes]

{{b2b-feature}}

>[!TIP]
>
>通过安装和启用Adobe Commerce的B2B，您可以利用公司特定的功能提供个性化的购买体验。 Adobe Commerce的B2B是一个集成式解决方案，同时支持B2B和B2C模型。 有关B2B功能的详细信息，请参见 [《 B2B for Adobe Commerce用户指南》](https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html).

{{config}}

<!-- [Quotes](https://docs.magento.com/user-guide/sales/quotes.html) -->

## [!UICONTROL General]

![常规](./assets/quotes-general.png)<!-- zoom -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Minimum Amount] | 网站 | 客户提交报价请求之前所需的购物车小计的最小金额（扣除任何折扣后）。 默认值： `0` |
| [!UICONTROL Minimum Amount Message] | 商店视图 | 当客户尝试提交询价但未满足所需最小金额时购物车中显示的消息。 |
| [!UICONTROL Default Expiration Period] | 网站 | 确定默认生命周期 [引用](../../b2b/quote-price-negotiation.md) 作为自提交报价请求日期起的时间段。 选项： `Days` / `Weeks` / `Months` |

{：style=&quot;table-layout：auto&quot;}

## [!UICONTROL Attached Files]

![附加文件](./assets/quotes-attached-files.png)<!-- zoom -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL File formats for upload] | 全局 | 确定可以附加到引号的文件格式。 支持的默认值： `doc`， `docx`， `xls`， `xlsx`， `pdf`， `txt`， `jpg`， `png`、和 `jpeg` |
| [!UICONTROL Maximum file size] | 全局 | 确定附加到引号的文件的最大大小。 服务器配置可以覆盖此设置。 |

{：style=&quot;table-layout：auto&quot;}

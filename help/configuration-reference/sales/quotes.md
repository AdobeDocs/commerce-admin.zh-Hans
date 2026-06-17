---
title: '[!UICONTROL Sales] > [!UICONTROL Quotes]'
description: 查看Commerce管理员的[!UICONTROL Sales] &gt； [!UICONTROL Quotes]页面上的配置设置。
exl-id: 9382552d-1be5-47f2-b0e3-931e5c6298d4
feature: Configuration, Quotes
TQID: https://experienceleague.adobe.com/puZjB2YCCyZXT0U6AdDBd-YjxopU637-yxgOaB6hkvM
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 193
ht-degree: 1%

---

# [!UICONTROL Sales] > [!UICONTROL Quotes]

{{b2b-feature}}

>[!TIP]
>
>通过安装和启用Adobe Commerce B2B，您可以利用公司的特定功能个性化购买体验。 Adobe Commerce B2B是一个集成式解决方案，同时支持B2B和B2C模型。 有关B2B功能的详细信息，请参阅[Adobe Commerce B2B用户指南](https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html?lang=zh-Hans)。

{{config}}

<!-- [Quotes](https://experienceleague.adobe.com/en/docs/commerce-admin/b2b/quotes/quotes) -->

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

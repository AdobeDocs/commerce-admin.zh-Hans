---
title: '[!UICONTROL Catalog] > [!UICONTROL Email to a Friend]'
description: 查看Commerce管理员的[!UICONTROL Catalog] &gt； [!UICONTROL Email to a Friend]页面上的配置设置。
exl-id: cd1e3a8d-14ce-47e9-a3bc-c1b1dcbe0d8c
feature: Configuration, Communications
TQID: https://experienceleague.adobe.com/TzkDDALdwE5MMIEuZBpBL4DnOgngN93-YEf4biNwYMI
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 172
ht-degree: 1%

---

# [!UICONTROL Catalog] > [!UICONTROL Email to a Friend]

{{config}}

## [!UICONTROL Email Templates]

![电子邮件模板](./assets/email-to-a-friend-email-templates.png)<!-- zoom -->

<!-- [Email Templates](https://experienceleague.adobe.com/en/docs/commerce-admin/systems/communications/email-templates#configure-email-templates) -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Enabled] | 商店视图 | 激活流程，使客户能够向朋友发送有关您商店中产品的电子邮件。 选项： `Yes` / `No` |
| [!UICONTROL Select Email Template] | 商店视图 | 标识用于由&#x200B;_通过电子邮件发送Friend_&#x200B;函数生成的邮件的电子邮件模板。 默认模板： `Send Product to Friend` |
| [!UICONTROL Allow for Guests] | 商店视图 | 确定发件人是否必须是注册客户才能向朋友发送有关产品的电子邮件。 选项： `Yes` / `No` |
| [!UICONTROL Max Recipients] | 商店视图 | 限制单个电子邮件可在通讯组列表中的人数。 |
| [!UICONTROL Max Products Sent in 1  Hour] | 商店视图 | 限制单个用户在一小时内可以共享的产品数量。 |
| [!UICONTROL Limit Sending By] | 商店视图 | 确定用于识别发件人的方法。 选项包括： <br/>**`IP Address`**- （推荐）通过用于发送产品电子邮件的计算机的IP地址识别发件人。<br/>**`Cookie (unsafe)`** — 通过浏览器Cookie识别发件人。 此方法不安全，因为用户可以删除Cookie以避免限制。 |

{style="table-layout:auto"}

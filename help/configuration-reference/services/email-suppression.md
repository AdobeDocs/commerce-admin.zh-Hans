---
title: '[!UICONTROL Adobe Services] > [!UICONTROL Email Suppression]'
description: 查看Commerce管理员的[!UICONTROL Adobe Services] &gt； [!UICONTROL Email Suppression]页面上的配置设置。
feature: Configuration, Communications
badgeSaas: label="仅限SaaS" type="Positive" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="仅适用于Adobe Commerce as a Cloud Service和Adobe Commerce Optimizer项目（Adobe管理的SaaS基础架构）。"
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
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: f4d7033067a99421224ab2159b1b95775e5e949f
workflow-type: tm+mt
source-wordcount: 316
ht-degree: 0%

---

# [!UICONTROL Adobe Services] > [!UICONTROL Email Suppression]

{{config}}

[!UICONTROL Email Suppression]允许管理员关闭特定类别的自动化系统电子邮件，而不影响商店的其余电子邮件或要求开发人员参与。 使用此功能可暂时或永久停止某些通知，例如，在数据迁移期间订购电子邮件或营销电子邮件。

>[!IMPORTANT]
>
>此功能绝不会禁止与安全相关的管理员通知，例如双重身份验证代码和管理员密码重置电子邮件。

此页面上的设置适用于每个[商店视图](../../getting-started/websites-stores-views.md#scope-settings)，因此您可以禁止不同商店前面的不同电子邮件类别。

>[!NOTE]
>
>关闭隐藏会立即恢复正常的电子邮件投放，但在隐藏期间发送的电子邮件不会排队。

## [!UICONTROL Email Suppression]

![电子邮件抑制](./assets/email-suppression.png)<!-- zoom -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Enable Email Suppression] | 商店视图 | 该功能的主开关开关。 当设置为`No`（默认）时，将忽略此页面上的所有其他设置，并且所有电子邮件都会正常发送。 |
| [!UICONTROL Disabled Functional Areas] | 商店视图 | 选择其电子邮件被禁止的一个或多个业务类别。 有关每个类别包含的内容，请参阅[业务类别](#business-categories)。 |
| [!UICONTROL Disabled Template IDs] | 商店视图 | 要单独禁止显示的特定电子邮件模板的可选逗号分隔列表，不考虑类别。 使用模板代码（例如，`customer_password_forgot_email_template`）或您在管理员中创建的自定义模板的数值模板ID。 |

{style="table-layout:auto"}

### 业务类别 {#business-categories}

| 类别 | 包括的典型电子邮件 |
|--- |--- |
| 客户帐户 | 帐户创建、密码重置、帐户信息更改。 |
| Order Management | 订单确认、发票、发运、贷项通知单、订单取消。 |
| 退货(RMA) | 退货授权通知。 |
| 结账与付款 | 结帐和按链接付费相关电子邮件。 |
| 营销 | 快讯、产品提醒、愿望清单共享、给朋友发送电子邮件、提醒、邀请、礼品注册表。 |
| 商店信用和奖励 | 礼品卡、奖励积分、商店信用余额更改。 |
| B2B | 公司、可转让报价和采购订单通知。 |
| 系统通知 | 操作通知，如计划的导入、导出和联系表单电子邮件。 |

{style="table-layout:auto"}

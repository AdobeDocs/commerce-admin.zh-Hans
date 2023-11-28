---
title: 电子邮件提醒
description: 了解在满足一组特定条件时会自动向客户发送的电子邮件提醒。
exl-id: 3293caca-9dd3-4d64-a80c-58c92a9208e5
feature: Merchandising, Communications
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '559'
ht-degree: 0%

---

# 电子邮件提醒

{{ee-feature}}

电子邮件提醒的目的是鼓励访问过您的商店的人利用促销活动并购物。 当满足一组特定条件时，可以自动向客户发送电子邮件提醒。 例如，您可以向购物车或愿望清单中添加了一些东西，但尚未购买的客户发送提醒。 您可以使用电子邮件提醒来鼓励客户返回您的商店，并附上 [优惠券代码](price-rules-cart-coupon.md) 作为激励。 系统可以为每批电子邮件提醒自动生成优惠券代码，以便您控制与每批电子邮件提醒关联的优惠。

在放弃购物车后过了特定天数后，或者对于您要定义的任何其他条件，可以触发电子邮件提醒。 常见条件包括购物车总值、数量、购物车中的商品等。

>[!NOTE]
>
>如果客户有多个匹配的放弃购物车、愿望清单或两者的组合，则仅为该客户触发一次电子邮件提醒。 要再次触发相同的电子邮件提醒，请使用 _[!UICONTROL Repeat Schedule]_用于设置电子邮件间隔天数的字段。

![电子邮件提醒](./assets/email-reminders.png){width="700" zoomable="yes"}

## 配置电子邮件提醒

电子邮件提醒规则可以按分钟、小时或天定期发送。 该配置确定批量发送的电子邮件数量，以及显示为消息发送者的存储身份。

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中，展开 **[!UICONTROL Customers]** 并选择 **[!UICONTROL Promotions]**.

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Automated Email Reminder Rules]** 部分并执行以下操作：

   ![客户配置 — 自动电子邮件提醒规则](../configuration-reference/customers/assets/promotions-automated-email-reminder-rules.png){width="600" zoomable="yes"}

   - 设置 **[!UICONTROL Enable Reminder Emails]** 到 `Yes`.

   - 要设置对符合自动电子邮件提醒条件的新客户运行检查的频率，请设置 **[!UICONTROL Frequency]** 更改为以下任一项：

      - `Minute Intervals`
      - `Hourly`
      - `Daily`

   - 设置适当的 **[!UICONTROL Interval]**，基于 _[!UICONTROL Frequency]_设置。

   - 设置 **[!UICONTROL Start Time]** 按24小时制发送电子邮件的时间（小时、分钟和秒）。

   - 要限制可批量发送的电子邮件数量，请在 **[!UICONTROL Maximum Emails per One Run]** 字段。

   - 要避免多次尝试发送失败的电子邮件，请在 **[!UICONTROL Email Send Failure Threshold]** 字段。

   - 设置 **[!UICONTROL Reminder Email Sender]** 到 [商店联系人](../getting-started/store-details.md#store-email-addresses) 显示为提醒电子邮件的发件人。

   有关这些选项的详细列表，请参阅 [自动电子邮件提醒规则](../configuration-reference/customers/promotions.md#automated-email-reminder-rules) 在 _配置引用_.

1. 完成后，单击 **[!UICONTROL Save Config]**.

## 电子邮件提醒模板

可以自定义默认电子邮件提醒模板，并为不同促销活动创建其他模板。 电子邮件提醒包含一系列可纳入消息中的特定变量。 这些变量中的信息由您设置的电子邮件提醒规则以及与优惠券关联的购物车价格规则决定。 “插入变量”按钮可用于将带有变量的标记标记插入到模板中。 要了解更多信息，请参阅 [电子邮件](../systems/email-templates.md).

![电子邮件提醒预览](./assets/email-reminder-preview-promotion-template.png){width="600" zoomable="yes"}

### 自定义电子邮件提醒模板

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Email Templates]**.

1. 单击 **[!UICONTROL Add New Template]**.

1. 在 **[!UICONTROL Template]** 列表在 `Magento_Reminder`，选择 **[!UICONTROL Promotion Notification/Reminder]** 模板。

1. 单击 **[!UICONTROL Load Template]**.

遵循标准 [说明](../systems/email-template-custom.md) 以自定义模板。

### 电子邮件提醒变量

#### 优惠券代码

```
{{var coupon.getCode()|escape}}
```

#### 优惠券使用限制

```
{{var coupon.usage_limit|escape}}
```

#### 每位客户的优惠券使用情况

```
{{var coupon.usage_per_customer|escape}}
```

#### 客户帐户URL

```
{{var this.getUrl($store,'customer/account/',[_nosid:1])}}
```

#### 客户名称

```
{{var customer_data.name|escape}}
```

#### 电子邮件页脚模板

```
{{template config_path="design/email/footer_template"}}
```

#### 电子邮件标头模板

```
{{template config_path="design/email/header_template"}}
```

#### 电子邮件徽标图像替代

```
{{var logo_alt}}
```

#### 电子邮件徽标图像URL

```
{{var logo_url}}
```

#### 提升描述

```
{{var promotion_description|escape|nl2br}}
```

#### 促销名称

```
{{var promotion_name|escape}}
```

#### 存储名称

```
{{var store.frontend_name}}
```

#### 商店URL

```
{{store url=""}}
```

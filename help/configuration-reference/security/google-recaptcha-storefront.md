---
title: '[!UICONTROL Security] > [!UICONTROL Google reCAPTCHA Storefront]'
description: 查看Commerce管理员的[!UICONTROL Security] &gt； [!UICONTROL Google reCAPTCHA Storefront]页面上的配置设置。
exl-id: 6c03ee68-7421-4c74-bdc1-0855f088b7f9
feature: Configuration, Security
TQID: https://experienceleague.adobe.com/Hl5Ivzg-z8tu96TaZN45UFCMMJ4g05fU5t-Jwok1jZE
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2:
  - id: f56d26ed-050b-4fb7-b29b-8e6e994e80a2
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
source-wordcount: 1480
ht-degree: 0%

---

# [!UICONTROL Security] > [!UICONTROL Google reCAPTCHA Storefront]

>[!IMPORTANT]
>
>在配置Google reCAPTCHA之前，必须确保您的`PHP.ini`文件包含以下设置：`allow_url_fopen = 1`。 这可能需要开发人员的帮助。 请参阅&#x200B;_安装指南_&#x200B;中的[PHP设置](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/php-settings.html?lang=zh-Hans)。

{{config}}

有关使用Google reCAPTCHA保护存储安全的更多信息，请参阅&#x200B;_Admin Systems指南_&#x200B;中的Google [reCAPTCHA](../../systems/security-google-recaptcha.md)。

## [!UICONTROL reCAPTCHA v2 ("I am not a robot")]

![reCAPTCHA v2 （“我不是机器人”）](./assets/recaptcha-storefront-v2-not-robot.png)<!-- zoom -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--|--|--|
| [!UICONTROL Google API Website Key] | 网站 | 注册Google reCAPTCHA帐户时创建的网站密钥。 |
| [!UICONTROL Google API Secret Key] | 网站 | 与您的Google reCAPTCHA帐户关联的密钥。 |
| [!UICONTROL Size] | 网站 | 客户登录其帐户时显示的Google reCAPTCHA框的大小。 选项： `Normal` （默认） / `Compact` |
| [!UICONTROL Theme] | 网站 | 确定Google reCAPTCHA框的样式。 选项： `Light Theme` （默认） / `Dark Theme` |
| [!UICONTROL Language Code] | 商店视图 | [双字符代码](https://developers.google.com/recaptcha/docs/language)，它指定用于Google reCAPTCHA文本和消息传递的语言。 |

{style="table-layout:auto"}

## [!UICONTROL reCAPTCHA v2 Invisible]

![reCAPTCHA v2不可见](./assets/recaptcha-storefront-v2-invisible.png)<!-- zoom -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--|--|--|
| [!UICONTROL Google API Website Key] | 网站 | 注册Google reCAPTCHA帐户时创建的网站密钥。 |
| [!UICONTROL Google API Secret Key] | 网站 | 与您的Google reCAPTCHA帐户关联的密钥。 |
| [!UICONTROL Invisible Badge Position] | 网站 | 每个页面上不可见reCAPTCHA徽章的位置。 选项： `Inline` / `Bottom Right` / `Bottom Left` |
| [!UICONTROL Theme] | 全局 | 确定Google reCAPTCHA框的样式。 选项： `Light Theme` （默认） / `Dark Theme` |
| [!UICONTROL Language Code] | 商店视图 | [双字符代码](https://developers.google.com/recaptcha/docs/language)，它指定用于Google reCAPTCHA文本和消息传递的语言。 |

{style="table-layout:auto"}

## [!UICONTROL reCAPTCHA v3 Invisible]

![reCAPTCHA v3不可见](./assets/recaptcha-storefront-v3-invisible.png)<!-- zoom -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--|--|--|
| [!UICONTROL Google API Website Key] | 网站 | 注册Google reCAPTCHA帐户时创建的网站密钥。 |
| [!UICONTROL Google API Secret Key] | 网站 | 与您的Google reCAPTCHA帐户关联的密钥。 |
| [!UICONTROL Minimum Score Threshold] | 全局 | 将用户交互识别为潜在风险的最小分数，其中1.0表示典型的用户交互，0.0表示可能是机器人。 默认： `0.5` |
| [!UICONTROL Invisible Badge Position] | 网站 | 每个页面上不可见reCAPTCHA徽章的位置。 选项： `Inline` / `Bottom Right` / `Bottom Left` |
| [!UICONTROL Theme] | 网站 | 确定Google reCAPTCHA框的样式。 选项： `Light Theme` （默认） / `Dark Theme` |
| [!UICONTROL Language Code] | 商店视图 | [双字符代码](https://developers.google.com/recaptcha/docs/language)，它指定用于Google reCAPTCHA文本和消息传递的语言。 |

{style="table-layout:auto"}

## [!UICONTROL reCAPTCHA Enterprise]

仅[!BADGE SaaS]{type=Positive url="https://experienceleague.adobe.com/zh-hans/docs/commerce/user-guides/product-solutions" tooltip="仅适用于Adobe Commerce as a Cloud Service项目（Adobe管理的SaaS基础架构）。"}

![reCAPTCHA v3 Enterprise](./assets/recaptcha-storefront-v3-enterprise.png)<!-- zoom -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--|--|--|
| [!UICONTROL Site Key] | 网站 | 注册Google reCAPTCHA Enterprise帐户时创建的站点密钥。 |
| [!UICONTROL Google Cloud Project ID] | 网站 | 项目ID显示在项目仪表板的&#x200B;**项目信息**&#x200B;部分中。 |
| [!UICONTROL Service Account JSON] | 网站 | 从Google Cloud控制台下载服务帐户密钥，并将其内容粘贴到此字段中。 |
| [!UICONTROL Minimum Score Threshold] | 网站 | 将用户交互识别为潜在风险的最小分数，其中1.0表示典型的用户交互，0.0表示可能是机器人。 默认： `0.5` |
| [!UICONTROL Badge Position] | 网站 | 每个页面上不可见reCAPTCHA徽章的位置。 选项： `Inline` / `Bottom Right` / `Bottom Left` |
| [!UICONTROL Theme] | 网站 | 确定Google reCAPTCHA框的样式。 选项： `Light Theme` （默认） / `Dark Theme` |
| [!UICONTROL Language Code] | 商店视图 | [双字符代码](https://developers.google.com/recaptcha/docs/language)，它指定用于Google reCAPTCHA文本和消息传递的语言。 将该字段留空以使用用户浏览器的默认语言。 |
| [!UICONTROL Validation Failure Message] | 商店视图 | 验证失败时显示的消息。 |

{style="table-layout:auto"}

## [!UICONTROL reCAPTCHA Failure Messages]

![失败消息](./assets/recaptcha-storefront-failure-messages.png)<!-- zoom -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--|--|--|
| [!UICONTROL reCAPTCHA Validation Failure Message] | 商店视图 | 验证失败时显示在店面中的消息。 默认文本： `reCAPTCHA verification failed.` |
| [!UICONTROL reCAPTCHA Technical Failure Message] | 商店视图 | 如果reCAPTCHA无法返回验证结果，则在店面中显示的消息。 默认文本： `Something went wrong with reCAPTCHA. Please contact the store owner.` |

{style="table-layout:auto"}

## [!UICONTROL Storefront]

![店面](./assets/recaptcha-storefront.png)<!-- zoom -->

>[!NOTE]
>
>您选择的reCAPTCHA类型必须与与Google reCAPTCHA帐户中的API密钥关联的类型匹配。

>[!WARNING]
>
>使用reCAPTCHA版本3时，得分较低的正版用户无法继续。 对于版本2，得分较低的真实用户会收到挑战。 仔细考虑得分较低的真实用户是否有机会解决难题（版本2）或遭到阻止（版本3）。

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--|--|--|
| [!UICONTROL Enable for Customer Login] | 网站 | 指定客户[登录](../../customers/customer-sign-in.md)其帐户时使用的reCAPTCHA类型。 选项： <br/>**`No`**- （默认）不验证登录请求。<br />**`reCAPTCHA v2 ("I am not a robot")`**  — 要求用户选中&#x200B;_我不是自动机_&#x200B;复选框。<br />**`Invisible reCAPTCHA v2`**— 在后台验证用户行为，无需根据分数进行交互。<br/>**`Invisible reCAPTCHA v3`**  — （推荐）根据交互得分在后台验证用户行为。 |
| [!UICONTROL Enable for Forgot Password] | 网站 | 指定客户请求[密码重置](../../customers/password-reset.md)时使用的reCAPTCHA类型。 选项： <br/>**`No`**- （默认）不验证密码重置请求。<br />**`reCAPTCHA v2 ("I am not a robot")`**  — 要求用户选中&#x200B;_我不是自动机_&#x200B;复选框。<br />**`Invisible reCAPTCHA v2`**— 在后台验证用户行为，无需根据分数进行交互。<br/>**`Invisible reCAPTCHA v3`**  — （推荐）根据交互得分在后台验证用户行为。 |
| [!UICONTROL Enable for Create New Customer Account] | 网站 | 指定客户注册[新帐户](../../customers/account-create.md)时使用的reCAPTCHA类型。 选项：<br/>**`No`**- （默认）不验证帐户请求。<br />**`reCAPTCHA v2 ("I am not a robot")`**  — 要求用户选中&#x200B;_我不是自动机_&#x200B;复选框。<br />**`Invisible reCAPTCHA v2`**— 在后台验证用户行为，无需根据分数进行交互。<br/>**`Invisible reCAPTCHA v3`**  — （推荐）根据交互得分在后台验证用户行为。 |
| [!UICONTROL Enable for Edit Customer Account] | 网站 | 指定客户更改其[帐户信息](../../customers/account-dashboard-account-information.md)时使用的reCAPTCHA类型。 选项：<br/>**`No`**- （默认）不验证帐户请求。<br />**`reCAPTCHA v2 ("I am not a robot")`**  — 要求用户选中&#x200B;_我不是自动机_&#x200B;复选框。<br />**`Invisible reCAPTCHA v2`**— 在后台验证用户行为，无需根据分数进行交互。<br/>**`Invisible reCAPTCHA v3`**  — （推荐）根据交互得分在后台验证用户行为。 |
| [!UICONTROL Enable for Create New Company Account] | 网站 | ![Adobe Commerce B2B](../../assets/b2b.svg) （仅适用于Adobe Commerce B2B）指定在创建新的[公司帐户](../../b2b/account-company-create.md)时使用的reCAPTCHA类型。 选项：<br/>**`No`**- （默认）不验证帐户请求。<br />**`reCAPTCHA v2 ("I am not a robot")`**  — 要求用户选中&#x200B;_我不是自动机_&#x200B;复选框。<br />**`Invisible reCAPTCHA v2`**— 在后台验证用户行为，无需根据分数进行交互。<br/>**`Invisible reCAPTCHA v3`**  — （推荐）根据交互得分在后台验证用户行为。 |
| [!UICONTROL Enable for Contact Us] | 网站 | 指定用于从商店的[联系我们](../../getting-started/store-details.md#contact-us-form)页面发送消息的reCAPTCHA类型。 选项：<br/>**`No`**- （默认）不验证消息请求。<br />**`reCAPTCHA v2 ("I am not a robot")`**  — 要求用户选中&#x200B;_我不是自动机_&#x200B;复选框。<br />**`Invisible reCAPTCHA v2`**— 在后台验证用户行为，无需根据分数进行交互。<br/>**`Invisible reCAPTCHA v3`**  — （推荐）根据交互得分在后台验证用户行为。 |
| [!UICONTROL Enable for Product Review] | 网站 | 指定客户提交[产品审核](../../merchandising-promotions/product-reviews.md)时使用的reCAPTCHA类型。 选项： <br/>**`No`**- （默认）不验证产品审核请求。<br />**`reCAPTCHA v2 ("I am not a robot")`**  — 要求用户选中&#x200B;_我不是自动机_&#x200B;复选框。<br />**`Invisible reCAPTCHA v2`**— 在后台验证用户行为，无需根据分数进行交互。<br/>**`Invisible reCAPTCHA v3`**  — （推荐）根据交互得分在后台验证用户行为。 |
| [!UICONTROL Enable for Newsletter Subscription] | 网站 | 指定客户注册[新闻稿订阅](../../merchandising-promotions/newsletter-subscribers.md)时使用的不可见reCAPTCHA类型。 选项：<br/>**`No`**- （默认）不验证新闻稿订阅请求。<br />**`reCAPTCHA v2 ("I am not a robot")`**  — 要求用户选中&#x200B;_我不是自动机_&#x200B;复选框。<br />**`Invisible reCAPTCHA v2`**— 在后台验证用户行为，无需根据分数进行交互。<br/>**`Invisible reCAPTCHA v3`**  — （推荐）根据交互得分在后台验证用户行为。 |
| [!UICONTROL Enable for Gift Card] | 网站 | ![Adobe Commerce](../../assets/adobe-logo.svg)（仅限Adobe Commerce）指定客户输入[礼品卡](../../catalog/product-gift-card-create.md)代码时使用的reCAPTCHA类型。 选项：<br/>**`No`**- （默认）不验证礼品卡代码提交。<br />**`reCAPTCHA v2 ("I am not a robot")`**  — 要求用户选中&#x200B;_我不是自动机_&#x200B;复选框。<br />**`Invisible reCAPTCHA v2`**— 在后台验证用户行为，无需根据分数进行交互。<br/>**`Invisible reCAPTCHA v3`**  — （推荐）根据交互得分在后台验证用户行为。 |
| [!UICONTROL Enable for Invitation Create Account] | 网站 | 指定客户发送帐户创建[邀请](../../merchandising-promotions/invitations.md)代码时使用的reCAPTCHA类型。 选项：<br/>**`No`**- （默认）不验证邀请电子邮件提交。<br />**`reCAPTCHA v2 ("I am not a robot")`**  — 要求用户选中&#x200B;_我不是自动机_&#x200B;复选框。<br />**`Invisible reCAPTCHA v2`**— 在后台验证用户行为，无需根据分数进行交互。<br/>**`Invisible reCAPTCHA v3`**  — （推荐）根据交互得分在后台验证用户行为。 |
| [!UICONTROL Enable for Send to Friend] | 网站 | 指定客户[与朋友共享产品](../../stores-purchase/email-a-friend.md)时使用的reCAPTCHA类型。 选项：<br/>**`No`**- （默认）不验证电子邮件提交。<br />**`reCAPTCHA v2 ("I am not a robot")`**  — 要求用户选中&#x200B;_我不是自动机_&#x200B;复选框。<br />**`Invisible reCAPTCHA v2`**— 在后台验证用户行为，无需根据分数进行交互。<br/>**`Invisible reCAPTCHA v3`**  — （推荐）根据交互得分在后台验证用户行为。 |
| [!UICONTROL Enable for Wishlist Sharing] | 网站 | 指定客户[共享愿望清单](../../stores-purchase/wishlist-storefront.md#share-the-wish-list)时使用的reCAPTCHA类型。 选项：<br/>**`No`**- （默认）不验证邮件和电子邮件提交。<br />**`reCAPTCHA v2 ("I am not a robot")`**  — 要求用户选中&#x200B;_我不是自动机_&#x200B;复选框。<br />**`Invisible reCAPTCHA v2`**— 在后台验证用户行为，无需根据分数进行交互。<br/>**`Invisible reCAPTCHA v3`**  — （推荐）根据交互得分在后台验证用户行为。 |
| [!UICONTROL Enable for Coupon Codes] | 网站 | 指定客户输入[优惠券代码](../../merchandising-promotions/price-rules-cart-coupon.md)时使用的reCAPTCHA类型。 选项：<br/>**`No`**- （默认）不验证优惠券代码提交。<br />**`reCAPTCHA v2 ("I am not a robot")`**  — 要求用户选中&#x200B;_我不是自动机_&#x200B;复选框。<br />**`Invisible reCAPTCHA v2`**— 在后台验证用户行为，无需根据分数进行交互。<br/>**`Invisible reCAPTCHA v3`**  — （推荐）根据交互得分在后台验证用户行为。 |
| [!UICONTROL Enable for PayPal Payflow Pro payment form] | 网站 | 指定客户使用[PayPal Payflow Pro](../../stores-purchase/paypal-payflow-pro.md)支付购买费用时使用的reCAPTCHA类型。 选项： <br/>**`No`**- （默认）不验证密码重置请求。<br />**`reCAPTCHA v2 ("I am not a robot")`**  — 要求用户选中&#x200B;_我不是自动机_&#x200B;复选框。<br />**`Invisible reCAPTCHA v2`**— 在后台验证用户行为，无需根据分数进行交互。<br/>**`Invisible reCAPTCHA v3`**  — （推荐）根据交互得分在后台验证用户行为。 |

{style="table-layout:auto"}

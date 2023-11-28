---
title: 客户密码选项
description: 客户密码选项决定了您的商店的各种面向客户的功能的安全级别。
exl-id: 84dec8e8-3363-4133-bbcc-9e58467749c4
feature: Customers, Configuration, Security
source-git-commit: ea9eeea0fc5213de2787e0b7ea2aed825ca3a9de
workflow-type: tm+mt
source-wordcount: '394'
ht-degree: 0%

---

# 客户密码选项

客户密码选项决定了用于密码重置请求的安全级别、用于客户通知的电子邮件模板以及密码恢复链接的生命周期。 您可以允许客户更改自己的密码，或要求仅存储管理员可以更改密码。

## 配置客户密码选项

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中，展开 **[!UICONTROL Customers]** 并选择 **[!UICONTROL Customer Configuration]**.

1. 展开 **[!UICONTROL Password Options]** 部分。

   ![密码选项](../configuration-reference/customers/assets/customer-configuration-password-options.png){width="600" zoomable="yes"}

1. 设置 **[!UICONTROL Password Reset Protection Type]** 要用于检查密码重置请求的方法：

   - `By IP and Email`  — 检查以前是否尝试重置特定电子邮件或特定IP的密码。
   - `By IP`  — 检查以前是否尝试从特定IP重置密码。
   - `By Email`  — 检查以前是否尝试重置特定电子邮件的密码。
   - `None`  — 已禁用保护（对重置密码没有限制）。

   此 **[!UICONTROL Max Number of Password Reset Requests]** 和 **[!UICONTROL Min Time Between Password Reset Requests]** 将基于此配置进行计算。

1. 要限制每小时发送的密码重置请求数，请执行以下操作：

   - 对象 **[!UICONTROL Max Number of Password Reset Requests]**，输入每小时可发送的最大密码重置请求数。

   - 对象 **[!UICONTROL Min Time Between Password Reset Requests]**，输入两次请求之间必须经过的最小分钟数。

1. 要配置密码重置电子邮件通知，请执行以下操作：

   - 设置 **[!UICONTROL Forgot Email Template]** 用于发送给忘记密码的客户的电子邮件的模板。

   - 设置 **[!UICONTROL Remind Email Template]** 到管理员用户重置客户密码时使用的模板。

   - 设置 **[!UICONTROL Reset Password Template]** 更改为客户更改密码时使用的模板。

   - 设置 **[!UICONTROL Password Template Email Sender]** 到 [商店联系人](../getting-started/store-details.md) 显示为密码相关通知的发送者。

1. 完成以下密码重置安全选项：

   - 对象 **[!UICONTROL Recovery Link Expiration Period (hours)]**，输入密码恢复链接过期的小时数。

   - 如果您希望客户登录和忘记密码表单中的字段自动填写以前条目中的字段，请设置 **[!UICONTROL Enable Autocomplete on login/forgot password forms]** 到 `Yes`.

   - 对象 **[!UICONTROL Number of Required Character Classes]**，根据以下字符类输入密码中必须包括的不同字符类型数：

      - `Lowercase`
      - `Uppercase`
      - `Numeric`
      - `Special Characters`

   - 对象 **[!UICONTROL Maximum Login Failures to Lockout Account]**，输入在锁定客户帐户之前的失败登录尝试次数。 对于无限制的尝试，输入零(`0`)。

   - 对象 **[!UICONTROL Minimum Password Length]**，输入密码中可以使用的最小字符数。 数字必须大于零。

   - 对象 **[!UICONTROL Lockout Time (minutes)]**，输入客户帐户在尝试登录失败次数过多后锁定的分钟数。

1. 完成后，单击 **[!UICONTROL Save Config]**.

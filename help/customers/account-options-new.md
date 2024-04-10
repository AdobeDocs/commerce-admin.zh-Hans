---
title: 新的客户帐户选项
description: 了解商店中新客户帐户的配置选项。
exl-id: aa19f0e2-ffbe-433d-8bd5-c14700b67b37
feature: Customers, Configuration
source-git-commit: 06673ccb7eb471d3ddea97218ad525dd2cdcf380
workflow-type: tm+mt
source-wordcount: '368'
ht-degree: 0%

---

# 新的客户帐户选项

在 _[!UICONTROL Create New Account Options]_在配置部分，基本帐户选项与与VAT ID验证和自定义集成相关的更多高级选项组合在一起。 以下说明仅涵盖最常用的选项。 要了解自动客户组分配，请参阅 [增值税验证](../stores-purchase/vat.md).

![创建新帐户选项](assets/customer-configuration-create-new-account-options.png){width="600" zoomable="yes"}

## 设置基本客户帐户选项

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中，展开 **[!UICONTROL Customers]** 并选择 **[!UICONTROL Customer Configuration]**.

1. 展开 **[!UICONTROL Create New Account Options]** 部分：

   ![新建帐户选项默认设置](../configuration-reference/customers/assets/customer-configuration-create-new-account-options.png){width="600" zoomable="yes"}

1. 根据您在店面需要支持的客户体验设置每个选项：

   - 设置 **[!UICONTROL Default Group]** 创建帐户时分配给新客户的客户组。

   - 如果您拥有 _增值税_ 编号并希望客户能够看到它，请设置 **[!UICONTROL Show VAT Number on Storefront]** 到 `Yes`.

   - 要在客户管理员订单创建过程中需要客户发送电子邮件，请设置 **[!UICONTROL Email is required field for Admin order creation]** 到 `Yes`.

   - 输入 **[!UICONTROL Default Email Domain]** 对于商店，如 `mystore.com`

   - 设置 **[!UICONTROL Default Welcome Email]** ，该模板用于向新客户发送欢迎电子邮件。

   - 要要求客户确认其使用您的商店开立帐户的请求，请设置 **[!UICONTROL Require Emails Confirmation]** 到 `Yes`. 然后，设置 **[!UICONTROL Confirmation Link Email]** 添加到用于确认电子邮件的模板。

     >[!NOTE]
     >
     >从版本2.4.7开始，客户必须重新输入其电子邮件和密码，以在电子邮件确认后登录到其帐户，而不考虑浏览器。

   - 设置 **[!UICONTROL Welcome Email]** 用于确认帐户后发送的欢迎消息的模板。

   - 设置 **[!UICONTROL Default Welcome Email without Password]** 到创建还没有密码的客户帐户时使用的模板。 例如，从管理员创建的客户帐户尚未分配密码。

   - 设置 **[!UICONTROL Email Sender]** 将显示为欢迎电子邮件发件人的商店联系人。

   - 要要求客户确认其使用您的商店开立帐户的请求，请设置 **[!UICONTROL Require Emails Confirmation]** 到 `Yes`. 然后，设置 **[!UICONTROL Confirmation Link Email]** 添加到用于确认电子邮件的模板。

   ![在启用VAT的情况下创建新帐户选项](../configuration-reference/customers/assets/customer-configuration-create-new-account-options-vat.png){width="600" zoomable="yes"}

   有关此配置选项集中每个可用选项的详细信息，请参见 _创建新帐户选项_ [配置引用](../configuration-reference/customers/customer-configuration.md).

1. 完成后，单击 **[!UICONTROL Save Config]**.

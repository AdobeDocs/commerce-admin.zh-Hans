---
title: 创建单个客户帐户
description: 访客可以轻松地创建单个客户帐户来管理他们的购买。
exl-id: 8d08c0e1-f3ba-4423-98a7-ffa8ba5a1b8b
feature: Customers, Storefront
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '1246'
ht-degree: 0%

---

# 创建单个客户帐户

您商店的访客可以开立帐户来管理其购买和活动。 客户通常从您的商店创建自己的帐户。 但是，您也可以直接从管理员创建客户帐户，这对于通过电话帮助客户非常有用。

以下说明代表默认的客户帐户配置。 要更改表单中某些字段的选择和行为，请参阅 [配置客户帐户](../customers/customer-account-scope.md).

作为商店管理员，您还可以设置 [新帐户选项](../customers/account-options-new.md) 向新的注册客户发送确认电子邮件，这有助于确保注册帐户有效。

{{beta-updates}}

## 从店面创建帐户

店铺客户在店面上创建帐户。

1. 从店面，单击 **[!UICONTROL Create an Account]** 标题的右上角。

   ![创建帐户](assets/storefront-create-an-account-link.png){width="700" zoomable="yes"}

1. 下 **[!UICONTROL Personal Information]**，输入其 **[!UICONTROL First Name]** 和 **[!UICONTROL Last Name]**.

   ![个人信息](assets/storefront-create-account-personal-information.png){width="600" zoomable="yes"}

1. 如果他们想要将其姓名和电子邮件地址添加到新闻稿订阅者的列表，客户将选择 **[!UICONTROL Sign Up for Newsletter]** 复选框。

   >[!INFO]
   >
   > 即使商店未发布新闻稿，也会出现此选项。

1. 如果他们希望商店支持人员 [查看他们看到的内容](../customers/login-as-customer.md) 并提供远程协助，客户应选择 **[!UICONTROL Allow remote shopping assistance]** 复选框。

1. 下 **[!UICONTROL Sign-in Information]**，输入其 **[!UICONTROL Email]** 地址。

   >[!INFO]
   >
   > 此电子邮件地址将成为其登录凭据的一部分，且无法与任何其他客户帐户关联。

   ![登录信息](assets/storefront-create-account-signin-information.png){width="600" zoomable="yes"}

1. 输入 **[!UICONTROL Password]** 其中包括以下三种类型的信息：

   - 小写字符
   - 大写字符
   - 数字
   - 特殊字符

   按下按钮后 **[!UICONTROL Enter]**，将评估密码的强度，并显示在字段下方。 如果密码被认为是 _弱_，尝试其他值，直到它被评估为 _强_.

   ![建议使用强密码](assets/storefront-customer-account-create-password-strong.png){width="600" zoomable="yes"}

1. 然后，客户再次输入 **[!UICONTROL Confirm Password]**.

1. 如果需要，请单击 **[!UICONTROL Show Password]** 查看您输入的密码。

1. 完成后，单击 **创建帐户**.

然后，客户可以使用他们的电子邮件地址和密码来 [登录](../customers/customer-sign-in.md) 并填写地址信息。

## 从管理员创建帐户

作为贸易商，您可以从管理员创建客户帐户。

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. 单击 **[!UICONTROL Add New Customer]**.

### 第1步：填写帐户信息

![客户信息](assets/new-information.png){width="700" zoomable="yes"}

1. 在 **[!UICONTROL Account Information]** 部分，执行以下操作：

   - 对于多站点安装，请设置 **[!UICONTROL Associate to Website]** 到客户帐户适用的网站。
   - 如果适用，将客户分配给其他 **[!UICONTROL Customer Group]**.
   - 如果您使用 [VAT ID验证](../stores-purchase/vat.md) 并希望 **[!UICONTROL Disable Automatic Group Change Based on VAT ID]**，选中复选框。

1. 填写必填字段：

   - **[!UICONTROL First Name]**
   - **[!UICONTROL Last Name]**
   - **[!UICONTROL Email]**

1. 根据需要填写可选字段：

   - **[!UICONTROL Name Prefix]**
   - **[!UICONTROL Middle Name/Initial]**
   - **[!UICONTROL Name Suffix]**
   - **[!UICONTROL Date of Birth]**
   - **[!UICONTROL Tax/VAT Number]**
   - **[!UICONTROL Gender]**

   >[!WARNING]
   >
   >按照最新的安全和隐私最佳实践，了解将客户的完整出生日期（月、日、年）与其他个人标识符一起存储可能会带来的任何法律和安全风险。 建议您限制存储客户的完整出生日期，并建议使用客户出生年份作为替代方法。

1. 设置 **[!UICONTROL Send Welcome Email From]** 到商店视图，商店视图 _欢迎_ 将发送电子邮件。

   >[!INFO]
   >
   > 如果存储有不同的视图 [语言](../stores-purchase/store-localize.md)，此设置确定欢迎电子邮件的语言。

1. 单击 **[!UICONTROL Save and Continue Edit]** 页面顶部的。

   >[!INFO]
   >
   >保存客户帐户后，整套选项将显示在左侧面板和页面顶部的菜单中。 此 _[!UICONTROL Customer View]_选项卡显示帐户的摘要。

   ![客户视图](assets/customer-account-create-saved.png){width="600" zoomable="yes"}

### 第2步：填写地址信息

1. 在左侧面板中，选择 **[!UICONTROL Addresses]** 并单击 **[!UICONTROL Add New Addresses]**.

1. 如果帐单和送货使用相同的地址，则切换两个选项。

   - **[!UICONTROL Default Billing Address]**
   - **[!UICONTROL Default Shipping Address]**

   ![添加客户地址信息](assets/information-addresses.png){width="600" zoomable="yes"}

1. 向下滚动并填写第二列中的必填地址字段。

   - **[!UICONTROL Street Address]**
   - **[!UICONTROL City]**
   - **[!UICONTROL Country]**
   - **[!UICONTROL State/Province]**
   - **[!UICONTROL ZIP/Postal Code]**

1. 输入 **[!UICONTROL Phone Number]** 用于此地址。

1. 如果适用，请输入 **[!UICONTROL VAT Number]** 与客户相关联。

1. 如果此地址是该帐户唯一需要的地址，请单击 **[!UICONTROL Save]**.

   否则，请单击 **[!UICONTROL Save and Continue Edit]** 并重复上述步骤以添加其他地址。

   新地址显示在 [!UICONTROL Addresses] 选定的页面 _[!UICONTROL Default Billing]_和_[!UICONTROL Default Shipping]_ 地址在完整列表上方。

   ![地址视图](assets/address-list.png){width="600" zoomable="yes"}

### 步骤3：重置密码

从管理员创建的客户帐户最初不会分配密码。

1. 在网格中查找新的客户帐户。

1. 单击 **[!UICONTROL Edit]** 在 _[!UICONTROL Action]_列。

1. 在页面顶部的菜单栏中，单击 **[!UICONTROL Reset Password]**.

1. 通知将发送给帐户所有者，其中包含设置密码的说明。

## 按钮栏

首次保存配置文件时，其他按钮将变为可用。 要了解更多信息，请参阅 [更新客户配置文件](../customers/update-account.md).

| 按钮 | 描述 |
|--- |--- |
| **[!UICONTROL Back]** | 返回到 _[!UICONTROL Customers]_页面，而不保存更改。 |
| **[!UICONTROL Delete Customer]** | 删除当前客户。 不会删除与客户关联的已完成订单。 |
| **[!UICONTROL Reset]** | 将客户表单中未保存的任何更改重置为其以前的值。 |
| **[!UICONTROL Create Order]** | 为客户创建订单。 |
| **[!UICONTROL Reset Password]** | 发送 [重置密码](../customers/password-reset.md) 通过电子邮件链接到客户。 |
| **[!UICONTROL Force Sign-in]** | 撤销与客户帐户关联的OAuth访问令牌。 此函数只能用于已将OAuth令牌作为Web API的一部分分配的客户帐户 [集成](../systems/integrations.md). 要了解更多信息，请参阅 [基于OAuth的身份验证](https://developer.adobe.com/commerce/webapi/get-started/authentication/gs-authentication-oauth/) 在开发人员文档中。 |
| **[!UICONTROL Manage Shopping Cart]** | 允许管理员管理客户的购物车。 |
| **[!UICONTROL Save and Continue Edit]** | 保存更改并保持客户个人资料处于打开状态。 |
| **[!UICONTROL Save Customer]** | 保存更改并关闭客户配置文件。 |

{style="table-layout:auto"}

## 字段描述

### [!UICONTROL Account Information]

| 字段 | 描述 |
|--- |--- |
| **[!UICONTROL Associate to Website]** | 标识与客户帐户关联的网站。 |
| **[!UICONTROL Group]** | 标识 [客户组](../customers/customer-groups.md) 客户是会员的。 如果适用，请选中此复选框以禁用基于增值税的自动组更改。 |
| **[!UICONTROL Name Prefix]** | 如果使用，则为与客户名称关联的前缀（例如Mr、Ms.或Dr）。 前缀值由 [配置](../configuration-reference/customers/customer-configuration.md). 根据配置，输入控件可以是文本字段或选项列表。 |
| **[!UICONTROL First Name]** | 客户的名字。 |
| **[!UICONTROL Middle Name / Initial]** | 客户的中间名或首字母。 仅当在 [配置](../configuration-reference/customers/customer-configuration.md) 主题。 |
| **[!UICONTROL Last Name]** | 客户的姓氏。 |
| **[!UICONTROL Name Suffix]** | 如果使用后缀，则为与客户名称关联的后缀（如Jr.、Sr.或III）。 后缀值由 [配置](../configuration-reference/customers/customer-configuration.md). 根据配置，输入控件可以是文本字段或选项的下拉列表。 |
| **[!UICONTROL Email]** | 客户的电子邮件地址。 |
| **[!UICONTROL Date of Birth]** | 客户的出生日期。 出生日期包括在 [配置](../configuration-reference/customers/customer-configuration.md) 主题。 <br><br>按照最新的安全和隐私最佳实践，了解将客户的完整出生日期（月、日、年）与其他个人标识符一起存储可能会带来的任何法律和安全风险。 建议限制存储客户的完整出生日期，并建议使用客户出生年份作为替代方法。 |
| **[!UICONTROL Tax / VAT Number]** | 客户的税务或增值税编号（如果适用）。 |
| **[!UICONTROL Gender]** | 确定客户的性别。 性别包括(如果 [配置](../configuration-reference/customers/customer-configuration.md). 选项： `Male` / `Female` / `Not Specified` |
| **[!UICONTROL Send Welcome Email From]** | 如果您有多个存储视图，此设置将标识从中发送欢迎消息的存储视图。 如果商店视图用于不同的语言，则此设置将确定欢迎电子邮件的语言。 |

### [!UICONTROL Addresses]

| 字段 | 描述 |
|--- |--- |
| **[!UICONTROL New Addresses]** | 标识新地址的类型。 选项： `Default Billing Address` / `Default Shipping Address` |
| **[!UICONTROL Add New Addresses]** | 显示另一个“新建地址”部分，以标识要输入的地址的类型。 |
| **[!UICONTROL Company]** | 公司名称（如果适用于此地址）。 |
| **[!UICONTROL Street Address]** | 客户的街道地址。 街道地址的第二行是可用的，如果在 [配置](../configuration-reference/customers/customer-configuration.md) 主题。 |
| **[!UICONTROL City]** | 客户地址所在的城市。 |
| **[!UICONTROL Country]** | 客户地址所在的国家/地区。 |
| **[!UICONTROL State/Province]** | 客户地址所在的省/市/自治区。 |
| **[!UICONTROL Zip/Postal Code]** | 客户地址所在的邮政编码。 |
| **[!UICONTROL Phone Number]** | 客户与地址关联的电话号码。 |
| **[!UICONTROL VAT Number]** | 适用于此地址客户的增值税编号（如果适用）。 |

---
title: 重置客户密码
description: 客户通常从店面重置密码，但店面管理员可以从管理员启动密码重置或强制登录。
exl-id: bca1ef3e-2bc6-4146-ac86-d6c58c8995e4
feature: Customers, Configuration, Security
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '386'
ht-degree: 0%

---

# 重置客户密码

客户通常通过单击从店面重置密码 _[!UICONTROL Forgot Your Password?]_. 但是，存储管理员可以从管理员启动密码重置或强制登录。

| 函数 | 描述 |
| --- | --- |
| 重置密码 | 密码重置电子邮件将直接发送到客户的电子邮件帐户。 商店管理员无法获得对客户密码的访问权限。 |
| 强制登录 | 撤销与客户帐户关联的OAuth访问令牌。 这只能用于已分配OAuth令牌作为Web API一部分的客户帐户 [集成](../systems/integrations.md). 要了解更多信息，请参阅 [基于OAuth的身份验证](https://developer.adobe.com/commerce/webapi/get-started/authentication/gs-authentication-oauth/) 在开发人员文档中。 <br/><br/>从店面或管理员创建的标准客户帐户没有OAuth令牌。 |

{style="table-layout:auto"}

## 从店面重置密码

1. 在登录页面上，客户单击 **[!UICONTROL Forgot Your Password?]**.

1. 出现提示时，输入 **[!UICONTROL Email Address]** 与其帐户和点击量关联的页面数量 **[!UICONTROL Reset My Password]**.

   ![忘记密码](assets/forgot-password.png){width="600" zoomable="yes"}

   >[!INFO]
   >
   >如果输入的电子邮件地址与帐户关联的电子邮件地址匹配，则客户会收到“密码重置确认”电子邮件，其中包含用于重置其密码的链接。

1. 当电子邮件到达时，客户单击 _重置密码_ 链接并输入其 **[!UICONTROL New Password]** 出现提示时。

1. 再次输入以进行确认并单击 **[!UICONTROL Reset Password]**.

   >[!IMPORTANT]
   >
   >新密码长度必须是6个或更多字符，且不能包含空格。 当他们收到密码已更新的确认信息时，可以使用新密码登录到他们的帐户。 默认情况下， _重置密码_ 链接的有效期限为24小时。

## 从管理员重置密码

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. 在网格中查找客户帐户，然后单击 **[!UICONTROL Edit]** 在 _操作_ 列。

1. 在页面顶部的一组选项中，单击 **[!UICONTROL Reset Password]**.

   一小时内允许的密码重置请求数在 [配置](../configuration-reference/customers/customer-configuration.md) 主题。

## 撤销客户的OAuth令牌

>[!IMPORTANT]
>
>除非您完全了解API身份验证，否则不要继续。

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. 在网格中查找客户帐户，然后单击 **[!UICONTROL Edit]** 在 _操作_ 列。

1. 在页面顶部的一组选项中，单击 **[!UICONTROL Force Sign In]**.

1. 提示确认时，单击 **确定**.

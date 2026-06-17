---
title: 重置客户密码
description: 客户通常从店面重置密码，但店面管理员可以从管理员启动密码重置或强制登录。
exl-id: bca1ef3e-2bc6-4146-ac86-d6c58c8995e4
feature: Customers, Configuration, Security
TQID: https://experienceleague.adobe.com/yzGC0T8unOSE-sZkE4PRHM6xMVX68qD6fARb-OSUB0U
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: ba9e5be9-7de1-4f71-a5d2-baead0e425eeid: bd989d82-1e15-4534-88db-f1f51dd77ffaid: d1e21356-0064-4f48-9089-16e3f0dbd2a6id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: d095671a-1355-40aa-8b5f-06c33c68080bid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 393
ht-degree: 0%

---

# 重置客户密码

客户通常通过单击&#x200B;_[!UICONTROL Forgot Your Password?]_从店面重置密码。 但是，存储管理员可以从管理员启动密码重置或强制登录。

| 函数 | 描述 |
| --- | --- |
| 重置密码 | 密码重置电子邮件将直接发送到客户的电子邮件帐户。 商店管理员无法获得对客户密码的访问权限。 |
| 强制登录 | 撤销与客户帐户关联的OAuth访问令牌。 它只能用于已分配OAuth令牌的客户帐户，作为Web API [集成](../systems/integrations.md)的一部分。 要了解更多信息，请参阅开发人员文档中的[基于OAuth的身份验证](https://developer.adobe.com/commerce/webapi/get-started/authentication/gs-authentication-oauth/)。 <br/><br/>从店面或管理员创建的标准客户帐户没有OAuth令牌。 |

{style="table-layout:auto"}

## 从店面重置密码

1. 在登录页面上，客户单击&#x200B;**[!UICONTROL Forgot Your Password?]**。

1. 出现提示时，输入与其帐户关联的&#x200B;**[!UICONTROL Email Address]**&#x200B;并单击&#x200B;**[!UICONTROL Reset My Password]**。

   ![忘记密码](assets/forgot-password.png){width="600" zoomable="yes"}

   >[!INFO]
   >
   >如果输入的电子邮件地址与帐户关联的电子邮件地址匹配，则客户会收到“密码重置确认”电子邮件，其中包含用于重置其密码的链接。

1. 当电子邮件到达时，客户单击&#x200B;_重置密码_&#x200B;链接，然后在出现提示时输入其&#x200B;**[!UICONTROL New Password]**。

1. 再次输入以确认并单击&#x200B;**[!UICONTROL Reset Password]**。

   >[!IMPORTANT]
   >
   >新密码长度必须是6个或更多字符，且不能包含空格。 当他们收到密码已更新的确认信息时，可以使用新密码登录到他们的帐户。 默认情况下，_重置密码_&#x200B;链接的有效时间为24小时。

## 从管理员重置密码

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Customers]** > **[!UICONTROL All Customers]**。

1. 在网格中查找客户帐户，然后单击&#x200B;_操作_&#x200B;列中的&#x200B;**[!UICONTROL Edit]**。

1. 在页面顶部的选项集中，单击&#x200B;**[!UICONTROL Reset Password]**。

   在[配置](../configuration-reference/customers/customer-configuration.md)主题中设置了一小时内允许的密码重置请求数。

## 撤销客户的OAuth令牌

>[!IMPORTANT]
>
>除非您完全了解API身份验证，否则不要继续。

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Customers]** > **[!UICONTROL All Customers]**。

1. 在网格中查找客户帐户，然后单击&#x200B;_操作_&#x200B;列中的&#x200B;**[!UICONTROL Edit]**。

1. 在页面顶部的选项集中，单击&#x200B;**[!UICONTROL Force Sign In]**。

1. 提示确认时，单击&#x200B;**确定**。

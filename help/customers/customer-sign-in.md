---
title: 客户登录
description: 店面中的客户登录功能允许轻松访问客户的帐户。
exl-id: eadcc15a-a052-4213-a818-d5b248d974d2
feature: Customers, Storefront
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 0%

---

# 客户登录

客户可以从您商店的每个页面轻松访问其帐户。 根据 [配置](../customers/account-options-new.md)，则客户可能会被重定向到其帐户仪表板，或在登录到其帐户后继续购物。

如果 [验证码](../systems/security-captcha.md) 在配置中启用，人员必须正确完成一项测试来验证他们是否为人类，然后才能访问其帐户。

当客户忘记密码时，会向与该帐户关联的电子邮件地址发送重置链接。 此 [密码选项](../customers/password-options.md) 配置控制客户尝试登录的体验：

- 客户可以尝试输入密码的次数
- 两次尝试之间的分钟数
- 帐户锁定前的总尝试次数
- 锁定的长度

![店面页眉上的登录链接](assets/storefront-sign-in-create-account.png){width="700" zoomable="yes"}

## 登录到客户帐户

1. 在商店的标题中，客户单击 **[!UICONTROL Sign in]**.

   ![客户登录](assets/login.png){width="700" zoomable="yes"}

1. 进入他们的 **[!UICONTROL Email]** 地址和 **[!UICONTROL Password]**.

1. 点击次数 **[!UICONTROL Sign in]**.

   >[!IMPORTANT]
   >
   >如果他们忘记了自己的密码，客户可以单击 **[!UICONTROL Forgot Your Password?]** 并遵循 [说明](../customers/password-reset.md) 以重置密码。

## 在客户登录后将重定向设置为帐户仪表板

您可以将商店配置为在客户登录后将其重定向到帐户信息板，或让他们继续购物。

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中，展开 **[!UICONTROL Customers]** 并选择 **[!UICONTROL Customer Configuration]**.

1. 展开 **[!UICONTROL Login Options]** 部分。

1. 设置 **[!UICONTROL Redirect Customer to Account Dashboard after Logging in]** 更改为以下任一项：

   - `Yes`  — 当客户登录其帐户时，将显示帐户仪表板。
   - `No`  — 客户在登录到其帐户后可以继续购物。

1. 完成后，单击 **[!UICONTROL Save Config]**.

## 使用Amazon登录

对于配置了的商店 [!DNL Amazon Pay] 和 [!DNL Login with Amazon] 集成，客户可以登录到其Amazon购买者帐户。

1. 在商店的标题中，客户单击 **[!UICONTROL Sign in]**.

1. 点击次数 **[!UICONTROL Login with Amazon]**.

   ![使用Amazon登录](assets/amazon-pay.png){width="700" zoomable="yes"}

1. 提示登录时，客户输入 **[!UICONTROL email address]** 和 **[!UICONTROL password]** 他们的Amazon买家账户上。

   ![输入Amazon凭据](assets/amazon-popup1.png){width="700" zoomable="yes"}

1. 要授予Amazon在处理购买时从其帐户与应用商店共享以下信息的权限，请单击 **确定**.

   - 名称
   - 电子邮件地址
   - 配送地址

   ![授予共享数据的权限](assets/amazon-popup2.png){width="700" zoomable="yes"}

## 注销客户帐户

1. 在右上角旁边的  _[!UICONTROL Welcome, Customer Name!]_，客户单击&#x200B;**[!UICONTROL v]**菜单选择器。

1. 选择 **[!UICONTROL Sign Out]**.

注销后，客户将被重定向到主页。

---
title: 浏览器功能检测
description: 了解如何配置浏览器功能检测，以及在需要更改客户的浏览器设置时显示通知。
exl-id: 16caab8b-3ba5-43a1-a6f0-7c1e921be132
role: Admin
feature: Configuration, Security
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '254'
ht-degree: 0%

---

# 浏览器功能检测

与Internet上的大多数网站和应用程序一样，Adobe Commerce和Magento Open Source要求访客的浏览器允许Cookie和JavaScript进行完整操作。 但是，有时，用户的浏览器会被设置为最高的隐私设置，这样会同时阻止Cookie和JavaScript。 可以将您的商店配置为测试每位访客浏览器的功能，并在需要更改设置时显示通知。

- 如果浏览器的隐私设置不允许Cookie，您可以将系统配置为自动将它们重定向到 [启用Cookie](../content-design/pages.md#enable-cookies) 页面，该页面介绍了如何在大多数浏览器中进行建议的设置。
- 如果浏览器的隐私设置不允许JavaScript，您可以将系统配置为在每个页面的标头上方显示以下消息。

有关技术信息，请参阅 [支持的浏览器](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/system-requirements.html#supported-browsers) 在 _安装指南_.

## 配置浏览器功能检测

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧的面板中，位于 _[!UICONTROL General]_，选择&#x200B;**[!UICONTROL Web]**.

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Browser Capabilities Detection]** 部分并执行以下操作：

   - 要显示说明如何将浏览器配置为允许Cookie的说明，请设置 **[!UICONTROL Redirect to CMS-page if Cookies are Disabled]** 到 `Yes`.

   - 要在用户浏览器中禁用JavaScript时在标题上方显示横幅，请设置 **[!UICONTROL Show Notice if JavaScript is Disabled]** 到 `Yes`.

   - 要在用户浏览器中禁用本地存储时在标题上方显示横幅，请设置 **[!UICONTROL Show Notice if Local Storage is Disabled]** 到 `Yes`.

   ![常规配置 — Web浏览器功能检测](../configuration-reference/general/assets/web-browser-capabilities-detection.png){width="600" zoomable="yes"}

1. 完成后，单击 **[!UICONTROL Save Config]**.

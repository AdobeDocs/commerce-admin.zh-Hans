---
title: 浏览器功能检测
description: 了解如何配置浏览器功能检测，以及在需要更改客户的浏览器设置时显示通知。
exl-id: 16caab8b-3ba5-43a1-a6f0-7c1e921be132
role: Admin
feature: Configuration, Security
badgePaas: label="仅限PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="仅适用于云项目（Adobe管理的PaaS基础架构）和内部部署项目上的Adobe Commerce 。"
TQID: https://experienceleague.adobe.com/zPxdplYIYblw6-tsDvxEmvKfAx-2M6opb6qjX7YL1I4
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
  - id: f42e0a1a-0d79-488d-a83f-f2c30672b137
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 285
ht-degree: 0%

---

# 浏览器功能检测

与Internet上的大多数网站和应用程序一样，Adobe Commerce和Magento Open Source要求访客的浏览器允许Cookie和JavaScript进行完整操作。 但是，有时，用户的浏览器会被设置为最高的隐私设置，这样会同时阻止Cookie和JavaScript。 可以将您的商店配置为测试每位访客浏览器的功能，并在需要更改设置时显示通知。

- 如果浏览器的隐私设置不允许Cookie，您可以将系统配置为自动将它们重定向到[启用Cookie](../content-design/pages.md#enable-cookies)页面，该页面介绍了如何在大多数浏览器中进行推荐的设置。
- 如果浏览器的隐私设置不允许JavaScript，您可以将系统配置为在每个页面的标题上方显示以下消息。

有关技术信息，请参阅&#x200B;_安装指南_&#x200B;中的[支持的浏览器](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/system-requirements.html#supported-browsers)。

## 配置浏览器功能检测

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧&#x200B;_[!UICONTROL General]_&#x200B;下的面板中，选择&#x200B;**[!UICONTROL Web]**。

1. 展开&#x200B;**[!UICONTROL Browser Capabilities Detection]**&#x200B;部分中的![扩展选择器](../assets/icon-display-expand.png)并执行以下操作：

   - 要显示说明如何将浏览器配置为允许Cookie的说明，请将&#x200B;**[!UICONTROL Redirect to CMS-page if Cookies are Disabled]**&#x200B;设置为`Yes`。

   - 要在用户浏览器中禁用JavaScript时显示标题上方的横幅，请将&#x200B;**[!UICONTROL Show Notice if JavaScript is Disabled]**&#x200B;设置为`Yes`。

   - 要在用户的浏览器中禁用本地存储时显示标头上方的横幅，请将&#x200B;**[!UICONTROL Show Notice if Local Storage is Disabled]**&#x200B;设置为`Yes`。

   ![常规配置 — Web浏览器功能检测](../configuration-reference/general/assets/web-browser-capabilities-detection.png){width="600" zoomable="yes"}

1. 完成后，单击&#x200B;**[!UICONTROL Save Config]**。

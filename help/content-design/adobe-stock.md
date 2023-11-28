---
title: Adobe Stock集成
description: 将Adobe Stock与您的集成 [!DNL Commerce] 实例访问，以便在您的商店中使用的无数媒体资产。
exl-id: 0f399ea7-5726-476c-a945-c37e44a9ea55
feature: CMS, Media, Configuration, Integration
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 0%

---

# Adobe Stock集成

要访问要在商店中使用的无数媒体资产，请集成 [Adobe Stock][adobe-stock] 替换为 [!UICONTROL Commerce].

![Adobe Stock搜索结果](./assets/adobe-stock-search-grid.png){width="700" zoomable="yes"}

Adobe Stock服务为企业提供了数百万张高质量、精选且免版税的照片、矢量、插图、视频、模板和3D资产，供其所有创意项目使用。 [!DNL Commerce] 用户能够快速查找、预览和许可Adobe Stock资源。 用户还可以将它们保存到 [媒体存储][media-storage]，无需离开管理员工作区。

## 先决条件

此集成需要：

- An [Adobe Developer][dev-console] 帐户
- Adobe Commerce或Magento Open Source，2.3.4或更高版本

许可Adobe Stock映像需要：

- An [Adobe帐户][adobe-signin]
- 付费 [Adobe Stock][adobe-stock] 与帐户关联的计划

## 集成 [!DNL Commerce] 和Adobe Stock

为Adobe Commerce配置Adobe Stock集成分为两步：

1. [创建adobe.developer集成](#create-an-adobe-developer-integration) 生成API密钥
1. [在商务管理中配置Adobe Stock集成](#configure-the-adobe-stock-integration)

### 创建Adobe Developer集成

1. 导航至 [Adobe Developer控制台][dev-console].

1. 下 _[!UICONTROL Quick Start]_，单击&#x200B;**[!UICONTROL Create new project]**.

1. 在 _[!UICONTROL Project overview]_阻止，单击&#x200B;**[!UICONTROL Add API]**.

1. 选择 **[!UICONTROL Adobe Stock]** 从集成列表中，单击 **[!UICONTROL Next]**.

1. 选择OAuth 2.0 **[!UICONTROL Web App]**.

1. 指定 **[!UICONTROL redirect URI]**.

   默认重定向URI采用格式 `${HOST}/${ADMIN_URI}/adobe_ims/oauth/callback/`，例如 `https://store.myshop.com/admin_hgkq1l/adobe_ims/oauth/callback/`，其中：

   - `${HOST}` 是您的 [!DNL Commerce] 完全限定的域名(例如， `https://store.myshop.com`)。
   - `${ADMIN_URI}` 是您的 [!DNL Commerce] 管理员URI(如 `admin_hgkq1l`)，可以通过运行 `magento info:adminuri`.

1. 指定 **[!UICONTROL Redirect URI pattern]**，这与您的重定向URI相同，但有两个区别：

   - 任何句点(`.`)必须使用两个反斜杠(`\\`)。
   - 添加 `.*` 到模式的尽头。

   使用上一个默认重定向URI中的示例，它是 `https://store\\.myshop\\.com/admin_hgkq1l/adobe_ims/oauth/callback/.*`.

1. 单击 **[!UICONTROL Next]**.

1. 查看可用的范围，然后单击 **[!UICONTROL Save configured API]**.

1. 在后续页面上，复制 **[!UICONTROL Client ID]** （API密钥）和 **[!UICONTROL Client secret]**.

   此信息将在下一部分的步骤中使用。

### 配置Adobe Stock集成

要在中设置系统配置，请执行以下操作 [!DNL Commerce] 管理员，使用 _API密钥_ 和 _客户端密码_ 在中生成 [上一节][create-integration].

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中，展开 **[!UICONTROL Advanced]** 并选择 **[!UICONTROL System]**.

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) **[!UICONTROL Adobe Stock Integration]** 并执行以下操作：

   - 设置 **[!UICONTROL Enabled Adobe Stock]** 到 `Yes`.

   - 输入您的 **[!UICONTROL API Key (Client ID)]**.

   - 输入您的 **[!UICONTROL Client Secret]**.

   - 单击 **[!UICONTROL Test Connection]** 来验证您的密钥。

   ![高级配置 — Adobe Stock集成](./assets/system-adobe-stock-integration.png){width="600" zoomable="yes"}

   给验证几秒钟。 如果您的凭据有效，您应该会看到绿色内容 _连接成功！_ 消息。

1. 完成后，单击 **[!UICONTROL Save Config]**.

[adobe-stock]: https://stock.adobe.com
[adobe-signin]: https://helpx.adobe.com/manage-account/using/access-adobe-id-account.html
[media-storage]: media-storage.md
[dev-console]: https://developer.adobe.com/console/home
[create-integration]: #create-an-adobeio-integration

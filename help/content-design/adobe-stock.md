---
title: Adobe Stock集成
description: 将Adobe Stock与您的 [!DNL Commerce] 实例集成，以访问要在商店中使用的无数媒体资源。
exl-id: 0f399ea7-5726-476c-a945-c37e44a9ea55
feature: CMS, Media, Configuration, Integration
badgePaas: label="仅限PaaS" type="Informative" url="https://experienceleague.adobe.com/zh-hans/docs/commerce/user-guides/product-solutions" tooltip="仅适用于云项目(Adobe管理的PaaS基础架构)和内部部署项目上的Adobe Commerce 。"
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '397'
ht-degree: 0%

---

# Adobe Stock集成

若要访问要在商店中使用的无数媒体资源，请将[Adobe Stock][adobe-stock]与[!UICONTROL Commerce]集成。

![Adobe Stock搜索结果](./assets/adobe-stock-search-grid.png){width="700" zoomable="yes"}

Adobe Stock服务为企业提供了数百万张高质量、精选且免版税的照片、矢量、插图、视频、模板和3D资产，供其所有创意项目使用。 [!DNL Commerce]用户能够快速查找、预览和许可Adobe Stock资源。 用户还可以将它们保存到[媒体存储](./media-storage.md)，所有这些操作无需离开管理员工作区。

## 先决条件

此集成需要：

- [Adobe Developer][dev-console]帐户
- Adobe Commerce或Magento Open Source，2.3.4或更高版本

许可Adobe Stock映像需要：

- [Adobe帐户][adobe-signin]
- 与该帐户关联的付费[Adobe Stock][adobe-stock]计划

## 集成[!DNL Commerce]和Adobe Stock

为Adobe Commerce配置Adobe Stock集成分为两步：

1. [创建adobe.developer集成](#create-an-adobe-developer-integration)以生成API密钥
1. [在Commerce管理中配置Adobe Stock集成](#configure-the-adobe-stock-integration)

### 创建Adobe Developer集成

1. 导航到[Adobe Developer Console][dev-console]。

1. 在&#x200B;_[!UICONTROL Quick Start]_&#x200B;下，单击&#x200B;**[!UICONTROL Create new project]**。

1. 在&#x200B;_[!UICONTROL Project overview]_&#x200B;块中，单击&#x200B;**[!UICONTROL Add API]**。

1. 从集成列表中选择&#x200B;**[!UICONTROL Adobe Stock]**&#x200B;并单击&#x200B;**[!UICONTROL Next]**。

1. 选择OAuth 2.0 **[!UICONTROL Web App]**。

1. 指定&#x200B;**[!UICONTROL redirect URI]**。

   默认重定向URI采用`${HOST}/${ADMIN_URI}/adobe_ims/oauth/callback/`格式，如`https://store.myshop.com/admin_hgkq1l/adobe_ims/oauth/callback/`，其中：

   - `${HOST}`是您的[!DNL Commerce]完全限定的域名（例如，`https://store.myshop.com`）。
   - `${ADMIN_URI}`是您的[!DNL Commerce]管理员URI（如`admin_hgkq1l`），可以通过运行`magento info:adminuri`来检索该URI。

1. 指定&#x200B;**[!UICONTROL Redirect URI pattern]**，它与您的重定向URI相同，但有两个区别：

   - 任何句点(`.`)都必须使用两个反斜杠(`\\`)进行转义。
   - 将`.*`添加到模式的结尾。

   使用上一个默认重定向URI中的示例，它将为`https://store\\.myshop\\.com/admin_hgkq1l/adobe_ims/oauth/callback/.*`。

1. 单击&#x200B;**[!UICONTROL Next]**。

1. 查看可用的作用域并单击&#x200B;**[!UICONTROL Save configured API]**。

1. 在接下来的页面上，复制您的&#x200B;**[!UICONTROL Client ID]** （API密钥）和&#x200B;**[!UICONTROL Client secret]**。

   此信息将在下一部分的步骤中使用。

### 配置Adobe Stock集成

要在[!DNL Commerce]管理员中设置系统配置，请使用[上一节][create-integration]中生成的&#x200B;_API密钥_&#x200B;和&#x200B;_客户端密钥_。

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧面板中，展开&#x200B;**[!UICONTROL Advanced]**&#x200B;并选择&#x200B;**[!UICONTROL System]**。

1. 展开![扩展选择器](../assets/icon-display-expand.png) **[!UICONTROL Adobe Stock Integration]**&#x200B;并执行以下操作：

   - 将&#x200B;**[!UICONTROL Enabled Adobe Stock]**&#x200B;设置为`Yes`。

   - 输入您的&#x200B;**[!UICONTROL API Key (Client ID)]**。

   - 输入您的&#x200B;**[!UICONTROL Client Secret]**。

   - 单击&#x200B;**[!UICONTROL Test Connection]**&#x200B;验证密钥。

   ![高级配置 — Adobe Stock集成](./assets/system-adobe-stock-integration.png){width="600" zoomable="yes"}

   给验证几秒钟。 如果凭据有效，您应会看到绿色的&#x200B;_连接成功！_&#x200B;消息。

1. 完成后，单击&#x200B;**[!UICONTROL Save Config]**。

[adobe-stock]: https://stock.adobe.com
[adobe-signin]: https://helpx.adobe.com/cn/manage-account/using/access-adobe-id-account.html
[dev-console]: https://developer.adobe.com/console/home
[create-integration]: #create-an-adobeio-integration

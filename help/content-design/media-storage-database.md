---
title: 使用媒体数据库
description: 了解如何使用媒体数据库存储 [!DNL Commerce] 媒体文件。
exl-id: b59349fb-0cb6-4812-a126-6e0d8d37564f
feature: Page Content, Media, Configuration
level: Experienced
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 0%

---

# 使用媒体数据库

>[!IMPORTANT]
>
>自Adobe Commerce和Magento Open Source2.4.3起，数据库媒体存储方法已弃用。

默认情况下，[!DNL Commerce]实例的所有图像、编译的CSS文件和编译的JavaScript文件都存储在Web服务器上的文件系统中。 您可以选择将这些文件存储在数据库服务器的数据库中。 此方法的一个优点是在Web服务器文件系统和数据库之间自动同步和反向同步。 您可以使用默认数据库存储介质或创建介质。 要将新创建的数据库用作媒体存储，必须将有关该数据库及其访问凭据的信息添加到`env.php`文件中。

## 数据库工作流

1. **浏览器请求媒体** — 商店中的页面会在客户的浏览器中打开，浏览器会请求HTML中指定的媒体。

1. **系统在文件系统中查找介质** — 系统在文件系统中搜索介质，如果找到，则将其传递给浏览器。

1. **系统在数据库**&#x200B;中查找媒体 — 如果在文件系统中未找到媒体，则会向配置中指定的数据库发送对媒体的请求。

1. **系统在数据库中定位媒体** - PHP脚本将文件从数据库传输到文件系统，并发送到客户的浏览器。 浏览器对媒体的请求会触发脚本运行，如下所示：

   - 如果为[!DNL Commerce]启用了Web服务器[重写](../merchandising-promotions/url-rewrite.md)，并且服务器支持该重写，则只有在文件系统中找不到所请求的媒体时，PHP脚本才会运行。
   - 如果[!DNL Commerce]禁用了Web服务器重写，或者服务器不支持重写，则即使文件系统中有所需的介质，PHP脚本仍会运行。

## 使用数据库进行媒体存储

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧面板中，展开&#x200B;**[!UICONTROL Advanced]**&#x200B;并选择&#x200B;**[!UICONTROL System]**。

1. 在左上角，将&#x200B;**[!UICONTROL Store View]**&#x200B;设置为`Default Config`以在全局级别应用配置。

1. 展开&#x200B;**[!UICONTROL Storage Configuration for Media]**&#x200B;部分中的![扩展选择器](../assets/icon-display-expand.png)并执行以下操作：

   ![高级配置 — 媒体的存储配置](./assets/database-storage-deprecated.png){width="600" zoomable="yes"}

   - 将&#x200B;**[!UICONTROL Media Storage]**&#x200B;设置为`Database`。

   - 将&#x200B;**[!UICONTROL Select Media Database]**&#x200B;设置为要使用的数据库。

   - 要将现有媒体传输到新选择的数据库中，请单击&#x200B;**[!UICONTROL Synchronize]**。

   - 输入&#x200B;**[!UICONTROL Environment Update Time]**（以秒为单位）。

1. 完成后，单击&#x200B;**[!UICONTROL Save Config]**。

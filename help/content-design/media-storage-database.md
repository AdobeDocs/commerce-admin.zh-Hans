---
title: 使用媒体数据库
description: 了解如何使用媒体数据库来存储 [!DNL Commerce] 媒体文件。
exl-id: b59349fb-0cb6-4812-a126-6e0d8d37564f
feature: Page Content, Media, Configuration
level: Experienced
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 0%

---

# 使用媒体数据库

>[!IMPORTANT]
>
>自Adobe Commerce和Magento Open Source2.4.3起，数据库媒体存储方法已弃用。

默认情况下，所有图像、编译的CSS文件和编译的JavaScript文件 [!DNL Commerce] 实例存储在Web服务器上的文件系统中。 您可以选择将这些文件存储在数据库服务器的数据库中。 此方法的一个优点是在Web服务器文件系统和数据库之间自动同步和反向同步。 您可以使用默认数据库存储介质或创建介质。 要将新创建的数据库用作介质存储，您必须将有关该数据库及其访问凭据的信息添加到 `env.php` 文件。

## 数据库工作流

1. **浏览器请求媒体**  — 应用商店中的页面将在客户的浏览器中打开，浏览器将请求HTML中指定的介质。

1. **系统在文件系统中查找介质**  — 系统在文件系统中搜索介质，如果找到，则将其传递给浏览器。

1. **系统在数据库中定位媒体**  — 如果在文件系统中找不到介质，则会向配置中指定的数据库发送介质请求。

1. **系统在数据库中定位媒体** - PHP脚本将文件从数据库传输到文件系统，并发送到客户的浏览器。 浏览器对媒体的请求会触发脚本运行，如下所示：

   - 如果Web服务器 [重写](../merchandising-promotions/url-rewrite.md) 已启用 [!DNL Commerce] 并且受服务器支持，只有在文件系统中找不到所请求的媒体时，PHP脚本才会运行。
   - 如果禁用Web服务器重写 [!DNL Commerce]或者服务器不支持的，PHP脚本仍会运行，即使文件系统中有所需的介质可用。

## 使用数据库进行媒体存储

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中，展开 **[!UICONTROL Advanced]** 并选择 **[!UICONTROL System]**.

1. 在左上角，设置 **[!UICONTROL Store View]** 到 `Default Config` 以在全局级别应用配置。

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Storage Configuration for Media]** 部分并执行以下操作：

   ![高级配置 — 媒体的存储配置](./assets/database-storage-deprecated.png){width="600" zoomable="yes"}

   - 设置 **[!UICONTROL Media Storage]** 到 `Database`.

   - 设置 **[!UICONTROL Select Media Database]** 到要使用的数据库。

   - 要将现有介质传输到新选择的数据库中，请单击 **[!UICONTROL Synchronize]**.

   - 输入 **[!UICONTROL Environment Update Time]** 以秒为单位。

1. 完成后，单击 **[!UICONTROL Save Config]**.

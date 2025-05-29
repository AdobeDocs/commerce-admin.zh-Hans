---
title: 站点地图
description: 了解如何配置站点地图以索引Commerce站点的所有页面和图像。
exl-id: 48c975ae-b088-4e52-80cf-cb19c2b9b00f
feature: Merchandising, Storefront, Search
badgePaas: label="仅限PaaS" type="Informative" url="https://experienceleague.adobe.com/zh-hans/docs/commerce/user-guides/product-solutions" tooltip="仅适用于云项目(Adobe管理的PaaS基础架构)和内部部署项目上的Adobe Commerce 。"
source-git-commit: 7e28081ef2723d4113b957edede6a8e13612ad2f
workflow-type: tm+mt
source-wordcount: '1209'
ht-degree: 0%

---

# 站点地图

>[!TIP]
>
>对于Adobe Commerce as a Cloud Service，请参阅Commerce Storefront文档中的[SEO准则](https://experienceleague.adobe.com/developer/commerce/storefront/setup/seo/indexing/?lang=zh-Hans)

网站地图改进了搜索引擎为存储编制索引的方式，并设计为可查找可能被网络爬虫忽略的页面。 可以将站点地图配置为为所有页面和图像编制索引。

启用后，Commerce会创建一个名为`sitemap.xml`的文件，该文件将保存到您指定的安装位置。 利用配置，可设置更新频率以及每种内容类型的优先级。 您的网站地图应按照网站内容更改频率进行更新，更改频率可以是每日、每周或每月。

当您的网站处于开发状态时，您可能会在`robots.txt`文件中为Web爬网程序提供说明，以避免对网站编制索引。 然后，在启动之前，您可以更改相关说明，以允许为网站编制索引。

有关技术信息，请参阅&#x200B;_Commerce on Cloud Infrastructure指南_&#x200B;中的[Add sitemap and robots.txt][1]。

![站点地图网格](./assets/marketing-sitemap-grid-generated.png){width="700" zoomable="yes"}

## 步骤1. 配置站点地图

完成[XML站点地图配置](#site-map-configuration)以确定包含的内容以及更新站点地图的频率。

## 步骤2. 生成网站地图

1. 在&#x200B;_管理员_&#x200B;菜单上，转到&#x200B;**[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL Site Map]**。

1. 单击&#x200B;**[!UICONTROL Add Site Map]**。

   ![站点地图网格](./assets/marketing-sitemap.png){width="700" zoomable="yes"}

1. 输入网站地图&#x200B;**[!UICONTROL Filename]**。 例如： `sitemap.xml`

1. 输入&#x200B;**[!UICONTROL Path]**&#x200B;以确定站点地图文件在服务器上的存放位置。 确保路径可写。

   - `/sitemap/` — 将站点地图文件放置在名为&#x200B;_站点地图_&#x200B;的目录中。

   - `/` — 将站点地图文件放置在Commerce安装的基本路径或根目录下。

   ![新站点地图](./assets/marketing-sitemap-new.png){width="600" zoomable="yes"}

1. 完成后，单击&#x200B;**[!UICONTROL Save & Generate]**。

   站点地图可能需要几分钟才能显示在网格中。

## 步骤3. 配置和启用robots.txt （可选）

完成[搜索引擎机器人](seo-overview.md#search-engine-robots)配置，并指示搜索引擎爬取要编制索引的网站部分。

## 步骤4. 将您的网站地图提交到搜索引擎

通过提供指向Commerce安装中的`sitemap.xml`文件的链接，您可以将站点地图提交到其他搜索引擎。 要复制链接，请执行以下操作：

1. 在&#x200B;_网站地图_&#x200B;列表中，右键单击&#x200B;**[!UICONTROL Link for Google]**&#x200B;列中的URL。

1. 在菜单上，选择&#x200B;**[!UICONTROL Copy Link Address]**。

有关更多信息，请参阅特定搜索引擎的说明。 以下是指向两个热门搜索引擎的说明的链接：

- [Google][2]
- [Microsoft® Bing][3]

## 步骤5：恢复先前的自动机指令（可选）

您现在可以恢复原始（默认）限制。

## 管理多个网站的站点地图和robots.txt

如果您拥有多个网站，则可以简化创建和提交站点地图的过程。 只需[创建](#site-map-configuration)一个或多个包含所有已验证存储的URL的站点地图，并将站点地图保存到单个位置。 必须在[Google搜索控制台](https://support.google.com/webmasters/answer/7451001)中验证所有站点。

要为多存储实例创建站点地图，请执行以下操作：

1. 在网站的根目录下创建名为`sitemaps`的文件夹，然后为每个域创建子文件夹：

       /sitemaps/domain_1/
       /sitemaps/domain_2/
   
1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL Site Map]**。

1. 创建或编辑每个商店的站点地图列表，并将&#x200B;**[!UICONTROL Path]**&#x200B;设置为您为商店创建的列表：

   `/sitemaps/domain_1/`
   `/sitemaps/domain_2/`

1. 如果需要，请更新robots.txt文件。

   要确保将搜索引擎蜘蛛正确定向到新的sitemap，可以更新或创建robots.txt文件。 在顶部添加以下行。

       网站站点地图
       站点地图： https://www.domain_1.com/sitemaps/domain_1/sitemap.xml
       站点地图： https://www.domain_2.com/sitemaps/domain_2/sitemap.xml
   
>[!NOTE]
>
>如果您的站点使用[Apache](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/web-server/apache.html?lang=zh-Hans) Web服务器引擎，则应更新网站根目录中的[`.htaccess`](https://httpd.apache.org/docs/current/howto/htaccess.html)文件，以将任何其他Sitemap请求定向到适当的位置。

## 列描述

| 列 | 描述 |
|------|-----------|
| [!UICONTROL ID] | 当前站点地图的连续记录编号。 |
| [!UICONTROL Filename] | 站点地图的文件名。 |
| [!UICONTROL Path] | 站点地图在服务器上的位置。 例如： <br/>`/sitemap/` — 将站点地图文件放置在名为&#x200B;_Sitemap_&#x200B;的目录中，该目录比Commerce安装的根目录低一个级别。 <br/>`/` — 将站点地图文件放置在Commerce安装的基本路径或根目录下。 |
| [!UICONTROL Link for Google] | 将提交到Google和其他搜索引擎的站点地图的URL。 |
| [!UICONTROL Last Generated] | 指示上次生成网站地图的日期和时间。 |
| [!UICONTROL Store View] | 应用站点地图的商店视图。 |
| [!UICONTROL Generate] | 重新生成站点地图。 |

{style="table-layout:auto"}

## 站点地图配置

您的网站地图应按照网站内容更改频率进行更新，更新频率可以是每日、每周或每月。 利用配置，可设置每种内容类型的频率和优先级。

### 步骤1. 设置内容更新的频率和优先级

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧面板中，展开&#x200B;**[!UICONTROL Catalog]**&#x200B;并选择&#x200B;**[!UICONTROL XML Sitemap]**。

1. 展开&#x200B;**[!UICONTROL Categories Options]**&#x200B;部分中的![扩展选择器](../assets/icon-display-expand.png)并执行以下操作：

   >[!NOTE]
   >
   >如果需要，请清除&#x200B;**[!UICONTROL Use system value]**&#x200B;复选框以更改这些设置。

   - 将&#x200B;**[!UICONTROL Frequency]**&#x200B;设置为以下项之一：

      - `Always`
      - `Hourly`
      - `Daily`
      - `Weekly`
      - `Monthly`
      - `Yearly`
      - `Never`

   - 对于&#x200B;**[!UICONTROL Priority]**，请输入一个介于`0.0`和`1.0`之间的值。 零的优先级最低。

   ![XML Sitemap — 类别选项](../configuration-reference/catalog/assets/xml-sitemap-categories-options.png){width="600" zoomable="yes"}

   有关这些选项的详细列表，请参阅&#x200B;_配置引用_&#x200B;中的[类别选项](../configuration-reference/catalog/xml-sitemap.md#categories-options)。

1. 展开![扩展选择器](../assets/icon-display-expand.png) **[!UICONTROL Products Options]**&#x200B;部分并根据需要完成&#x200B;**[!UICONTROL Frequency]**&#x200B;和&#x200B;**[!UICONTROL Priority]**&#x200B;设置。

   有关这些选项的详细列表，请参阅&#x200B;_配置引用_&#x200B;中的[产品选项](../configuration-reference/catalog/xml-sitemap.md#products-options)。

1. 要确定站点地图中包含图像的范围，请将&#x200B;**[!UICONTROL Add Images into Sitemap]**&#x200B;设置为以下任一项：

   - `None`
   - `Base Only`
   - `All`

   ![目录配置 — XML Sitemap产品](../configuration-reference/catalog/assets/xml-sitemap-products-options.png){width="600" zoomable="yes"}

1. 展开![扩展选择器](../assets/icon-display-expand.png) **[!UICONTROL CMS Pages Options]**&#x200B;部分并根据需要完成&#x200B;**[!UICONTROL Frequency]**&#x200B;和&#x200B;**[!UICONTROL Priority]**&#x200B;设置。

   ![目录配置 — XML Sitemap CMS页面](../configuration-reference/catalog/assets/xml-sitemap-cms-pages-options.png){width="600" zoomable="yes"}

   有关这些选项的详细列表，请参阅&#x200B;_配置引用_&#x200B;中的[CMS页面选项](../configuration-reference/catalog/xml-sitemap.md#cms-pages-options)。

1. 展开![扩展选择器](../assets/icon-display-expand.png) **[!UICONTROL Store Url Options]**&#x200B;部分并根据需要完成&#x200B;**[!UICONTROL Frequency]**&#x200B;和&#x200B;**[!UICONTROL Priority]**&#x200B;设置。

   ![目录配置 — XML站点地图存储URL](./assets/xml-sitemap.png){width="600" zoomable="yes"}

   有关这些选项的详细列表，请参阅&#x200B;_配置引用_&#x200B;中的[存储URL选项](../configuration-reference/catalog/xml-sitemap.md#store-url-options)。

1. 完成后，单击&#x200B;**[!UICONTROL Save Config]**。

### 步骤2. 完成生成设置

1. 展开&#x200B;**[!UICONTROL Generation Settings]**&#x200B;部分的![扩展选择器](../assets/icon-display-expand.png)。

   如果需要，请清除&#x200B;**使用系统值**&#x200B;复选框以更改这些设置。

   ![目录配置 — XML站点地图生成设置](../configuration-reference/catalog/assets/xml-sitemap-generation-settings.png){width="600" zoomable="yes"}

   有关这些选项的详细列表，请参阅&#x200B;_配置引用_&#x200B;中的[生成设置](../configuration-reference/catalog/xml-sitemap.md#generation-settings)。

1. 要生成站点地图，请将&#x200B;**[!UICONTROL Enabled]**&#x200B;设置为`Yes`并执行以下操作：

   - 将&#x200B;**[!UICONTROL Start Time]**&#x200B;设置为您希望站点地图更新的小时、分钟和秒。

   - 将&#x200B;**[!UICONTROL Frequency]**&#x200B;设置为以下项之一：

      - `Daily`
      - `Weekly`
      - `Monthly`

   - 对于&#x200B;**[!UICONTROL Error Email Recipient]**，输入在站点地图更新期间发生错误时要接收通知的人员的电子邮件地址。

   - 将&#x200B;**[!UICONTROL Error Email Sender]**&#x200B;设置为显示为错误通知发送者的商店联系人。

   - 将&#x200B;**[!UICONTROL Error Email Template]**&#x200B;设置为用于错误通知的模板。

### 步骤3. 设置站点地图文件限制

1. 展开&#x200B;**[!UICONTROL Sitemap File Limits]**&#x200B;部分的![扩展选择器](../assets/icon-display-expand.png)。

   ![目录配置 — XML站点地图文件限制](../configuration-reference/catalog/assets/xml-sitemap-sitemap-file-limits.png){width="600" zoomable="yes"}

   有关这些选项的详细列表，请参阅&#x200B;_配置引用_&#x200B;中的[站点地图文件限制](../configuration-reference/catalog/xml-sitemap.md#sitemap-file-limits)。

1. 对于&#x200B;**[!UICONTROL Maximum No of URLs per File]**，请输入站点地图中可以包含的最大URL数。

   默认情况下，限制为50,000。

1. 对于&#x200B;**[!UICONTROL Maximum File Size]**，输入为站点地图分配的最大大小（以字节为单位）。

   默认大小为10,485,760字节。

### 步骤4. 设置搜索引擎提交设置

1. 展开&#x200B;**[!UICONTROL Search Engine Submission Settings]**&#x200B;部分的![扩展选择器](../assets/icon-display-expand.png)。

   ![目录配置 — XML Sitemap搜索引擎提交设置](../configuration-reference/catalog/assets/xml-sitemap-search-engine-submission-settings.png){width="600" zoomable="yes"}

1. 如果使用`robots.txt`文件向爬网网站的搜索引擎提供说明，请将&#x200B;**[!UICONTROL Enable Submission to Robots.txt]**&#x200B;设置为`Yes`。

1. 完成后，单击&#x200B;**[!UICONTROL Save Config]**。

[1]: https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure-store/robots-sitemap.html?lang=zh-Hans
[2]: https://support.google.com/webmasters/answer/183669?hl=en
[3]: https://www.bing.com/webmasters/help/Sitemaps-3b5cf6ed

---
title: 页面
description: 了解有关 [!DNL Commerce] 演示存储中包含的核心内容页面以及更改默认页面配置的详细信息。
exl-id: 4be7d3d6-ce36-42bc-9224-4804c3211f16
feature: Page Content, Configuration
badgePaas: label="仅限PaaS" type="Informative" url="https://experienceleague.adobe.com/zh-hans/docs/commerce/user-guides/product-solutions" tooltip="仅适用于云项目(Adobe管理的PaaS基础架构)和内部部署项目上的Adobe Commerce 。"
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '932'
ht-degree: 0%

---

# 页面

内容可以按照货架期来查看，就像商店中的任何产品一样。 您知道社交媒体内容的保质期不到24小时吗？ 您创建的内容的潜在存储期限可以帮助您确定将资源投入到何处。

保质期长的内容有时称为&#x200B;_常绿内容_。 常青内容的示例包括客户成功案例、_如何_&#x200B;说明以及常见问题解答(FAQ)。 相反，自然易腐的内容包括活动、行业新闻和新闻稿。

![示例Luma存储区中包含的“关于我们”页面](./assets/storefront-about-us.png){width="700" zoomable="yes"}

## 核心内容页面

[!DNL Commerce]演示存储包含核心内容页面的示例，可帮助您入门。 所有这些页面都可以修改以满足您的需求。 查看您商店中的以下页面，并确保内容传达您的消息、语音和品牌。

### 主页

演示[主页](../getting-started/storefront.md#home-page)页面包含一个横幅、一个图像轮播、多个带链接的静态块以及新产品列表。

### 隐私政策

应该使用您自己的信息更新商店[隐私策略](../getting-started/privacy-policy.md)页面。 作为最佳实践，您的隐私政策应向您的客户说明贵公司收集的信息类型及其使用方式。

### 404未找到

“404页面未找到”页面的命名依据是找不到页面时返回的响应代码。 URL重定向可减少此页面的显示次数。 但是，在必要的时候，您最好利用这个机会提供一些客户可能感兴趣的产品的链接。

### 访问被拒绝

{{b2b-feature}}

如果分配给公司用户的权限禁止访问页面，则会显示[拒绝访问](../b2b/account-company-roles-permissions.md)页面。

### 启用Cookie

当访问您网站的访客的浏览器中未启用Cookie时，会显示[启用Cookie](../getting-started/compliance-cookie-law.md)页面。 此页面提供了分步式的插图说明，用于为最受欢迎的浏览器启用Cookie。

### 服务不可用

[503服务不可用](../configuration-reference/general/general.md)页面是以服务器不可用时返回的响应代码命名的。

### 关于我们

“关于我们”页面将从您商店的页脚链接。 您可以包括图像、视频、新闻稿链接和公告。 示例页面右侧有一个图像，和一个用于指示页面结束的装饰性图像。

### 客户服务

“客户服务”页是页面层次结构中的另一个节点。 页面上的两个标题包含的内容，只有在客户单击标题时才会显示。

店面上的![客户服务页面](./assets/storefront-customer-service.png){width="700" zoomable="yes"}

## 配置默认页面

_默认页面_&#x200B;配置确定与[基本URL](../stores-purchase/store-urls.md)和相应的主页关联的登陆页面。 它还确定出现&#x200B;_页面未找到_&#x200B;错误时显示的页面，以及每个页面顶部是否显示[痕迹导航路径](../catalog/navigation-breadcrumb-trail.md)。

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧面板中的&#x200B;_[!UICONTROL General]_&#x200B;下，选择&#x200B;**[!UICONTROL Web]**。

1. 展开&#x200B;**[!UICONTROL Default Pages]**&#x200B;部分的![扩展选择器](../assets/icon-display-expand.png)。

   ![默认页面](./assets/web-default-pages.png){width="500" zoomable="yes"}

   | 字段 | [作用域](../getting-started/websites-stores-views.md#scope-settings) | 描述 |
   |--- |--- |--- |
   | [!UICONTROL Default Web URL] | 商店视图 | 指示与基本URL关联的登陆页面。 默认情况下，此字段设置为`cms`表示来自[!DNL Commerce]内容管理系统的页面。 您还可以使用其他类型的登陆页面，如博客。 例如，如果在`magento/blog`处的服务器上安装了博客，则可以输入文件夹名称`blog`作为页面选择的相对路径。 |
   | [!UICONTROL CMS Home Page] | 商店视图 | 要选择商店的主页，只需从列表中选择CMS页面即可。 默认情况下，CMS主页会列出您商店可用的所有CMS页面选择。 |
   | [!UICONTROL Default No-route URL] | 商店视图 | 包含发生`404 Page not Found`错误时要显示的默认页面的URL。 默认值为`cms/noroute/index`。 |
   | [!UICONTROL CMS No Route Page] | 商店视图 | 标识您希望在出现404页面未找到错误时显示的特定CMS页面。 默认页面为`404 Not Found`。 |
   | [!UICONTROL CMS No Cookies Page] | 商店视图 | 标识未为浏览器启用Cookie时显示的特定CMS页面。 本页介绍了为何使用Cookie，以及如何为每个浏览器启用它们。 默认页面为`Enable Cookies`。 |
   | [!UICONTROL Show Breadcrumbs for CMS Pages] | 商店视图 | 确定是否在目录中的所有CMS页面上显示痕迹导航路径。 选项： `Yes` / `No` |

   {style="table-layout:auto"}

1. 对于&#x200B;**[!UICONTROL Default Web URL]**，输入包含登陆页面的[!DNL Commerce]安装中文件夹的相对路径。

   默认设置`cms`表示来自[!DNL Commerce]内容管理系统的页面。

   >[!NOTE]
   >
   >对于特定商店视图，请清除&#x200B;_[!UICONTROL Default Web URL]_&#x200B;旁边的&#x200B;**[!UICONTROL Use Default]**&#x200B;复选框，以及任何其他要更改的默认设置。

1. 将&#x200B;**[!UICONTROL CMS Home Page]**&#x200B;设置为要用作主页的CMS页面。 其他创建的页面可用作主页，例如：

   - 欢迎使用独家在线商店
   - 奖励点数
   - 关于我们
   - 客户服务
   - 启用Cookie
   - 隐私政策
   - 公司：访问被拒绝

1. 对于&#x200B;**[!UICONTROL Default No-route URL]**，输入[!DNL Commerce]安装中文件夹的相对路径，在出现&#x200B;_404页面未找到_&#x200B;错误时，将重定向该页面。

   默认值为`cms/index/noRoute`。

1. 将&#x200B;**[!UICONTROL CMS No Route Page]**&#x200B;设置为发生&#x200B;_404页面未找到_&#x200B;错误时显示的CMS页面。

1. 将&#x200B;**[!UICONTROL CMS No Cookies Page]**&#x200B;设置为在浏览器中禁用Cookie时显示的CMS页面。 本页介绍了为何使用Cookie，以及如何为每个浏览器启用它们。 默认页面为`Enable Cookies`。

1. 如果希望痕迹导航跟踪显示在所有CMS页面的顶部，请将&#x200B;**[!UICONTROL Show Breadcrumbs for CMS Pages]**&#x200B;设置为`Yes`。

1. 完成后，单击&#x200B;**[!UICONTROL Save Config]**。

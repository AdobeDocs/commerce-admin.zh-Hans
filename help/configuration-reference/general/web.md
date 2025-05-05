---
title: '[!UICONTROL General] &amp；gt； [!UICONTROL Web]'
description: 查看Commerce管理员的[!UICONTROL General] &amp；gt； [!UICONTROL Web]页面上的配置设置。
exl-id: 1809b03a-a55c-41b4-947b-f66f4bd290a1
feature: Site Management, Configuration
source-git-commit: 5a4417373f6dc720e8e14f883c27348a475ec255
workflow-type: tm+mt
source-wordcount: '1793'
ht-degree: 0%

---

# [!UICONTROL General] > [!UICONTROL Web]

{{config}}

## [!UICONTROL URL Options]

![Web >常规选项](./assets/web-url-options.png)<!-- zoom -->

<!-- [URL Options configuration settings](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/site-store/store-urls) -->

| 字段 | 范围 | 描述 |
|  ---  |  ---  |  ---  |
| [!UICONTROL Add Store Code to URLs] | 全局 | 如果启用了Web服务器重写，则在URL中插入当前视图的存储代码。 选项： `Yes` / `No`。 <br />当此字段设置为`Yes`时，必须在浏览器URL中包含存储代码，以确保URL重写正确映射并且所有页面都成功打开。 这可避免&#x200B;_404页面未找到_&#x200B;错误。 |
| [!UICONTROL Auto-redirect to Base URL] | 商店视图 | （对于单商店设置）如果您的网站上存在断开的链接，会将流量重定向到基本URL，而不是重定向到显示“404页面未找到”消息的页面。 选项：` No` / `Yes (302 Found)` / `Yes (301 Moved Permanently)` <br />**_重要提示：_**&#x200B;请勿在多商店设置中使用自动重定向到基本URL。 |
| [!UICONTROL Catalog media URL format] | 全局 | 定义分配给产品和类别的[URL格式](../../catalog/catalog-urls.md)。 选项：每个图像变体的唯一哈希值（旧模式）将转换的文件名定义为唯一哈希值。 基于查询参数的图像优化根据查询参数定义了[图像优化](../../content-design/media-gallery-image-optimization.md)进程。 |

{style="table-layout:auto"}

## [!UICONTROL Search Engine Optimization]

![Web >搜索引擎优化](./assets/web-search-engine-optimization.png)<!-- zoom -->

<!-- [Search Engine Optimization configuration settings](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/seo/url-rewrites/url-rewrite) -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Use Web Server Rewrites] | 商店视图 | 基于PHP的系统通常在根文件夹中包含名为`index.php`的文件。 默认情况下，文件名显示在URL中根文件夹名称的后面。 启用此功能后，系统会忽略URL中的`index.php`。 此可用性最佳实践使每个URL更加简洁，并且不会影响性能或网站排名。 选项： `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Base URLs]

![Web >基本URL](./assets/web-base-urls.png)<!-- zoom -->

<!-- [Base URLS configuration settings](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/site-store/store-urls) -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Base URL] | 商店视图 | 未通过加密(SSL)渠道运行的Commerce根文件夹的完整地址。 URL必须以正斜杠结尾。 |
| [!UICONTROL Base Link URL] | 商店视图 | 用作基本URL占位符的标记标记。 |
| [!UICONTROL Base URL for Static View Files] | 商店视图 | 指向主题使用的静态文件(如css、字体、图像和JavaScript)位置的路径。 占位符用于表示基本URL。 如果Commerce安装具有多个具有相同文件夹结构的站点，则每个站点可以有不同的文件夹。 在输入静态视图文件的基本URL之前，将配置范围设置为正确的站点。 您还可以在Commerce安装之外指定文件夹。 |
| [!UICONTROL Base URL for User Media Files] | 商店视图 | 指向目录图像和其他媒体文件位置的路径。 占位符用于表示基本URL。 如果Commerce安装有多个具有相同文件夹结构的站点，则可以为每个站点使用不同的介质文件夹。 这使您能够分别备份和回滚每个介质文件夹。 您还可以在Commerce安装之外指定介质文件夹。 |

{style="table-layout:auto"}

## [!UICONTROL Base URLs (Secure)]

![Web >基本URL（安全）](./assets/web-base-urls-secure.png)<!-- zoom -->

<!-- [Base URLs (Secure) configuration settings](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/site-store/store-urls) -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Secure Base URL] | 商店视图 | 使用加密安全(SSL/TLS)协议传送的Commerce根文件夹的完整地址。 URL必须以正斜杠结尾。 |
| [!UICONTROL Secure Base Link URL] | 商店视图 | 标记标记，用作在安全渠道上运行的基础URL的占位符。 |
| [!UICONTROL Secure Base URL for Static View Files] | 商店视图 | 指向主题使用的静态文件(如CSS、字体、图像和JavaScript)位置的标记标记。 文件可以在不安全的通道或安全通道上。 如果Commerce安装具有多个具有相同文件夹结构的站点，则每个站点可以有不同的文件夹。 在输入静态视图文件的基本URL之前，将配置范围设置为正确的站点。 您还可以在Commerce安装之外指定文件夹。 |
| [!UICONTROL Secure Base URL for User Media Files] | 商店视图 | 指向目录图像和其他媒体文件位置的路径。 文件可以在不安全的通道或安全通道上。 占位符用于表示基本URL。 如果Commerce安装有多个具有相同文件夹结构的站点，则可以为每个站点使用不同的介质文件夹。 这使您能够分别备份和回滚每个介质文件夹。 您还可以在Commerce安装之外指定介质文件夹。 |
| [!UICONTROL Use Secure URLs on Storefront] | 商店视图 | 如果您的域具有安全证书，您可以选择运行店面（无论是否使用SSL加密）。 选项：<br />**`Yes`**— 存储URL以`https`开头，表示页面是使用加密的安全协议交付的。<br />**`No`** — 存储URL以`http`开头，表示页面交付时没有安全协议。 |
| [!UICONTROL Use Secure URLs in Admin] | 全局 | 如果您的域具有安全证书，则可以选择运行应用商店管理员，无论是否使用SSL加密。 选项： <br />**`Yes`**— 管理员URL以`https`开头，表示页面是使用加密的安全协议交付的。<br />**`No`** — 管理员URL以`http`开头，表示页面交付时没有安全协议。<br />为商店和管理员启用安全URL后，将显示两个额外的字段以启用和配置`HSTS`。 |
| [!UICONTROL Enable HTTP Strict Transport Security (HSTS)] | 商店视图 | 启用后，[`HSTS`][1]提供针对“中间人”攻击的安全措施，并防止用户覆盖“无效证书”消息。 选项： `Yes` / `No` |
| [!UICONTROL Upgrade Insecure Requests] | 商店视图 | 启用后，将从浏览器接收的不安全(`HTTP`)请求转换为安全(`HTTPS`)协议。 选项： `Yes` / `No` |
| [!UICONTROL Offloader Header] | 全局 | 指定服务器配置中的`offloader_header`值，以标识客户端和负载平衡器之间的协议。 大多数Commerce安装都使用默认值`X-Forwarded-Proto` (XFP)将协议标识为`HTTP`或`HTTPS`。 |

{style="table-layout:auto"}

## [!UICONTROL Default Pages]

![网页>默认页面](./assets/web-default-pages.png)<!-- zoom -->

<!-- [Default Pages configuration settings](https://experienceleague.adobe.com/en/docs/commerce-admin/content-design/elements/pages/pages#configure-default-pages) -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Default Web URL] | 商店视图 | 指示与基本URL关联的登陆页面。 默认情况下，此参数设置为“cms”，表示来自Commerce内容管理系统(CMS)的页面。 您还可以使用其他类型的登陆页面，如博客。 例如，如果在`magento/blog`处的服务器上安装了博客，则可以输入“blog”文件夹的名称，作为选择页面的相对路径。 |
| [!UICONTROL CMS Home Page] | 商店视图 | 要选择商店的主页，只需从列表中选择CMS页面即可。 默认情况下，CMS主页会列出您商店可用的所有CMS页面选择。 |
| [!UICONTROL Default No-route URL] | 商店视图 | 包含发生`404 Page not Found`错误时要显示的默认页面的URL。 默认值为`cms/noroute/index`。 |
| [!UICONTROL CMS No Route Page] | 商店视图 | 标识您希望在出现404页面未找到错误时显示的特定CMS页面。 默认页面为404 Not Found。 |
| [!UICONTROL CMS No Cookies Page] | 商店视图 | 标识未为浏览器启用Cookie时显示的特定CMS页面。 本页介绍了为何使用Cookie，以及如何为每个浏览器启用它们。 默认页面为启用Cookie。 |
| [!UICONTROL Show Breadcrumbs for CMS Pages] | 商店视图 | 确定是否在目录中的所有CMS页面上显示痕迹导航路径。 选项： `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Default Layouts]

![默认布局](./assets/web-default-layouts.png)<!-- zoom -->

<!--[Default Layouts](https://experienceleague.adobe.com/en/docs/commerce-admin/content-design/design/layout/page-layout) -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Default Product Layout] | 全局 | 确定默认用于产品页面的[布局](../../content-design/page-layout.md)。 选项： <br/>**`No layout updates`**— 默认情况下，布局更新不可用于产品页面。<br/>**`Empty`** — 默认情况下，产品页面使用空白布局。 <br/>**`1 column`**— 默认情况下，产品页面使用单列布局。<br/>**`2 columns with left bar`** — 默认情况下，对于产品页面，使用左侧带有侧栏的双列布局。 <br/>**`2 columns with right bar`**— 默认情况下，对产品页面使用右侧带有侧栏的双列布局。<br/>**`3 columns`** — 默认情况下，产品页面使用左边栏和右边栏的三列布局。<br/>**`Page -- Full Width`**- （需要[!DNL Page Builder]）默认情况下，使用产品页面的“页面 — 全宽”布局。<br/>**`Category - Full Width`** - （需要[!DNL Page Builder]）默认情况下，使用产品页面的“类别 — 全宽”布局。 <br/>**`Product - Full Width`**- （需要[!DNL Page Builder]）默认情况下，使用产品页面的“产品 — 全宽”布局。 |
| [!UICONTROL Default Category Layout] | 全局 | 确定默认情况下用于类别页面的[布局](../../content-design/page-layout.md)。 选项： <br/>**`No layout updates`**— 默认情况下，布局更新不可用于类别页面。<br/>**`Empty`** — 默认情况下，类别页面使用空白布局。 <br/>**`1 column`**— 默认情况下，对类别页面使用单列布局。<br/>**`2 columns with left bar`** — 默认情况下，对于类别页面，使用左侧带有侧栏的双列布局。 <br/>**`2 columns with right bar`**— 默认情况下，对类别页面使用右侧带有侧栏的双列布局。<br/>**`3 columns`** — 默认情况下，对于类别页面，使用左边栏和右边栏的三列布局。<br/>**`Page - Full Width`**- （需要[!DNL Page Builder]）默认情况下，使用类别页面的“页面 — 全宽”布局。<br/>**`Category - Full Width`** - （需要[!DNL Page Builder]）默认情况下，使用类别页面的类别 — 全宽布局。 <br/>**`Product - Full Width`**- （需要[!DNL Page Builder]）默认情况下，使用类别页面的“产品 — 全宽”布局。 |
| 默认页面布局 | 全局 | 确定CMS页面默认使用的[布局](../../content-design/page-layout.md)。 选项： <br/>**`No layout updates`**— 默认情况下，布局更新不适用于CMS页面。<br/>**`Empty`** — 默认情况下，CMS页面使用空白布局。 <br/>**`1 column`**— 默认情况下，对CMS页面使用单列布局。<br/>**`2 columns with left bar`** — 默认情况下，对于CMS页面，使用左侧带有侧栏的双列布局。<br/>**`2 columns with right bar`**— 默认情况下，对于CMS页面，使用右侧带有侧栏的双列布局。<br/>**`3 columns`** — 默认情况下，对于CMS页面，使用左右两侧带有侧栏的三列布局。<br/>**`Page - Full Width`**— （需要[!UICONTROL Page Builder]）默认情况下，使用CMS页面的“页面 — 全宽”布局。<br/>**`Category - Full Width`** — （需要[!UICONTROL Page Builder]）默认情况下，使用CMS页面的“类别 — 全宽”布局。 <br/>**`Product - Full Width`**— （需要[!DNL Page Builder]）默认情况下，使用CMS页面的“产品 — 全宽”布局。 |

{style="table-layout:auto"}

## [!UICONTROL Default Cookie Settings]

![Web >默认Cookie设置](./assets/web-default-cookie-settings.png)<!-- zoom -->

<!-- [Default Cookie configuration settings](https://experienceleague.adobe.com/en/docs/commerce-admin/start/compliance/privacy/compliance-cookie-law) -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Cookie Lifetime] | 商店视图 | 确定Cookie在自动删除之前可以存在的时间。 默认值为3600秒（1小时） |
| [!UICONTROL Cookie Path] | 商店视图 | 指定服务器上可以使用Commerce Cookie的文件夹。 要使Commerce Cookie在安装中的任意位置可用，请将Cookie路径设置为单个正斜杠： `/`。 此值只能包含Cookie路径，**_不能_**&#x200B;包含任何其他Cookie参数。 |
| [!UICONTROL Cookie Domain] | 商店视图 | 确定Commerce Cookie是否对子域可用。 例如，要支持`mysubdomain`.domain.com，请输入以句点开头的域名称，如`.domain.com`。 此值只能包含Cookie域，**_不能_**&#x200B;包含任何其他Cookie参数。 |
| [!UICONTROL Use HTTP Only] | 商店视图 | 确定Commerce Cookie是只能通过不安全的渠道(http)使用，还是也可以通过加密渠道(https)使用。 选项： `Yes` / `No` |
| [!UICONTROL Cookie Restriction Mode] | 网站 | 确定是否启用Cookie限制模式。 选项： `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Session Validation Settings]

![Web >会话验证](./assets/web-session-validation-settings.png)<!-- zoom -->

<!-- [Session Validation configuration settings](https://experienceleague.adobe.com/en/docs/commerce-admin/systems/security/security-session-management#session-validation) -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Validate REMOTE_ADDR] | 全局 | 验证请求的IP地址是否与`$_SESSION`数据匹配。 如果检测到其他IP地址，则会话终止。 选项： `Yes` / `No` |
| [!UICONTROL Validate HTTP_VIA] | 全局 | 验证传入的代理数据并检查请求的代理地址是否与`$_SESSION`数据匹配。 如果检测到不同的代理地址，则会话终止。 选项： `Yes` / `No` |
| [!UICONTROL Validate HTTP_x_FORWARDED_FOR] | 全局 | 验证传出代理数据并检查请求的转发地址是否与`$_SESSION`数据匹配。 如果检测到不同的转发地址，则会话终止。 选项： `Yes` / `No` |
| [!UICONTROL Validate HTTP_USER_AGENT] | 全局 | `USER_AGENT`是指用于访问网站的浏览器或设备。 它验证浏览器的名称和版本以及操作系统是否与`$_SESSION`数据匹配。 如果在同一会话中从一个请求到另一个请求检测到不同的用户代理，则会话终止。 选项： `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Browser Capabilities Detection]

![Web >浏览器功能检测](./assets/web-browser-capabilities-detection.png)<!-- zoom -->

<!-- [Browser Capabilities Detection configuration settings](https://experienceleague.adobe.com/en/docs/commerce-admin/systems/security/security-browser-capabilities-detection) -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Redirect to CMS-page if Cookies are Disabled] | 商店视图 | 如果浏览器禁用Cookie，则会自动重定向到CMS无Cookie页面。 选项： `Yes` / `No` |
| [!UICONTROL Show Notice if JavaScript is Disabled] | 商店视图 | 如果浏览器禁用了JavaScript，它会显示一条通知，提示用户启用JavaScript选项： `Yes` / `No`（禁用） |
| [!UICONTROL Show Notice if Local Storage is Disabled] | 商店视图 | 如果本地缓存被禁用，则显示一条消息。 选项： `Yes` / `No` |

{style="table-layout:auto"}

[1]: https://cheatsheetseries.owasp.org/cheatsheets/HTTP_Strict_Transport_Security_Cheat_Sheet.html

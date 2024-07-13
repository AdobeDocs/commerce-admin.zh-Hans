---
title: Cookie法律合规性
description: 为了跟上许多国家关于使用Cookie的法规，Adobe Commerce和Magento Open Source为商家提供了多种获取客户同意的方法。
exl-id: 42df20cd-50a7-4618-98fd-9ced936e305b
feature: Compliance
source-git-commit: ae43d97bb3031a06ce6a0211ee304aae53e4eb08
workflow-type: tm+mt
source-wordcount: '2105'
ht-degree: 0%

---

# Cookie法律合规性

Cookie是保存到网站每位访客的计算机中的小文件，用作信息的临时存放处。 保存在Cookie中的信息可用于个性化购物体验、将访客链接到其购物车、衡量流量模式以及提高促销效率。 为了跟上许多国家关于使用Cookie的法规，Adobe Commerce和Magento Open Source为商家提供了多种获取客户同意的方法。 有关Adobe Commerce和Magento Open Source中的默认Cookie的列表，[Cookie引用](#default-cookies)。

>[!NOTE]
>
>如果您修改了默认[Google隐私设置](../merchandising-promotions/google-tools.md#google-privacy-settings)以符合[通用数据保护条例](compliance-gdpr.md)，则无需获取用户同意即可使用Google AnalyticsCookie。

## 方法1：默示同意

默示同意意味着您商店的访客已清楚地了解Cookie是操作的一个必要部分，并且通过使用您的网站，已间接授予使用它们的权限。 获得默示同意的关键是提供足够的信息，以便访客做出知情决定。 许多商店会在所有标准页面顶部显示一条消息，简要概述Cookie的使用方式，并提供指向商店隐私策略的链接。 隐私策略应描述存储收集的信息类型以及信息的使用方式。

## 方法2：表示同意

在&#x200B;_Cookie限制模式_&#x200B;下运行存储区需要访客先表达同意，然后才能将任何Cookie保存到其计算机。 除非获得同意，否则您应用商店的许多功能将不可用。 例如，如果Google Analytics可用于您的商店，则只有在访客授予使用Cookie的权限后，才能调用该商店。

## Cookie限制模式

启用Cookie限制模式后，您商店的访客将收到通知，告知您需要Cookie才能执行全功能操作。 根据您的主题，消息可能会显示在页眉上方、页脚下方或页面上的其他位置。 该消息链接到您的隐私政策以获取更多信息，并鼓励访客单击允许按钮授予同意。 获得同意后，消息将消失。

您的[隐私政策](privacy-policy.md))应包含商店名称和联系信息，并解释商店使用的每个Cookie的用途。 若要了解详细信息，请参阅[Cookie引用](#default-cookies)。

>[!NOTE]
>
>如果您更改隐私策略的URL密钥，则还必须创建自定义URL重写以将流量重定向到新的URL密钥。 否则，Cookie限制模式消息中的链接将返回`404 Page Not Found`。

![店面示例 — Cookie限制通知](./assets/storefront-cookie-restriction-message.png){width="600"}

### 步骤1：启用Cookie限制模式

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧导航面板中的&#x200B;**[!UICONTROL General]**&#x200B;下，选择&#x200B;**[!UICONTROL Web]**。

1. 展开&#x200B;**[!UICONTROL Default Cookie Settings]**&#x200B;部分并执行以下操作：

   ![Web配置 — 默认Cookie设置](./assets/web-default-cookie-settings.png){width="600"}

   - 输入&#x200B;**[!UICONTROL Cookie Lifetime]**（以秒为单位）。

   - 如果要使Cookie对其他文件夹可用，请输入&#x200B;**[!UICONTROL Cookie Path]**。 要使Cookie在网站的任何位置都可用，请输入正斜杠(`/`)。 此值只能包含Cookie路径，**_不能_**&#x200B;包含任何其他Cookie参数。

   - 要使Cookie可用于子域，请在&#x200B;**[!UICONTROL Cookie Domain]**&#x200B;字段(`subdomain.yourdomain.com`)中输入子域名。 要使Cookie对所有子域都可用，请输入前面有句点(`.yourdomain.com`)的域名。 此值只能包含Cookie域，**_不能_**&#x200B;包含任何其他Cookie参数。

   - 要阻止脚本语言(如JavaScript)访问Cookie，请确保&#x200B;**仅使用HTTP**&#x200B;设置为`Yes`。

   - 将&#x200B;**[!UICONTROL Cookie Restriction Mode]**&#x200B;设置为`Yes`。

     如有必要，请清除该复选框，然后单击&#x200B;**[!UICONTROL OK]**&#x200B;确认范围切换。

1. 完成后，单击&#x200B;**[!UICONTROL Save Config]**。

1. 提示更新缓存时，单击系统消息中的&#x200B;**[!UICONTROL Cache Management]**&#x200B;链接。 然后，刷新每个无效缓存。

### 步骤2：更新您的隐私政策

更新您的[隐私策略](privacy-policy.md)，以便它反映贵公司收集的信息及其使用方式。

## 默认Cookie

Adobe Commerce和Magento Open Source中的默认Cookie被分类为劐免/非劐免，以帮助商家满足隐私法规的要求，例如[GDPR](compliance-gdpr.md)。 商家应将此信息用作指南，并咨询法律顾问，以更新其隐私和Cookie政策，作为全面的隐私法规合规策略的一部分。

[!DNL Commerce]将以下Cookie用于“开箱即用”的内部部署和云安装。 客户明确请求的功能可能需要这些Cookie。 要了解会话Cookie的生命周期，请参阅[会话生命周期](../customers/customer-online-options.md)。

其中一些Cookie可能会根据需要提供配置选项，包括启用/禁用。

### 请求的功能Cookie（免费）


#### `add_to_cart`

Google标签管理器使用的![Adobe Commerce](../assets/adobe-logo.svg)(仅限Adobe Commerce)。 捕获从购物车中移除的产品SKU、名称、价格和数量，并让该信息可供第三方脚本在将来的集成。

#### `guest-view`

存储访客购物者用于检索其订单状态的订单ID。 来宾订单视图。 在&#x200B;_[!DNL Orders and Returns]_小组件中使用。

- 安全吗？ 否
- 仅限HTTP：是
- 过期策略：会话
- 模块： `Magento_Sales`

#### `login_redirect`

保留在指引客户登录之前加载的目标页面。 如果[Display Mini Cart](../stores-purchase/cart-configuration.md#mini-cart)配置选项设置为`Yes`，则登录重定向将与迷你购物车一起使用。

- 安全吗？ 否
- 仅限HTTP：否
- 过期策略：会话
- 模块： `Magento_Customer`

#### `mage-banners-cache-storage`

![Adobe Commerce](../assets/adobe-logo.svg)(仅限Adobe Commerce)在本地存储横幅内容以提高性能。

#### `mage-messages`

跟踪向用户显示的错误消息和其他通知，如Cookie同意消息以及各种错误消息。 消息在向购物者显示后，将从Cookie中删除。

没有选项可禁用此Cookie。

- 安全吗？ 否
- 仅限HTTP：否
- 到期策略：持续时间1年。 向用户显示消息时，已在前端清除。
- 模块： `Magento_Theme`

#### `mage-translation-storage` （本地存储）

当购物者请求时，存储翻译的内容。 在[翻译策略](../configuration-reference/advanced/developer.md)配置为“字典（店面翻译）”时使用。

- 安全吗？ 否
- 仅限HTTP：否
- 过期策略：每个本地存储规则
- 模块： `Magento_Translation`

#### `mage-translation-file-version` （本地存储）

跟踪本地存储中的翻译版本。 在[翻译策略](../configuration-reference/advanced/developer.md)配置为`Dictionary (Translation on Storefront side)`时使用。

- 安全吗？ 否
- 仅限HTTP：否
- 过期策略：每个本地存储规则
- 模块： `Magento_Translation`

#### `product_data_storage` （本地存储）

存储与最近查看/比较的产品相关的产品数据的配置。

- 安全吗？ 否
- 仅限HTTP：否
- 过期策略：每个本地存储规则
- 模块： `Magento_Catalog`

#### `recently_compared_product` （本地存储）

存储最近比较的产品的产品ID。

- 安全吗？ 否
- 仅限HTTP：否
- 过期策略：每个本地存储规则
- 模块： `Magento_Catalog`

#### `recently_compared_product_previous` （本地存储）

存储以前比较的产品的产品ID以便轻松导航。

- 安全吗？ 否
- 仅限HTTP：否
- 过期策略：每个本地存储规则
- 模块： `Magento_Catalog`

#### `recently_viewed_product` （本地存储）

存储最近查看的产品的产品ID以便轻松导航。

- 安全吗？ 否
- 仅限HTTP：否
- 过期策略：每个本地存储规则
- 模块： `Magento_Catalog`

#### `recently_viewed_product_previous` （本地存储）

存储最近查看过的产品的产品ID以便轻松导航。

- 安全吗？ 否
- 仅限HTTP：否
- 过期策略：每个本地存储规则
- 模块： `Magento_Catalog`

#### `remove_from_cart`

![Adobe Commerce](../assets/adobe-logo.svg)(仅限Adobe Commerce)由[Google标签管理器](../merchandising-promotions/google-tag-manager.md)使用。 捕获添加到购物车的产品SKU、名称、价格和数量，并让该信息可供第三方脚本在将来集成。

#### `stf`

记录SendFriend （[向Friend发送电子邮件](../stores-purchase/email-a-friend.md)）模块发送邮件的时间。

- 安全吗？ 是
- 仅限HTTP：是
- 过期策略：会话
- 模块： `Magento_SendFriend`

#### `X-Magento-Vary`

使用清漆静态内容缓存时提高性能的配置设置。

- 安全吗？ 是
- 仅限HTTP：是
- 过期策略：基于PHP设置session.cookie_lifetime
- 模块： `Magento_PageCache`

#### `form_key`

一种安全措施，可在所有表单提交中附加随机字符串，以保护数据免受跨站点请求伪造(CSRF)攻击。

- 安全吗？ 否
- 仅限HTTP：否
- 过期策略：
   - PHP：基于PHP设置session.cookie_lifetime
   - JS：会话
- 模块：页面缓存

#### `mage-cache-sessid`

此Cookie的值会触发本地缓存存储的清理。 当后端应用程序删除Cookie时，管理员将清理本地存储，并将Cookie值设置为`true`。

- 安全吗？ 否
- 仅限HTTP：否
- 过期策略：会话
- 模块： `Magento_Customer`

#### `mage-cache-storage`

用于启用电子商务功能的访客特定内容的本地存储。

- 安全吗？ 否
- 仅限HTTP：否
- 过期策略：会话
- 模块： `Magento_Customer`，`Magento_Persistent`

#### `mage-cache-storage` （本地存储）

用于启用电子商务功能的访客特定内容的本地存储。

- 安全吗？ 否
- 仅限HTTP：否
- 过期策略：会话
- 模块： `Magento_Customer`，`Magento_Persistent`，`Magento_NegotiableQuote`

#### `mage-cache-storage-section-invalidation` （本地存储）

强制在本地存储应失效的特定内容部分。

- 安全吗？ 否
- 仅限HTTP：否
- 过期策略：每个本地存储
- 模块： `Magento_Customer`

#### `persistent_shopping_cart`

存储永久购物车的密钥(ID)，以便能够恢复匿名购物者的购物车。

- 安全吗？ 是
- 仅限HTTP：是
- 到期策略：基于[持久购物车](../stores-purchase/cart-persistent.md) — 持久存留期（秒）配置
- 模块： `Magento_Persistent`

#### `private_content_version`

将随机、唯一数字和时间附加到包含客户内容的页面，以防止在服务器上缓存这些页面。

它在多个位置设置：在PHP中，在JavaScript中设置为Cookie，在JavaScript中设置为本地存储。

对于HTTP Only=`Yes`（基于请求），这意味着如果在HTTPS请求期间设置了Cookie，那么它是安全的；如果在HTTP请求期间设置了，那么它是不安全的。

- 安全吗？ `Yes` （基于请求），`No`
- 仅限HTTP： `No`
- 到期策略：基于[持久购物车](../stores-purchase/cart-persistent.md) — 持久存留期（秒）配置
   - PHP： `1`年/ `315360000s` （十年）
   - JS： `1`天
   - JS本地存储：每个本地存储规则（永久）
- 模块： `Magento_PageCache`，`Magento_Customer`

#### `section_data_ids`

存储与购物者启动的操作相关的客户特定信息，例如愿望清单显示和结帐信息。

- 安全吗？`No`
- 仅限HTTP： `No`
- 到期策略： `Session`
- 模块： `Magento_Customer`

#### `store`

跟踪购物者选择的特定商店视图/区域设置。

- 安全吗？`No`
- 仅限HTTP： `Yes`
- 过期策略：`1`年
- 模块： `Magento_Store`

#### `mage-banners-cache-storage` — 本地存储

![Adobe Commerce](../assets/adobe-logo.svg) (仅限Adobe Commerce)用于横幅功能的本地存储。

- 安全吗？`No`
- 仅限HTTP： `No`
- 过期策略：每个本地存储规则
- 模块： `Magento_Banner`

## Google AnalyticsCookie

在为您的安装完全启用[Google Analytics](../merchandising-promotions/google-analytics.md)或Google Universal Analytics时，将使用以下Cookie。 要禁用这些Cookie以符合隐私法规，请参阅[Google隐私设置](../merchandising-promotions/google-tools.md#google-privacy-settings)。 若要了解更多信息，请参阅[网站上的Google AnalyticsCookie使用情况][1]。

### Google Universal Analytics Cookie — 非劐免

![Adobe Commerce](../assets/adobe-logo.svg)(仅限Adobe Commerce)JavaScript库： `gtag.js`和`analytics.js`

- `_ga`：区分您网站的访客。
- `_gid`：区分您网站的访客。
- `gat`：用于限制请求速率。
- `dc_gtm_<property-id>`：使用[Google Tag Manager](../merchandising-promotions/google-tag-manager.md)部署Google Analytics时限制请求速率。
- `AMP_TOKEN`：包含可用于从AMP客户端ID服务检索客户端ID的令牌。 其他可能的值包括选择禁用、请求正在发送或从AMP客户端ID服务检索客户端ID时出错。
- `_gac_<property-id>`：包含用户的促销活动相关信息。 如果Google Analytics已链接到您的[AdWords][2]帐户，则Google AdWords转化标记会读取此Cookie。

### Google AnalyticsCookie — 非劐免

![Adobe Commerce](../assets/adobe-logo.svg)(仅限Adobe Commerce)JavaScript库： `ga.js`

- `__utma`：区分购物者和会话。 此Cookie在JavaScript库执行时创建，并且不存在现有的`__utma` Cookie。 每次向Google Analytics发送数据时，Cookie都会更新。
- `__utmt`：用于限制请求速率。
- `__utmb`：确定新会话/访问。 此Cookie在JavaScript库执行时创建，并且不存在现有的`__utmb` Cookie。 每次向Google Analytics发送数据时，Cookie都会更新。
- `_utmz`：保存说明购物者如何访问您网站的流量源或营销活动。 Cookie在JavaScript库执行时创建，并在每次向Google Analytics发送数据时更新。
- `__utmv`：存储访客级别的自定义变量数据。 此Cookie是在开发人员将`_setCustomVar`方法与访客级别的自定义变量结合使用时创建的。 每次向Google Analytics发送数据时，此Cookie都会更新。

## 产品Recommendations Cookie

![Adobe Commerce](../assets/adobe-logo.svg)(仅限Adobe Commerce)以下Cookie由产品Recommendations用于Adobe Commerce客户。 这些Cookie随[数据服务模块](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/getting-started/install-configure.html)一起安装。

- `mg_dnt`：如果您拥有用于管理您网站上的Cookie同意的自定义代码，则允许您[限制Adobe Commerce数据收集](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/developer/setting-cookie.html)。
- `user_allowed_save_cookie`：用于[Cookie限制模式](#cookie-restriction-mode)。
- `authentication_flag`：指示购物者是否已登录或注销。 此Cookie与`dataservices_customer_id` Cookie同时更新。
- `dataservices_customer_id`：指示购物者是否已登录或注销。 此Cookie包含系统中客户的唯一ID。
- `dataservices_customer_group`：指示客户的组。 此Cookie存储为客户组ID的[sha1](https://en.wikipedia.org/wiki/SHA-1)校验和。
- `dataservices_cart_id`：标识购物者的购物车操作。 此Cookie包含系统中客户的唯一购物车ID。
- `dataservices_product_context`：标识购物者的产品交互。 此Cookie包含系统中客户的唯一报价ID。

## 其他Cookie

![Adobe Commerce](../assets/adobe-logo.svg)(仅限Adobe Commerce)已为Adobe Commerce客户设置以下Cookie。 这些Cookie随[数据服务模块](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/getting-started/install-configure.html)一起安装。

- `mg`：由Snowplow JavaScript跟踪器设置。 有关详细信息，请参阅[雪铲文档](https://docs.snowplow.io/docs/collecting-data/collecting-from-own-applications/javascript-trackers/javascript-tracker/javascript-tracker-v3/tracker-setup/initialization-options)。
- `com.adobe.alloy.getTld`：给定当前网页的主机名，这是最顶层的域，不是https://publicsuffix.org中所述的“公共后缀”。 本质上，这是可以接受Cookie的最顶部域。 此Cookie是[Alloy Web SDK](https://github.com/adobe/alloy)的一部分。

[1]: https://developers.google.com/analytics/devguides/collection/analyticsjs/cookie-usage
[2]: https://support.google.com/adwords/answer/7521212

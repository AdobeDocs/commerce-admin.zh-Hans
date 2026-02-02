---
title: Cookie法律合规性
description: 为了跟上许多国家关于使用Cookie的法规，Adobe Commerce和Magento Open Source为商家提供了多种获取客户同意的方法。
exl-id: 42df20cd-50a7-4618-98fd-9ced936e305b
feature: Compliance
source-git-commit: c68b464025c00acd4aea6a23aef97fb440e2ed05
workflow-type: tm+mt
source-wordcount: '2244'
ht-degree: 0%

---

# Cookie法律合规性

Cookie是保存到网站每位访客的计算机中的小文件，用作信息的临时存放处。 保存在Cookie中的信息可用于个性化购物体验、将访客链接到其购物车、衡量流量模式以及提高促销效率。 为了跟上许多国家关于使用Cookie的法规，Adobe Commerce和Magento Open Source为商家提供了多种获取客户同意的方法。 有关Adobe Commerce和Magento Open Source中的默认Cookie的列表，[Cookie引用](#default-cookies)。

>[!NOTE]
>
>如果您修改了默认[Google隐私设置](../merchandising-promotions/google-tools.md#google-privacy-settings)以符合[通用数据保护条例](compliance-gdpr.md)，则无需获取用户同意即可使用Google Analytics Cookie。

## Cookie限制模式

启用Cookie限制模式后，您商店的访客将收到通知，告知您需要Cookie才能执行全功能操作。 根据您的主题，消息可能会显示在页眉上方、页脚下方或页面上的其他位置。 该消息链接到您的隐私政策以获取更多信息，并鼓励访客单击允许按钮授予同意。 获得同意后，消息将消失。

您的[隐私政策](privacy-policy.md)应包含商店名称和联系信息，并解释商店使用的每个Cookie的用途。 若要了解详细信息，请参阅[Cookie引用](#default-cookies)。

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

1. 提示更新缓存时，单击系统消息中的&#x200B;**[!UICONTROL Cache Management]**&#x200B;链接，并刷新每个无效缓存。

### 步骤2：更新您的隐私政策

更新您的[隐私策略](privacy-policy.md)，以便它反映贵公司收集的信息及其使用方式。

## 默认Cookie

Adobe Commerce和Magento Open Source中的默认Cookie被分类为劐免/不劐免，以帮助商家满足隐私法规的要求，例如[GDPR](compliance-gdpr.md)。 商家应将此信息用作指南，并咨询法律顾问，以更新其隐私和Cookie政策，作为全面的隐私法规合规策略的一部分。

[!DNL Commerce]将以下Cookie用于“开箱即用”的内部部署和云安装。 客户明确请求的功能可能需要这些Cookie。 要了解有关会话Cookie生命周期的更多信息，请参阅[会话生命周期](../customers/customer-online-options.md)。

其中一些Cookie可能会根据需要提供配置选项，包括启用/禁用。

### 请求的功能Cookie（免费）

| 名称 | 类型 | 描述 |
| ------ | ------ | ------------- |
| **`add_to_cart`** | Cookie | ![Adobe Commerce](../assets/adobe-logo.svg)(仅限Adobe Commerce)捕获从购物车中移除的产品SKU、名称、价格和数量。 允许Google Analytics知道产品何时已添加到购物车。 |
| **`guest-view`** | Cookie | 将访客订单链接到访客（因为没有访客帐户）。 要维护系统稳定性，请勿禁用此Cookie。 |
| **`login_redirect`** | Cookie | 保存重定向URL以在成功登录和用户注册时路由用户。 保存用户在登录之前所在的页面（以确定他们在登录后返回的位置）。 |
| **`mage-banners-cache-storage`** | 本地存储 | ![Adobe Commerce](../assets/adobe-logo.svg) (仅限Adobe Commerce)用于横幅功能的本地存储。 在本地存储横幅内容以提高性能。 横幅内容包括向购物者显示信息的常规网站资产。 要维护系统稳定性，请勿禁用此Cookie。 |
| **`mage-messages`** | Cookie | 跟踪向用户显示的错误消息和其他通知，如Cookie同意消息以及各种错误消息。 消息在向购物者显示后，将从Cookie中删除。 没有选项可禁用此Cookie。 这就是一次性信息（如错误消息）传达给用户的方式。 要维护系统稳定性，请勿禁用此Cookie。 |
| **`product_data_storage`** | 本地存储 | 存储用于使用“最近查看”和“比较产品”功能的产品数据的配置。 存储用户的特定设置（例如，他们最近是否查看过产品或比较了哪些产品）。 要维护系统稳定性，请勿禁用此Cookie。 |
| **`recently_compared_product`** | 本地存储 | 存储最近比较的产品的产品ID。 要维护系统稳定性，请勿禁用此Cookie。 |
| **`recently_compared_product_previous`** | 本地存储 | 存储以前比较的产品的产品ID以便轻松导航。 要维护系统稳定性，请勿禁用此Cookie。 |
| **`recently_viewed_product`** | 本地存储 | 存储最近查看的产品的产品ID以便轻松导航。 要维护系统稳定性，请勿禁用此Cookie。 |
| **`recently_viewed_product_previous`** | 本地存储 | 存储最近查看的产品的产品ID以便轻松导航。 要维护系统稳定性，请勿禁用此Cookie。 |
| **`remove_from_cart`** | Cookie | ![Adobe Commerce](../assets/adobe-logo.svg)(仅限Adobe Commerce)允许Google Analytics知道产品何时从购物车中删除。 |
| **`stf`** | Cookie | 记录SendFriend （[向Friend发送电子邮件](../stores-purchase/email-a-friend.md)）模块发送邮件的时间。 当购物者向产品发送链接时，此Cookie记录时间戳和维护计数。 |
| **`X-Magento-Vary`** | Cookie | 指示何时需要从缓存中提供页面的新版本。 支持网站性能。 要维护系统稳定性，请勿禁用此Cookie。 |
| **`form_key`** | Cookie | 一种安全机制，可保存随机生成的值，以帮助确定请求是来自真实来源还是来自错误操作者，从而防止跨站点请求伪造攻击(CSRF)。 这是用于防止CSRF攻击的行业标准做法。 要维护系统稳定性，请勿禁用此Cookie。 |
| **`mage-cache-sessid`** | Cookie | 在决定会话过期后何时清理浏览器中的本地存储时非常有用。 用于确定是否需要清理本地存储。 缺少此Cookie会触发本地存储清理。 要维护系统稳定性，请勿禁用此Cookie。 |
| **`mage-cache-storage`** | 本地存储 | 用于启用电子商务功能的访客特定内容的本地存储。 默认情况下未使用，但在使用时，会使用它来加快结帐速度，以便在用户离开和返回时可以使用基本的用户信息。 要维护系统稳定性，请勿禁用此Cookie。 |
| **`mage-cache-storage-section-invalidation`** | 本地存储 | 存储与页面的哪些部分需要失效和移除相关的信息。 要维护系统稳定性，请勿禁用此Cookie。 |
| **`mage-cache-timeout`** | 本地存储 | 控制与客户相关的数据在浏览器中缓存的时长。 超时过期后，Magento会清除并重新加载缓存的客户部分，例如购物车、愿望清单和客户数据。 此行为有助于保持数据准确性和隐私，同时平衡客户端性能。 超时值与配置的Cookie生命周期一致，以保持与服务器端会话管理的一致性。 |
| **`persistent_shopping_cart`** | Cookie | 存储永久性购物车的密钥ID，以便能够恢复匿名购物者的购物车。 要维护系统稳定性，请勿禁用此Cookie。 |
| **`private_content_version`** | Cookie | 将随机、唯一数字和时间附加到包含客户内容的页面，以防止在服务器上缓存这些页面。 它在多个位置设置：在PHP中，在JavaScript中设置为Cookie，在JavaScript中设置为本地存储。 要维护系统稳定性，请勿禁用此Cookie。 |
| **`section_data_ids`** | Cookie | 存储与购物者启动的操作相关的客户特定信息，例如愿望清单显示和结帐信息。 要维护系统稳定性，请勿禁用此Cookie。 |
| **`store`** | Cookie | 跟踪购物者选择的特定商店视图/区域设置。 要维护系统稳定性，请勿禁用此Cookie。 |
| **`PHPSESSID`** | Cookie | 跟踪店面上的用户会话。 这是使用最终产品的购物者。 要维护系统稳定性，请勿禁用此Cookie。 |
| **`admin`** | Cookie | 在管理员端跟踪用户会话。 要维护系统稳定性，请勿禁用此Cookie。 |
| **`loggedOutReasonCode`** | Cookie | 当管理员用户在密码尝试失败一定次数后被锁定时设置。 |
| **`section_data_clean`** | Cookie | 当用户切换存储视图时设置。 此Cookie的存在会触发JavaScript重新加载页面上的某些部分，以反映正确的商店视图。 要维护系统稳定性，请勿禁用此Cookie。 |
| **`lang`** | Cookie | 由Admin Analytics模块间接设置。 仅在商店的管理区域使用。 不适用于购物者。 要维护系统稳定性，请勿禁用此Cookie。 |
| **`s_fid`** | Cookie | 由Admin Analytics模块间接设置。 备用独特访客ID时间戳/日期戳。 如果标准`s_vi` Cookie由于受第三方Cookie限制而不可用，可用于识别独特访客。 仅在商店的管理区域使用。 不适用于购物者。 要维护系统稳定性，请勿禁用此Cookie。 |
| **`s_cc`** | Cookie | 由Admin Analytics模块间接设置。 它通过JavaScript代码设置和读取，以确定是否已启用Cookie。 仅在商店的管理区域使用。 不适用于购物者。 要维护系统稳定性，请勿禁用此Cookie。 |
| **`apt.sid`** | Cookie | 由Admin Analytics模块间接使用的Gainsight PX库设置。 此Cookie的用途是允许在产品的顶级域下跟踪永久会话ID，并将其用作活动会话的参考ID。 仅在商店的管理区域使用。 不适用于购物者。 要维护系统稳定性，请勿禁用此Cookie。 |
| **`apt.uid`** | Cookie | 由Admin Analytics模块间接使用的Gainsight PX库设置。 此Cookie的用途是允许对产品顶级域进行持久ID跟踪，并用作用户实体的参考ID。 仅在商店的管理区域使用。 不适用于购物者。 要维护系统稳定性，请勿禁用此Cookie。 |
| **`s_sq`** | Cookie | 由Admin Analytics模块间接设置。 由ClickMap功能使用，该功能收集有关访客点击位置及其点击内容的数据。 存储每次点击的信息。 仅在商店的管理区域使用。 不适用于购物者。 要维护系统稳定性，请勿禁用此Cookie。 |
| **`pagebuilder_modal_dismissed`** | Cookie | 由页面生成器模块设置。 包含一个标志，阻止在管理员之前明确取消某项操作时，后续提示要求管理员确认是否将其打开。 仅在商店的管理区域使用。 不适用于购物者。 |
| **`pagebuilder_template_apply_confirm`** | Cookie | 由页面生成器模块设置。 包含一个标志，阻止在管理员之前明确取消某项操作时，后续提示要求管理员确认是否将其打开。 仅在商店的管理区域使用。 不适用于购物者。 |
| **`accordion-{VARIABLE}-{VARIABLE}`** | Cookie | 仅在存储的管理区域中用作选项卡功能实施的一部分。 不适用于购物者。 |

{style="table-layout:auto"}

## 产品推荐Cookie

![Adobe Commerce](../assets/adobe-logo.svg)(仅限Adobe Commerce)以下Cookie由面向Adobe Commerce客户的产品推荐使用。 这些Cookie随[数据服务模块](https://experienceleague.adobe.com/en/docs/commerce/product-recommendations/getting-started/install-configure)一起安装。

- `mg_dnt`：如果您拥有用于管理您网站上的Cookie同意的自定义代码，则允许您[限制Adobe Commerce数据收集](https://experienceleague.adobe.com/en/docs/commerce/product-recommendations/developer/setting-cookie)。
- `user_allowed_save_cookie`：用于[Cookie限制模式](#cookie-restriction-mode)。
- `authentication_flag`：指示购物者是否已登录或注销。 此Cookie与`dataservices_customer_id` Cookie同时更新。
- `dataservices_customer_id`：指示购物者是否已登录或注销。 此Cookie包含系统中客户的唯一ID。
- `dataservices_customer_group`：指示客户的组。 此Cookie存储为客户组ID的[sha1](https://en.wikipedia.org/wiki/SHA-1)校验和。
- `dataservices_cart_id`：标识购物者的购物车操作。 此Cookie包含系统中客户的唯一购物车ID。
- `dataservices_product_context`：标识购物者的产品交互。 此Cookie包含系统中客户的唯一报价ID。

### 产品推荐本地存储数据

安装Live Search或产品推荐后，使用Luma主题将以下数据保存到本地存储中，以便进行存储：

- `ds-cart`：存储Luma特定功能的购物车信息
- `ds-cart-order`：存储购物车功能的订单信息
- `ds-purchase-history`：跟踪客户购买历史记录
- `ds-view-history-time-decay`：存储具有基于时间的衰减的产品视图历史记录
- `ds-logged-in`：指示客户登录状态。 此数据仅在客户登录时存在，并且即使在启用Cookie限制模式的情况下也会存储。 这是启用Cookie限制模式后，Commerce在本地存储中存储的唯一数据，无论用户同意状态如何。

## 其他Cookie

![Adobe Commerce](../assets/adobe-logo.svg)(仅限Adobe Commerce)已为Adobe Commerce客户设置以下Cookie。 这些Cookie随[数据服务模块](https://experienceleague.adobe.com/en/docs/commerce/product-recommendations/getting-started/install-configure)一起安装。

- `mg`：由Snowplow JavaScript跟踪器设置。 有关详细信息，请参阅[雪铲文档](https://docs.snowplow.io/docs/sources/trackers/javascript-trackers/web-tracker/tracker-setup/initialization-options/)。
- `com.adobe.alloy.getTld`：给定当前网页的主机名，这是最顶层的域，不是https://publicsuffix.org中所述的“公共后缀”。 本质上，这是可以接受Cookie的最顶部域。 此Cookie是[Alloy Web SDK](https://github.com/adobe/alloy)的一部分。
- `aep-segments-membership`：包含[受众信息](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/audience-activation)，例如购物者属于哪个区段。

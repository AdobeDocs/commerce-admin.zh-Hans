---
title: 配置事件
description: 在店面侧边栏中了解如何完成基本配置以启用事件并设置事件块。
exl-id: 620b2d60-ce6f-4f31-93bb-18d3dd9cdce6
feature: Marketing Tools, Promotions/Events
badgePaas: label="仅限PaaS" type="Informative" url="https://experienceleague.adobe.com/zh-hans/docs/commerce/user-guides/product-solutions" tooltip="仅适用于云项目(Adobe管理的PaaS基础架构)和内部部署项目上的Adobe Commerce 。"
source-git-commit: 7e28081ef2723d4113b957edede6a8e13612ad2f
workflow-type: tm+mt
source-wordcount: '484'
ht-degree: 0%

---

# 配置事件

{{ee-feature}}

在创建事件之前，您必须完成基本配置以启用事件并在侧边栏中设置事件块。

## 启用和配置事件

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧面板中，展开&#x200B;**[!UICONTROL Catalog]**&#x200B;并在下面选择&#x200B;**[!UICONTROL Catalog]**。

1. 展开&#x200B;**[!UICONTROL Catalog Events]**&#x200B;部分中的![扩展选择器](../assets/icon-display-expand.png)并执行以下操作：

   ![目录配置 — 目录事件](../configuration-reference/catalog/assets/catalog-events.png){width="600" zoomable="yes"}

   - 将&#x200B;**[!UICONTROL Enable Catalog Events Functionality]**&#x200B;设置为`Yes`。

   - 将&#x200B;**[!UICONTROL Enable Catalog Event Widget on Storefront]**&#x200B;设置为`Yes`。

   - 输入&#x200B;**[!UICONTROL Number of Events to be Displayed in the Event Slider Sidebar Widget]**。 默认情况下，此值设置为`5`。 如果一次只想在滑块中显示一个事件，请输入`1`。

   - 输入&#x200B;**[!UICONTROL Events to Scroll per Click in Event Slider Sidebar Widget]**&#x200B;的数字。 默认情况下，此值设置为`2`。 如果希望滑块在单击时按顺序显示下一个事件，请输入`1`。

1. 完成后，单击&#x200B;**[!UICONTROL Save Config]**。

## 访问限制

个人促销、活动或网站的访问仅限于登录的注册客户，或扩展到在获取访问权之前必须注册的非注册客户。

![常规配置 — 网站限制](../configuration-reference/general/assets/general-website-restrictions.png){width="600" zoomable="yes"}

### 限制访问

个人促销、活动或网站的访问仅限于登录的注册客户，或扩展到在获取访问权之前必须注册的非注册客户。

![常规配置 — 网站限制](../configuration-reference/general/assets/general-website-restrictions.png){width="600" zoomable="yes"}

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧面板中，展开&#x200B;**[!UICONTROL General]**&#x200B;并在下面选择&#x200B;**[!UICONTROL General]**。

1. 展开&#x200B;**[!UICONTROL Website Restrictions]**&#x200B;部分的![扩展选择器](../assets/icon-display-expand.png)。

1. 将&#x200B;**[!UICONTROL Access Restriction]**&#x200B;设置为`Yes`。

1. 将&#x200B;**[!UICONTROL Restriction Mode]**&#x200B;设置为以下项之一：

   - `Website Closed`
   - `Private Sales: Login Only`
   - `Private Sales: Login and Register`

1. 将&#x200B;**[!UICONTROL Startup Page]**&#x200B;设置为以下项之一：

   - `To login form (302 Found)` — 用户在获得对网站的访问权限之前被重定向到登录表单。

   - `To landing page (302 Found)` — 用户将被重定向到指定的登陆页面，直到他们登录。

     >[!IMPORTANT]
     >
     >请务必加入登陆页面中指向登录页面的链接，以便客户能够登录并访问该网站。

1. 选择客户登录私人销售网站之前显示的&#x200B;**[!UICONTROL Landing Page]**。

1. 若要让搜索引擎机器人和蜘蛛知道登陆页面正确且网站上没有要索引的其他页面，请将&#x200B;**[!UICONTROL HTTP Response]**&#x200B;设置为`200 OK`。

   在所有其他情况下设置为`503 Service Unavailable`。

   >[!NOTE]
   >
   >仅当限制模式设置为&#x200B;_网站已关闭_&#x200B;时才适用。 登陆页面呈现为原始HTML。

1. 如果您希望客户登录和忘记密码表单中的字段自动填写以前条目中的字段，请将&#x200B;**[!UICONTROL Enable Autocomplete on login/forgot password forms]**&#x200B;设置为`Yes`。

1. 完成后，单击&#x200B;**[!UICONTROL Save Config]**。

### 限制销售

默认情况下，即将发生或已关闭的事件中显示的产品不可用于一般销售，并且&#x200B;_[!UICONTROL Add to Cart]_&#x200B;按钮不会出现在产品列表或产品页面上。

若要还原已关闭事件的&#x200B;_[!UICONTROL Add to Cart]_&#x200B;按钮，必须删除该事件（请参阅[更新事件](event-create.md#update-events)）。 但是，如果某个产品与另一个没有销售限制的类别关联，则产品页面上会显示该按钮。 同样，如果产品与无销售限制的其他类别关联，则股票代码块不会显示在产品页面上。

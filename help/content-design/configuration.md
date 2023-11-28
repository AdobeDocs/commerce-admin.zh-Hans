---
title: 设计配置
description: “设计配置”可通过在单个页面上显示设置来轻松编辑与设计相关的规则和配置设置。
exl-id: 43fec57f-d76d-45a9-812b-ba1947cea46d
feature: Page Content, Configuration
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '253'
ht-degree: 0%

---

# 设计配置

设计配置可通过在单个页面上显示设置来轻松编辑与设计相关的规则和配置设置。

![设计配置页面](./assets/configuration.png){width="700" zoomable="yes"}

## 更改设计配置

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. 查找要配置的商店视图，然后单击 **[!UICONTROL Edit]** 在 _[!UICONTROL Action]_列。

   页面将显示商店视图的当前设计设置。

1. 要更改默认主题，请设置 **[!UICONTROL Applied Theme]** 要应用于视图的主题。

   如果未指定主题，则使用系统默认主题。 某些第三方扩展会修改系统默认主题。

1. 如果主题仅用于特定设备，请设置 **[!UICONTROL User Agent Rules]**.

   ![用户代理规则](./assets/configuration-user-agent-rules.png){width="400" zoomable="yes"}

   对于要指定主题的每种设备类型：

   - 单击 **[!UICONTROL Add New User Agent Rule]**.

   - 对象 **[!UICONTROL Search String]**，输入特定设备的浏览器ID。

     搜索字符串可以是标准表达式，也可以是与Perl兼容的正则表达式(PCRE)(请参阅 [用户代理](https://en.wikipedia.org/wiki/User_agent) 了解更多信息)。 以下搜索字符串标识Firefox：

         /^mozilla/i
     
   - 对象 **[!UICONTROL Theme Name]**，选择要用于指定设备的主题。

   >[!NOTE]
   >
   >您可以为要指定的设备添加任意数量的规则。 搜索字符串按输入顺序进行匹配。

1. 下 _[!UICONTROL Other Settings]_，展开每个部分，然后按照链接的主题中的说明根据需要编辑设置。

   - [[!UICONTROL Pagination]](../catalog/navigation-product-listings.md#pagination-controls)
   - [[!UICONTROL HTML Head]](page-setup.md#html-head)
   - [[!UICONTROL Header]](page-setup.md#header)
   - [[!UICONTROL Footer]](page-setup.md#footer)
   - [[!UICONTROL Search Engine Robots]](../merchandising-promotions/seo-overview.md#search-engine-robots)
   - [[!UICONTROL Product Image Watermarks]](../catalog/product-image.md#watermarks)
   - [[!UICONTROL Transactional Emails]](../systems/email-templates.md#configure-email-templates)

   ![影响设计的其他设置](./assets/configuration-other-settings.png){width="500" zoomable="yes"}

1. 完成后，单击 **[!UICONTROL Save Configuration]**.

---
title: “[!DNL Page Builder]安装程序”
description: 了解Adobe Commerce和Magento Open Source管理员中的 [!DNL Page Builder] 功能配置。
exl-id: 48396045-0fef-4f4f-8138-e6d969560e42
feature: Page Builder, Configuration
source-git-commit: 2299beb6c11af801076d3aff0b026d41b9dbd212
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 0%

---

# [!DNL Page Builder]设置

在配置中启用时，[!DNL Page Builder]是CMS页面、块和动态块的默认内容创建工具。 此外，_[!UICONTROL Enable Advanced CMS]_&#x200B;按钮还将[!DNL Page Builder]作为类别和产品的选项提供。 您还可以选择要用于产品、类别和CMS页面的默认[页面布局](../content-design/page-layout.md)。 [!DNL Page Builder]不可用于使用WYSIWYG [编辑器](../content-design/editor.md)的新闻稿内容。

>[!NOTE]
>
>安装后，[!DNL Page Builder]将覆盖[!UICONTROL Mask for Meta Description]配置字段的默认设置。 值已从`{{name}} {{description}}`更改为`{{name}}`。
><br>
>当您转到[!UICONTROL Stores] > _[!UICONTROL Settings]_> [!UICONTROL Configuration]，展开[!UICONTROL Catalog]，然后选择下面的[!UICONTROL Catalog]时，您可以访问此设置。 [!UICONTROL Mask for Meta Description]字段在[!UICONTROL Product Fields Auto-generation]部分中。

>[!NOTE]
>
>管理员用户必须具有针对其[角色范围](../systems/permissions-user-roles.md)的[!UICONTROL Content]权限，才能看到[!UICONTROL Edit with Page Builder]按钮并能够使用页面生成器。

有关内容管理高级工具配置选项的详细信息，请参阅&#x200B;[_配置参考指南_](../configuration-reference/general/content-management.md)。

## 配置[!DNL Page Builder]

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧面板中的&#x200B;_[!UICONTROL General]_&#x200B;下，选择&#x200B;**[!UICONTROL Content Management]**。

1. 展开![扩展选择器](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]**&#x200B;并验证&#x200B;**[!UICONTROL Enable Page Builder]**&#x200B;是否设置为`Yes`。

   ![高级内容工具](../configuration-reference/general/assets/content-management-advanced-content-tools.png){width="600" zoomable="yes"}

1. 如果您已准备好设置[!DNL Google Maps]，请执行以下操作：

   - 如有必要，请按照[获取API密钥][1]说明操作，然后复制并粘贴您的&#x200B;**[!UICONTROL Google Maps API Key]**。

   - 要更改&#x200B;**[!UICONTROL Google Maps Style]**，请粘贴由[[!DNL Google Maps] API样式向导][2]生成的JSON代码。

   >[!NOTE]
   >
   >有关在[!DNL Page Builder]内容中使用[!DNL Google Maps]的详细信息，请参阅[媒体 — 地图](map.md)。

1. 要在[!DNL Page Builder]列网格中配置准则数，请执行以下操作：

   - 对于&#x200B;**[!UICONTROL Default Column Grid Size]**，输入您希望显示在网格中的默认列数。

   - 对于&#x200B;**[!UICONTROL Maximum Column Grid Size]**，请输入网格中可用的最大列数。

   >[!NOTE]
   >
   >有关在使用[!DNL Page Builder]内容时使用列网格的详细信息，请参阅[布局 — 列](column.md)。

1. 完成后，单击&#x200B;**[!UICONTROL Save Config]**。

## 配置默认布局

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧面板中的&#x200B;_[!UICONTROL General]_&#x200B;下，选择&#x200B;**[!UICONTROL Web]**。

1. 展开![扩展选择器](../assets/icon-display-expand.png) **[!UICONTROL Default Layouts]**&#x200B;并执行以下操作：

   ![默认布局](../configuration-reference/general/assets/web-default-layouts.png){width="600" zoomable="yes"}

   有关Web配置选项的详细信息，请参阅&#x200B;[_配置参考指南_](../configuration-reference/general/web.md#default-layouts)。

   - 选择要用于产品页面的&#x200B;**[!UICONTROL Default Product Layout]**。

   - 选择要用于类别页面的&#x200B;**[!UICONTROL Default Category Layout]**。

   - 选择要用于CMS页面的&#x200B;**[!UICONTROL Default Page Layout]**。

1. 完成后，单击&#x200B;**[!UICONTROL Save Config]**。

## 禁用[!DNL Page Builder]

>[!NOTE]
>
>禁用[!DNL Page Builder]会将高级内容工具替换为WYSIWYG [编辑器](../content-design/editor.md)，并可能导致店面显示错误。 您之前使用[!DNL Page Builder]创建的内容可能无法从管理员中编辑。

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧面板中的&#x200B;_[!UICONTROL General]_&#x200B;下，选择&#x200B;**[!UICONTROL Content Management]**。

1. 展开![扩展选择器](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]**&#x200B;并将&#x200B;**[!UICONTROL Enable Page Builder]**&#x200B;设置为`No`。

1. 提示确认时，单击&#x200B;**[!UICONTROL Turn Off]**。

1. 完成后，单击&#x200B;**[!UICONTROL Save Config]**。

1. 出现提示时，[刷新](../systems/cache-management.md)任何无效的缓存。

[1]: https://developers.google.com/maps/documentation/javascript/get-api-key
[2]: https://mapstyle.withgoogle.com/

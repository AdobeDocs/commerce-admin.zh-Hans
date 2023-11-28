---
title: ’[!DNL Page Builder] 设置
description: 了解 [!DNL Page Builder] Adobe Commerce和Magento Open Source管理员中的功能配置。
exl-id: 48396045-0fef-4f4f-8138-e6d969560e42
feature: Page Builder, Configuration
source-git-commit: 2299beb6c11af801076d3aff0b026d41b9dbd212
workflow-type: tm+mt
source-wordcount: '427'
ht-degree: 0%

---

# [!DNL Page Builder] 设置

在配置中启用时， [!DNL Page Builder] 是CMS页面、块和动态块的默认内容创建工具。 此外， _[!UICONTROL Enable Advanced CMS]_按钮选件 [!DNL Page Builder] 作为“类别”和“产品”的选项。 您还可以选择缺省值 [页面布局](../content-design/page-layout.md) 要用于产品、类别和CMS页面的。 [!DNL Page Builder] 对于使用WYSIWYG的新闻稿内容不可用 [编辑者](../content-design/editor.md).

>[!NOTE]
>
>安装后， [!DNL Page Builder] 覆盖 [!UICONTROL Mask for Meta Description] 配置字段。 此值更改自 `{{name}} {{description}}` 到 `{{name}}`.
><br>
>您可以在转到以下位置时访问此设置： [!UICONTROL Stores] > _[!UICONTROL Settings]_> [!UICONTROL Configuration]，展开 [!UICONTROL Catalog]，并选择 [!UICONTROL Catalog] 下方。 此 [!UICONTROL Mask for Meta Description] 字段位于 [!UICONTROL Product Fields Auto-generation] 部分。

>[!NOTE]
>
>管理员用户必须具有 [!UICONTROL Content] 的权限 [角色范围](../systems/permissions-user-roles.md) 以查看 [!UICONTROL Edit with Page Builder] 按钮，并能够使用Page Builder。

有关内容管理高级工具配置选项的详细信息，请参见 [_配置参考指南_](../configuration-reference/general/content-management.md).

## 配置 [!DNL Page Builder]

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中的 _[!UICONTROL General]_，选择&#x200B;**[!UICONTROL Content Management]**.

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]** 并验证 **[!UICONTROL Enable Page Builder]** 设置为 `Yes`.

   ![高级内容工具](../configuration-reference/general/assets/content-management-advanced-content-tools.png){width="600" zoomable="yes"}

1. 如果您已准备好进行设置 [!DNL Google Maps]，请执行以下操作：

   - 如有必要，请按照 [获取API密钥][1] 说明，然后复制并粘贴 **[!UICONTROL Google Maps API Key]**.

   - 要更改 **[!UICONTROL Google Maps Style]**，粘贴由生成的JSON代码 [[!DNL Google Maps] API样式向导][2].

   >[!NOTE]
   >
   >请参阅 [媒体 — 地图](map.md) 有关使用的更多信息 [!DNL Google Maps] 在您的 [!DNL Page Builder] 内容。

1. 要配置 [!DNL Page Builder] 列网格，请执行以下操作：

   - 对象 **[!UICONTROL Default Column Grid Size]**，输入要在网格中显示的默认列数。

   - 对象 **[!UICONTROL Maximum Column Grid Size]**，输入网格中可用的最大列数。

   >[!NOTE]
   >
   >请参阅 [布局 — 列](column.md) 有关使用列网格的详细信息 [!DNL Page Builder] 内容。

1. 完成后，单击 **[!UICONTROL Save Config]**.

## 配置默认布局

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中的 _[!UICONTROL General]_，选择&#x200B;**[!UICONTROL Web]**.

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) **[!UICONTROL Default Layouts]** 并执行以下操作：

   ![默认布局](../configuration-reference/general/assets/web-default-layouts.png){width="600" zoomable="yes"}

   有关Web配置选项的详细信息，请参见 [_配置参考指南_](../configuration-reference/general/web.md#default-layouts).

   - 选择 **[!UICONTROL Default Product Layout]** 要用于产品页面的URL。

   - 选择 **[!UICONTROL Default Category Layout]** 要用于类别页面的URL。

   - 选择 **[!UICONTROL Default Page Layout]** 要用于CMS页面的对象。

1. 完成后，单击 **[!UICONTROL Save Config]**.

## 禁用 [!DNL Page Builder]

>[!NOTE]
>
>正在禁用 [!DNL Page Builder] 将高级内容工具替换为WYSIWYG [编辑者](../content-design/editor.md)，可能会导致店面显示错误。 您之前创建的内容 [!DNL Page Builder] 管理员可能不可编辑。

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中的 _[!UICONTROL General]_，选择&#x200B;**[!UICONTROL Content Management]**.

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]** 并设置 **[!UICONTROL Enable Page Builder]** 到 `No`.

1. 提示确认时，单击 **[!UICONTROL Turn Off]**.

1. 完成后，单击 **[!UICONTROL Save Config]**.

1. 出现提示时， [刷新](../systems/cache-management.md) 任何无效缓存。

[1]: https://developers.google.com/maps/documentation/javascript/get-api-key
[2]: https://mapstyle.withgoogle.com/

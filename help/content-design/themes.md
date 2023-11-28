---
title: 主题
description: 了解 [!DNL Commerce] 主题，包括布局文件、模板文件、翻译文件以及定义商店外观的外观。
exl-id: d2ccff51-5019-4f80-8eaa-3fe50d5cd6cc
feature: Page Content, Themes
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '433'
ht-degree: 0%

---

# 主题

主题是确定商店视觉呈现方式的文件集合。 首次安装时 [!DNL Commerce]，则该存储库的设计元素基于 _默认_ 主题。 除了您的电子邮件所附的初始默认主题之外， [!DNL Commerce] 安装时，您可以使用多种可用的主题 _原样_ 或根据您的需求进行修改。

响应式主题调整页面布局以适合设备的视图端口。 示例 _Luma_ 主题具有灵活的响应式布局，可以从桌面、平板电脑或移动设备中查看。

[!DNL Commerce] 主题包括布局文件、模板文件、翻译文件和外观。 外观是支持CSS、图像和JavaScript文件的集合，这些文件共同创建客户访问您的商店时体验的可视展示和交互。 理解Commerce主题设计且具有服务器访问权限的开发人员或设计专业人员可以修改和自定义主题和外观。 要了解更多信息，请参阅 [_前端开发人员指南_](https://developer.adobe.com/commerce/frontend-core/guide/themes/).

![Luma主题](./assets/design-responsive.png){width="600" zoomable="yes"}

## 默认主题

此 `Magento Blank` 响应式主题呈现不同设备的店面显示，并融合了桌面、表格和移动设备的最佳实践。 某些主题仅设计用于特定设备。 时间 [!DNL Commerce] 检测特定浏览器ID或用户代理，它会使用为特定浏览器配置的主题。 搜索字符串还可以包含与Perl兼容的正则表达式(PCRE)。

![主题](./assets/themes.png){width="700" zoomable="yes"}

### 筛选主题网格

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Themes]**.

1. 单击 **[!UICONTROL Filters]**.

1. 输入ID范围、主题名称（或标题）、文件夹路径或父主题。

1. 单击 **[!UICONTROL Apply Filters]** 更新主题列表。

## 查看当前主题设置

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Themes]**.

1. 在已安装的主题列表中，找到要检查的主题，然后单击行以显示设置。

1. 要查看示例页面，请单击 **[!UICONTROL Theme Preview Image]**.

![预览主题](./assets/theme-settings.png){width="600" zoomable="yes"}

## 应用默认主题

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. 查找要配置的商店视图，然后单击 **[!UICONTROL Edit]** 在 _[!UICONTROL Action]_列。

1. 下 _[!UICONTROL Default Theme]_，设置&#x200B;**[!UICONTROL Applied Theme]**到要用于当前视图的。

   ![应用的主题](./assets/theme-default-apply.png){width="600" zoomable="yes"}

1. 完成后，单击 **[!UICONTROL Save Configuration]**.

## 添加用户代理规则

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. 下 _[!UICONTROL Design Rule]_，单击&#x200B;**[!UICONTROL Add New User Agent Rule]**.

   ![设计规则](./assets/theme-design-rule.png){width="600" zoomable="yes"}

1. 对象 **[!UICONTROL Search String]**，输入特定设备的浏览器ID。

   搜索字符串按输入顺序进行匹配。 例如，对于Firefox，输入：

   `/^mozilla/i`

1. 要输入其他设备，请重复此过程。

1. 完成后，单击 **[!UICONTROL Save Configuration]**.

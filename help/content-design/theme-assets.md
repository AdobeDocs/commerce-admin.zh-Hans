---
title: 主题资产
description: 了解如何管理主题资产，如CSS、字体、图像和JavaScript文件。
exl-id: 326c648e-eace-45a0-b53d-bbc8702fee05
feature: Page Content, Themes
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '464'
ht-degree: 0%

---

# 主题资产

此 _静态文件_ 是主题使用的资产（如CSS、字体、图像和JavaScript）的集合。 静态文件的位置在 [基本URL](../stores-purchase/store-urls.md) 配置。 您可以向每个静态文件的URL添加数字签名，以便浏览器能够检测到较新版本何时可用。 如果签名与浏览器缓存中存储的签名不同，则使用较新版本的文件。

对于标准安装，与主题关联的资产将整理在 `web` 文件夹，该文件夹位于 [!DNL Commerce] 根。

`[commerce_root]/app/design/frontend/Magento/[theme_name]/web`

## 向静态文件URL添加数字签名

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中，展开 **[!UICONTROL Advanced]** 并选择 **[!UICONTROL Developer]**.

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Static Files Settings]** 部分。

   ![静态文件设置](./assets/developer-static-files-settings.png){width="500" zoomable="yes"}

1. 设置 **[!UICONTROL Sign Static Files]** 到 `Yes`.

1. 完成后，单击 **[!UICONTROL Save Config]**.

| 文件类型 | 描述 |
|--- |--- |
| CSS | 控制与外观关联的视觉样式。 服务器上的示例位置： `[commerce]/app/design/frontend/Magento/[theme]/web/css` |
| 字体 | 提供主题可用的字体。 服务器上的位置： `[commerce]/app/design/frontend/Magento/[theme]/web/fonts` |
| 图像 | 提供主题使用的图形资源，包括按钮、背景纹理等。 服务器上的示例位置： `[commerce]/app/design/frontend/Magento/[theme]/web/images` |
| JS | 特定于主题的JavaScript例程和可调用函数。 服务器上的示例位置： `[commerce]/app/design/frontend/Magento/[theme]/web/js` |

{style="table-layout:auto"}

## 合并CSS文件

作为优化网站并减少页面加载时间努力的一部分，您可以通过将CSS文件合并到单个压缩文件来减少单独的CSS文件数量。 如果打开合并的CSS文件，您会看到一个连续的文本流，其中删除了换行符。 您无法编辑合并的文件，因此最好等到退出开发模式并且不再频繁更改CSS。

>[!NOTE]
>
>CSS文件可合并自 _管理员_ 仅在使用时面板 [开发者模式](../systems/developer-tools.md#operation-modes).

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中， **[!UICONTROL Advanced]** 并选择 **[!UICONTROL Developer]**.

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL CSS Settings]** 部分。

   ![CSS设置](./assets/developer-css-settings.png){width="500" zoomable="yes"}

   有关这些配置选项的详细说明，请参阅 [CSS设置](../configuration-reference/advanced/developer.md#css-settings) 在 _配置引用_.

1. 设置 **[!UICONTROL Merge CSS Files]** 到 `Yes`.

1. 完成后，单击 **[!UICONTROL Save Config]**.

## 合并JavaScript文件

可以将多个JavaScript文件合并到单个压缩文件中，以缩短页面加载时间。 如果打开合并的JavaScript文件，您会看到一个连续的文本流，其中删除了换行符。 如果您已完成开发过程并且代码不含错误，则可以考虑合并文件。

>[!NOTE]
>
>JavaScript文件可以从 _管理员_ 仅在使用时面板 [开发人员模式](../systems/developer-tools.md#operation-modes).

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中， **[!UICONTROL Advanced]** 并选择 **[!UICONTROL Developer]**.

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL JavaScript Settings]** 部分。

   ![JavaScript设置](./assets/developer-javascript-settings.png){width="600" zoomable="yes"}

   有关这些配置选项的详细说明，请参阅 [JavaScript设置](../configuration-reference/advanced/developer.md#javascript-settings) 在 _配置引用_.

1. 设置 **[!UICONTROL Merge JavaScript Files]** 到 `Yes`.

1. 完成后，单击 **[!UICONTROL Save Config]**.

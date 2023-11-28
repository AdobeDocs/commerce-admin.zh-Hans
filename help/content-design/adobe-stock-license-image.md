---
title: 许可Adobe Stock图像
description: 要确保您具有合法访问权限并消除Adobe Stock水印，请许可您的Adobe Stock图像。
exl-id: a2d6b7b8-e9ac-4f3e-bcd1-05e2bb74b6c2
feature: CMS, Media
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 0%

---

# 许可Adobe Stock图像

您要用于生产Adobe Commerce和Magento Open Source商店的Adobe Stock资源应当获得许可。 此许可确保您有权合法访问图像，并消除所有图像上存在的Adobe Stock水印 [图像预览][save-preview]. 要许可图像或保存已获得许可的图像，您必须登录到您的Adobe帐户。

新 [[!DNL Media Gallery]](media-gallery.md) 提供了与Adobe Stock的直接集成，从而能够轻松地直接从图库页面许可您的图像。

## 先决条件

此功能需要 [Adobe Stock集成][adobe-stock-integration] 模块和配置。 许可 [Adobe Stock][adobe-stock] 图像需要付费Adobe Stock计划和 [Adobe帐户][adobe-signin].

## 从新授权图像 [!DNL Media Gallery]

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**.

1. 按照上的步骤操作 [使用Adobe Stock图像][using-adobe-stock] 以登录并将预览图像保存到 [媒体存储][media-storage].

   ![已保存的预览图像](./assets/adobe-stock-gallery-unlicensed.png){width="600" zoomable="yes"}

1. 单击图像下方的三个圆点(![资产菜单图标](./assets/media-gallery-asset-menu-icon.png){width="10" zoomable="no"})，然后单击 **[!UICONTROL License]**.

   ![Adobe Stock图像操作](./assets/adobe-stock-gallery-image-actions.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >如果您未登录，则会显示登录表单。 有关登录的详细信息，请参阅 [使用Adobe Stock图像][using-adobe-stock].

1. 在许可确认对话框中，单击 **[!UICONTROL Confirm]** 以许可图像。

   ![许可证确认](./assets/adobe-stock-gallery-license-confirm.png){width="350" zoomable="yes"}

   >[!NOTE]
   >
   >您必须具有可用的 [Adobe Stock积分][stock-credits] 在您的帐户中授权图像。

## 从标准媒体存储中许可图像

1. [访问Adobe Stock搜索网格][access-search].

1. 至 [查看图像详细信息][view-details]，按顺序单击搜索网格中的图像。

1. 根据映像的当前许可状态，执行以下操作之一：

   - 如果图像已获得许可，请单击 **[!UICONTROL Save]**.

   - 如果图像为 _非_ 已许可，请单击 **[!UICONTROL License and Save]**.

     >[!NOTE]
     >
     >您必须具有可用的 [Adobe Stock积分][stock-credits] 在您的帐户中授权图像。

   此操作会显示一个提示，提示您指定用于将图像保存到的文件名 [媒体存储][media-storage]. 提供了默认的文件名，但可以根据您的首选项自定义名称。

   ![保存Adobe Stock许可图像](./assets/adobe-stock-save-licensed.png){width="550" zoomable="yes"}

1. 单击 **[!UICONTROL Confirm]**.

   页面将重定向到媒体存储，并且会显示您保存的预览。

[adobe-stock-integration]: adobe-stock.md
[media-storage]: media-storage.md
[using-adobe-stock]: adobe-stock-manage.md
[save-preview]: adobe-stock-save-preview.md
[access-search]: adobe-stock-manage.md#access-the-adobe-stock-search-grid
[view-details]: adobe-stock-manage.md#view-image-details
[stock-credits]: https://helpx.adobe.com/stock/help/credit-packs.html
[adobe-stock]: https://stock.adobe.com
[adobe-signin]: https://helpx.adobe.com/manage-account/using/access-adobe-id-account.html

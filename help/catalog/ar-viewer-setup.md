---
title: 用于Adobe Commerce设置的“[!DNL AR Viewer]”
description: 了解如何使用产品列表的 [!DNL AR Viewer] 扩展管理3D模型资源。
exl-id: e3f081ff-b994-4842-a1f3-613012d33a9c
source-git-commit: f84667a7bbc93504499279d77967796bcd11791c
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 0%

---

# 使用Adobe Commerce的[!DNL AR Viewer]管理产品3D模型

对于每个产品，您可以上传一个`.USDZ`文件，以便在产品列表中使用AR和3D模型。

[!DNL AR Viewer]仅支持`.USDZ`个文件。

## 安装扩展

[!DNL AR Viewer]已作为扩展从[Adobe Commerce Marketplace](https://commercemarketplace.adobe.com/magento-module-arviewer.html){target=_blank}安装。

有关扩展安装过程的详细信息，请参阅&#x200B;[_安装指南_](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html)。

安装并配置[!DNL AR Viewer]扩展后，管理员用户可以设置、自定义和管理产品列表以包含3D模型。

## 添加3D模型

1. 在编辑模式下打开产品。

1. 若要使用特定的商店视图，请将&#x200B;**[!UICONTROL Store View]**&#x200B;选择器设置为适用的视图。

   >[!NOTE]
   >
   >新产品3D模型在&#x200B;_所有_&#x200B;商店视图中都是&#x200B;_始终_&#x200B;已上传和可见的，即使未使用`All Store Views`范围进行上传。 <br/><br/>要从特定商店视图中隐藏任何产品3D模型，您必须切换到该商店视图，选中3D模型的&#x200B;**[!UICONTROL Hide from Product Page]**&#x200B;复选框，然后单击&#x200B;**[!UICONTROL Save]**。

1. 向下滚动并展开&#x200B;_[!UICONTROL Product 3D Model]_&#x200B;部分。

   ![菜单弹出窗口](assets/ar-viewer-product-options.png){width="700" zoomable="yes"}

1. 添加产品的3D模型（`.USDZ`文件）。

1. 单击&#x200B;**[!UICONTROL Save]**。

### 删除3D模型

要从产品详细信息中删除3D模型，请执行以下操作：

1. 单击&#x200B;**[!UICONTROL Delete]**。

1. 单击&#x200B;**[!UICONTROL Save]**。

## 查看产品3D模型

当使用3D模型更新产品详细信息时：

1. [!DNL AR Viewer]在产品描述中生成一个对AR文件进行编码的二维码。

1. 客户可在产品页面中看到此二维码。

1. 当客户使用移动设备扫描二维码时，将在移动设备上呈现AR体验。

>[!NOTE]
>
> 有关将3d模型添加到产品的用户的一系列演示视频，请参阅&#x200B;_Adobe Commerce视频和Tutorials_&#x200B;中的[Commerce的AR查看器](https://experienceleague.adobe.com/docs/commerce-learn/tutorials/catalog/augmented-reality.html)页。

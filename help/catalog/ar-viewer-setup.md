---
title: ’[!DNL AR Viewer] (适用于Adobe Commerce设置)
description: 了解如何使用管理3D模型资源 [!DNL AR Viewer] 产品列表的扩展。
exl-id: e3f081ff-b994-4842-a1f3-613012d33a9c
source-git-commit: f84667a7bbc93504499279d77967796bcd11791c
workflow-type: tm+mt
source-wordcount: '307'
ht-degree: 0%

---

# 使用管理产品3D模型 [!DNL AR Viewer] 适用于Adobe Commerce的

对于每个产品，您可以上传 `.USDZ` 文件允许在产品列表中使用AR和3D模型。

此 [!DNL AR Viewer] 仅支持 `.USDZ` 文件。

## 安装扩展

[!DNL AR Viewer] 作为扩展进行安装，可从 [Adobe Commerce市场](https://commercemarketplace.adobe.com/magento-module-arviewer.html){target=_blank}.

请参阅 [_安装指南_](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html) 以了解有关扩展安装过程的更多信息。

在 [!DNL AR Viewer] 安装并配置了扩展，管理员用户可以设置、自定义和管理产品列表以包含3D模型。

## 添加3D模型

1. 在编辑模式下打开产品。

1. 要使用特定的商店视图，请设置 **[!UICONTROL Store View]** 选择适用的视图。

   >[!NOTE]
   >
   >新产品3D模型包括 _始终_ 已上传并在中可见 _所有_ 商店视图，即使 `All Store Views` 范围不用于上传。 <br/><br/>要从特定商店视图中隐藏任何产品3D模型，您必须切换到该“商店视图”，选择 **[!UICONTROL Hide from Product Page]** 复选框，然后单击 **[!UICONTROL Save]**.

1. 向下滚动并展开 _[!UICONTROL Product 3D Model]_部分。

   ![菜单弹出菜单](assets/ar-viewer-product-options.png){width="700" zoomable="yes"}

1. 添加3D模型(`.USDZ` 文件)。

1. 单击 **[!UICONTROL Save]**.

### 删除3D模型

要从产品详细信息中删除3D模型，请执行以下操作：

1. 单击 **[!UICONTROL Delete]**.

1. 单击 **[!UICONTROL Save]**.

## 查看产品3D模型

当使用3D模型更新产品详细信息时：

1. 此 [!DNL AR Viewer] 在产品描述中生成一个二维码，用于编码AR文件。

1. 客户可在产品页面中看到此二维码。

1. 当客户使用移动设备扫描二维码时，将在移动设备上呈现AR体验。

>[!NOTE]
>
> 有关用户将3d模型添加到产品的一系列演示视频，请参阅 [Adobe Commerce的AR查看器](https://experienceleague.adobe.com/docs/commerce-learn/tutorials/catalog/augmented-reality.html) 页面位置 _Commerce视频和Tutorials_.

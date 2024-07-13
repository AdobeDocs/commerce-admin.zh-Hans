---
title: 用于Adobe Commerce的“[!DNL AR Viewer]”
description: 了解 [!DNL AR Viewer] 如何使您的Adobe Commerce实例受益，以及如何成功载入和设置扩展。
exl-id: 9f9f3ff3-2402-4f70-9fc7-031dd2bb3916
source-git-commit: f84667a7bbc93504499279d77967796bcd11791c
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 0%

---

# Adobe Commerce的[!DNL AR Viewer]

增强现实(AR)描述用户体验，这些体验通过设备摄像头将2D或3D元素添加到实时视图中，其方式使这些元素看起来像是生活在现实世界中。

适用于Adobe Commerce的[!DNL AR Viewer]扩展支持无缝体验，旨在为用户显示渲染的3D图形。

本指南中的信息概述了Adobe Commerce中[!DNL AR Viewer]的入门体验以及[!DNL AR Viewer]如何让用户受益，并提供了在该历程中遵循的最佳实践。

由Pixar开发的[Universal Scene Description (USD)](https://www.pixar.com/usd){target=_blank}是第一个可以强壮且可缩放地交换可能由许多不同资产、源和动画组成的3D场景的开源软件，同时支持高度协作的工作流。 此USD在`.USDZ`文件内使用。 此`.USDZ`文件将AR和3D内容交付给用户的设备。

>[!NOTE]
>
> [!DNL AR Viewer]仅支持`.USDZ`个文件。

## [!DNL AR Viewer]要求

[!DNL AR Viewer]与[!DNL Magento Open Source]和Adobe Commerce都兼容。 有关支持的版本的详细信息，请参阅[生命周期策略](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/lifecycle-policy.html){target=_blank}。

有关详细信息，请参阅[安装 [!DNL AR Viewer] 扩展](../catalog/ar-viewer-setup.md)。

要使用[!DNL AR Viewer]，您必须具备可用于实例的以下项：

* PHP 8.1.0
* Adobe Commerce版本2.4.4及更高版本
* Magento Open Source(CE)版本2.4.x

## 兼容性限制

[!DNL AR Viewer]现有兼容性限制：

* 仅限`.USDZ`：此功能仅支持`.USDZ`文件。
* `qr-code`：需要`endroid/qr-code`版本4.5。
* `Catalog module`：需要`magento/module-catalog`版本104.0.0。

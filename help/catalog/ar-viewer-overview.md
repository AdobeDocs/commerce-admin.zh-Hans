---
title: ’[!DNL AR Viewer] (适用于Adobe Commerce)
description: 了解如何 [!DNL AR Viewer] 可能会对您的Adobe Commerce实例以及如何成功载入和设置扩展有所帮助。
exl-id: 9f9f3ff3-2402-4f70-9fc7-031dd2bb3916
source-git-commit: f84667a7bbc93504499279d77967796bcd11791c
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 0%

---

# [!DNL AR Viewer] 适用于Adobe Commerce的

增强现实(AR)描述用户体验，这些体验通过设备摄像头将2D或3D元素添加到实时视图中，其方式使这些元素看起来像是生活在现实世界中。

此 [!DNL AR Viewer] for Adobe Commerce扩展提供了无缝体验，旨在为用户显示渲染的3D图形。

本指南中的信息概述了的入门体验 [!DNL AR Viewer] 以及Adobe Commerce的 [!DNL AR Viewer] 有益于用户，以及在这一历程中遵循的最佳实践。

由皮克斯开发， [通用场景描述(USD)](https://www.pixar.com/usd){target=_blank} 是第一个可以强有力且可缩放地交换3D场景的开源软件，这些场景可能由许多不同的资产、来源和动画组成，同时促进高度协作的工作流。 本美元的使用范围 `.USDZ` 文件。 此 `.USDZ` 文件将AR和3D内容交付到用户的设备。

>[!NOTE]
>
> 此 [!DNL AR Viewer] 仅支持 `.USDZ` 文件。

## [!DNL AR Viewer] 要求

此 [!DNL AR Viewer] 与两者都兼容 [!DNL Magento Open Source] 和Adobe Commerce。 请参阅 [生命周期政策](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/lifecycle-policy.html){target=_blank} 有关支持的版本的详细信息。

请参阅 [安装 [!DNL AR Viewer] 扩展](../catalog/ar-viewer-setup.md) 以了解更多信息。

要使用 [!DNL AR Viewer]中，您必须为实例提供以下内容：

* PHP 8.1.0
* Adobe Commerce版本2.4.4及更高版本
* Magento Open Source(CE)版本2.4.x

## 兼容性限制

[!DNL AR Viewer] 现有兼容性限制：

* `.USDZ` 仅限：此功能仅支持 `.USDZ` 文件。
* `qr-code`：需要 `endroid/qr-code` 版本4.5。
* `Catalog module`：需要 `magento/module-catalog` 版本104.0.0。

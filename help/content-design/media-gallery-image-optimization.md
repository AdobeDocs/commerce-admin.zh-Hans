---
title: 媒体集图像优化
description: 了解如何对 [!DNL Commerce] 媒体资源使用图像优化。
exl-id: ba75e90a-406b-4b14-b049-0b78c4a27188
feature: Page Content, Media
badgePaas: label="仅限PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="仅适用于云项目（Adobe管理的PaaS基础架构）和内部部署项目上的Adobe Commerce 。"
TQID: https://experienceleague.adobe.com/BTjXX6X70q2Mwm0xPNx-t429R5m93VprCHBDcYgQNpY
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 211
ht-degree: 0%

---

# 媒体集图像优化

新[媒体集](media-gallery.md)提供了&#x200B;_图像优化_&#x200B;功能，该功能可提高性能并降低店面上的媒体文件大小。 此优化默认处于启用状态，并可在存储配置设置中进行修改。

## 配置图像优化

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧面板中，展开&#x200B;**[!UICONTROL Advanced]**&#x200B;并选择&#x200B;**[!UICONTROL System]**。

1. 展开![扩展选择器](../assets/icon-display-expand.png) **[!UICONTROL Media Gallery Image Optimization]**&#x200B;并执行以下操作：

   - 将&#x200B;**[!UICONTROL Enable Image Optimization]**&#x200B;设置为`Yes`。
   - 根据需要输入&#x200B;**[!UICONTROL Maximum Width]**&#x200B;和&#x200B;**[!UICONTROL Maximum Height]**&#x200B;值（以像素为单位）。

## 行为

启用媒体集图像优化功能后，会自动将图像的优化副本插入[媒体集](media-gallery.md)中的内容，而不是原始文件。

当配置中的&#x200B;_最大宽度_&#x200B;和&#x200B;_最大高度_&#x200B;值更改时，它会更新之前插入的所有现有优化图像。

媒体集图像优化要求在配置更改时运行`media.gallery.renditions.update`队列使用者以重新生成优化图像。 有关详细信息，请参阅&#x200B;_配置指南_&#x200B;中的[管理消息队列](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html)。

{{$include /help/_includes/image-optimization-animated-gif-note.md}}

<!-- Last updated from includes: 2024-01-30 15:43:39 -->

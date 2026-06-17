---
title: 目录事件轮播小组件
description: 了解如何使用目录事件轮播小组件在页面上显示即将举行的事件的滑块。
exl-id: 4e88b253-f320-4c94-9996-94d7005effc6
feature: Page Content, Promotions/Events
badgePaas: label="仅限PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="仅适用于云项目（Adobe管理的PaaS基础架构）和内部部署项目上的Adobe Commerce 。"
TQID: https://experienceleague.adobe.com/vXrTBTqPkpIevzmmE-iHnFkqjpKSV6ynK027M404a7c
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 478
ht-degree: 0%

---

# 目录事件轮播小组件

{{ee-feature}}

目录事件轮播小组件显示即将发生的事件的滑块，其中每个事件都有一个倒计时滚动条。 您可以选择您希望轮播显示的页面布局的页面和区域，并控制同时显示的事件的宽度和数量。 您得到的结果取决于您的主题、主题在页面上出现的位置以及您选择的选项。

在左侧边栏中![事件轮播](./assets/storefront-event-carousel-sidebar-gear.png){width="700" zoomable="yes"}

## 步骤1：启用目录轮播小组件

在开始之前，请按照[说明](../merchandising-promotions/event-configure.md)配置&#x200B;_目录事件_&#x200B;构件，使其为店面启用。

![目录事件配置](./assets/config-catalog-catalog-events-1.png){width="500" zoomable="yes"}

## 第2步：创建构件

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**。

1. 单击右上角的&#x200B;**[!UICONTROL Add Widget]**。

1. 在&#x200B;_[!UICONTROL Settings]_&#x200B;部分中，执行以下操作：

   - 将&#x200B;**[!UICONTROL Type]**&#x200B;设置为`Catalog Events Carousel`。

   - 选择商店使用的&#x200B;**[!UICONTROL Design Theme]**。

1. 单击&#x200B;**[!UICONTROL Continue]**。

   ![事件轮播的小组件设置](./assets/widget-event-carousel-settings.png){width="500" zoomable="yes"}

1. 在&#x200B;_[!UICONTROL Storefront Properties]_&#x200B;部分中，执行以下操作：

   - 对于&#x200B;**[!UICONTROL Widget Title]**，输入小部件的描述性标题。

     此标题仅在&#x200B;_管理员_&#x200B;中可见。

   - 对于&#x200B;**[!UICONTROL Assign to Store Views]**，选择您希望小组件可见的存储区视图。

     您可以选择特定的商店视图，或`All Store Views`。 要选择多个视图，请按住Ctrl键(PC)或Command键(Mac)并单击每个选项。

   - （可选）为&#x200B;**[!UICONTROL Sort Order]**&#x200B;输入一个数字，以确定该项在页面的同一部分中与其他项一起出现的顺序。 （`0` =第一，`1` =第二，`3` =第三，依此类推。）

     ![小组件店面属性](./assets/widget-event-carousel-storefront-properties.png){width="600" zoomable="yes"}

## 步骤3：选择位置

1. 在&#x200B;_布局更新_&#x200B;分区中，单击&#x200B;**[!UICONTROL Add Layout Update]**。

1. 将&#x200B;**[!UICONTROL Display On]**&#x200B;设置为`Specified Page`。

1. 将&#x200B;**[!UICONTROL Page]**&#x200B;设置为`CMS Home Page`。

1. 将&#x200B;**[!UICONTROL Container]**&#x200B;设置为以下项之一：

   - `Main Content Area`
   - `Sidebar Additional`
   - `Sidebar Main`

   >[!NOTE]
   >
   >结果因主题和页面布局而异。 您还必须在类别配置中指定&#x200B;_[!UICONTROL Catalog Events Carousel Default Template]_。

1. 如果您希望事件轮播显示在店面的其他位置，请单击&#x200B;**[!UICONTROL Add Layout Update]**，然后对该位置重复这些步骤。

   ![布局更新](./assets/widget-event-carousel-layout-updates-catalog-category-sidebar.png){width="600" zoomable="yes"}

1. 单击&#x200B;**[!UICONTROL Save and Continue Edit]**。

   现在，您可以忽略消息以刷新缓存。

## 步骤4：配置选项

1. 在左侧面板中，选择&#x200B;**[!UICONTROL Widget Options]**。

1. 对于&#x200B;**[!UICONTROL Frame Size]**，输入要在滑块中同时列出的事件数。

   要一次只查看一个事件，请输入`1`。

1. 对于&#x200B;**[!UICONTROL Scroll]**，输入每次点击要滚动的事件列表数量。

   要滚动到下一个事件，请输入`1`。

1. 对于自定义宽度，输入&#x200B;**[!UICONTROL Block Custom Width]**&#x200B;的像素数。

   在以下示例页面上，自定义宽度设置为250像素。

   ![自定义宽度构件选项](./assets/widget-options-custom-width.png){width="400" zoomable="yes"}

1. 完成后，单击&#x200B;**[!UICONTROL Save]**。

1. 提示刷新缓存时，单击页面顶部消息中的链接，然后按照说明操作。

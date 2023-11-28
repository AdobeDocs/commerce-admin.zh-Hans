---
title: 动态块
description: 使用动态块创建由价格规则和客户区段中的逻辑驱动的丰富交互式内容。
exl-id: 0c842ad9-2e46-48aa-9a12-2f74a54c352e
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '629'
ht-degree: 0%

---

# 动态块

{{ee-feature}}

创建由以下项的逻辑驱动的丰富交互式内容 [价格规则](../merchandising-promotions/introduction.md#price-rules) 和 [客户区段](../customers/customer-segments.md). 现有 [动态块](../page-builder/dynamic-block.md) 可以直接添加到 [!DNL Page Builder] [阶段](../page-builder/workspace.md). 有关使用动态块的详细分步示例，请参阅 [教程2：块](../page-builder/2-blocks.md).

>[!NOTE]
>
>此 _[!UICONTROL Banner]_中的选项 [[!UICONTROL Content] 菜单](content-menu.md) 在2.3.1中已弃用，在2.4.0中已移除。其功能已被动态块取代。

![[!DNL Page Builder]  — 包含价格规则和客户区段的动态块](../page-builder/assets/pb-tutorial2-dynamic-block-storefront.png){width="600" zoomable="yes"}

## 步骤1：创建动态块

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Dynamic Blocks]**.

   ![动态块列表](../page-builder/assets/pb-tutorial2-block-dynamic-add.png){width="600" zoomable="yes"}

1. 在右上角，单击 **[!UICONTROL Add Dynamic Block]**.

   ![新建动态块](../page-builder/assets/pb-tutorial2-block-dynamic-new.png){width="600" zoomable="yes"}

1. 如果适用，请设置 **[!UICONTROL Store View]** 到要显示动态块的特定商店视图。

1. 要激活动态块，请设置 **[!UICONTROL Enable Dynamic Block]** 到 `Yes`.

1. 要供内部参考，请输入描述性 **[!UICONTROL Dynamic Block Name]**.

1. 设置 **[!UICONTROL Dynamic Block Type]** 到您希望显示动态块的页面区域，然后单击 **[!UICONTROL Done]**.

   ![设置动态块类型](../page-builder/assets/pb-dynamic-block-type.png){width="500" zoomable="yes"}

1. 在 **[!UICONTROL Customer Segment]** 列表中，选中要查看动态块的每个区段的复选框，然后单击 **[!UICONTROL Done]** 以保存设置。

   ![选择客户区段](../page-builder/assets/pb-dynamic-block-customer-segment.png){width="500" zoomable="yes"}

   >[!NOTE]
   >
   >- 如果未创建区段，则该动态块对每个人都可见。
   >- 如果客户不属于任何区段，并且已为所有区段创建了动态块，则仍会显示动态块的内容。
   >- 如果删除了分配给某个动态块的所有客户区段，则其内容对所有人可见。

### 在动态块中使用Real-Time CDP受众

如果您 [已安装](../customers/audience-activation.md#install-the-extension) 和 [已配置](../customers/audience-activation.md#configure-the-extension) 该 [!DNL Audience Activation] 扩展中，您会看到一个名为 **[!UICONTROL Audiences]**.

![选择Real-Time CDP受众](./assets/dynamic-block-rtcdp.png){width="600" zoomable="yes"}

在 **[!UICONTROL Real-Time CDP Audience]** 列表上，选中要查看动态块的每个受众的复选框，然后单击 **[!UICONTROL Done]** 以保存设置。

## 第2步：完成内容

使用 [!DNL Page Builder] [工作区](../page-builder/workspace.md) 以完成内容。

![[!DNL Page Builder]  — 动态块工作区](../page-builder/assets/pb-dynamic-block-workspace.png){width="600" zoomable="yes"}

## 步骤3：选择相关促销

1. 向下滚动并展开 ![扩展选择器](../assets/icon-display-expand.png) **[!UICONTROL Related Promotions]**.

1. 单击要与动态块关联的促销活动类型：

   - **[!UICONTROL Add Cart Price Rules]** (请参阅 [购物车价格规则](../merchandising-promotions/price-rules-cart.md))

   - **[!UICONTROL Add Catalog Price Rules]** (请参阅 [目录价格规则](../merchandising-promotions/price-rules-catalog.md))

   >[!NOTE]
   >
   >Real-Time CDP受众不支持目录价格规则。

1. 在可用规则列表中，选中要使用的每个规则的复选框，然后单击 **[!UICONTROL Add Selected]**.

1. 动态块完成后，单击 **[!UICONTROL Save]**.

## 步骤4：将动态块添加到页面

1. 打开要在其中显示动态块的页面。

1. 使用 [[!UICONTROL Add Dynamic Block]](../page-builder/dynamic-block.md) 内容类型，用于将动态块添加到暂存环境。

## 字段和工具描述

| 字段 | 描述 |
|--- |--- |
| [!UICONTROL Store View] | 指定动态块将可用的存储视图。 |
| [!UICONTROL Enable Dynamic Block] | 激活或停用动态块。 选项：是/否 |
| [!UICONTROL Dynamic Block Name] | 在管理员中标识动态块的描述性名称。 |
| [!UICONTROL Dynamic Block Type] | 标识 [标准页面布局](layout-updates.md) 放置动态块的位置。 选项： <br/>**[!UICONTROL Content Area]**— 将动态块放置在主区域中 [内容区域](layout-updates.md) 页面的。<br/>**[!UICONTROL Footer]**  — 将动态块放置在页面中 [页脚](page-setup.md#footer). <br/>**[!UICONTROL Header]**— 将动态块放置在页面中 [标题](page-setup.md#header).<br/>**[!UICONTROL Left Column]**  — 将动态块放入 [左侧边栏](page-layout.md#standard-page-layouts) 两列或三列的布局。 <br/>**[!UICONTROL Right Column]**— 将动态块放入 [右侧边栏](page-layout.md#standard-page-layouts) 两列或三列的布局。 |
| 客户区段 | 将客户区段与动态块关联以确定哪些客户可以看到它。 |
| Real-Time CDP受众 | 联营公司a [Real-Time CDP受众](../customers/audience-activation.md) ，以确定哪些客户可以看到它。 |

{style="table-layout:auto"}

### 目录

| 字段 | 描述 |
|--- |--- |
| [!UICONTROL Layout] | 向舞台中添加行、列或选项卡。 |
| [!UICONTROL Elements] | 将文本、标题、按钮、分隔符和HTML代码添加到舞台上的任何布局容器中。 |
| [!UICONTROL Media] | 将图像、视频、横幅、滑块和Google映射添加到舞台上的任何现有布局容器。 |
| [!UICONTROL Add Content] | 将现有块、动态块和产品添加到暂存器。 |

{style="table-layout:auto"}

### 相关促销活动

| 字段 | 描述 |
|--- |--- |
| [!UICONTROL Related Cart Price Rule] | **[!UICONTROL Add Cart Price Rules]**  — 关联现有的 [购物车价格规则](../merchandising-promotions/price-rules-cart.md) 将动态块作为促销活动。 |
| [!UICONTROL Related Catalog Price Rule] | **[!UICONTROL Add Catalog Price Rules]**  — 关联现有的 [目录价格规则](../merchandising-promotions/price-rules-catalog.md) 将动态块作为促销活动。 |

{style="table-layout:auto"}

---
title: 页面布局
description: 了解页面布局区域以及如何配置默认布局。
exl-id: 397a92cf-6f20-4729-8d7c-c5f672fc1c9a
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '871'
ht-degree: 0%

---

# 页面布局

商店中每个页面的布局由不同的部分或容器组成，这些部分或容器定义页面的页眉、页脚和内容区域。 根据布局，每个页面可能包含一列、两列、三列或更多列。 您可以将该布局视为 _平面图_ ，并分配特定布局以用作CMS、产品和类别页面的默认布局。

在页面上，内容块会浮动以填充可用空间，具体情况可根据 [页面布局](layout-updates.md) 指定显示它们的位置。 请注意，如果将布局从三列更改为两列，则主区域的内容将展开以填充可用空间。 另请注意，与未使用的侧栏关联的任何块似乎都消失了。 但是，如果恢复三列布局，块会重新出现。 这种流动进刀，或 _液体布局_，无需重新处理内容即可更改页面布局。 如果您习惯于使用单个HTML页，则此模块化、 _构建基块_ 方法需要不同的思维方式。

![带左栏页面布局的标准两列](./assets/storefront-2-column-ee.png){width="700" zoomable="yes"}

## 配置默认布局

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中的 _[!UICONTROL General]_，选择&#x200B;**[!UICONTROL Web]**.

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Default Layouts]** 部分。

   ![默认布局](./assets/web-default-layouts.png){width="600" zoomable="yes"}

1. 选择 **[!UICONTROL Default Product Layout]** 要用于产品页面的URL。

   此设置确定默认用于产品页面的布局。

   - `No layout updates`  — 布局更新不适用于产品页面。
   - `Empty`  — 对产品页面使用空白布局。
   - `1 column`  — 对产品页面使用单列布局。
   - `2 columns with left bar`  — 对于产品页面，使用左侧带有侧栏的双列布局。
   - `2 columns with right bar`  — 对于产品页面，使用右侧带有侧栏的双列布局。
   - `3 columns`  — 对于产品页面，使用左右两侧带有侧栏的三列布局。

   时间 [页面生成器](../page-builder/introduction.md) 已启用，则还有其他完整的宽度选项可用。 然后，您可以使用页面生成器内容工具来设计产品页面的布局。

   - `Page -- Full Width`  — 使用 _页面 — 全宽_  产品页面的布局。
   - `Category -- Full Width`  — 使用 _类别 — 完整宽度_ 产品页面的布局。
   - `Product -- Full Width`  — （推荐）使用 _产品 — 完整宽度_ 产品页面的布局。

1. 选择 **[!UICONTROL Default Category Layout]** 要用于类别页面的URL。

   此设置确定默认情况下用于类别页面的布局。

   - `No layout updates`  — 布局更新不适用于类别页面。
   - `Empty`  — 对类别页面使用空白布局。
   - `1 column`  — 对类别页面使用单列布局。
   - `2 columns with left bar`  — 对于类别页面，使用左侧带有侧栏的双列布局。
   - `2 columns with right bar`  — 对于类别页面，使用右侧带有侧栏的双列布局。
   - `3 columns`  — 对于类别页面，使用左边和右边带有侧栏的三列布局。

   时间 [页面生成器](../page-builder/introduction.md) 已启用，则还有其他完整的宽度选项可用。 然后，您可以使用页面生成器内容工具来设计类别页面的布局。

   - `Page -- Full Width`  — 使用 _页面 — 全宽_ 类别页面的布局。
   - `Category -- Full Width`  — （推荐）使用 _类别 — 完整宽度_ 类别页面的布局。
   - `Product -- Full Width`  — 使用 _产品 — 完整宽度_ 类别页面的布局。

1. 选择 **[!UICONTROL Default Page Layout]** 要用于CMS页面的对象。

   此设置确定CMS页面默认使用的布局。

   - `No layout updates` - CMS页面不提供布局更新。
   - `Empty`  — 对CMS页面使用空白布局。
   - `1 column`  — 对CMS页面使用单列布局。
   - `2 columns with left bar`  — 对于CMS页面，使用左侧带有侧栏的双列布局。
   - `2 columns with right bar`  — 对于CMS页面，使用右侧带有侧栏的双列布局。
   - `3 columns`  — 对于CMS页面，使用左边栏和右边栏的三列布局。

   时间 [页面生成器](../page-builder/introduction.md) 已启用，则还有其他完整的宽度选项可用。 然后，您可以使用页面生成器内容工具来设计CMS页面的布局。

   - `Page -- Full Width`  — （推荐）使用 _页面 — 全宽_ CMS页面的布局。
   - `Category - Full Width`  — 使用 _类别 — 完整宽度_ CMS页面的布局。
   - `Product - Full Width`  — 使用 _产品 — 完整宽度_ CMS页面的布局。

1. 完成后，单击 **[!UICONTROL Save Config]**.

## 标准页面布局

### 一列

![图 — 一列式布局](./assets/layout-1-col-th.png){zoomable=&quot;yes&quot;}

此 _[!UICONTROL 1 Column]_布局可用于创建具有大图像或焦点的生动主页。 此外，它还是登陆页面或包含文本、图像和视频组合的任何其他页面的理想选择。

### 带左栏的两列

![图 — 带左栏的双列布局](./assets/layout-2-col-lft-bar-th.png){zoomable=&quot;yes&quot;}

此 _[!UICONTROL 2 Columns with Left Bar]_布局通常用于左侧导航的页面，例如具有分层导航的目录或搜索结果页面。 此外，对于需要在左侧添加导航或支持内容块的主页而言，它也是一个非常好的选择。

### 带右栏的两列

![图 — 带右栏的两列式布局](./assets/layout-2-col-rt-bar-th.png){zoomable=&quot;yes&quot;}

带有 _[!UICONTROL 2 Columns with Right Bar]_布局，主内容区域足够大，可形成引人注目的图像或横幅。 此布局还经常用于右侧包含支持内容块的产品页面。

### 三列

![图 — 三柱式布局](./assets/layout-3-col-th.png){zoomable=&quot;yes&quot;}

此 _[!UICONTROL 3 Column]_布局的中心列宽得足以容纳页面的主文本，两边都有空间用于额外的导航和支持内容块。

### 空

![图表 — 空布局](./assets/layout-blank-th.png){zoomable=&quot;yes&quot;}

此 _[!UICONTROL Empty]_布局可用于定义自定义页面布局。

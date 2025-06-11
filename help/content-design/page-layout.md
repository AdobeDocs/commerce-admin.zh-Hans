---
title: 页面布局
description: 了解页面布局区域以及如何配置默认布局。
exl-id: 397a92cf-6f20-4729-8d7c-c5f672fc1c9a
badgePaas: label="仅限PaaS" type="Informative" url="https://experienceleague.adobe.com/zh-hans/docs/commerce/user-guides/product-solutions" tooltip="仅适用于云项目(Adobe管理的PaaS基础架构)和内部部署项目上的Adobe Commerce 。"
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '878'
ht-degree: 0%

---

# 页面布局

商店中每个页面的布局由不同的部分或容器组成，这些部分或容器定义页面的页眉、页脚和内容区域。 根据布局，每个页面可能包含一列、两列、三列或更多列。 您可以将该布局视为页面的&#x200B;_平面图_，并分配特定布局作为CMS、产品和类别页面的默认布局。

在页面上，根据内容块被指定显示的[页面布局](layout-updates.md)的区域，内容块会浮动以填充可用空间。 请注意，如果将布局从三列更改为两列，则主区域的内容将展开以填充可用空间。 另请注意，与未使用的侧栏关联的任何块似乎都消失了。 但是，如果恢复三列布局，块会重新出现。 这种流动方式，即&#x200B;_流动布局_，使得无需重新处理内容即可更改页面布局。 如果您习惯于使用单独的HTML页面，则这种模块化&#x200B;_构建基块_&#x200B;方法需要不同的思维方式。

![标准两列，左栏页面布局](./assets/storefront-2-column-ee.png){width="700" zoomable="yes"}

## 配置默认布局

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧面板中的&#x200B;_[!UICONTROL General]_&#x200B;下，选择&#x200B;**[!UICONTROL Web]**。

1. 展开&#x200B;**[!UICONTROL Default Layouts]**&#x200B;部分的![扩展选择器](../assets/icon-display-expand.png)。

   ![默认布局](./assets/web-default-layouts.png){width="600" zoomable="yes"}

1. 选择要用于产品页面的&#x200B;**[!UICONTROL Default Product Layout]**。

   此设置确定默认用于产品页面的布局。

   - `No layout updates` — 布局更新不可用于产品页面。
   - `Empty` — 对产品页面使用空白布局。
   - `1 column` — 对产品页面使用单列布局。
   - `2 columns with left bar` — 对于产品页面，使用左边带有侧栏的双列布局。
   - `2 columns with right bar` — 对产品页面使用右侧带有侧栏的双列布局。
   - `3 columns` — 对产品页面使用左边栏和右边栏的三列布局。

   启用[页面生成器](../page-builder/introduction.md)后，还有其他可用的全宽选项。 然后，您可以使用页面生成器内容工具来设计产品页面的布局。

   - `Page -- Full Width` — 对产品页面使用&#x200B;_页面 — 全宽_&#x200B;布局。
   - `Category -- Full Width` — 对产品页面使用&#x200B;_类别 — 全宽_&#x200B;布局。
   - `Product -- Full Width` - （推荐）对产品页面使用&#x200B;_Product - Full Width_&#x200B;布局。

1. 选择要用于类别页面的&#x200B;**[!UICONTROL Default Category Layout]**。

   此设置确定默认情况下用于类别页面的布局。

   - `No layout updates` — 布局更新不可用于类别页面。
   - `Empty` — 对类别页面使用空白布局。
   - `1 column` — 对类别页使用单列布局。
   - `2 columns with left bar` — 对类别页面使用左边带有侧栏的双列布局。
   - `2 columns with right bar` — 对类别页面使用右侧带有侧栏的双列布局。
   - `3 columns` — 对类别页面使用左边栏和右边栏的三列布局。

   启用[页面生成器](../page-builder/introduction.md)后，还有其他可用的全宽选项。 然后，您可以使用页面生成器内容工具来设计类别页面的布局。

   - `Page -- Full Width` — 对类别页面使用&#x200B;_页面 — 全宽_&#x200B;布局。
   - `Category -- Full Width` - （推荐）对类别页面使用&#x200B;_类别 — 全宽_&#x200B;布局。
   - `Product -- Full Width` — 对类别页面使用&#x200B;_Product - Full Width_&#x200B;布局。

1. 选择要用于CMS页面的&#x200B;**[!UICONTROL Default Page Layout]**。

   此设置确定默认情况下用于CMS页面的布局。

   - `No layout updates` - CMS页面没有布局更新。
   - `Empty` — 对CMS页面使用空白布局。
   - `1 column` — 对CMS页面使用单列布局。
   - `2 columns with left bar` — 对CMS页面使用左边带有侧栏的双列布局。
   - `2 columns with right bar` — 对CMS页面使用右侧带有侧栏的双列布局。
   - `3 columns` — 对CMS页面使用左边栏和右边栏的三列布局。

   启用[页面生成器](../page-builder/introduction.md)后，还有其他可用的全宽选项。 然后，您可以使用页面生成器内容工具来设计CMS页面的布局。

   - `Page -- Full Width` - （推荐）使用CMS页面的&#x200B;_Page — 全宽_&#x200B;布局。
   - `Category - Full Width` — 对CMS页面使用&#x200B;_类别 — 全宽_&#x200B;布局。
   - `Product - Full Width` — 对CMS页面使用&#x200B;_Product - Full Width_&#x200B;布局。

1. 完成后，单击&#x200B;**[!UICONTROL Save Config]**。

## 标准页面布局

### 一列

![图表 — 一列式布局](./assets/layout-1-col-th.png){zoomable="yes"}

_[!UICONTROL 1 Column]_&#x200B;布局可用于创建具有大图像或焦点的生动主页。 此外，它还是登陆页面或包含文本、图像和视频组合的任何其他页面的理想选择。

### 带左栏的两列

![图表 — 左栏的双列布局](./assets/layout-2-col-lft-bar-th.png){zoomable="yes"}

_[!UICONTROL 2 Columns with Left Bar]_&#x200B;布局通常用于左侧导航的页面，如目录或具有分层导航的搜索结果页面。 此外，对于需要在左侧添加导航或支持内容块的主页而言，它也是一个非常好的选择。

### 带右栏的两列

![图表 — 带有右栏的双列布局](./assets/layout-2-col-rt-bar-th.png){zoomable="yes"}

使用&#x200B;_[!UICONTROL 2 Columns with Right Bar]_&#x200B;布局时，主内容区域足够大，足以形成引人注目的图像或横幅。 此布局还经常用于右侧包含支持内容块的产品页面。

### 三列

![图表 — 三列式布局](./assets/layout-3-col-th.png){zoomable="yes"}

_[!UICONTROL 3 Column]_&#x200B;布局的中心列宽得足以容纳页面的主文本，两边都有空间用于额外的导航和支持内容块。

### 空

![图表 — 布局为空](./assets/layout-blank-th.png){zoomable="yes"}

_[!UICONTROL Empty]_&#x200B;布局可用于定义自定义页面布局。

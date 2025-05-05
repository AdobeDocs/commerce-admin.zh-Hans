---
title: 创建类别
description: 您可以根据配置中设置的最大菜单深度，根据需要创建任意数量的其他子类别。
exl-id: 8ba5fc1a-3bf2-4a29-bbc3-709fc0ad7497
feature: Catalog Management, Categories
source-git-commit: 5da244a548b15863fe31b5df8b509f8e63df27c2
workflow-type: tm+mt
source-wordcount: '1137'
ht-degree: 0%

---

# 创建类别

目录的类别结构就像一个上下颠倒的树，其根位于顶部。 树的每一部分都可以展开和折叠。 任何禁用或隐藏的类别都会呈灰显状态。 第一级别（[根](category-root.md)之下）的类别通常在[主菜单](navigation-top.md)中显示为选项。 您可以根据配置中设置的最大菜单深度，根据需要创建任意数量的其他子类别。 可以将类别拖放到树中的其他位置。 类别ID编号显示在页面顶部的类别名称后面的括号中。

对于具有多个[商店](../stores-purchase/stores.md#add-stores)的网站，您可以为每个商店创建不同的根类别，以定义用于[顶部导航](navigation-top.md)的类别集。

![类别树](./assets/category-selected.png){width="700" zoomable="yes"}

## 最佳实践

在规划和创建类别时，请使用这些最佳实践。

### 类别结构

主菜单中的类别结构可能会影响客户体验和性能。 作为最佳实践，您应该确定一个首要的顶级类别，并避免其他类别具有相同名称。 例如，不要在不同部门（如`Clothing/Kids`、`Shoes/Kids`、`Accessories/Kids`）下为“儿童”组织多个类别。 更高效的方法是先创建顶层父类别`Kids`，然后创建下面所需的子类别。 与类别结构保持一致，对目录中的所有产品类型使用相同的方法。

### 业务规则和自动化

在使用业务逻辑在目录页面上显示相似项目，或设置个性化促销、自动化流程或搜索标准时，请考虑类别结构和可用属性值。 例如，如果指定“polo”作为父类别，则结果可能包括性别和年龄不适当的混合产品。 但是，如果您与特定子类别的polo衫匹配，则结果会更窄，并且可能会吸引特定客户。 如果与针对特定客户的其他属性值相结合，结果可能会更加具体。 考虑在引用特定类别路径时必须过滤和检索的产品数量。 结果上的差别可能非常大。 考虑以下类别路径返回的不同结果：

- `[Category:  All Products/Shirts/Father's Day/Polos/Sale]`
- `[Category Path: Men/Shirts/Polos]`
- `[Child Category: Polos]`

必须明确定义分类关系，例如：

- 父类别
- 子类别
- 类别路径

还可定义任何关联的关键字和属性，例如：

- 可用性
- 售价
- 品牌
- 大小
- 颜色

## 步骤1：创建类别

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Catalog]** > **[!UICONTROL Categories]**。

1. 设置&#x200B;**[!UICONTROL Store View]**&#x200B;以确定新类别在何处可用。

1. 在类别树中，选择新类别的父类别。

   父级比新类别高一级。

   如果您从头开始，没有任何数据，则列表中可能只有两个类别：_默认类别_（根类别）和&#x200B;_示例类别_

1. 单击&#x200B;**[!UICONTROL Add Subcategory]**。

## 第2步：完成基本信息

1. 如果您希望该类别在存储中立即可用，请将&#x200B;**[!UICONTROL Enable Category]**&#x200B;设置为`Yes`。

1. 要在[顶部导航](navigation-top.md)中包含该类别，请将&#x200B;**[!UICONTROL Include in Menu]**&#x200B;设置为`Yes`。

1. 输入&#x200B;**[!UICONTROL Category Name]**。

   ![基本类别信息](./assets/catalog-categories-currently-active.png){width="500" zoomable="yes"}

1. 单击&#x200B;**[!UICONTROL Save]**&#x200B;并继续。

## 第3步：完成类别内容

1. 展开&#x200B;**[!UICONTROL Content]**&#x200B;部分的![扩展选择器](../assets/icon-display-expand.png)。

   ![类别内容](./assets/category-content.png){width="600" zoomable="yes"}

1. 要在页面顶部显示&#x200B;**[!UICONTROL Category Image]**，您可以上传自己的图像或使用[媒体存储](../content-design/media-storage.md)中存在的图像。

   - 要上传您自己的图像，请单击&#x200B;**[!UICONTROL Upload]**，然后选择要表示该类别的图像。

   - 若要使用媒体存储中的图像，请单击&#x200B;**[!UICONTROL Select from Gallery]**&#x200B;并选择要表示该类别的图像。

   在媒体集内，您还可以通过单击&#x200B;**[!UICONTROL Search Adobe Stock]**&#x200B;使用[Adobe Stock集成](../content-design/adobe-stock.md)来查找合适的图像。

   >[!NOTE]
   >
   > 如果您已启用AEM Assets，请参阅[管理类别](../content-design/aem-assets-manage.md)以了解更多信息。

1. 对于&#x200B;**[!UICONTROL Description]**，输入要显示在类别登录页面上的文本或其他内容。

   有关详细信息，请参阅[类别内容](categories-content-settings.md)。

1. 要在类别登录页面上包含内容块，请选择要显示的&#x200B;**[!UICONTROL CMS Block]**。

1. 单击&#x200B;**[!UICONTROL Save]**&#x200B;并继续。

## 第4步：完成显示设置

1. 展开&#x200B;**[!UICONTROL Display Setting]**&#x200B;部分的![扩展选择器](../assets/icon-display-expand.png)。

   ![显示设置](./assets/category-display-settings.png){width="600" zoomable="yes"}

   有关这些选项的详细信息，请参阅。有关这些选项的详细信息，请参阅[显示设置](categories-display-settings.md)。

1. 将&#x200B;**[!UICONTROL Display Mode]**&#x200B;设置为以下项之一：

   - `Products Only`
   - `Static Block Only`
   - `Static Block and Products`

1. 如果希望类别页面包含分层导航的&#x200B;_`Filter by Attribute`_部分，请将&#x200B;**[!UICONTROL Anchor]**&#x200B;设置为`Yes`。

1. 对于&#x200B;**[!UICONTROL Available Product Listing Sort By]**&#x200B;选项，请选择一个或多个可供客户对列表进行排序的可用值。 此设置不适用于[!DNL Live Search] [产品列表页面小组件](https://experienceleague.adobe.com/zh-hans/docs/commerce/live-search/live-search-storefront/plp-styling)。

   默认情况下，将包含所有可用值。 取消选中&#x200B;**[!UICONTROL Use All]**&#x200B;复选框以更改选择。 例如，值可能包括：

   - `Position`
   - `Product Name`
   - `Price`

1. 要设置类别的默认排序顺序，请选择&#x200B;**[!UICONTROL Default Product Listing Sort By]**&#x200B;值。 此设置不适用于[!DNL Live Search] [产品列表页面小组件](https://experienceleague.adobe.com/zh-hans/docs/commerce/live-search/live-search-storefront/plp-styling)。

1. 要更改默认分层导航[价格步骤](navigation-layered.md#configure-price-navigation)设置，请执行以下操作：

   - 取消选中&#x200B;**[!UICONTROL Use Config Settings]**&#x200B;复选框。

   - 输入要用作分层导航的增量价格步骤的值。

1. 单击&#x200B;**[!UICONTROL Save]**&#x200B;并继续。

## 步骤5：完成搜索引擎优化设置

1. 展开&#x200B;**[!UICONTROL Search Engine Optimization Settings]**&#x200B;部分的![扩展选择器](../assets/icon-display-expand.png)。

   ![搜索引擎优化](./assets/categories-search-engine-optimization.png){width="600" zoomable="yes"}

   有关这些选项的更多信息，请参阅[搜索引擎优化](categories-search-engine-optimization.md)。

1. 为类别完成以下[元数据](../merchandising-promotions/meta-data.md)：

   - [!UICONTROL Meta Title]
   - [!UICONTROL Meta Keywords]
   - [!UICONTROL Meta Description]

1. 单击&#x200B;**[!UICONTROL Save]**&#x200B;并继续。

## 步骤6：选择类别中的产品

1. 展开&#x200B;**[!UICONTROL Products in Category]**&#x200B;部分的![扩展选择器](../assets/icon-display-expand.png)。

   ![类别中的产品](./assets/category-products-in-category.png){width="600" zoomable="yes"}

   有关这些选项的更多信息，请参阅[类别](categories-product-assignments.md)中的产品。

1. 如果需要，请使用[筛选器](../getting-started/admin-grid-controls.md)查找产品。

   要显示尚未包含在类别中的所有记录，请将第一列中的记录选择器设置为`No`，然后单击&#x200B;**[!UICONTROL Search]**。

1. 在第一列中，选中要包含在类别中的每个产品的复选框。

1. 单击&#x200B;**[!UICONTROL Save]**&#x200B;并继续。

## 步骤7：设置类别权限

{{ee-feature}}

1. 展开&#x200B;**[!UICONTROL Category Permissions]**&#x200B;部分的![扩展选择器](../assets/icon-display-expand.png)。

1. 对于多站点安装，请选择应用类别权限的&#x200B;**[!UICONTROL Website]**。

1. 选择应用类别权限的&#x200B;**[!UICONTROL Customer Group]**。

   ![Adobe Commerce B2B](../assets/b2b.svg) (仅限[Adobe Commerce B2B](../b2b/introduction.md))如果需要，您可以改为选择&#x200B;**[!UICONTROL Shared Catalog]**。

1. 根据需要设置以下权限：

   - [!UICONTROL Browsing Category]
   - [!UICONTROL Display Product Prices]
   - [!UICONTROL Add to Cart]

1. 要添加其他权限规则，请单击&#x200B;**[!UICONTROL New Permission]**&#x200B;并重复该过程。

   ![类别权限](./assets/category-create-permissions.png){width="600" zoomable="yes"}

## 步骤8：完成设计设置

1. 展开&#x200B;**[!UICONTROL Design]**&#x200B;部分的![扩展选择器](../assets/icon-display-expand.png)。

1. 根据需要设置设计设置：

   - (仅限[Adobe Commerce B2B](../b2b/introduction.md))若要将父类别设计设置应用于此类别，请将&#x200B;**[!UICONTROL Use Parent Category Settings]**&#x200B;设置为`Yes`。

   - 要更改类别页面的设计，请选择要应用的&#x200B;**[!UICONTROL Theme]**。

   - 要更改类别页面的列布局，请选择要应用的&#x200B;**[!UICONTROL Layout]**。

   - 若要输入自定义代码，请在&#x200B;**[!UICONTROL Layout Update XML]**&#x200B;框中输入有效的XML代码。

   - 要对产品页面使用相同的设计，请将&#x200B;**[!UICONTROL Apply Design to Products]**&#x200B;设置为`Yes`。

   ![设计设置](./assets/category-design.png){width="600" zoomable="yes"}

1. ![Magento Open Source](../assets/open-source.svg)(仅限Magento Open Source)要计划在特定时间段进行设计更新，请执行以下操作：

   - 展开&#x200B;_[!UICONTROL Schedule Design Update]_&#x200B;部分。

   - 使用日历（![日历图标](../assets/icon-calendar.png)）选择计划更新&#x200B;**[!UICONTROL from]**&#x200B;和&#x200B;**[!UICONTROL to]**&#x200B;日期。

   ![计划的设计更新](./assets/category-scheduled-design-update.png){width="600" zoomable="yes"}

1. 完成后，单击&#x200B;**[!UICONTROL Save]**。

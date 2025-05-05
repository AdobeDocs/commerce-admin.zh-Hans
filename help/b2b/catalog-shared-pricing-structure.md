---
title: 设置共享目录定价和结构
description: 使用Adobe Commerce B2B，了解如何设置共享目录的定价和结构。
exl-id: 67caf56f-1b31-44bb-98dc-ea6ea7d8a4d5
feature: B2B, Companies, Catalog Management
role: Admin
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '1305'
ht-degree: 0%

---

# 设置共享目录定价和结构

设置共享目录的定价和结构需要两个步骤。 您在流程中的当前位置在页面顶部的进度条中以数字突出显示。 您可以随时通过单击进度条查看进程中的其他步骤。 例如，如果您正在处理自定义定价，则可能需要返回到产品选择页面以供参考。 只需单击页面顶部进度栏中的&#x200B;**[!UICONTROL Products]**，然后单击&#x200B;**[!UICONTROL Pricing]**&#x200B;即可返回自定义定价页面。 在此过程中，您的工作不会丢失。

目录![&#128279;](./assets/shared-catalog-products-workspace.png){width="700" zoomable="yes"}中的产品

在标准类别树中，根类别是最顶层的容器，在示例数据中称为&#x200B;_默认类别_。 但是，如果启用了共享目录，则类别树具有名为&#x200B;_根目录_&#x200B;的外部容器。 根目录包含系统中存在的所有其他类别结构。 有关详细信息，请参阅[目录范围](../catalog/introduction.md#catalog-scope)。

## 第1步：打开共享目录定价和结构配置

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**

1. 对于网格中的共享目录，转到&#x200B;_[!UICONTROL Action]_&#x200B;列并单击&#x200B;**[!UICONTROL Set Pricing and Structure]**。

   ![设置共享目录的定价和结构](./assets/shared-catalog-set-pricing-structure.png){width="700" zoomable="yes"}

1. 首次配置共享目录时，单击&#x200B;**[!UICONTROL Configure]**&#x200B;以继续执行以下步骤。

## 第2步：选择产品

此流程的第一步是选择要包含在共享目录中的产品。 产品选择页面左侧显示[类别树](../catalog/category-create.md)，右侧显示同步的产品网格。 如果单击树中的某个类别，则该类别中的产品将显示在网格中。

从店面查看共享目录时，[顶部导航](../catalog/navigation-top.md)中仅显示具有选定产品的类别。 默认情况下，店面导航中只包含前三个类别级别，不包括根类别。

1. 使用&#x200B;**存储**&#x200B;选择器设置配置的[作用域](../catalog/introduction.md#product-scope)。

   只能在首次保存共享目录之前设置配置的范围。 如果您稍后编辑产品选择，则“商店”选择器将不可用。

   ![选择商店](./assets/shared-catalog-products-scope.png){width="600" zoomable="yes"}

1. 在类别树中，执行以下任一操作：

   - 要包含所有产品，请单击&#x200B;**[!UICONTROL Select all]**&#x200B;或选中父类别的复选框。
   - 要包含特定类别的产品，请选中要包含的每个类别的复选框。
   - 要包含或排除单个产品，请选中或取消选中产品的复选框。

   树中每个类别下面的表示法显示当前包含在共享目录中的类别中的产品数量。 [根类别](../catalog/category-root.md)下的表示法显示当前为共享目录选择的所有类别中的产品总数。

1. 要查看网格中的类别产品，请单击树中类别的名称。 选择类别时，会发生以下情况：

   - 网格第一列中的切换设置为每个所选产品的绿色&#x200B;_On_&#x200B;位置。
   - 如果将产品分配给多个类别，并且未在其中某个类别中选择该产品，则它仍可通过其他类别使用，在使用[目录搜索](../catalog/search.md)时也可使用。
   - 系统自动将所选产品的[类别权限](../catalog/category-permissions.md)设置为`Allow`。

1. 如有必要，请使用筛选器和其他网格控件来查找要包含在共享目录中的产品。

   您可以通过单击第一列中的切换来单独选择或忽略各个产品。

   如果您选择的类别没有产品，但是已链接到CMS内容或外部链接，则该类别会显示在店面的顶部导航中。

   在保存配置之前，您所做的类别设置不会永久记录在数据库中。 但是，当您处理结构和定价时，它们会暂时保存。

1. 单击&#x200B;**[!UICONTROL Next]**。

   ![为目录选择产品](./assets/shared-catalog-select-products-step-1.png){width="600" zoomable="yes"}

## 步骤3：设置自定义价格

您可以单独为每个产品设置自定义定价，也可以使用&#x200B;_[!UICONTROL Action]_&#x200B;控件将自定义定价设置为多个产品记录的固定金额或百分比。

- **[!UICONTROL Fixed]**：指定最终产品价格。 例如，如果您输入的固定价格为$10.00，则相应公司的店面价格为$10.00。

  >[!NOTE]
  >
  >基本价格和输入的固定值之间的最小值用作最终产品价格。

  >[!NOTE]
  >
  >**_固定价格_**&#x200B;产品可自定义选项&#x200B;_不_&#x200B;受组价格、层价格、特殊价格或目录价格规则的影响。

- **[!UICONTROL Percentage]**：根据折扣百分比确定自定义价格。 例如，要提供10%的折扣，请将自定义价格类型设置为`Percentage`并输入`10`。 折扣的定制价格是原始产品价格的90%。

若要为以下产品类型将折扣设置为固定金额或百分比，请在网格中使用&#x200B;_[!UICONTROL Custom Price]_&#x200B;列：

- [简单](../catalog/product-create-simple.md)（包括可配置的产品变体）
- [捆绑](../catalog/product-create-bundle.md)
- [可下载](../catalog/product-create-downloadable.md)
- [虚拟](../catalog/product-create-virtual.md)

对于[可配置](../catalog/product-create-configurable.md)和[已分组](../catalog/product-create-grouped.md)的产品类型以及[礼品卡](../catalog/product-gift-card-create.md)，自定义价格列为空。

无法从&#x200B;_自定义价格_&#x200B;页面更改网格中的产品选择。 但是，您可以使用页面顶部的进度指示器返回到上一步并更改产品选择。

![为目录选择产品](./assets/shared-catalog-custome-prices-step-3.png){width="600" zoomable="yes"}

### 应用自定义价格

1. 对于多站点安装，请将&#x200B;**[!UICONTROL Website]**&#x200B;设置为应用自定义价格的网站。

   ![选择网站](./assets/shared-catalog-scope-pricing.png){width="600" zoomable="yes"}

1. 使用以下方法之一选择要应用自定义定价的产品。

   - 使用类别树选择特定类别中的所有产品。
   - 将标头中的&#x200B;_[!UICONTROL Mass Actions]_&#x200B;控件设置为`Select All`。
   - 选中各个产品的复选框。

   网格显示当前选定类别中的产品，您可以使用标准控件查找产品并筛选列表。

   ![全选](./assets/shared-catalog-custom-pricing-mass-actions.png){width="600" zoomable="yes"}

1. 将&#x200B;**[!UICONTROL Actions]**&#x200B;设置为以下项之一：

   - `Set Discount` — 将折扣百分比应用于所有选定产品。 每个受影响的产品价格均以&#x200B;**_折扣_**&#x200B;价格显示。
   - `Adjust Fixed Price` — 对所有选定产品应用固定价格折扣百分比。 每个受影响的产品价格都显示为&#x200B;**_调整后的固定_**&#x200B;价格。

   ![操作控件 — 设置折扣](./assets/shared-catalog-set-custom-prices-discount-action.png){width="600" zoomable="yes"}

1. 出现提示时，输入折扣或价格调整，然后单击&#x200B;**[!UICONTROL Apply]**。

   ![设置折扣](./assets/shared-catalog-set-custom-prices-discount.png){width="400"}<br/>

   ![调整固定价格](./assets/shared-catalog-set-custom-fixed-prices.png){width="400"}

   折扣将应用于所有选定的产品，且&#x200B;_自定义价格_&#x200B;列反映应用的折扣和金额类型。

   ![带折扣的自定义价格列](./assets/shared-catalog-set-custom-prices-discount-applied.png){width="600" zoomable="yes"}

### 应用层价格

[层定价](../catalog/product-price-tier.md)允许您为共享目录中的产品提供数量折扣。 网格的&#x200B;_层价格_&#x200B;列包含指向专门应用于共享目录的&#x200B;_高级定价_&#x200B;选项的链接。 如果产品已包含层定价，则链接后的括号中会显示现有层的数量。

以下说明显示了如何将分层定价应用于单个产品。 要对多个产品应用层定价，请参阅[导入层价格](../systems/data-import-price-tier.md)。

1. 对于网格中的产品，转到&#x200B;_层价格_&#x200B;列并单击&#x200B;**[!UICONTROL Configure]**。

   ![配置层价格](./assets/shared-catalog-tier-price-configure.png){width="600" zoomable="yes"}

1. 在&#x200B;_高级定价_&#x200B;页面上，单击&#x200B;**[!UICONTROL Add Price]**&#x200B;并执行以下操作：

   ![目录和层价格](./assets/shared-catalog-tier-price-configure-add-price.png){width="600" zoomable="yes"}

   - 将&#x200B;**[!UICONTROL Website]**&#x200B;设置为应用层价格的网站。
   - 输入必须购买才能获得折扣的产品数量。
   - 将&#x200B;**[!UICONTROL Price]**&#x200B;设置为以下折扣类型之一：
      - `Fixed`
      - `Discount`
   - 输入折扣金额。
   - 要输入另一层，请单击&#x200B;**添加价格**&#x200B;并重复此过程以定义下一层。

   ![多层价格](./assets/shared-catalog-tier-price-configure-multiple-tiers.png){width="600" zoomable="yes"}

1. 完成后，单击&#x200B;**[!UICONTROL Done]**。

   在网格中，_[!UICONTROL Tier Price]_&#x200B;列的括号中显示了层数。

   ![多个层](./assets/shared-catalog-tier-price-configure-parentheses.png){width="600" zoomable="yes"}

## 保存结构和定价

自定义定价完成后，单击&#x200B;**[!UICONTROL Generate Catalog]**，然后单击&#x200B;**[!UICONTROL Save]**。

共享目录现已保存到数据库。 其名称显示在&#x200B;_[!UICONTROL Products]_&#x200B;网格的&#x200B;_[!UICONTROL Shared Catalog]_&#x200B;列中。 下一步是[将共享目录分配给公司](./catalog-shared-assign-companies.md)。

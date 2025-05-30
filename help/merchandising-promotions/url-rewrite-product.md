---
title: 产品URL重写
description: 了解如何使用产品URL重写以将链接重定向到Commerce商店中其他产品的URL。
exl-id: 42b28ff7-e148-44f2-b6b4-63a38458e752
feature: Products, Configuration
badgePaas: label="仅限PaaS" type="Informative" url="https://experienceleague.adobe.com/zh-hans/docs/commerce/user-guides/product-solutions" tooltip="仅适用于云项目(Adobe管理的PaaS基础架构)和内部部署项目上的Adobe Commerce 。"
source-git-commit: 6d782e3aafa7460a0e0d5ca07a2bde2ae371a9ea
workflow-type: tm+mt
source-wordcount: '897'
ht-degree: 0%

---

# 产品URL重写

在开始之前，请确保您确切了解重定向应该实现的目标。 从&#x200B;_target_ / _原始请求_&#x200B;或&#x200B;_重定向到_ / _重定向来自_。 尽管人们可能仍会从搜索引擎或过时的链接导航到之前的页面，但重定向会导致您的商店切换到新目标。

如果您的商店启用了[自动重定向](url-redirect-product-automatic.md)，则当产品[URL密钥](../catalog/catalog-urls.md)更改时，无需创建重写。

{{url-rewrite-skip}}

## 步骤1. 计划重写

为避免错误，请记下&#x200B;_重定向到_&#x200B;路径和&#x200B;_从_&#x200B;路径重定向并包含URL密钥和后缀（如果适用）。

如果您不确定，请打开您商店中的每个产品页面，然后从浏览器的地址栏复制路径。 创建产品重定向时，您可以包含或排除[类别路径](../catalog/catalog-urls.md)。 在本例中，我们创建了一个没有类别路径的产品重定向。

### 具有类别路径的产品

重定向到：`gear/bags/impulse-duffle.html`

重定向自： `gear/bags/overnight-duffle.html`

### 没有类别路径的产品

重定向到：`impulse-duffle.html`

重定向自： `overnight-duffle.html`

## 步骤2. 创建重写

{{url-rewrite-params}}

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL URL Rewrites]**。

1. 在继续操作之前，请执行以下操作以验证请求路径是否可用。

   - 在&#x200B;**[!UICONTROL Request Path]**&#x200B;列顶部的搜索筛选器中，输入要重定向的页面的URL键，然后单击&#x200B;**[!UICONTROL Search]**。

   - 如果该页面有多个重定向记录，请查找与适用的商店视图匹配的重定向记录，然后在编辑模式下打开该页面。

   - 单击右上角的&#x200B;**[!UICONTROL Delete]**。 出现提示时，单击&#x200B;**[!UICONTROL OK]**&#x200B;确认。

1. 在“URL重写”页面的右上角，单击&#x200B;**添加URL重写**。

1. 将&#x200B;**[!UICONTROL Create URL Rewrite]**&#x200B;设置为`For product`。

1. 在网格中，查找作为重定向的目标（目标）的产品，然后单击行。

   ![URL重写 — 产品](./assets/url-rewrite-product.png){width="700" zoomable="yes"}

1. 在类别树下，单击&#x200B;**[!UICONTROL Skip Category Selection]**。

   对于此示例，重定向不包含类别。

   ![产品URL重写 — 跳过类别选择](./assets/url-rewrite-skip-category-selection.png){width="600" zoomable="yes"}

   “为产品添加URL重写”页面的左上角显示指向目标的链接，而“目标路径”字段显示路径的系统版本，该版本无法更改。 最初，重定向路径字段还会显示目标路径。

   - 如果您有多个存储视图，请将&#x200B;**[!UICONTROL Store]**&#x200B;设置为应用重写的视图。 否则，将为每个视图创建一个重写。

   - 对于&#x200B;**[!UICONTROL Request Path]**，通过输入原始产品请求的URL键和后缀（如果适用）来替换默认值。 这是您在规划步骤中识别的&#x200B;_产品中的_&#x200B;重定向。

     >[!NOTE]
     >
     >对于指定的存储，请求路径必须是唯一的。 如果已经有使用同一请求路径的重定向，则在尝试保存该重定向时会收到一个错误。 必须先删除以前的重定向，然后才能创建重定向。

   - 将&#x200B;**[!UICONTROL Redirect Type]**&#x200B;设置为以下项之一：

      - `Temporary (302)`
      - `Permanent (301)`

   - 供您参考，请输入简短的重写&#x200B;**[!UICONTROL Description]**。

   ![产品URL重写 — 信息](./assets/url-rewrite-product-permanent-301.png){width="600" zoomable="yes"}

1. 在保存重定向之前，请查看以下内容：

   - 左上角的链接显示目标产品的名称。
   - 请求路径包含来自&#x200B;_产品的原始_&#x200B;重定向的路径。

1. 完成后，单击&#x200B;**[!UICONTROL Save]**。

   新产品重写现在显示在“URL重写”网格的顶部。

## 步骤3. 测试结果

1. 转到您商店的主页。

1. 执行以下操作之一：

   - 从&#x200B;_产品请求页面导航到原始的_&#x200B;重定向。
   - 在浏览器的地址栏中，在商店URL之后立即输入原始&#x200B;_重定向自_&#x200B;产品的路径，然后按&#x200B;**Enter**。

   此时将显示新的Target产品，而不是原始产品请求。

## 字段描述

| 字段 | 描述 |
|--- |--- |
| [!UICONTROL Create URL Rewrite] | 指示重写的类型。 创建重写后无法更改类型。 选项： `Custom` / `For category` / `For product` / `For CMS page` |
| [!UICONTROL Request Path] | 要重定向的产品。 根据您的配置，请求路径可能包含`.html`或`.htm`后缀和类别。 请求路径必须是唯一的，并且不能被另一个重定向使用。 如果您收到请求路径存在的错误，请删除现有重定向，然后重试。 |
| [!UICONTROL Target Path] | 系统用来指向重定向目标的内部路径。 目标路径呈灰显状态，无法编辑。 |
| [!UICONTROL Redirect] | 确定重定向的类型。 选项： <br/>**[!UICONTROL No]**— 未指定重定向。 许多操作都会创建此类型的重定向请求。 例如，每次将产品添加到类别时，都会在每次商店视图中创建`No`类型的重定向。<br/>**[!UICONTROL Temporary (302)]** — 向搜索引擎指示重写时间有限。 搜索引擎通常不会保留页面排名信息以进行临时重写。 <br/>**[!UICONTROL Permanent (301)]**— 向搜索引擎指示重写是永久的。 搜索引擎通常会保留页面排名信息以进行永久重写。 |
| [!UICONTROL Description] | 描述重写的用途，以供内部参考。 |

{style="table-layout:auto"}

## 多个URL重写

您可以使用以下步骤同时快速更新多个或所有产品的URL重写。

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Catalog]** > **[!UICONTROL Products]**。

1. 选择要更新URL重写的所有产品。

1. 在&#x200B;_[!UICONTROL Actions]_&#x200B;下，选择&#x200B;**[!UICONTROL Update attributes]**&#x200B;以更新多个重写或所有重写。

1. 在&#x200B;_[!UICONTROL PRODUCTS INFORMATION]_&#x200B;下，单击&#x200B;**[!UICONTROL Websites]**&#x200B;选项卡。

1. 在&#x200B;_[!UICONTROL Add Product To Websites]_&#x200B;部分中，选择要还原URL重写的所有网站。

1. 准备更新时，单击&#x200B;**[!UICONTROL Save]**。

>[!NOTE]
>
>所有选定的产品都将读取到选定的网站，并重新生成URL重写。

![更新属性 — 更新多个URL重写](./assets/url-rewrites-update.png){width="600" zoomable="yes"}

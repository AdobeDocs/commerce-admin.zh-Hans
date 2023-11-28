---
title: 目录搜索概述
description: 了解客户可用于在店面中查找产品的快速搜索和高级搜索工具。
exl-id: a796fa48-212a-47c7-ab6e-98edd4d040f4
feature: Catalog Management, Search
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '517'
ht-degree: 0%

---

# 目录搜索概述

>[!TIP]
>
>[[!DNL Live Search]](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/overview.html) 提供了快速、超级相关且直观的搜索体验，可供Adobe Commerce免费使用。 本节介绍可能与以下内容不同的标准搜索功能 [!DNL Live Search].

研究表明，使用搜索的用户比仅依赖导航的客户更有可能购物。 事实上，根据一些研究，使用搜索功能的人购买产品的可能性几乎是两倍。

以下各节介绍了基本的目录搜索功能。 有关如何配置和自定义本机目录搜索功能的信息，请参阅：

- [配置目录搜索](search-configuration.md)
- [搜索结果](search-results.md)
- [管理搜索词](search-terms.md)

>[!NOTE]
>
>Commerce中的本机搜索功能提供完全匹配的搜索结果。 同时 [!DNL Live Search]是一个可选模块，可在Adobe Commerce中安装和启用，但它采用不同的实施方式，因此产生的结果并不限于精确的搜索字符串。 例如，您有10个产品以数字形式标记为 _欧米茄_：搜索 `Omega 1` 结果匹配 _欧米茄1_ 具有本机搜索功能。 但由Live Search提供支持的同一搜索字符串会匹配多个项目， _欧米茄1_ 和 _欧米茄10_.

## 快速搜索

>[!NOTE]
>
>时间 [[!DNL Live Search]](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/live-search-storefront/quick-tour.html) 安装，则搜索框会在弹出窗口中返回“键入内容时搜索”结果。

商店标题中的搜索框可帮助访客在目录中查找产品。 搜索文本可以是完整或部分产品名称，也可以是描述产品的任何其他单词或短语。 管理员可管理用户用于查找产品的搜索词。

1. 对象 **[!UICONTROL Search]**，客户会输入他们希望查找内容的前几个字母。

   以下显示目录中的任何匹配项，其中包含找到的结果数。

1. 客户按Enter键或单击匹配产品列表中的结果。

   ![Search](./assets/storefront-search-box.png){width="700" zoomable="yes"}

## 高级搜索

>[!NOTE]
>
>此处介绍的高级表单搜索功能不适用于 [[!DNL Live Search]](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/overview.html).

通过高级搜索，购物者可以根据在表单中输入值搜索目录。 由于表单包含多个字段，因此单次搜索可以包含多个参数。 结果将列出目录中符合条件的所有产品。 高级搜索的链接位于商店的页脚中。

![高级搜索](./assets/storefront-search-advanced.png){width="700" zoomable="yes"}

表单中的每个字段对应于产品目录中的属性。 要添加字段，请将属性的前端属性设置为 `Include in Advanced Search`. 作为最佳实践，应仅包含客户最有可能用于查找产品的字段，因为数量过多会减慢搜索速度。

1. 在商店的页脚中，客户单击 **[!UICONTROL Advanced Search]**.

1. 在 _高级搜索_ 表单，根据需要在任意数量的字段中添加完整或部分值。

1. 点击次数 **[!UICONTROL Search]** 以显示结果。

   ![搜索结果](./assets/storefront-search-advanced-results-modify.png){width="700" zoomable="yes"}

1. 如果他们在搜索结果中未看到要查找的内容，则表示客户单击了 **[!UICONTROL Modify your search]** 并尝试其他标准组合。

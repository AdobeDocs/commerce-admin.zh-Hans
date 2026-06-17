---
title: 目录搜索概述
description: 了解客户可用于在店面中查找产品的快速搜索和高级搜索工具。
exl-id: a796fa48-212a-47c7-ab6e-98edd4d040f4
feature: Catalog Management, Search
TQID: https://experienceleague.adobe.com/PV3ZrkqHaUZw-2LFHCNKUeDcvJmkvFcuoR3ZxxURP54
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 541
ht-degree: 0%

---

# 目录搜索概述

>[!TIP]
>
>[[!DNL Live Search]](https://experienceleague.adobe.com/docs/commerce/live-search/overview.html)提供了快速、超级相关且直观的搜索体验，可供Adobe Commerce免费使用。 本节介绍可能与[!DNL Live Search]不同的标准搜索功能。

研究表明，使用搜索的用户比仅依赖导航的客户更有可能购物。 事实上，根据一些研究，使用搜索功能的人购买产品的可能性几乎是两倍。

以下各节介绍了基本的目录搜索功能。 有关如何配置和自定义本机目录搜索功能的信息，请参阅：

- [配置目录搜索](search-configuration.md)
- [搜索结果](search-results.md)
- [管理搜索词](search-terms.md)

>[!NOTE]
>
>Commerce中的本机搜索功能提供完全匹配的搜索结果。 而[!DNL Live Search]（可在Adobe Commerce中安装和启用的可选模块）的实施方式不同，结果不限于确切的搜索字符串。 例如，您有10个编号为&#x200B;_Omega_&#x200B;的产品：搜索`Omega 1`将导致&#x200B;_Omega 1_&#x200B;与本机搜索功能有一个匹配。 但是，由Live Search提供支持的同一搜索字符串将匹配多个项目&#x200B;_Omega 1_&#x200B;和&#x200B;_Omega 10_。

## 快速搜索

>[!NOTE]
>
>安装[[!DNL Live Search]](https://experienceleague.adobe.com/en/docs/commerce/live-search/overview)并启用[[!DNL Storefront Popover]](https://experienceleague.adobe.com/en/docs/commerce/live-search/live-search-storefront/storefront-popover)构件时，搜索框会在弹出窗口中返回“键入时搜索”结果。

商店标题中的搜索框可帮助访客在目录中查找产品。 搜索文本可以是完整或部分产品名称，也可以是描述产品的任何其他单词或短语。 管理员可管理用户用于查找产品的搜索词。

1. 对于&#x200B;**[!UICONTROL Search]**，客户输入其要查找内容的前几个字母。

   以下显示目录中的任何匹配项，其中包含找到的结果数。

1. 客户按Enter键或单击匹配产品列表中的结果。

   ![搜索](./assets/storefront-search-box.png){width="700" zoomable="yes"}

## 高级搜索

>[!NOTE]
>
>此处介绍的高级表单搜索功能不适用于[[!DNL Live Search]](https://experienceleague.adobe.com/docs/commerce/live-search/overview.html)。

通过高级搜索，购物者可以根据在表单中输入值搜索目录。 由于表单包含多个字段，因此单次搜索可以包含多个参数。 结果将列出目录中符合条件的所有产品。 高级搜索的链接位于商店的页脚中。

![高级搜索](./assets/storefront-search-advanced.png){width="700" zoomable="yes"}

表单中的每个字段对应于产品目录中的属性。 要添加字段，请将属性的前端属性设置为`Include in Advanced Search`。 作为最佳实践，应仅包含客户最有可能用于查找产品的字段，因为数量过多会减慢搜索速度。

1. 在商店的页脚中，客户单击&#x200B;**[!UICONTROL Advanced Search]**。

1. 在&#x200B;_高级搜索_&#x200B;窗体中，将完整或部分值添加到所需数量的字段中。

1. 单击&#x200B;**[!UICONTROL Search]**&#x200B;以显示结果。

   ![搜索结果](./assets/storefront-search-advanced-results-modify.png){width="700" zoomable="yes"}

1. 如果他们在搜索结果中未看到要查找的内容，则客户单击&#x200B;**[!UICONTROL Modify your search]**&#x200B;并尝试其他条件组合。

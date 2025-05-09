---
title: 产品属性概述
description: 了解产品属性以及如何使用它们描述产品的特定特征。
exl-id: e15770ee-fb71-43f0-8c26-e8029935799a
feature: Catalog Management, Products
source-git-commit: e0468763b2314e69e8ee4922da9bb9cf65578904
workflow-type: tm+mt
source-wordcount: '532'
ht-degree: 0%

---

# 产品属性概述

属性是产品目录的构建块，用于描述产品的特定特征。 产品属性可以组织为[属性集](attribute-sets.md)，然后用作创建产品的模板。

属性确定用于产品选项的输入控件的类型，并为产品页面提供附加信息。 它们还用作搜索参数和标准，用于分层导航、产品比较报表和促销。 您可以根据需要创建任意数量的属性和属性集来描述目录中的产品。 除了您可以创建的属性之外，系统属性（如价格）也已内置到核心Commerce平台中，无法更改。

![编辑产品时创建新属性](./assets/product-attribute-add-new.png){width="600" zoomable="yes"}

在规划和创建产品属性时，请使用以下部分中描述的最佳实践。

## 属性名称

建立一致的属性命名约定，包括字母大小写和标点。 例如，`Color:Green`和`Color:green`可能被不同的系统视为两个不同的属性值。 数据中的此类噪音可能会影响将产品与规则匹配的应用程序的业务规则、搜索结果和数据过滤器。

## 属性使用

考虑如何在分配属性和值时使用属性。 确定用作演示文稿标签的属性（如产品名称、图像、价格和描述）以及用于数据输入的属性。 考虑属性在整个网站的不同页面中的表示方式，以及它们在类别页面、产品详细信息页面、类别网格和缩略图滑块中的显示方式。

## 颜色

从数据库操作的角度来看，临时颜色描述可能会带来挑战。 颜色名称（如“Azure Skies”或“Robin Egg Blue”）很有吸引力，但在用作搜索条件或推销要求您指定`Color_Family:Blue`时，可能无法返回最佳结果。 考虑搜索结果和分层导航中颜色的显示方式，并为您的业务需求制定一些指导原则。 然后，在整个目录中指定颜色属性值时需保持一致。

## 变量管理

使用产品[配置选项](product-configurations.md)和[可配置产品](product-create-configurable.md)来管理产品方案中的变体。 通过这些功能，可更轻松地对产品进行分类，创建购物车价格规则和动态类别规则，并提供包含各种文本、选择和日期输入类型的选项选择。

## 加权搜索

为[目录搜索](search.md)启用的产品属性可以分配权重，以便在搜索结果中赋予它们较高的值。 权重较大的属性会先于权重较低的属性返回。 例如，考虑系统中的两个属性，搜索权重为3的&#x200B;_color_&#x200B;和搜索权重为1的&#x200B;_description_。 对单词&#x200B;_red_&#x200B;的搜索将返回颜色属性值为`red`的产品列表，但不会返回描述包含&#x200B;_red_&#x200B;的单词的产品。 在此示例中，`color`属性的定义权重大于`description`属性。

## 未使用的属性

删除未使用的产品属性以获得更好的结构化和更快的索引编制。


>[注释！]
>
>有关优化产品属性配置以提高性能的信息，请参阅&#x200B;_实施行动手册_&#x200B;中的[目录管理最佳实践](https://experienceleague.adobe.com/zh-hans/docs/commerce-operations/implementation-playbook/best-practices/planning/catalog-management#product-attributes)。

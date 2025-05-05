---
title: 翻译内容页面
description: 了解如何创建可从特定存储视图中找到的每个页面的翻译版本。
exl-id: e8743ea5-0c8e-4970-987d-c9ac7c1e2a66
feature: Page Content
topic: Commerce, Localization
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '341'
ht-degree: 0%

---

# 翻译内容页面

如果您的商店具有使用不同[语言](../stores-purchase/store-localize.md)的多个视图，并且您已将每个视图的区域设置设置为不同的语言，则结果为部分翻译的站点。 下一步是创建可从特定存储视图中找到的每个页面的翻译版本。 _[!UICONTROL Manage Pages]_&#x200B;列表的[!UICONTROL Store View]列显示具有页面翻译版本的每个视图。

要翻译内容页面，您必须创建另一个页面，该页面具有与原始页面相同的URL键，但已分配给特定的商店视图。 然后，使用翻译的文本更新特定视图的页面。 以下示例说明如何为西班牙商店视图创建&#x200B;_About Us_&#x200B;页面的翻译版本。

## 第1步：为要翻译的页面复制URL键

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**。

1. 在网格中，找到要翻译的页面，并在&#x200B;_编辑_&#x200B;模式下打开。

1. 展开&#x200B;**[!UICONTROL Search Engine Optimization]**&#x200B;部分的![扩展选择器](../assets/icon-display-expand.png)，并将&#x200B;**[!UICONTROL URL Key]**&#x200B;复制到剪贴板。

1. 要返回到&#x200B;_[!UICONTROL Pages]_&#x200B;网格，请单击顶部按钮栏中的&#x200B;**[!UICONTROL Back]**。

## 步骤2：为翻译的内容添加页面

1. 单击&#x200B;**[!UICONTROL Add New Page]**。

1. 输入已翻译的&#x200B;**[!UICONTROL Page Title]**。

1. 展开![扩展选择器](../assets/icon-display-expand.png) **[!UICONTROL Content]**&#x200B;部分并完成页面的已翻译文本。

1. 展开&#x200B;**[!UICONTROL Search Engine Optimization]**&#x200B;部分中的![扩展选择器](../assets/icon-display-expand.png)并执行以下操作：

   - 粘贴您从原始页面复制的&#x200B;**[!UICONTROL URL Key]**。

   - 输入&#x200B;**[!UICONTROL Meta Title]**、**[!UICONTROL Meta Keywords]**&#x200B;和&#x200B;**[!UICONTROL Meta Description]**&#x200B;的已翻译文本。

1. 展开&#x200B;**[!UICONTROL Page in Websites]**&#x200B;部分的![扩展选择器](../assets/icon-display-expand.png)并将&#x200B;**[!UICONTROL Store View]**&#x200B;设置为页面可用的存储视图。

1. 展开![扩展选择器](../assets/icon-display-expand.png) **[!UICONTROL Design]**&#x200B;部分并设置页面的列&#x200B;**[!UICONTROL Layout]**。

1. 单击&#x200B;**[!UICONTROL Save]**。

1. 出现提示时，刷新任何无效的[缓存](../systems/cache-management.md)。

## 步骤3：验证翻译

要验证翻译，请转到店面并使用语言选择器更改店面视图。

请注意，页面上仍有一些元素需要翻译，包括公司页脚链接[块](block-add.md)、[欢迎消息](../getting-started/storefront-branding.md#change-the-welcome-message)和[产品信息](../stores-purchase/store-localize.md#localize-products)。

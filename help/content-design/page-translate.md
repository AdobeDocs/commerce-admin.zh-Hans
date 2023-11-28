---
title: 翻译内容页面
description: 了解如何创建可从特定存储视图中找到的每个页面的翻译版本。
exl-id: e8743ea5-0c8e-4970-987d-c9ac7c1e2a66
feature: Page Content
topic: Commerce, Localization
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '338'
ht-degree: 0%

---

# 翻译内容页面

如果您的商店在不同的页面中有多个视图 [语言](../stores-purchase/store-localize.md)，并且您已将每个视图的区域设置设置为不同的语言，则结果为部分翻译的站点。 下一步是创建可从特定存储视图中找到的每个页面的翻译版本。 此 [!UICONTROL Store View] 列 _[!UICONTROL Manage Pages]_列表显示具有页面翻译版本的每个视图。

要翻译内容页面，您必须创建另一个页面，该页面具有与原始页面相同的URL键，但已分配给特定的商店视图。 然后，使用翻译的文本更新特定视图的页面。 以下示例说明如何创建 _关于我们_ 西班牙商店视图页面。

## 第1步：为要翻译的页面复制URL键

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. 在网格中，找到要翻译的页面，并在中打开 _编辑_ 模式。

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Search Engine Optimization]** 部分并复制 **[!UICONTROL URL Key]** 到剪贴板中。

1. 返回 _[!UICONTROL Pages]_网格，单击&#x200B;**[!UICONTROL Back]**在顶部按钮栏中。

## 步骤2：为翻译的内容添加页面

1. 单击 **[!UICONTROL Add New Page]**.

1. 输入已翻译的内容 **[!UICONTROL Page Title]**.

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Content]** 并完成页面的已翻译文本。

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Search Engine Optimization]** 部分并执行以下操作：

   - 粘贴 **[!UICONTROL URL Key]** 从原始页面复制的。

   - 输入已翻译的文本 **[!UICONTROL Meta Title]**， **[!UICONTROL Meta Keywords]**、和 **[!UICONTROL Meta Description]**.

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Page in Websites]** 分区和设置 **[!UICONTROL Store View]** 页面可用的商店视图。

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Design]** 并设置列 **[!UICONTROL Layout]** 页面的。

1. 单击 **[!UICONTROL Save]**.

1. 出现提示时，刷新任何无效的 [缓存](../systems/cache-management.md).

## 步骤3：验证翻译

要验证翻译，请转到店面并使用语言选择器更改店面视图。

请注意，页面上仍有一些需要翻译的元素，包括公司页脚链接 [块](block-add.md)， [欢迎消息](../getting-started/storefront-branding.md#change-the-welcome-message)、和 [产品信息](../stores-purchase/store-localize.md#localize-products).

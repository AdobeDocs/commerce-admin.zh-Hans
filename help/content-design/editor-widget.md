---
title: 在编辑器中插入构件
description: 使用WYSIWYG编辑器中的小组件工具，将各种内容元素添加到页面中。
exl-id: bbc5e059-06d8-4dda-89a7-6c9826b73fd3
badgePaas: label="仅限PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="仅适用于云项目(Adobe管理的PaaS基础架构)和内部部署项目上的Adobe Commerce 。"
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '346'
ht-degree: 0%

---

# 在编辑器中插入构件

[构件](widget-create.md)工具可用于向页面添加各种内容元素，包括指向任何Commerce内容页面或节点、产品或类别的链接。 链接能够以块格式放置在页面上，或直接并入内容中。 您可以使用构件工具创建指向以下内容类型的链接：

- [内容页面](pages.md)
- [目录类别](../catalog/categories.md)
- [目录产品](../catalog/product-create.md)

默认情况下，链接会从主题的样式表中继承其样式。

{{$include /help/_includes/directives-caution.md}}

1. 在编辑模式下打开页面、块或动态块。

1. 转到&#x200B;_[!UICONTROL Content]_&#x200B;部分并单击支持该编辑器的任何元素。

1. 将光标放在您希望小组件出现的位置，然后单击&#x200B;_插入小组件_&#x200B;图标。

   ![编辑器工具栏 — 插入小组件](./assets/editor-toolbar-widget-button.png){width="700" zoomable="yes"}

   如果未启用页面生成器，但希望使用代码，请单击&#x200B;**[!UICONTROL Show / Hide Editor]**。 将插入点放置在要显示小部件的文本中。 然后，单击&#x200B;**[!UICONTROL Insert Widget]**。

1. 选择&#x200B;**[!UICONTROL Widget Type]**。

   有关这些选项的更多信息，请参阅[构件类型](widgets.md#widget-types)。 以下步骤使用了一个示例来插入指向产品的链接。

1. 若要使用产品名称，请将&#x200B;**[!UICONTROL Anchor Custom Text]**&#x200B;字段留空。

1. 输入&#x200B;**[!UICONTROL Anchor Custom Title]**&#x200B;以获得最佳SEO实践。

   此标题在页面上不可见。

1. 将&#x200B;**[!UICONTROL Template]**&#x200B;设置为以下项之一：

   - 要将链接合并到文本中，请选择`Product Link Inline Template`。

   - 要将链接放在单独的一行中，请选择`Product Link Block Template`。

1. 单击&#x200B;**[!UICONTROL Select Product]**&#x200B;并执行以下操作：

   - 在树中，导航到所需的类别。

   - 在列表中，选择链接的产品。

1. 单击&#x200B;**[!UICONTROL Insert Widget]**&#x200B;将链接放置到页面上。

   如果使用HTML代码，则链接的[标记标记](../systems/markup-tags.md)将显示在页面顶部，并用双大括号括起来。 如果需要，可使用&#x200B;_剪切并粘贴_&#x200B;将标记标记标记放置在您希望链接显示的代码中。

1. 完成内容编辑后，单击&#x200B;**[!UICONTROL Save]**。

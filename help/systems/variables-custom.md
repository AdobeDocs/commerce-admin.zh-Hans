---
title: 添加自定义变量
description: 了解如何创建自定义变量并将其插入到页面、块和产品内容中。
exl-id: 8233518a-abcf-4889-b75b-4aa503c7cebb
role: Admin, User
feature: System, Variables, Page Content, Communications
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '341'
ht-degree: 1%

---

# 添加自定义变量

为了满足您的特定业务需求，您可以创建自定义变量并将它们插入到 [页面](../content-design/pages.md)， [个块](../content-design/blocks.md)、和 [电子邮件模板](email-templates.md). 单击 _插入变量_ 按钮包含两者 [预定义](variables-predefined.md) 和自定义变量。 特定电子邮件模板的可用变量列表由与该模板关联的数据确定。 请参阅 [变量引用](variables-reference.md) 有关常用电子邮件模板及其关联变量的列表。

![自定义变量](./assets/variables-custom.png){width="600" zoomable="yes"}

>[!NOTE]
>
>电子邮件和新闻稿模板中只能使用允许的预定义或自定义变量。

## 第1步：创建自定义变量

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL System]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Custom Variables]**.

1. 单击 **[!UICONTROL Add New Variable]**.

1. 输入标识符 **[!UICONTROL Variable Code]**，全部使用小写字符且不加空格。

   如果需要，您可以使用下划线字符或连字符来表示空格。 例如： `my_custom_variable`

1. 输入 **[!UICONTROL Variable Name]**，用于内部引用。 例如： `My Custom Variable`

1. 要输入与变量关联的值，请执行下列操作之一：

   - 对象 **[!UICONTROL Variable HTML Value]**，输入使用简单HTML标记格式化的变量值。 例如：

     `<b>This formatted content appears in place of the variable.</b>`

   - 对象 **[!UICONTROL Variable Plain Value]**，以纯文本形式输入变量值，而不设置格式。 例如：

     `This unformatted content appears in place of the variable.`

   >[!TIP]
   >
   >如果需要更多空间，请拖动文本框的右下角。

   ![新建自定义变量](./assets/variable-custom-add.png){width="600" zoomable="yes"}

1. 完成后，单击 **[!UICONTROL Save]**.

## 步骤2：在内容中插入自定义变量

使用 [!DNL Page Builder] 以插入自定义变量。

1. 打开要将变量添加到内容的页面、块、类别或产品。

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Content]** 部分。

1. 单击 **[!UICONTROL Edit with Page Builder]**.

1. 在左侧面板中，单击 **[!UICONTROL Elements]** 并执行以下操作之一：

   - 在要插入变量的现有文本区域中单击。

   - 拖动新的 **[!UICONTROL Text]** 舞台上的对象。

1. 在编辑器工具栏的最右侧，单击( ![插入变量](./assets/editor-btn-insert-variable.png) )以插入变量。

   ![[!DNL Page Builder] 暂存和面板](./assets/variable-custom-pagebuilder-stage.png){width="600" zoomable="yes"}

1. 在列表中，选择要插入的自定义变量，然后单击 **[!UICONTROL Insert Variable]**.

   ![新建自定义变量](./assets/variable-custom-insert-select.png){width="600" zoomable="yes"}

   变量标识符在编辑器中显示为占位符。

   ![[!DNL Page Builder] 阶段 — 变量占位符](./assets/pagebuilder-variable-inserted.png){width="600" zoomable="yes"}

1. 完成后，单击 **[!UICONTROL Save]**.

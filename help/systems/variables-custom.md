---
title: 添加自定义变量
description: 了解如何创建自定义变量并将其插入到页面、块和产品内容中。
exl-id: 8233518a-abcf-4889-b75b-4aa503c7cebb
role: Admin, User
feature: System, Variables, Page Content, Communications
TQID: 'https://experienceleague.adobe.com/zhgemfdr2g5sanaFuiF9l20figj9ZD-3codE97WWWg8'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
    internal-label: Security
  - id: 8d0b446f-5b16-5a10-b272-01143504a11c
    internal-label: System
  - id: 17d326fa-534a-55a5-b46f-8ae1de1e2f75
    internal-label: Page Content
  - id: bb03f6c4-cab9-560e-9d02-5816e1808d17
    internal-label: Communications
subfeature_v2:
  - id: 2191e157-828a-5358-ad69-ebcaa8402915
    internal-label: Variables
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: acc7571574eb9c7e96911266897350a77913488e
workflow-type: tm+mt
source-wordcount: '344'
ht-degree: 1%
---
# 添加自定义变量

为满足您业务的特定需求，您可以创建自定义变量并将其插入到[页面](../content-design/pages.md)、[块](../content-design/blocks.md)和[电子邮件模板](email-templates.md)中。 单击&#x200B;_插入变量_&#x200B;按钮时显示的允许变量列表包括[预定义](variables-predefined.md)和自定义变量。 特定电子邮件模板的可用变量列表由与该模板关联的数据确定。 有关常用电子邮件模板及其关联变量的列表，请参阅[变量引用](variables-reference.md)。

![自定义变量](./assets/variables-custom.png){width="600" zoomable="yes"}

>[!NOTE]
>
>电子邮件和新闻稿模板中只能使用允许的预定义或自定义变量。

## 第1步：创建自定义变量

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL System]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Custom Variables]**。

1. 单击&#x200B;**[!UICONTROL Add New Variable]**。

1. 输入&#x200B;**[!UICONTROL Variable Code]**&#x200B;的标识符，使用所有小写字符且不加空格。

   如果需要，您可以使用下划线字符或连字符来表示空格。 例如： `my_custom_variable`

1. 输入用于内部引用的&#x200B;**[!UICONTROL Variable Name]**。 例如： `My Custom Variable`

1. 要输入与变量关联的值，请执行下列操作之一：

   - 对于&#x200B;**[!UICONTROL Variable HTML Value]**，输入使用简单HTML标记格式化的变量值。 例如：

     `<b>This formatted content appears in place of the variable.</b>`

   - 对于&#x200B;**[!UICONTROL Variable Plain Value]**，以纯文本形式输入变量值，而不设置格式。 例如：

     `This unformatted content appears in place of the variable.`

   >[!TIP]
   >
   >如果需要更多空间，请拖动文本框的右下角。

   ![新自定义变量](./assets/variable-custom-add.png){width="600" zoomable="yes"}

1. 完成后，单击&#x200B;**[!UICONTROL Save]**。

## 步骤2：在内容中插入自定义变量

使用[!DNL Page Builder]插入自定义变量。

1. 打开要将变量添加到内容的页面、块、类别或产品。

1. 展开&#x200B;**[!UICONTROL Content]**&#x200B;部分的![扩展选择器](../assets/icon-display-expand.png)。

1. 单击&#x200B;**[!UICONTROL Edit with Page Builder]**。

1. 在左侧面板中，单击&#x200B;**[!UICONTROL Elements]**&#x200B;并执行以下操作之一：

   - 在要插入变量的现有文本区域中单击。

   - 将新的&#x200B;**[!UICONTROL Text]**&#x200B;对象拖到舞台上。

1. 在编辑器工具栏的最右侧，单击（![插入变量](./assets/editor-btn-insert-variable.png) ）以插入变量。

   ![[!DNL Page Builder]阶段和面板](./assets/variable-custom-pagebuilder-stage.png){width="600" zoomable="yes"}

1. 在列表中，选择要插入的自定义变量，然后单击&#x200B;**[!UICONTROL Insert Variable]**。

   ![新自定义变量](./assets/variable-custom-insert-select.png){width="600" zoomable="yes"}

   变量标识符在编辑器中显示为占位符。

   ![[!DNL Page Builder]阶段 — 变量占位符](./assets/pagebuilder-variable-inserted.png){width="600" zoomable="yes"}

1. 完成后，单击&#x200B;**[!UICONTROL Save]**。

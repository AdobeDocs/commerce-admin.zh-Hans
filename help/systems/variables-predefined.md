---
title: 使用预定义变量
description: 了解预定义变量以及如何在电子邮件模板中添加它们。
exl-id: 01e909c4-c932-4262-9f33-bd2740a6355f
role: Admin, User
feature: System, Variables, Page Content, Communications
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 0%

---

# 使用预定义变量

[预定义](variables-predefined.md) 变量使个性化更容易 [电子邮件](email-templates.md) 和 [新闻稿](../merchandising-promotions/newsletters.md) 模板和其他类型的内容。 允许的列表 [预定义](variables-predefined.md) 单击“插入变量”按钮时，将显示变量。 如下图所示，特定电子邮件模板的可用变量列表由与该模板关联的数据决定。 请参阅 [变量引用](variables-reference.md) 有关常用电子邮件模板及其关联变量的列表。

![电子邮件模板的预定义变量](./assets/email-template-new-pickup-order-predefined-variables.png){width="700" zoomable="yes"}

## 向电子邮件模板添加变量

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Email Templates]**.

1. 执行以下操作之一：

   - 要将变量添加到现有模板，请在列表中单击该模板以在编辑模式下打开。

   - 要在新模板中使用变量，请单击 **[!UICONTROL Add New Template]** 和自定义默认模板代码。 请参阅 [消息模板](email-template-custom.md#message-templates).

1. 下 _[!UICONTROL Load default template]_，选择&#x200B;**[!UICONTROL Template]**要进行自定义的页面。

1. 要应用模板，请单击 **[!UICONTROL Load Template]**.

   此 _[!UICONTROL Currently used for]_字段显示模板的配置路径。 此_[!UICONTROL Template Subject]_ 和 _[!UICONTROL Template Content]_相对于所选模板自动生成。

   - **[!UICONTROL Template Subject]**  — 此文本显示在电子邮件的主题行中。

   - **[!UICONTROL Template Content]**  — 此文本显示在已发送电子邮件的完整内容中。

   ![电子邮件模板内容](./assets/email-template-content.png){width="600" zoomable="yes"}

1. 输入 **[!UICONTROL Template Name]**.

1. 要查看 [预定义](variables-predefined.md) 可以与此电子邮件模板一起使用的变量，请单击 **[!UICONTROL Insert Variable]**.

   确定要插入到模板中的变量。 然后，单击 _关闭_ (X)的右上角。 （稍后将返回此页面。）

1. 要查看模板模型，请单击 **[!UICONTROL Preview Template]** 在按钮栏中。

   当预览在新选项卡中打开时，请确定变量相对于其他内容的放置位置。 然后返回到原始选项卡以继续。

   ![预览模板](./assets/email-template-new-pickup-order-preview.png){width="600" zoomable="yes"}

1. 在 **[!UICONTROL Template Content]** 框，将插入点放置在要显示变量的位置，然后单击 **[!UICONTROL Insert Variable...]**.

1. 在可用变量列表中，单击要插入到模板中的变量。

1. 完成后，单击 **[!UICONTROL Save Template]**.

## 将模板转换为纯文本

1. 在编辑模式下打开模板。

1. 在页面顶部，单击 **[!UICONTROL Convert to Plain Text]**.

1. 提示删除标记时，单击 **[!UICONTROL OK]**.

1. 要保存纯文本版本，请单击 **[!UICONTROL Save Template]**.

## 恢复HTML版本

1. 在页面顶部，单击 **[!UICONTROL Return HTML Version]**.

1. 要保存模板的HTML版本，请单击 **[!UICONTROL Save Template]**.

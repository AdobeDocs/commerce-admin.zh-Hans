---
title: 礼品注册设置
description: 了解如何为商店客户设置礼品注册类型。
exl-id: d618c769-10be-4881-a799-42484d35c57b
feature: Gift, Storefront
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '1091'
ht-degree: 0%

---

# 礼品注册设置

{{ee-feature}}

可以为任何类型的活动（例如婚礼、生日、周年纪念日、新生婴儿或任何其他特殊场合）创建礼品注册表。 默认情况下，Adobe Commerce包括以下特殊活动：

- 婴儿
- 生日
- 婚礼

在创建注册表时，它会成为客户帐户中礼品注册表类型列表中的选项。

您可以使用三个准备好的礼品登记簿之一，或者创建您自己的自定义登记簿。 每个礼品注册类型都包含多个属性，这些属性是客户创建礼品注册时完成的数据输入字段。 属性提供有关事件、时间和位置的附加信息，或所需的任何其他信息。 根据输入类型，某些属性有多个选项。 例如，`Wedding`礼品注册表类型具有属性`Role`，并具有`Bride`、`Groom`和`Partner`选项。 若要了解有关属性和输入类型的详细信息，请参阅[属性](../customers/attribute-properties.md)。

![礼品注册表类型](./assets/gift-registry-types.png){width="700" zoomable="yes"}

## 使用准备好的礼品登记表

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Gift Registry]**。

   生日、婚礼和婴儿登记处已可供客户从他们的帐户中使用。

1. 确保完成[电子邮件模板配置](../systems/email-templates.md#configure-email-templates)，以便它们反映您的品牌。

## 创建自定义礼品注册表

1. 在管理员侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Gift Registry]**。

1. 单击右上角的&#x200B;**[!UICONTROL Add Gift Registry Type]**。

1. 在&#x200B;**[!UICONTROL General Information]**&#x200B;下，完成以下操作：

   - 输入唯一的&#x200B;**[!UICONTROL Code]**&#x200B;以在内部标识礼品注册表。

     代码必须以小写字母开头。 其余代码可以是小写字母(a-z)、数字(0-9)和下划线(`_`)的任意组合。

   - 对于&#x200B;**[!UICONTROL Label]**，输入您希望在商店中显示的礼品注册名称。

     此标签是客户可用的礼品注册类型列表中的选项。

   - 对于&#x200B;**[!UICONTROL Sort Order]**，输入一个数字以确定此礼品注册与其他类型一起列出时的显示顺序。

   - 要激活礼品注册表，请将&#x200B;**[!UICONTROL Is Listed]**&#x200B;设置为`Yes`。

     ![礼品注册表 — 常规信息](./assets/gift-registry-new-general-information.png){width="600" zoomable="yes"}

1. 检查礼品注册表的每个部分，以确定要包括的信息类型。

1. 在左侧面板中，选择&#x200B;**[!UICONTROL Attributes]**&#x200B;并单击&#x200B;**[!UICONTROL Add Attribute]**。

   ![礼品注册表 — 新属性](./assets/gift-registry-type-new-attribute.png){width="600" zoomable="yes"}

1. 对于每个属性，执行以下操作：

   - 分配唯一的&#x200B;**[!UICONTROL Code]**&#x200B;以在内部标识该属性。 该代码的长度最多可为15个字符，且必须以小写字母开头。 其余代码可以包括小写字母(`a`-`z`)、数字(`0`-`9`)和下划线(`_`)字符来分隔单词。

   - 选择要用于数据输入的&#x200B;**[!UICONTROL Input Type]**。 您可以使用自定义类型或静态类型之一。

   - 如果输入类型有多个选项，请单击&#x200B;**[!UICONTROL Add New Option]**&#x200B;并填写每个选项的信息。

     某些输入类型具有其他属性。 例如，事件位置具有使事件可搜索的其他属性，并包含在商店的礼品注册公开列表中。

      - 将&#x200B;**[!UICONTROL Attribute Group]**&#x200B;设置为礼品注册表中希望显示属性的部分。

      - 对于&#x200B;**[!UICONTROL Label]**，输入名称以标识注册表中的数据输入字段。

      - 如果要求客户进行选择或在字段中输入值，请将&#x200B;**[!UICONTROL Is Required]**&#x200B;设置为`Yes`。

      - 对于&#x200B;**[!UICONTROL Sort Order]**，请输入一个数字以确定此礼品注册与其他可能在商店中提供的礼品注册一起列出时的显示顺序。

1. 若要添加其他选项，请单击&#x200B;**添加新选项**。

   添加的每个新选项都会显示在顶部的新部分中。 对新属性重复此过程。

1. 完成后，单击&#x200B;**[!UICONTROL Save]**。

## 字段描述

### [!UICONTROL General Information]

| 字段 | 描述 |
|--- |--- |
| [!UICONTROL Code] | 用于在内部标识礼品注册类型的唯一名称。 该代码的第一个字符必须为小写字母。 其余代码可以是小写字母(a-z)、数字(0-9)和下划线字符(`_`)的任意组合。 |
| [!UICONTROL Label] | 出现在商店中的礼品注册表类型的名称。 |
| [!UICONTROL Sort Order] | 确定与其他类型一起列出时此礼品注册类型的显示顺序。 |
| [!UICONTROL Is Listed] | 确定商店中的客户是否可以使用礼品注册类型。 选项： `Yes` / `No`。 |

{style="table-layout:auto"}

### [!UICONTROL Attributes]

| 字段 | 描述 |
|--- |--- |
| [!UICONTROL Code] | 用于在内部标识属性的唯一名称。 代码可以包含小写字母(a-z)、数字(0-9)和下划线字符(`_`)的任意组合。 |
| [!UICONTROL Input Type] | 根据类型确定与属性关联的数据类型和输入控件。 |
| [!UICONTROL Attribute Group] | 选择属性在礼品注册表中列出的组。 |
| [!UICONTROL Label] | 在客户的帐户仪表板中标识属性的名称。 |
| [!UICONTROL Is Required] | 指示属性是否为必需条目。 在完成所有必需属性之前，无法保存礼品注册表。 选项： `Yes` / `No`。 |
| [!UICONTROL Sort Order] | 确定与其他属性一起列出时属性出现的顺序。 |

{style="table-layout:auto"}

#### [!UICONTROL Input Type Options]

选择与属性关联的数据类型和输入控件。

**_[!UICONTROL Custom Types]_**

| 字段 | 描述 |
|--- |--- |
| [!UICONTROL Text] | 将属性显示为文本字段。 |
| [!UICONTROL Select] | 将属性显示为下拉列表。 单击&#x200B;**[!UICONTROL Add New Option]**&#x200B;可向下拉列表添加更多条件：<br/>**[!UICONTROL Code]**— 用于内部标识属性的唯一名称。<br/>**[!UICONTROL Label]** — 在客户的帐户仪表板中标识属性的名称。<br/>**[!UICONTROL Is Default]**— 设置此开关以选择默认条件。<br/>**[!UICONTROL Delete Option]** — 单击以删除选项。 |
| [!UICONTROL Date] | 将属性显示为日期字段。 选项： `Short (3/23/2014)` / `Medium (Mar 23, 1914)` / `Long (March 23, 1914)` / `Full (Sunday, March 23, 2014)` |
| [!UICONTROL Country] | 将属性显示为国家/地区的下拉列表。 将&#x200B;**[!UICONTROL Show Region]**&#x200B;设置为： `Yes` / `No`。 |

{style="table-layout:auto"}

**_[!UICONTROL Static Types]_**

| 字段 | 描述 |
|--- |--- |
| [!UICONTROL Event Date] | 确定在存储中使用日期属性的方式。 选项： <br/>**[!UICONTROL Searchable]**— 确定该属性是否可用于高级搜索。 选项： `Yes` / `No`。<br/>**[!UICONTROL Is Listed]** — 确定该事件是否包含在存储中可用的事件列表中。 选项： `Yes` / `No`。 <br/>**[!UICONTROL Date Format]**— 确定事件日期的格式。 选项： `Short (3/23/2014)` / `Medium (Mar 23, 1914)` / `Long (March 23, 1914)` / `Full (Sunday, March 23, 2014)` |
| [!UICONTROL Event Country] | 将属性显示为国家/地区列表。 选项： <br/>**[!UICONTROL Searchable]**— 确定该属性是否可用于高级搜索。 选项： `Yes` / `No`。<br/>**[!UICONTROL Is Listed]** — 确定该事件是否包含在存储中可用的事件列表中。 选项： `Yes` / `No`。 <br/>**[!UICONTROL Show Region]**— 确定事件的区域。 |
| [!UICONTROL Event Location] | 与礼品注册相关的事件的位置。 <br/>将&#x200B;**[!UICONTROL Is Searcheable]**&#x200B;设置为： `Yes` / `No` <br/>将&#x200B;**[!UICONTROL Is Listed]**&#x200B;设置为： `Yes` / `No` |
| [!UICONTROL Role] | 用于标识礼品收件人的角色。 例如，`Bride`、`Groom`或`Partner`。<br/>**[!UICONTROL Is Searcheable]**— 设置为`Yes`/ `No`<br/>**&#x200B;已列出&#x200B;**— 设置为`Yes` / `No`<br/>**[!UICONTROL Add New Option]** — 单击向下拉菜单添加更多条件：<br/>**代码** — 用于内部标识属性的唯一名称。<br/>**[!UICONTROL Label]**— 在客户的帐户仪表板中标识属性的名称。<br/>**[!UICONTROL Is Default]** — 设置此开关以选择默认条件。<br/>**[!UICONTROL Delete Option]**— 单击以删除选项。 |

{style="table-layout:auto"}

#### [!UICONTROL Attribute Group Options]

选择属性在礼品注册表中列出的组。

| 字段 | 描述 |
|--- |--- |
| [!UICONTROL Event Information] | 对所有添加有关礼品注册事件、时间、地点等信息的礼品注册属性进行分组。 |
| [!UICONTROL Gift Registry Properties] | 合并所有属性，这些属性直接添加有关礼品注册的信息。 |
| [!UICONTROL Privacy Settings] | 列出添加有关礼品注册事件隐私信息的属性。 |
| [!UICONTROL Recipients Information] | 对属性进行分组，以提供有关创建礼品注册表的人员的信息。 |
| [!UICONTROL Shipping Address] | 组合用于添加有关礼品注册事件装运地址信息的属性。 |

{style="table-layout:auto"}

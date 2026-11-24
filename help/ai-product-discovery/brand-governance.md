---
title: 创建目录扩充品牌规则
description: 了解如何为目录扩充创建和管理品牌治理规则、定义产品复制要求以及将规则应用于目录扩充作业。
role: Admin, User, Leader
source-git-commit: 9d7a4f4e98fe2d2d51261d96a2e072c28925babd
workflow-type: tm+mt
source-wordcount: '639'
ht-degree: 1%
---
# 创建目录扩充品牌规则

品牌治理和品牌治理规则仅适用于目录扩充。 它们不适用于PDP扩充。 这些规则定义了[!DNL Commerce Catalog Agent]生成的产品名称和说明的要求。 编辑或配置默认品牌标准的默认规则，然后为特定营销活动、产品类别或子品牌创建自定义规则。 在创建[目录扩充](catalog-enrichment.md)作业时Select规则。

## 开放式品牌治理

1. 在“管理员”中，转到&#x200B;**[!UICONTROL AI Product Discovery]** > **[!UICONTROL Catalog Enrichment]**。
1. 打开&#x200B;**[!UICONTROL Brand Governance]**&#x200B;选项卡。

**品牌治理**&#x200B;选项卡包含默认规则和您创建的任何自定义规则。 您可以搜索规则或筛选规则表。

每行都会看到&#x200B;**规则名称**、**字段**、**音调**、**上次修改时间**&#x200B;和&#x200B;**状态**。 默认规则标记为&#x200B;**[!UICONTROL Default]**。

**[!UICONTROL Needs your attention]**&#x200B;区域突出显示需要处理的规则，例如需要设置的草稿或存在冲突的规则。 查看规则详细信息并使用可用的操作，如&#x200B;**[!UICONTROL Finish setup]**&#x200B;或&#x200B;**[!UICONTROL Fix conflict]**。

## 了解规则类型

目录扩充支持默认规则和自定义规则。

### 默认规则

每个[!DNL Adobe Commerce]实例只有一个默认规则。 [!DNL Adobe Commerce]创建具有空字段的规则。 其名称固定为&#x200B;**[!UICONTROL Global]**。 您可以编辑规则，但无法删除它。

在创建目录扩充作业时，[!DNL Adobe Commerce]默认应用默认规则，而不选择自定义规则。 默认规则为目录扩充提供基线管理。

### 自定义规则

您可以为促销活动、产品类别或子品牌创建任意数量的自定义规则。 自定义规则不会自动应用。 在创建目录扩充作业时Select它。

自定义规则不继承默认规则的值。 创建自定义规则时，您可以复制默认规则的当前值作为一次性起点。 对默认规则的后续更改不会更新自定义规则。

将“默认规则”用于用户未选择自定义规则时应应用的标准。 为具有不同要求的营销活动或类别创建自定义规则。 添加自定义规则还需要的任何全局要求，因为自定义规则不会继承全局值。

## 创建自定义规则

在此部分中，您将了解如何创建品牌治理规则。

![创建品牌治理规则](./assets/brand-gov-create-rule.png)

1. 在&#x200B;**品牌治理**&#x200B;选项卡中，单击&#x200B;**[!UICONTROL Create Rule]**。
1. 选择启动规则的方式：
   - **[!UICONTROL Blank]**：自行设置所有值。
   - **[!UICONTROL Copy Global enrichment]**：以当前默认规则值作为一次性副本开始。
   - **[!UICONTROL Draft with AI]**： （**即将推出**）描述您的品牌声音，以获取建议的规则值。
1. 输入标识其用途的&#x200B;**规则名称**，如促销活动、类别或子品牌。
1. 在要增强&#x200B;**的**&#x200B;字段下，配置产品名称和产品描述要求。

   分别配置产品名称和描述。 每个字段都有自己的启用交换机和治理要求。

1. 设置&#x200B;**产品名称长度**。

   设置扩充产品名称的最小和最大名称长度范围。 例如，规则最少可包含20个字符，最多可包含200个字符。

1. 设置&#x200B;**大写**&#x200B;选项：

   - **[!UICONTROL Sentence case]**: `Waterproof hiking boots`
   - **[!UICONTROL Title Case]**: `Waterproof Hiking Boots`
   - **[!UICONTROL As written]**：保留源文本的大写。

1. 描述&#x200B;**品牌色调**。 请参阅[设置品牌调](#set-brand-tone)以获取指导。
1. 设置必需和排除的短语

   添加&#x200B;**[!UICONTROL Must include]**短语。
   添加**[!UICONTROL Never use]**&#x200B;短语。

1. 单击&#x200B;**[!UICONTROL Save as draft]**&#x200B;稍后完成，或单击&#x200B;**[!UICONTROL Publish rule]**&#x200B;以在创建目录扩充规则时可供选择规则。 单击&#x200B;**[!UICONTROL Cancel]**&#x200B;离开而不保存。

1. 您现在可以将规则应用于[目录扩充](catalog-enrichment.md)作业。

### 设置品牌色调

在多行&#x200B;**[!UICONTROL Brand tone]**&#x200B;字段中输入指南以描述扩充名称的声音和样式。

以下是您可以用于&#x200B;**描述**&#x200B;的一些色调示例：

- **B2B工业**： `Write for the operator and the buyer. Open with what the unit does and where it fits in the kitchen, then throughput, utility requirements, footprint, and certifications. Plain, technical language. Mention cleaning and maintenance, because total cost of ownership drives the decision. No lifestyle language.`
- **奢侈时尚**： `Quiet confidence. Lead with craftsmanship and provenance (atelier, tannery, technique), then how the piece wears and ages. Short, measured sentences. Sensory detail is fine. Never compare to other brands or mention price or value.`
- **消费电子产品**： `Clear and benefit-led. Turn every spec into what it does for the user. Scannable short paragraphs or bullets. Put compatibility and what's in the box up front. Don't make performance claims without a source, and don't use comparative claims like "fastest"`
- **特色食品和杂货**： `Warm and appetizing, but honest. Describe taste, texture, and aroma in concrete terms, then origin and how it's made, then serving ideas. Plain, friendly language. Put allergens and dietary attributes in a consistent closing line. Don't make health claims.`
- **家庭家具**： `Inviting and practical. Open with how the piece is used, then dimensions, materials, and care. Help the shopper picture it in their space without overselling. Always mention assembly, delivery, and weight, since those drive returns.`

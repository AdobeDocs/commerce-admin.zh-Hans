---
title: 客户地址模板
description: 了解如何自定义客户地址模板。
exl-id: 9fd32c0a-ff9a-47f9-84e2-f5d6bf307d8c
feature: Customers, Configuration
TQID: https://experienceleague.adobe.com/b8tCsMqk6IQJjs5YWCH4-CNmBPrz-3pdPG7ttH4eawk
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: bd989d82-1e15-4534-88db-f1f51dd77ffaid: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 146
ht-degree: 0%

---

# 客户地址模板

{{ee-feature}}

您可以修改模板，以控制打印发票、发运和退款以及客户帐户地址簿中显示的客户开单和发运地址的格式。 如果要包含其他信息，可创建与客户帐户和[地址](address-attributes.md)关联的[自定义属性](attribute-properties.md)，并将它们合并到模板中。

## 示例1：短格式

对于[!UICONTROL Text One Line]地址模板：

```text
{{depend prefix}}{{var prefix}} {{/depend}}{{var firstname}} {{depend middlename}}{{var middlename}} {{/depend}}{{var lastname}}{{depend suffix}} {{var suffix}}{{/depend}}, {{var street}}, {{var city}}, {{var region}} {{var postcode}}, {{var country}}
```

## 示例2：长格式

对于[!UICONTROL Text]、[!UICONTROL HTML]和[!UICONTROL PDF]地址模板：

```text
{{depend prefix}}{{var prefix}} {{/depend}}{{var firstname}} {{depend middlename}}{{var middlename}} {{/depend}}{{var lastname}}{{depend suffix}} {{var suffix}}{{/depend}}{{depend company}}{{var company}}{{/depend}}{{if street1}}{{var street1}}{{/if}}{{depend street2}}{{var street2}}{{/depend}}{{depend street3}}{{var street3}}{{/depend}}{{depend street4}}{{var street4}}{{/depend}}{{if city}}{{var city}},  {{/if}}{{if region}}{{var region}}, {{/if}}{{if postcode}}{{var postcode}}{{/if}}{{var country}}{{depend telephone}}T: {{var telephone}}{{/depend}}{{depend fax}}F: {{var fax}}{{/depend}}{{depend vat_id}}VAT: {{var vat_id}}{{/depend}}
```

![客户地址模板](../configuration-reference/customers/assets/customer-configuration-address-templates.png){width="600" zoomable="yes"}

## 更改地址字段的顺序

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧面板中，展开&#x200B;**[!UICONTROL Customers]**&#x200B;并选择&#x200B;**[!UICONTROL Customer Configuration]**。

1. 单击以展开&#x200B;**[!UICONTROL Address Templates]**&#x200B;部分。

   部分包含适用于以下各项的单独格式化说明集：

   - [!UICONTROL Text]
   - [!UICONTROL Text One Line]
   - [!UICONTROL HTML]
   - [!UICONTROL PDF]

1. 根据需要编辑每个模板，并参考这些示例。

1. 完成后，单击&#x200B;**[!UICONTROL Save Config]**。

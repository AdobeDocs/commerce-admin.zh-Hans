---
title: 客户地址模板
description: 了解如何自定义客户地址模板。
exl-id: 9fd32c0a-ff9a-47f9-84e2-f5d6bf307d8c
feature: Customers, Configuration
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 0%

---

# 客户地址模板

{{ee-feature}}

您可以修改模板，以控制打印发票、发运和退款以及客户帐户地址簿中显示的客户开单和发运地址的格式。 如果要包含其他信息，您可以创建 [自定义属性](attribute-properties.md) 关联到的客户帐户和 [地址](address-attributes.md)，并将它们合并到模板中。

## 示例1：短格式

对象 [!UICONTROL Text One Line] 地址模板：

```text
{{depend prefix}}{{var prefix}} {{/depend}}{{var firstname}} {{depend middlename}}{{var middlename}} {{/depend}}{{var lastname}}{{depend suffix}} {{var suffix}}{{/depend}}, {{var street}}, {{var city}}, {{var region}} {{var postcode}}, {{var country}}
```

## 示例2：长格式

对象 [!UICONTROL Text]， [!UICONTROL HTML]、和 [!UICONTROL PDF] 地址模板：

```text
{{depend prefix}}{{var prefix}} {{/depend}}{{var firstname}} {{depend middlename}}{{var middlename}} {{/depend}}{{var lastname}}{{depend suffix}} {{var suffix}}{{/depend}}{{depend company}}{{var company}}{{/depend}}{{if street1}}{{var street1}}{{/if}}{{depend street2}}{{var street2}}{{/depend}}{{depend street3}}{{var street3}}{{/depend}}{{depend street4}}{{var street4}}{{/depend}}{{if city}}{{var city}},  {{/if}}{{if region}}{{var region}}, {{/if}}{{if postcode}}{{var postcode}}{{/if}}{{var country}}{{depend telephone}}T: {{var telephone}}{{/depend}}{{depend fax}}F: {{var fax}}{{/depend}}{{depend vat_id}}VAT: {{var vat_id}}{{/depend}}
```

![客户地址模板](../configuration-reference/customers/assets/customer-configuration-address-templates.png){width="600" zoomable="yes"}

## 更改地址字段的顺序

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中，展开 **[!UICONTROL Customers]** 并选择 **[!UICONTROL Customer Configuration]**.

1. 单击以展开 **[!UICONTROL Address Templates]** 部分。

   部分包含适用于以下各项的单独格式化说明集：

   - [!UICONTROL Text]
   - [!UICONTROL Text One Line]
   - [!UICONTROL HTML]
   - [!UICONTROL PDF]

1. 根据需要编辑每个模板，并参考这些示例。

1. 完成后，单击 **[!UICONTROL Save Config]**.

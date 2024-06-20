---
title: 数据传输
description: 了解对数据传输的支持，包括数据验证。
exl-id: 5057e398-c458-42e9-8ec0-bf116a667a3c
feature: System, Data Import/Export
source-git-commit: ae3bb3463df13c30ce34739bb6e476d3f7422671
workflow-type: tm+mt
source-wordcount: '493'
ht-degree: 0%

---

# 数据传输

使用导入和导出工具在一次操作中管理多个记录。 您可以导入新项目以及更新、替换和删除现有产品集。

例如，您可以向库存中添加新产品、更新产品数据和高级价格数据，以及用新产品替换一组现有产品。 导入和导出工具有助于更高效地管理大型产品目录，因为您可以导出数据、在电子表格中编辑该数据并将其导入回您的商店，而不是在管理员中执行多项操作。

除了导入和导出工具之外，Adobe Commerce还包含以下流程 [SaaS数据导出](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/saas-data-export/overview) 可将产品数据从Commerce服务器导出到SaaS服务。 SaaS数据导出已与Commerce SaaS服务集成，包括 [产品Recommendations](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/overview.html)， [实时搜索](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/overview)， [目录服务](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/catalog-service/guide-overview)、和 [SaaS价格索引](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/price-indexer/price-indexing).

## 数据验证

所有数据都必须通过验证，以确保这些值的质量、准确性和完整性，然后才能将其导入存储中。 单击后即开始验证 **[!UICONTROL Check Data]**. 在此过程中，会针对以下内容验证导入文件中的所有图元：

- **属性**  — 验证列标题名称，确保它们与系统数据库中的相应属性匹配。 检查每个属性的值以确保它满足数据类型（decimal、integer、varchar、text和datetime）的要求。
- **复杂数据**  — 验证来自定义集的值（如下拉列表或多选输入类型），以确保定义集中的值存在。
- **服务数据**  — 验证服务数据列中的值，以确保属性或复杂数据值与系统数据库中已定义的值一致。
- **必需值**  — 对于新实体，将检查文件中是否存在所需的属性值。 对于现有实体，无需重新检查所需属性值的存在。
- **分隔符**  — 虽然在电子表格中查看分隔符时不可见，但CSV文件中的数据值以逗号分隔，并且文本值使用双引号括起来。 在验证过程中，将验证分隔符的格式设置以及包含字符串的每组引号。

验证结果显示在“验证结果”部分，其中包括以下信息：

- 已检查的实体数
- 无效行数
- 找到的错误数

如果数据有效，则 _导入成功_ 出现消息。

![系统消息 — 文件有效](./assets/data-import-validation-message.png){width="500" zoomable="yes"}

如果验证失败，请阅读每个错误的描述，并在CSV文件中更正问题。 例如，如果某行包含无效的SKU，则导入过程将停止，并且该行和所有后续行都不会导入。 在正确解决问题后，再次导入数据。 如果遇到许多错误，可能需要多次尝试才能通过验证。

### 数据验证报文

#### 验证

- `Product with specified SKU not found in rows: 1`
- `URL key for specified store already exists`
- `'7z' file extension is not supported`
- `TXT file extension is not supported`

#### 错误数

- `Wrong field type. Type in the imported file %decimal%, expected type is %text%.`
- `Value is not allowed. Attribute value does not exist in the system.`
- `Field %column name% is required.Wrong value separator is used.`
- `Wrong encoding used. Supported character encoding is UTF-8 and Windows-1252.`
- `Imported file does not contain SKU field.`
- `SKU does not exist in the system.`
- `Column name %column name% is invalid. Should start with a letter. Alphanumeric.`
- `Imported file does not contain a header.`
- `%website name% website does not exist in the system.`
- `%storeview name% storeview does not exist in the system.`
- `Imported attribute %attribute name% does not exist in the system.`
- `Imported resource (image) could not be downloaded from external resource due to timeout or access permissions.`
- `Imported resource (image) does not exist in the local media storage.`
- `Product creation error displayed to the user equal to the one seen during manual product save.`
- `Advanced Price creation error displayed to the user equal to the one seen during the manual product save.`
- `Customer creation error displayed to the user equal to the one seen during the manual customer save.`

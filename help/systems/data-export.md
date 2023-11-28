---
title: 导出数据
description: 了解数据导出筛选器和属性，以及如何从存储导出数据。
exl-id: 80e7a2fc-beaa-416e-a00f-a3cad5055975
feature: Products, Customers, Data Import/Export
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '840'
ht-degree: 0%

---

# 导出数据

熟悉数据库结构的最佳方法是导出数据并在电子表格中将其打开。 熟悉此过程后，您就可以将它用作管理大量信息的一种有效方法。

特殊字符（如等号、大于和小于符号、单引号和双引号、反斜杠、管道和&amp;符号）可能会导致数据传输过程中出现问题。 要确保此类特殊字符被正确解释，可以将它们标记为 _转义序列_. 例如，如果数据包含文本字符串，例如 `code="str"`， `code="str2"`，用双引号将文本括起来可确保原始双引号被视为数据的一部分： `"code="str""`. 当系统遇到双引号集时，它知道外双引号集将实际数据括起来。

数据导出是一项异步操作，将在后台执行，以便您可以继续在Admin中工作而不等待操作完成。 任务完成后，系统将显示一条消息。

## 导出标准

导出筛选器用于根据属性值指定您希望在导出文件中的数据。 此外，您还可以指定要在导出中包括或排除的属性数据。

![数据导出条件](./assets/data-export-entity-attributes-exclude.png){width="600" zoomable="yes"}

### 导出筛选器

您可以使用过滤器来确定导出文件中包含哪些SKU。 例如，如果在“制造国家/地区”字段中输入值，则导出的CSV文件将仅包含在该国家/地区制造的产品。

筛选器的类型对应于数据类型。 对于日期字段，您可以从“日历”中选择日期 ![日历图标](../assets/icon-calendar.png). 请参阅 [属性输入类型](../catalog/attributes-input-types.md) 以了解更多信息。

日期的格式由 [区域设置](../getting-started/store-details.md#locale-options).

要仅包含具有特定值（如SKU）的记录，请在“筛选器”字段中输入该值。 某些字段（如“价格”、“重量”和“将产品设置为新”）具有自/至值范围。

### 排除属性

第一列中的复选框用于从导出文件中排除属性。 如果排除属性，则导出数据中包含关联的列，但为空。

| 排除 | 筛选 | 结果 |
|--- |--- |--- |
| ![已清除复选框](../assets/checkbox-clear.png) | 否 | 导出的文件包含所有现有记录的每个属性。 |
| ![已清除复选框](../assets/checkbox-clear.png) | 是 | 导出文件包含每个属性，其中仅包含过滤器允许的记录。 |
| ![已选中复选框](../assets/checkbox-selected.png) | 否 | 导出文件中不包含排除属性的列，但包含所有现有记录。 |
| ![已选中复选框](../assets/checkbox-selected.png) | 是 | 导出文件中不包含排除属性的列，仅包含过滤器允许的记录。 |

{style="table-layout:auto"}

## 导出数据

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Export]**.

1. 在 _导出设置_ 部分，设置 **[!UICONTROL Entity Type]** 更改为以下任一项：

   - `Advanced Pricing`
   - `Products`
   - `Customer Finances`
   - `Customers Main File`
   - `Customer Addresses`
   - `Stock Sources`

   ![数据导出设置](./assets/data-export-settings.png){width="600" zoomable="yes"}

1. 接受默认值 **[!UICONTROL Export File Format]** /CSV.

1. 如果要将数据中可能存在的任何特殊字符作为 _转义序列_，选择 **[!UICONTROL Fields Enclosure]** 复选框。

1. 如果需要，可更改实体属性的显示。

   默认情况下，“实体属性”部分按字母顺序列出所有可用的属性。 您可以使用标准 [列表控件](../getting-started/admin-grid-controls.md) 搜索特定属性并对列表进行排序。 “搜索和重置筛选器”控制列表的显示，但不会影响导出文件中要包含的属性的选择。

   ![数据导出过滤的实体属性](./assets/data-export-filter-entity-attributes.png){width="600" zoomable="yes"}

1. 要根据属性值筛选导出的数据，请执行以下操作：

   - 要仅导出具有特定属性值的记录，请在 **[!UICONTROL Filter]** 列。 以下示例仅导出特定SKU。

   - 要从导出中省略属性，请选择 **[!UICONTROL Exclude]** 复选框。 例如，要仅导出 `sku` 和 `image` 列中，选中其他所有属性的复选框。 列会显示在导出文件中，但不显示任何值。

1. 向下滚动并单击 **[!UICONTROL Continue]** 在页面的右下角。

   任务完成后，将通过消息队列处理文件（确保cron作业正在运行）。 导出的文件保存在 `var/export/ folder`. 有关消息队列的详细信息，请参见 [管理消息队列](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html) 在 _配置指南_.

   您可以将导出的CSV文件保存或打开为电子表格，然后编辑数据并将其导入回您的商店。

   >[!NOTE]
   >
   >默认情况下，所有导出的文件都位于 `<Magento-root-directory>/var/export` 文件夹。 如果启用了远程存储模块，则所有导出的文件都位于 `<remote-storage-root-directory>/import_export/export` 文件夹。

## 资源疑难解答

有关排查数据导出问题的帮助，请参阅以下Commerce支持知识库文章：

- [导出的产品.csv文件不显示](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/exported-products-.csv-file-does-not-appear.html)
- [产品导出文件未显示在管理员中](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-9/mdva-31168-magento-patch-product-export-file-does-not-show-in-admin.html)
- [以CSV格式导出订单时出现问题](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-8/mdva-31242-magento-patch-issue-in-exporting-orders-in-csv-format.html)

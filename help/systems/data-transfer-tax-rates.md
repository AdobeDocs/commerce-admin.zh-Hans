---
title: 更新税率数据
description: 了解如何使用导出和导入操作来更新商店的税率。
exl-id: a3ef718d-b296-41d7-a1b8-ae8274da71b6
feature: Taxes, Data Import/Export
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '615'
ht-degree: 0%

---

# 更新税率数据

如果您在多个州经营业务并且发运大量产品，那么手动输入税率可能非常耗时。 通过邮政编码下载税率并将其导入Commerce会更快、更有效。 以下示例显示如何导入从可信来源下载的一组特定于州的税率。 阿瓦拉提供 [税率表](https://www.avalara.com/taxrates/en/download-tax-tables.html)，您可为美国的每个邮政编码免费下载。

>[!NOTE]
>
>如果您希望实现销售自动化并使用税务合规性和报告功能，则可以在 [商业合作伙伴](https://solutionpartners.adobe.com/s/directory/?solution=commerce) 站点。

## 步骤1：导出商业税率数据

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Import/Export Tax Rates]**.

1. 单击 **[!UICONTROL Export Tax Rates]**.

1. 在Web浏览器的下载位置中查找文件。

1. 在电子表格中保存并打开文件。

   此示例使用 [!DNL OpenOffice Calc].

   导出的商业税率数据包括以下列：
   - 代码
   - 国家/地区
   - 状态
   - 邮政编码
   - 费率
   - 范围从
   - 范围到
   - 每个商店视图的列

   ![导出的数据 — 税率](./assets/data-exported-tax-rates.png){width="500" zoomable="yes"}

1. 在电子表格的第二个实例中打开新的税率数据，以便您可以并排查看它们。

1. 在新税率数据中，请注意在导入数据之前您可能需要在商店中设置的任何其他税率数据。

   例如，加利福尼亚的税率数据还包括：

   - `TaxRegionName`
   - `CombinedRate`
   - `StateRate`
   - `CountyRate`
   - `CityRate`
   - `SpecialRate`

   如果您需要导入其他 [税区和税率](../stores-purchase/tax-zones-rates.md)，您必须首先从存储管理员中定义这些区段并更新 [税则](../stores-purchase/tax-rules.md) 根据需要。 然后，导出数据并在文本编辑器中打开文件，以便将其用于参考。 但是，为了简化此示例，我们只导入标准税率列。

## 步骤2：准备导入数据

您同时打开了两个电子表格。 一个包含Commerce导出文件结构，另一个包含要导入的新税率数据。

1. 要在电子表格中使用新的税率数据创建一个位置，请在最右侧插入所需数量的空白列，以从Commerce导出文件中添加数据。 使用剪切并粘贴来添加数据，然后重新排列各列，使它们与Commerce导出数据文件的顺序匹配。

1. 重命名列标题以匹配Commerce导出数据。

1. 删除任何没有数据的列。

   否则，导入文件的结构应与原始Commerce导出数据匹配。

1. 在保存文件之前，向下滚动并确保税率列仅包含数字数据。

   在“税率”列中找到的任何文本均阻止导入数据。

1. 将准备的数据另存为.CSV文件。

   出现提示时，确认使用逗号作为字段分隔符，使用双引号作为文本分隔符。 然后单击 **[!UICONTROL OK]**.

## 步骤3：导入税率

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Import/Export Tax Rates]**.

1. 单击 **[!UICONTROL Choose File]** 并选择您准备导入的CSV税率文件。

1. 单击 **[!UICONTROL Import Tax Rates]**.

   导入数据可能需要几分钟的时间。 当该过程完成时， `The tax rate has been imported` 出现消息。 如果收到错误消息，请更正数据中的问题并重试。

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Zones and Rates]**.

   导入的费率会显示在列表中。

1. 使用页控件查看新税率。

   ![数据导入税率](../stores-purchase/assets/tax-zones-rates.png){width="600" zoomable="yes"}

1. 在您的商店中与来自不同邮政编码的客户运行一些测试交易记录，以确保新税率正确运行。

---
title: 税则
description: 了解如何使用产品分类、客户分类和税率定义税则。
exl-id: 38d65998-7769-49ce-9814-e65df9d77bba
feature: Taxes, Currency
source-git-commit: 7288a4f47940e07c4d083826532308228d271c5e
workflow-type: tm+mt
source-wordcount: '438'
ht-degree: 0%

---

# 税则

税则包含产品分类、客户分类和税率的组合。 每个客户都被分配给一个客户分类，每个产品都分配有一个产品分类。 Commerce分析每位客户的购物车，并根据客户、产品类别以及区域计算相应的税额。 区域基于客户的送货地址、帐单地址或送货来源。

>[!NOTE]
>
>当必须定义多个税率时，可以通过导入这些税率来简化该过程。

![税则](./assets/tax-rules.png){width="600" zoomable="yes"}

## 步骤1：完成税则信息

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Rules]**。

1. 单击右上角的&#x200B;**[!UICONTROL Add New Tax Rule]**。

1. 在&#x200B;_税则信息_&#x200B;下，为新规则输入&#x200B;**[!UICONTROL Name]**。

   ![税则信息](./assets/tax-rule-information.png){width="600" zoomable="yes"}

1. 选择应用于规则的&#x200B;**[!UICONTROL Tax Rate]**。

   要编辑现有税率，请执行以下操作：

   - 将鼠标悬停在税率上，然后单击&#x200B;_编辑_ ![铅笔图标](../assets/icon-edit-pencil.png)图标。

   - 根据需要更新表单，然后单击&#x200B;**[!UICONTROL Save]**。

1. 要输入税率，请使用以下方法之一：

### 方法1：人工输入税率

1. 单击&#x200B;**[!UICONTROL Add New Tax Rate]**。

1. 根据需要填写表单（请参阅[税区和税率](tax-zones-rates.md)）。

1. 完成后，单击&#x200B;**[!UICONTROL Save]**。

   ![新税率](./assets/tax-rate-create-new.png){width="600" zoomable="yes"}

### 方法2：进口税率

1. 向下滚动到页面底部的部分。

1. 要导入税率，请执行以下操作：

   - 单击&#x200B;**[!UICONTROL Choose File]**&#x200B;并导航到包含要导入的税率的CSV文件。

   - 单击&#x200B;**[!UICONTROL Import Tax Rates]**。

1. 若要导出税率，请单击&#x200B;**[!UICONTROL Export Tax Rates]**（请参阅[导入/导出税率](../systems/data-transfer-tax-rates.md)）。

![进口/出口税率](./assets/tax-rule-new-import-export.png){width="600" zoomable="yes"}

## 第2步：完成其他设置

1. 要打开此分区，请单击&#x200B;**[!UICONTROL Additional Settings]**。

   税则的![其他设置](./assets/tax-class-additional-settings.png){width="600" zoomable="yes"}

1. 选择应用规则的&#x200B;**[!UICONTROL Customer Tax Class]**。

   - 要编辑客户税类，请单击&#x200B;_编辑_ ![铅笔图标](../assets/icon-edit-pencil.png)图标，根据需要更新表单，然后单击&#x200B;**[!UICONTROL Save]**。

   - 要创建税分类，请单击&#x200B;**[!UICONTROL Add New Tax Class]**，根据需要完成表单，然后单击&#x200B;**[!UICONTROL Save]**。

1. 选择应用规则的&#x200B;**[!UICONTROL Product Tax Class]**。

   - 要编辑产品税类，请单击&#x200B;_编辑_ ![铅笔图标](../assets/icon-edit-pencil.png)图标，根据需要更新表单，然后单击&#x200B;**[!UICONTROL Save]**。

   - 要创建税分类，请单击&#x200B;**[!UICONTROL Add New Tax Class]**，根据需要完成表单，然后单击&#x200B;**[!UICONTROL Save]**。

1. 当多个税适用时，输入一个数字以指示此税对&#x200B;**[!UICONTROL Priority]**&#x200B;的优先级。

   如果两个具有相同优先级的税则适用，则增加税额。 如果两个税具有不同的优先权设置，则这些税是复合的。

1. 如果您希望税额基于订单小计，请选中&#x200B;**[!UICONTROL Calculate off Subtotal Only]**&#x200B;复选框。

1. 对于&#x200B;**[!UICONTROL Sort Order]**，输入一个数字以指示此税则与其他规则一起列出的顺序。

1. 完成后，单击&#x200B;**[!UICONTROL Save Rule]**。

## 币种和税则演示

通过观看以下视频，了解如何管理货币和税则：

>[!VIDEO](https://video.tv.adobe.com/v/3410210/?quality=12&learn=on&captions=chi_hans)

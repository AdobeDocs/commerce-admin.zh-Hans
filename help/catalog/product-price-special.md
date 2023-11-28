---
title: 特别价格
description: 了解如何在指定的时间段内提供特殊定价。
exl-id: 4a1e2045-f0a8-4bae-a5a3-8ce8b258b217
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '851'
ht-degree: 0%

---

# 特别价格

可以在指定的时间段内提供特别价格。 在指定的时间段内，将显示特殊价格而不是常规价格，随后将显示表示法，该表示法显示常规价格。

![产品页面上的特殊价格](./assets/storefront-price-special.png){width="700" zoomable="yes"}

## 对单个产品应用特殊价格

您可以轻松地为目录中的单个产品设置特殊价格。

### 使用计划更新

{{ee-feature}}

Adobe Commerce包含对的支持 [计划的更新](../content-design/content-staging-scheduled-update.md). 使用这些促销工具在特定时间段内对特定产品应用特殊价格。

1. 在编辑模式下打开产品。

1. 单击 **[!UICONTROL Scheduled Update]**.

   ![为产品添加计划更新](./assets/product-schedule-new-update.png){width="600" zoomable="yes"}

1. 对象 **更新名称**，输入特殊价格促销的名称。

1. 输入摘要 **[!UICONTROL Description]**.

1. 使用 _日历_ ( ![日历图标](../assets/icon-calendar.png) )图标以选择 **[!UICONTROL Start Date]** 和 **[!UICONTROL End Date]** 进行特价促销。

   您可以使用 **[!UICONTROL Hour]** 和 **[!UICONTROL Minute]** 滑块以选择开始时间和结束时间。 单击 **[!UICONTROL Close]** 设置开始和结束日期时。

   ![另存为新更新](./assets/product-price-special-scheduled-update.png){width="600" zoomable="yes"}

1. 向下滚动到 _价格_ 字段，请单击 **[!UICONTROL Advanced Pricing]**，并输入 **[!UICONTROL Special Price]** 将根据计划的更新应用。

   ![特殊定价设置](./assets/product-price-special.png){width="600" zoomable="yes"}

1. 完成后，单击 **[!UICONTROL Done]** 然后 **[!DNL Save]**.

   在店面，特价应同时出现在目录列表和产品页面上。

   此 _[!UICONTROL Scheduled Change]_显示在页面顶部。

   ![计划的更改](./assets/product-price-special-scheduled-change.png){width="600" zoomable="yes"}

### 使用简单的开始和结束日期

{{ce-feature}}

Magento Open Source包括高级定价选项中的简单起始日期和终止日期选项。

1. 在编辑模式下打开产品。

1. 向下滚动到 _[!UICONTROL Price]_字段，请单击&#x200B;**[!UICONTROL Advanced Pricing]**，并输入&#x200B;**[!UICONTROL Special Price]**数量。

1. 使用 _日历_ ( ![日历图标](../assets/icon-calendar.png) )图标以选择 **[!UICONTROL Start Date]** 和 **[!UICONTROL End Date]** 进行特价促销。

   特价从开始日期的午夜开始(00:01)立即生效，一直持续到结束日期前一天的午夜之前(23:59)。

   ![计划的更改](./assets/product-special-price-from-ce.png){width="600" zoomable="yes"}

1. 完成后，单击 **[!UICONTROL Done]** 然后 **[!UICONTROL Save]**.

   在店面，特价应同时出现在目录列表和产品页面上。

## 对多个产品应用特殊价格

您还可以为多个产品指定特殊价格，例如一个产品的多个变体 [可配置产品](product-create-configurable.md).

### 为所选产品设置特殊价格

{{ee-feature}}

以下示例显示如何在Adobe Commerce中为可配置产品的多个产品变体分配相同的特殊价格。

1. 在 _[!UICONTROL Products]_页面，单击&#x200B;**[!UICONTROL Filters]**并输入&#x200B;**[!UICONTROL Name]**可配置产品的。

1. 设置 **[!UICONTROL Type]** 到 `Configurable Product` 并单击 **[!UICONTROL Apply Filters]**.

1. 如果要对所有产品指定相同的特殊价格，请将第一列标题中的控件设置为 `Select All`.

   作为替代方法，您可以选中要包含的每个产品的复选框。

1. 设置 **[!UICONTROL Actions]** 控制对象 `Update attributes`.

1. 向下滚动到 _[!UICONTROL Special Price]_字段并选择&#x200B;**[!UICONTROL Change]**复选框_[!UICONTROL Special Price]_ 字段，然后输入要提供的特殊价格。

   ![特殊价格字段](./assets/product-price-special-commerce.png){width="600" zoomable="yes"}

1. 完成后，单击 **[!UICONTROL Save]**.

商店中可用的特殊价格会显示在目录清单和产品页面中。 对于可配置产品，在选择相关选项时，产品页面上也会显示常规价格。

### 为所选产品设置特殊价格和日期范围

{{ce-feature}}

以下示例显示了如何在Magento Open Source中为可配置产品的多个产品变体分配相同的特殊价格。

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. 单击 **[!UICONTROL Filters]**.

1. 输入 **[!UICONTROL Name]** 可配置产品的。

1. 设置 **[!UICONTROL Type]** 到 `Simple Product`.

   ![过滤器](./assets/product-price-special-filter.png){width="600" zoomable="yes"}

1. 单击 **[!UICONTROL Apply Filters]**.

   该网格列出了作为可配置产品的变体关联的所有简单产品。

1. 如果要对所有产品指定相同的特殊价格，请将第一列标题中的控件设置为 `Select All`.

   作为替代方法，您可以选中要包含的每个产品的复选框。

1. 设置 **[!UICONTROL Actions]** 控制对象 `Update attributes`.

   ![更新属性](./assets/product-price-special-action-update-attributes-ce.png){width="600" zoomable="yes"}

1. 向下滚动到_[!UICONTROL Special Price]**字段并执行以下操作：

   - 选择 **[!UICONTROL Change]** _下的复选框[!UICONTROL Special Price]**字段，然后输入要提供的特殊价格。

   - 选择 **[!UICONTROL Change]** 复选框 _特殊价格起始日期_ 字段中，单击 _日历_ ( ![日历图标](../assets/icon-calendar.png) )，然后选择特殊价格促销的第一个日期。

     特价从开始日期的午夜开始(00:01)立即生效，一直持续到结束日期前一天的午夜之前(23:59)。

   - 选择 **[!UICONTROL Change]** 复选框 _至今日的特殊价格_ 字段中，单击 _日历_ ( ![日历图标](../assets/icon-calendar.png) )，然后选择特殊价格促销的最后日期。

   ![特殊价格字段](./assets/product-price-special-action-update-attributes-fields-ce.png){width="600" zoomable="yes"}

1. 完成后，单击 **[!UICONTROL Save]**.

   一条消息指示有多少条记录使用特殊价格进行了更新。

   特殊价格将在指定的日期出现在商店中，并显示在目录清单和产品页面上。 对于可配置产品，在选择相关选项时，产品页面上也会显示常规价格。

   ![可配置产品的特殊价格](./assets/storefront-special-price-configurable-product-detail.png){width="600" zoomable="yes"}

## 测试

如果特殊价格未在目录列表和产品页面的店面中正确显示，请清除浏览器缓存：

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL System]** > **[!UICONTROL Cache Management]**.

1. 单击 **[!UICONTROL Flush Magento Cache]**.

>[!NOTE]
>
>此 **_最终_** 产品价格的计算方式为 **_最小值_** 相关价格，使用下列公式： <br/>`Final Price=Min(Regular(Base) Price, Group(Tier) Price, Special Price, Catalog Price Rule) + Sum(Min Price per each required custom option)`

>[!NOTE]
>
>**_固定价格_** 产品可自定义选项包括 _非_ 受组价格、层价格、特殊价格或目录价格规则影响。

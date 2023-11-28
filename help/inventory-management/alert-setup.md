---
title: 产品警报
description: 了解产品警报以及如何使用它们通知客户产品的库存状态和价格变化。
exl-id: c9f736c5-7bba-4e3e-804d-5b0fe52c8f9b
feature: Inventory, Configuration
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '631'
ht-degree: 0%

---

# 产品警报

客户可以通过电子邮件订阅两种类型的警报：价格更改警报和库存警报。 对于每种类型的警报，您可以确定客户是否能够订阅，选择使用的电子邮件模板，并识别电子邮件的发件人。

![注册产品警报](assets/product-alert-setting.png){width="600" zoomable="yes"}

## 价格更改警报

启用价格更改警报后， _价格下降时通知我_ 链接会显示在每个产品页面上。 客户可以单击该链接以订阅与产品相关的警报。 系统会提示访客在您的商店中开立帐户。 每当价格发生变化或产品推出特殊产品时，订阅该警报的每个人都会收到电子邮件警报。

## 库存警报

库存警报会创建一个名为的链接 _此产品有库存时通知我_ 每件缺货的产品都有。 客户可以单击链接以订阅警报。 当产品重新上架时，客户会收到一封电子邮件通知，告知该产品可供使用。 具有警报的产品具有 _产品警报_ 选项卡，其中列出了订阅了警报的客户。

![产品和价格警报订阅的列表](assets/inventory-product-alerts.png){width="600" zoomable="yes"}

## 设置产品警报

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中，展开 **[!UICONTROL Catalog]** 并选择 **[!UICONTROL Catalog]** 下方。

1. 单击以展开 _[!UICONTROL Product Alerts]_部分并执行以下操作：

   ![产品警报](assets/config-catalog-product-alerts.png){width="600" zoomable="yes"}

   - 要向客户提供价格更改警报，请设置 **[!UICONTROL Allow Alert When Product Price Changes]** 到 `Yes`.

   - 设置 **[!UICONTROL Price Alert Email Template]** 要用于价格预警通知的模板。

   - 要在缺货产品再次可用时提供警报，请设置 **[!UICONTROL Allow Alert When Product Comes Back in Stock]** 到 `Yes`.

     >[!NOTE]
     >
     >此 _此产品有库存时通知我_ 消息仅在以下情况下显示 **[!UICONTROL Display Out of Stock Products]** 设置为 `Yes` (在配置中的 [!UICONTROL Catalog] > [!UICONTROL Inventory])。

   - 设置 **[!UICONTROL Stock Alert Email Template]** 更改为要用于product stock警报的模板。

   - 设置 **[!UICONTROL Alert Email Sender]** 到 [商店联系人](../getting-started/store-details.md#store-email-addresses){target="_blank"} that you want to appear as the sender of the email alert. Learn more about [store email addresses](../configuration-reference/general/store-email-addresses.md){target="_blank"} （在核心用户指南中）。

1. 完成后，单击 **[!UICONTROL Save Config]**.

## 配置产品警报电子邮件模板

接下来，配置、添加或修改价格警报的电子邮件模板。 创建其他模板后，您可能需要编辑价格警报配置。

有关使用电子邮件的详细信息，请参阅 [消息模板](../systems/email-template-custom.md#message-templates) 在 _管理系统指南_.

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Email Templates]**.

1. 单击 **[!UICONTROL Add New Template]**.

1. 下 _加载默认模板_，选择 **[!UICONTROL Template]** 要进行自定义的页面。

   您可以选择主题中包含的警报模板。 或者，您可以选择 `Price Alert` 或 `Stock Alert` 模板位于 _[!UICONTROL Magento_PriceAlert]_.

1. 单击 **[!UICONTROL Load Template]**.

1. 输入 **[!UICONTROL Template Name]**.

   您可以在以下位置选择此名称 _价格警报_ 配置。

1. 通读现有内容，并根据需要进行更改，以实现以下目标：

   | 字段 | 描述 |
   | ----- | ----- |
   | [!UICONTROL Template Subject] | 此文本显示在电子邮件的主题行中。 |
   | [!UICONTROL Template Content] | 此文本显示在已发送电子邮件的完整内容中。 |

1. 添加生成的信息 [!DNL Commerce] 数据，使用 **[!UICONTROL Insert Variable]** 选项以使用可用变量列表。

1. 单击 **[!UICONTROL Save Template]**.

## 产品警报运行设置

这些设置允许您选择频率 [!DNL Commerce] 检查需要发送警报的更改。 您还可以为发送警报失败时发送的电子邮件选择收件人、发件人和模板。

![产品警报运行设置](assets/config-catalog-product-alerts-run-settings.png){width="600" zoomable="yes"}

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中，展开 **[!UICONTROL Catalog]** 并选择 **[!UICONTROL Catalog]** 下方。

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Product Alerts Run Settings]** 部分。

1. 要确定发送产品警报的频率，请设置 **[!UICONTROL Frequency]** 更改为以下任一项：

   - `Daily`
   - `Weekly`
   - `Monthly`

1. 要确定一天中发送产品警报的时间，请设置 **[!UICONTROL Start Time]** 到小时、分钟和秒。

   >[!NOTE]
   >
   >产品警报由“product_alert”使用者发送。

1. 对象 **[!UICONTROL Error Email Recipient]**，输入出错时联系人的电子邮件。

1. 对于 **[!UICONTROL Error Email Sender]**，选择显示为错误通知发送者的存储标识。

1. 设置 **[!UICONTROL Error Email Template]** 用于错误通知的事务性电子邮件模板。

1. 完成后，单击 **[!UICONTROL Save Config]**.

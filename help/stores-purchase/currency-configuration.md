---
title: 货币配置
description: 了解如何设置基本货币的范围，以及如何指定您接受的货币以及要用于价格显示的货币。
exl-id: ba78095f-36eb-4e38-a6e8-72d85e0cf980
feature: Currency, Configuration, Data Import/Export
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '817'
ht-degree: 0%

---

# 货币配置

在设置单个货币汇率之前，必须首先设置 [基础货币](../configuration-reference/general/currency-setup.md). 默认情况下，它设置为全局，这将对整个应用基础货币设置 [存储层级](../getting-started/websites-stores-views.md). 如果您安装的是多站点Adobe Commerce或Magento Open Source，则可以通过将范围设置为网站级别来管理多个基础货币。

您还可以指定接受的货币以及要用于显示的货币 [价格](../catalog/catalog-price-scope.md) 在你的店里。 在下图中，基础货币的范围在网站级别设置，因此每个网站可以具有不同的基础货币。

![货币范围图](./assets/scope-currency-config.svg){width="600" zoomable="yes"}

## 步骤1：选择接受的币种

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左上角，设置 **[!UICONTROL Scope]** 到应用配置的商店视图。

1. 在左侧面板中的 _常规_，选择 **[!UICONTROL Currency Setup]**.

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Currency Options]** 并设置以下选项：

   - **[!UICONTROL Base Currency]**  — 设置为用于在线交易的主要货币。

   - **[!UICONTROL Default Display Currency]**  — 设置为您在商店视图中显示定价时使用的货币。

   - **[!UICONTROL Allowed Currencies]**  — 选择您在商店视图中接受作为付款的所有货币。 请确保同时选择您的主要货币。

     对于多种货币，按住Ctrl键(PC)或Command键(Mac)，然后单击每个选项。

   ![常规配置 — 货币选项](../configuration-reference/general/assets/currency-setup-currency-options.png){width="600" zoomable="yes"}

   有关每个配置设置的详细说明，请参阅 [货币选项](../configuration-reference/general/currency-setup.md) 在 _配置参考指南_.

1. 提示刷新缓存时，单击 _关闭_ ( ![关闭框](../assets/icon-close-x.png) )。

   您可以 [刷新缓存](../systems/cache-management.md) 稍后。

1. 定义基础货币的范围：

   - 在左侧面板中，展开 **[!UICONTROL Catalog]** 并选择 **[!UICONTROL Catalog]** 下方。

   - 向下滚动并展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Price]** 部分。 (仅当范围设置为时，才会显示此部分 **[!UICONTROL Store View:]** _默认配置_.)

   - 设置 **[!UICONTROL Catalog Price Scope]** 更改为 `Global` 或 `Website`.

   ![目录配置 — 价格选项](../configuration-reference/catalog/assets/catalog-price.png){width="600" zoomable="yes"}

## 步骤2：配置导入连接

1. 滚动到页面顶部。

1. 在左侧面板中，展开 **[!UICONTROL General]** 并选择 **[!UICONTROL Currency Setup]**.

1. 配置您的货币服务连接：

   有三种服务选项： _[!UICONTROL Fixer.io (legacy)]_，_[!UICONTROL Fixer Api (APILayer)]_、和 _[!UICONTROL Currency Converter API]_

   >[!IMPORTANT]
   >
   >从2.4.6版本开始， [[!DNL Fixer.io]](https://fixer.io/) 服务已弃用，并替换为 [[!DNL Fixer API] （阿皮耶尔）](https://apilayer.com/marketplace/fixer-api) 服务。 强烈建议您使用APILayer帐户而不是已弃用的帐户 [!DNL Fixer.io] 帐户。

   - _要连接到 [fixer.io服务](https://fixer.io/)：_

      - 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Fixer.io]** 部分。

      - 输入您的fixer.io **[!UICONTROL API key]**.

      - 对象 **[!UICONTROL Connection Timeout in Seconds]**，输入在连接超时之前允许处于非活动状态的秒数。

     ![常规配置 — 货币设置 — Fixer.io选项](../configuration-reference/general/assets/currency-setup-fixer.png){width="600" zoomable="yes"}

   - _要连接到 [[!DNL Fixer Api (APILayer)] 服务](https://apilayer.com/)：_

      - 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Fixer Api (APILayer)]** 部分。

      - 输入您的 [!DNL APILayer] **[!UICONTROL API key]**.

      - 对象 **[!UICONTROL Connection Timeout in Seconds]**，输入在连接超时之前允许处于非活动状态的秒数。

     ![常规配置 — 货币设置 — 修复器API (APILayer)选项](../configuration-reference/general/assets/currency-setup-fixer-api.png){width="600" zoomable="yes"}

   - _要连接到 [[!DNL Currency Convertor API] 服务](https://free.currencyconverterapi.com/)：_

      - 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Currency Convertor API]** 部分。

      - 输入您的货币换算器 **[!UICONTROL API key]**.

      - 对象 **[!UICONTROL Connection Timeout in Seconds]**，输入在连接超时之前允许处于非活动状态的秒数。

     ![常规配置 — 货币设置 — 货币转换器API选项](../configuration-reference/general/assets/currency-setup-converter.png){width="600" zoomable="yes"}

## 步骤3：配置计划的导入设置

1. 继续货币设置，展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Scheduled Import Settings]** 部分。

   ![常规配置 — 货币计划导入设置](../configuration-reference/general/assets/currency-setup-scheduled-import-settings.png){width="600" zoomable="yes"}

1. 要自动更新汇率，请设置 **[!UICONTROL Enabled]** 到 `Yes`.

1. 设置更新选项：

   - **[!UICONTROL Service]**  — 设置为费率提供器。 默认值为 `Fixer.io (legacy)`.

   - **[!UICONTROL Start Time]**  — 设置为根据计划更新费率的小时、分钟和秒。

   - **[!UICONTROL Frequency]**  — 要确定更新费率的频率，请设置为以下项之一：

      - `Daily`
      - `Weekly`
      - `Monthly`

   - **[!UICONTROL Error Email Recipient]**  — 输入导入过程中发生错误时接收电子邮件通知的人员的电子邮件地址。

     要输入多个电子邮件地址，请使用逗号分隔每个电子邮件地址。

   - **[!UICONTROL Error Email Sender]**  — 设置为 [商店联系人](../getting-started/store-details.md#store-email-addresses) 显示为错误通知的发件人。

   - **[!UICONTROL Error Email Template]**  — 设置为用于错误通知的电子邮件模板。

1. 完成后，单击 **[!UICONTROL Save Config]**.

1. 提示更新缓存时，单击 **[!UICONTROL Cache Management]** 链接并刷新无效缓存。

   ![系统消息 — 刷新无效的缓存](./assets/msg-cache-management.png){width="600" zoomable="yes"}

## 步骤4：更新汇率

在汇率生效之前，必须使用当前值更新汇率。 [更新费率](currency-update.md) 手动或自动导入费率。

## 步骤5：自定义货币符号（可选）

通过管理货币符号，您可以自定义与商店中接受作为付款的每种货币关联的符号。

![货币符号](./assets/stores-currency-symbols.png){width="600" zoomable="yes"}

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Currency]_>**[!UICONTROL Currency Symbols]**.

   为您的商店启用的每种货币都显示在 _[!UICONTROL Currency]_列表。

1. 根据需要更改列表中的设置：

   - 为要使用的每种货币输入自定义符号，或选择 **[!UICONTROL Use Standard]** 复选框。

   - 要覆盖缺省符号，请清除 _[!UICONTROL Use Standard]_复选框，然后输入要使用的符号。

   >[!NOTE]
   >
   >不能将货币符号的对齐方式从左更改为右。

1. 完成后，单击 **[!UICONTROL Save Currency Symbols]**.

1. 提示更新缓存时，单击 **[!UICONTROL Cache Management]** 链接并刷新任何无效的缓存。

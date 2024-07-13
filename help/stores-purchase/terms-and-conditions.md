---
title: 结账的条款和条件
description: 了解可为您的商店配置的条款和条件功能。
exl-id: 59ba6385-3cc6-43e8-b984-5c26516bba88
feature: Checkout, Compliance
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '322'
ht-degree: 0%

---

# 结账的条款和条件

当手动&#x200B;_条款和条件_&#x200B;功能启用时，客户必须在最终完成购买之前同意销售条款和条件。 销售条款和条件通常包括法律可能要求对B2C或B2B站点进行披露的信息，并概述了买方和卖方的权利。 “条款和条件”消息显示在付款信息之后，紧接&#x200B;_下订单_&#x200B;按钮之前。

![结账时的条款和条件](./assets/storefront-checkout-step2-terms-conditions.png){width="700" zoomable="yes"}

## 步骤1：启用结账条款和条件

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧面板中，展开&#x200B;**[!UICONTROL Sales]**&#x200B;并选择&#x200B;**[!UICONTROL Checkout]**。

1. 展开&#x200B;**[!UICONTROL Checkout Options]**&#x200B;部分的![扩展选择器](../assets/icon-display-expand.png)。

   ![签出选项](../configuration-reference/sales/assets/checkout-checkout-options.png){width="600" zoomable="yes"}

1. 验证&#x200B;**[!UICONTROL Enable Onepage Checkout]**&#x200B;是否设置为`Yes`。

1. 将&#x200B;**[!UICONTROL Enable Terms and Conditions]**&#x200B;设置为`Yes`。

1. 单击&#x200B;**[!UICONTROL Save Config]**。

## 第2步：添加您自己的条款和条件信息

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Terms and Conditions]**。

   ![条款和条件网格](./assets/terms-conditions.png){width="600" zoomable="yes"}

1. 单击右上角的&#x200B;**[!UICONTROL Add New Condition]**。

1. 输入&#x200B;**[!UICONTROL Condition Name]**&#x200B;供内部引用。

   ![新条件](./assets/terms-conditions-new.png){width="600" zoomable="yes"}

1. 将&#x200B;**[!UICONTROL Status]**&#x200B;设置为`Enabled`。

1. 将&#x200B;**[!UICONTROL Applied]**&#x200B;设置为以下项之一：

   - `Automatically` — 签出时自动接受条件。
   - `Manually` — 客户需要手动接受下订单的条件。

1. 将&#x200B;**[!UICONTROL Show Content as]**&#x200B;设置为以下项之一：

   - `Text` — 将条款和条件内容显示为未格式化的文本。
   - `HTML` — 将内容显示为HTML，可以设置其格式。

1. 选择要使用这些条款和条件的每个&#x200B;**[!UICONTROL Store View]**。

1. 向下滚动并完成要显示的信息：

   - 输入要用作条款和条件链接文本的&#x200B;**[!UICONTROL Checkbox Text]**。 例如，`I understand and accept the terms and conditions of the sale`。

   - 在&#x200B;**[!UICONTROL Content]**&#x200B;框中，输入销售条款和条件的全文。

1. （可选）输入&#x200B;**[!UICONTROL Content Height (css)]**&#x200B;像素，以确定签出期间显示条款和条件语句的文本框的高度。

   例如，若要使文本框在96 dpi显示屏上变高1英寸，请输入`96`。 如果内容超出框的高度，将显示滚动条。

1. 单击&#x200B;**[!UICONTROL Save Condition]**。

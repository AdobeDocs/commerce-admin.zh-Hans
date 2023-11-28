---
title: '[!DNL Google Content Experiments]'
description: 了解如何使用 [!DNL Google Content Experiments] 设置Commerce产品、类别或内容页面的A/B测试。
exl-id: ae03bc5a-de84-4dad-932e-e79e509feebe
feature: Marketing Tools, Integration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '440'
ht-degree: 0%

---

# [!DNL Google Content Experiments]

以下示例演示了如何使用Google Analytics内容实验设置产品、类别或内容页面的A/B测试。 我们建议您在按照相关说明操作时保持两个浏览器选项卡处于打开状态，因为您需要在Commerce管理员与您的 [!DNL Google Analytics] 帐户。

>[!NOTE]
>
>[!DNL Google Content Experiments] 已弃用，计划由替换 [Google优化](https://support.google.com/optimize/answer/7084762?hl=en).

## 步骤1. 启用内容试验(Commerce)

1. 登录到Commerce安装的管理员。

1. 按照说明启用 [Google Analytics](google-analytics.md) 通过Commerce配置中的内容实验。

   ![Sales配置 — Google API -Google Analytics](../configuration-reference/sales/assets/google-api-analytics-ee.png){width="600" zoomable="yes"}

## 步骤2. 设置变体(Commerce)

创建同一产品、类别或页面的多个变体。

- 每个变体必须具有唯一的 [URL键](../catalog/catalog-urls.md).
- 每个变体必须具有相同的 [商店视图](../getting-started/websites-stores-views.md#scope-settings) 已选定。

您可以为要测试的每个实体创建最多十个变体。 对于产品，使用 [保存并复制](../catalog/product-workspace.md) 以节省时间。

## 步骤3. 设置试验(Google)

>[!NOTE]
>
>您必须对Google帐户具有相应的权限才能创建试验。

1. 打开另一个浏览器选项卡，并登录到 [Google Analytics][2] 帐户。

   如有必要，请导航至 **[!UICONTROL Account]** 和 **[!UICONTROL Property]**.

1. 在左侧的侧栏中，选择 **[!UICONTROL Admin]** 并使用以下方法之一：

   **方法1：** 选择现有视图

   在的标题中 _[!UICONTROL View]_列中，单击向下箭头，然后选择要为试验提供数据的视图。

   **方法2：** 创建新的报表视图

   - 在的标题中 _视图_ 列，单击 **[!UICONTROL Create View]** 并执行以下操作：

      - 将试验位置标识为 `Website` 或 `Mobile app`.

      - 输入描述性 **[!UICONTROL Reporting View Name]**.

      - 指定 **[!UICONTROL Reporting Time Zone]**.

   - 完成后，单击 **[!UICONTROL Create View]** 然后单击“上一步”箭头返回上一页。

1. 在左侧面板中的 _[!UICONTROL Reports]_，选择&#x200B;**[!UICONTROL Behavior]**>**[!UICONTROL Experiments]**.

1. 单击 **[!UICONTROL Create experiment]** 并执行以下操作：

   - 指定要重定向的流量的百分比。

   - 指定 **[!UICONTROL Original Page URL]** 以及每个页面的URL **[!UICONTROL page variation]** 要测试的对象。

   - 完成其他选项。

1. 设置试验后，单击 **[!UICONTROL Manually Insert the Code]** 并复制代码段。

## 步骤4. 粘贴代码段(Commerce)

1. 返回到Commerce安装的管理员，并在编辑模式下打开产品、类别或页面的原始版本。

1. 展开 **[!UICONTROL View Optimization]** 产品、类别或页面的部分。

1. 将您从Google Analytics复制的代码段粘贴到 **[!UICONTROL Experiment Code]** 文本框。

   >[!NOTE]
   >
   >请勿将代码段粘贴到任何变体中。

   ![产品视图优化](../catalog/assets/product-view-optimization.png){width="600" zoomable="yes"}

1. 完成后，单击 **[!UICONTROL Save]**.

## 步骤5：查看并开始试验(Google)

1. 返回您的 [Google Analytics][2] 帐户。

1. 查看试验设置。

1. 如果准备就绪，请单击 **[!UICONTROL Start Experiment]**.

   否则，请单击 **[!UICONTROL Save for Later]**.


[2]: https://analytics.google.com/

---
title: 类别URL重写
description: 了解如何使用类别URL重写以将链接重定向到Commerce商店中其他类别的URL。
exl-id: fc18f472-4aa8-4203-ade9-7ca576689d61
feature: Categories, Configuration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '680'
ht-degree: 0%

---

# 类别URL重写

如果从目录中删除某个类别，则可以使用类别重写将链接重定向到商店中其他类别的URL。 思考以下方面 _目标_ / _原始请求_  或 _重定向到_ / _重定向自_. 尽管人们可能仍会从搜索引擎或过时的链接导航到之前的页面，但重定向会导致您的商店切换到新目标。

如果 [自动重定向](url-redirect-product-automatic.md) 为您的商店启用，在类别时不需要创建重写 [URL键](../catalog/catalog-urls.md) 已更改。

{{url-rewrite-skip}}

## 步骤1. 计划重写

要避免出错，请写下 _重定向到_ 路径和 _重定向自_ 路径并包含URL密钥和后缀（如果适用）。

如果不确定，请打开商店中的每个类别页面，然后从浏览器的地址栏复制路径。

**示例：**

重定向至： `gear/backpacks-and-bags.html`

重定向自： `gear/bags.html`

## 步骤2. 创建重写

{{url-rewrite-params}}

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL URL Rewrites]**.

1. 在继续操作之前，请执行以下操作以验证请求路径是否可用：

   - 在顶部的搜索筛选器中 **[!UICONTROL Request Path]** 列中，输入要重定向的类别的URL键，然后单击 **[!UICONTROL Search]**.

   - 如果该页面有多个重定向记录，请找到与适用的商店视图匹配的重定向记录，然后在编辑模式下打开该重定向记录。

   - 在右上角，单击 **[!UICONTROL Delete]**. 出现提示时，单击 **[!UICONTROL OK]** 以确认。

1. 当您返回 _[!UICONTROL URL Rewrites]_页面，单击&#x200B;**[!UICONTROL Add URL Rewrite]**.

1. 设置 **[!UICONTROL Create URL Rewrite]** 到 `For category` 并在树中选择作为重定向目标的目标类别。

   ![URL重写 — 选择类别](./assets/url-rewrite-category-choose.png){width="700" zoomable="yes"}

1. 在 _URL重写_ 部分，执行以下操作：

   - 如果您有多个商店，请选择 **[!UICONTROL Store]** 在适用重写时。

   - 对象 **[!UICONTROL Request Path]**，输入客户请求的类别的URL键。 这是 _重定向自_ 类别。

     >[!NOTE]
     >
     >对于指定的存储，请求路径必须是唯一的。 如果已经有使用同一请求路径的重定向，则在尝试保存该重定向时会收到一个错误。 必须先删除以前的重定向，然后才能创建重定向。

   - 设置 **[!UICONTROL Redirect]** 更改为以下任一项：

      - `Temporary (302)`
      - `Permanent (301)`

   - 请键入重写的简短说明，以供您参考。

   ![为类别添加URL重写](./assets/url-rewrite-for-category.png){width="700" zoomable="yes"}

1. 在保存重定向之前，请查看以下内容：

   - 左上角的链接显示目标类别的名称。
   - 请求路径包含原始文件的路径 _重定向自_ 类别。

1. 完成后，单击 **[!UICONTROL Save]** 按钮。

   新的类别重写显示在“URL重写”网格的顶部。

## 步骤3. 测试结果

1. 转到您商店的主页。

1. 执行以下操作之一：

   - 导航到原始文件 _重定向自_ 类别。
   - 在浏览器的地址栏中，输入原始文件的路径 _重定向自_ 类别，紧跟在商店URL之后，然后按 **[!UICONTROL Enter]**.

   此时将显示新的目标类别，而不是原始类别请求。

## 字段描述

| 字段 | 描述 |
|--- |--- |
| [!UICONTROL Create URL Rewrite] | 指示重写的类型。 创建重写后无法更改类型。 选项： `Custom` / `For category` / `For product` / `For CMS page` |
| [!UICONTROL Request Path] | 要重定向的类别。 根据您的配置，请求路径可能包含.html或.htm后缀以及父类别。 请求路径必须是唯一的，并且不能被另一个重定向使用。 如果您收到请求路径存在的错误，请删除现有重定向，然后重试。 |
| [!UICONTROL Target Path] | 系统用来指向重定向目标的内部路径。 目标路径呈灰显状态，无法编辑。 |
| [!UICONTROL Redirect] | 确定重定向的类型。 选项： <br/>**[!UICONTROL No]**— 未指定重定向。 许多操作都会创建此类型的重定向请求。 例如，每次将产品添加到类别时， `No` 在每个商店视图中创建类型。<br/>**[!UICONTROL Temporary (302)]**  — 向搜索引擎指示重写时间有限。 搜索引擎通常不会保留页面排名信息以进行临时重写。 <br/>**[!UICONTROL Permanent (301)]**— 向搜索引擎指示重写是永久的。 搜索引擎通常会保留页面排名信息以进行永久重写。 |
| [!UICONTROL Description] | 描述重写的用途，以供内部参考。 |

{style="table-layout:auto"}

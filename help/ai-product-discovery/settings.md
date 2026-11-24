---
title: 扩充设置
description: 在AI产品发现中配置交付、每月代理流量作业以及由目录扩充和PDP扩充共享的合格AI代理。
source-git-commit: ed404fb8515374a33116ccc811c96548fb14dd35
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 0%
---
# 扩充设置

使用AI产品发现工作区中的&#x200B;**[!UICONTROL Settings]**&#x200B;选项卡配置您的Adobe Commerce实例。 配置后，目录和PDP增强功能会显示在AI产品发现工作区中。

此选项卡上的字段标识AI产品发现连接到的[!DNL Adobe Commerce]环境和存储视图。 有关IMS登录和组织要求，请参阅[AI产品发现先决条件](prerequisites.md)。

1. 在管理员中，转到&#x200B;**[!UICONTROL AI Product Discovery]** > **[!UICONTROL Catalog Enrichment]**&#x200B;或&#x200B;**[!UICONTROL Product Details Page Enrichment]**。
1. 在页面顶部的&#x200B;**[!UICONTROL Scope]**&#x200B;列表中，选择要配置的商店视图，或保留&#x200B;**[!UICONTROL All Store Views]**&#x200B;以跨商店视图管理设置。
1. 打开&#x200B;**[!UICONTROL Settings]**&#x200B;选项卡。
1. 在&#x200B;**[!UICONTROL Commerce Configuration]**&#x200B;中，展开标记为其URL的存储区视图面板。

   提供您的[!DNL Adobe Commerce]环境详细信息以启用AI产品发现服务和审核工作流。

   “目录扩充设置”选项卡上的![Commerce配置](./assets/catalog-enrichment-commerce-config.png){zoomable="yes"}

1. 输入商店视图所需的连接详细信息。

   - **[!UICONTROL Store View URL]**：对应于商店视图的URL（例如，`https://brand.example.com/fr/`）。
   - **[!UICONTROL Environment ID]**：连接访问的[!DNL Adobe Commerce]环境的唯一标识符。
   - **[!UICONTROL Website Code]**、**[!UICONTROL Store Code]**&#x200B;和&#x200B;**[!UICONTROL Store View Code]**： Commerce网站的网站、商店和商店视图代码。 这些值必须与您的Commerce管理员中的代码匹配。
   - **[!UICONTROL Host Name]**： [!DNL Adobe Commerce]实例的主机名。
   - **（可选 — 仅用于目录扩充）**&#x200B;在&#x200B;**[!UICONTROL Catalog field limits]**&#x200B;下，选择&#x200B;**[!UICONTROL Limit maximum characters for product name]**&#x200B;并为任何生成的产品名称指定字符限制。 Select **[!UICONTROL Limit maximum characters for product description]**&#x200B;并指定任何生成的产品说明的字符限制。

1. 单击&#x200B;**[!UICONTROL Save]**。

保存后，请等待任何初始同步或验证作业完成，然后再依赖该存储视图的目录或审核结果。 产品建议可能需要24小时才能显示在&#x200B;**[!UICONTROL Catalog Enrichment]**&#x200B;页面上。

要删除商店视图配置，请展开该条目并单击&#x200B;**[!UICONTROL Delete]**。

## 字段描述 {#commerce-connection-fields}

在&#x200B;**[!UICONTROL Commerce Configuration]**&#x200B;表单中，必填字段标有星号(*)。

| 字段 | 必填 | 描述 |
| --- | --- | --- |
| 商店视图URL | 是 | 与商店视图对应的URL（例如，`https://brand.example.com/fr/`）。 |
| 环境ID | 是 | 连接访问的[!DNL Adobe Commerce]环境的唯一标识符。 |
| 网站代码 | 是 | Commerce网站的网站代码。 |
| 商店代码 | 是 | Commerce网站商店代码。 |
| 存储视图代码 | 是 | Commerce网站的商店视图。 |
| 主机名 | 是 | [!DNL Adobe Commerce]实例的主机名。 |
| 目录字段限制（仅限目录扩充） | 否 | 为任何生成的产品名称和描述定义字符限制。 |

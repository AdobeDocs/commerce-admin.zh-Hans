---
title: 为Visual Merchandiser配置智能属性
description: 了解如何配置可视化促销器使用的智能属性。
exl-id: 7bbbca40-d991-4393-b99c-5bef2e711071
feature: Merchandising, Products, Configuration, Attributes
badgePaas: label="仅限PaaS" type="Informative" url="https://experienceleague.adobe.com/zh-hans/docs/commerce/user-guides/product-solutions" tooltip="仅适用于云项目（Adobe管理的PaaS基础架构）和内部部署项目上的Adobe Commerce 。"
TQID: https://experienceleague.adobe.com/-6tbdpZ7L6nS1sIOXdk5Faxpkkt9qzqWhIjqp9MwgiM
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 196
ht-degree: 0%

---

# 为Visual Merchandiser配置智能属性

{{ee-feature}}

可视促销器配置确定可在促销窗口中使用的属性以及最小库存阈值。 该配置还标识用于颜色的属性和颜色值的顺序。

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧面板中，展开&#x200B;**[!UICONTROL Catalog]**&#x200B;并在下面选择&#x200B;**[!UICONTROL Visual Merchandiser]**。

1. 展开&#x200B;**[!UICONTROL General Options]**&#x200B;部分的![扩展选择器](../assets/icon-display-expand.png)。

   ![目录配置 — 可视化推销员](../configuration-reference/catalog/assets/catalog-visual-merchandiser-general-options.png){width="600" zoomable="yes"}

1. 在&#x200B;**[!UICONTROL Attributes for Category Rules]**&#x200B;列表中，选择要用于可视化促销的每个属性。

   要选择多个属性，请按住Ctrl键(PC)或Command键(Mac)并单击每个项目。

1. 输入产品在“可视推销”窗口中显示的&#x200B;**[!UICONTROL Minimum Stock Threshold]**。

1. 输入&#x200B;**[!UICONTROL Color Attribute Code]**。

   默认值为`color`。 如果您的目录使用不同的属性，请以小写输入属性名称。

1. 对于&#x200B;**[!UICONTROL Color Order]**，请在单独的行上按顺序输入每个颜色值，以确定每个颜色的优先级。

1. 完成后，单击&#x200B;**[!UICONTROL Save Config]**。

---
title: 隐藏的类别
description: 了解如何将隐藏类别用于内部目的或链接到未包含在导航菜单中的类别。
exl-id: 43aa74b3-b4cd-488d-aa58-fa2c468fe3a2
feature: Catalog Management, Categories
TQID: https://experienceleague.adobe.com/vXJFiYxeTBcRQxdc4XGrPEPKuBAcqr-mnuUlh1WIskM
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
subfeature_v2:
  - id: e91a50b1-0b31-436e-9033-00e4776e94cb
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 186
ht-degree: 0%

---

# 隐藏的类别

隐藏类别有许多种使用方式。 您可能希望为自己的内部目的创建其他类别级别，但只向客户显示更高级别的类别。 或者，您可能希望链接到未包含在导航菜单中的类别。

## 创建隐藏类别

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Catalog]** > **[!UICONTROL Categories]**。

1. 在类别树中，选择要隐藏的类别，然后执行以下操作：

   - 将&#x200B;**[!UICONTROL Is Active]**&#x200B;设置为`Yes`。
   - 将&#x200B;**[!UICONTROL Include in Menu]**&#x200B;设置为`No`。

1. 在&#x200B;**[!UICONTROL Display Settings]**&#x200B;部分中，将&#x200B;**[!UICONTROL Anchor]**&#x200B;设置为`No`。

   ![隐藏的类别](./assets/hidden-categories.png){width="600" zoomable="yes"}

   隐藏类别处于活动状态，但不显示在顶部菜单或分层导航中。

1. 为每个隐藏的子类别完成以下设置以创建子类别：

   >[!NOTE]
   >
   >尽管类别是隐藏的，但您可以在其下面创建子类别并使它们处于活动状态。

   - 将&#x200B;**[!UICONTROL Enable Category]**&#x200B;设置为`Yes`。
   - 在&#x200B;**[!UICONTROL Display Settings]**&#x200B;部分中，将&#x200B;**[!UICONTROL Anchor]**&#x200B;设置为`Yes`。

   作为活动类别，您现在可以从商店中的其他位置链接到它们，但它们不会显示在菜单中。

1. 完成后，单击&#x200B;**[!UICONTROL Save]**。

---
title: 询价
description: 了解与公司帐户关联的客户如何提交询价。
exl-id: c52176a7-4076-4cea-8ddb-17e0d1a77fd9
feature: B2B, Quotes
role: Admin, User
TQID: https://experienceleague.adobe.com/lRPDBgKHCTklbiZ1QWsvXD--n86T-IySJDu9nv-umsU
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 258
ht-degree: 0%

---

# 询价

如果在[Sales功能配置](configure-quotes.md)中启用了报价，则公司的授权购买者可以通过从购物车中请求报价来启动价格洽谈流程。 如果买方未准备好提交报价以进行洽谈，则可以将它另存为草稿。

>[!NOTE]
>
>询价不能包含折扣码或礼品卡。

## 客户报价请求体验

1. 客户以具有[权限](account-company-roles-permissions.md)的购买者身份登录其用户帐户，以请求报价。

1. 将要包含在报价中的产品添加到购物车。

   >[!TIP]
   > 
   >客户可以使用[快速订购](quick-order.md)更快速地向购物车添加产品SKU列表。

1. 选择&#x200B;**[!UICONTROL Request a Quote]**。

   ![向购物车请求报价](./assets/quote-request-from-cart.png){width="700" zoomable="yes"}

1. 在&#x200B;**[!UICONTROL Add your comment]**&#x200B;框中，客户输入简短的注释以描述请求。

1. 输入&#x200B;**[!UICONTROL Quote Name]**。

   ![输入报价注释和名称](./assets/quote-request-from-cart-name-comments.png){width="400" zoomable="yes"}

1. 如果需要，将支持文档或图像附加到引号中：

   - 选择&#x200B;**[!UICONTROL Attach file]**。
   - 从系统选择文件。

   默认情况下，[附加文件](configure-quotes.md)最大为2 MB，采用以下任何文件格式：DOC、DOCX、XLS、XLSX、PDF、TXT、JPG或JPEG、PNG。

1. 创建并处理报价：

   - 通过选择&#x200B;**[!UICONTROL Request a Quote]**&#x200B;将报价发送给销售方。
   - 通过选择&#x200B;**[!UICONTROL Save as Draft]**&#x200B;将报价另存为草稿。

     如果买方将报价另存为草稿，则报价在[!UICONTROL My Quotes]中处于`Draft`状态。 在买方发送草稿报价以供复查之前，卖方看不到草稿报价。

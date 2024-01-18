---
title: 询价
description: 了解与公司帐户关联的客户如何提交询价。
exl-id: c52176a7-4076-4cea-8ddb-17e0d1a77fd9
feature: B2B, Quotes
role: Admin, User
source-git-commit: 265ec236d8391f676c876bcd95c610a8e72f4e70
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 0%

---

# 询价

如果在 [销售功能配置](configure-quotes.md)，公司的授权购买者可以通过从其购物车中请求报价来启动价格协商过程。 如果买方未准备好提交报价以进行洽谈，则可以将它另存为草稿。

>[!NOTE]
>
>询价不能包含折扣码或礼品卡。

## 客户报价请求体验

1. 客户以购买者的身份登录到其用户帐户， [权限](account-company-roles-permissions.md) 以请求报价。

1. 将他们希望包含在报价中的产品添加到购物车。

   >[!TIP]
   > 
   >如果您有要订购的产品SKU列表，请使用更快地将其添加到购物车 [快速订购](quick-order.md).

1. 选择 **[!UICONTROL Request a Quote]**.

   ![从购物车请求报价](./assets/quote-request-from-cart.png){width="700" zoomable="yes"}

1. 在 **[!UICONTROL Add your comment]** 框中，输入描述请求的简短说明。

1. 输入 **[!UICONTROL Quote Name]**.

   ![输入报价单注释和名称](./assets/quote-request-from-cart-name-comments.png){width="400" zoomable="yes"}

1. 如果需要，将支持文档或图像附加到引号中：

   - 选择 **[!UICONTROL Attach file]**.
   - 从系统选择文件。

   默认情况下， [附加文件](configure-quotes.md) 最大为2 MB，采用以下任意文件格式：DOC、DOCX、XLS、XLSX、PDF、TXT、JPG或JPEG、PNG。

1. 创建并处理报价：

   - 通过选择将报价发送给销售方 **[!UICONTROL Request a Quote]**.
   - [!BADGE 1.5.0 Beta版功能]{type=Informative url="/help/b2b/release-notes.md" tooltip="仅供测试版计划参与者使用"}**[!UICONTROL Save as Draft]**.

     如果买方将报价另存为草稿，则报价可在 [!UICONTROL My Quotes] 在 `Draft` 省/州。 在买方打开草稿报价并提交它之前，卖方看不到它。

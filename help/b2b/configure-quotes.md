---
title: 配置引号
description: 了解报价配置，该配置控制报价请求所需的最低订单量、报价生命周期和文件附件。
exl-id: 865f6624-df9b-4f78-abfa-1f9a3d82bc0d
feature: B2B, Companies, Configuration, Quotes
role: Admin
source-git-commit: d4c3ea4b49e30ae3af249516d32fb28437d218b8
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 0%

---

# 配置引号

如果在一般情况下启用了引号 [B2B功能](enable-basic-features.md)中，您可以在管理员中配置对引号的支持。 报价配置确定了报价请求所需的最低订单量、报价存留期以及附件支持的文件格式。

>[!NOTE]
>
>报价配置选项和使用报价洽谈功能的能力可通过以下选项进行控制 [角色资源](../systems/permissions-user-roles.md#role-resources). 必须为分配给管理员用户帐户的管理员用户角色选择这些角色资源。 要授予对Admin中报价功能的访问权限，请转到 **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL User Roles]**，选择角色，然后导航到 [!UICONTROL Sales] > [!UICONTROL Operations] > [!UICONTROL Quotes] 在_&#x200B;角色资源&#x200B;_树。

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中，展开 **[!UICONTROL Sales]** 并选择 **[!UICONTROL Quotes]**.

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL General]** 部分并执行以下操作：

   ![销售报价单配置 — 常规](./assets/quotes-general.png){width="700" zoomable="yes"}

   请参阅 [引号](../configuration-reference/sales/quotes.md) 在 _配置引用_ 有关Quotes功能选项及其功能的完整列表。

   - 输入 **[!UICONTROL Minimum Amount]** 在提交报价请求之前必须满足的购物车中。

   - 对象 **[!UICONTROL Minimum Amount Message]**，输入当购物车总计不符合最低要求金额时要显示的消息。

   - 对象 **[!UICONTROL Default Expiration Period]**，输入数字 **[!UICONTROL days]**， **[!UICONTROL weeks]**，或 **[!UICONTROL months]** 引号将保持有效。

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Attached files]** 部分并执行以下操作：

   - 对象 **[!UICONTROL File formats for upload]**，输入您支持附加到引号中文件的每种文件类型的后缀。

     以小写输入每个文件后缀，并用逗号分隔。

     默认情况下，支持以下格式： `doc`， `docx`， `xls`， `xlsx`， `pdf`， `txt`， `jpg`， `png`、和 `jpeg`

   - 对象 **[!UICONTROL Maximum file size]**，输入附加文件的最大大小（以MB为单位）。

     输入的值可能会被服务器设置覆盖。

     ![销售报价单配置 — 附加文件](./assets/quotes-attached-files.png){width="600" zoomable="yes"}

1. 完成后，单击 **[!UICONTROL Save Config]**.

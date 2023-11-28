---
title: 存档订单
description: 了解如何配置订单存档以提高性能并简化组织的Commerce。
exl-id: 12025591-bfe2-4f44-9358-a38ea4493b5c
feature: Orders, Configuration
source-git-commit: 47f170f1a1dd1c236b99c2e7139bb119368abf47
workflow-type: tm+mt
source-wordcount: '745'
ht-degree: 0%

---

# 存档订单

{{ee-feature}}

定期存档订单可提高性能，使您的工作区中不存在不必要的信息，因此您可以专注于当前的业务。 发票、发运和贷项通知单可以自动或人工存档，并可以随时查看。

>[!NOTE]
>
>此 _[!UICONTROL Archive]_选项将显示在 [[!UICONTROL Sales] 菜单](sales-menu.md) 仅当存档为 [已启用](../configuration-reference/sales/sales.md).

## 配置订单存档

可以将您的商店配置为在设定的天数后存档订单、发票、发运和贷项通知单。 您可以将订单及其关联文档移到存档中，或将它们恢复到其以前的状态。 存档的订单不会被删除，并且管理员可以继续使用这些订单。 存档数据可导出为CSV文件并在电子表格中打开。 启用后， _存档_ 操作显示在工作区顶部。

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中，展开 **[!UICONTROL Sales]** 部分并选择 **[!UICONTROL Sales]** 下方。

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Orders, Invoices, Shipments, Credit Memos Archiving]** 部分。

   ![订单、发票、发运、贷项通知单存档配置设置](../configuration-reference/sales/assets/sales-orders-invoices-shipments-credit-memos-archiving.png){width="600" zoomable="yes"}

1. 设置 **[!UICONTROL Enable Archiving]** 到 `Yes`.

   >[!NOTE]
   >
   >如果您稍后决定关闭存档，则所有已存档的订单将恢复到以前的状态。

1. 设置 **[!UICONTROL Archive Orders Purchased]** 到完成订单存档前等待的天数。

   默认情况下，订单会在购买30天后存档。

1. 在 **[!UICONTROL Order Statuses to be Archived]** 列表中，选择要用于标识要存档的订单的每个订单状态。

   要选择多个项目，请在单击每个项目时按住Ctrl键(Windows)或Command键(Mac)。

1. 单击 **[!UICONTROL Save Config]**.

1. 出现提示时，刷新任何无效的缓存。

## 查看存档的文档

1. 在 _[!UICONTROL Sales]_下的菜单_[!UICONTROL Archive]_，选择以下任一选项：

   - **[!UICONTROL Orders]**
   - **[!UICONTROL Invoices]**
   - **[!UICONTROL Shipments]**
   - **[!UICONTROL Credit Memos]**

1. 要查看详细信息，请单击列表中的任何存档文档。

## 将操作应用到已存档文档

选择要作为操作目标的每个文档，然后选择下列选项之一 **[!UICONTROL Actions]**：

- `Cancel`
- `Hold`
- `Unhold`
- `Print`
- `Move to Orders Management`

## 手动存档文档

1. 从以下项中选择要存档的文档类型：

   - **[!UICONTROL Orders]**
   - **[!UICONTROL Invoices]**
   - **[!UICONTROL Shipments]**
   - **[!UICONTROL Credit Memos]**

1. 选中要存档的每个项目的复选框。

1. 在右上角，设置 **[!UICONTROL Actions]** 到 `Move to Archive`.

1. 单击 **[!UICONTROL Submit]** 将所选文档存档。

## 恢复存档的文档

1. 选择要还原的文档类型。

1. 使用以下选项之一选择文档：

   - 要选择所有可见文档，请单击左上角的 **[!UICONTROL Select Visible]**.

   - 手动选中要还原的每个文档的复选框。

1. 在右上角，设置 **[!UICONTROL Action]** 到 `Move to Orders Management`.

1. 单击 **[!UICONTROL Submit]** 以恢复文档。

## 导出存档的文档

1. 选择要导出的文档类型。

1. 在右上角菜单中，设置 **[!UICONTROL Export to:]** 更改为下列值之一：

   - `CSV`
   - `Excel`

1. 单击 **[!UICONTROL Export]**.

可以将您的商店配置为在设定的天数后存档订单、发票、发运和贷项通知单。 您可以将订单及其关联文档移到存档中，或将它们恢复到其以前的状态。 存档的订单不会被删除，并且管理员可以继续使用这些订单。 存档数据可导出为CSV文件并在电子表格中打开。 启用后， _[!UICONTROL Archive]_命令显示在工作区的顶部。

## 手动存档订单

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. 要选择网格上的顺序，请选中第一列中的复选框。

1. 设置 **[!UICONTROL Actions]** 控制对象 `Move to Archive` 并查找已存档订单的消息。

   ![将所选订单移至存档 ](./assets/order-move-to-archive.png){width="700" zoomable="yes"}

>[!TIP]
>
>要指定可存档的订单状态列表，请参阅 [配置订单存档](#configure-the-order-archive).

## 查看已存档订单

1. 使用以下方法之一打开存档视图：

   - 在上方的按钮栏中 _[!UICONTROL Orders]_网格，单击&#x200B;**[!UICONTROL Go to Archive]**.

   - 在 _管理员_ 侧栏，转到 **[!UICONTROL Sales]** > _[!UICONTROL Archive]_>**[!UICONTROL Orders]**.

   >[!NOTE]
   >
   >与“订单”页一样，存档订单页的标题为 _[!UICONTROL Orders]_. 唯一显着的区别是按钮栏中用于_[!UICONTROL Return to Orders Management]_. 页面的URL还指示您处于顺序存档中。

1. 在 _操作_ 列，单击 **[!UICONTROL View]**.

   ![查看已存档订单](./assets/order-archived-view.png){width="600" zoomable="yes"}

## 恢复已存档的订单

>[!NOTE]
>
>根据中配置的天数，系统会将从已存档订单恢复的订单再次存档。 [!UICONTROL Archive Orders Purchased] 设置(请参阅 [配置订单存档](#configure-the-order-archive))。 天数根据 [!UICONTROL Updated At] 订单的日期，当从存档中移动订单时，此日期会更改。

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. 在按钮栏中，单击 **[!UICONTROL Go to Archive]**.

1. 找到要恢复的记录，然后单击复选框将其选中。

   ![选择要恢复的顺序](./assets/order-archived-select-to-restore.png){width="600" zoomable="yes"}

1. 设置 **[!UICONTROL Actions]** 控制值至 `Move to Order Management`.

查找已存档订单已从存档中删除的消息。

## 导出存档订单

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. 在操作菜单中，单击 **[!UICONTROL Export]** 并选择所需的格式。

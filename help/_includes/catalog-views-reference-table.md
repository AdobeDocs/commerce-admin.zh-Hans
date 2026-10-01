---
title: 目录视图引用表
description: 目录视图网格的重用参考表
source-git-commit: bc4baccc4b40fb7ecdc7f489bfaf3c797881db88
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 0%
---
# 目录视图引用表

网格为共享目录同步到[!DNL Adobe Commerce Optimizer]时创建的每个目录视图列出一行。 除了键分配操作之外，该网格是只读的。 当连接器同步Adobe Commerce中配置的共享目录时，将自动创建和删除目录视图。 如果删除目录，则在删除相应的目录视图和数据之前存在[宽限期](/help/systems/catalog-view-sync-status.md#configure-the-deletion-grace-period)。

要分配或取消分配受限访问密钥，请参阅[将密钥分配给目录视图](/help/systems/restricted-access-keys.md#assign-keys-to-a-catalog-view)。

| 字段 | 描述 |
| --- | --- |
| [!UICONTROL ACO Catalog View ID] | [!DNL Adobe Commerce Optimizer]中相应目录视图的标识符。 查看[目录视图同步状态摘要](/help/systems/catalog-view-sync-status.md#catalog-view-sync-status-summary)以检查其同步运行状况。 |
| [!UICONTROL Store View] | 目录视图表示的存储视图。 查看[存储视图](/help/stores-purchase/store-views.md)。 |
| [!UICONTROL Access Keys] | 当前分配给目录视图的受限制访问键的标题。 请参阅[受限访问密钥管理](/help/systems/restricted-access-keys.md)。 |
| [!UICONTROL Actions] | 选择&#x200B;**[!UICONTROL Edit Restricted Access Keys]**&#x200B;为目录视图分配或取消分配密钥。 查看[将密钥分配给目录视图](/help/systems/restricted-access-keys.md#assign-keys-to-a-catalog-view)。 |

{style="table-layout:auto"}

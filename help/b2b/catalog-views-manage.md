---
title: 管理目录视图配置
description: 了解如何查看为B2B共享目录创建的Adobe Commerce Optimizer目录视图，并分配保护它们的受限访问密钥。
feature: B2B, Companies, Catalog Management
last-update: 2026-10-01
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
    internal-label: Catalog management
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: e9004f3c-09ae-5d24-acd2-fa0987fdb66e
    internal-label: Companies
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
    internal-label: Accounts
subfeature_v2:
  - id: f56d26ed-050b-4fb7-b29b-8e6e994e80a2
    internal-label: B2B
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 15f1e2ee152fb047443da68dec2cc69551e6c7a0
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 0%
---
# 管理目录视图配置

安装[!DNL Adobe Commerce Optimizer Connector for B2B]扩展后，“目录视图”页面会列出为自定义共享目录创建的[!DNL Adobe Commerce Optimizer] [目录视图投影](https://experienceleague-review.adobe.com/en/docs/commerce/aco-optimizer-connector/b2b-shared-catalog-projection){target="_blank"}。  _投影_&#x200B;是连接器将共享目录数据同步到[!DNL Adobe Commerce Optimizer]时创建的目录视图。 连接器为共享目录中的每个存储视图创建单独的投影，因此共享目录可以有多个目录视图。 在店面体验中，这些目录视图仅可供分配给相关共享目录的公司访问。

例如，假设Acme Industrial被分配到一个共享目录EU Business，它属于EU网站。 该网站有两种商店视图：

- `English (UK)`

- `German (Germany)`

连接器将共享目录投影到两个[!DNL Adobe Commerce Optimizer]目录视图中：

- `EU Business – English (UK)`

- `EU Business – German (Germany)`

该公司拥有英语和德语目录视图，但只有一个共享目录分配。 每个商店视图显示其相应目录视图中的数据。

当两个目录视图使用相同的网站和客户组定价范围时，它们可以共享相同的价格手册。

## 目录视图身份验证

连接器使用受限访问密钥保护目录视图。 Adobe Commerce使用私钥为授权买家签署访问令牌。 在返回受保护的目录数据之前，[!DNL Adobe Commerce Optimizer]根据与所请求的目录视图关联的相应公钥验证令牌。

要配置令牌生命周期或禁用令牌颁发，请参阅[服务> ACO目录视图](/help/configuration-reference/services/aco-catalog-view.md)。

您可以查看这些目录视图，并从共享目录的&#x200B;_[!UICONTROL Catalog Views]_选项卡或关联公司的_[!UICONTROL Catalog Views]_&#x200B;部分管理其分配的密钥，这两个部分均列出相同的目录视图和当前密钥分配。 请参阅[编辑受限访问密钥](#edit-restricted-access-keys)，以了解每个位置的确切导航路径。

要监视到[!DNL Adobe Commerce Optimizer]的共享目录数据同步，请参阅[目录视图同步状态监视](/help/systems/catalog-view-sync-status.md)。

## 目录视图引用

{{$include /help/_includes/catalog-views-reference-table.md}}

## 编辑受限访问密钥

{{$include /help/_includes/edit-restricted-access-keys.md}}

有关其他详细信息，请参阅[管理受限访问密钥](/help/systems/restricted-access-keys.md)。

>[!MORELIKETHIS]
>
> - [B2B共享目录投影](https://experienceleague-review.adobe.com/en/docs/commerce/aco-optimizer-connector/b2b-shared-catalog-projection){target="_blank"}
> - [服务> ACO目录视图](/help/configuration-reference/services/aco-catalog-view.md)
> - [目录视图同步状态监视](/help/systems/catalog-view-sync-status.md)
> - [管理您的共享目录](catalog-shared-manage.md)
> - [管理公司帐户](account-company-manage.md)

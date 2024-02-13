---
title: 适用于Commerce管理员的Adobe Experience Cloud集成
description: 了解Admin Unified Experience扩展，该扩展将Commerce与Experience Cloud集成，以便客户可以从Experience Cloud主页访问Commerce项目。
feature: Integration
exl-id: e3fb6337-c7d5-4b6f-8f4a-583697a1f2d2
source-git-commit: a07c91bc2f01cd110f3e0ccd6d27fe5d37eb2fc9
workflow-type: tm+mt
source-wordcount: '520'
ht-degree: 0%

---

# 适用于Commerce的Adobe Experience Cloud集成

{{ee-feature}}

通过启用Admin Unified Experience扩展，将Adobe Commerce项目与Experience Cloud集成。 当集成处于活动状态时，管理员可以从Adobe Experience Cloud访问Commerce项目。

![从Experience Cloud主页访问Commerce](./assets/admin-uex-home-page.png){width="700" zoomable="yes"}

## 查看可用的商务项目

管理员可以通过选择查看他们有权访问的Commerce项目 **[!UICONTROL Commerce]** 从Experience Cloud主页访问。

![Experience Cloud上的Commerce项目工作区](./assets/admin-uex-commerce-projects-home.png){width="700" zoomable="yes"}

管理员可以从打开每个项目的管理员和店面 [!DNL Commerce Projects] 并查看其他信息。

- **Commerce店面主页快照** — 店面主页的快照。 如果一个项目有多个网站，则快照会显示默认站点的主页。

- **[项目名称](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/architecture/pro-develop-deploy-workflow.html)** — 标识实例的云项目环境。 项目名称默认为 [Git分支名称](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/console-branches.html) 在云项目中。 在中更改或更新项目名称 [统一的Experience Store配置设置](admin-unified-experience-integration-manage.md#manage-the-integration-from-the-admin).

- **[店面URL](../stores-purchase/store-urls.md)** — 显示默认网站的基本URL。

- **[环境类型](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/architecture/pro-develop-deploy-workflow.html)** — 使用标识部署到开发或暂存环境的商务实例 [!UICONTROL Development] 或 [!UICONTROL Staging] 标签。 将没有标签的实例部署到生产环境。

- **Commerce管理员访问权限** — 通过单击打开“管理员” **[!UICONTROL Open]**.

- **店面访问** — 通过选择打开店面 **[!UICONTROL Open storefront]** （从选项菜单中）。

- **快速访问所选项目** — 选择 **[!UICONTROL Add to Favorites]** 从选项菜单将项目添加到 [!UICONTROL Favorites] 选项卡。

## 身份验证流程

启用Experience Cloud集成后，管理员使用以下工作流验证和访问Commerce项目。

1. 通过Experience Cloud登录页面登录。

   ![Experience Cloud登录页面](./assets/admin-uex-experience-cloud-login.png){width="600" zoomable="yes"}

   管理员必须登录才能使用与Commerce实例关联的Adobe的业务配置文件Experience Cloud。 请参阅 [管理Adobe配置文件](https://helpx.adobe.com/enterprise/using/manage-adobe-profiles.html).

1. 在Experience Cloud主页上，打开 [!UICONTROL Commerce Projects workspace] 通过选择 **[!UICONTROL Open]**.

1. 通过选择访问项目的管理员 **[!UICONTROL Open]**.

1. 在Adobe Commerce登录页面上，选择 **[!UICONTROL Sign in with Adobe ID]** 以完成身份验证并打开管理员。

   ![Adobe Commerce登录页面](./assets/admin-adobeid-login.png){width="600" zoomable="yes"}

>[!NOTE]
>
>请参阅 [管理Experience Cloud集成](admin-unified-experience-integration-manage.md) 以了解在启用或禁用Experience Cloud集成时身份验证工作流受到什么影响的详细信息。

## 要求

- Adobe Commerce 2.4.5或更高版本
- 云基础架构上的Adobe Commerce
- Adobe Commerce扩展

   - Commerce Admin Unified Experience扩展(`magento/module-unified-experience`)

     如果模块在商务实例上不可用，则可以使用编辑器进行安装。

   - [Adobe I/O事件服务](https://developer.adobe.com/commerce/extensibility/events/) — 需要发送事件数据以管理管理员对Commerce项目的Experience Cloud访问权限。

     Adobe I/O事件与Commerce的集成由Commerce Event扩展(`magento/commerce-eventing`)，此版本随Adobe Commerce 2.4.4及更高版本提供。

## 启用集成

按照以下说明启用集成： [配置与Commerce管理员的Experience Cloud集成](admin-unified-experience-integration-configure.md).

>[!TIP]
>
>如果已在商务实例上启用Experience Cloud集成，请参阅 [管理Experience Cloud集成](admin-unified-experience-integration-manage.md) 有关更改或更新配置、管理管理员访问权限和故障排除的详细信息。

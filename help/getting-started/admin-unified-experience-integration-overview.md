---
title: 适用于Commerce管理员的Adobe Experience Cloud集成
description: 了解Admin Unified Experience扩展，该扩展将Commerce与Experience Cloud集成，以便客户可以从Experience Cloud主页访问Commerce项目。
feature: Integration
exl-id: e3fb6337-c7d5-4b6f-8f4a-583697a1f2d2
badgePaas: label="仅限PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="仅适用于云项目(Adobe管理的PaaS基础架构)和内部部署项目上的Adobe Commerce 。"
source-git-commit: 77e7eb00e9f8d5af6361059c287707993180c4c4
workflow-type: tm+mt
source-wordcount: '549'
ht-degree: 0%

---

# 适用于Commerce的Adobe Experience Cloud集成

<table style="border:1px solid red">
<tr><td><img alt="Adobe Commerce功能" src="../assets/adobe-logo.svg" width="20" height="20" /> 仅在Adobe Commerce中独占的功能（<a href="https://experienceleague.adobe.com/docs/commerce-admin/user-guides/home.html#product-editions">了解更多</a>）</td></tr>
</table>

通过启用Admin Unified Experience扩展，将Adobe Commerce项目与Experience Cloud集成。 当集成处于活动状态时，管理员可以从Adobe Experience Cloud访问Commerce项目。

![从Experience Cloud主页访问Commerce](./assets/admin-uex-home-page.png){width="700" zoomable="yes"}

## 查看可用的Commerce项目

管理员可以通过从Commerce主页中选择&#x200B;**[!UICONTROL Commerce]**&#x200B;来查看他们有权访问的Experience Cloud项目。

Experience Cloud上的![Commerce项目工作区](./assets/admin-uex-commerce-projects-home.png){width="700" zoomable="yes"}

管理员可以从[!DNL Commerce Projects]工作区打开每个项目的管理员和店面，并查看其他信息。

- **Commerce店面主页的快照** — 店面主页的快照。 如果一个项目有多个网站，则快照会显示默认站点的主页。

- **[项目名称](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/architecture/pro-develop-deploy-workflow.html)** — 标识实例的云项目环境。 项目名称默认为云项目中的[Git分支名称](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/console-branches.html)。 在[统一Experience Store配置设置](admin-unified-experience-integration-manage.md#manage-the-integration-from-the-admin)中更改或更新项目名称。

- **[店面URL](../stores-purchase/store-urls.md)** — 显示默认网站的基本URL。

- **[环境类型](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/architecture/pro-develop-deploy-workflow.html)** — 部署到开发或暂存环境的Commerce实例使用[!UICONTROL Development]或[!UICONTROL Staging]标签进行标识。 将没有标签的实例部署到生产环境。

- **Commerce管理员访问权限** — 单击&#x200B;**[!UICONTROL Open]**&#x200B;打开管理员。

- **店面访问** — 通过从选项菜单中选择&#x200B;**[!UICONTROL Open storefront]**&#x200B;打开店面。

- **快速访问以选择项目** — 从“选项”菜单中选择&#x200B;**[!UICONTROL Add to Favorites]**&#x200B;以向[!UICONTROL Favorites]选项卡添加项目。

## 身份验证流程

启用Experience Cloud集成后，管理员使用以下工作流来验证和访问Commerce项目。

1. 通过Experience Cloud登录页面登录。

   ![Experience Cloud登录页面](./assets/admin-uex-experience-cloud-login.png){width="600" zoomable="yes"}

   管理员必须使用与Experience Cloud实例关联的组织的Adobe业务配置文件登录到Commerce。 请参阅[管理Adobe配置文件](https://helpx.adobe.com/enterprise/using/manage-adobe-profiles.html)。

1. 在Experience Cloud主页上，通过选择&#x200B;**[!UICONTROL Open]**&#x200B;打开[!UICONTROL Commerce Projects workspace]。

1. 通过选择&#x200B;**[!UICONTROL Open]**&#x200B;访问项目的管理员。

1. 在Adobe Commerce登录页面上，选择&#x200B;**[!UICONTROL Sign in with Adobe ID]**&#x200B;以完成身份验证并打开管理员。

   ![Adobe Commerce登录页面](./assets/admin-adobeid-login.png){width="600" zoomable="yes"}

>[!NOTE]
>
>有关启用或禁用Experience Cloud集成时身份验证工作流如何受到影响的详细信息，请参阅[管理Experience Cloud集成](admin-unified-experience-integration-manage.md)。

## 要求

- Adobe Commerce 2.4.5或更高版本
- 云基础架构上的Adobe Commerce
- Adobe Commerce扩展

   - Commerce Admin Unified Experience扩展(`magento/module-unified-experience`)

     如果该模块在Commerce实例中不可用，则可以使用编辑器进行安装。

   - [Adobe I/O Events服务](https://developer.adobe.com/commerce/extensibility/events/) — 需要发送事件数据以管理管理员对Experience Cloud中Commerce项目的访问权限。

     Adobe I/O Events与Commerce的集成通过Commerce Event扩展(`magento/commerce-eventing`)启用，该扩展在Adobe Commerce 2.4.4及更高版本中可用。

## 启用集成

按照[配置Experience Cloud与Commerce管理员的集成](admin-unified-experience-integration-configure.md)的说明启用集成。

>[!TIP]
>
>如果已在Commerce实例上启用Experience Cloud集成，请参阅[管理Experience Cloud集成](admin-unified-experience-integration-manage.md)，以了解有关更改或更新配置、管理管理员访问权限和疑难解答的详细信息。

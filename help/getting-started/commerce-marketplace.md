---
title: ’[!DNL Adobe Commerce Marketplace]’
description: 了解 [!DNL Commerce Marketplace]，为商家提供精选的解决方案，并为符合条件的开发人员提供工具、平台和首选位置，以打造欣欣向荣的业务。
exl-id: e04e48f2-3b1d-45bf-b0f6-3a1ed43e78c5
feature: Extensions
source-git-commit: 02e7c71fc47e6850371bfbdc1be50f65ec8015e9
workflow-type: tm+mt
source-wordcount: '1268'
ht-degree: 0%

---

# Adobe Commerce市场

[Adobe Commerce市场][1] 是应用商店，为商家提供精选的解决方案，并为符合条件的开发人员提供工具、平台和理想的位置，以打造欣欣向荣的业务。 [!DNL Commerce Marketplace] 提供一系列免费扩展和其他待售扩展。 可以通过信用卡或支付购买费用 [PayPal][2].

所有扩展均在以下位置提供： [!DNL Commerce Marketplace] 通过了广泛的审查。 此 [扩展质量计划][3] (EQP)组合项 [!DNL Commerce] 专业知识、开发准则和验证工具，以确保Commerce Marketplace的所有扩展都符合编码标准和最佳实践。 审核过程包括自动检查和手动QA审核。 在此过程中，会检查并测试每个扩展的结构和代码，以查找病毒/恶意软件感染的证据以及是否存在任何抄袭迹象。 审核工作包括由一名董事进行深入的技术审查及健康情况检查。 [!DNL Commerce] 工程师，侧重于文档、编码结构、性能、可扩展性、安全性和与 [!DNL Commerce] 核心。

尽管您可以从其他来源购买扩展，但只能购买上可用的扩展 [!DNL Commerce Marketplace] 通过扩展质量计划内的大量技术和营销审查进行了验证。

## 应用程序资源

开发人员传统上使用PHP创建进程内扩展以向Adobe Commerce添加特性、功能、服务和集成。 通过创建具有进程外可扩展性的应用程序（而不是扩展），您可以避免出现兼容性问题。

以下资源为新采用者熟悉应用程序提供了起点：

### Commerce资源

- [为Adobe Commerce设置I/O事件](https://developer.adobe.com/commerce/extensibility/events/)
- [为Adobe Commerce配置事件](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/)
- [设置管理员UI SDK](https://developer.adobe.com/commerce/extensibility/admin-ui-sdk/)
- [将扩展转换为应用程序](https://developer.adobe.com/commerce/extensibility/app-development/#how-do-i-port-an-extension-into-an-app)

### App Builder资源

- [Commerce App Builder概述](https://developer.adobe.com/commerce/extensibility/app-development/)
- [为Adobe Developer App Builder设置API网格](https://developer.adobe.com/graphql-mesh-gateway/gateway/getting-started/)
- [部署App Builder应用程序](https://developer.adobe.com/app-builder/docs/guides/deployment/)
- [App Builder应用程序的CI/CD](https://developer.adobe.com/app-builder/docs/guides/deployment/ci_cd_for_firefly_apps/)
- App Builder/开发人员控制台快速入门
   - [App Builder快速入门](https://developer.adobe.com/app-builder/docs/getting_started/)
   - [了解项目和工作区](https://developer.adobe.com/app-builder/docs/resources/videos/exploring/projects-and-workspaces/)

## [!DNL Marketplace] 凭据

安装从购买的扩展之前 [!DNL Commerce Marketplace]，登录到您的 [!DNL Commerce] 帐户并验证您是否拥有有效的访问密钥。 您可以登录到 [!DNL Commerce] 标题中的帐户 [[!DNL Marketplace]][1] 或 [Magento.com][6].

您的访问密钥是一组公共和私钥，用于同步 [!DNL Commerce] 使用进行安装 [!DNL Commerce] 帐户并验证您的凭据。 帐户同步后，每次从Commerce Marketplace安装扩展或模块或升级时，都必须输入私钥。 [!DNL Commerce] 安装。

您可以为不同目的创建多个访问密钥，并根据需要启用或禁用它们。 但是，您必须使用用于安装 [!DNL Commerce] 软件。 例如，您不能使用Magento Open Source访问密钥来更新或升级Adobe Commerce，反之亦然。 您也无法使用属于另一个用户或来自的用户的访问密钥 [共享帐户](commerce-account-share.md).

### 创建访问密钥

1. 登录到您的 [!DNL Commerce] 帐户。

1. 在 _[!UICONTROL My Account]_页面上，选择&#x200B;**[!UICONTROL Marketplace]**选项卡。

1. 在名称的右上角，单击向下箭头并选择 **[!UICONTROL My Profile]**.

   ![您的 [!DNL Marketplace] 个人资料](./assets/marketplace-profile.png){width="600"}

1. 在 _[!UICONTROL Marketplace]_选项卡在_[!UICONTROL My Products]_，单击 **[!UICONTROL Access Keys]**，然后执行以下任一操作：

   - 查看您是否已经拥有一组用于您的市场购买的访问密钥。 您可以为不同目的创建多组访问键。

   ![访问密钥](./assets/access-keys.png){width="600"}

   - 单击 **[!UICONTROL Create a New Access Key]**. 输入新密钥对的名称，然后单击 **[!UICONTROL OK]**. 有效字符包括大写和小写字符以及连字符而不是空格。

1. 完成后，单击 **[!UICONTROL OK]**.

   您的新访问密钥已启用，并显示在列表中。

   请注意 _复制_ 每个公钥和私钥之后的链接。 在下一步中，您将复制并粘贴这些值，以将存储与Commerce Marketplace同步。

## 安装过程

>[!IMPORTANT]
>
>从Adobe Commerce和Magento Open Source2.4.0开始，将删除“Web设置向导”，您必须使用命令行执行以下操作 [安装](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/advanced.html) 或 [升级](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/implementation/perform-upgrade.html) 您的实例。 此要求还包括 [模块](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html) 和 [扩展](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html).

的安装过程 [!DNL Marketplace] 购买与以下内容不同 _内部部署_ Commerce的安装比托管在上的安装的多 [Adobe云架构][4].

![Commerce Marketplace](./assets/marketplace.png){width="600"}

## 支持

如果您在安装或使用扩展时需要帮助，请首先查看扩展随附的文档。 如果找不到问题的答案，请使用扩展列表中的联系信息直接联系开发人员。 如果您在Marketplace上购买的产品无法满足您的需求，您可以 [请求退款](#refund-requests) 二十五日内支付。 Adobe将复查所有退款请求，并（如果获得批准）发出相应的退款。 有关与Commerce Marketplace相关的支持问题，请参阅 [[!DNL Marketplace] 帮助中心][5].

### 签出问题

必须在Marketplace购买系统中填写帐户配置文件中的地址字段以进行验证。

1. 在您的Marketplace帐户配置文件中添加地址字段。
1. 保存更新的配置文件。
1. 继续您的结帐。

### 登录问题

登录问题通常与帐户数据库中的MAGEID和电子邮件地址不匹配有关。 如需帮助，请联系市场支持。

>[!INFO]
>
>应用程序和扩展购买不能为 [已传输](#purchase-transfers) 到新帐户。

### 开源问题

市场支持团队解决了与以下内容相关的问题： [commercemarketplace.adobe.com/](https://commercemarketplace.adobe.com/) 和 [commercedeveloper.adobe.com/](https://commercedeveloper.adobe.com/) 仅限站点。 请将有关Magento Open Source的问题发送至 [社区论坛](https://community.magento.com/) 或 [联系合作伙伴](https://business.adobe.com/products/magento/partners.html) 可以协助Magento Open Source的人。

### 退款申请

要申请购买Marketplace的退款，请登录您的帐户并执行以下步骤：

1. 单击 [!UICONTROL **我的个人资料**] > [!UICONTROL **购买历史记录**].
1. 找到购买内容并单击 [!UICONTROL **请求退款**].
1. 完成退款订单表。

Marketplace Support将在生成退款请求后请求信息。 退款选项可在购买日期后25天内使用。 请参阅 [Marketplace客户协议](https://www.adobe.com/legal/terms/enterprise-licensing/magento-legacy-terms.html).

### 订单发票

您可以从以下位置下载订单发票： [!UICONTROL **购买历史记录**] （在您的Marketplace帐户中）。 发票不提供VAT或卖方地址，因为此时它不是Marketplace要求。

要下载Marketplace购买的订单发票，请登录Marketplace帐户并执行以下步骤：

1. 单击 [!UICONTROL **我的个人资料**] > [!UICONTROL **购买历史记录**].
1. 找到购买。
1. 单击订单右上角的打印机图标。

### 采购转帐

Marketplace支持团队无法将购买转移到其他帐户。 您必须购买主Commerce帐户下的所有应用程序和扩展，以避免安装和部署问题。 Adobe Commerce有权使用一个唯一标识符。 由于使用Composer进行安装，因此 [访问密钥](#create-an-access-key) 可使用绑定到主帐户的情况。 唯一可用的解决方案是 [请求退款](#refund-requests) 从Marketplace购买帐户(如果Adobe Commerce退款政策允许)访问。

您可以 [共享](commerce-account-share.md) 通过主帐户访问的Commerce实例。 共享访问权限授予主帐户的下属帐户的特殊权限。 共享接入点是从主帐户生成的。 主帐户可以是Commerce授权帐户、主商家帐户或在组织内共享的帐户。

这些特殊权限会授予用户与主要用户相同级别的Adobe Commerce访问权限，但不会转到Adobe Commerce Marketplace或开发人员门户。 这意味着从市场中的从属帐户购买扩展时不能与主帐户共享。 共享访问是单向访问（主帐户到从属帐户）。 当从属帐户尝试共享回主帐户时，此方法不起作用。

[1]: https://marketplace.magento.com/
[2]: https://www.paypal.com/us/home
[3]: https://developer.adobe.com/commerce/marketplace/guides/sellers/extension-quality-program/
[4]: https://www.adobe.com/commerce/magento/enterprise.html
[5]: https://marketplacesupport.magento.com/hc/en-us
[6]: https://business.adobe.com/products/magento/magento-commerce.html

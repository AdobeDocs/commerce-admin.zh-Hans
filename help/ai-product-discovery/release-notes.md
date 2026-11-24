---
title: AI产品发现发行说明
description: 有关目录和PDP扩充功能、修复、升级指导、支持的Commerce版本以及已知问题，请查看AI产品发现发行说明。
feature: Release Notes
source-git-commit: ed404fb8515374a33116ccc811c96548fb14dd35
workflow-type: tm+mt
source-wordcount: '734'
ht-degree: 0%
---
# AI产品发现发行说明

这些发行说明涵盖对目录扩充和PDP扩充的更新，包括新功能、修复、升级要求和已知问题。 每个版本条目都会标识受影响的扩展或工作流。

![新](../assets/new.svg)新功能
![已修复问题](../assets/fix.svg)修复和改进
![已知问题](../assets/bug.svg)已知问题

## 发行版本2.1.3 {#release-2-1-3}

*2026年11月30日*

在PHP 8.3到8.5上[!BADGE 支持]{type=Informative tooltip="支持"}[!DNL Adobe Commerce] 2.4.9、2.4.8和2.4.7。[!DNL Adobe Commerce as a Cloud Service]

版本2.1.3将产品详细信息页面扩充与目录扩充合并到一个名为&#x200B;**AI产品发现**&#x200B;的新管理员菜单项中。 此外，支持范围扩展到[!DNL Adobe Commerce as a Cloud Service]。

## 发行版本2.1.2 {#release-2-1-2}

*2026年10月22日*

在PHP 8.3到8.5上[!BADGE 支持]{type=Informative tooltip="支持"}[!DNL Adobe Commerce] 2.4.9、2.4.8和2.4.7。

版本2.1.2将目录扩充作为自含扩展。 它现在包含以前由单独的[!DNL Adobe Brand Visibility]扩展(`magento/llm-optimizer`)提供的所有内容：将批准的建议应用于目录、回滚这些建议，以及保护您自己的编辑内容不被覆盖。

### 从早期版本升级 {#upgrade-from-earlier-versions}

>[!IMPORTANT]
>
>版本2.1.2不能与[!DNL Adobe Brand Visibility]扩展一起安装。 如果已安装，请在升级过程中将其删除。

1. 删除[!DNL Adobe Brand Visibility]扩展（如果已安装）：

   ```bash
   composer remove magento/llm-optimizer
   ```

   如果该扩展是通过将`Magento/LlmoCatalog`复制或符号链接到`app/code`中安装的，请删除该目录。 不仅要禁用模块：磁盘上仍存在的已禁用模块可能会导致`setup:upgrade`删除存储扩充产品原始值的表。

1. 更新目录扩充并应用更改：

   ```bash
   composer require magento/module-catalog-enrichment:^2.1
   bin/magento setup:upgrade
   bin/magento cache:flush
   ```

   升级后刷新缓存。 升级会将现有访问授权移动到新权限资源，并且这些授权在清除缓存之前不会生效。

### 要求

![新](../assets/new.svg) **PHP 8.3和[!DNL Adobe Commerce] 2.4.7或更高版本**—PHP 8.1的生命周期已终止，并且PHP 8.2的生命周期将于2026年12月31日终止，因此这两种版本均不受支持。不支持[!DNL Adobe Commerce] 2.4.6及更早版本。

### 新增功能

![新建](../assets/new.svg) **[!UICONTROL AI Product Discovery]菜单** — 目录扩充页面现在在管理员侧边栏中有自己的部分。 转到&#x200B;**[!UICONTROL AI Product Discovery]** > **[!UICONTROL Catalog Enrichment]**。 以前，页面位于&#x200B;**[!UICONTROL Catalog]**&#x200B;下。

![新](../assets/new.svg) [!BADGE Beta]{type=Informative tooltip="尚未正式提供"} **[!UICONTROL Product Details Page Enrichment (Beta)]** — 位于&#x200B;**[!UICONTROL AI Product Discovery]**&#x200B;下的新页面，用于查看产品详细信息页面的扩充建议。 产品详细信息页面扩充为测试版，尚未正式发布。

![新建](../assets/new.svg) **应用并回退已批准的建议** — 已批准的名称和描述更新将由此扩展写入目录。 Commerce会在每个扩充属性首次更改时记录其原始值，因此回滚始终会恢复您在扩充之前的值，即使已向同一属性应用了多个建议也是如此。

![新](../assets/new.svg) **遵守您的编辑** — 当您在“管理员产品”表单中通过&#x200B;**[!UICONTROL Update Attributes]**&#x200B;或通过导入更改扩充名称或描述时，将保留您的值并将相关建议标记为&#x200B;*已过时*。 在默认范围中所做的更改只会影响继承该值的存储视图。

![新](../assets/new.svg) **建议的只读目录访问权限**—[!DNL Commerce Catalog Agent]可以读取产品、类别、属性集和产品类型数据，以选择要分析的产品。 读取仅返回标记为&#x200B;**[!UICONTROL Used in Product Listing]**&#x200B;的属性，以及可扩充的属性。 它无法更改目录数据。

### 修复和改进功能

![已修复问题](../assets/fix.svg) **重试的应用报告成功** — 如果应用请求在完成之后重试，重试现在将报告应用的更改，而不是报告无更改。 没有什么是两次写的。

![已修复问题](../assets/fix.svg) **只有已批准的服务才能更改目录** — 应用和回滚仅接受来自[!DNL Commerce Catalog Agent]的请求。 以前，接受任何有效的Adobe IMS令牌。 现在，同样的检查也适用于SOAP请求。

![已修复问题](../assets/fix.svg) **更清晰的错误**—Adobe IMS中断现在返回`401`而不是`500`，因此不会针对目录重试请求，并且会拒绝无法识别的Adobe IMS环境，而不是将其视为暂存。

![修复了问题](../assets/fix.svg) **Adobe IMS环境** — 默认情况下，目录扩充现在登录到生产Adobe IMS环境，包括在连接到非生产[!DNL Commerce Services]数据空间的实例上。 以前，这些实例会被发送到暂存环境。

![修复了问题](../assets/fix.svg) **在[!DNL Adobe Brand Visibility]域更改**&#x200B;后登录 — 目录扩充页面现在从`abv.adobe.com`加载，这修复了上一个域开始重定向后的登录循环。

### 已知问题

![已知问题](../assets/bug.svg) **具有完全[!UICONTROL Catalog]访问权限的角色** — 在此版本之前保存的、被授予所有&#x200B;**[!UICONTROL Catalog]**&#x200B;的用户角色将保留对&#x200B;**[!UICONTROL Catalog Enrichment Service API]**&#x200B;资源的访问权限。 在&#x200B;**[!UICONTROL System]** > **[!UICONTROL Permissions]** > **[!UICONTROL User Roles]**&#x200B;中查看此类角色，并在不需要时清除该资源。

## 发行版本1.0.2 {#release-1-0-2}

目录扩充管理页面的初始版本。 需要[!DNL Adobe Brand Visibility]扩展才能将建议应用到目录。

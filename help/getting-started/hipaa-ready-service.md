---
title: Adobe Commerce上的HIPAA准备工作
description: 了解如何添加Adobe Commerce HIPAA就绪模块并获得附加功能，使您能够遵守HIPAA义务。
feature: Security, Compliance
exl-id: 4b3eb5b0-4475-47df-92a9-10d12fec1e66
source-git-commit: 7e132d66523feba579baf0bae14e1de9de4d6591
workflow-type: tm+mt
source-wordcount: '1542'
ht-degree: 0%

---

# Adobe Commerce上的HIPAA准备工作

>[!IMPORTANT]
>
>**法律声明**<br/>
>此信息旨在帮助Adobe客户回答他们有关AdobeHIPAA就绪服务的问题。 这不构成法律建议。 商家应该咨询自己的法律顾问，了解他们在HIPAA下的义务以及Adobe产品的正确使用和配置。

>[!BEGINSHADEBOX]

**健康保险流通与责任法案(HIPAA)**

健康保险便携性和责任法案(HIPAA)是美国主要的联邦医疗保健隐私法律，由美国卫生和公众服务部(HHS)执行。 HIPAA适用于 _覆盖的实体_ （如医疗保健提供商、保险商和清算所）和 _商业伙伴_ （如向所涉实体提供服务的实体）。 HIPAA要求通过三个单独的规则进行设置：隐私规则、安全规则和违规通知规则。 Adobe充当某些产品的业务合作伙伴，这些产品被Adobe分类为“HIPAA就绪服务”。 受HIPAA监管的数据称为 _受保护的健康信息_ 或PHI。 PHI是健康信息的子集，即(1)由医疗保健提供商、健康计划或医疗保健清算所创建或接收的健康信息，(2)关于个人的过去、现在或将来身心健康或状况，关于向个人提供医疗的付款，或关于向个人提供医疗保健的过去、现在或将来付款，以及(3)识别个人或有合理依据相信该信息可用于识别个人的健康信息。 《HIPAA隐私和安全规则》要求被覆盖实体以商业伙伴协议（简称BAA）的形式从商业伙伴获得书面保证，要求商业伙伴保护被覆盖实体的PHI的隐私和安全。 有关更多信息，请参阅 [HIPAA和Adobe产品和服务](https://www.adobe.com/trust/compliance/hipaa-ready.html) 在Adobe托管中心。

>[!ENDSHADEBOX]

## Adobe Commerce HIPAA就绪

Adobe Commerce HIPAA-Ready具有附加特性和功能，允许商家遵守各自的HIPAA义务。

Adobe Commerce HIPAA-Ready作为Adobe Commerce扩展提供， `magento/hipaa-ee` 这可用于Adobe Commerce on cloud基础架构或AdobeManaged Services项目。 Adobe Commerce HIPAA就绪安装过程会禁用某些本机服务和功能以符合HIPAA要求。 请参阅 [禁用的服务和功能](#disabled-services-and-features).

*这些资料仅供参考。 提供此信息并不赋予收件人任何合同权利或其他权利。 虽然已努力确保资料在提供之日准确无误，但没有表示资料准确完整。 随着法律或Adobe产品的变化，Adobe不承担更新此信息的义务。 此外，未经Adobe书面同意，不得将此文档分发给目标收件人以外的任何一方。*

## 系统要求

Adobe Commerce必须部署在Adobe Commerce on cloud infrastructure或Adobe Commerce Managed Services的2.4.6-p3或更高版本（无测试版）上。

## 安装

安装最新版本的AdobeHIPAA就绪服务扩展(`magento/hipaa-ee`)在运行Adobe Commerce版本2.4.6-p3或更高版本的实例上。 该扩展将作为编辑器中继从提供。 [repo.magento.com](https://repo.magento.com) 存储库。

>[!BEGINSHADEBOX]

**先决条件**

您必须有权访问 [repo.magento.com](https://repo.magento.com) 以安装扩展。 有关密钥生成和获取必要权限的信息，请参阅 [获取您的身份验证密钥](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html).

>[!ENDSHADEBOX]

1. 在本地工作站上，转到云基础架构项目上Adobe Commerce的项目目录。

   >[!NOTE]
   >
   >有关在本地管理Commerce项目环境的信息，请参阅  [使用CLI管理分支](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/cli-branches) 在 _《云基础架构上的Adobe Commerce用户指南》_.

1. 使用Adobe Commerce Cloud CLI签出要更新的环境分支。

   ```shell
   magento-cloud environment:checkout <environment-id>
   ```

1. 添加中继包 `magento/hipaa-ee` 到使用编辑器CLI的编辑器配置。

   ```shell
   composer require "magento/hipaa-ee" --no-update
   ```

1. 更新包依赖关系。

   ```shell
   composer update "magento/hipaa-ee"
   ```

1. 添加、提交更新的代码并将其推送到云环境。

   ```shell
   git add -A
   git commit -m "Add HIPAA-Ready Services modules"
   git push origin <branch-name>
   ```

   推送更新会启动 [Commerce云部署流程](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/deploy/process) 以应用更改。 从检查部署状态 [部署日志](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/test/log-locations#deploy-log).

### 验证安装

部署更新后，请验证 `Hipaa*` 已安装扩展

1. 使用SSH登录到远程云环境。

   ```shell
   magento-cloud ssh
   ```

1. 在命令行中，使用Adobe Commerce CLI检查模块状态。

   ```shell
   bin/magento module:status
   ```

1. 验证HIPAA模块是否包含在已启用的模块列表中：

   ```text
   List of enabled modules:
   <truncated for brevity>
   Magento_HipaaAnalytics
   Magento_HipaaCheckout
   Magento_HipaaLogging
   Magento_HipaaScheduledImportExport
   Magento_HipaaAdminLogging
   Magento_HipaaCustomerLogging
   Magento_HipaaNewsletter
   Magento_HipaaImportExport
   Magento_HipaaApiLogging
   <truncated for brevity>
   ```

   所有带有前缀的模块 `Magento_Hipaa` 必须在“启用的模块”部分中。

## 针对HIPAA准备工作的功能增强

此 `magento/hipaa-ee` 此包引入了对Commerce基本产品的一些更改和增强。 以下部分提供了有关这些更改以及它们如何更改基本产品的详细信息。

### 操作日志

审核日志记录是HIPAA要求。 在Adobe Commerce中 [操作日志](https://experienceleague.adobe.com/docs/commerce-admin/systems/action-logs/action-log.html?lang=en) 功能会记录您商店中的管理员用户所做的每项更改。 为了满足审核日志的HIPAA要求，已更新该功能，以记录通过管理员UI和API调用执行的所有管理员用户和客户操作。

#### 操作日志报告

此 _操作日志_ 报表网格(**[!UICONTROL System]** >操作日志>报表)进行了修改，以适应客户通过管理员UI和API执行的操作。

1. 添加了两列：
   - ***来源***：显示执行操作的位置。
值： `Admin UI` / `Customer UI` / `REST API` / `SOAP API` / `GraphQL API`
   - ***客户端类型***：显示客户端类型。
值：客户 | 管理员 | 集成

2. 已重命名 ***用户名*** 列至 ***客户端标识符***
   - ***客户端标识符***：显示执行操作的用户的登录ID。
值：
      - 如果Client Type为Customer，则发送电子邮件
      - 如果Client Type为Admin，则为用户名
      - 如果客户端类型为集成，则为名称

3. 已重命名 ***完整操作名称*** 列至 ***Target***
   - ***Target***：显示操作名称。
值：
      - 如果源是REST API或SOAP API，则为端点
      - 查询名或突变名(如果是GraphQL API)
      - 操作名称，如果是Admin UI或客户UI。

#### 配置用于日志记录的管理操作

此功能不可用，因为默认情况下必须记录所有操作。

### 导入和导出特征

对导入和导出功能的增强侧重于改进管理体验以及更好地显示用户操作。

>[!NOTE]
>
>这些 ***增强功能不会更改导入和导出核心逻辑***；而是扩展功能以提供更全面的日志记录和改进的数据归因。 进出口的基本功能保持不变。 用户可以继续使用现有功能和工作流，而不会造成任何中断。

#### 管理操作日志记录

导入和导出功能中的一项关键改进是增强了管理操作的日志记录。 此增强功能引入了更深入探究与数据导入和导出相关的活动的功能，有助于改进跟踪和可审核性。 以下操作现已记录并反映在 **[!UICONTROL System]> _[!UICONTROL Action Logs]_>[!UICONTROL Report]**网格：

| 类型 | 操作 |
| ---- | ------- |
| 导入 | <ul><li>管理员用户执行导入<li>管理员用户下载导入的文件<li>管理员用户下载错误文件<ul/> |
| 导出 | <ul><li>管理员用户请求<li>管理员用户下载导出的文件<ul/> |
| 计划的导入/导出 | <ul><li>管理员用户计划导出<li>管理员用户编辑计划导出<li>管理员用户运行计划的导出<li>管理员用户删除计划的导出<li>管理员用户计划导入<li>管理员用户编辑计划导入<li>管理员用户运行计划导入<li>管理员用户删除计划的导入<li>管理员用户执行导入/导出操作的批量删除<ul/> |

### 显示增强功能以及改进的过滤和排序

为了让管理员用户拥有更多信息网格，HIPAA就绪服务提供了几项增强功能，用于显示、过滤和排序数据。

#### 导入历史记录([!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Import History])

- 已对所有列启用筛选，除以下列外 **[!UICONTROL Imported File]**， **[!UICONTROL Error File]**， **[!UICONTROL Execution Time]**、和 **[!UICONTROL Summary]**.

#### 导出([!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Export])

- 添加了 **[!UICONTROL ID]** 列。
- 添加了 **[!UICONTROL Requested At]** 列(_请求导出的日期和时间_)。
- 添加了 **[!UICONTROL User]** 列(_执行请求的管理员的用户名_)。
- 删除了 **[!UICONTROL Action]** 列。
- 已移动 **[!UICONTROL Download]** 链接到 **[!UICONTROL File name]** 列(_类似“导入历史记录”网格_)。
- 已禁用负责删除导出文件的操作(_改进跟踪_)。
- 为除外的所有列启用排序 **[!UICONTROL File name]**.
- 已为所有列启用筛选。

#### 计划的导入和导出([!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Scheduled Import/Export])

- 添加了 **[!UICONTROL ID]** 列。
- 添加了 **[!UICONTROL Scheduled At]** 列( _计划导入或导出的日期和时间_)。
- 添加了 **[!UICONTROL User]** 列( _计划导入或导出的管理员用户的用户名_)。

## 禁用的服务和功能

为符合HIPAA要求，Adobe Commerce支持的某些服务和功能不可用，或默认处于禁用状态。 商家可以选择重新启用或使用这些服务和功能，但需自行承担风险。

### 服务

- **Adobe Commerce服务** — 在HIPAA就绪性服务中，没有一项Adobe Commerce服务或可扩展性服务可用。 这些服务包括但不限于：

   - 实时搜索
   - API网格
   - App Builder
   - 目录服务

- **[SendGrid服务](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/sendgrid.html)** — 默认情况下禁用此服务，因为应用程序不符合HIPAA。 商家可以提交支持请求来启用Sendgrid，但是他们必须承认他们承担了使用该服务的风险。

### 默认禁用功能

默认情况下，HIPAA就绪模块中禁用以下功能。 商家可以自行承担启用上述任何功能的风险。

- **[来宾结帐](../stores-purchase/checkout-guest.md)** — 此功能给HIPAA的各个方面带来潜在风险，包括日志记录、访问控制、PHI卫生和族系，可能还包括更多方面。

- **[新闻稿功能](../merchandising-promotions/newsletters.md)** — 此功能已禁用，以防止在营销上下文中使用PHI。

- **[高级报告服务设置](../getting-started/business-intelligence.md)** — 禁用此配置设置是为了防止将PHI用于分析和报告。

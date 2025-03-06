---
title: Adobe Commerce上的HIPAA准备工作
description: 了解如何添加 Adobe Commerce HIPAA-Ready 扩展并获取允许您遵守 HIPAA 义务的附加特性和功能。
feature: Security, Compliance
exl-id: 4b3eb5b0-4475-47df-92a9-10d12fec1e66
source-git-commit: 7e18b0b0ea308a6126b6cd35f943b133c75adff3
workflow-type: tm+mt
source-wordcount: '2300'
ht-degree: 1%

---

# Adobe Commerce上的HIPAA准备工作

>[!IMPORTANT]
>
>**法律免责声明**<br/>
>此信息旨在帮助Adobe客户回答他们有关Adobe的HIPAA就绪服务的问题。 这不构成法律建议。 商家应该咨询自己的法律顾问，了解他们在HIPAA下的义务以及Adobe产品的正确使用和配置。

>[!BEGINSHADEBOX]

**健康保险便携性和责任法案(HIPAA)**

健康保险便携性和责任法案(HIPAA)是美国主要的联邦医疗保健隐私法律，由美国卫生和公众服务部(HHS)执行。 HIPAA适用于&#x200B;_覆盖的实体_（如医疗保健提供商、保险公司和清算所）和&#x200B;_商业伙伴_（如向覆盖的实体提供服务的实体）。 HIPAA要求通过三个单独的规则进行设置：隐私规则、安全规则和违规通知规则。 Adobe充当某些产品的业务联系人，Adobe将这些产品归类为“HIPAA就绪服务”。 受HIPAA监管的数据称为&#x200B;_受保护的健康信息_&#x200B;或PHI。 PHI是健康信息的子集，即(1)由医疗保健提供商、健康计划或医疗保健清算所创建或接收的健康信息，(2)关于个人的过去、现在或将来身心健康或状况，关于向个人提供医疗的付款，或关于向个人提供医疗保健的过去、现在或将来付款，以及(3)识别个人或有合理依据相信该信息可用于识别个人的健康信息。 《HIPAA隐私和安全规则》要求被覆盖实体以商业伙伴协议（简称BAA）的形式从商业伙伴获得书面保证，要求商业伙伴保护被覆盖实体的PHI的隐私和安全。 有关详细信息，请参阅Adobe信任中心中的[HIPAA和Adobe产品和服务](https://www.adobe.com/trust/compliance/hipaa-ready.html)。

>[!ENDSHADEBOX]

## Adobe Commerce HIPAA就绪

Adobe Commerce HIPAA就绪扩展为Adobe Commerce安装添加了其他特性和功能，使商家能够遵守各自的HIPAA义务。

Adobe Commerce HIPAA就绪扩展`magento/hipaa-ee`可用于Adobe Commerce on Cloud Infrastructure或Adobe Managed Services项目。 Adobe Commerce HIPAA就绪安装过程会禁用某些本机服务和功能以符合HIPAA要求。 请参阅[已禁用的服务和功能](#disabled-services-and-features)。

>[!NOTE]
>
>仅已购买Adobe Commerce的医疗保健附加组件的商家方可访问符合HIPAA要求的特性和功能。

*这些资料仅供参考。 提供此信息并不赋予收件人任何合同权利或其他权利。 虽然已努力确保资料在提供之日准确无误，但没有表示资料准确完整。 随着法律或Adobe产品的变更，Adobe不承担更新此信息的义务。 此外，未经Adobe书面同意，不得将此文档分发给目标收件人以外的任何一方。*

## 系统要求

Adobe Commerce必须部署在Adobe Commerce on cloud infrastructure或Adobe Commerce Managed Services的2.4.6-p3 - 2.4.6-p8版本（无测试版）上。

## 安装

**预修课程**

>[!BEGINSHADEBOX]

- Adobe已配置您的Adobe Commerce帐户以访问HIPAA Ready扩展。
- 访问[repo.magento.com](https://repo.magento.com)以安装扩展。 有关密钥生成和获取必要的权限，请参阅[获取您的身份验证密钥](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html)。

>[!ENDSHADEBOX]

在运行Adobe 2.4.6-p3 - 2.4.6-p8版的实例上安装最新版本的Adobe Commerce HIPAA-Ready Services扩展(`magento/hipaa-ee`)。 该扩展是作为[repo.magento.com](https://repo.magento.com)存储库中的编辑器中继包提供的。 该元包包括为Adobe Commerce实例启用HIPAA功能的模块集合。

>[!NOTE]
>
>要确保发送到Experience Platform的后台事件数据已可使用HIPAA，请参阅[数据连接扩展指南](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/fundamentals/install#install-the-data-services-hipaa-extension)。

1. 在本地工作站上，转到云基础架构项目上Adobe Commerce的项目目录。

   >[!NOTE]
   >
   >有关在本地管理Commerce项目环境的信息，请参阅《云基础架构用户指南》_上的_ Adobe Commerce中的[使用CLI管理分支](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/cli-branches)。

1. 使用Adobe Commerce Cloud CLI签出要更新的环境分支。

   ```shell
   magento-cloud environment:checkout <environment-id>
   ```

1. 使用编辑器CLI将中继包`magento/hipaa-ee`添加到编辑器配置中。

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

   推送更新将启动[Commerce云部署流程](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/deploy/process)以应用更改。 从[部署日志](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/test/log-locations#deploy-log)中检查部署状态。

### 验证安装

部署更新后，验证是否已安装`Hipaa*`扩展

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
   Magento_HipaaSales
   Magento_HipaaCustomer
   <truncated for brevity>
   ```

   以`Magento_Hipaa`为前缀的所有模块都必须在“启用的模块”部分中。

## 针对HIPAA准备工作的功能增强

`magento/hipaa-ee`扩展引入了对基本Commerce产品的一些更改和增强。 以下部分提供了有关这些更改以及它们如何更改基本产品的详细信息。

### 操作日志

审核日志记录是HIPAA要求。 在Adobe Commerce中，[操作日志](../../systems/action-log.md)功能会记录您的商店中工作的管理员用户所做的每项更改。 为了满足审核日志的HIPAA要求，已更新该功能，以记录通过管理员UI和API调用执行的所有管理员用户和客户操作。

在Adobe服务访问您的存储数据时，操作日志还会捕获事件。 您可以通过筛选“Action Logs”报表中的“Data Sent Outside”操作来确定这些事件。

#### 操作日志报告

已修改&#x200B;_操作日志_&#x200B;报表网格（**[!UICONTROL System]** >操作日志>报表），以适应客户通过管理员UI和API执行的操作。

1. 添加了两列：
   - ***Source***：显示执行操作的位置。
值： `Admin UI` / `Customer UI` / `REST API` / `SOAP API` / `GraphQL API`
   - ***客户端类型***：显示客户端类型。
值：客户 | 管理员 | 集成

2. 已将&#x200B;***用户名***&#x200B;列重命名为&#x200B;***客户端标识符***
   - ***客户端标识符***：显示执行操作的用户的登录ID。
值：
      - 如果Client Type为Customer，则发送电子邮件
      - 如果Client Type为Admin，则为用户名
      - 如果客户端类型为集成，则为名称

3. 已将&#x200B;***完整操作名称***&#x200B;列重命名为&#x200B;***目标***
   - ***目标***：显示操作名称。
值：
      - 如果Source是REST API或SOAP API，则为端点
      - 查询名或突变名(如果是GraphQL API)
      - 操作名称，如果是Admin UI或客户UI。

#### 配置用于日志记录的管理操作

此功能不可用，因为默认情况下必须记录所有操作。

### HIPAA客户搜索结果限制

Adobe Commerce中的HIPAA客户搜索结果限制功能通过限制对受保护的健康信息(PHI)和个人身份信息(PII)的访问，确保符合HIPAA法规。 此功能限制根据用户角色搜索和查看客户记录的能力，确保只有授权用户才能访问此信息。

#### 主要功能

- **搜索限制**：没有必要角色的用户无法搜索或查看客户记录。
- **必须搜索访问**：与默认的Adobe Commerce行为不同，不执行搜索就无法查看客户信息。 这可确保用户必须了解客户的特定详细信息才能找到其信息。
- **有限的搜索结果**：符合条件的搜索结果限制为10条记录，以确保一次只显示可管理的记录数。
- **最小筛选器数**：用户必须至少应用三个筛选器（例如，电子邮件、姓名和状态）才能执行搜索，确保搜索是特定和有针对性的。
- **筛选通知**：启用搜索限制时，将通知用户应用筛选条件以优化其搜索结果。

#### 配置

用于限制搜索结果中客户数量的配置位于&#x200B;**[!UICONTROL Stores]** > **[!UICONTROL Configuration]** > **[!UICONTROL Advanced]** > **[!UICONTROL Admin]** > **[!UICONTROL Admin Grids]**&#x200B;下的管理面板中。 安装`hipaa-ee`扩展时，默认启用此配置。

- **限制网格中的客户数**：此设置允许您启用或禁用对网格搜索结果中显示的客户数的限制。
- **客户网格搜索结果限制**：此设置指定可在网格搜索结果中显示的最大客户记录数。

#### 受影响的功能区域

“管理员创建订单”页面(**[!UICONTROL Sales]** > **[!UICONTROL Orders]** > **[!UICONTROL Create New Order]**)和“客户”页面(**[!UICONTROL Customers]** > **[!UICONTROL All Customers]**)上的客户网格受搜索结果限制功能的影响。

- 默认情况下，将打开过滤器。
- 用户必须应用至少三个过滤器才能执行搜索。
- 默认情况下，搜索结果限制为10条记录。
- 如果有更多记录与搜索条件匹配，则通知将通知用户结果限制以及优化搜索的需要。
- 网格分页不可用。
- 导航离开页面时，不会保存应用的先前搜索结果和过滤器。

搜索结果限制功能也应用于用于客户搜索(`/V1/customers/search`)的REST API。

- 如果未应用过滤器或过滤器不足，API会返回一条错误消息，指示执行搜索需要一定数量的过滤器。
- 当授权用户应用了足够的过滤器时，API会返回指定限制内的结果。
- 当结果有限时，将向响应添加一条消息，指示找到的记录总数和当前应用的限制。

### 导入和导出特征

对导入和导出功能的增强侧重于改进管理体验以及更好地显示用户操作。

>[!NOTE]
>
>这些&#x200B;***增强不会更改导入和导出核心逻辑***；而是扩展了功能以提供更全面的日志记录和改进的数据归因。 进出口的基本功能保持不变。 用户可以继续使用现有功能和工作流，而不会造成任何中断。

#### 管理操作日志记录

导入和导出功能中的一项关键改进是增强了管理操作的日志记录。 此增强功能引入了更深入探究与数据导入和导出相关的活动的功能，有助于改进跟踪和可审核性。 以下操作现已记录并反映在&#x200B;**[!UICONTROL System]> _[!UICONTROL Action Logs]_>[!UICONTROL Report]**网格中：

| 类型 | 操作 |
| ---- | ------- |
| 导入 | <ul><li>管理员用户执行导入<li>管理员用户下载导入的文件<li>管理员用户下载错误文件<ul/> |
| 导出 | <ul><li>管理员用户请求<li>管理员用户下载导出的文件<ul/> |
| 计划的导入/导出 | <ul><li>管理员用户计划导出<li>管理员用户编辑计划导出<li>管理员用户运行计划的导出<li>管理员用户删除计划的导出<li>管理员用户计划导入<li>管理员用户编辑计划导入<li>管理员用户运行计划导入<li>管理员用户删除计划的导入<li>管理员用户执行导入/导出操作的批量删除<ul/> |

### 显示增强功能以及改进的过滤和排序

为了让管理员用户拥有更多信息网格，HIPAA就绪服务提供了几项增强功能，用于显示、过滤和排序数据。

#### 导入历史记录([!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Import History])

- 已为&#x200B;**[!UICONTROL Imported File]**、**[!UICONTROL Error File]**、**[!UICONTROL Execution Time]**&#x200B;和&#x200B;**[!UICONTROL Summary]**&#x200B;以外的所有列启用筛选。

#### 导出([!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Export])

- 添加了&#x200B;**[!UICONTROL ID]**&#x200B;列。
- 添加了&#x200B;**[!UICONTROL Requested At]**&#x200B;列（_请求导出的日期和时间_）。
- 添加了&#x200B;**[!UICONTROL User]**&#x200B;列（_执行请求的管理员的用户名_）。
- 删除了&#x200B;**[!UICONTROL Action]**&#x200B;列。
- 已将&#x200B;**[!UICONTROL Download]**&#x200B;链接移动到&#x200B;**[!UICONTROL File name]**&#x200B;列（_如“导入历史记录”网格_）。
- 已禁用负责删除导出文件的操作（_以改进跟踪_）。
- 已为&#x200B;**[!UICONTROL File name]**&#x200B;以外的所有列启用排序。
- 已为所有列启用筛选。

#### 计划的导入和导出([!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Scheduled Import/Export])

- 添加了&#x200B;**[!UICONTROL ID]**&#x200B;列。
- 添加了&#x200B;**[!UICONTROL Scheduled At]**&#x200B;列（计划导入或导出的&#x200B;_日期和时间_）。
- 添加了&#x200B;**[!UICONTROL User]**&#x200B;列（计划导入或导出的管理员用户的&#x200B;_用户名_）。

## 支持HIPAA的服务和工具

此部分介绍可用于Adobe Commerce的HIPAA产品且支持HIPAA的Adobe服务。 它还介绍了可用于帮助监视存储的关键安全和合规性控制的工具。

| 服务 | 生产 | 暂存 | staging_for_support | 开发 |
|---------------------------------------|------------|---------|---------------------|-------------|
| 带有医疗保健附加组件的Adobe Commerce | 是 | 是 | 是 | 否 |
| 发送网格 | 否 | 否 | 否 | 否 |
| AWS简单电子邮件服务 | 是 | 是 | 是 | 否 |

### Adobe Commerce服务

下表列出了可用于HIPAA就绪型产品的Adobe Commerce服务。 这些服务包括但不限于：

| 服务 | 非生产 | 生产 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------|------------|
| [Adobe Developer App Builder](https://developer.adobe.com/app-builder/docs/overview/) | 是 | 是 |
| 适用于Adobe Developer App Builder的[API网格](https://developer.adobe.com/graphql-mesh-gateway/) | 是 | 是 |
| [SaaS数据导出](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/saas-data-export/overview) | 是 | 是 |
| [实时搜索](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/overview) | 否 | 否 |
| [产品推荐](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/product-recommendations/overview) | 否 | 否 |
| [付款服务](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/payment-services/guide-overview) | 否 | 否 |
| [数据连接后台事件](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice) | 是 | 是 |
| [数据连接店面事件](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#storefront-events) | 否 | 否 |
| [Audience Activation](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/audience-activation) | 否 | 否 |

### 工具

适用于Adobe Commerce的[安全扫描工具](../../systems/security-scan.md)可帮助您监视存储区，以确保所有必需的安全控制均已启用并正常运行。 除了标准安全检查之外，Adobe还增强了该工具，以便为使用Adobe Commerce HIPAA产品的客户显示特定于HIPAA的检查。 安全扫描工具中的HIPAA检查旨在确保：

- 未禁用审核模块
- 未禁用双重身份验证(2FA)
- 营销功能已禁用
- 所有安装的扩展都与预定义的允许列表匹配
- 未安装不支持的Adobe服务

您可以[将工具](../../systems/security-scan.md#run-a-security-scan)配置为通过计划的扫描或[手动查看报告](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/launch/overview#to-review-the-report)向您发送电子邮件通知，其中包含详细信息。

## 禁用的功能

为符合HIPAA要求，Adobe Commerce支持的某些功能不可用或默认处于禁用状态。 商家可以选择重新启用或使用这些功能，但需自行承担风险。

默认情况下，HIPAA就绪模块中禁用以下功能。 商家可以自行承担启用上述任何功能的风险。

- **[事务性电子邮件](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/sendgrid.html)** — 默认情况下已禁用SendGrid，因为服务未就绪。 Adobe Commerce提供了一个集成选项，您可以将其用于您自己的[AWS Simple Email Service](https://docs.aws.amazon.com/ses/)帐户。 有关配置详细信息，请联系您的客户技术客户经理或Adobe Commerce支持。

- **[访客签出](../../stores-purchase/checkout-guest.md)** — 此功能对HIPAA的各个方面带来潜在风险，包括日志记录、访问控制、PHI卫生和谱系等等。

- **[新闻稿功能](../../merchandising-promotions/newsletters.md)** — 此功能已禁用，以防止在营销上下文中使用PHI。

- **[高级报告服务设置](../../getting-started/business-intelligence.md)** — 此配置设置已禁用，以防止将PHI用于分析和报告。

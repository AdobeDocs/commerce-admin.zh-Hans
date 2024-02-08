---
title: Adobe Commerce上的HIPAA准备工作
description: 了解如何添加Adobe Commerce HIPAA就绪模块并获得附加功能，使您能够遵守HIPAA义务。
feature: Security, Compliance
exl-id: 4b3eb5b0-4475-47df-92a9-10d12fec1e66
source-git-commit: 3364a07b4c79a60ed813bf669a04711b69dae6f9
workflow-type: tm+mt
source-wordcount: '1443'
ht-degree: 0%

---

# Adobe Commerce上的HIPAA准备工作

>[!IMPORTANT]
>
>**法律声明**<br/>
>此信息旨在帮助Adobe客户回答他们有关AdobeHIPAA就绪服务的问题。 这不构成法律建议。 商家应该咨询自己的法律顾问，了解他们在HIPAA下的义务以及Adobe产品的正确使用和配置。

## 健康保险流通与责任法案(HIPAA)

健康保险便携性和责任法案(HIPAA)是美国主要的联邦医疗保健隐私法律，由美国卫生和公众服务部(HHS)执行。 HIPAA适用于 _覆盖的实体_ （如医疗保健提供商、保险商和清算所）和 _商业伙伴_ （如向所涉实体提供服务的实体）。 HIPAA要求通过三个单独的规则进行设置：隐私规则、安全规则和违规通知规则。 Adobe充当某些产品的业务合作伙伴，这些产品被Adobe分类为“HIPAA就绪服务”。 受HIPAA监管的数据称为 _受保护的健康信息_ 或PHI。 PHI是健康信息的子集，即(1)由医疗保健提供商、健康计划或医疗保健清算所创建或接收的健康信息，(2)关于个人的过去、现在或将来身心健康或状况，关于向个人提供医疗的付款，或关于向个人提供医疗保健的过去、现在或将来付款，以及(3)识别个人或有合理依据相信该信息可用于识别个人的健康信息。 《HIPAA隐私和安全规则》要求被覆盖实体以商业伙伴协议（简称BAA）的形式从商业伙伴获得书面保证，要求商业伙伴保护被覆盖实体的PHI的隐私和安全。

## Adobe Commerce HIPAA就绪

Adobe Commerce HIPAA-Ready具有附加特性和功能，允许商家遵守各自的HIPAA义务。 您可以安装Adobe Commerce HIPAA就绪(`magento/hipaa-ee`)模块添加到您的Adobe Commerce on cloud基础架构中。 还有一些功能必须禁用才能符合HIPAA。

*这些资料仅供参考。 提供此信息并不赋予收件人任何合同权利或其他权利。 虽然已努力确保资料在提供之日准确无误，但并未作出任何声明确保此种资料准确完整，而且Adobe没有义务在法律或Adobe产品变更时增补这些资料。 此外，未经Adobe书面同意，不得将此文档分发给目标收件人以外的任何一方。*

## 系统要求

Adobe Commerce上的HIPAA准备工作具有与Adobe Commerce相同的系统要求，但还有其他要求：

- Adobe Commerce版本2.4.6-p3或更高版本（非测试版）
- 云基础架构上的Adobe Commerce或Managed Services上的Adobe Commerce
- 最新版本的 `magento/hipaa-ee` 扩展

## 安装

从技术上讲，Adobe的HIPAA就绪服务是一个作曲家隐喻 `magento/hipaa-ee` 包含指向特殊模块的链接。 此中继包驻留在存储库中 [repo.magento.com](https://repo.magento.com).

1. 能够安装 `magento/hipaa-ee` 隐含，您必须有权访问它。 有关密钥生成和获取必要权限的信息，请参阅 [获取您的身份验证密钥](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html?lang=en).

1. 检查将在其中安装包的环境，并确保它符合常规要求 [系统要求](#system-requirements).

1. 添加中继包 `magento/hipaa-ee` 到编辑器配置。

   最简单的方法是使用编辑器CLI。 例如：

   ```shell
   composer require magento/hipaa-ee
   ```

1. 如果尚未安装Adobe Commerce，则可以开始安装(按照 [安装说明](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/composer.html?lang=en))。

   如果已安装Adobe Commerce，则在下载模块后，运行 `bin/magento setup:upgrade` 命令，然后遵循建议。

   ```shell
   bin/magento setup:upgrade
   ```

   运行此命令时，将启用新下载的模块，并启动安装这些模块的脚本。 要了解有关模块管理的更多信息，请参阅 [启用或禁用模块](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/manage-modules.html?lang=en).

1. 安装或更新过程完成后，您应检查 `Hipaa*` 还包括了相关模块。

   运行以下命令：

   ```shell
   bin/magento module:status
   ```

   如果正确添加了HIPAA编辑器包，您将在命令输出中看到HIPAA模块。 例如：

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

此 `magento/hipaa-ee` 包引入了基本Commerce产品的一些更改和增强。 以下部分提供了有关这些更改以及它们如何更改基本产品的详细信息。

### 操作日志

审核日志记录是HIPAA要求。 在Adobe Commerce中 [操作日志](https://experienceleague.adobe.com/docs/commerce-admin/systems/action-logs/action-log.html?lang=en) 功能会记录您商店中的管理员用户所做的每项更改。 为了满足有关审核日志的HIPAA要求，对功能进行了更改，以记录通过管理员UI和API调用执行的所有管理员用户和客户操作。

#### 操作日志报告

此 _操作日志_ 报表网格(**[!UICONTROL System]** >操作日志>报表)进行了修改，以适应客户通过管理员UI和API执行的操作。

1. 另外两列：
   - ***来源***：显示执行操作的位置。\
     值： `Admin UI` / `Customer UI` / `REST API` / `SOAP API` / `GraphQL API`
   - ***客户端类型***：显示客户端类型。\
     值：客户 | 管理员 | 集成


2. 重命名 ***用户名*** 到 ***客户端标识符***
   - ***客户端标识符***：显示执行操作的用户的登录ID\
     值：
      - 如果Client Type为Customer，则发送电子邮件
      - 如果Client Type为Admin，则为用户名
      - 如果客户端类型为集成，则为名称

3. 重命名 ***完整操作名称*** 到 ***Target***
   - ***Target***：显示操作名称\
     值：
      - 如果源是REST API或SOAP API，则为端点
      - 查询/突变名称(如果GraphQL API)
      - 管理员UI或客户UI中的操作名称。

#### 配置用于日志记录的管理操作

此功能不可用，因为默认情况下必须记录所有操作。

### 导入/导出功能

对导入/导出功能的增强侧重于改进管理体验以及更好地显示用户操作。

>[!NOTE]
>
>这些 ***增强功能不会更改导入/导出核心逻辑***；而是扩展功能以提供更全面的日志记录和改进的数据归因。 进口/出口的基本功能保持不变。 用户可以继续使用现有功能和工作流，而不会造成任何中断。

#### 管理操作日志记录

导入/导出功能中的一项关键改进是增强了管理操作的日志记录。 这引入了深入挖掘与数据导入/导出相关的活动的功能，有助于改进跟踪和可审计性。 以下操作现已记录并反映在 **[!UICONTROL System]> _[!UICONTROL Action Logs]_>[!UICONTROL Report]**网格：

| 类型 | 操作 |
| ---- | ------- |
| 导入 | <ul><li>管理员用户执行导入<li>管理员用户下载导入的文件<li>管理员用户下载错误文件<ul/> |
| 导出 | <ul><li>管理员用户请求<li>管理员用户下载导出的文件<ul/> |
| 计划的导入/导出 | <ul><li>管理员用户计划导出<li>管理员用户编辑计划导出<li>管理员用户运行计划的导出<li>管理员用户删除计划的导出<li>管理员用户计划导入<li>管理员用户编辑计划导入<li>管理员用户运行计划导入<li>管理员用户删除计划的导入<li>管理员用户执行导入/导出操作的批量删除<ul/> |

### 显示增强功能和改进的筛选/排序

为了让管理员用户拥有更多信息网格，在数据的显示以及筛选和排序功能方面进行了一些增强：

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

#### 计划的导入/导出([!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Scheduled Import/Export])

- 添加了 **[!UICONTROL ID]** 列。
- 添加了 **[!UICONTROL Scheduled At]** 列(_计划导入或导出的日期和时间_)。
- 添加了 **[!UICONTROL User]** 列(_计划导入/导出的管理员用户的用户名_)。

## 禁用了HIPAA准备功能

### SaaS服务

为Adobe Commerce提供的SaaS服务均不提供HIPAA就绪服务。 这包括但不限于：

- 实时搜索
- API网格
- App Builder
- 目录服务

### 默认情况下禁用来宾签出

- 访客结账会给HIPAA的各个方面带来潜在风险，包括日志记录、访问控制、PHI卫生和血统以及潜在的更多信息。
- 在HIPAA就绪模块中，默认情况下会禁用访客签出，但可以自行承担风险启用我的商家。

### 默认情况下已禁用新闻稿功能

- 默认情况下，新闻稿功能处于禁用状态，以防止在营销上下文中使用PHI，但商家可以自行承担启用该功能的风险。

### 默认情况下禁用了高级报告服务设置

默认情况下，“高级报告”服务设置处于禁用状态，以防止将PHI用于分析和报告，但商家可以自行承担启用该设置的风险。

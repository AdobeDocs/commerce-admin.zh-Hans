---
title: 将媒体文件迁移到AEM
description: 将媒体文件从Adobe Commerce或外部源迁移到AEM Assets DAM。
feature: CMS, Media, Integration
source-git-commit: 094c585b335e5751a1387989d5ba33332c351c57
workflow-type: tm+mt
source-wordcount: '769'
ht-degree: 0%

---

# 将媒体文件迁移到AEM Assets DAM

Adobe Commerce和Adobe Experience Manager (AEM)均提供内置功能，以简化从Commerce到AEM Assets数字资产管理系统(DAM)的媒体文件迁移。 您还可以从其他源迁移介质文件。

## 先决条件

| 类别 | 要求 |
|----------|-------------|
| **系统要求** | <ul><li>使用AEM Assets配置的AEM as a Cloud Service环境</li><li>足够的存储容量</li><li>用于大型文件传输的网络带宽</li></ul> |
| **所需的访问和权限** | <ul><li>AEM Assets as a Cloud Service的管理员访问权限</li><li>访问存储介质文件的源系统(Adobe Commerce或外部系统)</li><li>访问云存储服务的适当权限</li></ul> |
| **云存储帐户** | <ul><li>AWS S3或Azure Blob Storage帐户</li><li>专用容器/存储段配置</li><li>身份验证凭据</li></ul> |
| **Source内容** | <ul><li>准备好迁移的有组织的媒体文件</li><li>AEM Assets</a>支持的<a href="https://experienceleague.adobe.com/zh-hans/docs/experience-manager-cloud-service/content/assets/file-format-support#image-formats">格式的图像和视频文件。</li><li>干净的重复资产</li></li> |
| **元数据准备** | <ul><li>为AEM Assets资源配置的<a href="https://experienceleague.adobe.com/zh-hans/docs/commerce-admin/content-design/aem-asset-management/getting-started/aem-assets-configure-aem">Commerce元数据配置文件</a></li><li>每个资源的映射元数据值</li><li>CSV文件编辑器(例如Microsoft Excel)</li></ul> |

## 迁移最佳实践

1. 在迁移之前，通过删除未使用和重复的内容来策划资源。
1. 按大小、格式或用例以逻辑方式组织资源。
1. 考虑将大型迁移分解为较小的批次。
1. 在非高峰时间安排资源密集型导入。
1. 在完全导入之前验证元数据映射。

## 迁移工作流

按照迁移工作流从Adobe Commerce或其他外部系统导出媒体文件，并将它们导入AEM Assets DAM。

### 步骤1：从现有数据源导出内容

对于Adobe Commerce商家，“远程存储”模块提供了一种简化的方式，可让您从Commerce导出媒体文件并将其导入AEM Assets。 本模块使您能够在AWS S3等远程存储服务上存储和管理媒体文件，从而使迁移过程更加高效。 要为Commerce实例设置远程存储，请参阅&#x200B;*Commerce配置指南*&#x200B;中的[配置远程存储](https://experienceleague.adobe.com/zh-hans/docs/commerce-operations/configuration-guide/storage/remote-storage/remote-storage-aws-s3)。

如果您的媒体文件存储在Adobe Commerce外部，请将其直接上传到AEM as a Cloud Service支持的[数据源](https://experienceleague.adobe.com/zh-hans/docs/experience-manager-cloud-service/content/assets/assets-view/bulk-import-assets-view#prerequisites)之一。

### 步骤2：构建用于元数据映射的CSV文件

创建CSV格式的元数据映射文件，并将其上传到包含媒体文件的源文件夹。 此文件将基本元数据映射到每个资源，以便：

- 在DAM中组织和分类资产以方便发现
- 在Adobe Commerce和AEM Assets之间启用正确同步
- 迁移后维护资产和产品之间的关系

对于您计划迁移的每个媒体文件，请为Commerce资源的[AEM Assets元数据配置文件](aem-assets-configure-aem.md)中包含的元数据字段提供值，如下表所述。

| 元数据 | 描述 | 值 |
|-------|-------------|--------|
| 资产路径 | 资产存储在AEM Assets存储库中的完整路径。<br><br>使用路径创建子文件夹以整理Commerce资源，例如`content/dam/commerce/<brand>/<type>`。 | `/content/dam/commerce/<sub-folder>/..<filename>` |
| dc：title | AEM Assets中资源的显示标题 | 字符串值（例如，`Sample 1`） |
| dam：status | AEM Assets中资源的审批状态 | `approved` |
| commerce：positions | 资产在产品库中的位置/顺序 | 数值（例如，“1”） |
| commerce：isCommerce | 指示资产是否用于商业的标记 | `Yes` |
| commerce：skus | 与此资产关联的产品SKU | 字符串值（例如，`sample1`） |
| commerce：roles | 资产的角色或图像类型（例如，`thumbnail`、`main image`、`swatch`） | 多个值以分号分隔（例如，“thumbnail； image； swatch_image； small_image”） |

+++CSV代码

使用此示例CSV代码在代码编辑器或电子表格应用程序(如Microsoft Excel)中创建文件。

```csv
assetPath,dc:title{{String}},dam:status{{String}},commerce:positions{{String: multi}},commerce:isCommerce{{String}},commerce:skus{{String: multi}},commerce:roles{{String: multi}}
/content/dam/commerce/sample1.jpg,Sample 1,approved,1,Yes,sample1,thumbnail; image; swatch_image; small_image
/content/dam/commerce/sample2.jpg,Sample 2,approved,1,Yes,sample2,thumbnail; image; swatch_image; small_image
/content/dam/commerce/sample3.jpg,Sample 3,approved,1,Yes,sample3,thumbnail; image; swatch_image; small_image
```

+++

### 步骤3：将Assets批量导入AEM Assets

创建元数据映射文件后，请使用AEM Assets批量导入工具来导入您的资源。

以下是使用该工具的高级概述。

1. [登录到您的AEM Assets as a Cloud Service创作环境](https://experienceleague.adobe.com/zh-hans/docs/experience-manager-cloud-service/content/onboarding/journey/aem-users#login-aem)。

1. 从“Experience Manager工具”视图中，选择&#x200B;**[!UICONTROL Assets]** > **[!UICONTROL Bulk Import]**。

   ![AEM Assets创作](./assets/aem-assets-bulk-import-selection.png){width="600" zoomable="yes"}

1. 在批量导入配置中，选择&#x200B;**[!UICONTROL Create]**&#x200B;以打开配置表单。

   ![AEM Assets创作](./assets/aem-assets-bulk-import-configuration.png){width="600" zoomable="yes"}

1. 设置并保存配置。

   您将需要：

   - 数据源的身份验证凭据
   - AEM Assets中将存储导入文件的目标文件夹
   - 有关MIME类型、文件大小和其他参数的信息，以自定义导入配置（可选）
   - 您上传到云存储实例的元数据映射CSV文件的路径。

   有关详细步骤，请参阅&#x200B;*AEM Assets as a Cloud Service用户指南*&#x200B;中的[配置批量导入工具](https://experienceleague.adobe.com/zh-hans/docs/experience-manager-cloud-service/content/assets/manage/add-assets#configure-bulk-ingestor-tool)。

1. 保存配置后，使用批量导入工具测试和运行导入操作。

>[!MORELIKETHIS]
>
>[批量导入工具视频演示](https://experienceleague.adobe.com/zh-hans/docs/experience-manager-cloud-service/content/assets/manage/add-assets#asset-bulk-ingestor)
>[提示、最佳实践和限制](https://experienceleague.adobe.com/zh-hans/docs/experience-manager-cloud-service/content/assets/manage/add-assets#tips-limitations)
>[使用API上载或引入资源](https://experienceleague.adobe.com/zh-hans/docs/experience-manager-cloud-service/content/assets/admin/developer-reference-material-apis#asset-upload)


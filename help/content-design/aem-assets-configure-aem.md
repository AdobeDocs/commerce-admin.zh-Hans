---
title: 配置Experience Manager Assets
description: 添加启用Commerce的AEM Assets集成所需的资源元数据，以便在Adobe Commerce和Experience Manager Assets项目之间同步资源。
feature: CMS, Media, Integration
exl-id: deb7c12c-5951-4491-a2bc-542e993f1f84
source-git-commit: 6b0c8054e86ae697025626ad2eb575d633003578
workflow-type: tm+mt
source-wordcount: '668'
ht-degree: 0%

---

# 配置Experience Manager Assets

通过更新环境配置并配置AEM as a Cloud Service元数据来标识和管理Commerce资源，从而准备Assets环境以管理Commerce资源。

集成需要添加自定义`Commerce`命名空间以及其他[配置文件元数据](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/manage/metadata-profiles)和[架构元数据](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/manage/metadata-schemas)。

Adobe提供了一个AEM项目模板，用于将命名空间和元数据架构资源添加到AEM Assetsas a Cloud Service环境配置。 该模板添加了：

- [自定义命名空间](https://github.com/ankumalh/assets-commerce/blob/main/ui.config/jcr_root/apps/commerce/config/org.apache.sling.jcr.repoinit.RepositoryInitializer~commerce-namespaces.cfg.json)，`Commerce`用于标识与Commerce相关的属性。

- 带有标签`Does it exist in Commerce?`的自定义元数据类型`commerce:isCommerce`用于标记与Adobe Commerce项目关联的Commerce资源。

- 用于添加&#x200B;*[!UICONTROL Product Data]*&#x200B;属性的自定义元数据类型`commerce:productmetadata`和相应的UI组件。 产品数据包括元数据属性，用于将Commerce资源与产品SKU关联，以及指定资源的图像`role`和`position`属性。

  ![自定义产品数据UI控件](./assets/aem-commerce-sku-metadata-fields-from-template.png){width="600" zoomable="yes"}

- 具有Commerce选项卡的元数据架构表单，包括用于标记Commerce资源的`Does it exist in Adobe Commerce?`和`Product Data`字段。 该表单还提供了在AEM Assets UI中显示或隐藏`roles`和`order`（位置）字段的选项。

  AEM Assets元数据架构表单的![Commerce选项卡](./assets/assets-configure-metadata-schema-form-editor.png){width="600" zoomable="yes"}

- [示例已标记并批准Commerce资源](https://github.com/ankumalh/assets-commerce/blob/main/ui.content/src/main/content/jcr_root/content/dam/wknd/en/activities/hiking/equipment_6.jpg/.content.xml) `equipment_6.jpg`以支持初始资源同步。 只有已获批准的Commerce资源才能从AEM Assets同步到Adobe Commerce。

有关Commerce-Assets AEM项目的更多信息，请参阅[自述文件](https://github.com/ankumalh/assets-commerce)。

## 自定义AEM Assets环境配置

>[!BEGINSHADEBOX]

**先决条件**

- [使用计划和部署管理员角色访问AEM Assets Cloud Manager计划和环境](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/onboarding/journey/cloud-manager#access-sysadmin-bo)。

- [本地AEM开发环境](https://experienceleague.adobe.com/en/docs/experience-manager-learn/cloud-service/local-development-environment-set-up/overview)，熟悉AEM本地开发过程。

- 了解[AEM项目结构](https://experienceleague.adobe.com/zh-hans/docs/experience-manager-cloud-service/content/implementing/developing/aem-project-content-package-structure)以及如何使用Cloud Manager部署自定义内容包。

>[!ENDSHADEBOX]

### 将Commerce-Assets AEM项目部署到AEM Assets创作环境

1. 如果需要，可在Cloud Manager中为AEM Assets项目创建生产和暂存环境。

1. 根据需要配置部署管道。

1. 从GitHub中，从[Commerce-Assets AEM项目](https://github.com/ankumalh/assets-commerce)下载样板代码。

1. 从您的[本地AEM开发环境](https://experienceleague.adobe.com/en/docs/experience-manager-learn/cloud-service/local-development-environment-set-up/overview)，将自定义代码作为Maven包安装到AEM Assets环境配置中，或通过将代码手动复制到现有项目配置中。

1. 提交更改并将本地开发分支推送到Cloud Manager Git存储库。

1. 从Cloud Manager [部署您的代码以更新AEM环境](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/using-cloud-manager/deploy-code#deploying-code-with-cloud-manager)。

## 配置元数据配置文件

通过创建元数据配置文件，设置Commerce资源元数据的默认值。 设置后，将此配置文件应用到AEM Asset文件夹以自动使用这些默认值。 此可选设置可减少手动步骤，从而帮助简化资产处理。

1. 在Adobe Experience Manager工作区中，单击Adobe Experience Manager图标以转到为AEM Assets创作内容管理工作区。

   ![AEM Assets创作](./assets/aem-assets-authoring.png){width="600" zoomable="yes"}

1. 通过选择锤子图标打开管理员工具。

   ![AEM作者管理员管理元数据配置文件](./assets/aem-manage-metadata-profiles.png){width="600" zoomable="yes"}

1. 通过单击&#x200B;**[!UICONTROL Metadata Profiles]**&#x200B;打开配置文件配置页面。

1. **[!UICONTROL Create]** Commerce集成的元数据配置文件。

   ![AEM作者管理员添加元数据配置文件](./assets/aem-create-metadata-profile.png){width="600" zoomable="yes"}

1. 为Commerce元数据添加选项卡。

   1. 单击左侧的&#x200B;**[!UICONTROL Settings]**。

   1. 在选项卡部分中单击&#x200B;**[!UICONTROL +]**，然后指定&#x200B;**[!UICONTROL Tab Name]**、`Commerce`。

1. 将`Does it exist in Commerce?`字段添加到表单，并将默认值设置为`yes`。

   ![AEM作者管理员将元数据字段添加到配置文件](./assets/aem-edit-metadata-profile-fields.png){width="600" zoomable="yes"}

1. 保存更新。

1. 将`Commerce integration`元数据配置文件应用到存储Commerce资源的文件夹。

   1. 从[!UICONTROL  Metadata Profiles]页面中，选择Commerce集成配置文件。

   1. 从操作菜单中选择&#x200B;**[!UICONTROL Apply Metadata Profiles to Folder(s)]**。

   1. 选择包含Commerce资源的文件夹。

      创建不存在的Commerce文件夹。

   1. 单击&#x200B;**[!UICONTROL Apply]**。

>[!TIP]
>
>您可以通过更新元数据配置文件将&#x200B;_[!UICONTROL Review Status]_字段的默认值设置为`Approved`，在上传到Commerce环境时自动同步AEM Assets资源。 `Review Status`字段的属性类型为`./jcr:content/metadata/dam:status`。


## 后续步骤

更新AEM环境后，设置Adobe Commerce：

1. [安装和配置适用于Commerce的AEM Assets集成](aem-assets-configure-commerce.md)
2. [启用资源同步以在Adobe Commerce项目环境和AEM Assets项目环境之间传输资源](aem-assets-setup-synchronization.md)

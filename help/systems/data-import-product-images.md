---
title: 产品图像导入
description: 了解如何使用每个映像的路径和文件名导入产品映像。
exl-id: 991550e6-9ce2-4472-becb-3492bd4c9582
feature: Products, Data Import/Export, Media
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '835'
ht-degree: 0%

---

# 产品图像导入

每种类型的多个产品图像都可以导入到Adobe Commerce和Magento Open Source中，并与特定产品关联。 在CSV文件中输入每个产品图像的路径和文件名，并将要导入的图像文件上传到Commerce服务器或外部服务器上的相应路径。

Commerce为按字母顺序组织的产品图像创建自己的目录结构。 将产品数据与现有图像导出到CSV文件时，您可以在每个图像的文件名之前看到按字母顺序排列的路径。 但是，在导入新图像时，您无需指定路径，因为Commerce会自动管理目录结构。 但请确保在要导入的每个映像的文件名之前输入导入目录的相对路径。

要上传图像，您必须拥有登录凭据和正确的权限才能访问服务器上的Commerce文件夹。 使用正确的凭据，您可以使用任何SFTP实用程序将文件从台式计算机上传到服务器。

在尝试导入许多图像之前，请查看导入方法中要使用的步骤，并使用一些产品完成整个过程。 了解了它的工作原理后，您就会对导入大量图像充满信心。

>[!IMPORTANT]
>
>建议您使用支持UTF-8编码的程序来编辑CSV文件，例如Notepad++。 Microsoft® Excel在CSV文件的列标题中插入其他字符，这会阻止数据导入回Commerce。

## 方法1：从本地服务器导入图像

1. 在Commerce服务器上，将图像文件上传到 `var/import/images` 文件夹或子文件夹，如 `var/import/images/product_images`. 这是用于导入产品映像的默认根文件夹。

   ```terminal
   <Magento root folder>/var/import/images
   ```

   >[!NOTE]
   >
   Adobe Commerce和Magento Open Source入门 `2.3.2` 发行版，中指定的 **[!UICONTROL Images File Directory]** 连接以导入到图像基目录 —  `<Magento-root-folder>/var/import/images`. 对于早期的Adobe Commerce和Magento Open Source版本，您可以在商务服务器上使用其他文件夹，但前提是在导入过程中指定了该文件夹的路径。

1. 在CSV数据中，输入要导入到正确行上的每个图像文件的名称，方法为 `sku`，并根据图像类型(`base_image`， `small_image`， `thumbnail_image`，或 `additional_images`)。

   >[!NOTE]
   >
   对于默认导入文件夹中的图像(`var/import/images`)，在CSV数据中不要在文件名之前包含路径。

   CSV文件必须仅包含 `sku` 列和相关图像列。

   ![示例 — CSV图像数据导入](./assets/data-import-csv-image-files-default-local.png){width="600" zoomable="yes"}

1. 按照说明进行操作，以 [导入](data-import.md) 数据。

1. 选择要导入的文件后，输入以下相对路径 **[!UICONTROL Images File Directory]**.

   ```terminal
   var/import/images
   ```

   ![数据导入图像文件目录](./assets/data-import-file-to-import.png){width="600" zoomable="yes"}

   >[!TIP]
   >
   离开 _[!UICONTROL Images File Directory]_留空以使用 `<Magento-root-folder>/var/import/images` 目录。 从Adobe Commerce和Magento Open Source版本2.3.2开始，这是默认的导入图像基目录。

   如果为单个导入多个图像 `sku`，将图像插入名为的列中 `additional_images` （添加列，如果尚未添加），用逗号分隔。 示例： `image02.jpg,image03.jpg`

## 方法2：从外部服务器导入图像

1. 上传要导入到外部服务器上的指定文件夹中的图像。

1. 在CSV数据中，按图像类型(`base_image`， `small_image`， `thumbnail_image`，或 `additional_images`)。

   ```terminal
   https://example.com/images/image.jpg
   ```

1. 按照说明进行操作，以 [导入](data-import.md) 数据。

## 方法3：使用远程存储导入映像

1. 在远程存储模块中，将映像文件上传到 `var/import/images` 文件夹或子文件夹，如 `var/import/images/product_images`. 这是用于导入产品映像的默认根文件夹。

   ```terminal
   <remote-storage-root-folder>/var/import/images
   ```

   >[!NOTE]
   >
   Adobe Commerce和Magento Open Source入门 `2.3.2` 发行版，中指定的 _[!UICONTROL Images File Directory]_连接以导入到图像基目录： `<remote-storage-root-folder>/var/import/images`. 对于早期的Adobe Commerce和Magento Open Source版本，您可以在导入过程中使用Commerce服务器上的其他文件夹，前提是指定了该文件夹的路径。

1. 在CSV数据中，输入要导入到正确行上的每个图像文件的名称，方法为 `sku`，并根据图像类型(`base_image`， `small_image`， `thumbnail_image`，或 `additional_images`)。

   >[!NOTE]
   >
   对于默认导入文件夹中的图像(`var/import/images`)，在CSV数据中不要在文件名之前包含路径。

   CSV文件必须仅包含 `sku` 列和相关图像列。

   ![示例 — CSV图像数据导入](./assets/data-import-csv-image-files-default-local.png){width="600" zoomable="yes"}

1. 按照说明进行操作，以 [导入](data-import.md) 数据。

1. 选择要导入的文件后，输入以下相对路径 **[!UICONTROL Images File Directory]**.

   ```terminal
   var/import/images/product_images
   ```

   >[!TIP]
   >
   离开 _[!UICONTROL Images File Directory]_留空以使用 `<Magento-root-folder>/var/import/images` 目录。 从Adobe Commerce和Magento Open Source版本2.3.2开始，这是默认的导入图像基目录。

   如果为单个导入多个图像 `sku`，将图像插入名为的列中 `additional_images` (添加列（如果尚未添加），用逗号分隔： `image02.jpg,image03.jpg`

有关启用和管理远程存储模块的详细信息，请参见 [配置远程存储](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/storage/remote-storage/remote-storage.html) 在 _配置指南_.

>[!NOTE]
>
导入产品图像不会启动图像大小调整。 产品图像的前端大小调整方式 `pub/get.php`. 确保您的 `pub/get.php` 工作正常；否则，可能无法调整图像大小。

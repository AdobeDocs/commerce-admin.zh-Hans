---
title: 导入可下载的产品
description: 查看为可下载产品导入产品数据的示例。
exl-id: e0b45ef5-dff1-4ee4-aa7e-2407162669fd
feature: Products, Data Import/Export
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 0%

---

# 导入可下载的产品

用于导入可下载产品的流程与用于的相同 [捆绑产品](data-transfer-bundle-products.md) 或 [可配置产品](data-transfer-configurable-products.md). 不同之处在于，可下载产品具有 [可下载的链接](../catalog/product-create-downloadable.md) 和 [可下载的样本](../catalog/product-create-downloadable.md) 和它的图像。

可下载链接和示例的默认根目录为 `<Magento-root-folder>/pub/media/import`. 如果启用了远程存储模块，可下载链接和示例的默认根目录为 `<remote-storage-root-folder>/media/import` 目录。

CSV文件具有单独的列 `downloadable_links` 和 `downloadable_samples`.

- **可下载的链接图像**  — 在以下示例中，可下载的链接图像(`red.jpg` 和 `black.jpg`)在 `<Magento-root-folder>/pub/media/import/test` 文件夹。 如果启用了远程存储，则这些映像位于 `<remote-storage-root-folder>/media/import/test` 文件夹。

  ![示例数据 — 带有可下载链接的可下载产品](./assets/data-import-downloadable-links.png){width="600" zoomable="yes"}

- **可下载的示例图像**  — 在以下示例中，可下载的示例图像(`white.jpg`)在 `<Magento-root-folder>/pub/media/import/test` 文件夹。 如果启用了远程存储，则此映像位于 `<remote-storage-root-folder>/media/import/test` 文件夹。

  ![示例数据 — 带有可下载示例的可下载产品](./assets/data-import-downloadable-samples.png){width="400" zoomable="yes"}

有关启用和管理远程存储模块的详细信息，请参见 [配置远程存储](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/storage/remote-storage/remote-storage.html) 在 _配置指南_.

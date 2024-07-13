---
title: 导入捆绑包产品
description: 查看为捆绑产品导入产品数据的示例。
exl-id: 52146979-9911-449b-9f14-54377e2ae9f4
feature: Products, Data Import/Export
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '628'
ht-degree: 0%

---

# 导入捆绑包产品

捆绑产品会显示一系列项目，并允许客户选择他们希望购买的项目。 构成捆绑包的所有项都以[简单产品](../catalog/product-create-simple.md)或[虚拟产品](../catalog/product-create-virtual.md)的形式存在于目录中。 通常，从管理员创建和更新捆绑包产品。 但是，也可以导入数据以创建捆绑产品，或者导出现有的捆绑产品、编辑数据并将它们导入回目录中。 Sprite Yoga Companion Kit是以下示例中使用的示例数据中的捆绑产品。

![捆绑产品](../catalog/assets/product-bundle.png){width="700" zoomable="yes"}

## 更改捆绑项目的顺序

有两种方法可以更改捆绑产品中项目的顺序。

### 方法1：拖放

使用管理员的[捆绑包](../catalog/product-create-bundle.md)产品时，您可以将项和部分拖放到适当位置。

![包项目](../catalog/assets/product-bundle-items-move.png){width="600" zoomable="yes"}

### 方法2：编辑产品数据

了解捆绑产品结构的最佳方法是导出产品并在电子表格中检查数据。 可通过导出产品并向每个项目的数据添加位置参数来更改捆绑项目的顺序。 项目数据位于导出产品的`bundle_values`列中。 在电子表格中打开时，与产品关联的所有项目将作为长文本字符串位于单个单元格中。 `bundle_values`列包含每个项目的以下元素：

- 项目部分的名称
- 输入控件
- 必需的项目指示器
- SKU
- 颜色
- 价格
- 默认选项指示器
- 默认数量
- 价格类型
- 可编辑数量指示器

#### 步骤1：导出捆绑产品

在此步骤中，将Sprite瑜伽伴侣套件导出为([CSV](data-csv.md)文件。 您可以使用目录中的任何其他捆绑包产品。

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Export]**。

1. 在&#x200B;_导出设置_&#x200B;下，将&#x200B;**[!UICONTROL Entity Type]**&#x200B;设置为`Products`。

1. 在产品属性列表中，向下滚动到&#x200B;**[!UICONTROL SKU]**&#x200B;并输入要导出的捆绑产品的SKU。

   在此示例中，产品的SKU为`24-WG080`。

1. 向下滚动到部分的底部，然后单击&#x200B;**[!UICONTROL Continue]**。

1. 在&#x200B;_[!UICONTROL File name]_网格的_[!UICONTROL Action]_&#x200B;列中，单击&#x200B;**[!UICONTROL Select]**&#x200B;并选择`Download`。

   该文件显示在浏览器使用的下载位置。

#### 第2步：编辑数据

1. 在电子表格中打开下载的CSV文件。

1. 滚动到最右侧，直到您看到`bundle_values`列。

   在`bundle_values`数据中，每个元素用逗号分隔，每个包项用竖线与下一个包项分隔。 （最后一个项目未以垂直栏结尾。） 导出的捆绑包数据应类似于以下示例：

   ![包值](./assets/product-bundle-values-export-data.png){width="600" zoomable="yes"}

1. 为了更便于编辑，您可以复制`bundle_values`数据，并将其粘贴到文本编辑器中，然后在每个项目后添加换行符，以使每个项目位于单独的行中。

1. 编辑数据后，请仔细删除换行符，然后将编辑的数据粘贴回`bundle_values`列。

   在下图中，向每个瑜伽带添加了`position=[number]`参数，以更改商店清单中项目的顺序。

   ![位置参数](./assets/product-bundle-values-position-parameter.png){width="500" zoomable="yes"}

1. 编辑数据后，**[!UICONTROL Save]** CSV文件。

#### 步骤3：导入更新的产品

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Import]**。

1. 在&#x200B;_[!UICONTROL Import Settings]_下，将&#x200B;**[!UICONTROL Entity Type]**设置为`Products`。

1. 将&#x200B;**[!UICONTROL Import Behavior]**&#x200B;设置为`Replace`。

   此选项会覆盖捆绑产品先前的数据，而不是将更改添加为附加项。

1. 向下滚动到&#x200B;_要导入的文件_&#x200B;部分，然后单击&#x200B;**[!UICONTROL Choose File]**。

1. 选择您编辑的CSV文件。

1. 单击&#x200B;**[!UICONTROL Check Data]**&#x200B;并等待片刻，以便检查数据。

1. 如果文件有效，请单击&#x200B;**[!UICONTROL Import]**。

1. 进程完成后，转到&#x200B;**[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**并单击&#x200B;**[!UICONTROL Flush Cache Storage]**。

   这可确保更新的产品立即在店面中可用。

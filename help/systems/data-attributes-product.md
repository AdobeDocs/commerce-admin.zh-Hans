---
title: 产品数据属性参考
description: 在处理产品数据导入和导出时，请使用此产品数据属性的引用。
exl-id: 9ffa4d1f-cbf8-4a08-bb79-33f21e698a74
feature: Products, Attributes
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '2473'
ht-degree: 0%

---

# 产品数据属性参考

下表按默认显示顺序列出了典型产品导出的属性。 每个属性在CSV文件中都表示为一列，产品记录则表示为行。 以下划线开头的列包含服务数据，如复杂数据的属性或选项值。 您可以[从目录中](data-export.md)导出产品，以查看每个属性在数据中的表示方式。

用于导出此数据的安装已安装示例数据，并具有两个网站和多个商店视图。 尽管此列表包含通常导出的所有列，但`sku`是唯一所需的值。 要导入数据，只能包含更改后的列。 `sku`应为第一列，但其余属性的顺序无关紧要。

## 简单的产品CSV文件结构

| 属性 | 描述 |
|--- |--- |
| `sku` | （必需）库存单位是用于跟踪库存的唯一字母数字标识符。 SKU的长度最多可为64个字符。 例如： `sku123`<br/>**_注意：_**超过64个字符的SKU会导致导入失败。 |
| `store_view_code` | 标识产品可用的特定商店视图。 如果留空，则产品在默认商店视图中可用。 例如： `storeview1`，`english`，`spanish` |
| `attribute_set_code` | 根据产品类型将产品分配给特定的属性集或产品模板。 创建产品后，便无法更改属性集。 例如： `default` |
| `product_type` | 指示产品类型。 值：<br/>`simple` — 通常作为单个单位或以固定数量出售的有形项目。<br/>`grouped` — 作为集合销售的一组单独产品。<br/>`configurable` — 客户在购买之前必须选择具有多个选项的产品。 可以管理每组变体的库存，因为它们代表一个具有不同SKU的单独产品。 例如，可配置产品的颜色和大小的组合与目录中的特定SKU相关联。<br/>`virtual` — 一种不需要装运且未保留在库存中的无形产品。 示例包括服务、成员资格和订阅。<br/>`bundle` — 可自定义的产品集，其中包含一起销售的简单产品。 |
| `categories` | 指示分配给产品的每个类别。 使用正斜杠分隔类别和子类别。 要指示多个类别路径，请使用管道分隔每个路径 | 符号。 例如： `Default Category/Gear&#124;Default Category/Gear/Bags` |
| `product_websites` | 提供产品的每个网站的网站代码。 单个产品可以分配给多个网站，也可以仅分配给一个网站。 如果指定多个网站，请用逗号分隔每个网站，不带空格。 例如： `base`或`base,website2` |
| `name` | 产品名称出现在所有产品列表中，是客户用于标识产品的名称。 |
| `description` | 产品描述提供了有关产品的详细信息，并且可能包括简单的HTML标签。 |
| `short_description` | 简短的产品描述的使用取决于主题。 它可能会出现在产品列表中，有时用于发送到购物网站的RSS馈送列表。 |
| `weight` | 单个产品的重量。 实际产品重量由承运人在发运时确定。 |
| product_line | 确定产品是否可在商店中销售。 值： <br/>`1` — （是）产品已启用，可供销售。<br/>`2` — （否）该产品已禁用，不可销售。 |
| `tax_class_name` | 与此产品关联的税分类的名称。 |
| `visibility` | 确定产品在目录中是否可见，以及产品是否可用于搜索。 值：<br/>`Not Visible Individually` — 产品不包含在产品列表中，尽管它可能是其他产品的变体。<br/>`Catalog` — 产品出现在所有目录列表中。<br/>`Search` — 该产品可用于搜索操作。<br/>`Catalog, Search` — 产品包含在目录列表中，也可用于搜索。 |
| `price` | 产品在您的商店中销售的价格。 |
| `special_price` | 指定日期范围内产品的折扣价格。 |
| `special_price_from_date` | 特别价格生效时的时段的开始日期。 |
| `special_price_to_date` | 特殊价格生效时的时段的最后日期。 |
| `url_key` | URL中标识产品的一部分。 默认值基于产品名称。 例如： `product-name` |
| save_rewrites_history | 如果为值`1`提供了新的`url_key`，则会生成新的301 URL重写，以便将旧URL重定向到新URL。 |
| `meta_title` | 元标题显示在浏览器和搜索结果列表的标题栏和选项卡中。 元标题应为产品所独有的，包含高值关键词，并且长度应小于70个字符。 |
| `meta_keywords` | 元关键字仅对搜索引擎可见，并且被某些搜索引擎忽略。 选择用逗号分隔的高值关键字。 例如： `keyword1`，`keyword2`，`keyword3` |
| `meta_description` | 元描述提供了用于搜索结果列表的产品简要概述。 理想情况下，元描述长度应介于150到160个字符之间，尽管字段最多可接受255个字符。 |
| `base_image` | 产品页面上主图像的相对路径。 Commerce以字母顺序的文件夹结构在内部存储文件。 您可以查看导出数据中每个图像的确切位置。 例如： `/sample_data/m/b/mb01-blue-0.jpg`<br/>要上传新映像或覆盖现有映像，请输入文件名，其前面加有正斜杠。 例如： `/image.jpg` |
| `base_image_label` | 与基本图像关联的标签。 |
| `small_image` | 在目录页面上使用的小图像的文件名，它前面有正斜杠。 例如： `/image.jpg` |
| `small_image_label` | 与小图像关联的标签。 例如： `Small Image 1`，`Small Image 2` |
| `thumbnail_image` | 要在产品页面的图库中显示的任何缩略图图像的文件名，前带有正斜杠。 例如： `/image.jpg` |
| `thumbnail_image_label` | 与任何缩略图图像关联的标签。 例如： `Thumbnail 1`，`Thumbnail 2` |
| `created_at` | 指示产品的创建日期。 创建产品时会自动生成日期，但可以稍后编辑。 |
| `updated_at` | 指示上次更新产品的日期。 |
| `new_from_date` | 指定新产品列表的“起始”日期，并确定该产品是否作为新产品提供。 |
| `new_to_date` | 指定新产品列表的“截止”日期，并确定该产品是否作为新产品提供。 |
| `display_product_options_in` | 如果产品有多个选项，则确定它们在产品页面上的显示位置。 值：产品信息列/信息列后的块 |
| `map_price` | 产品的最低广告价格。 （仅在启用MAP时显示。） |
| `msrp_price` | 制造商建议的产品零售价。 （仅在启用MAP时显示。） |
| `map_enabled` | 确定配置中是否启用了最低广告价格。 值： <br/>`1` — （是） MAP已启用。<br/>`0` （或空白） — （无）未启用MAP。 |
| `gift_message_available` | 确定产品购买中是否可以包含礼品消息。 值：<br/>`1` — （是）向客户显示包含礼品消息的选项。<br/>`0`（或空白） — （否）未向客户显示包含礼品消息的选项。 |
| `custom_design` | 列出可应用于产品页面的可用主题。 |
| `custom_design_from` | 指定将所选主题应用于产品页面时的开始日期。 |
| `custom_design_to` | 指定将所选主题应用于产品页面时的结束日期。 |
| `custom_layout_update` | 作为产品页的布局更新应用的其他XML代码。 |
| `page_layout` | 确定产品页面的页面布局。 值：<br/>`No layout updates` — 不更改页面布局。<br/>`1 column` — 将一列布局应用于产品页面。<br/>`2 columns with left bar` — 将带有左侧栏的双列布局应用于产品页面。<br/>`2 columns with right bar` — 将带有右侧栏的两列布局应用于产品页面。<br/>`3 columns` — 将三列布局应用于产品页面。<br/>`empty` — 将空白布局应用于产品页面。 |
| `product_options_container` | 如果产品有多个选项，则确定它们在产品页面上的显示位置。 值：产品信息列/信息列后的块 |
| `msrp_display_actual_price_type` | 确定客户可在何处看到产品的实际价格。 值： <br/>`In Cart` — 显示购物车中的实际产品价格。<br/>`Before Order Confirmation` — 在订单确认之前显示结账流程结束时实际产品价格。<br/>`On Gesture` — 当客户单击&#x200B;_单击以获取价格_&#x200B;或&#x200B;_这是什么时，在弹出窗口中显示实际产品价格？_&#x200B;链接。 |
| `country_of_manufacture` | 标识生产产品的国家/地区。 |
| `additional_attributes` | 为产品创建的其他属性。 例如： <br/>`has_options=0,required_options=0color=Black,has_options=0,required_options=0,size_general=XS` |
| `qty` | 当前库存产品的数量。 |
| `out_of_stock_qty` | 确定产品缺货的库存水平。 |
| `use_config_min_qty` | 确定是否使用配置中的默认值，该值对应于“使用配置设置”复选框。 值：<br/>`1` — （是）默认配置设置用于此属性的值。<br/>`0` （或空白） — （否）可以覆盖此属性的值的默认配置。 |
| `is_qty_decimal` | 确定qty属性是否具有小数值。 值：<br/>`1` — （是） qty属性的值是十进制值。<br/>`0` （或空白） — （否） qty属性的值是整数。 |
| `allow_backorders` | 确定您的商店是否允许延期交货，以及如何管理延期交货。 |
| `use_config_backorders` | 确定是否使用延交订单的默认配置设置，并且与“使用配置设置”复选框的状态相对应。 值：<br/>`1` — （是） qty属性的值是十进制值。<br/>`0` （或空白） — （否） qty属性的值是整数。 |
| `min_cart_qty` | 指定单个订单中可采购的项目的最小数量。 |
| `use_config_min_sale_qty` | 确定是否使用最小数量的默认配置设置，它对应于“使用配置设置”复选框的状态。 值：<br/>`1` — （是）<br/>`0` （或空白） — （否） |
| `max_cart_qty` | 指定单笔订单可购买产品的最大数量。 |
| `use_config_max_sale_qty` | 确定是否使用最大数量的默认配置设置，该设置对应于“使用配置设置”复选框的状态。 值：<br/>`1` — （是）<br/>`0` （或空白） — （否） |
| `is_in_stock` | 指示产品是否有库存。 |
| `notify_on_stock_below` | 指定触发&#x200B;_缺货_&#x200B;通知的Stock级别。 |
| `use_config_notify_stock_qty` | 确定默认配置设置是否用于触发库存级别通知，并与使用配置设置复选框的状态相对应。 值：<br/>`1` — （是）<br/>`0` （或空白） — （否） |
| `manage_stock` | 确定是否使用库存控制来管理产品。 值：<br/>`1` — （是）激活完整库存控制以管理产品的库存水平。<br/>`0` （或空白） — （否）系统不跟踪当前有库存的项数。 |
| `use_config_manage_stock` | 确定是否使用用于管理库的默认配置设置，该设置对应于“使用配置设置”复选框的状态。 值：<br/>`1` — （是）<br/>`0` （或空白） — （否） |
| `use_config_qty_increments` | 确定是否使用数量增量的默认配置设置，该设置对应于“使用配置设置”复选框的状态。 值：<br/>`1` — （是）<br/>`0` （或空白） — （否） |
| `qty_increments` | 确定构成数量增量的产品数量。 |
| `use_config_enable_qty_inc` | 确定是否使用默认配置设置来启用数量增量，该设置对应于“使用配置设置”复选框的状态。 值：<br/>`1` — （是）<br/>`0` （或空白） — （否） |
| `enable_qty_increments` | 确定是否为产品启用数量增量。 |
| `is_decimal_divided` | 确定产品部件是否可以单独发运。 选项： `Yes` / `No` |
| `website_id` | 对于具有多个网站的安装，会标识提供产品的特定网站。 如果留为空白，则该产品将在所有网站中提供。 |
| `related_skus` | 列出已标识为相关产品的每个产品的SKU。 例如： `24-WG080,24-UG03,24-UG01,24-UG02` |
| `related_position` | 确定related_skus列中列为“相关产品”的SKU的位置（排序顺序）。 例如： `1,2,3,4` |
| `crosssell_skus` | 列出已标识为交叉销售的每种产品的SKU。 |
| `crosssell_position` | 确定在`crosssell_skus`列中作为交叉销售产品列出的SKU的位置（排序顺序）。 |
| `upsell_skus` | 列出已标识为追加销售的每种产品的SKU。 |
| `upsell_position` | 确定`upsell_skus`列中作为追加销售产品列出的SKU的位置（排序顺序）。 |
| `additional_images` | 要与产品关联的任何其他图像的文件名，其前面带有正斜杠。 例如： `/image.jpg` |
| `additional_image_labels` | 与任何其他图像关联的标签。 例如： `Label 1`，`Label 2` |
| `custom_options` | 指定分配给每个自定义选项的属性和值。 例如： <br/>`name=Color, type=drop_down, required=1, price= price_type=fixed, sku=, option_title=Black|name=Color, type=drop_down, required=1, price=, price_type=fixed, sku=, option_title=White` |

{style="table-layout:auto"}

## 产品变体的服务数据

| 属性 | 描述 | 应用于 |
|--- |--- | --- |
| `_super_products_sku` | 为可配置产品变体生成的SKU。 例如：WB03-XS-Green | 可配置产品 |
| `_super_attribute_code` | 可配置产品变体的属性代码。 例如：颜色 | 可配置产品 |
| `_super_attribute_option` | 可配置产品变体的值。 例如：绿色 | 可配置产品 |
| `_super_attribute_price_corr` | 与可配置产品变体关联的价格调整。 | 可配置产品 |
| `_associated_sku` | 与分组产品关联的产品的SKU。 | 分组产品<br/>捆绑产品 |
| `_associated_default_qty` | 确定包含的关联产品的数量。 | 可配置产品<br/>分组产品<br/>捆绑销售产品 |
| `_associated_position` | 确定关联产品与其他关联产品一起列出时的位置。 | 可配置产品<br/>分组产品<br/>捆绑销售产品 |

{style="table-layout:auto"}

## 复杂的产品数据属性

术语复杂数据是指与多个产品选项关联的数据。 以下产品类型使用来自单独产品的数据来创建产品变体和多个选项。

- [可配置](../catalog/product-create-configurable.md)
- [已分组](../catalog/product-create-grouped.md)
- [捆绑](../catalog/product-create-bundle.md)

如果导出可配置产品，您将找到构成简单产品的标准属性，以及管理复杂数据所需的其他属性。

![可配置的产品 — 导出的数据](./assets/data-exported-configurable-product.png){width="600" zoomable="yes"}

### 可配置的产品

| 属性 | 描述 |
|--- |--- |
| `configurable_variation_labels` | 标识产品变体的标签。 例如： `Choose Color:`或`Choose Size:` |
| `configurable_variations` | 描述与产品变体关联的值。 例如： `sku=sku-red xs,color=red,size=xs,price=10.99,display=1,image=/pub/media/import/image1.png|sku=sku-red-m,color=red,size=m,price=20.88,display=1,image=/pub/media/import/image2.png` |

{style="table-layout:auto"}

### 分组的产品

| 属性 | 描述 |
|--- |--- |
| `associated_skus` | 标识组成组的各个产品的SKU。 |

{style="table-layout:auto"}

### 捆绑产品

| 属性 | 描述 |
|--- |--- |
| `bundle_price_type` | 确定捆绑项目的价格是固定价格还是动态价格。 |
| `bundle_sku_type` | 确定每个项目是否分配了变量、动态SKU或是否为捆绑使用了固定SKU。 选项：固定/动态 |
| `bundle_weight_type` | 确定捆绑项目的权重是可变的还是固定的。 |
| `bundle_values` | 描述与捆绑选项关联的教导值。 例如： `name=Bundle Option One,type=dropdown; required=1, sku=sku-option2,price=10, price_type=fixed` |

{style="table-layout:auto"}

## 高级定价属性

通过“高级价格导入/导出”，您可以快速更新产品组和层价格的定价信息。 [导入](data-import.md)和[导出](data-export.md)高级价格数据的进程与任何其他实体类型相同。 示例CSV文件包含每个支持高级定价的产品类型的层价和组价。 更改高级定价不会影响产品记录的其余部分。

![示例导出数据 — 高级定价](./assets/data-advanced-pricing-export-sample.png){width="600" zoomable="yes"}

| 属性 | 描述 |
|--- |--- |
| `sku` | （必需）库存单位是用于跟踪库存的唯一字母数字标识符。 SKU的长度最多可为64个字符。 例如： `sku123`<br/>**_注意：_**超过64个字符的SKU会导致导入失败。 |
| `tier_price_website` | [网站代码](../stores-purchase/stores.md#add-websites)标识了每个可用层定价的网站。 例如： `-  website1 -  All Websites [USD]` |
| `tier_price_customer` | 标识提供层定价的[客户组](../customers/customer-groups.md)。 例如： `-  ALL GROUPS -  NOT LOGGED IN -  General -  Wholesale -  Retailer` |
| `tier_price_customer_group` | 标识提供层定价的客户组。 例如： `-  ALL GROUPS -  NOT LOGGED IN -  General -  Wholesale -  Retailer` |
| `tier_price_qty` | 必须订购才能获得层价格折扣的产品数量。 |
| `tier_price` | 产品的折扣价格。 对于[捆绑产品](../catalog/product-create-bundle.md)，层价格按百分比计算。 |
| `group_price_website` | 每个网站的[网站代码](../stores-purchase/stores.md#add-websites)，每个网站都有可用的组定价。 如果指定多个网站，请用逗号分隔每个网站，不带空格。 例如： `-  website1 -  All Websites [USD]` |
| `group_price_customer_group` | 标识提供组定价的客户组。 例如： `-  NOT LOGGED IN -  General -  Wholesale -  Retailer` |
| `group_price` | 产品的折扣组价。 对于[捆绑产品](../catalog/product-create-bundle.md)，组价格按百分比计算。 |

{style="table-layout:auto"}

---
title: ’[!UICONTROL Catalog] &gt； [!UICONTROL XML Sitemap]’
description: 查看 [!UICONTROL Catalog] &gt； [!UICONTROL XML Sitemap] 商务管理员页面。
exl-id: 319c34e9-bd5f-46f8-810f-bc4d5228f9c9
feature: Configuration, Site Navigation
source-git-commit: 76bd1b1af9b55d69bd98209d70fb5518f190a3e1
workflow-type: tm+mt
source-wordcount: '360'
ht-degree: 1%

---

# [!UICONTROL Catalog] > [!UICONTROL XML Sitemap]

{{config}}

## [!UICONTROL Categories Options]

![类别选项](./assets/xml-sitemap-categories-options.png)<!-- zoom -->

<!-- [Categories Options](https://docs.magento.com/user-guide/marketing/sitemap-xml-configure.html) -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Frequency] | 商店视图 | 确定Sitemap类别的更新频率。 选项： `Always` / `Hourly` / `Daily` / `Weekly` / `Monthly` / `Yearly` / `Never` |
| [!UICONTROL Priority] | 商店视图 | 值介于 `0.0` 和 `1.0` 确定类别Sitemap更新相对于其他内容的优先级。 零(`0.0`)的优先级最低。 |

{：style=&quot;table-layout：auto&quot;}

## [!UICONTROL Products Options]

![产品选项](./assets/xml-sitemap-products-options.png)<!-- zoom -->

<!-- [Products Options](https://docs.magento.com/user-guide/marketing/sitemap-xml-configure.html) -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Frequency] | 商店视图 | 确定Sitemap产品的更新频率。 选项： `Always` / `Hourly` / `Daily` / `Weekly` / `Monthly` / `Yearly` / `Never` |
| [!UICONTROL Priority] | 商店视图 | 值介于 `0.0` 和 `1.0` 确定产品站点地图更新相对于其他内容的优先级。 零(`0.0`)的优先级最低。 |
| [!UICONTROL Add Images into Sitemap] | 商店视图 | 确定图像在站点地图中的包含范围。 选项： `None` / `Base Only` / `All` |

{：style=&quot;table-layout：auto&quot;}

## [!UICONTROL CMS Pages Options]

![CMS页面选项](./assets/xml-sitemap-cms-pages-options.png)<!-- zoom -->

<!-- [CMS Pages Options](https://docs.magento.com/user-guide/marketing/sitemap-xml-configure.html) -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Frequency] | 商店视图 | 确定Sitemap CMS页面的更新频率。 选项： `Always` / `Hourly` / `Daily` / `Weekly` / `Monthly` / `Yearly` / `Never` |
| [!UICONTROL Priority] | 商店视图 | 值介于 `0.0` 和 `1.0` 确定CMS页面Sitemap更新相对于其他内容的优先级。 零(`0.0`)的优先级最低。 |

{：style=&quot;table-layout：auto&quot;}

## [!UICONTROL Store Url Options]

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Frequency] | 商店视图 | 确定存储URL的更新频率。 选项： `Always` / `Hourly` / `Daily` / `Weekly` / `Monthly` / `Yearly` / `Never` |
| [!UICONTROL Priority] | 商店视图 | 值介于 `0.0` 和 `1.0` 确定存储URL更新相对于其他内容的优先级。 零(`0.0`)的优先级最低。 |

{：style=&quot;table-layout：auto&quot;}

## [!UICONTROL Generation Settings]

![生成设置](./assets/xml-sitemap-generation-settings.png)<!-- zoom -->

<!-- [Generation Settings](https://docs.magento.com/user-guide/marketing/sitemap-xml-configure.html) -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Enabled] | 商店视图 | 确定XML Sitemap是否可用于存储。 选项： `Yes` / `No` |
| [!UICONTROL Start Time] | 商店视图 | 指定站点地图在一天中的小时、分钟和秒进行更新。 |
| [!UICONTROL Frequency] | 商店视图 | 确定站点地图的更新频率。 选项： `Daily` / `Weekly` / `Monthly` |
| [!UICONTROL Error Email Recipient] | 商店视图 | 在站点地图更新过程中发生错误时接收通知的人员的电子邮件地址。 对于多个地址，请使用逗号分隔每个地址。 |
| [!UICONTROL Error Email Sender] | 网站 | 标识显示为错误通知发送者的商店联系人。 选项： `General Contact` / `Sales Representative` / `Customer Support` / `Custom Email 1` / `Custom Email 2` |
| [!UICONTROL Error Email Template] | 网站 | 标识用于错误通知的电子邮件模板。 默认模板： `Sitemap generate Warnings` |

{：style=&quot;table-layout：auto&quot;}

## [!UICONTROL Sitemap File Limits]

![站点地图文件限制](./assets/xml-sitemap-sitemap-file-limits.png)<!-- zoom -->

<!-- [Sitemap File Limits](https://docs.magento.com/user-guide/marketing/sitemap-xml-configure.html) -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Maximum No of URLs Per File] | 商店视图 | 确定单个站点地图中可以包含的最大URL数。 |
| [!UICONTROL Maximum File Size] | 商店视图 | 确定生成的站点地图的最大大小（字节）。 |

{：style=&quot;table-layout：auto&quot;}

## [!UICONTROL Search Engine Submission Settings]

![搜索引擎提交设置](./assets/xml-sitemap-search-engine-submission-settings.png)<!-- zoom -->

<!-- [Search Engine Submission Settings](https://docs.magento.com/user-guide/marketing/sitemap-xml-configure.html) -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Enable Submission to Robots.txt] | 商店视图 | 允许为robots.txt文件提交指令。 选项： `Yes` / `No` |

{：style=&quot;table-layout：auto&quot;}

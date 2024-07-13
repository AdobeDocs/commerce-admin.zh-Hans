---
title: 客户数据属性参考
description: 当您处理客户数据导入和导出时，请使用此客户数据属性的引用。
exl-id: d22ebfed-f439-4a3f-b39e-e957b65c8c21
feature: Customers, Attributes
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '483'
ht-degree: 0%

---

# 客户数据属性参考

下表列出了客户主文件和客户地址的典型导出中的属性。 用于导出此数据的安装有两个网站和多个商店视图，其中安装了示例数据。

每个属性或字段在CSV文件中均表示为一列，客户记录则表示为行。 以下划线开头的列是包含属性或复杂数据的服务实体。

## 客户主文件

| 属性 | 描述 |
|--- |--- |
| `email` | 客户的电子邮件地址。 |
| `_website` |  |
| `_store` |  |
| `confirmation` | 确认标记。 |
| `created_at` | 创建客户帐户的日期。 |
| `created_in` | 创建帐户的存储区视图。 |
| `disable_auto_group_change` | 确定在验证VAT ID期间是否可以动态分配客户组。 |
| `dob` | 客户的出生日期。 <br><br>**_重要信息：_**根据当前安全和隐私最佳实践，查看客户的完整出生日期（月、日、年）的存储和处理情况。 与其他个人标识符（如_全名&#x200B;_）一起收集时，可能会有法律和安全风险。 我们建议限制存储客户的完整出生日期，并转而建议使用客户出生年份作为替代方法。 |
| `firstname` | 客户的名字。 |
| `gender` | 客户性别。 |
| `group_id` | 分配客户的客户组的ID。 |
| `lastname` | 客户的姓氏。 |
| `middlename` | 客户的中间名或中间首字母。 |
| `password_hash` | 密码哈希 |
| `prefix` | 与客户名称一起使用的任何前缀（如`Mr.`、`Ms.`、`Mrs.`和`Dr.`）。 |
| `rp_token` | 重置密码令牌。 |
| `rp_token_created_at` | 密码重置日期。 |
| `store_id` | 商店ID |
| `suffix` | 与客户名称一起使用的任何后缀（如`Jr.`、`Sr.`和`Esquire`）。 |
| `taxvat` |  |
| `website_id` | 创建客户帐户的网站的网站ID。 |
| `password` | 客户密码。 |

{style="table-layout:auto"}

## 客户地址

| 属性 | 描述 |
|--- |--- |
| `_website` |  |
| `_email` |  |
| `_entity_id` |  |
| `city` | 客户地址所在的城市。 |
| `company` | 公司名称（如果适用于此地址）。 |
| `country_id` | 客户地址所在的国家/地区ID。 |
| `fax` | 客户的传真号码（如果适用）。 |
| `firstname` | 客户的名字。 |
| `lastname` | 客户的姓氏。 |
| `middlename` | 客户的中间名或中间首字母。 |
| `postcode` | 客户地址所在的邮政编码。 |
| `prefix` | 与客户名称一起使用的任何前缀（如`Mr.`、`Ms.`、`Mrs.`和`Dr.`）。 |
| `region` | 客户地址所在的地区。 |
| `region_id` | 区域ID |
| `street` | 客户的街道地址。 如果配置中指定了街道地址，则第二行是可用的。 |
| `suffix` | 如果使用的是与客户名称关联的后缀（如`Jr.`、`Sr.`或`III`）。 |
| `telephone` | 客户与地址关联的电话号码。 |
| `vat_id` | VAT ID是用于增值税验证的客户增值税编号的内部标识符。 |
| `vat_is_valid` |  |
| `vat_request_date` |  |
| `vat_request_id` |  |
| `vat_request_success` |  |
| `_address_default_billing_` | 标识默认帐单地址。 值为`1`表示该地址是客户的默认帐单地址。 值： 1 / 0 |
| `_address_default_shipping_` | 标识默认送货地址。 值为`1`表示该地址是客户的默认送货地址。 值： `1` / `0` |

{style="table-layout:auto"}

---
title: Adobe Commerce B2B向后不兼容的更改
description: 了解Adobe Commerce B2B版本中的更改，这些更改可能需要您更新自定义代码。
exl-id: 79b66843-3f34-4fe9-9670-53d19b749eb4
source-git-commit: 29663b8a88abc581b9543621ddb475f7d7903027
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---

# Adobe Commerce B2B向后不兼容的更改

有关Adobe Commerce版本的B2B中所有向后不兼容的更改的高级参考信息。 请参阅高亮部分以了解具有重大影响并需要详细说明和特殊说明的不兼容更改。

## 高亮

### 1.4.2至1.5.0

添加多公司分配后，公司用户帐户现在可以有多个`company_id`值。 已更新`Magento\Company\Api\Data\CompanyCustomerInterface`以设置用户的默认`company_id`。 默认设置为分配给公司用户帐户的第一个公司。

如果您从以前的版本升级，Adobe建议在使用`Magento\Company\Api\Data\CompanyCustomerInterface`的类中实现以下方法。

- Magento\Company\Api\Data\CompanyCustomerInterface：：getIsDefault
- Magento\Company\Api\Data\CompanyCustomerInterface：：setIsDefault

## 引用

{{$include /help/_includes/backward-incompatible-changes/1.4.2-1.5.0.md}}

{{$include /help/_includes/backward-incompatible-changes/1.4.1-1.4.2.md}}

{{$include /help/_includes/backward-incompatible-changes/1.4.0-1.4.1.md}}

{{$include /help/_includes/backward-incompatible-changes/1.3.5-1.4.0.md}}

{{$include /help/_includes/backward-incompatible-changes/1.3.4-1.3.5.md}}

{{$include /help/_includes/backward-incompatible-changes/1.3.3-1.3.4.md}}

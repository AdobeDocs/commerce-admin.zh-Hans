---
title: 变量引用
description: 查看常用电子邮件模板及其相关变量的示例。
exl-id: b5e49a56-4b7c-431d-bd44-e8591106fa4e
role: Admin, User
feature: System, Variables, Communications
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 0%

---

# 变量引用

最多 [电子邮件模板](email-template-custom.md) 部分为 [预定义变量](variables-predefined.md) 模板的特定属性。 以下列表包含常用电子邮件模板及其关联变量的示例。

## 电子邮件模板变量

| 变量 | 标记标记 |
|--- |--- |
| [!UICONTROL Email Footer Template] | `{{template config_path="design/email/footer_template"}}` |
| [!UICONTROL Email Header Template] | `{{template config_path="design/email/header_template"}}` |
| [!UICONTROL Email Logo Image Alt] | `{{var logo_alt}}` |
| [!UICONTROL Email Logo Image URL] | `{{var logo_url}}` |
| [!UICONTROL Email Logo Image Height] | `{{var logo_height}}` |
| [!UICONTROL Email Logo Image Width] | `{{var logo_width}}` |
| [!UICONTROL Template CSS] | `{{var template_styles\|raw}}` |

{style="table-layout:auto"}

## 存储联系信息变量

| 变量 | 标记标记 |
|--- |--- |
| [!UICONTROL Base Unsecure URL] | `{{config path="web/unsecure/base_url"}}` |
| [!UICONTROL Base Secure URL] | `{{config path="web/secure/base_url"}}` |
| [!UICONTROL General Contact Name] | `{{config path="trans_email/ident_general/name"}}` |
| [!UICONTROL General Contact Email] | `{{config path="trans_email/ident_general/email"}}` |
| [!UICONTROL Sales Representative Contact Name] | `{{config path="trans_email/ident_sales/name"}}` |
| [!UICONTROL Sales Representative Contact Email] | `{{config path="trans_email/ident_sales/email"}}` |
| [!UICONTROL Customer Support Name] | `{{config path="trans_email/ident_support/name"}}` |
| [!UICONTROL Customer Support Email] | `{{config path="trans_email/ident_support/email"}}` |
| [!UICONTROL Custom1 Contact Name] | `{{config path="trans_email/ident_custom1/name"}}` |
| [!UICONTROL Custom1 Contact Email] | `{{config path="trans_email/ident_custom1/email"}}` |
| [!UICONTROL Custom2 Contact Name] | `{{config path="trans_email/ident_custom2/name"}}` |
| [!UICONTROL Custom2 Contact Email] | `{{config path="trans_email/ident_custom2/email"}}` |
| [!UICONTROL Store Name] | `{{config path="general/store_information/name"}}` |
| [!UICONTROL Store Phone Telephone] | `{{config path="general/store_information/phone"}}` |
| [!UICONTROL Store Hours] | `{{config path="general/store_information/hours"}}` |
| [!UICONTROL Country] | `{{config path="general/store_information/country_id"}}` |
| [!UICONTROL Region/State] | `{{config path="general/store_information/region_id"}}` |
| [!UICONTROL Zip/Postal Code] | `{{config path="general/store_information/postcode"}}` |
| [!UICONTROL City] | `{{config path="general/store_information/city"}}` |
| [!UICONTROL Street Address 1] | `{{config path="general/store_information/street_line1"}}` |
| [!UICONTROL Street Address 2] | `{{config path="general/store_information/street_line2"}}` |
| [!UICONTROL Store Contact Address] | `{{config path="general/store_information/address"}}` |
| [!UICONTROL VAT Number] | `{{config path="general/store_information/merchant_vat_number"}}` |

{style="table-layout:auto"}

## 新帐户模板变量

| 变量 | 标记标记 |
|--- |--- |
| [!UICONTROL Customer Account URL] | `{{var this.getUrl($store, 'customer/account/')}}` |
| [!UICONTROL Customer Email] | `{{var customer.email}}` |
| [!UICONTROL Customer Name] | `{{var customer.name}}` |

{style="table-layout:auto"}

## 新订单模板变量

| 变量 | 标记标记 |
|--- |--- |
| [!UICONTROL Billing Address] | `{{var formattedBillingAddress\|raw}}` |
| [!UICONTROL Email Order Note] | `{{var order.getEmailCustomerNote()}}` |
| [!UICONTROL Order ID] | `{{var order.increment_id}}` |
| [!UICONTROL Order Items Grid] | `{{layout handle="sales_email_order_items" order=$order area="frontend"}}` |
| [!UICONTROL Payment Details] | `{{var payment_html\|raw}}` |
| [!UICONTROL Shipping Address] | `{{var formattedShippingAddress\|raw}}` |
| [!UICONTROL Shipping Description] | `{{var order.getShippingDescription()}}` |

{style="table-layout:auto"}

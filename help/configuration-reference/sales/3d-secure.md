---
title: ’[!UICONTROL Sales] &gt； [!UICONTROL 3D Secure]’
description: 查看 [!UICONTROL Sales] &gt； [!UICONTROL 3D Secure] 商务管理员页面。
exl-id: 38eb3ee6-8b80-4ba3-afce-8ab82baa76a9
feature: Configuration, Security, Payments
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL 3D Secure]

[!DNL 3-D Secure] 开发人员 [!DNL Visa] 提升安全的在线交易。 示例 [!DNL 3-D Secure] 由卡网络创建的解决方案由验证 [!DNL Visa]， [!DNL Mastercard SecureCode]， [!DNL American Express SafeKey]、和 [!DNL CardinalCommerce Consumer Authentication]. [!DNL CardinalCommerce] 是全球领先的数字交易身份验证公司，并且是 [!DNL Visa].

[!DNL 3-D Secure] 版本2.0支持大量增强功能，包括高级身份验证方法和身份验证流程，以及改进的商家和颁发者之间的数据共享。

>[!NOTE]
>
>此 [Braintree](../../stores-purchase/braintree.md) 支付网关还支持 [!DNL 3-D Secure] 验证。

{{config}}

## [!UICONTROL CardinalCommerce]

![CardinalCommerce](./assets/3d-secure-cardinalcommerce.png)<!-- zoom -->

| 字段 | [范围](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Environment] | 网站 | 指示您的操作模式 [!DNL CardinalCommerce] 帐户。 如果您在测试环境中运行，请选择“沙盒”。 选项：沙盒/生产（默认） |
| [!UICONTROL Org Unit ID] | 网站 | 您网站上的组织单位ID [!DNL CardinalCommerce] 商户帐户。 |
| [!UICONTROL API Key] | 网站 | 来自您的 [!DNL CardinalCommerce] 商户帐户。 |
| [!UICONTROL API Identifier] | 网站 | 来自您的 [!DNL CardinalCommerce] 商户帐户。 |
| [!UICONTROL Debug] | 网站 | 选项： `Yes` / `No` |

{style="table-layout:auto"}

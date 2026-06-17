---
title: '[!UICONTROL Sales] > [!UICONTROL 3D Secure]'
description: 查看Commerce管理员的[!UICONTROL Sales] &gt； [!UICONTROL 3D Secure]页面上的配置设置。
exl-id: 38eb3ee6-8b80-4ba3-afce-8ab82baa76a9
feature: Configuration, Security, Payments
TQID: https://experienceleague.adobe.com/WzxM9ZYbobbC1fWSIph0jv89uXLte6Wzjs5be27eMyU
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 126
ht-degree: 1%

---

# [!UICONTROL Sales] > [!UICONTROL 3D Secure]

[!DNL 3-D Secure]由[!DNL Visa]开发，用于提升安全的在线交易。 由卡网络创建的[!DNL 3-D Secure]解决方案的示例已由[!DNL Visa]、[!DNL Mastercard SecureCode]、[!DNL American Express SafeKey]和[!DNL CardinalCommerce Consumer Authentication]验证。 [!DNL CardinalCommerce]是数字交易身份验证领域的全球领先公司，是[!DNL Visa]的全资子公司。

[!DNL 3-D Secure]版本2.0支持大量增强功能，包括高级身份验证方法和身份验证流程，以及改进的商家和颁发者之间的数据共享。

>[!NOTE]
>
>[Braintree](../../stores-purchase/braintree.md)付款网关还支持[!DNL 3-D Secure]验证。

{{config}}

## [!UICONTROL CardinalCommerce]

![CardinalCommerce](./assets/3d-secure-cardinalcommerce.png)<!-- zoom -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|--- |--- |--- |
| [!UICONTROL Environment] | 网站 | 指示[!DNL CardinalCommerce]帐户的操作模式。 如果您在测试环境中运行，请选择“沙盒”。 选项：沙盒/生产（默认） |
| [!UICONTROL Org Unit ID] | 网站 | [!DNL CardinalCommerce]商家帐户中的组织单位ID。 |
| [!UICONTROL API Key] | 网站 | [!DNL CardinalCommerce]商家帐户的API密钥。 |
| [!UICONTROL API Identifier] | 网站 | [!DNL CardinalCommerce]商家帐户的API标识符。 |
| [!UICONTROL Debug] | 网站 | 选项： `Yes` / `No` |

{style="table-layout:auto"}

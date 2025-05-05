---
title: '[!UICONTROL General] &amp；gt； [!UICONTROL B2B Features]'
description: 查看Commerce管理员的[!UICONTROL General] &amp；gt； [!UICONTROL B2B Features]页面上的配置设置。
exl-id: fc07a067-b92a-49c7-8512-2dfcc1c6ba0c
feature: Configuration, B2B
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '342'
ht-degree: 1%

---

# [!UICONTROL General] > [!UICONTROL B2B Features]

{{b2b-feature}}

{{config}}

>[!TIP]
>
>通过安装和启用Adobe Commerce B2B，您可以利用公司的特定功能个性化购买体验。 Adobe Commerce B2B是一个集成式解决方案，同时支持B2B和B2C模型。 有关B2B功能的详细信息，请参阅&#x200B;[_Adobe Commerce B2B用户指南_](https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html?lang=zh-Hans)。

## [!UICONTROL B2B Features]

![B2B功能](./assets/b2b-features.png)<!-- zoom -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|------- |----------------------------------------------------------------------- |------------ |
| [[!UICONTROL Enable Company]](../../b2b/account-companies.md) | 网站 | 启用后，允许客户从其帐户仪表板管理其公司分配，默认情况下还启用“共享目录”和“B2B报价”功能。 选项： `Yes` / `No` |
| [[!UICONTROL Enable Quick Order]](../../b2b/quick-order.md) | 网站 | 启用后，允许客户和来宾根据SKU或产品名称快速下订单。 选项： `Yes` / `No` |
| [[!UICONTROL Enable Requisition List]](../../b2b/configure-requisition-lists.md) | 网站 | 启用后，允许客户从其帐户信息板创建和管理申请列表。 |

{style="table-layout:auto"}

![启用公司和共享目录的B2B功能](./assets/b2b-features-company-enabled.png)<!-- zoom -->

启用“公司”功能后，“共享目录”和B2B Quote将可使用其他字段。

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|------- |----------------------------------------------------------------------- |------------ |
| [[!UICONTROL Enable Shared Catalog]](../../b2b/catalog-shared.md) | 网站 | 启用后，即可使用自定义定价创建特选目录，这些目录可在全球范围内使用，或仅限特定公司使用。 选项： `Yes` / `No` |
| [!UICONTROL Enable Shared Catalog direct products price assigning] | 网站 | 当&#x200B;_[!UICONTROL Enable Shared Catalog]_&#x200B;字段设置为`Yes`时，此选项可用。 启用后，只有分配给共享目录的产品才会存储在价格指数中。 店面中不会显示未分配给共享目录的产品。 选项： `Yes` / `No` |
| [[!UICONTROL Enable B2B Quote]](../../b2b/configure-quotes.md) | 网站 | 启用后，允许公司购买者从购物车提交询价。 选项： `Yes` / `No` |

{style="table-layout:auto"}

### [!UICONTROL Default B2B Payment Methods]

![B2B配置 — 默认付款方式设置](./assets/b2b-features-default-payment-methods.png)<!-- zoom -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|------- |----------------------------------------------------------------------- |------------ |
| [!UICONTROL Applicable Payment Methods] | 全局 | 确定B2B买家可用的支付方式选择。 选项： `All Payment Methods` / `Specific Payment Methods` |
| [!UICONTROL Payment Methods] | 全局 | 指定B2B购买者可用的每种支付方式。 |

{style="table-layout:auto"}

### [!UICONTROL Default B2B Shipping Methods]

![B2B配置 — 默认配送方式](./assets/b2b-features-shipping-methods.png)<!-- zoom -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|------- |----------------------------------------------------------------------- |------------ |
| [!UICONTROL Applicable Shipping Methods] | 全局 | 确定默认情况下可供B2B购买者使用的配送方法的选择。 选项： `All Shipping Methods` / `Specific Shipping Methods` |
| [!UICONTROL Shipping Methods] | 全局 | 指定B2B购买者默认可用的每种配送方式。 <br/>**_注意：_**&#x200B;您还可以限制特定[公司帐户](../../b2b/account-companies.md)的配送方式。 |

{style="table-layout:auto"}

## [!UICONTROL Order Approval Configuration]

![B2B功能 — 订单审批配置](./assets/b2b-features-order-approval.png)<!-- zoom -->

| 字段 | [作用域](../../getting-started/websites-stores-views.md#scope-settings) | 描述 |
|------- |----------------------------------------------------------------------- |------------ |
| [[!UICONTROL Enable Purchase Orders]](../../stores-purchase/purchase-order.md) | 网站 | 启用后，允许公司创建采购订单。 选项： `Yes` / `No` |

{style="table-layout:auto"}



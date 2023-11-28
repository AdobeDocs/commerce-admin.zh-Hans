---
title: ’[!DNL Business Intelligence] 工具'
description: 了解Adobe Commerce和Magento Open Source商户如何使用商业智能工具来获得用于制定合理业务决策的见解。
exl-id: 687d04e4-841b-44f7-94ca-bbb20fbe2d8b
feature: Commerce Intelligence, Reporting
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '1157'
ht-degree: 0%

---

# [!DNL Business Intelligence] 工具

使用业务智能工具获得用于制定合理业务决策的洞察力。

## [!DNL Business Intelligence] 帐户

当您激活 [!DNL Business Intelligence] 通过Adobe，您可以访问五个包含大约70个报表的仪表板。 这些报表旨在提供有关数据的洞察，并回答诸如“我的订单环比增长如何？”、“谁是我的最忠实客户？”和“我的优惠券策略有效吗？”等之类的问题。 有关此工具集的详细信息，请参阅 [MBI用户指南][1].

## [!DNL Advanced Reporting]

[!DNL Advanced Reporting] 包含在Adobe Commerce和Magento Open Source中。 通过此功能，您可以访问基于您的产品、订单和客户数据的一组动态报表，并根据您的业务需求定制个性化仪表板。 同时 [!DNL Advanced Reporting] 用途 [!DNL Business Intelligence] 对于analytics，您无需拥有Business Intelligence帐户即可使用 [!DNL Advanced Reporting].

有关技术信息，请参见 [[!DNL Advanced Reporting]][2]开发人员文档中的{：target=&quot;_blank&quot;}主题。

>[!NOTE]
>
>[!DNL Business Intelligence] 帐户使用内置报表，而不是 [!DNL Advanced Reporting] 功能。

![高级报告仪表板](./assets/reporting-advanced.png){width="700"}

### 要求

* 网站必须在公共Web服务器上运行。

* 域必须具有有效的安全(SSL)证书。

* [!DNL Commerce] 必须已成功安装或升级，并且没有错误。

* 在 [!DNL Commerce] 配置 [存储URL](../stores-purchase/store-urls.md)， **[!UICONTROL Base URL (Secure)]** 存储视图的设置必须指向安全URL。 例如： `https://yourdomain.com`.

* 在 [!DNL Commerce] 存储URL的配置， **[!UICONTROL Use Secure URLs on Storefront]** 和 **[!UICONTROL Use Secure URLs in Admin]** 必须设置为 `Yes`.

* [[!DNL Commerce] crontab][3] 创建了cron作业，且该作业正在已安装的服务器上运行。

>[!NOTE]
>
>[!DNL Advanced Reporting] 只能用于 [!DNL Commerce] 已持续使用单个 [基础货币](../stores-purchase/currency-configuration.md).


### 步骤1：启用 [!DNL Advanced Reporting]

在 [!DNL Commerce] 配置， [[!DNL Advanced Reporting]](../configuration-reference/general/advanced-reporting.md) 默认启用，如果cron为，则自动启动 [已配置](../configuration-reference/advanced/system.md) 然后逃跑。 在接下来的24小时内，每小时开始时都会开始尝试建立订阅，直到成功。 在成功建立订阅之前，订阅状态为“挂起”。

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧导航面板中，其中 **[!UICONTROL General]** 已展开，请选择 **[!UICONTROL Advanced Reporting]** 并执行以下操作：

   * 验证 **[!UICONTROL Advanced Reporting Service]** 设置为 `Enable` （默认设置）。

   * 设置 **[!UICONTROL Time of day to send data]** 根据24小时制，您希望服务从您的商店接收更新数据的时间（小时、分钟和秒）。 默认情况下，数据在凌晨2:00发送。

   * 下 **[!UICONTROL Industry Data]**，选择 **[!UICONTROL Industry]** 最能描述您的业务的。

   ![高级报告配置](./assets/advanced-reporting-config.png){width="400"}

1. 完成后，单击 **[!UICONTROL Save Config]**.

1. 出现提示时，单击 **[[!UICONTROL Cache Management]](../systems/cache-management.md)** 并刷新任何无效的缓存。

1. 整夜等待，或等到下次计划更新时再更新。 然后，检查您的订阅的状态。 如果状态仍为 _待处理_，确保您的安装满足所有要求。

### 步骤2：访问 [!DNL Advanced Reporting]

1. 执行以下操作之一：

   * 在 _管理员_ 侧栏，选择 **[!UICONTROL Dashboard]**. 然后，单击 **[!UICONTROL Go to Advanced Reporting]**.
   * 在 _管理员_ 侧栏，转到 **[!UICONTROL Reports]** > _[!UICONTROL Business Intelligence]_>**[!UICONTROL Advanced Reporting]**.

   此 [!DNL Advanced Reporting] 仪表板提供订单、客户和产品的快速摘要。 确保向下滚动以查看完整的功能板。

1. 为了更好地查看数据，请设置 **[!UICONTROL Filters]** ，其中显示要包含在报表中的时段和存储视图。 然后，执行以下操作：

   * 将鼠标悬停在任意数据点上以了解更多信息。
   * 要查看所有功能板报表，请单击每个选项卡。

   ![数据点](./assets/reporting-advanced-data-point.png){width="600" zoomable="yes"}

## 访问 [!DNL Advanced Reporting] 数据资源

在高级报告功能板的右上角，单击 **[!UICONTROL Additional Resources]**.

![高级报告数据资源](./assets/advanced-reporting-your-data-resources.png){width="600" zoomable="yes"}

## 故障排除

如果您收到404“页面未找到”消息，请验证您的商店是否满足以下要求 [!DNL Advanced Reporting]. 然后，按照说明验证集成是否已安装。

### 验证集成是否处于活动状态

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL System]** > _[!UICONTROL Extensions]_>**[!UICONTROL Integration]**.

1. 验证 **[!UICONTROL Magento Analytics user]** 集成将显示在列表中，并且 **[!UICONTROL Status]** 是 `Active`.

1. 要重新建立用户，请单击 **[!UICONTROL Reauthorize]** 并执行以下操作：

   ![重新授权](./assets/advanced-reporting-integration-reauthorize.png){width="600"}

   * 出现提示时，单击 **[!UICONTROL Reauthorize]** 批准对API资源的访问。

     ![重新授权对API资源的访问](./assets/advanced-reporting-integration-api.png){width="600"}

   * 验证扩展的集成令牌列表是否完整。 然后，单击 **完成**.

     ![集成令牌](./assets/advanced-reporting-integration-tokens-for-extensions.png){width="600"}

1. 查找指示集成的消息 `Magento Analytics user` 已重新授权。

1. 整夜等待或等到下次计划更新时再进行。

### 验证单一基础货币

[!DNL Advanced Reporting] 只能用于 [!DNL Commerce] 仅使用单个的安装 [基础货币](../stores-purchase/currency-configuration.md) 从安装时起。 结果是，在历史记录中，所有订单都使用相同的基准货币。 [!DNL Advanced Reporting] 如果您在任何时候更改了基础货币，并且历史记录中有使用不同基础货币处理的订单，则无法正常工作。

要确定您的商店是否具有多个基本货币，您可以查询 [!DNL Commerce] 数据库从命令行使用以下MySQL示例。 您可能需要更改表名以匹配数据结构：

```sql
select distinct base_currency_code from sales_order;
```

### 数据差异

如果您注意到 `Data last updated...` 题注显示的是昨天的日期，而不是今天的日期，高级报告更新中可能会延迟多达一天。 此延迟是由于队列大小大于预期所致。

## 信息板报表

**[!UICONTROL Orders]**

| 字段 | 描述 |
|--- |--- |
| [!UICONTROL Revenue] | 显示商店视图在定义的时间段内收到的所有收入。 |
| [!UICONTROL Orders] | 显示在定义的时间段内通过商店视图下达的所有订单。 |
| [!UICONTROL AOV] | 显示在定义的时间段内通过商店视图下达的平均订单值。 |
| [!UICONTROL Refunds] | 显示在定义的时间段内通过商店视图处理的所有退款。 |
| [!UICONTROL Tax Collected] | 显示在定义的时间段内通过商店视图征收的所有税。 |
| [!UICONTROL Shipping Collected] | 显示在定义的时间段内通过商店视图收集的所有运输费用。 |
| [!UICONTROL Orders by Status] | 显示在定义的时间段内商店视图的按状态显示的订单数。 |
| [!UICONTROL Orders by Status] | 按状态列出订单数量的汇总。 |
| [!UICONTROL Coupon Usage] | 列出在定义的时间段内通过商店视图兑换的所有优惠券代码和每个优惠券的用户数。 |
| [!UICONTROL Orders and Revenue by Billing Region] | 列出在定义的时间段内商店视图的订单数和按区域列出的收入。 |
| [!UICONTROL Tax Collected by Billing Region] | 列出在定义的时间期内，按区域为商店视图征收的税额。 |
| [!UICONTROL Shipping Fees Collected by Shipping Region] | 列出在定义的时间段内按区域为商店视图收集的运输费用。 |

{style="table-layout:auto"}

**[!UICONTROL Customers]**

| 字段 | 描述 |
|--- |--- |
| [!UICONTROL Unique Customers] | 显示在定义的时间段内与商店视图关联的独特客户帐户数。 |
| [!UICONTROL New Registered Accounts] | 显示在定义的时间段内向商店视图注册的新客户帐户数。 |
| [!UICONTROL Top Coupon Users] | 按客户ID列出排名最前的优惠券用户，以及在定义的时间段内为商店视图下含优惠券的订单数。 |
| [!UICONTROL Customer KPI Table] | 列出在定义的时间段内商店视图的订单数、收入和平均订单值（按客户ID）。 |

{style="table-layout:auto"}

**[!UICONTROL Products]**

| 字段 | 描述 |
|--- |--- |
| [!UICONTROL Quantity of Products Sold] | 显示在定义的时间段内通过商店视图销售的产品数。 |
| [!UICONTROL Products Added to Wishlists] | 列出在定义的时间段内通过商店视图添加到愿望清单的所有产品。 |
| [!UICONTROL Best Selling Products by Quantity] | 列出在定义的时间段内通过商店视图销售的最畅销产品和数量。 |
| [!UICONTROL Best Selling Products by Revenue] | 列出在定义的时间段内通过商店视图销售产品时产生的畅销产品和收入。 |

{style="table-layout:auto"}


[1]: https://experienceleague.adobe.com/docs/commerce-business-intelligence/mbi/guide-overview.html
[2]: https://developer.adobe.com/commerce/php/development/advanced-reporting/
[3]: https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html

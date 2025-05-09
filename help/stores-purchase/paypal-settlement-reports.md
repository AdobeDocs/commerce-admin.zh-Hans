---
title: PayPal结算报告
description: 了解PayPal结算报表，将其作为管理PayPal交易的工具。
exl-id: cd087e15-e6ad-4472-9038-8c64fde316f9
feature: Payments
badgePaas: label="仅限PaaS" type="Informative" url="https://experienceleague.adobe.com/zh-hans/docs/commerce/user-guides/product-solutions" tooltip="仅适用于云项目(Adobe管理的PaaS基础架构)和内部部署项目上的Adobe Commerce 。"
source-git-commit: cd5b5ebec6e72ab4ba9de775bcfe8f8a89fbbb93
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 0%

---

# PayPal结算报告

PayPal结算报告为商家提供有关影响资金结算的每项交易的信息。

>[!NOTE]
>
>在生成结算报表之前，商店管理员必须请求PayPal Merchant Technical Services创建一个SFTP用户帐户，启用结算报表的生成，并在其PayPal商业帐户中启用SFTP。

在PayPal商户帐户中配置并启用结算报表后，Adobe Commerce和Magento Open Source将在以下24小时内开始生成报表。 管理员可查看可用结算报表的列表。

**_要查看结算报告：_**

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Reports]** > _[!UICONTROL Sales]_>**[!UICONTROL PayPal Settlement]**。

   ![PayPal结算报告](../getting-started/assets/reports-sales-paypal-settlement.png){width="600" zoomable="yes"}

1. 有关最新更新，请单击右上角的&#x200B;**[!UICONTROL Fetch Updates]**。

   系统连接到PayPal SFTP服务器以获取报表。 进程完成后，将显示一条消息，其中包含已获取的报告数。 此报表包含每个事务处理的以下信息：

   | 报表列 | 描述 |
   | ------------ | ----------- |
   | [!UICONTROL PayPal Reference ID Type] | 下列参考代码之一：<br/> — 订单IDT<br/> — 交易ID<br/> — 订阅ID |
   | [!UICONTROL Preapproved Payment ID] | **[!UICONTROL Custom]** — 商家在PayPal上交易时输入的文本。<br/>**[!UICONTROL Transaction Debit or Credit]**— 总额的货币流动方向。<br/>**[!UICONTROL Fee Debit or Credit]** — 费用的资金流动方向。 |

   {style="table-layout:auto"}

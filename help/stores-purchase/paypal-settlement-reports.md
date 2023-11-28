---
title: PayPal结算报告
description: 了解PayPal结算报表，将其作为管理PayPal交易的工具。
exl-id: cd087e15-e6ad-4472-9038-8c64fde316f9
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 0%

---

# PayPal结算报告

PayPal结算报告为商家提供有关影响资金结算的每项交易的信息。

>[!NOTE]
>
>在生成结算报表之前，商店管理员必须请求PayPal Merchant Technical Services创建一个SFTP用户帐户，启用结算报表的生成，并在其PayPal商业帐户中启用SFTP。

在PayPal商户帐户中配置和启用结算报表后，Adobe Commerce和Magento Open Source将在以下24小时内开始生成报表。 管理员可查看可用结算报表的列表。

**_要查看结算报表，请执行以下操作：_**

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Reports]** > _[!UICONTROL Sales]_>**[!UICONTROL PayPal Settlement]**.

   ![PayPal结算报告](../getting-started/assets/reports-sales-paypal-settlement.png){width="600" zoomable="yes"}

1. 有关最新更新，请单击 **[!UICONTROL Fetch Updates]** 在右上角。

   系统连接到PayPal SFTP服务器以获取报表。 进程完成后，将显示一条消息，其中包含已获取的报告数。 此报表包含每个事务处理的以下信息：

   | 报表列 | 描述 |
   | ------------ | ----------- |
   | [!UICONTROL PayPal Reference ID Type] | 以下参考代码之一：<br/> — 订单IDT<br/> — 交易ID<br/> — 订阅ID |
   | [!UICONTROL Preapproved Payment ID] | **[!UICONTROL Custom]**  — 商家在PayPal上输入的交易文本。<br/>**[!UICONTROL Transaction Debit or Credit]**— 总额的货币流动方向。<br/>**[!UICONTROL Fee Debit or Credit]**  — 收费资金的流动方向。 |

   {style="table-layout:auto"}

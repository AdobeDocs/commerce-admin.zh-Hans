---
title: PayPal结算报告
description: 了解PayPal结算报表，将其作为管理PayPal交易的工具。
exl-id: cd087e15-e6ad-4472-9038-8c64fde316f9
feature: Payments
badgePaas: label="仅限PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="仅适用于云项目（Adobe管理的PaaS基础架构）和内部部署项目上的Adobe Commerce 。"
TQID: https://experienceleague.adobe.com/c7v5oSsVPmD6r6obfGEoxPiGkMI4KMWAmfJAW0-CCJk
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 233
ht-degree: 0%

---

# PayPal结算报告

PayPal结算报告为商家提供有关影响资金结算的每项交易的信息。

>[!NOTE]
>
>在生成结算报表之前，商店管理员必须请求PayPal Merchant Technical Services创建一个SFTP用户帐户，启用结算报表的生成，并在其PayPal商业帐户中启用SFTP。

在PayPal商户帐户中配置并启用结算报表后，Adobe Commerce和Magento Open Source将在以下24小时内开始生成报表。 管理员可查看可用结算报表的列表。

**_查看结算报告:_**

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Reports]** > _[!UICONTROL Sales]_>**[!UICONTROL PayPal Settlement]**。

   ![PayPal结算报告](../getting-started/assets/reports-sales-paypal-settlement.png){width="600" zoomable="yes"}

1. 有关最新更新，请单击右上角的&#x200B;**[!UICONTROL Fetch Updates]**。

   系统连接到PayPal SFTP服务器以获取报表。 进程完成后，将显示一条消息，其中包含已获取的报告数。 此报表包含每个事务处理的以下信息：

   | 报表列 | 描述 |
   | ------------ | ----------- |
   | [!UICONTROL PayPal Reference ID Type] | 下列参考代码之一：<br/> — 订单IDT<br/> — 交易ID<br/> — 订阅ID |
   | [!UICONTROL Preapproved Payment ID] | **[!UICONTROL Custom]** — 商家在PayPal上交易输入的文本。<br/>**[!UICONTROL Transaction Debit or Credit]**— 总额的货币流动方向。<br/>**[!UICONTROL Fee Debit or Credit]**  — 收费资金的流动方向。 |

   {style="table-layout:auto"}

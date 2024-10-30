---
title: “[!UICONTROL My Quote Templates]”
description: 了解报价模板的客户体验，该体验可在店面帐户信息板中获取。
feature: B2B, Companies, Quotes
source-git-commit: c2cb4db24effa764996b0fb77fbda67727392efe
workflow-type: tm+mt
source-wordcount: '729'
ht-degree: 0%

---


# [!UICONTROL My Quote Templates]

如果启用了报价，则客户帐户仪表板的&#x200B;_[!UICONTROL My Quotes Template]_部分将列出与客户帐户关联的所有报价模板。 根据他们的权限，只有代表公司进行采购的采购员才能请求报价模板，并协商报价定价和重复订单条款。

![我的报价模板](./assets/account-dashboard-quote-templates-list.png){width="700" zoomable="yes"}

报价模板列表按状态组织模板。

- **[!UICONTROL Active Quote Templates]**&#x200B;列出了已协商并批准使用的模板。 信息包括最小报价总额和下达的订单（如果在洽谈流程中配置了这些选项）。 买方可以从模板生成链接报价，以根据报价条款提交订单。

- **[!UICONTROL In Review]**&#x200B;在协商过程中列出模板，显示当前状态并提供链接以打开模板。

- **[!UICONTROL Inactive]**&#x200B;列出了已过期、已取消或因买方已用完允许的承诺订单数而不再有效的模板。

对于买方而言，*[!UICONTROL My Quotes Templates]*&#x200B;页面是谈判过程中买方与卖方之间所有通信的焦点。

接受卖方提供的议定条款的买方可以接受模板，然后使用该模板生成可用于下订单的预批准链接报价。

- 与管理报价模板相关的操作：

   - 取消模板
   - 发送给卖方进行审核
   - 接受报价模板
   - 更改报价单模板到期日期
   - 添加送货地址

- 在洽谈过程中更新报价模板详细信息的活动：

   - 复查项目定价和更新。
   - 如果报价模板上配置了数量阈值，请调整最小值和最大值。
   - 跟踪来自[!UICONTROL Comments]和[!UICONTROL History]部分的协商进程。
   - 对于仍在审阅的模板，买方可以通过删除项目来修改报价模板。
   - 通过在明细项目和报价级别添加备注，与卖方进行沟通和协商。

  进行更改后，买方将模板退回给卖方进行审阅。

- 协商过程中的常规操作：

   - 将报价模板发送给卖方以供审阅
   - 接受报价模板
   - 取消以结束洽谈并关闭报价

以下示例显示了一个报价模板，该模板已由买方更新并发送回卖方以供审阅。

![报价模板的买方视图](./assets/account-dashboard-my-quote-template-detailed.png){width="700" zoomable="yes"}

状态为`Submitted`的模板将被锁定，直到卖家审阅并更新模板并将其返回给买家。

## 创建报价模板

采购员可以使用以下任一方法开始报价模板洽谈流程：

- 通过单击&#x200B;**[!UICONTROL Create quote template]**&#x200B;操作，从现有报价单中创建模板。

- 从店面提交报价请求，并添加注释，要求销售代表根据报价请求创建报价模板。

## 查看报价模板

1. 购买者登录到他们的帐户。

1. 在左侧面板中，选择&#x200B;**[!UICONTROL My Quote Templates]**。

1. 在列表中查找报价模板，然后单击&#x200B;_[!UICONTROL Action]_列中的&#x200B;**[!UICONTROL View]**。

## 添加送货地址

在报价模板具有送货地址之前，买方不能接受该模板。

1. 购买者登录到他们的帐户。

1. 在左侧面板中，选择&#x200B;**[!UICONTROL My Quote Templates]**。

1. 选择所需的报价模板。

1. 在&#x200B;**[!UICONTROL Shipping Information]**&#x200B;部分中，单击&#x200B;**[!UICONTROL Add New Address]**。

1. 填写新地址的详细信息。

1. 单击&#x200B;**[!UICONTROL Save Address]**。

买方添加地址后，他们将模板发回卖方进行审阅。 卖方提供运输和交货选项。 这些更新可能会影响协商报价的定价。 结账时将锁定送货选项。

## 生成链接报价

采购员接受报价模板后，即可使用&#x200B;**[!UICONTROL Generate a quote]**&#x200B;操作从&#x200B;*[!UICONTROL My Quote Templates dashboard]*&#x200B;或报价模板中生成预批准的链接报价。

链接的报价包含通知，表明它已被批准并准备好结帐。 它还提供了标头信息中指向报价模板的链接。

![从报价模板生成的链接报价](./assets/quote-templates-linked-quote.png){width="700" zoomable="yes"}

如果报价模板配置了订单阈值，则当生成链接的报价时，计数将递增。

采购员可以从链接报价完成以下操作：

- 如果报价配置了数量阈值，请调整行项目的订单数量。
- 继续结帐以提交订单。
- 删除或打印报价。
- 打开用于生成报价的报价模板。

## 取消报价模板

在报价模板页面中，单击&#x200B;**[!UICONTROL Cancel Quote Template]**。

报价模板已取消，报价状态更改为`Closed`。 已关闭的引号将保留在您的&#x200B;*[!UICONTROL Inactive]*&#x200B;引号列表中，并且仍然列在管理员的&#x200B;_[!UICONTROL Quote Templates]_网格中。





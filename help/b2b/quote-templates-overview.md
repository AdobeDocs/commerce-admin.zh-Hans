---
title: 报价模板用例和工作流
description: 从现有报价创建报价模板，以简化经常性订单的报价洽谈。
feature: B2B, Quotes
source-git-commit: 3000d9abab467a86e37c7eca6e7db16b39c763ab
workflow-type: tm+mt
source-wordcount: '970'
ht-degree: 0%

---


# 报价模板用例和工作流

“报价模板”功能允许买方和卖方通过创建可重复使用且可自定义的报价模板来简化报价流程。

- **可自定义的报价** — 采购员可以从预批准的模板生成链接报价，从而允许在指定的参数（如行项目数量和选择）中进行自定义。
- **订单阈值** — 卖方可以设置最小和最大订单承诺，确保买方遵守商定的购买量。
- **到期日期** — 模板可以具有有效期，确保这些条款只在指定的时间范围内适用。
- **折扣和定价** — 销售商可以使用与报价一起提供的相同行项目、报价级别和发运价格折扣功能为经常性订单设置折扣，从而简化洽谈流程。
- **跟踪和报告** — 系统跟踪从模板生成的链接报价数，并成功完成订单，以便深入了解商定的订单配额的履行情况。

## 用例

公司采购员可以使用报价模板在一段时间内订购一组特定产品。 买方配置以下报价模板选项，以使报价流程更高效、更一致且与战略采购协议保持一致。

- 订单阈值，用于指定适用于协议定价的最小和最大订单数。 这可用于应用和跟踪合同协议中指定的订单配额。

- 数量阈值（最小/最大数量）模板指定数量阈值，以设置每个订单可购买的最小和最大数量，从而确保卖方能够有效地管理库存水平，同时使买方能够根据需要灵活地调整数量。

## 报价模板工作流

报价模板可由买方或卖方启动。

**步骤1：报价模板创建（新建）**

- **采购员创建报价模板**

  在查看现有报价模板时，买方决定公司需要在下一年提交多个订单，并且希望根据重复的业务请求额外的折扣。 他们使用报价上的&#x200B;*[!UICONTROL Create quote template]*&#x200B;操作创建报价模板。 然后，他们将新模板发送给卖方进行审阅，开始谈判。

  购买者还可以直接从店面的&#x200B;*[!UICONTROL My Quote Templates]**页面创建报价模板。

- **销售代表** — 销售代表可以从管理员中代表特定公司买方创建报价模板。 销售代表可以在管理员中通过现有报价或[!UICONTROL Quote Templates]网格创建报价模板，并将其保存为`draft`或发送给买方以开始洽谈。 在草稿状态下，报价仅对卖方可见。 发送报价后，状态为`Submitted`。 在买方将其发回之前，卖方不能对其进行修改。

  ![卖方从Admin的Quotes网格中启动买方报价](./assets/quote-template-create-from-grid.png){width="700" zoomable="yes"}

**步骤2：报价审核和协商（审核）**

复查或洽谈报价模板可以包括更改数量、删除项目、添加行项目备注、应用行项目或报价折扣（卖方）以及添加发运地址（买方）。

- **卖方查看请求并发送回应** — 在管理员中，卖方从&#x200B;*[!UICONTROL Quote Templates]**网格查看报价模板，或从电子邮件通知中的链接打开报价模板。 在店面，报价的状态更改为`Pending`，买方无法进行任何更改。 在对[报价洽谈](quote-price-negotiation.md)执行相同的流程后，卖方通过提供价格折扣并根据需要调整数量和项目来进行回应，输入备注并将报价发送回买方。 通过电子邮件通知买方和销售代表，卖方已作出回应。

- **买方查看卖方的报价模板并发送回应** — 买方单击电子邮件通知中的链接打开报价模板，或从帐户仪表板的&#x200B;_我的报价模板_&#x200B;页面打开报价。 采购员可以在行项目或报价层向卖方留下附注、更改数量以及移除项目。

买方和卖方继续协商过程，直到达成协议或卖方拒绝报价模板。 如果采购员更改报价 — 添加或删除产品或更改产品数量 — 则必须将报价返回给卖方进行复查。

- **采购员添加送货地址** — 采购员必须在报价模板中添加送货地址（如果没有）。 在买方添加地址之后，卖方可以提供运输和交货选项。 显示的配送方式取决于Storefront配置。

如果买方添加发运地址，则必须复查洽谈协议，并且卖方可以继续洽谈流程，直到达成协议或卖方拒绝报价模板为止。

**步骤3：买方接受报价模板**

买方接受模板中的议定条款。 在报价模板被接受之后，采购员可以使用它来生成预批准的链接报价，这些报价可用于提交订单，而无需进一步洽谈。

结帐时锁定送货选项。

### 查看报价模板

1. 在记录的&#x200B;**[!UICONTROL Actions]**&#x200B;列中，单击&#x200B;**[!UICONTROL View]**。

1. 要响应客户请求，请按照说明开始用于洽谈报价的相同[价格洽谈](quote-price-negotiation.md)流程。

### 查看报价模板活动

从[!UICONTROL Comments]和[!UICONTROL History Log]中查看洽谈时间线、通信和其他报价活动 — 信息包括状态更改、客户和发运信息的更新、物料和价格更新以及其他重要信息。

1. 打开报价模板。

1. 通过滚动到&#x200B;**[!UICONTROL Negotiation]**&#x200B;并选择&#x200B;**[!UICONTROL Comments]**&#x200B;和&#x200B;**[!UICONTROL History Log]**&#x200B;来查看报价议价备注和历史记录。

   ![查看历史记录](./assets/quote-view-history.png){width="400"}

1. 还会在行项目层跟踪历史记录。

   ![查看行项目历史记录](./assets/quote-view-line-item-history.png){width="400"}


### 拒绝报价模板

只能拒绝状态为`In Review`的报价模板。

1. 从&#x200B;*[!UICONTROL Quote Templates]*&#x200B;网格中，打开要拒绝的报价模板。

1. 在报价模板上，单击&#x200B;**[!UICONTROL Decline]**。

1. 出现提示时，输入报价被拒绝的原因，然后单击&#x200B;**[!UICONTROL Confirm]**。
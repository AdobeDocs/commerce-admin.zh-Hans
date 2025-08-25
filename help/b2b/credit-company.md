---
title: 管理公司信用
description: 了解公司信用额度、设置参数和处理分期付款信息。
exl-id: 62ff2a36-053d-4ba0-9969-0f05701afbff
feature: B2B, Companies, Payments
role: Admin
source-git-commit: 1fc1e07f20e2c22ac430f384e9e2b278edae405c
workflow-type: tm+mt
source-wordcount: '1223'
ht-degree: 0%

---

# 管理公司信用

公司信贷允许B2B企业根据预先批准的信贷额度进行购买，而不是要求立即付款。 启用[帐户付款](../b2b/enable-basic-features.md#configure-payment-on-account)后，公司最多可以购买其信用额度，并从帐户信息板查看其信用状态。

![公司信用](./assets/company-create-credit-admin.png){width="700" zoomable="yes"}

公司信用使您能够：

* **延长信用期限** — 允许受信任的业务客户以延期付款分期购买
* **设置信用额度** — 通过为每个公司设置信用额度来控制财务风险
* **跟踪信用活动** — 实时监控所有信用交易、付款和未清余额
* **简化B2B事务** — 简化已建立信用关系的公司的采购流程
* **支持复杂的工作流** — 与采购订单、报价和批准流程集成

## 先决条件

在设置公司点数之前，请确保：

* B2B功能已在Adobe Commerce安装中启用
* [帐户](../b2b/enable-basic-features.md#configure-payment-on-account)付款已配置并启用
* 公司帐户已正确设置必要的业务信息
* 您具有管理公司信用设置的管理权限
* 如果使用多种货币操作，则配置货币设置

## 用例

公司信贷非常适合：

* **已建立的B2B关系** — 具有经验证的付款记录的长期业务客户
* **大型企业客户** — 进行大量常规购买且需要延长付款期限的公司
* **季节性业务** — 具有周期性现金流、需要灵活付款时间的公司
* **公司采购** — 具有集中采购但分布式付款处理的组织
* **供应链合作伙伴** — 需要信贷机制的分销商、转销商和渠道合作伙伴

## 了解公司信用设置

您可以为每个公司配置文件配置以下与信用相关的参数：

* **贷方币种** — 所有贷方交易和余额的币种
* **信用额度** — 公司随时可以缺的最大金额
* **允许超出信用额度** — 公司是否可以下超出可用信用额度的订单
* **更改原因** — 用于记录信用设置修改的文档字段

有关这些设置和配置公司配置文件的详细信息，请参阅[创建公司帐户](account-company-create.md)。

>[!NOTE]
>
>如果公司有未清余额，则在管理员查看时，将向销售订单顶部的商店管理员显示通知。 这有助于确保在订单处理期间了解信用状态。

## 公司信用活动

公司配置文件的[!UICONTROL Company Credit]部分以网格格式显示所有信用交易、余额更改和付款活动的完整历史记录。

![公司信用活动](./assets/company-credit-reimbursements-grid.png){width="700" zoomable="yes"}

网格显示每个事务处理的以下信息：

| 列 | 描述 |
|--- |--- |
| [!UICONTROL Date] | 交易的日期。 要显示日期和时间，请将鼠标悬停在日期上。 |
| [!UICONTROL Operation] | 与交易记录关联的活动的类型。 值： <br/>**[!UICONTROL Allocated]**— 分配给公司的信用。<br/>**[!UICONTROL Updated]** — 更改应用于以下字段之一：[!UICONTROL Credit limit] / [!UICONTROL Credit currency] / [!UICONTROL Allow to exceed credit limit] <br/>**[!UICONTROL Purchased]**— 已下订单。<br/>**[!UICONTROL Reimbursed]** — 已偿还未清余额。 <br/>**[!UICONTROL Refunded]**— 贷项通知单金额已退款。<br/>**[!UICONTROL Reverted]** — 订单已取消，金额已返回贷方余额。 |
| [!UICONTROL Amount] | 与以下交易类型关联的交易金额： `Purchased` / `Reimbursed` / `Refunded` / `Reverted` <br/>对于购买金额，金额以商店的显示货币和贷方货币设置的格式显示，后跟当前兑换率（如果适用）。 例如：<br/>EUR 20,000.00 ($22,400.00) <br/>USD/EUR 0.8928 |
| [!UICONTROL Outstanding Balance] | 退款金额减去使用“分期付款”方法下达的所有订单的应付总额。 数量可能显示为正值或负值。 <br/>**[!UICONTROL Positive value]**— 预付款以正值表示。<br/>**[!UICONTROL Negative value]** — 到期金额表示为负值。 |
| [!UICONTROL Available Credit] | _[!UICONTROL Credit Limit]_和_[!UICONTROL Outstanding Balance]_&#x200B;的总和。 如果公司已超出信用限额，则金额将显示为负值。 |
| [!UICONTROL Credit Limit] | 给予公司的贷方金额。 |
| [!UICONTROL Updated By] | 发起操作的人员的姓名。 |
| [!UICONTROL Custom Reference Number] | 与交易记录关联的自定义参考编号。 |
| [!UICONTROL Comment] | 根据操作类型，`Reason for Change`字段中的值的编译。 <br/>**[!UICONTROL Purchased]**— 包含采购注释、订单编号和订单链接。<br/>**[!UICONTROL Reimbursed]** — 包含已报销交易记录的注释。 |
| [!UICONTROL Action] | 仅用于`Reimbursed`操作。 **[!UICONTROL Edit]** — 允许更新报销金额。 |

{style="table-layout:auto"}

## 更新信用信息

当客户付款时，管理员会在管理员中更新信用信息。

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**客户>公司**。

1. 在网格中查找公司并在&#x200B;_编辑_&#x200B;模式下打开。

1. 展开&#x200B;**公司业绩**&#x200B;部分。

1. 对于&#x200B;**信用额度**，请输入新值。

1. 根据需要更改其他值。

1. 更新完成后，单击&#x200B;**[!UICONTROL Save]**。

## 接收付款

偿还余额是公司对其帐户余额进行的离线付款。 商店管理员使用&#x200B;_报销余额_&#x200B;按钮，在公司配置文件中手动输入金额。 在提交金额时，系统会重新计算未清余额和可用的公司信用，并在公司信用历史记录中记录操作。 按照配置中的指定，以贷方币种输入偿还金额。

### 用付款核销公司帐户

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Customers]** > **[!UICONTROL Companies]**。

1. 在列表中查找公司记录并在&#x200B;**[!UICONTROL Edit]**&#x200B;模式下打开。

1. 在页面顶部，单击&#x200B;**偿还余额**。

1. 在对话框中，添加付款信息：

   ![报销余额](./assets/company-reimburse-balance.png){width="500"}

   * 输入付款的&#x200B;**金额**。

     金额可以输入为正值或负值。

   * 如果适用，请输入&#x200B;**自定义参考编号**&#x200B;以供参考。

     每个报销只能输入一个自定义参考编号。 要将付款应用于多个PO，请为每个PO创建单独的报销。

   * 根据需要，输入&#x200B;**注释**&#x200B;以描述报销情况。

1. 单击&#x200B;**报销**。

   系统会自动更新余额和信用历史记录以反映报销情况。

### 编辑报销

1. 以&#x200B;**[!UICONTROL Edit]**&#x200B;模式打开公司配置文件。

1. 展开![公司业绩](../assets/icon-display-expand.png)部分的&#x200B;**扩展选择器**。

1. 在网格中查找报销交易记录，然后单击&#x200B;**[!UICONTROL Edit]**。

1. 对&#x200B;**自定义参考编号**&#x200B;和&#x200B;**评论**&#x200B;进行任何必要的更改。

   无法更改报销金额。

1. 单击&#x200B;**[!UICONTROL Save]**。

## 店面信用信息

公司管理员可以在帐户信息板上查看其信用信息，包括未结余额、可用信用、信用额度和未结发票。 取消订单后，金额将返回至公司余额，并显示在“信用分配历史记录”字段中。

![公司信用](./assets/company-credit.png){width="700" zoomable="yes"}

## 公司信用演示

通过观看此演示视频了解如何管理公司信用：

>[!VIDEO](https://video.tv.adobe.com/v/344445?quality=12&learn=on)

## 安全性注意事项

在管理公司信用时，实施强有力的安全措施以保护敏感的金融数据：

* **访问控制** — 将信用管理权限限制为仅授权人员
* **审核跟踪** — 维护所有信用交易和修改的完整日志
* **数据保护** — 对传输中或静止的财务敏感信息进行加密
* **审批工作流** — 为重大信用调整实施多级审批流程
* **定期审核** — 定期审核用户访问和信用关系

## 最佳实践

* 
   * **信用政策管理** — 在管理公司信用时，建立明确的政策来根据客户付款历史记录和业务关系设置信用额度。 定期审查未清余额和支付模式以评估风险，并始终用详细的审计原因记录信贷设置的变化。

及时处理付款以保持准确的余额，并确保信用货币设置与每个公司的主要业务运营保持一致。

* **法规遵从性和安全性** — 将信用管理权限限制为仅授权人员，实施重大信用调整的审批工作流，并根据您组织的安全策略保护敏感财务信息。 定期审查用户访问和信用关系有助于保持适当的监督和合规性。

>[!MORELIKETHIS]
>
>* [启用B2B功能](enable-basic-features.md) *配置分期付款和其他B2B功能
>* [创建公司帐户](account-company-create.md) *设置具有信用功能的公司帐户
>* [管理公司](manage-companies.md) *公司管理功能概述
>* [公司角色和权限](account-company-roles-permissions.md) *配置信用管理的用户访问权限
>* [采购订单工作流](purchase-order-flow.md) *了解信用如何与采购订单集成
>* [B2B配置引用](../configuration-reference/general/b2b-features.md) - B2B功能的详细配置设置

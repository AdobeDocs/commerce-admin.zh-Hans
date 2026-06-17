---
title: 商店点数
description: 商店贷记是还原到客户帐户的金额，可用于支付购买或现金退款。
exl-id: 1fe627dd-5c49-4ff8-85e0-3c987285726d
feature: Customers, Storefront
TQID: https://experienceleague.adobe.com/kG-y-O2Yh-h1ct-oCwqylZFvS2FOCXFPD6qVIkKrpbg
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
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
source-wordcount: 291
ht-degree: 0%

---

# 商店点数

{{ee-feature}}

商店贷记是还原到客户帐户的金额。 客户可以使用商店积分支付购买费用，管理员可以使用商店积分支付现金退款。 礼品卡余额可贷记到客户的帐户，而不是使用礼品卡代码进行将来购买。

在支付订单并开票后，可通过[签发贷项通知单](../stores-purchase/credit-memo-create.md)来退款该订单或订单的一部分。 贷项通知单与退款不同，因为贷项金额会还原到客户帐户，以便将来购买。 有时，可以在签发贷项通知单的同时提供退款，并应用于客户的商店贷记余额。 在配置中指定客户帐户中可用的商店贷记金额。

>[!NOTE]
>
>如果商店积分涵盖订单总额，则必须启用&#x200B;[_零小计结帐_](../stores-purchase/zero-subtotal-checkout.md)&#x200B;付款方法。

## 存储信用工作流

1. **客户登录** — 客户在开始结帐流程之前登录到帐户。

1. **使用商店** — 信用在结账流程的&#x200B;[!UICONTROL _审核和付款_]&#x200B;步骤中，客户选择&#x200B;[!UICONTROL _使用商店信用_]&#x200B;作为付款选项。 可用余额显示在括号中。 如果可用余额大于总计，则不再显示其他付款方法。

1. **应用于订单的贷项** — 应用于订单的商店贷项金额将与订单总额一起显示，并从总计中减去。

1. **已调整客户余额** — 下达订单时调整客户的可用余额。

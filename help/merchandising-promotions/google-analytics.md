---
title: '[!DNL Google Analytics]'
description: 了解如何使用 [!DNL Google Analytics] 以收集用于您的Commerce网站的有用量度。
exl-id: d4df2ef2-d67f-46bf-8569-cbee9dde77e4
feature: Marketing Tools, Integration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '735'
ht-degree: 0%

---

# [!DNL Google Analytics]

[!DNL Google Analytics] 让您能够定义额外的自定义维度和量度以进行跟踪，并支持离线和移动设备应用程序交互，以及访问正在进行的更新。 [!DNL Google Analytics] 4是Google的下一代测量解决方案，并且正在取代 [!DNL Universal Analytics]. 在2023年7月1日，标准Universal Analytics属性将停止处理新点击。

>[!NOTE]
>
>如果您的业务受隐私法规的约束，例如 [通用数据保护条例](../getting-started/compliance-gdpr.md) 和/或 [《加州消费者隐私法案》](../getting-started/compliance-ccpa.md)，请参见 [Google隐私设置](google-tools.md#google-privacy-settings).

>[!IMPORTANT]
>
>如果您启用 [Cookie限制模式](../getting-started/compliance-cookie-law.md)， [!DNL Google Analytics] 除非访客已接受Cookie，否则不会收集有关访客的数据。

## [!DNL Google Analytics] 4

{{gtag-api-note}}

### 第1步：设置 [!UICONTROL Google Analytics] 4

如果您还没有 [!DNL Google Analytics] 4按照以下方法之一设置您的站点：

- [首次设置Analytics数据收集](https://support.google.com/analytics/answer/9304153)
- [使用以下方式将Google Analytics4添加到站点 [!DNL Universal Analytics]](https://support.google.com/analytics/answer/9744165)

### 步骤2：完成Commerce配置

1. 登录Commerce商店的管理员。

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中，展开 **[!UICONTROL Sales]** 并选择 **[!UICONTROL Google API]**.

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Google GTag]** 部分。

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Google Analytics4]** 子部分并执行以下操作：

   - 设置 **[!UICONTROL Enable]** 到 `Yes`.

   - 离开 **[!UICONTROL Account type]** 作为 `Google Analytics4`.

   - 输入您的 **[!UICONTROL Measurement ID]**. 要了解更多信息，请参阅 [Google Analytics帮助](https://support.google.com/analytics/answer/9539598).

   - 如果要对内容执行A/B测试和其他性能测试，请设置 **内容实验** 到 `Yes`.

   ![Sales配置 — 适用于Google Analytics4的Google API](../configuration-reference/sales/assets/google-api-gtag-google-analytics4.png){width="600" zoomable="yes"}

1. 完成后，单击 **[!UICONTROL Save Config]**.

## Google Universal Analytic

>[!IMPORTANT]
>
>2023年7月1日，标准Universal Analytics属性将不再处理数据。 如果你还依靠 [!DNL Universal Analytics]，建议您 [准备使用Google Analytics4](https://support.google.com/analytics/answer/10759417) 往前走。

### 步骤1：设置Google Universal Analytics

访问Google网站，并注册 [Google Universal Analytic][1] 帐户。

### 步骤2：完成Commerce配置

1. 登录Commerce商店的管理员。

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中，展开 **[!UICONTROL Sales]** 并选择 **[!UICONTROL Google API]**.

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Google Analytics]** 部分并执行以下操作：

   - 设置 **[!UICONTROL Enable]** 到 `Yes`.

   - 输入您的 [!DNL Google Analytics] **[!UICONTROL Account Number]**.

   - 如果要对内容执行A/B测试和其他性能测试，请设置 **[!UICONTROL Content Experiments]** 到 `Yes`.

   ![Sales配置 — Google API -Google Analytics](../configuration-reference/sales/assets/google-api-analytics-ee.png){width="600" zoomable="yes"}

1. 完成后，单击 **[!UICONTROL Save Config]**.

## 增强型电子商务

“增强型电子商务”是 [!DNL Google Universal Analytics] 这让您能够深入了解客户的购物和购买行为。 您可以使用增强型电子商务生成有关关键客户活动的报表，例如，当客户在购物车中添加商品、开始结帐流程或完成购买时。 您还可以识别和分析放弃购物而不进行购买的购物者的模式。

以下说明显示如何配置 [!DNL Google Tag Manager] 替换为 [!DNL Universal Analytics] 以生成增强的电子商务数据和报表。

### 步骤1. 注册Google帐户

1. 注册一个 [Google Tag Manager](google-tag-manager.md) 帐户，并完成Commerce配置。

1. 注册新 [Google Universal Analytic][1] 帐户。

### 步骤2. 配置增强型电子商务

1. 登录到您的Google Universal Analytics帐户。

1. 使用以下设置为增强型电子商务分析创建属性：

   - 状态：打开
   - 相关产品：打开
   - 启用增强型电子商务报表：开启
   - 签出标签： （非必需）

1. 完成后，单击 **[!UICONTROL Submit]**.

### 步骤3. 创建标记和触发器

1. 登录到您的 [!DNL Google Tag Manager] 帐户并创建以下触发器：

   | 名称 | 事件类型 | 筛选 |
   |--- |--- |--- |
   | `addToCart` | 自定义事件 |  |
   | `checkout` | 自定义事件 |  |
   | `checkout only` | 页面查看 | 页面URL与RegEx /checkout/匹配。* |
   | `checkoutOption` | 自定义事件 |  |
   | `gtm.dom` | 自定义事件 |  |
   | `productClick` | 自定义事件 |  |
   | `promotionClick` | 自定义事件 |  |
   | `removeFromCart` | 自定义事件 |  |

   >[!NOTE]
   >
   >此 [!UICONTROL Checkout] 仅针对内置Commerce基本支付方法触发事件(例如 `Check / Money Order` 和 `Cash On Delivery Payment`)。 此事件不执行的对象 `PayPal checkout` 以及其他外部支付方式，这些方式使用从外部资源重定向到结账。

1. 使用相同的基本配置创建以下Universal Analytics标记。

   - Universal Analytics标记

     | 名称 | 类型 | 触发触发器 |
     |--- |--- |--- |
     | `Add to cart tracking` | Universal Analytics | addToCart |
     | `Checkout option tracking` | Universal Analytics | checkoutOption |
     | `Checkout tracking` | Universal Analytics | 结账 |
     | `Pageview tracking` | Universal Analytics | gtm.dom |
     | `Product click tracking` | Universal Analytics | productClick |
     | `Promo click tracking` | Universal Analytics | promotionClick |
     | `Remove from cart tracking` | Universal Analytics | removeFromCart |

   - 基本标记配置

     | 设置 | 值 |
     |--- |--- |
     | [!UICONTROL Product] | Google Analytics |
     | [!UICONTROL Tag Type] | Universal Analytics |
     | [!UICONTROL Tracking ID] | UA-XXX（来自Universal Analytics帐户的跟踪ID。） |
     | [!UICONTROL Enable Enhanced Ecommerce Features] | True |
     | [!UICONTROL Use data layer] | True |
     | [!UICONTROL Use Debug version] | True |

1. 完成各个跟踪配置。

   - 输入以下内容 **[!UICONTROL Add to Cart]** 跟踪设置：

     | 设置 | 值 |
     |--- |--- |
     | [!UICONTROL Track Type] | Event |
     | [!UICONTROL Category] | 电子商务 |
     | [!UICONTROL Action] | 添加到购物车 |
     | [!UICONTROL Trigger] | addToCart |

   - 输入以下内容 **[!UICONTROL Checkout option]** 跟踪设置：

     | 设置 | 值 |
     |--- |--- |
     | [!UICONTROL Track Type] | Event |
     | [!UICONTROL Category] | 电子商务 |
     | [!UICONTROL Action] | 签出选项 |
     | [!UICONTROL Trigger] | checkoutOption |

   - 输入以下内容 **[!UICONTROL PageView]** 跟踪设置：

     | 设置 | 值 |
     |--- |--- |
     | [!UICONTROL Track Type] | 页面查看 |
     | [!UICONTROL Trigger] | gtm.dom |

   - 完成以下操作 **[!UICONTROL Product Click]** 跟踪配置：

     | 设置 | 值 |
     |--- |--- |
     | [!UICONTROL Track Type] | Event |
     | [!UICONTROL Category] | 电子商务 |
     | [!UICONTROL Action] | 产品点击量 |
     | [!UICONTROL Trigger] | productClick |

   - 完成以下操作 **[!UICONTROL Promotion Click]** 跟踪配置：

     | 设置 | 值 |
     |--- |--- |
     | [!UICONTROL Track Type] | Event |
     | [!UICONTROL Category] | 电子商务 |
     | [!UICONTROL Action] | 促销活动点击 |
     | [!UICONTROL Trigger] | promotionClick |

   - 完成以下操作 **[!UICONTROL Remove from Cart]** 跟踪配置：

     | 设置 | 值 |
     |--- |--- |
     | [!UICONTROL Track Type] | Event |
     | [!UICONTROL Category] | 电子商务 |
     | [!UICONTROL Action] | 从购物车中移除 |
     | [!UICONTROL Trigger] | removeFromCart |

1. 完成后，单击 **[!UICONTROL Preview]** 并验证标记是否正常工作。

1. 验证设置后，单击 **[!UICONTROL Publish]**.


[1]: https://support.google.com/analytics/answer/2817075?hl=en

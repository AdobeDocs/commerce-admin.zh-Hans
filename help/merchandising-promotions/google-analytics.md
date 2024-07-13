---
title: '[!DNL Google Analytics]'
description: 了解如何使用 [!DNL Google Analytics] 为Commerce网站收集有用的量度。
exl-id: d4df2ef2-d67f-46bf-8569-cbee9dde77e4
feature: Marketing Tools, Integration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '731'
ht-degree: 0%

---

# [!DNL Google Analytics]

[!DNL Google Analytics]使您能够定义用于跟踪的其他自定义维度和量度，支持离线和移动设备应用程序交互，并可访问正在进行的更新。 [!DNL Google Analytics] 4是Google的新一代测量解决方案，正在替换[!DNL Universal Analytics]。 在2023年7月1日，标准Universal Analytics属性将停止处理新点击。

>[!NOTE]
>
>如果您的业务受隐私法规约束，例如[通用数据保护条例](../getting-started/compliance-gdpr.md)和/或[加州消费者隐私法案](../getting-started/compliance-ccpa.md)，请参阅[Google隐私设置](google-tools.md#google-privacy-settings)。

>[!IMPORTANT]
>
>如果启用[Cookie限制模式](../getting-started/compliance-cookie-law.md)，[!DNL Google Analytics]将不会收集有关访客的数据，除非他们已接受Cookie。

## [!DNL Google Analytics] 4

{{gtag-api-note}}

### 步骤1：设置[!UICONTROL Google Analytics] 4

如果您还没有为网站设置[!DNL Google Analytics] 4，请按照以下方法之一操作：

- [首次设置Analytics数据收集](https://support.google.com/analytics/answer/9304153)
- [将Google Analytics4添加到具有 [!DNL Universal Analytics]](https://support.google.com/analytics/answer/9744165)的网站

### 步骤2：完成Commerce配置

1. 登录到您的Commerce商店的管理员。

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧面板中，展开&#x200B;**[!UICONTROL Sales]**&#x200B;并选择&#x200B;**[!UICONTROL Google API]**。

1. 展开&#x200B;**[!UICONTROL Google GTag]**&#x200B;部分的![扩展选择器](../assets/icon-display-expand.png)。

1. 展开&#x200B;**[!UICONTROL Google Analytics4]**&#x200B;子部分的![扩展选择器](../assets/icon-display-expand.png)并执行以下操作：

   - 将&#x200B;**[!UICONTROL Enable]**&#x200B;设置为`Yes`。

   - 将&#x200B;**[!UICONTROL Account type]**&#x200B;保留为`Google Analytics4`。

   - 输入您的&#x200B;**[!UICONTROL Measurement ID]**。 若要了解详细信息，请参阅[Google Analytics帮助](https://support.google.com/analytics/answer/9539598)。

   - 如果要对内容执行A/B测试和其他性能测试，请将&#x200B;**内容实验**&#x200B;设置为`Yes`。

   ![Sales配置 — 适用于Google Analytics的Google API 4](../configuration-reference/sales/assets/google-api-gtag-google-analytics4.png){width="600" zoomable="yes"}

1. 完成后，单击&#x200B;**[!UICONTROL Save Config]**。

## Google Universal Analytic

>[!IMPORTANT]
>
>2023年7月1日，标准Universal Analytics属性将不再处理数据。 如果您仍然依赖[!DNL Universal Analytics]，则建议您[准备以后使用Google Analytics4](https://support.google.com/analytics/answer/10759417)。

### 步骤1：设置Google Universal Analytics

访问Google网站，并注册[Google Universal Analytics][1]帐户。

### 步骤2：完成Commerce配置

1. 登录到您的Commerce商店的管理员。

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧面板中，展开&#x200B;**[!UICONTROL Sales]**&#x200B;并选择&#x200B;**[!UICONTROL Google API]**。

1. 展开&#x200B;**[!UICONTROL Google Analytics]**&#x200B;部分中的![扩展选择器](../assets/icon-display-expand.png)并执行以下操作：

   - 将&#x200B;**[!UICONTROL Enable]**&#x200B;设置为`Yes`。

   - 输入您的[!DNL Google Analytics] **[!UICONTROL Account Number]**。

   - 如果要对内容执行A/B测试和其他性能测试，请将&#x200B;**[!UICONTROL Content Experiments]**&#x200B;设置为`Yes`。

   ![销售配置 — Google API -Google Analytics](../configuration-reference/sales/assets/google-api-analytics-ee.png){width="600" zoomable="yes"}

1. 完成后，单击&#x200B;**[!UICONTROL Save Config]**。

## 增强型电子商务

增强型电子商务是[!DNL Google Universal Analytics]的一个插件，可让您深入了解客户的购物和购买行为。 您可以使用增强型电子商务生成有关关键客户活动的报表，例如，当客户在购物车中添加商品、开始结帐流程或完成购买时。 您还可以识别和分析放弃购物而不进行购买的购物者的模式。

以下说明显示如何使用[!DNL Universal Analytics]配置[!DNL Google Tag Manager]以生成增强的电子商务数据和报表。

### 步骤1. 注册Google帐户

1. 注册[Google Tag Manager](google-tag-manager.md)帐户，并完成Commerce配置。

1. 注册新的[Google Universal Analytics][1]帐户。

### 步骤2. 配置增强型电子商务

1. 登录到您的Google Universal Analytics帐户。

1. 使用以下设置为增强型电子商务分析创建属性：

   - 状态：打开
   - 相关产品：打开
   - 启用增强型电子商务报表：开启
   - 签出标签： （非必需）

1. 完成后，单击&#x200B;**[!UICONTROL Submit]**。

### 步骤3. 创建标记和触发器

1. 登录到您的[!DNL Google Tag Manager]帐户并创建以下触发器：

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
   >仅针对内置的Commerce基本付款方法触发[!UICONTROL Checkout]事件（如`Check / Money Order`和`Cash On Delivery Payment`）。 此事件不针对`PayPal checkout`和其他外部付款方法执行，这些付款方法使用重定向从外部资源结帐。

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

   - 输入以下&#x200B;**[!UICONTROL Add to Cart]**&#x200B;跟踪设置：

     | 设置 | 值 |
     |--- |--- |
     | [!UICONTROL Track Type] | 事件 |
     | [!UICONTROL Category] | 电子商务 |
     | [!UICONTROL Action] | 添加到购物车 |
     | [!UICONTROL Trigger] | addToCart |

   - 输入以下&#x200B;**[!UICONTROL Checkout option]**&#x200B;跟踪设置：

     | 设置 | 值 |
     |--- |--- |
     | [!UICONTROL Track Type] | 事件 |
     | [!UICONTROL Category] | 电子商务 |
     | [!UICONTROL Action] | 签出选项 |
     | [!UICONTROL Trigger] | checkoutOption |

   - 输入以下&#x200B;**[!UICONTROL PageView]**&#x200B;跟踪设置：

     | 设置 | 值 |
     |--- |--- |
     | [!UICONTROL Track Type] | 页面查看 |
     | [!UICONTROL Trigger] | gtm.dom |

   - 完成以下&#x200B;**[!UICONTROL Product Click]**&#x200B;跟踪配置：

     | 设置 | 值 |
     |--- |--- |
     | [!UICONTROL Track Type] | 事件 |
     | [!UICONTROL Category] | 电子商务 |
     | [!UICONTROL Action] | 产品点击量 |
     | [!UICONTROL Trigger] | productClick |

   - 完成以下&#x200B;**[!UICONTROL Promotion Click]**&#x200B;跟踪配置：

     | 设置 | 值 |
     |--- |--- |
     | [!UICONTROL Track Type] | 事件 |
     | [!UICONTROL Category] | 电子商务 |
     | [!UICONTROL Action] | 促销活动点击 |
     | [!UICONTROL Trigger] | promotionClick |

   - 完成以下&#x200B;**[!UICONTROL Remove from Cart]**&#x200B;跟踪配置：

     | 设置 | 值 |
     |--- |--- |
     | [!UICONTROL Track Type] | 事件 |
     | [!UICONTROL Category] | 电子商务 |
     | [!UICONTROL Action] | 从购物车中移除 |
     | [!UICONTROL Trigger] | removeFromCart |

1. 完成后，单击&#x200B;**[!UICONTROL Preview]**&#x200B;并验证标记是否正常工作。

1. 验证设置后，单击&#x200B;**[!UICONTROL Publish]**。


[1]: https://support.google.com/analytics/answer/2817075?hl=en

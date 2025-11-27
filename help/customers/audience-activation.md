---
title: '[!DNL Audience Activation]'
description: 了解如何在Adobe Commerce中激活Real-Time CDP受众，以促进您商店中的个性化。
exl-id: b53908f2-c0c1-42ad-bb9e-c762804a744b
feature: Customers, Configuration, Personalization
topic: Commerce, Personalization
level: Experienced
badgePaas: label="仅限PaaS" type="Informative" url="https://experienceleague.adobe.com/zh-hans/docs/commerce/user-guides/product-solutions" tooltip="仅适用于云项目(Adobe管理的PaaS基础架构)和内部部署项目上的Adobe Commerce 。"
source-git-commit: 676081da615d02f8cb2e4896b200b1e4c0855913
workflow-type: tm+mt
source-wordcount: '1688'
ht-degree: 1%

---

# [!DNL Audience Activation]

[!DNL Audience Activation]扩展允许您在Adobe Commerce中激活Real-Time CDP受众，以便在购物车中创建独特优惠。 这些优惠和奖励包括常见的电子商务促销技术，如&#x200B;_购买2 get 1 free_、面向该客户的英雄横幅，以及通过各种优惠修改的产品定价。 在Real-Time CDP中构建的受众基于来自各种企业系统的数据，例如企业资源规划(ERP)、客户关系管理(CRM)、销售点和营销系统。 由于客户区段信息会不断刷新，因此在您商店中购物时，客户可能会与区段相关联或取消关联。

您可以在Luma店面或[Headless](#headless-support)店面中激活受众。 在Luma店面中，受众信息（区段成员资格）存储在Commerce端的Cookie中。 在Headless店面中，受众信息作为名为`aep-segments-membership`的参数传递到GraphQL API标头。

## 发行说明

此部分包含有关Audience Activation扩展更新的信息，其中包括：

![新](../assets/new.svg) — 新功能
![修复](../assets/fix.svg) — 修复和改进
![错误](../assets/bug.svg) — 已知问题

请参阅[即将发布的版本](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/schedule.html?lang=zh-Hans)，了解版本计划和支持。

请参阅开发人员文档，以[了解产品兼容性](https://experienceleague.adobe.com/docs/commerce-operations/release/product-availability.html?lang=zh-Hans)。

## 支持的服务更新

以下发行说明介绍了与Audience Activation使用的扩展相关的功能更改和修复。

+++支持的服务更新

_2023年8月15日_

![修复](../assets/fix.svg) — 更新了[Real-Time CDP受众仪表板](#real-time-cdp-audiences-dashboard)以简化筛选。

_2023年6月27日_

![修复](../assets/fix.svg) — 在`magento/module-data-services-graphql`包中添加了对PHP 8.2的支持。

_2023年5月30日_

![新](../assets/new.svg) — 更新了[Real-Time CDP受众功能板](#real-time-cdp-audiences-dashboard)，使其包含对Adobe Commerce实例中的活动受众进行排序、搜索和过滤的功能。

+++

### 2.4.0

[!BADGE 兼容性]{type=Informative tooltip="兼容性"} Adobe Commerce版本2.4.4及更高版本

_2025年3月24日_

![新](../assets/new.svg) — 添加了PHP 8.4支持。

### 2.3.1

[!BADGE 兼容性]{type=Informative tooltip="兼容性"} Adobe Commerce版本2.4.4及更高版本

_2024年11月12日_

![修复](../assets/fix.svg) — 修复了在筛选可供选择的Real-Time CDP受众时出现的问题。

### 2.3.0

[!BADGE 兼容性]{type=Informative tooltip="兼容性"} Adobe Commerce版本2.4.4及更高版本

_2024年7月29日_

![新](../assets/new.svg) — 添加了命令行语法，因此您可以[测试凭据](#validate-the-connection)以确定是否需要更新凭据以从Adobe Experience Platform提取受众数据。

### 2.2.0

[!BADGE 兼容性]{type=Informative tooltip="兼容性"} Adobe Commerce版本2.4.4及更高版本

_2024年6月12日_

受众通知了![新](../assets/new.svg) - [相关产品规则](../merchandising-promotions/product-related-rule-create.md)的GA版本。

### 2.1.1

[!BADGE 兼容性]{type=Informative tooltip="兼容性"} Adobe Commerce版本2.4.4及更高版本

_2024年4月4日_

![新](../assets/new.svg) — 添加了对PHP 8.3的支持。

### 2.2.0-beta1

[!BADGE 兼容性]{type=Informative tooltip="兼容性"} Adobe Commerce版本2.4.4及更高版本

_2024年2月16日_

![新](../assets/new.svg) — 如果您正在参与测试版，请确保您的`composer.json`文件在根级别具有以下内容： ` "minimum-stability": "beta"`。
![新](../assets/new.svg) - (**Beta**)已添加根据受众信息创建[相关产品规则](../merchandising-promotions/product-related-rule-create.md)的功能。

### 2.1.0

[!BADGE 兼容性]{type=Informative tooltip="兼容性"} Adobe Commerce版本2.4.4及更高版本

_2024年1月24日_

![新](../assets/new.svg) — 更新了[Real-Time CDP受众仪表板](#real-time-cdp-audiences-dashboard)以包含包含受众的网站，并指定将哪些动态块和购物车价格规则配置为使用这些受众。

### 2.0.1

[!BADGE 兼容性]{type=Informative tooltip="兼容性"} Adobe Commerce版本2.4.4及更高版本

_2023年11月16日_

![修复](../assets/fix.svg) — 改进的稳定性。

### 2.0.0

[!BADGE 兼容性]{type=Informative tooltip="兼容性"} Adobe Commerce版本2.4.4及更高版本

_2023年10月10日_

![新](../assets/new.svg) — 在您[配置](#configure-the-extension) Audience Activation扩展时添加了对OAuth 2.0的支持。
![修复](../assets/fix.svg) — 改进的稳定性。

### 1.2.0

[!BADGE 兼容性]{type=Informative tooltip="兼容性"} Adobe Commerce版本2.4.4及更高版本

_2023年8月15日_

![修复](../assets/fix.svg) — 更新了UI组件版本。

### 1.1.0

_2023年5月30日_

[!BADGE 兼容性]{type=Informative tooltip="兼容性"} Adobe Commerce版本2.4.4及更高版本

![新](../assets/new.svg) — 在Headless店面中添加了[动态块](#headless-support)的支持。

### 1.0.1

_2023年5月11日_

[!BADGE 兼容性]{type=Informative tooltip="兼容性"} Adobe Commerce版本2.4.4及更高版本

![修复](../assets/fix.svg) — 修复了动态块或购物车价格规则未应用于店面的问题。
![修复](../assets/fix.svg) — 修复了在商户尝试创建或更新动态块时，未配置的Audience Activation扩展安装导致错误的问题。

### 1.0.0

_2023年3月31日_

[!BADGE 兼容性]{type=Informative tooltip="兼容性"} Adobe Commerce版本2.4.4及更高版本

![新](../assets/new.svg) — 一般可用性版本

## 实现

以下任务适用于Luma和headless店面实施。 要在Adobe Commerce中激活受众，您必须：

- 安装Adobe Commerce版本2.4.4或更高版本
- 在Real-Time CDP中将[激活](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/adobe-commerce.html?lang=zh-Hans)Adobe Commerce作为目标
- 在管理员中[安装](#install-the-extension) [!DNL Audience Activation]扩展
- [在管理员中配置](#configure-the-extension) [!DNL Audience Activation]扩展

### 安装扩展

从[!DNL Audience Activation]marketplace[安装](https://commercemarketplace.adobe.com/magento-audiences.html)扩展，或运行以下命令：

```bash
composer require magento/audiences
```

### 配置扩展

安装[!DNL Audience Activation]扩展后，您必须登录Commerce管理员并完成以下操作：

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL System]** > _[!UICONTROL Services]_>**[!UICONTROL Commerce Services Connector]**。

1. [登录到您的Adobe帐户](https://experienceleague.adobe.com/docs/commerce/user-guides/integration-services/saas.html?lang=zh-Hans#organizationid)并选择您的组织ID。

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL System]** > _[!UICONTROL Services]_>**[!UICONTROL [!DNL Data Connection]]**。

1. 在&#x200B;**[!UICONTROL Datastream ID]**&#x200B;字段中，将您在[激活](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/adobe-commerce.html?lang=zh-Hans#parameters) Adobe Commerce时创建的数据流的ID粘贴为Real-Time CDP中的目标。

   此数据流将数据从您的Commerce网站发送到Real-Time CDP，以确定购物者是否属于受众。 如果您尚未创建数据流，请在Experience Platform中[创建](https://experienceleague.adobe.com/docs/experience-platform/datastreams/configure.html?lang=zh-Hans#create)数据流，[将其添加到Real-Time CDP中的Commerce目标以及管理员中的](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/adobe-commerce.html?lang=zh-Hans) [[!DNL Data Connection]扩展。](https://experienceleague.adobe.com/docs/commerce/data-connection/fundamentals/connect-data.html?lang=zh-Hans#data-collection)

   >[!NOTE]
   >
   >指定数据流ID时，您可以[将其关联到](https://experienceleague.adobe.com/docs/commerce/data-connection/fundamentals/connect-data.html?lang=zh-Hans#data-collection)扩展中的特定网站[!DNL Data Connection]。 如果您的Commerce商店有多个网站，请在Real-Time CDP中为每个网站[创建一个目标](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/connect-destination.html?lang=zh-Hans)，并为每个网站使用不同的数据流ID。

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 展开&#x200B;**[!UICONTROL Services]**&#x200B;并选择&#x200B;**[!UICONTROL [!DNL Data Connection]]**。

1. [添加](https://experienceleague.adobe.com/docs/commerce/data-connection/fundamentals/connect-data.html?lang=zh-Hans#add-service-account-and-credential-details)服务帐户和凭据详细信息。

## 在Commerce中的何处使用Real-Time CDP受众

启用[!DNL Audience Activation]扩展后，您可以：

- [创建受众通知的购物车价格规则](../merchandising-promotions/price-rules-cart-create.md#set-a-condition-using-real-time-cdp-audiences)
- [创建受众通知的动态块](../content-design/dynamic-blocks.md#use-real-time-cdp-audiences-in-dynamic-blocks)
- [创建受众通知的相关产品规则](../merchandising-promotions/product-related-rule-create.md)

>[!TIP]
>
>有关如何将[!DNL Commerce]数据导出到Real-Time CDP、构建受众然后将该受众激活到[!DNL Commerce]的完整端到端用例，请参阅[使用 [!DNL Commerce] 事件数据在Real-Time CDP中创建受众](https://experienceleague.adobe.com/zh-hans/docs/commerce/data-connection/use-cases/create-audience)。

## Real-Time CDP受众功能板

您可以使用[Real-Time CDP Audiences](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/activate-edge-personalization-destinations.html?lang=zh-Hans)仪表板在Adobe Commerce实例中查看可用于个性化的所有&#x200B;**活动**&#x200B;受众。

要访问&#x200B;**Real-Time CDP受众**&#x200B;仪表板，请转到&#x200B;_管理员_&#x200B;侧栏，然后转到&#x200B;**[!UICONTROL Customers]** > **[!UICONTROL Real-time CDP Audience]**。

![Real-Time CDP受众信息板](./assets/real-time-cdp-dashboard.png){width="700" zoomable="yes"}

仪表板包含以下字段：

| 列 | 描述 |
|--- |--- |
| `Hide filters` | 可让您显示或隐藏可应用于功能板的任何筛选器。 目前，您可以应用的唯一过滤器是`Last updated`。 通过此过滤器，您可以根据受众的上次更新时间为其选择日期范围。 |
| `Search` | 允许您在Commerce实例中搜索活动受众。 |
| `Name` | 在Real-Time CDP中提供给受众的名称。 |
| `Origin` | 指示受众的来源，如`Experience Platform`。 |
| `Websites` | 指示将哪些网站配置为使用受众。 |
| `Dynamic Blocks` | 指示将哪些动态块配置为使用受众。 |
| `Cart Price Rules` | 指示将哪些购物车价格规则配置为使用受众。 |
| `Related Product Rules` | 指示将哪些相关产品规则配置为使用受众。 |
| `Last updated` | 指示在Real-Time CDP中修改受众的时间。 |
| `Sync now` | 从Real-Time CDP中检索新的或更新受众。 |
| `Customize table` | 允许您显示或隐藏`Origin`、`Websites`、`Dynamic Blocks`、`Cart Price Rules`和`Last updated`列。 |

{style="table-layout:auto"}

## Headless支持

您可以在headless Adobe Commerce实例(如AEM和PWA)中激活受众，以根据受众显示购物车价格规则、相关产品规则或动态块。

### 购物车价格规则和相关产品规则

对于购物车价格规则和相关产品规则，Headless店面通过[Commerce integration framework (CIF)](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/content-and-commerce/integrations/magento.html?lang=zh-Hans)与Experience Platform通信。 该框架提供了一个使用GraphQL实现的服务器端API。 受众信息（例如购物者的区段）通过名为`aep-segments-membership`的GraphQL标头参数传递到Commerce。

整体架构如下：

![将数据从Headless Storefront发送到后端](./assets/aem-commerce-architecture.png){width="700" zoomable="yes"}

在您[安装](#install-the-extension)和[配置](#configure-the-extension)扩展后，Experience Platform Web SDK将以区段成员资格的形式包含受众信息。

要从SDK捕获这些区段成员资格，请参阅此[代码片段](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/custom-personalization.html?lang=zh-Hans#example-response-for-custom-personalization-with-attributes)。

在检索区段后，您可以在GraphQL标题中将这些区段传递到Commerce。 例如：

```bash
curl 'http://magento.config/graphql' -H 'Authorization: Bearer abc123' -H 'aep-segments-membership: urlencoded_list_of_segments' -H 'Content-Type: application/json' --data-binary '{"query":"query {\ncustomer {\nfirstname\nlastname\nemail\n}\n}"}'
```

### 动态块

对于动态块，GraphQL `dynamicBlocks`查询可以包含`audience_id`输入属性。 如果在`audience_id`查询中指定了一个或多个`dynamicBlocks`值，它将返回分配给这些受众的动态块列表。

#### 使用示例

以下查询返回与多个受众ID关联的所有动态块。

**请求：**

```graphql
{
  dynamicBlocks(input:
  {
    type: SPECIFIED
    audience_id: {
      in: [
        "cd29a789-9be8-40ad-a1ef-640c33b3742e"
        "92c3e14d-c72b-40d0-96b7-b96801dcc135"
      ]
    }
  })
  {
    items {
      uid
      audience_id
      content {
        html
      }
    }
    page_info {
      current_page
      page_size
      total_pages
    }
    total_count
  }
}
```

**响应：**

```json
{
  "data": {
    "dynamicBlocks": {
      "items": [
        {
          "uid": "MQ==",
          "audience_id": [
            "cd29a789-9be8-40ad-a1ef-640c33b3742e"
          ],
          "content": {
            "html": "<h2><strong>SAVE 20%</strong></h2>\r\n<p>(some restrictions apply)</p>\r\n<p>&nbsp;</p>"
          }
        },
        {
          "uid": "Mg==",
          "audience_id": [
            "cd29a789-9be8-40ad-a1ef-640c33b3742e",
            "92c3e14d-c72b-40d0-96b7-b96801dcc135"
          ],
          "content": {
            "html": "<p><img src=\"{{media url=&quot;wysiwyg/save20.png&quot;}}\" alt=\"save 20% red\"></p>"
          }
        }
      ],
      "page_info": {
        "current_page": 1,
        "page_size": 20,
        "total_pages": 1
      },
      "total_count": 2
    }
  }
}
```

在`dynamicBlocks`开发人员文档[中了解有关](https://developer.adobe.com/commerce/webapi/graphql/schema/store/queries/dynamic-blocks/) GraphQL查询的更多信息。

## 使用Adobe Experience Platform Mobile SDK检索受众

您可以使用Adobe Experience Platform Mobile SDK检索Real-Time CDP受众。

1. [安装](#install-the-extension) Audience Activation扩展。
1. [为您的移动设备Commerce站点安装和配置SDK](https://experienceleague.adobe.com/docs/commerce/data-connection/fundamentals/mobile-sdk-epc.html?lang=zh-Hans)。

>[!IMPORTANT]
>
>适用于iOS的Adobe Experience Platform Mobile SDK支持iOS 11或更高版本。

完成配置后，使用移动设备SDK操作检索受众数据。 例如：

```swift
Edge.sendEvent(experienceEvent: experienceEvent) { (handles: [EdgeEventHandle]) in
    for handle in handles {
        if handle.type == "activation:pull" {
        let payloadItems = handle.payload ?? []
            for payloadItem in payloadItems {
                if let segments = payloadItem["segments"] as? any Sequence {
                    var segmentsArr = [Any]()
                    for segment in segments {
                        let response = segment as AnyObject?
                        segmentsArr.append(response?.object(forKey: "id")! ?? "")
                    }
                    print("Saving segments ->  \(segments)")
                    storage.set(segmentsArr, forKey: "segments")
                    print("End saving segments")
                }

                // Show segments
                let rSegments = storage.object(forKey: "segments") ?? nil;
                print("Retrieving segments -> \(rSegments)")
            }
        }
    }
}
```

检索数据后，您可以在Commerce应用程序中创建受众通知的[购物车价格规则](../merchandising-promotions/price-rules-cart-create.md#set-a-condition-using-real-time-cdp-audiences)、[动态块](../content-design/dynamic-blocks.md#use-real-time-cdp-audiences-in-dynamic-blocks)和[相关的产品规则](../merchandising-promotions/product-related-rule-create.md)。

## 受众不显示在Commerce中

如果Real-Time CDP受众未显示在Commerce中，原因可能是：

- 连接无效
- 在&#x200B;**数据连接**&#x200B;配置页面中选择的身份验证类型不正确
- 生成的令牌权限不足

以下部分介绍了如何解决这些问题。

### 验证连接

要验证Adobe Experience Platform的凭据和响应，请运行以下命令：

```bash
bin/magento audiences:config:status
```

此命令返回连接状态。 添加`-v`标记以提供额外的详细程度：

```
./bin/magento audiences:config:status -v
```

例如：

```
+----------------------------------+---------------+---------------------------------------------+---------------------------------------------------------+--------------+
| Client ID                        | Client secret | Technical account ID                        | Technical account email                                 | Sandbox name |
+----------------------------------+---------------+---------------------------------------------+---------------------------------------------------------+--------------+
| 1234bd57fac8497d8933327c535347d8 | *****         | 12341E116638D6B00A495C80@techacct.adobe.com | 12345-b95b-4894-a41c-a4130d26bd80@techacct.adobe.com | dev          |
```

### 配置中选择的身份验证类型不正确

1. 打开您的Commerce实例。
1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。
1. 展开&#x200B;**[!UICONTROL Services]**&#x200B;并选择&#x200B;**[!UICONTROL [!DNL Data Connection]]**。
1. 确保您在&#x200B;**[!UICONTROL Authentication Type]**&#x200B;字段中指定的服务器到服务器授权方法正确。 Adobe建议使用&#x200B;**OAuth**。 [JWT已弃用](https://experienceleague.adobe.com/zh-hans/docs/experience-manager-65/content/security/jwt-credentials-deprecation-in-adobe-developer-console)，当前所有证书将于2026年3月1日过期。

### 生成的令牌权限不足

此问题可能是由于生成的令牌的API权限不足导致的。 要确保令牌具有正确的权限，请执行以下操作：

1. 确定贵组织中Adobe Experience Platform的系统管理员。
1. 查找您将使用的项目和凭据。
1. 识别技术帐户电子邮件，例如： `fe3c9476-1234-1234-abcd-2a51a785009a@techacct.adobe.com`。
1. 让系统管理员启动Adobe Experience Platform并转到&#x200B;**[!UICONTROL Permissions]** -> **[!UICONTROL Users]** -> **[!UICONTROL API credentials]**。
1. 使用上面提供的技术帐户电子邮件，搜索要修改的凭据。
1. 打开凭据，然后选择&#x200B;**[!UICONTROL Roles]** -> **[!UICONTROL Add roles]**。
1. 添加包含&#x200B;**[!UICONTROL Manage destinations]**&#x200B;权限的角色。
1. 单击&#x200B;**[!UICONTROL Save]**。
1. [在控制台中重新生成](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-authentication.html?lang=zh-Hans#generate-access-token)访问令牌。
1. 使用[Target连接API](https://developer.adobe.com/experience-platform-apis/references/destinations/#tag/Target-connections/operation/getTargetConnections)验证令牌是否提供了有效的响应。

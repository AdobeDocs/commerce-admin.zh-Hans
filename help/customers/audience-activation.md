---
title: "[!DNL Audience Activation]"
description: 了解如何在Adobe Commerce中激活Real-Time CDP受众，以促进您商店中的个性化。
exl-id: b53908f2-c0c1-42ad-bb9e-c762804a744b
feature: Customers, Configuration, Personalization
topic: Commerce, Personalization
level: Experienced
source-git-commit: 9884d0991cceda7c2917f723467230d3702b2d0f
workflow-type: tm+mt
source-wordcount: '1455'
ht-degree: 0%

---

# [!DNL Audience Activation]

此 [!DNL Audience Activation] 通过扩展，您可以在Adobe Commerce中激活Real-Time CDP受众，以在购物车中创建独特选件。 这些优惠和奖励包括常见的电子商务促销技术，例如 _购买2得到1免费_，主页横幅面向该客户，并通过各种优惠修改了产品定价。 在Real-Time CDP中构建的受众基于来自各种企业系统的数据，例如企业资源规划(ERP)、客户关系管理(CRM)、销售点和营销系统。 由于客户区段信息会不断刷新，因此在您商店中购物时，客户可能会与区段相关联或取消关联。

您可以在Luma店面中激活受众或 [headless](#headless-support) 店面。 在Luma店面中，受众信息（区段成员资格）存储在Commerce端的Cookie中。 在Headless店面中，受众信息将作为名为的参数传递到GraphQL API标头： `aep-segments-membership`.

## 发行说明

此部分包含有关Audience Activation扩展更新的信息，其中包括：

![新建](../assets/new.svg)  — 新增功能
![修复](../assets/fix.svg)  — 修复和改进功能
![错误](../assets/bug.svg)  — 已知问题

请参阅 [即将发布的版本](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/schedule.html) 了解发布计划和支持。

请参阅开发人员文档以 [了解产品兼容性](https://experienceleague.adobe.com/docs/commerce-operations/release/product-availability.html).

## 支持的服务更新

这些发行说明介绍了与Audience Activation使用的扩展相关的功能更改和修复。

+++支持的服务更新

_2023年8月15日_

![修复](../assets/fix.svg)  — 已更新 [Real-Time CDP Audiences功能板](#real-time-cdp-audiences-dashboard) 以简化筛选。

_2023年6月27日_

![修复](../assets/fix.svg)  — 在中添加了对PHP 8.2的支持 `magento/module-data-services-graphql` 包。

_2023年5月30日_

![新建](../assets/new.svg)  — 已更新 [Real-Time CDP Audiences功能板](#real-time-cdp-audiences-dashboard) 在Adobe Commerce实例中包含对活动受众进行排序、搜索和过滤的功能。

+++

### 2.1.1

[!BADGE 兼容性]{type=Informative tooltip="兼容性"}

_2024年4月4日_

![新建](../assets/new.svg)  — 添加了对PHP 8.3的支持。

### 2.2.0-beta1

[!BADGE 兼容性]{type=Informative tooltip="兼容性"}

_2024年2月16日_

![新建](../assets/new.svg)  — 如果您正在参与Beta测试，请确保您的 `composer.json` 文件在根级别具有以下内容： ` "minimum-stability": "beta"`.
![新建](../assets/new.svg) - (**测试版**)添加了创建功能 [相关产品规则](../merchandising-promotions/product-related-rule-create.md) 由受众通知。

### 2.1.0

[!BADGE 兼容性]{type=Informative tooltip="兼容性"}

_2024年1月24日_

![新建](../assets/new.svg)  — 已更新 [Real-Time CDP Audiences功能板](#real-time-cdp-audiences-dashboard) 以包含包含受众的网站，并指定将哪些动态块和购物车价格规则配置为使用这些受众。

### 2.0.1

[!BADGE 兼容性]{type=Informative tooltip="兼容性"}

_2023年11月16_

![修复](../assets/fix.svg)  — 提高了稳定性。

### 2.0.0

[!BADGE 兼容性]{type=Informative tooltip="兼容性"}

_2023年10月10日_

![新建](../assets/new.svg)  — 当您使用OAuth 2.0时 [配置](#configure-the-extension) Audience Activation扩展。
![修复](../assets/fix.svg)  — 提高了稳定性。

### 1.2.0

[!BADGE 兼容性]{type=Informative tooltip="兼容性"}

_2023年8月15日_

![修复](../assets/fix.svg)  — 更新了UI组件版本。

### 1.1.0

_2023年5月30日_

[!BADGE 兼容性]{type=Informative tooltip="兼容性"}

![新建](../assets/new.svg)  — 添加了对 [动态块](#headless-support) 无头店面。

### 1.0.1

_2023年5月11日_

[!BADGE 兼容性]{type=Informative tooltip="兼容性"}

![修复](../assets/fix.svg)  — 修复了动态块或购物车价格规则未应用于店面的问题。
![修复](../assets/fix.svg)  — 修复了在商户尝试创建或更新动态块时，未配置的Audience Activation扩展安装导致错误的问题。

### 1.0.0

_2023年3月31日_

[!BADGE 兼容性]{type=Informative tooltip="兼容性"}

![新建](../assets/new.svg)  — 正式发布版本

## 实现

以下任务适用于Luma和headless店面实施。 要在Adobe Commerce中激活受众，您必须：

- 安装Adobe Commerce版本2.4.4或更高版本
- [激活](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/adobe-commerce.html) Adobe Commerce作为Real-Time CDP中的目标
- [安装](#install-the-extension) 该 [!DNL Audience Activation] Admin中的扩展
- [配置](#configure-the-extension) 该 [!DNL Audience Activation] Admin中的扩展

### 安装扩展

安装 [!DNL Audience Activation] 扩展来自 [marketplace](https://commercemarketplace.adobe.com/magento-audiences.html)，或运行以下命令：

```bash
composer require magento/audiences
```

### 配置扩展

安装之后 [!DNL Audience Activation] 扩展上，您必须登录Commerce管理员并完成以下操作：

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL System]** > _[!UICONTROL Services]_>**[!UICONTROL Commerce Services Connector]**.

1. [登录](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/integration-services/saas.html#organizationid) 到您的Adobe帐户，然后选择您的组织ID。

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL System]** > _[!UICONTROL Services]_>**[!UICONTROL [!DNL Data Connection]]**.

1. 在 **[!UICONTROL Datastream ID]** 字段中，粘贴您创建的数据流的ID [已激活](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/adobe-commerce.html#parameters) Adobe Commerce作为Real-Time CDP中的目标。

   此数据流将数据从您的Commerce网站发送到Real-Time CDP，以确定购物者是否属于受众。 如果您尚未创建数据流， [创建](https://experienceleague.adobe.com/docs/experience-platform/datastreams/configure.html#create) 一个Experience Platform， [添加](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/adobe-commerce.html) 到Real-Time CDP中的Commerce目标，然后到 [[!DNL Data Connection]](https://experienceleague.adobe.com/docs/commerce-merchant-services/data-connection/fundamentals/connect-data.html#data-collection) 扩展。

   >[!NOTE]
   >
   >指定数据流ID时，您可以 [将其关联到特定网站](https://experienceleague.adobe.com/docs/commerce-merchant-services/data-connection/fundamentals/connect-data.html#data-collection) 在 [!DNL Data Connection] 扩展。 如果您的Commerce商店有多个网站， [创建目标](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/connect-destination.html) Real-Time CDP中的每个网站，并为每个网站使用不同的数据流ID。

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 展开 **[!UICONTROL Services]** 并选择 **[!UICONTROL [!DNL Data Connection]]**.

1. [添加](https://experienceleague.adobe.com/docs/commerce-merchant-services/data-connection/fundamentals/connect-data.html#add-service-account-and-credential-details) 服务帐户和凭据详细信息。

## 在Commerce中的何处使用Real-Time CDP受众

使用 [!DNL Audience Activation] 扩展已启用，您可以：

- [创建购物车价格规则](../merchandising-promotions/price-rules-cart-create.md#set-a-condition-using-real-time-cdp-audiences) 由受众通知
- [创建动态块](../content-design/dynamic-blocks.md#use-real-time-cdp-audiences-in-dynamic-blocks) 由受众通知
- [(**测试版**)创建相关的产品规则](../merchandising-promotions/product-related-rule-create.md) 由受众通知

有关如何导出的完整端到端用例 [!DNL Commerce] 将数据发送到Real-Time CDP，构建受众，然后将该受众激活到 [!DNL Commerce]，请参见 [在Real-Time CDP中使用创建受众 [!DNL Commerce] 事件数据](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/use-cases/create-audience).

## Real-Time CDP受众功能板

您可以查看所有 [活动](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/activate-edge-personalization-destinations.html) 可用于在Adobe Commerce实例中使用 **Real-Time CDP受众** 仪表板。

要访问 **Real-Time CDP受众** 仪表板，转到 _管理员_ 侧栏，然后转到 **[!UICONTROL Customers]** > **[!UICONTROL Real-time CDP Audience]**.

![Real-Time CDP受众功能板](./assets/real-time-cdp-dashboard.png){width="700" zoomable="yes"}

仪表板包含以下字段：

| 列 | 描述 |
|--- |--- |
| `Hide filters` | 可让您显示或隐藏可应用于功能板的任何筛选器。 目前，您可以应用的唯一过滤器是 `Last updated`. 通过此过滤器，您可以根据受众的上次更新时间为其选择日期范围。 |
| `Search` | 允许您在Commerce实例中搜索活动受众。 |
| `Name` | 在Real-Time CDP中提供给受众的名称。 |
| `Origin` | 指示受众的来源，如 `Experience Platform`. |
| `Websites` | 指示将哪些网站配置为使用受众。 |
| `Dynamic Blocks` | 指示将哪些动态块配置为使用受众。 |
| `Cart Price Rules` | 指示将哪些购物车价格规则配置为使用受众。 |
| `Last updated` | 指示在Real-Time CDP中修改受众的时间。 |
| `Sync now` | 从Real-Time CDP中检索新的或更新受众。 |
| `Customize table` | 可让您显示或隐藏 `Origin`， `Websites`， `Dynamic Blocks`， `Cart Price Rules`、和 `Last updated` 列。 |

{style="table-layout:auto"}

## Headless支持

您可以在headless Adobe Commerce实例中激活受众(如AEM和PWA)，以根据受众显示购物车价格规则、相关产品规则或动态块。

### 购物车价格规则和相关产品规则

Experience Platform对于购物车价格规则和相关产品规则，Headless店面通过 [Commerce integration framework(CIF)](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/content-and-commerce/integrations/magento.html). 该框架提供了一个使用GraphQL实现的服务器端API。 受众信息（例如购物者的区段）通过名为的GraphQL标题参数传递到Commerce： `aep-segments-membership`.

整体架构如下：

![将数据从Headless店面发送到后端](./assets/aem-commerce-architecture.png){width="700" zoomable="yes"}

在您之后 [安装](#install-the-extension) 和 [配置](#configure-the-extension) 在扩展中，Experience PlatformWeb SDK包含以区段成员资格形式的受众信息。

要从SDK捕获这些区段成员资格，请参阅此 [代码段](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/custom-personalization.html#example-response-for-custom-personalization-with-attributes).

在检索区段后，您可以在GraphQL标题中将这些区段传递到Commerce。 例如：

```bash
curl 'http://magento.config/graphql' -H 'Authorization: Bearer abc123' -H 'aep-segments-membership: urlencoded_list_of_segments' -H 'Content-Type: application/json' --data-binary '{"query":"query {\ncustomer {\nfirstname\nlastname\nemail\n}\n}"}'
```

### 动态块

对于动态块，请使用GraphQL `dynamicBlocks` 查询可以包含 `audience_id` 输入属性。 如果指定一个或多个 `audience_id` 中的值 `dynamicBlocks` 查询时，将返回分配给这些受众的动态块列表。

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

了解关于 `dynamicBlocks` 中的GraphQL查询 [开发人员文档](https://developer.adobe.com/commerce/webapi/graphql/schema/store/queries/dynamic-blocks/).

## 使用Adobe Experience Platform Mobile SDK检索受众

您可以使用Adobe Experience Platform Mobile SDK检索Real-Time CDP受众。

1. [安装](#install-the-extension) Audience Activation扩展。
1. [为您的移动设备Commerce站点安装和配置SDK](https://experienceleague.adobe.com/docs/commerce-merchant-services/data-connection/fundamentals/mobile-sdk-epc.html).

>[!IMPORTANT]
>
>适用于iOS的Adobe Experience Platform Mobile SDK支持iOS 11或更高版本。

完成配置后，使用Mobile SDK操作检索受众数据。 例如：

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

检索数据后，您可以使用该数据创建受众知情的数据 [购物车价格规则](../merchandising-promotions/price-rules-cart-create.md#set-a-condition-using-real-time-cdp-audiences)， [动态块](../content-design/dynamic-blocks.md#use-real-time-cdp-audiences-in-dynamic-blocks) 和  [相关产品规则](../merchandising-promotions/product-related-rule-create.md) 在Commerce应用程序中。

## 受众不显示在Commerce中

如果Real-Time CDP受众未显示在Commerce中，原因可能是：

- 在中选择的身份验证类型不正确 **数据连接** 配置页面
- 生成的令牌权限不足

以下两部分介绍了如何对这两种情况均进行故障排除。

### 配置中选择的身份验证类型不正确

1. 打开您的Commerce实例。
1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.
1. 展开 **[!UICONTROL Services]** 并选择 **[!UICONTROL [!DNL Data Connection]]**.
1. 请确保您在中指定的服务器到服务器授权方法 **[!UICONTROL Authentication Type]** 字段是正确的。 Adobe建议使用 **OAuth**. 已弃用JWT。 [了解详情](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/migration/).

### 生成的令牌权限不足

此问题可能是由于生成的令牌的API权限不足导致的。 要确保令牌具有正确的权限，请执行以下操作：

1. 确定贵组织中Adobe Experience Platform的系统管理员。
1. 查找您将使用的项目和凭据。
1. 识别技术帐户电子邮件，例如： `fe3c9476-1234-1234-abcd-2a51a785009a@techacct.adobe.com`.
1. 让系统管理员启动Adobe Experience Platform并转到 **[!UICONTROL Permissions]** -> **[!UICONTROL Users]** -> **[!UICONTROL API credentials]**.
1. 使用上面提供的技术帐户电子邮件，搜索要修改的凭据。
1. 打开凭据，然后选择 **[!UICONTROL Roles]** -> **[!UICONTROL Add roles]**.
1. 添加 **全部生产访问权限**.
1. 单击 **[!UICONTROL Save]**.
1. [重新生成](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-authentication.html#generate-access-token) 控制台中的访问令牌。
1. 使用验证令牌是否提供有效响应 [Target连接API](https://developer.adobe.com/experience-platform-apis/references/destinations/#tag/Target-connections/operation/getTargetConnections).

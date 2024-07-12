---
title: 设置同步服务
description: “了解如何将您的Adobe Commerce和Experience Manager Assets项目连接到Assets规则引擎服务，以启用这两个系统之间的资源同步。”
feature: CMS, Media
source-git-commit: 9d7b1b58b472a99196213e5ab109142bc57b1692
workflow-type: tm+mt
source-wordcount: '1309'
ht-degree: 0%

---


# 设置同步服务

资产规则引擎服务(ARES)是一种多租户服务，它将AEM Assets与Adobe Commerce集成。 此服务在Adobe Commerce和Experience Manager之间同步资源。 ARES服务可根据SKU或其他关键属性，自动将AEM中的资产与Adobe Commerce中的产品相匹配。 它还确保电子商务网站上始终提供最新的产品资产和变体。

要设置服务，您需要使用ARES GraphQL API注册租户ID，并选择用于同步资产的匹配规则。

## 选择匹配策略

适用于Commerce的AEM Assets集成支持两种在Adobe Commerce和AEM Assets之间同步资产的匹配策略。

- **MatchBySku** — 这是根据产品的库存单位(SKU)匹配资产的默认匹配规则。 SKU是每个产品的唯一标识符。 此规则将资源元数据中的SKU与Commerce产品SKU相匹配，以确保将资源与正确的产品相关联。

- **ExternalMatcher** — 此匹配规则适用于需要自定义匹配逻辑的更复杂方案或特定业务要求。 要使用此规则，您必须在Adobe Developer App Builder中实施自定义代码以定义如何将资源与产品匹配。

对于初始载入，请使用`MatchBySku`策略。 如果需要，可以稍后更改匹配策略。

## 注册租户

>[!BEGINSHADEBOX]

**预修课程**

- [AEM Assets项目已配置映射资源所需的Commerce元数据](aem-assets-configure-aem.md)。

- [在Adobe Commerce中安装和配置Experience Manager Assets集成](aem-assets-configure-commerce.md)。

>[!ENDSHADEBOX]

## 收集凭据

您需要以下凭据来验证您的Commerce项目环境，并将其与AEM Assets项目环境连接到Commerce SaaS服务。

| 所需数据 | Source | 在何处查找它 |
| ---------- | ------ | ------------- |
| 来自Magento帐户的API密钥 | Commerce | 提供您正在使用的、暂存或生产环境的Commerce的公共API密钥。 您可以在[Commerce Service Connector设置](aem-assets-configure-commerce.md#configure-the-commerce-services-connector)页面的管理员或[!UICONTROL My Account]页面的[!UICONTROL API Portal]部分中找到生产和暂存环境的API密钥。 |
| Commerce SaaS项目标识符 <ul><li>`magento-environment-Id`</li><li>`Project ID`</li></ul> | Commerce管理员 | 这些值标识要连接到的Commerce环境和SaaS数据空间和项目。 值来自[Commerce服务连接器SaaS标识符配置]。(aem-assets-configure-commerce.md#configure-the-commerce-services-connector)。 |
| AEM `programId`<br>`environmentId` | [AEM Assets创作环境](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/authoring/quick-start) | 打开AEM Sites页面，然后选择&#x200B;**[!UICONTROL Assets]**。  从URL复制项目和环境ID： `https://author-p[Program ID]-e[EnvironmentID].adobeaemcloud.com/` |
| 基本URL | Commerce店面 | Commerce店面的[基本URL](../stores-purchase/store-urls.md)。 |
| 用于访问API的OAuth凭据 | Commerce管理员 | 您可以在Assets集成的Commerce [配置设置](aem-assets-configure-commerce.md#experience-manager-assets-integration-for-adobe-commerce-10-release)中找到这些凭据。 |

## 注册租户

通过向Assets规则引擎服务提交请求以添加身份验证凭据和租户ID来完成租户注册。 该请求包括在该服务、Commerce项目和Experience Manager Assets项目之间建立连接所需的凭据和项目标识符。

使用GraphQL客户端或cURL发送请求。

>[!BEGINTABS]

>[!TAB GraphQL请求]

使用GraphQL客户端向API终结点`https://commerce.adobe.io/assets-integration/graphql`发送POST请求

**必需的标头**

为请求指定以下HTTP标头：

- `x-api-key`：来自您Magento帐户的API密钥
- `magento-environment-Id`： SaaS标识符
- `x-gw-signature`：与MAGEID关联的JWT令牌

**请求：**

**语法**

```graphql
mutation registerTenant($tenantInput: TenantInput!) {
   registerTenant(tenantInput: $tenantInput) {
      tenantId
      userErrors {
         message
         path
      }
    }
}
```

**示例用法**

注册租户并选择`matchBySku`规则以在Adobe Commerce和AEM Assets项目之间映射资源。

**请求：**

```graphql
   {
      "tenantInput": {
         "enabled": true,
         "projectId": "8231afb6-90cd-65e8-84ba-d9abac0f94e6",
         "aem": {
               "programId": "11111",
               "environmentId": "222222"
         },
         "commerce": {
               "baseUrl": "***",
               "credentials": {
                  "consumerKey": "***",
                  "consumerSecret": "***",
                  "accessToken": "***",
                  "accessTokenSecret": "***"
               }
         },
         "rule": {
            "type": "matchBySKU"
            "matchBySkuRule": {
               "metadataField": "commerce:skus"
            }
         }
      }
   }
```

**响应**

```graphql
{
    "data": {
        "registerTenant": {
            "tenantId": "b65d5da7-2756-46a1-9ff1-14fb5d925fee",
            "userErrors": []
        }
    }
}
```

>[!TAB cURL请求]

```shell
curl --request POST \
  --url https://commerce.adobe.io/assets-integration/graphql \
  --header 'Content-Type: application/json' \
  --header 'Magento-Environment-Id: ****' \
  --header 'x-api-key: ****' \
  --header 'x-gw-signature: *****' \
  --data '{"query":"mutation registerTenant($tenantInput: TenantInput!) {\n\tregisterTenant(tenantInput: $tenantInput) {\n\t\ttenantId\n\t\tuserErrors {\n\t\t\tmessage\n\t\t\tpath\n\t\t}\n\t}\n}\n","operationName":"registerTenant","variables":{"tenantInput":{"enabled":true,"threshold":100,"projectId":"5d6faa03-e200-4623-9008-da144e4eefd8","aem":{"programId":"***","environmentId":"***"},"commerce":{"version":"2.4.6-p2","extensionVersion":"0.0.1","baseUrl":"***","credentials":{"consumerKey":"***","consumerSecret":"***","accessToken":"***","accessTokenSecret":"***"}},"rule":{"type":"matchBySKU","matchBySkuRule":{"metadataField":"commerce:skus"}}}}}'
```

>[!ENDTABS]

### 输入字段

#### AemInput

标识用于存储Commerce资源的AEM Assets实例。 您可以从Cloud Manager的“我的程序”视图或内容创作URL中获取此信息。

| 字段 | 数据类型 | 描述 |
| ----- | --------- | ----------- |
| `programId` | 字符串！ | AEM Cloud Service中项目的唯一标识符 |
| `environmentId` | 字符串！ | 您正在使用的项目环境（如生产、暂存或开发）的ID |

#### CommerceInput

此输入字段提供用于API访问Commerce目录的OAuth身份验证凭据。 您可以在Assets集成的Commerce [配置设置](aem-assets-configure-commerce.md#experience-manager-assets-integration-for-adobe-commerce-10-release)中找到这些凭据。

| 字段 | 数据类型 | 描述 |
| ----- | --------- | ----------- |
| `baseUrl` | 字符串 | Commerce店面的[基本URL](../stores-purchase/store-urls.md)。 |
| `credentials` | [CommerceCredentialsInput](#commercecredentialsinput)！ | 指定用于访问Commerce实例的凭据。 |
| `extensionVersion` | 字符串 | 可选。 适用于Commerce扩展的AEM Assets集成的版本，安装在Commerce实例上。 |
| `version` | 字符串 | 可选。 Commerce实例上安装的Commerce应用程序的版本。 |

#### CommerceCredentialsInput

此输入字段提供用于访问Commerce目录的API的OAuth凭据。 您可以在Assets集成的Commerce [配置设置](aem-assets-configure-commerce.md#experience-manager-assets-integration-for-adobe-commerce-10-release)中找到这些凭据。

| 字段 | 数据类型 | 描述 |
| ----- | --------- | ----------- |
| `accessToken` | 字符串！ | 为Assets集成生成的访问令牌。 |
| `accessTokenSecret` | 字符串！ | 为Assets集成生成的访问令牌密码。 |
| `consumerKey` | 字符串！ | 为Assets集成生成的使用者密钥。 |
| `consumerSecret` | 字符串！ | 为Assets集成生成的使用者密钥。 |

#### ExternalMatcherInput

| 字段 | 数据类型 | 描述 |
| ----- | --------- | ----------- |
| assetToProductUrl | 字符串！ | <!--Add field description--> |
| productToAssetUrl | 字符串！ | <!--Add field description--> |
| 凭据 | [ExternalMatcherCredentialsInput](#externalmatchercredentials)！ | 用于访问App Builder项目以进行Commerce的AEM Assets集成的凭据。 |

#### ExternalMatcherCredentials

| 字段 | 数据类型 | 描述 |
| ----- | --------- | ----------- |
| `oauthServerUrl` | 字符串！ |    |
| `clientId` | 字符串！ |      |
| `clientSecret` | 字符串！ |    |
| `imsOrgId` | 字符串！ | 配置AEM Assets和Adobe Commerce的IMS组织。 |

#### MatchBySkuRuleInput

| 字段 | 数据类型 | 描述 |
| ----- | --------- | ----------- |
| metadatafield | 字符串！ | 指定要用于匹配的资源元数据字段。 使用`commerce:skus` |

#### 规则输入

指定用于在Adobe Commerce和AEM Assets之间同步资源的匹配规则。

| 字段 | 数据类型 | 描述 |
| ----- | --------- | ----------- |
| externalMatcher | [ExternalMatcherInput](#externalmatcherinput) | 选择用于资产匹配的externalMatcher规则并指定使用该规则所需的数据。 |
| MatchBySkuRule | [MatchBySkuRuleInput](#matchbyskuruleinput) | 选择用于资产匹配的MatchBySkuRule并指定使用该规则所需的数据。 |

#### RuleTypeInput

| 字段 | 数据类型 | 描述 |
| ----- | --------- | ----------- |
| 规则类型 | 枚举 | 指定可用于Commerce的AEM Assets集成的资源匹配规则列表。 可用值为`matchBySKU`或`externalMatcher`。 |

#### TenantInput

| 字段 | 数据类型 | 描述 |
| ----- | --------- | ----------- |
| `aem` | [AemInput！](#aeminput) | 标识您在其中存储AEM Assets资源的AEM Cloud Service中的Commerce实例。 |
| `commerce` | [商务输入！](#commerceinput) | 为API访问提供Commerce项目信息和凭据 |
| `enabled` | 布尔型！ | 启用或禁用Adobe Commerce与AEM Assets之间的资源同步。 |
| `projectId` | 字符串！ | [Commerce服务连接器SaaS标识符配置](aem-assets-configure-commerce.md#configure-the-commerce-services-connector)中的SaaS项目Id。 |
| `rule` | [规则输入！](#ruleinput) | 指定用于在Adobe Commerce和AEM Assets之间同步资源的匹配规则。 指定`[matchBySkuRule](#matchbyskuruleinput)`或`[externalMatcher](#externalmatcherinput)`。 |

### 输出字段

| 字段 | 数据类型 | 描述 |
| ----- | --------- | ----------- |
| 数据 | [registerTenant] | 返回租户注册信息和来自服务器的任何错误消息。 |

#### RegisterTenantResponse

| 字段 | 数据类型 | 描述 |
| ----- | --------- | ----------- |
| tenantId | 字符串！ | 返回已注册的租户ID。 此ID可确保从与Commerce环境关联的SaaS数据空间中存储和检索Commerce的AEM Assets集成数据。 |
| userError | [[用户错误！]！](#usererror) | 返回请求生成的任何错误消息。 |

#### 用户错误

| 错误 | 描述 |
|:------|:------------|
| `IMS Org ID not associated to this Commerce` | 如果`Magento-Environment-Id`标头中指定的环境ID未分配给IMS帐户，则会发生此错误。 发生此错误的原因是，在为Commerce实例配置[Commerce服务连接器](aem-assets-configure-commerce.md#configure-the-commerce-services-connector)时，未连接IMS帐户。 |
| `Client ID is invalid` | `x-api-key`标头不正确。 |
| `Client ID is missing` | 未提供`x-api-key`标头。 |
| `JWT is required` | 未提供`x-gw-signature`标头。 |
| `JWT is invalid` | 未提供`x-gw-signature`标头。 |
| `Tenant already exists` | 具有给定的`mageID` （取自JWT令牌）和`saasId` （由`Magento-Environment-Id`标头提供）的租户已注册。 |
| `Unexpected error when connecting with AEM Assets` | 由于`programId`或`environmentId`值无效或不存在，出现此错误。 |
| `Unable to connect with AEM Assets` | 此错误可能有两个原因：<br>1。 AEM资产帐户与为Adobe Commerce提供的IMS组织ID不同，而是与其他IMS组织ID关联。<br>2。 `commerce:isCommerce`元数据在AEM Assets中不存在，这表示没有批准资源可从AEM Assets发送到Commerce实例。 |
| `Unexpected error when connecting with Commerce` | 当提供的商务`baseURL`无效时，会发生此错误。 |
| `Unable to connect with Commerce, unauthorized` | 提供的商业凭据无效，导致未经授权的访问。 |
| `Invalid rule. The value must be matchBySKU or externalMatcher` | `Rule`字段包含不正确的值。 对于RegisterTenant请求，可用的规则类型由[RuleTypeInput](#ruletypeinput)枚举定义。 |

## 启用Experience Manager Assets集成

在注册租户后，新用户引导过程的最后一步是在管理员中启用Experience Manager Assets集成到Commerce的扩展。

1. 启用该扩展。

   1. 转到&#x200B;**商店** >设置> **配置** > **目录**。

   1. 通过选择&#x200B;**[!UICONTROL Catalog]**&#x200B;打开目录配置。

   1. 展开&#x200B;**[!UICONTROL AEM Assets integration]**。

   1. 将&#x200B;**[!UICONTROL Integration enabled]**&#x200B;设置为`yes`。

      适用于Commerce管理员配置的![AEM Assets集成](assets/aem-integration-admin-enable.png){width="600" zoomable="yes"}

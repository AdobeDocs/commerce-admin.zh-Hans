---
title: 为购物者提供帮助
description: 使用“作为客户登录”功能时，您可以看到客户看到的内容，并代表他们进行更新。
exl-id: 6842ae7a-6440-45f1-af18-e6427088d29d
feature: Customers, Customer Service
source-git-commit: 29f3a8bb019d464e6d7646e0ebc7a4fa2ed0dd74
workflow-type: tm+mt
source-wordcount: '1077'
ht-degree: 0%

---

# 为购物者提供帮助

有时，客户需要帮助来安排订单。 存储管理员可以使用&#x200B;_以客户身份登录_，这样他们就可以查看客户看到的内容，并进行更新以帮助他们。

以客户身份登录时执行的任何操作将应用于实际客户的帐户。

>[!BEGINTABS]

>[!TAB Adobe Commerce]

仅[!BADGE PaaS]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="仅适用于云项目（Adobe管理的PaaS基础架构）和内部部署项目上的Adobe Commerce 。"}

为&#x200B;_管理员_&#x200B;用户启用&#x200B;_[!UICONTROL Login as Customer]_按钮后，该按钮会显示在多个页面中：

* [客户编辑页面](../customers/update-account.md)
* [订单查看页面](../stores-purchase/order-processing.md)
* [发票查看页](../stores-purchase/invoices.md)
* [装运视图页](../stores-purchase/shipments.md)
* [贷项通知单视图页](../stores-purchase/credit-memo-create.md)

![以客户身份登录](assets/login-as-customer.png){width="600" zoomable="yes"}

>[!TAB Adobe Commerce as a Cloud Service]

仅[!BADGE SaaS]{type=Positive url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="仅适用于Adobe Commerce as a Cloud Service和Adobe Commerce Optimizer项目（Adobe管理的SaaS基础架构）。"}

在Adobe Commerce as a Cloud Service中，“以客户身份登录”功能使用&#x200B;**一次性代码(OTC)**&#x200B;工作流，而不是直接登录。 管理员为客户生成一个短暂的、一次性代码。 然后，可以通过GraphQL将此代码交换为客户访问令牌，从而实现无密码登录作为销售商辅助购物方案的客户工作流。

该功能包括以下组件：

* **管理员UI** — 在客户编辑页面上，管理员可以请求一次性代码(OTC)，而不是以客户身份直接登录。
* **[REST API](https://developer.adobe.com/commerce/webapi/rest/saas-integrations/login-as-customer/)** - OTC生成的程序化端点，用于管理脚本和第三方集成。
* **GraphQL API** — 将OTC交换为店面或headless商务流的客户访问令牌的突变。

>[!ENDTABS]

## 启用客户登录

启用&#x200B;_以客户身份登录_&#x200B;要求您在Commerce实例中启用该功能，然后在用户角色权限中为管理员用户启用访问权限。

### 启用该功能

1. 在管理员侧边栏上，转到&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左侧面板中，展开&#x200B;**[!UICONTROL Customers]**&#x200B;并选择&#x200B;**[!UICONTROL Login as Customer]**。

   ![配置选项 — 以客户身份登录](../configuration-reference/customers/assets/login-as-customer.png){width="600" zoomable="yes"}

1. 将&#x200B;**[!UICONTROL Enable Login as Customer]**&#x200B;设置为`Yes`。

1. _（可选）_&#x200B;将&#x200B;**[!UICONTROL Disable Page Cache for Admin User]**&#x200B;设置为`No`以在管理员用户以客户身份登录时启用页面缓存。

   >[!WARNING]
   >
   > 禁用页面缓存（`Yes` — 默认）可确保客户登录时获得最新未缓存的数据。

1. _（可选）_&#x200B;如果您具有多站点和/或多商店设置，并且希望管理员用户在以客户身份登录时选择商店视图，请将&#x200B;**[!UICONTROL Store View to Log in]**&#x200B;设置为`Manual Selection`。

1. 完成后，单击&#x200B;**[!UICONTROL Save Config]**。

### 为管理员用户启用访问权限

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL System]** > _权限_ > **[!UICONTROL User Roles]**。

1. 单击列表中的角色。

1. 在&#x200B;[!UICONTROL _角色信息_]&#x200B;左侧面板中，单击&#x200B;**[!UICONTROL Role Resources]**。

1. 将页面上的&#x200B;**[!UICONTROL Role Resources]**&#x200B;更改为`Custom`。

   >[!INFO]
   >
   > 选中此选项后，资源层次结构将显示在页面中。

1. 滚动到&#x200B;**[!UICONTROL Customers]**&#x200B;父项和下面的&#x200B;**[!UICONTROL Login as Customer]**&#x200B;项。 然后，选择要为角色启用的资源：

   * **[!UICONTROL Allow Login as Customer]** — 允许管理员用户使用&#x200B;_以客户身份登录_&#x200B;功能。
   * **[!UICONTROL View Login as Customer Log]** — 允许管理员用户查看&#x200B;_以客户身份登录_&#x200B;日志。

   ![角色资源 — 以客户身份登录](assets/customers-login-as-customer-role-resources.png){width="400" zoomable="yes"}

1. 单击&#x200B;**[!UICONTROL Save Role]**。

## 用于远程购物协助的客户帐户权限

要从管理员为商店支持人员启用帐户访问权限，客户必须为其帐户启用该功能：

>[!BEGINTABS]

>[!TAB Adobe Commerce]

仅[!BADGE PaaS]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="仅适用于云项目（Adobe管理的PaaS基础架构）和内部部署项目上的Adobe Commerce 。"}

1. 客户转到&#x200B;**[!UICONTROL Account Information]**&#x200B;页面。

1. 选中&#x200B;**[!UICONTROL Allow remote shopping assistance]**&#x200B;复选框。

1. 客户单击&#x200B;**[!UICONTROL Save]**。

![帐户信息页](assets/permission.png){width="700" zoomable="yes"}

>[!TAB Adobe Commerce as a Cloud Service]

仅[!BADGE SaaS]{type=Positive url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="仅适用于Adobe Commerce as a Cloud Service和Adobe Commerce Optimizer项目（Adobe管理的SaaS基础架构）。"}

客户必须将`login_as_customer_assistance_allowed`扩展属性设置为&#x200B;**2**。 可以在管理员的&#x200B;**编辑客户**&#x200B;页面上或通过GraphQL在创建或编辑客户时配置此项。

>[!WARNING]
>
>如果没有此权限，管理员用户将无法以此客户身份登录。

在“编辑客户”页面上![客户同意扩展属性配置](assets/customer-consent-attribute.png){width="600" zoomable="yes"}

要通过GraphQL为现有客户帐户设置此权限，请使用`allow_remote_shopping_assistance``true`或[`updateCustomerV2`](https://developer.adobe.com/commerce/webapi/graphql/schema/customer/mutations/update-v2/)突变将[`createCustomerV2`输入设置为](https://developer.adobe.com/commerce/webapi/graphql/schema/customer/mutations/create-v2/)。

>[!ENDTABS]

## 以客户身份从管理员登录

>[!BEGINTABS]

>[!TAB Adobe Commerce]

仅[!BADGE PaaS]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="仅适用于云项目（Adobe管理的PaaS基础架构）和内部部署项目上的Adobe Commerce 。"}

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL Customers]** > [!UICONTROL _所有客户_]。

1. 在编辑模式下打开用户。

1. 在&#x200B;**[!UICONTROL Customer Information]**&#x200B;面板中，选择&#x200B;**[!UICONTROL Account Information]**&#x200B;部分。

1. 将&#x200B;**[!UICONTROL Allow remote shopping assistance]**&#x200B;设置为`Yes`。

   >[!INFO]
   >
   >管理员现在可以用户身份登录，而无需从店面获得权限。

>[!TAB Adobe Commerce as a Cloud Service]

仅[!BADGE SaaS]{type=Positive url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="仅适用于Adobe Commerce as a Cloud Service和Adobe Commerce Optimizer项目（Adobe管理的SaaS基础架构）。"}

>[!NOTE]
>
>有关使用REST实施此功能的指导，请参阅[以客户身份登录](https://developer.adobe.com/commerce/webapi/rest/saas-integrations/login-as-customer/) REST API文档。

### 向管理员请求一次性代码(OTC)

1. 导航到&#x200B;**[!UICONTROL Customers]**&#x200B;并选择客户以打开编辑页面。

1. 在“编辑客户”页面上，单击&#x200B;**[!UICONTROL Get Customer Login OTC]**。

   在“编辑客户”页面上![获取客户登录OTC按钮](assets/get-customer-login-otc-button.png){width="600" zoomable="yes"}

1. 输入&#x200B;**[!UICONTROL Reason]**（必需）并单击&#x200B;**[!UICONTROL Request]**。

   ![包含原因字段的OTC请求模式](assets/otc-reason-modal.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >**原因**&#x200B;字段为必填项。 此变量将传递到OTP生成流程，并保留用于即将推出的审核和事件日志记录功能。

1. 生成的OTC将显示在模态中。 将此代码与`generateCustomerToken`或`exchangeOtpForCustomerToken`GraphQL突变一起使用，以获得客户授权。

   ![生成的OTC显示在模式窗口中](assets/otc-generated-code.png){width="300" zoomable="yes"}

>[!IMPORTANT]
>
>默认情况下，生成的一次性代码OTC的有效期为30秒，并且在一次使用后失效。 可以通过提交[支持票证](https://experienceleague.adobe.com/home?support-tab=home#support)来配置TTL。

生成一次性代码后，您可以通过导航到店面并使用以下凭据登录来使用该代码：

* **电子邮件**：客户的电子邮件地址
* **密码**：生成的一次性代码(OTC)

>[!ENDTABS]

## 使用客户身份登录

>[!INFO]
>
>若要使用&#x200B;_Login作为客户_，请确保按照前面所述配置您的管理员。

_以客户身份登录_&#x200B;允许您查看站点（与客户一样），并允许您为客户排除故障和执行其他操作。 如果您分配了具有所需权限的用户角色：

1. 您可以在上一部分中列出的页面上单击&#x200B;**[!UICONTROL Login as Customer]**。
1. “作为客户登录”操作在“操作报表”中可用。

>[!WARNING]
>
>以客户&#x200B;[!UICONTROL _身份登录_]&#x200B;时执行的任何操作（如添加/删除产品）均应用于实际客户的订单。 在店面，当您`logged in as customer_name`时会显示一个横幅以提供特殊状态提醒。

## 以客户日志记录身份登录

{{ee-feature}}

Adobe Commerce为&#x200B;_作为客户登录_&#x200B;操作提供日志记录。 它列出了管理员用户访问功能的所有会话。 要访问记录的操作，请转到[管理员操作报表](../systems/action-log-report.md)。

您可以过滤页面顶部的报表设置&#x200B;**[!UICONTROL Action Group]**&#x200B;至`Login As Customer`，然后单击&#x200B;**[!UICONTROL Search]**。

![筛选操作报告](assets/customers-login-as-customer-log-filter.png){width="700" zoomable="yes"}

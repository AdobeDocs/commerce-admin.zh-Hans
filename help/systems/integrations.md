---
title: 集成
description: 了解如何为第三方集成配置OAuth凭据和重定向URL。
exl-id: b7632994-b07b-4cdb-b62c-79bc7a3a01c8
role: Admin, Developer
feature: System, Integration, Configuration
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '521'
ht-degree: 0%

---

# 集成

在商务管理员中定义集成，会为第三方集成建立OAuth凭据和重定向URL的位置，并标识集成所需的可用API资源。 有关集成注册过程的详细信息，请参阅 [基于OAuth的身份验证](https://developer.adobe.com/commerce/webapi/get-started/authentication/gs-authentication-oauth/) 在Commerce开发人员文档中。

![集成](./assets/integrations.png){width="700" zoomable="yes"}

## 载入工作流

1. **授权集成**  — 转到 **[!UICONTROL System]** > _[!UICONTROL Extensions]_>**[!UICONTROL Integrations]**页面中，找到相关的集成，然后进行授权。
1. **验证并建立登录**  — 出现提示时，接受请求的访问。 如果重定向到第三方，请登录到系统或创建帐户。 成功登录后，您将返回到集成页面。
1. **接收授权集成的确认**  — 系统会发送通知，告知集成已成功授权。 设置集成并接收凭据后，不再需要调用访问或请求令牌。

## 添加集成

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL System]** > _[!UICONTROL Extensions]_>**[!UICONTROL Integrations]**.

   ![新集成](./assets/integration-new.png){width="600" zoomable="yes"}

1. 输入以下集成信息：

   - 输入 **[!UICONTROL Name]** 集成和联系人的 **[!UICONTROL Email]** 地址。

   - 输入 **[!UICONTROL Callback URL]** 其中，当使用OAuth进行令牌交换时，可以发送OAuth凭据。 使用 `https://` 强烈建议。

   - 输入 **[!UICONTROL Identity Link URL]** 使用这些Adobe Commerce或Magento Open Source集成凭据将用户重定向到第三方帐户。

   >[!NOTE]
   >
   > 此 `Integration not secure` 警告标签显示在上的每个集成名称附近 [!UICONTROL Integrations] 提醒网格，直到将HTTPS URL保存到 [!UICONTROL Callback URL] 和 [!UICONTROL Identity Link URL] 字段。

   - 出现提示时，输入密码以确认您的身份。

1. 在左侧面板中，选择 **[!UICONTROL API]** 并执行以下操作：

   - 设置 **[!UICONTROL Resource Access]** 更改为以下任一项：

      - `All`
      - `Custom`

   - 对于自定义访问，请选中所需每个资源的复选框。

     ![集成 — 可用API](./assets/integrations-available-api.png){width="600" zoomable="yes"}

1. 完成后，单击 **[!UICONTROL Save]**.

## 激活集成

默认情况下，保存的集成会显示在网格上，其中包含 `Inactive` 状态。 要激活它，请完成以下步骤：

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL System]** > _[!UICONTROL Extensions]_>**[!UICONTROL Integrations]**.

1. 找到新创建的集成，然后单击 **[!UICONTROL Activate]** 链接。

1. 在右上角，单击 **[!UICONTROL Allow]**.

   此操作显示扩展的集成令牌。 将此信息复制到安全的加密位置，以便与集成一起使用。

   ![扩展的集成令牌](./assets/integration-tokens-for-extensions.png){width="600" zoomable="yes"}

1. 在右上角，单击 **[!UICONTROL Done]**.

## 重新授权集成

要生成新的集成访问令牌和访问令牌密码，请从管理员重新授权集成：

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL System]** > _[!UICONTROL Extensions]_>**[!UICONTROL Integrations]**.

1. 查找与的集成 **[!UICONTROL Active]** 状态。

1. 在 _[!UICONTROL Activate]_列中，单击&#x200B;**[!UICONTROL Reauthorize]**.

1. 单击 **[!UICONTROL Reauthorize]** 批准对API资源的访问。

1. 保存扩展的新集成令牌，然后单击 **[!UICONTROL Done]**.

## 更改API来宾访问安全设置

默认情况下，系统不允许匿名访客访问CMS、目录和其他存储资源。 如果必须更改设置，请执行以下操作：

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左侧面板中，展开 **[!UICONTROL Services]** 并选择 **[!UICONTROL Magento Web API]**.

1. 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL Web API Security Setting]** 部分。

   ![服务配置 — Web API安全设置](../configuration-reference/services/assets/web-api-security.png){width="600" zoomable="yes"}

1. 设置 **[!UICONTROL Allow Anonymous Guest Access]** 到 `Yes`.

1. 完成后，单击 **[!UICONTROL Save Config]**.

有关其他信息，请参阅 [限制对匿名Web API的访问](https://developer.adobe.com/commerce/webapi/rest/use-rest/anonymous-api-security/) 在Commerce开发人员文档中。

## 删除集成

1. 在 _管理员_ 侧栏，转到 **[!UICONTROL System]** > _[!UICONTROL Extensions]_>**[!UICONTROL Integrations]**.

1. 找到现有集成，然后单击图标( ![垃圾桶图标](../assets/icon-delete-trashcan-solid.png) ) **[!UICONTROL Delete]** 列。

1. 要确认您的操作，请单击 **[!UICONTROL OK]**.

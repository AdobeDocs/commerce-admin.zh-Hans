---
title: 安全扫描
description: 了解如何运行增强的安全扫描并监控每个Adobe Commerce和Magento Open Source站点。
exl-id: 87d4739f-496c-4e47-89a3-70d3969c0fdb
role: Admin
feature: Security, Site Management, Reporting
source-git-commit: fa3931d4aaa5e7b903a17ec074703d2c8130c71d
workflow-type: tm+mt
source-wordcount: '1183'
ht-degree: 0%

---


# 安全扫描

Adobe Commerce安全扫描工具可为Adobe Commerce和Magento Open Source站点提供免费的安全监控。 该工具作为基于Web的服务运行，您可以通过位于[account.magento.com](https://account.magento.com/customer/account/login)的Adobe Commerce在线帐户访问它。

![安全扫描工具](./assets/magento-security-scan.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Adobe免费提供此服务，但商家必须接受相关条款，根据扫描结果和站点配置限制Adobe的责任。

## 扫描覆盖范围

安全扫描工具可跨HTTP和HTTPS协议运行，以检测恶意软件、识别安全漏洞并帮助您保持存储的安全状态。 该工具适用于所有商家、开发人员和负责站点安全的指定人员。

安全扫描工具提供全面的安全监控功能，帮助您维护安全存储环境：

- 让insight了解您商店的实时安全状态。
- 接收基于最佳实践的建议，以帮助解决问题。
- 安排每周、每天或按需运行安全扫描。
- 运行21,000多项安全测试，帮助识别潜在的恶意软件。
- 访问跟踪和监控站点进度的历史安全报告。
- 访问显示成功和失败检查以及任何建议操作的扫描报告。

>[!NOTE]
>
>不能从Adobe Commerce的安全扫描工具扫描中排除特定的安全测试。 但是，如果适用，您可以在[中自助忽略失败](#manage-scan-failures)作为误报。

## 访问

安全扫描工具维护严格的访问控制以保护您的站点信息。 只有您可以扫描网站，因为该工具要求通过Adobe Commerce帐户验证域所有权。 每个网站都通过唯一的令牌连接到您的帐户，以防止第三方进行未经授权的扫描。

该工具专门针对Adobe Commerce域及其安全漏洞。 虽然您的网络商店可能包含来自其他平台的页面，但安全扫描工具应仅扫描Adobe Commerce生成的内容，以确保获得可靠的结果。 扫描非Adobe Commerce页面可能会产生不可靠的漏洞评估。

## 运行扫描

扫描过程会针对已知安全问题检查您的站点，并识别可能使存储易受攻击的缺失Adobe Commerce修补程序和更新。

>[!TIP]
>
>对于云基础架构项目上的Commerce，请参阅[设置安全扫描工具](https://experienceleague.adobe.com/zh-hans/docs/commerce-on-cloud/user-guide/launch/overview#set-up-the-security-scan-tool)。

要运行扫描，请执行以下操作：

1. 从Commerce主页登录到您的[Commerce/Magento帐户](../getting-started/commerce-account-create.md)。

1. 查看并接受使用安全扫描工具的条款。

   1. 在左侧面板中，选择&#x200B;**[!UICONTROL Security Scan]**。
   1. 单击&#x200B;**[!UICONTROL Go to Security Scan]**。
   1. 阅读&#x200B;**[!UICONTROL Terms and Conditions]**。
   1. 单击&#x200B;**[!UICONTROL Agree]**&#x200B;继续。

1. 在&#x200B;_[!UICONTROL Monitored Websites]_&#x200B;页面上，单击&#x200B;**[!UICONTROL +Add Site]**。

   如果您有多个具有不同域的站点，请为每个域配置单独的扫描。

   ![受监视的站点](./assets/monitored-website.png){width="600" zoomable="yes"}

1. 要通过添加确认代码来验证您对网站域的所有权，请执行以下操作之一：

   **Commerce店面**：

   1. 输入&#x200B;**[!UICONTROL Site URL]**&#x200B;和&#x200B;**[!UICONTROL Site Name]**。
   1. 单击&#x200B;**[!UICONTROL Generate Confirmation Code]**。
   1. 单击&#x200B;**复制**&#x200B;以将确认代码复制到剪贴板。

      ![生成确认码](./assets/scan-site1.png){width="400" zoomable="yes"}

   1. 以具有完全管理员权限的用户身份登录到存储的管理员，并执行以下操作：

      1. 在&#x200B;_管理员_&#x200B;侧边栏中，转到&#x200B;**[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**。
      1. 在列表中找到您的网站，然后单击&#x200B;**[!UICONTROL Edit]**。
      1. 展开&#x200B;**[!UICONTROL HTML Head]**&#x200B;部分的![扩展选择器](../assets/icon-display-expand.png)。
      1. 向下滚动到&#x200B;**[!UICONTROL Scripts and Style Sheets]**&#x200B;并单击任何现有代码末尾的文本框。 将确认代码粘贴到文本框中。

         ![脚本和样式表](./assets/scan-paste-code.png){width="600" zoomable="yes"}

      1. 完成后，单击&#x200B;**[!UICONTROL Save Configuration]**。

   **PWA店面**：

   1. 输入&#x200B;**[!UICONTROL Site URL]**&#x200B;和&#x200B;**[!UICONTROL Site Name]**。

   1. 对于&#x200B;**[!UICONTROL Confirmation Code]**，请选择`META Tag`选项，然后单击&#x200B;**[!UICONTROL Generate Code]**。

   1. 单击&#x200B;**[!UICONTROL Copy]**&#x200B;以将生成的确认代码META标记复制到剪贴板。

      ![生成确认码](./assets/scan-site2.png){width="400" zoomable="yes"}

   1. 转到PWA Studio storefront项目目录并执行以下操作：

      1. 在PWA Studio项目目录下，转到`packages > venia-concept > template.html`。
      1. 将复制的确认代码（生成的META标记）添加到HTML标题并保存更改。

         ![复制确认码](./assets/code-pwa.png){width="600" zoomable="yes"}

      1. 返回到PWA Studio CLI，然后使用yarn安装项目依赖项并运行项目构建命令。

         ```sh
         yarn install &&
         yarn build
         ```

      1. *在您的云项目*&#x200B;中，创建一个`pwa`文件夹，并复制店面项目的`dist`文件夹中的内容。

         ```sh
         mkdir pwa && cp -r <path to your storefront project>/dist/* pwa
         ```

      1. 使用Git CLI工具来暂存、提交这些更改，并将其推送到您的云项目。

         ```sh
         git add . &&
         git commit -m "Added storefront file bundles" &&
         git push origin
         ```

         构建过程完成后，更改将部署到您的PWA商店前面。

1. 返回到Commerce帐户中的&#x200B;_[!UICONTROL Security Scan]_&#x200B;页面，然后单击&#x200B;**[!UICONTROL Verify Confirmation Code]**&#x200B;以建立域的所有权。

1. 成功确认后，为以下类型之一配置&#x200B;**[!UICONTROL Set Automatic Security Scan]**&#x200B;选项：

   **每周扫描（推荐）**：

   选择每周进行扫描的&#x200B;**[!UICONTROL Week Day]**、**[!UICONTROL Time]**&#x200B;和&#x200B;**[!UICONTROL Time Zone]**。

   默认情况下，扫描计划从每周的星期六午夜(UTC)开始，并持续到星期日。

   ![每周扫描](./assets/scan-weekly.png){width="500" zoomable="yes"}

   **每日扫描**：

   选择每天进行扫描的&#x200B;**[!UICONTROL Time]**&#x200B;和&#x200B;**[!UICONTROL Time Zone]**。

   默认情况下，扫描计划于每天午夜(UTC)开始。

   ![每日扫描](./assets/scan-daily.png){width="500" zoomable="yes"}

1. 输入要接收已完成扫描和安全更新通知的&#x200B;**[!UICONTROL Email Address]**。

   ![电子邮件地址](./assets/scan-notification-email.png){width="400" zoomable="yes"}

1. 完成后，单击&#x200B;**[!UICONTROL Submit]**。

   验证域的所有权后，该站点将显示在Commerce帐户的“受监控网站”列表中。

1. 如果您有多个网站使用不同的域，请重复此过程为每个网站设置安全扫描。

## 管理扫描失败

安全扫描工具允许您直接从报告视图管理扫描失败。 您可以将特定的扫描失败标记为误报，并将其从风险分数中排除。

### 管理扫描失败的好处

管理扫描故障可通过以下方式帮助您维护存储区更准确的安全概述：

- 减少安全报表中的误报。
- 关注需要注意的相关安全问题。
- 保持更清楚地了解您商店的真实安全状态。
- 无需联系支持人员来查找已知误报。
- 通过自行管理您已经调查的扫描故障来节省时间。

您可能希望将扫描失败标记为误报的常见情况包括：

- 应用了扫描工具未检测到的安全修补程序后。
- 当检测到的问题不适用于您的特定商店配置时。
- 当您实施了替代安全措施来解决问题时。
- 当扫描失败基于您特意为业务需求设置的配置时。

### 忽略扫描失败

要管理已识别为误报的扫描失败，请执行以下步骤：

1. 从&#x200B;_[!UICONTROL Monitored Websites]_&#x200B;页面，单击要管理的站点的&#x200B;**[!UICONTROL View Report]**。

1. 在报表视图中，找到要标记为误报的失败扫描。

1. 单击&#x200B;**[!UICONTROL Ignore]**&#x200B;查看特定的扫描失败。

   ![忽略扫描失败](assets/security-scan-ignore-failure.png){width="600" zoomable="yes"}

1. 单击&#x200B;**[!UICONTROL Apply Changes]**&#x200B;保存您的选择。

忽略的扫描失败将移至&#x200B;_[!UICONTROL Ignored Results]_&#x200B;部分，并从风险分数中排除。

### 停止忽略扫描失败

如果需要将以前忽略的扫描故障恢复到活动监视状态，请执行以下步骤：

1. 在报表视图中，滚动到&#x200B;_[!UICONTROL Ignored Results]_&#x200B;部分。

1. 对于要恢复的扫描失败，单击&#x200B;**[!UICONTROL Stop Ignoring]**。

   ![取消忽略扫描失败](assets/security-scan-stop-ignoring-failure.png){width="600" zoomable="yes"}

1. 单击&#x200B;**[!UICONTROL Apply Changes]**&#x200B;保存您的选择。

扫描失败将移回到&#x200B;_[!UICONTROL Failed Scans]_&#x200B;部分，并包含在您的风险分数中。

### 查看忽略的扫描失败

忽略的结果显示在报告的单独部分中，并且风险分数会自动更新以仅反映活动扫描失败。 在应用更改之前，通过选择多个项目，可以一次管理多个扫描失败。

![查看忽略的扫描失败](assets/security-scan-view-ignored-failures.png){width="600" zoomable="yes"}

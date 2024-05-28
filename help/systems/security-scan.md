---
title: 安全扫描
description: 了解如何运行增强的安全扫描并监控每个Adobe Commerce和Magento Open Source站点。
exl-id: 87d4739f-496c-4e47-89a3-70d3969c0fdb
role: Admin
feature: Security, Site Management, Reporting
source-git-commit: 1f3173d17cc43227f7d44637f1ef0b62606cd0fd
workflow-type: tm+mt
source-wordcount: '614'
ht-degree: 0%

---

# 安全扫描

增强的安全扫描允许您监视每个Adobe Commerce和Magento Open Source站点(包括PWA)，以了解已知的安全风险和恶意软件，并接收修补程序更新和安全通知。

- 深入了解存储区的实时安全状态。
- 接收基于最佳实践的建议，以帮助解决问题。
- 安排每周、每天或按需运行安全扫描。
- 运行21,000多项安全测试，帮助识别潜在的恶意软件。
- 访问跟踪和监控站点进度的历史安全报告。
- 访问显示成功和失败检查以及任何建议操作的扫描报告。

安全扫描工具可从的仪表板中免费使用 [Commerce/Magento帐户](../getting-started/commerce-account-create.md). 有关技术信息，请参阅 [设置安全扫描工具](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/launch/overview.html#set-up-the-security-scan-tool) 在 _《云基础架构上的Commerce指南》_.

![安全扫描工具](./assets/magento-security-scan.png){width="600" zoomable="yes"}

## 运行安全扫描

1. 从Commerce主页，登录到您的 [Commerce/Magento帐户](../getting-started/commerce-account-create.md).

1. 查看并接受使用安全扫描工具的条款。

   - 在左侧面板中，选择 **[!UICONTROL Security Scan]**.
   - 单击 **[!UICONTROL Go to Security Scan]**.
   - 阅读 **[!UICONTROL Terms and Conditions]**.
   - 单击 **[!UICONTROL Agree]** 以继续。

1. 在 _[!UICONTROL Monitored Websites]_页面，单击&#x200B;**[!UICONTROL +Add Site]**.

   如果您有多个具有不同域的站点，请为每个域配置单独的扫描。

   ![受监视的站点](./assets/monitored-website.png){width="600" zoomable="yes"}

1. 要通过添加确认代码来验证您对网站域的所有权，请执行以下操作之一：

   **Commerce店面**：

   - 输入 **[!UICONTROL Site URL]** 和 **[!UICONTROL Site Name]**.
   - 单击 **[!UICONTROL Generate Confirmation Code]**.
   - 单击 **复制** 以将确认代码复制到剪贴板。

     ![生成确认代码](./assets/scan-site1.png){width="400" zoomable="yes"}

   - 以具有完全管理员权限的用户身份登录到存储的管理员，并执行以下操作：

      - 在 _管理员_ 侧栏，转到 **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.
      - 在列表中找到您的网站，然后单击 **[!UICONTROL Edit]**.
      - 展开 ![扩展选择器](../assets/icon-display-expand.png) 该 **[!UICONTROL HTML Head]** 部分。
      - 向下滚动到 **[!UICONTROL Scripts and Style Sheets]** ，然后单击任何现有代码末尾的文本框，并将确认代码粘贴到文本框中。

        ![脚本和样式表](./assets/scan-paste-code.png){width="600" zoomable="yes"}

      - 完成后，单击 **[!UICONTROL Save Configuration]**.

   **PWA店面**：

   - 输入 **[!UICONTROL Site URL]** 和 **[!UICONTROL Site Name]**.

   - 对象 **[!UICONTROL Confirmation Code]**，选择 `META Tag` 选项，然后单击 **[!UICONTROL Generate Code]**.

   - 单击 **[!UICONTROL Copy]** 将生成的确认代码META标记复制到剪贴板。

     ![生成确认代码](./assets/scan-site2.png){width="400" zoomable="yes"}

   - 转到PWA Studio店面项目目录并执行以下操作：

      - 在PWA Studio项目目录下，转到 `packages > venia-concept > template.html`.
      - 将复制的确认代码（生成的META标签）添加到HTML标题并保存更改。

        ![复制确认代码](./assets/code-pwa.png){width="600" zoomable="yes"}

      - 返回PWA StudioCLI，使用yarn安装项目依赖项并运行项目构建命令。

        ```sh
        yarn install &&
        yarn build
        ```

      - *在您的云项目中*，创建 `pwa` 文件夹并复制店面项目的 `dist` 文件夹。

        ```sh
        mkdir pwa && cp -r <path to your storefront project>/dist/* pwa
        ```

      - 使用Git CLI工具来暂存、提交这些更改，并将其推送到您的云项目。

        ```sh
        git add . &&
        git commit -m "Added storefront file bundles" &&
        git push origin
        ```

        构建过程完成后，更改将部署到您的PWA存储前面。

1. 返回到 _[!UICONTROL Security Scan]_Commerce页面，然后单击&#x200B;**[!UICONTROL Verify Confirmation Code]**建立域的所有权。

1. 成功确认后，配置 **[!UICONTROL Set Automatic Security Scan]** 下列类型之一的选项：

   **每周扫描（推荐）**：

   - 选择 **[!UICONTROL Week Day]**， **[!UICONTROL Time]**、和 **[!UICONTROL Time Zone]** 每周进行一次扫描。
   - 默认情况下，扫描计划从每周的星期六午夜(UTC)开始，并持续到星期日。

     ![每周扫描](./assets/scan-weekly.png){width="500" zoomable="yes"}

   **每日扫描**：

   - 选择 **[!UICONTROL Time]**、和 **[!UICONTROL Time Zone]** 每天都会进行扫描。
   - 默认情况下，扫描计划于每天午夜(UTC)开始。

     ![每日扫描](./assets/scan-daily.png){width="500" zoomable="yes"}

1. 输入 **[!UICONTROL Email Address]** 您希望接收已完成扫描和安全更新的通知。

   ![电子邮件地址](./assets/scan-notification-email.png){width="400" zoomable="yes"}

1. 完成后，单击 **[!UICONTROL Submit]**.

   验证域的所有权后，该站点将显示在Commerce帐户的“受监控网站”列表中。

1. 如果您有多个网站使用不同的域，请重复此过程为每个网站设置安全扫描。

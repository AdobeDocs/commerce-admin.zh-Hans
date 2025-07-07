---
title: 加密密钥
description: 了解如何更改您自己的加密密钥，应该定期更改以提高安全性。
exl-id: 78190afb-3ca6-4bed-9efb-8caba0d62078
role: Admin
feature: System, Security
badgePaas: label="仅限PaaS" type="Informative" url="https://experienceleague.adobe.com/zh-hans/docs/commerce/user-guides/product-solutions" tooltip="仅适用于云项目(Adobe管理的PaaS基础架构)和内部部署项目上的Adobe Commerce 。"
source-git-commit: 256517ebbbd6e28eb027f26c7f0a43001f5d7904
workflow-type: tm+mt
source-wordcount: '460'
ht-degree: 0%

---

# 加密密钥

>[!NOTE]
>
>如果您尝试完成这些步骤但遇到问题，请参阅[加密密钥轮换疑难解答： CVE-2024-34102](https://experienceleague.adobe.com/zh-hans/docs/commerce-knowledge-base/kb/troubleshooting/known-issues-patches-attached/troubleshooting-encryption-key-rotation-cve-2024-34102)知识库文章。

Adobe Commerce和Magento Open Source使用加密密钥保护密码和其他敏感数据。 行业标准[!DNL ChaCha20-Poly1305]算法与256位密钥一起使用，以加密所有需要加密的数据。 这包括信用卡数据和集成（支付和配送模块）密码。 此外，使用强安全哈希算法(SHA-256)来哈希所有不需要解密的数据。

在初始安装期间，系统会提示您允许Commerce生成加密密钥，或输入自己的密钥。 加密密钥工具允许您根据需要更改密钥。 应定期更改加密密钥以提高安全性，并且随时可能危及原始密钥。

有关技术信息，请参阅[安装指南](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/advanced.html?lang=zh-Hans)中的&#x200B;_高级内部部署_&#x200B;和[PHP开发人员指南](https://developer.adobe.com/commerce/php/development/security/data-encryption/)中的&#x200B;_数据重新加密_。

>[!IMPORTANT]
>
>- 在按照这些说明更改加密密钥之前，请确保以下文件可写： `[your store]/app/etc/env.php`
>- 管理员设置中的加密密钥更改功能已弃用，已在2.4.8中移除。升级到2.4.8后，您必须使用本页中所述的CLI命令更改加密密钥。
>- 轮换加密密钥将立即使所有客户和管理会话（不包括集成用户）失效，并且需要他们再次登录。

**要更改加密密钥：**

下面的说明需要访问终端。

1. 启用[维护模式](https://experienceleague.adobe.com/zh-hans/docs/commerce-operations/configuration-guide/setup/application-modes#maintenance-mode)。

   ```bash
   bin/magento maintenance:enable
   ```

1. 禁用cron作业。

   _云基础架构项目：_

   ```bash
   ./vendor/bin/ece-tools cron:disable
   ```

   _内部部署项目_

   ```bash
   crontab -e
   ```

1. 使用以下方法之一更改加密密钥。

   +++CLI命令

   运行以下CLI命令，并确保其完成时没有出现错误。 如果需要重新加密某些系统配置值或付款字段，请参阅[PHP开发指南](https://developer.adobe.com/commerce/php/development/security/data-encryption/)中有关重新加密&#x200B;_的详细_&#x200B;指南。

   ```bash
   bin/magento encryption:key:change
   ```

   +++

   +++管理员设置

   >[!IMPORTANT]
   >
   >此功能已被弃用，在2.4.8中已移除。Adobe建议使用CLI更改加密密钥。

   1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL System]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Manage Encryption Key]**。

      ![系统加密密钥](./assets/encryption-key.png){width="700" zoomable="yes"}

   1. 执行以下操作之一：

      - 要生成新密钥，请将&#x200B;**[!UICONTROL Auto-generate Key]**&#x200B;设置为`Yes`。
      - 若要使用其他键，请将&#x200B;**[!UICONTROL Auto-generate Key]**&#x200B;设置为`No`。 然后在&#x200B;**[!UICONTROL New Key]**&#x200B;字段中，输入或粘贴要使用的密钥。

   1. 单击&#x200B;**[!UICONTROL Change Encryption Key]**。

      >[!NOTE]
      >
      >将新密钥的记录保存在安全位置。 如果文件发生任何问题，则需要解密数据。

   +++

1. 刷新缓存。

   _云基础架构项目：_

   ```bash
   magento-cloud cc
   ```

   _内部部署项目：_

   ```bash
   bin/magento cache:flush
   ```

1. 启用cron作业。

   _云基础架构项目：_

   ```bash
   ./vendor/bin/ece-tools cron:enable
   ```

   _内部部署项目：_

   ```bash
   crontab -e
   ```

1. 禁用维护模式。

   ```bash
   bin/magento maintenance:disable
   ```

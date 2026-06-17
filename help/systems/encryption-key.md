---
title: 加密密钥
description: 了解如何更改您自己的加密密钥，应该定期更改以提高安全性。
exl-id: 78190afb-3ca6-4bed-9efb-8caba0d62078
role: Admin
feature: System, Security
badgePaas: label="仅限PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="仅适用于云项目（Adobe管理的PaaS基础架构）和内部部署项目上的Adobe Commerce 。"
TQID: https://experienceleague.adobe.com/jC0eV49rzff4ZZ0idMG4ChWZh80Yz43ZTmZ9CjYFhnk
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: ba9e5be9-7de1-4f71-a5d2-baead0e425eeid: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: c1579802-ddd4-4214-8a91-97b2066abe11id: d095671a-1355-40aa-8b5f-06c33c68080bid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 545
ht-degree: 0%

---

# 加密密钥

>[!NOTE]
>
>如果您尝试完成这些步骤但遇到问题，请参阅[加密密钥轮换疑难解答： CVE-2024-34102](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/troubleshooting/known-issues-patches-attached/troubleshooting-encryption-key-rotation-cve-2024-34102)知识库文章。

Adobe Commerce和Magento Open Source使用加密密钥保护密码和其他敏感数据。 行业标准[!DNL ChaCha20-Poly1305]算法与256位密钥一起使用，以加密所有需要加密的数据。 这包括信用卡数据和集成（支付和配送模块）密码。 此外，使用强安全哈希算法(SHA-256)来哈希所有不需要解密的数据。

在初始安装期间，系统会提示您允许Commerce生成加密密钥，或输入自己的密钥。 加密密钥工具允许您根据需要更改密钥。 应定期更改加密密钥以提高安全性，并且随时可能危及原始密钥。

有关技术信息，请参阅&#x200B;_安装指南_&#x200B;中的[高级内部部署](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/advanced.html)和&#x200B;_PHP开发人员指南_&#x200B;中的[数据重新加密](https://developer.adobe.com/commerce/php/development/security/data-encryption/)。

>[!IMPORTANT]
>
>- 在按照这些说明更改加密密钥之前，请确保以下文件可写： `[your store]/app/etc/env.php`
>- 管理员设置中的加密密钥更改功能已弃用，已在2.4.8中移除。 升级到2.4.8后，您必须使用本页中所述的CLI命令更改加密密钥。
>- 轮换加密密钥将立即使所有客户和管理会话（不包括集成用户）失效，并且需要他们再次登录。

**要更改加密密钥：**

下面的说明需要访问终端。

1. 启用[维护模式](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/setup/application-modes#maintenance-mode)。

   ```bash
   bin/magento maintenance:enable
   ```

1. 禁用cron作业。

   云基础结构项目&#x200B;:_(_C)

   ```bash
   ./vendor/bin/ece-tools cron:disable
   ```

   _内部部署项目_

   ```bash
   crontab -e
   ```

1. 使用以下方法之一更改加密密钥。

   +++CLI命令

   确认新命令存在：

   ```bash
   bin/magento list | grep encryption:key:change
   ```

   您应该会看到以下输出：

   ```bash
   encryption:key:change Change the encryption key inside the env.php file.
   ```

   如果看到此输出，请运行以下CLI命令，并确保它完成时没有出现错误。 如果需要重新加密某些系统配置值或付款字段，请参阅&#x200B;_PHP开发指南_&#x200B;中有关重新加密](https://developer.adobe.com/commerce/php/development/security/data-encryption/)的详细[指南。

   ```bash
   bin/magento encryption:key:change
   ```

   +++

   +++管理员设置

   >[!IMPORTANT]
   >
   >此功能已被弃用，在2.4.8中已移除。 Adobe建议使用CLI更改加密密钥。

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

   云基础结构项目&#x200B;:_(_C)

   ```bash
   magento-cloud cc
   ```

   内部部署项目(_O):_

   ```bash
   bin/magento cache:flush
   ```

1. 启用cron作业。

   云基础结构项目&#x200B;:_(_C)

   ```bash
   ./vendor/bin/ece-tools cron:enable
   ```

   内部部署项目(_O):_

   ```bash
   crontab -e
   ```

1. 禁用维护模式。

   ```bash
   bin/magento maintenance:disable
   ```

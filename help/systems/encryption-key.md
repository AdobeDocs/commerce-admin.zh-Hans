---
title: 加密密钥
description: 了解如何自动生成或添加您自己的加密密钥，应定期更改这些密钥以提高安全性。
exl-id: 78190afb-3ca6-4bed-9efb-8caba0d62078
role: Admin
feature: System, Security
source-git-commit: 21be3c7a56cb72d685b2b3605bc27266e8e55f37
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%

---

# 加密密钥

Adobe Commerce和Magento Open Source使用加密密钥保护密码和其他敏感数据。 行业标准[!DNL ChaCha20-Poly1305]算法与256位密钥一起使用，以加密所有需要加密的数据。 这包括信用卡数据和集成（支付和配送模块）密码。 此外，使用强安全哈希算法(SHA-256)来哈希所有不需要解密的数据。

在初始安装期间，系统会提示您允许Commerce生成加密密钥，或输入自己的密钥。 加密密钥工具允许您根据需要更改密钥。 应定期更改加密密钥以提高安全性，并且随时可能危及原始密钥。 无论何时更改键，都会使用新键对所有旧数据重新编码。

有关技术信息，请参阅&#x200B;_安装指南_&#x200B;中的[高级内部部署](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/advanced.html)。

## 步骤1：使文件可写

要更改加密密钥，请确保以下文件可写： `[your store]/app/etc/env.php`

## 步骤2：更改加密密钥

1. 在&#x200B;_管理员_&#x200B;侧边栏上，转到&#x200B;**[!UICONTROL System]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Manage Encryption Key]**。

   ![系统加密密钥](./assets/encryption-key.png){width="700" zoomable="yes"}

1. 执行以下操作之一：

   - 要生成新密钥，请将&#x200B;**[!UICONTROL Auto-generate Key]**&#x200B;设置为`Yes`。
   - 若要使用其他键，请将&#x200B;**[!UICONTROL Auto-generate Key]**&#x200B;设置为`No`。 然后在&#x200B;**[!UICONTROL New Key]**&#x200B;字段中，输入或粘贴要使用的密钥。

1. 单击&#x200B;**[!UICONTROL Change Encryption Key]**。

1. 将新密钥的记录保存在安全位置。

   如果文件发生任何问题，则需要解密数据。

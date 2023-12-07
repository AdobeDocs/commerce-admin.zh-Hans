---
title: 安全性
description: 了解可用于保护存储和数据安全的工具，以及在检测到危害时制定安全行动计划的准则。
exl-id: 10eef4ac-de83-4083-9ba3-e42c8eb33781
feature: Security, Site Management
source-git-commit: fede05a413428520eec89d46f41a1cdd9c9c3a2e
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 0%

---

# 安全性

可通过多种方法来保护存储区并维护数据安全：

- 设置 [双重身份验证](security-two-factor-authentication.md)
- 实施 [验证码](security-captcha.md) 或 [reCAPTCHA](security-google-recaptcha.md)
- 设置 [安全扫描](security-scan.md) Adobe Commerce或Magento Open Source安装中的每个域。

>[!NOTE]
>
>已启用存储 [!DNL Adobe Identity Management Services] (IMS)身份验证已禁用本机Adobe Commerce和Magento Open Source2FA。 使用Adobe凭据登录其Commerce实例的管理员用户不需要对许多管理员任务重新进行身份验证。 当管理员用户登录到其当前会话时，身份验证由Adobe IMS处理。 请参阅 [[!DNL Adobe Identity Management Service] (IMS)集成概述](../getting-started/adobe-ims-integration-overview.md).

访问 [安全中心](https://helpx.adobe.com/security.html){：target=&quot;_blank&quot;}以获取有关潜在漏洞的最新消息、注册Adobe安全通知并访问Adobe信任中心。

![安全中心](./assets/product-security-home.png){width="700" zoomable="yes"}

有关安全最佳实践的信息，请参阅 [保护您的Commerce网站和基础架构](https://experienceleague.adobe.com/docs/commerce-operations/implementation-playbook/best-practices/launch/security-best-practices.html) 在 _实施行动手册_.

## 安全行动计划

如果您怀疑您的Adobe Commerce或Magento Open Source站点受到危害，请立即遵循此行动计划。

1. **诊断**：运行扫描以建立Commerce存储的安全状态。 商务 [安全扫描](security-scan.md) 是Adobe提供的免费服务，允许您监控Commerce网站是否存在已知安全风险和恶意软件，并接收安全通知。

1. **清洁**：聘用一名 [合格的顾问](https://solutionpartners.adobe.com/s/directory/?partner_type=1) 或在线服务清除网站上的所有恶意代码。 一些Commerce社区成员建议 [[!DNL Sucuri Website Malware Removal]](https://sucuri.net/website-antivirus/malware-removal). 查看 `/media` 文件夹中的剩余可执行代码。 删除所有未知的管理员用户并重置所有管理员密码。

1. **Protect**：使用最新版本保持Commerce安装处于最新状态。 如果您使用的是旧版本，请在所有安全修补程序可用时应用它们。 审阅并关注 [Commerce安全最佳实践](https://www.adobe.com/content/dam/cc/en/trust-center/ungated/whitepapers/experience-cloud/adobe-commerce-best-practices-guide.pdf). 订阅 [Commerce安全警报](https://www.adobe.com/subscription/adbeSecurityNotifications.html).

1. **报表**：如果您认为已在Commerce中发现特定漏洞， [打开Adobe问题](https://hackerone.com/adobe?type=team) 并包括技术细节。

1. **升级**：为了让您全天候(24/7)支持带来的更多安全感，请计划升级到 [Adobe Commerce关于我们的云架构](https://business.adobe.com/products/magento/cloud-delivery.html) 现在。
